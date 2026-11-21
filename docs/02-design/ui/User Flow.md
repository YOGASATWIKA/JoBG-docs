---
tags: [desain, ui]
status: ✅ final
diperbarui: 2026-11-21
---
# User Flow

> Langkah-langkah pengguna mencapai tujuannya, **hanya fitur MVP**.
> Nama dalam `[kurung]` adalah **halaman**, yang nanti menjadi daftar di [[Wireframe]].
> Dasar: [[User Stories]] · [[Alur Rekrutmen]] · [[Gambaran Sistem]].

Simbol: `→` lanjut · `◇` pilihan / percabangan · `⚠` kondisi khusus

---

## 🎓 Kandidat (Raka)

### K-1. Daftar & profil dari CV · US-01, 02
```
[Beranda] → klik "Daftar"
→ [Daftar] isi email, HP, sekolah/institusi, minat, jenis (kerja/magang) + unggah CV
→ verifikasi email / HP (wajib)
→ [Profil: hasil AI] AI menyusun profil dari CV (pendidikan, pengalaman, skill, dll.)
   tiap isian bertanda 🤖 "perlu diperiksa"
→ Raka memeriksa: ◇ benar konfirmasi →
                  ◇ salah → ubah langsung
→ [Profil saya] profil aktif (data rawan klaim bertanda 💬 klaim)
```
⚠ AI gagal membaca CV → profil kosong, Raka bisa mengisi manual atau mengunggah ulang.
⚠ Raka berhenti di tengah → isian tersimpan, bisa dilanjutkan nanti.

### K-2. Menambah bukti · US-03
```
[Profil saya] → lihat ringkasan "X data masih 💬 klaim"
→ pilih satu data (mis. "Magang di PT A")
→ unggah dokumen / tempel link (sertifikat, portofolio, surat magang)
→ AI memeriksa kecocokan bukti ◇ cocok → ✅ terbukti
                              ◇ tidak cocok / ragu → tetap 💬 klaim + keterangan
```

### K-3. Mencari lowongan & melamar · US-05, 08
```
[Daftar lowongan] filter: jenis, sektor, lokasi, jenjang
→ [Detail lowongan] deskripsi + syarat (kriteria wajib & nilai tambah)
→ klik "Lamar"
→ [Konfirmasi lamaran] ringkasan profil yang akan dikirim
   + isi lokasi kerja & tanggal siap mulai (bila belum ada)
→ "Kirim" → pemberitahuan "Lamaran terkirim"
```
⚠ Profil belum dikonfirmasi → diarahkan ke K-1 dulu.
⚠ Sudah pernah melamar lowongan ini → tombol "Lamar" tidak aktif.

### K-4. Mengerjakan tes · US-09
```
Pemberitahuan "Anda diundang ke tahap Tes"
→ [Lamaran saya] → pilih lamaran
→ [Tes] petunjuk + batas waktu → kerjakan → "Kirim"
→ pemberitahuan "Tes terkirim"
```
⚠ Bila HR mengaktifkan batas waktu dan waktunya lewat → tes tidak bisa dikirim; status tercatat.

### K-5. Melihat status · US-10
```
[Pemberitahuan] / [Lamaran saya]
→ tiap lamaran menampilkan: nama lowongan · tahap saat ini · status
   (sedang diproses / lanjut / tidak lanjut / diterima)
```
Kandidat **tidak** melihat seluruh alur, hanya tahap saat ini.

---

## 🧑‍💼 HR (Sari)

### H-1. Membuat lowongan · US-20, 21, 22, 24
```
[Dashboard HR] → "Buat lowongan"
→ [Lowongan: info] judul, jenis (kerja/magang), sektor, lokasi, jenjang, deskripsi
→ [Lowongan: kriteria] tambah kriteria ◇ wajib / ◇ nilai tambah  (minimal 1 wajib)
→ [Lowongan: alur] susun tahap dari jenis: seleksi berkas · tes / tugas · interview
   (urutan & jumlah bebas)
   ◇ ada tahap Tes → [Tes: buat] soal / tugas + batas waktu ◇ aktif ◇ tanpa batas waktu
→ [Lowongan: pratinjau] → "Buka lowongan" → tampil di [Daftar lowongan] kandidat
```
⚠ Belum ada kriteria wajib → tidak bisa dibuka.
⚠ Simpan sebagai draf kapan saja.

