---
tags: [desain, ui]
status: ✅ final
diperbarui: 2026-11-21
---
# Wireframe

> Sketsa **kasar** untuk menunjukkan **isi & susunan** halaman, bukan tampilan akhir (warna, font, ikon diatur di [[Design System]]).
> Halaman inti digambar lengkap; halaman pendukung cukup dijelaskan.
> Dasar: [[User Flow]].

Simbol: `[Tombol]` · `( )` pilihan · `▾` dropdown · `🤖` hasil AI · `✅` terbukti · `💬` klaim · `❌` tidak ada · `⚑` tanda AI

---

## 🎓 Kandidat

### 1. Profil: hasil AI ⭐ (K-1)
Halaman terpenting untuk Raka: **memeriksa, bukan mengisi**.
```
┌──────────────────────────────────────────────────────────┐
│ JoBG                                  🔔  Raka ▾          │
├──────────────────────────────────────────────────────────┤
│ 🤖 Profil Anda sudah disusun dari CV                      │
│ Periksa sebentar. Ubah bila ada yang salah.               │
│ ███████████░░░░  12 dari 15 sudah diperiksa               │
├──────────────────────────────────────────────────────────┤
│ PENDIDIKAN                                                │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ S1 Teknik Informatika · Univ. X · lulus 2026     🤖  │ │
│ │ IPK 3.45                                             │ │
│ │                          [✓ Benar]   [✎ Ubah]        │ │
│ └──────────────────────────────────────────────────────┘ │
│ PENGALAMAN                                                │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Magang Backend · PT A · 3 bulan                  🤖  │ │
│ │                          [✓ Benar]   [✎ Ubah]        │ │
│ └──────────────────────────────────────────────────────┘ │
│ SKILL                                                     │
│ [Go 🤖 ✕] [SQL 🤖 ✕] [REST API 🤖 ✕]  [+ Tambah]          │
│                                                          │
│ [+ Tambah yang belum terbaca dari CV]                    │
├──────────────────────────────────────────────────────────┤
│             [Simpan & lanjutkan nanti]  [Konfirmasi ✓]   │
└──────────────────────────────────────────────────────────┘
```
- Satu tombol **[✓ Benar]** per isian: memeriksa harus lebih cepat daripada mengisi.
- Bila AI gagal membaca CV: pesan + [Unggah ulang] / [Isi manual].

### 2. Profil saya (+ bukti) (K-2)
```
┌──────────────────────────────────────────────────────────┐
│ Profil saya                                   [✎ Ubah]   │
├──────────────────────────────────────────────────────────┤
│ ⓘ 3 data masih 💬 klaim. Tambahkan bukti agar HR lebih    │
│   yakin dengan kemampuan Anda.                            │
├──────────────────────────────────────────────────────────┤
│ PENGALAMAN                                                │
│  Magang Backend · PT A           ✅ terbukti (surat.pdf)   │
│  Proyek: Aplikasi Kasir          💬 klaim  [+ Bukti]       │
│ SKILL                                                     │
│  Go        ✅ (repo GitHub)                               │
│  SQL       💬 klaim  [+ Bukti]                             │
│  REST API  💬 klaim  [+ Bukti]                             │
└──────────────────────────────────────────────────────────┘
  [+ Bukti] → pilih: (•) unggah dokumen  ( ) tempel link
            → 🤖 memeriksa… → ✅ cocok / 💬 tetap klaim + alasan
```

### 3. Daftar lowongan (K-3)
```
┌──────────────────────────────────────────────────────────┐
│ Cari lowongan                                            │
│ Jenis ▾ Kerja/Magang  Sektor ▾  Lokasi ▾  Jenjang ▾      │
├──────────────────────────────────────────────────────────┤
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Backend Developer (Kerja)                            │ │
│ │ PT B · Teknologi · Bandung · S1/D3                   │ │
│ │ Ditutup 30 Des                         [Lihat →]     │ │
│ └──────────────────────────────────────────────────────┘ │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Magang Admin Keuangan (Magang)                       │ │
│ │ PT C · Retail · Jakarta · SMK/D3                     │ │
│ └──────────────────────────────────────────────────────┘ │
└──────────────────────────────────────────────────────────┘
```

### 4. Detail lowongan (K-3)
```
┌──────────────────────────────────────────────────────────┐
│ ← Kembali                                                │
│ Backend Developer · PT B · Bandung · Kerja               │
├──────────────────────────────────────────────────────────┤
│ Deskripsi pekerjaan …                                    │
│                                                          │
│ SYARAT WAJIB                                             │
│  • Jurusan Informatika / Sistem Informasi                │
│  • Menguasai minimal satu bahasa backend                 │
│ NILAI TAMBAH                                             │
│  • Pernah magang / proyek backend                        │
├──────────────────────────────────────────────────────────┤
│                                          [Lamar]         │
└──────────────────────────────────────────────────────────┘
```
- Sudah melamar → tombol menjadi "Sudah dilamar" (nonaktif).

