---
tags: [desain, sistem]
status: ✅ final
diperbarui: 2026-11-21
---
# Gambaran Sistem (konseptual)

> Fase ini **belum teknis**: hanya bagian-bagian sistem, tugasnya, dan hubungannya, dalam bahasa sederhana.
> Pilihan bahasa, framework, database, dan arsitektur detail di-breakdown nanti dan dicatat di [[Daftar Keputusan]].
> Dasar: [[PRD]].

## 1. Bagian-bagian utama
| # | Bagian | Tugas | Dipakai oleh |
|---|---|---|---|
| 1 | **Portal Kandidat** | Halaman untuk mendaftar, memeriksa profil, menambah bukti, melihat lowongan, melamar, mengerjakan tes, melihat status | Kandidat |
| 2b | **Dashboard Master** | Halaman untuk menambah perusahaan & mengelola akun HR | Master user |
| 2 | **Dashboard HR** | Halaman untuk membuat lowongan & kriteria, menyusun alur, membuat tes, menilai, memutuskan | HR |
| 3 | **Inti JoBG** | "Otak" aturan bisnis: profil, lowongan, alur, lamaran, penilaian, keputusan. **Semua pintu masuk wajib lewat sini.** | Bagian 1, 2, 6 |
| 4 | **Penyimpanan Data** | Menyimpan data terstruktur (profil, lowongan, lamaran, penilaian, dll.) | Inti JoBG |
| 5 | **Penyimpanan Dokumen** | Menyimpan CV, dokumen bukti, hasil tes | Inti JoBG |
| 6 | **Pintu MCP** | Pintu bagi AI dari luar (mis. Claude) untuk mengakses JoBG atas nama HR | HR (lewat AI) |
| 7 | **Asisten AI internal** | Menyusun profil dari CV, memisahkan klaim vs bukti, menandai ketidaksesuaian, memberi tanda "lihat sekali lagi" | Inti JoBG |
| 8 | **Penjaga Akses** | Login, peran (kandidat / HR / master user), perusahaan, dan aturan data apa yang boleh dilihat siapa | Semua bagian |
| 9 | **Catatan Aktivitas** | Mencatat keputusan HR, saran AI, dan akses lewat MCP | Inti JoBG |
| 10 | **Pemberitahuan** | Memberi kabar ke kandidat (daftar berhasil, lamaran terkirim, status berubah). **MVP: di Portal saja**; email menyusul | Kandidat |

## 2. Hubungan antar bagian
```
   Kandidat              HR                  HR lewat AI luar (Claude)
      │                   │                          │
┌─────▼──────┐     ┌──────▼──────┐            ┌──────▼──────┐
│  Portal    │     │  Dashboard  │            │  Pintu MCP  │
│  Kandidat  │     │     HR      │            │             │
└─────┬──────┘     └──────┬──────┘            └──────┬──────┘
      └───────────────────┼──────────────────────────┘
                          │   (semua lewat Penjaga Akses)
                   ┌──────▼──────┐        ┌───────────────────┐
                   │  Inti JoBG  │◄──────►│ Asisten AI internal│
                   │ (aturan)    │        │ (memberi saran)    │
                   └──┬───────┬──┘        └───────────────────┘
          ┌───────────┘       └───────────┐
   ┌──────▼──────┐   ┌─────────────┐  ┌───▼──────────────┐
   │ Penyimpanan │   │  Catatan    │  │   Penyimpanan    │
   │    Data     │   │  Aktivitas  │  │     Dokumen      │
   └─────────────┘   └─────────────┘  └──────────────────┘
```

### Prinsip
1. **Satu otak, banyak pintu.** Portal, Dashboard, dan Pintu MCP hanyalah pintu. Aturannya hanya ada di Inti JoBG, jadi akses lewat Claude **tidak bisa** melakukan lebih dari yang bisa dilakukan HR di Dashboard.
2. **AI hanya memberi saran.** Asisten AI tidak pernah mengubah keputusan. Hasilnya disimpan sebagai **saran / tanda** yang bisa dilihat & ditelusuri buktinya.
3. **Dokumen kandidat = data.** Isi CV & bukti tidak pernah dianggap sebagai perintah bagi AI.
4. **Semua yang penting tercatat.** Keputusan, saran AI, dan akses MCP masuk Catatan Aktivitas.