### H-2. Menilai & memutuskan · US-25, 26, 27, 29
```
[Dashboard HR] → pilih lowongan
→ [Pelamar per tahap] pelamar dikelompokkan per tahap
→ pilih pelamar → [Penilaian kandidat]
   ├─ per kriteria: ✅ bukti / 💬 klaim / ❌ tidak ada  (+ tautan ke bukti)
   ├─ ⚠ tanda ketidaksesuaian dari AI (mis. klaim tanpa bukti, tanggal bertabrakan)
   └─ hasil tes / catatan interview (bila ada)
→ HR memutuskan ◇ Lanjut → kandidat pindah ke tahap berikutnya
               ◇ Tidak lanjut → alasan wajib diisi
→ pemberitahuan ke kandidat
```

### H-3. Tanda "lihat sekali lagi" · US-30
```
Setelah keputusan disimpan → AI membandingkan keputusan dengan kriteria & bukti
◇ sesuai → tidak ada tanda
◇ tidak sesuai → tanda "lihat sekali lagi" muncul di [Pelamar per tahap] & [Penilaian kandidat]
   (mis. "Kandidat memenuhi 4/4 kriteria wajib dengan bukti, tapi dihentikan")
→ HR ◇ buka & ubah keputusan  ◇ biarkan  (tanda hanya informasi)
```

### H-4. Mencatat interview · US-31
```
[Pelamar per tahap] tahap Interview → pilih kandidat
→ [Interview] isi jadwal & tautan / lokasi
→ setelah interview: catatan + nilai per kriteria
→ lanjut ke keputusan (H-2)
```

### H-5. Bertanya lewat Claude (MCP) · US-40
```
(sekali saja) [Dashboard HR: pengaturan] → hubungkan Claude ke JoBG
→ di Claude: "ringkas pelamar Admin Keuangan yang lolos tes"
→ Claude memanggil JoBG atas nama Sari → hanya data perusahaan Sari
→ jawaban di Claude; akses tercatat di Catatan Aktivitas
```

---

## 🛡️ Master user

### M-1. Membuat perusahaan & akun HR · US-50, 51
```
[Masuk] sebagai master user (akun tunggal, disiapkan sejak awal) → [Dashboard Master]
→ [Perusahaan] "Tambah perusahaan" (nama, sektor, lokasi)
→ [Akun HR] "Tambah HR" → pilih perusahaan → isi nama & email HR
→ JoBG mengirim undangan ke email HR
```
◇ Nonaktifkan akun HR (mis. HR sudah tidak bekerja di perusahaan tersebut).
◇ Master user juga bisa membuka **semua** halaman HR untuk perusahaan mana pun (akses penuh).

> 🔐 Kredensial master user **tidak ditulis** di dokumen atau repository. Disimpan di luar git (dibahas saat breakdown teknis).

### H-0. HR masuk pertama kali
```
Undangan di email → [Atur kata sandi] → [Masuk] → [Dashboard HR]
```

---

## Daftar halaman (bahan [[Wireframe]])
| Kandidat | HR | Master user |
|---|---|---|
| Beranda | Masuk | Masuk |
| Daftar (+ verifikasi) | Atur kata sandi | Dashboard Master |
| Profil: hasil AI | Dashboard HR | Perusahaan |
| Profil saya (+ bukti) | Lowongan: info / kriteria / alur / pratinjau | Akun HR |
| Daftar lowongan | Tes: buat | |
| Detail lowongan | Pelamar per tahap | |
| Konfirmasi lamaran | Penilaian kandidat | |
| Lamaran saya | Interview | |
| Tes | Pengaturan (hubungkan Claude) | |
| Pemberitahuan | | |
| Masuk | | |

## ❓ Pertanyaan terbuka
- [x] Akun HR → dibuat oleh **master user** (M-1)
- [x] Verifikasi email/HP kandidat → **wajib**
- [x] Batas waktu tes → **bisa diatur HR** (ada / tidak)
- [x] Flow terlewat / terlalu banyak → **tidak**
- [x] Akses master user → **semua akses tanpa terkecuali** (termasuk lowongan & pelamar); setiap aksinya tercatat di Catatan Aktivitas
- [x] Jumlah master user → **satu**, disiapkan sejak awal (tidak ada pendaftaran master user)