### 5. Lamaran saya (K-4, K-5)
```
┌──────────────────────────────────────────────────────────┐
│ Lamaran saya                                             │
├──────────────────────────────────────────────────────────┤
│ Backend Developer · PT B                                 │
│ Tahap: Tes          Status: 🟡 Menunggu Anda             │
│ Batas waktu: 25 Nov, 23:59              [Kerjakan tes →] │
├──────────────────────────────────────────────────────────┤
│ Magang Data · PT D                                       │
│ Tahap: Seleksi berkas   Status: ⚪ Sedang diproses        │
├──────────────────────────────────────────────────────────┤
│ Staf Admin · PT E                                        │
│ Status: 🔴 Tidak lanjut                                   │
└──────────────────────────────────────────────────────────┘
```
Hanya tahap saat ini yang terlihat, bukan seluruh alur.

### Halaman pendukung (kandidat)
| Halaman | Isi utama |
|---|---|
| Beranda | Penjelasan singkat JoBG + [Daftar] [Masuk] + contoh lowongan terbaru |
| Daftar | Email, HP, sekolah/institusi, minat, jenis (kerja/magang), unggah CV → verifikasi email/HP |
| Masuk | Email + kata sandi |
| Konfirmasi lamaran | Ringkasan profil yang dikirim + lokasi & tanggal siap mulai bila belum ada + [Kirim] |
| Tes | Petunjuk, batas waktu (bila diaktifkan), soal/tugas, [Kirim] |
| Pemberitahuan | Daftar kabar: daftar berhasil, lamaran terkirim, undangan tes, perubahan status |

---

## 🧑‍💼 HR

### 6. Dashboard HR (H-1, H-2)
```
┌──────────────────────────────────────────────────────────┐
│ JoBG · HR · PT B                              Sari ▾      │
├──────────────────────────────────────────────────────────┤
│ Lowongan saya                          [+ Buat lowongan] │
│ ┌──────────────────────────────────────────────────────┐ │
│ │ Backend Developer   🟢 Dibuka   42 pelamar   ⚑ 3     │ │
│ │ Magang Data         🟢 Dibuka   18 pelamar           │ │
│ │ Admin Keuangan      ⚪ Draf                           │ │
│ └──────────────────────────────────────────────────────┘ │
└──────────────────────────────────────────────────────────┘
```
`⚑ 3` = ada 3 tanda "lihat sekali lagi" di lowongan itu.

### 7. Lowongan: kriteria (H-1)
```
┌──────────────────────────────────────────────────────────┐
│ Buat lowongan   ① Info  ② Kriteria  ③ Alur  ④ Pratinjau  │
├──────────────────────────────────────────────────────────┤
│ Tulis kriteria SEBELUM melihat pelamar.                  │
│                                                          │
│ WAJIB (minimal 1)                                        │
│  1. Jurusan Informatika / Sistem Informasi        [✕]    │
│  2. Menguasai minimal satu bahasa backend         [✕]    │
│  [+ Tambah kriteria wajib]                               │
│ NILAI TAMBAH                                             │
│  1. Pernah magang / proyek backend                [✕]    │
│  [+ Tambah nilai tambah]                                 │
├──────────────────────────────────────────────────────────┤
│                         [← Kembali]  [Lanjut: Alur →]    │
└──────────────────────────────────────────────────────────┘
```

### 8. Lowongan: alur (H-1)
```
┌──────────────────────────────────────────────────────────┐
│ Buat lowongan   ① Info  ② Kriteria  ③ Alur  ④ Pratinjau  │
├──────────────────────────────────────────────────────────┤
│ Daftar akun → Melamar            (tetap)                 │
│   ↓                                                      │
│ ┌ 1. Seleksi berkas ─────────────────────── [↑][↓][✕] ┐  │
│ ┌ 2. Tes: Studi kasus API ──── [Atur tes] ─ [↑][↓][✕] ┐  │
│ ┌ 3. Interview User ───────────────────── [↑][↓][✕] ┐  │
│ [+ Tambah tahap ▾ Seleksi berkas / Tes / Interview]      │
│   ↓                                                      │
│ Diterima / Tidak lanjut          (tetap)                 │
├──────────────────────────────────────────────────────────┤
│                     [← Kembali]  [Lanjut: Pratinjau →]   │
└──────────────────────────────────────────────────────────┘
```
[Atur tes] → halaman **Tes: buat** (soal/tugas, batas waktu: ( ) aktif ( ) tidak).