## 3. Data utama (konsep)
```
Master user ──< Perusahaan ──< HR (akun dibuat master user)
Perusahaan ──< Lowongan ──< Kriteria (wajib / nilai tambah)
                   │
                   └──< Alur ──< Tahap (seleksi berkas / tes / interview) ── Tes
Kandidat ── Profil ──< Item profil (pendidikan, pengalaman, skill, ...) ──< Bukti
Kandidat ──< Lamaran >── Lowongan
Lamaran ──< Penilaian per tahap ──< Nilai per kriteria (+ bukti / klaim)
Lamaran ──< Keputusan per tahap (+ alasan)
Lamaran ──< Tanda AI ("lihat sekali lagi", ketidaksesuaian)
Perusahaan ──< Blacklist >── Kandidat ──< Banding          (Nanti)
```
`A ──< B` = satu A punya banyak B.

**Status penting:**
| Benda | Status |
|---|---|
| Item profil | 🤖 hasil AI (perlu diperiksa) → ✍️ dikonfirmasi kandidat · 💬 klaim / ✅ terbukti |
| Lowongan | Draf → Dibuka → Ditutup |
| Lamaran | Di tahap X → Lanjut / Tidak lanjut → Diterima / Tidak lanjut (akhir) |
| Tanda AI | Baru → Dilihat HR *(hanya informasi; HR tidak wajib menanggapi)* |

## 4. Alur data penting

### A. Dari CV menjadi profil
```
Kandidat unggah CV → disimpan di Penyimpanan Dokumen
  → Asisten AI menyusun item profil (status: 🤖 perlu diperiksa)
  → Kandidat memeriksa & membetulkan → item jadi ✍️ dikonfirmasi (💬 klaim)
  → Kandidat menambah bukti → Asisten AI memeriksa kecocokan bukti → ✅ terbukti
```

### B. Penilaian & "lihat sekali lagi"
```
Lamaran masuk tahap → Asisten AI menyiapkan ringkasan per kriteria
  (bukti / klaim / ketidaksesuaian; AI tidak memakai data sensitif)
  → HR menilai & memutuskan (+ alasan wajib bila tidak lanjut)
  → Asisten AI membandingkan keputusan dengan kriteria & bukti
  → bila tidak sesuai → Tanda "lihat sekali lagi" (informasi untuk HR)
  → HR boleh meninjau ulang & mengubah keputusan, atau membiarkannya → tercatat
```

### C. HR bertanya lewat Claude (MCP)
```
HR di Claude: "ringkas pelamar Admin Keuangan yang lolos tes"
  → Pintu MCP → Penjaga Akses (masuk sebagai HR tersebut)
  → Inti JoBG (aturan yang sama dengan Dashboard) → data perusahaan HR itu saja
  → jawaban ke Claude → akses tercatat di Catatan Aktivitas
```

## 5. Siapa boleh melihat apa (konsep)
| Data | Kandidat (pemilik) | HR perusahaan yang dilamar | HR perusahaan lain | Master user | AI lewat MCP |
|---|---|---|---|---|---|
| Profil & bukti | ✅ | ✅ setelah melamar | ❌ | ✅ | Sama seperti HR yang login |
| Data ⚠️ sensitif | ✅ | ✅ langsung terlihat setelah kandidat melamar (🔒 bila mode tanpa identitas dinyalakan, Nanti) | ❌ | ✅ | Sama seperti HR yang login |
| Lowongan aktif | ✅ | ✅ | ✅ | ✅ | Sama seperti HR yang login |
| Kriteria penilaian | ✅ sebagai syarat lowongan | ✅ | ❌ | ✅ | Sama seperti HR yang login |
| Alur lengkap lowongan | ❌ hanya tahap saat ini | ✅ | ❌ | ✅ | Sama seperti HR yang login |
| Penilaian & tanda AI | ❌ | ✅ | ❌ | ✅ | Sama seperti HR yang login |
| Alasan blacklist | ✅ (Nanti) | ✅ | ❌ | ✅ | Sama seperti HR yang login |

> **Master user** punya akses penuh ke semua data & aksi. Karena itu **semua aksi master user wajib tercatat** di Catatan Aktivitas.

## 6. Dibahas nanti (breakdown teknis)
- [ ] Pilihan bahasa & framework
- [ ] Arsitektur detail (bagian mana jadi satu, mana terpisah)
- [ ] Desain database
- [ ] Desain API
- [ ] Desain MCP tools
- [ ] Pilihan layanan AI / model
- [ ] Cara login & keamanan

## ❓ Pertanyaan terbuka
- [x] Kandidat melihat kriteria → **boleh**, ditampilkan sebagai syarat lowongan
- [x] Identitas untuk HR → **langsung terlihat**
- [x] Tanda "lihat sekali lagi" → **cukup sebagai informasi**
- [x] Pemberitahuan → **MVP di Portal saja**; nanti email untuk daftar, melamar, perubahan status, dll.
- [x] Konflik identitas vs penilaian tanpa identitas → **(b)** bawaan identitas terlihat; mode tanpa identitas jadi **pilihan per lowongan (Nanti)**; AI tetap tidak memakai data sensitif