### 9. Pelamar per tahap ⭐ (H-2, H-3)
```
┌──────────────────────────────────────────────────────────┐
│ Backend Developer · 42 pelamar                           │
│ [Seleksi berkas 30] [Tes 8] [Interview 3] [Selesai 1]    │
├──────────────────────────────────────────────────────────┤
│ Nama        Wajib     Bukti      Keputusan               │
│ ──────────────────────────────────────────────────────── │
│ Raka        2/2 ✅    4✅ 1💬    🔴 Tidak lanjut  ⚑       │
│ Dinda       2/2 💬    0✅ 9💬    🟢 Lanjut        ⚑       │
│ Budi        1/2 ✅    2✅ 2💬    ⚪ Belum dinilai          │
│ …                                                        │
└──────────────────────────────────────────────────────────┘
⚑ = "lihat sekali lagi" (keputusan tampak tidak sesuai bukti)
```
- Kolom **Bukti** memisahkan ✅ terbukti dan 💬 klaim, agar isian panjang tidak otomatis terlihat unggul.

### 10. Penilaian kandidat ⭐ (H-2, H-3)
Halaman terpenting untuk Sari: **menilai dari bukti**.
```
┌──────────────────────────────────────────────────────────┐
│ ← Pelamar   Raka · Backend Developer · Seleksi berkas    │
├──────────────────────────────────────────────────────────┤
│ ⚑ LIHAT SEKALI LAGI                                      │
│ Kandidat memenuhi 2/2 kriteria wajib dengan bukti,       │
│ tetapi diputuskan "Tidak lanjut".                        │
├──────────────────────────────────────────────────────────┤
│ KRITERIA                       STATUS   BUKTI            │
│ Wajib: Jurusan Informatika     ✅       transkrip.pdf    │
│ Wajib: Bahasa backend          ✅       repo GitHub (Go) │
│ Tambah: Magang/proyek backend  ✅       surat-magang.pdf │
├──────────────────────────────────────────────────────────┤
│ ⚠ CATATAN AI                                             │
│ • Skill "REST API" belum ada bukti (💬 klaim)            │
├──────────────────────────────────────────────────────────┤
│ Profil lengkap ▸   Hasil tes ▸   Catatan interview ▸     │
├──────────────────────────────────────────────────────────┤
│ Keputusan: ( ) Lanjut  (•) Tidak lanjut                  │
│ Alasan (wajib): [______________________________]         │
│                                          [Simpan]        │
└──────────────────────────────────────────────────────────┘
```
- AI **tidak** memberi skor tunggal; setiap status menunjuk ke bukti.

### Halaman pendukung (HR)
| Halaman | Isi utama |
|---|---|
| Masuk / Atur kata sandi | Dari undangan email master user |
| Lowongan: info | Judul, jenis, sektor, lokasi, jenjang, deskripsi |
| Lowongan: pratinjau | Tampilan lowongan seperti dilihat kandidat + [Buka lowongan] / [Simpan draf] |
| Tes: buat | Soal / tugas, batas waktu (aktif / tidak) |
| Interview | Jadwal, tautan/lokasi, catatan, nilai per kriteria |
| Pengaturan | Hubungkan Claude ke JoBG (MCP) |

---

## 🛡️ Master user

### 11. Dashboard Master
```
┌──────────────────────────────────────────────────────────┐
│ JoBG · Master                                            │
│ [Perusahaan] [Akun HR] [Semua lowongan] [Catatan aktivitas]│
├──────────────────────────────────────────────────────────┤
│ Akun HR                                     [+ Tambah HR] │
│ Sari    PT B    sari@…    🟢 Aktif     [Nonaktifkan]      │
│ Andi    PT F    andi@…    🟢 Aktif     [Nonaktifkan]      │
│ Tono    PT B    tono@…    ⚪ Diundang                      │
└──────────────────────────────────────────────────────────┘
```
Master user bisa membuka semua halaman HR untuk perusahaan mana pun.

---

## Catatan tampilan HP
- Tabel (Pelamar per tahap, Penilaian) berubah menjadi **kartu bertumpuk** di layar kecil.
- Prioritas HP: **halaman kandidat**. Dashboard HR & Master boleh lebih nyaman di laptop.

## ❓ Pertanyaan terbuka
- [x] Susunan halaman inti → **sesuai**
- [x] Kolom Pelamar per tahap → **cukup**
- [x] Versi visual → **dibuat setelah [[Design System]] final** (prototipe visual yang bisa diklik)
