---
tags: [prd]
status: ✅ final
diperbarui: 2026-11-21
---
# PRD: JoBG

## 1. Ringkasan
**JoBG** adalah portal lowongan kerja & magang untuk **pencari kerja pemula** (mahasiswa tingkat akhir, pencari magang, fresh graduate yang belum pernah bekerja) dari semua jenjang & sektor.

Masalah inti: **HR menilai dari isian kandidat, padahal isian tidak mencerminkan kemampuan.** Kandidat jago tapi malas mengisi terlewat; kandidat rajin mengisi tapi kurang mampu justru lolos.

JoBG menjawabnya dengan: **profil otomatis dari CV**, **penilaian berbasis bukti (bukan klaim)**, **tes langsung**, dan **penilaian HR yang terstruktur** dengan tanda "lihat sekali lagi". Detail: [[Visi]].

## 2. Pengguna
| Peran    | Persona utama MVP                    | Lainnya                      |
| -------- | ------------------------------------ | ---------------------------- |
| Kandidat | **K1 Raka**: jago tapi malas mengisi | K2 Dinda, K3 Putri, K4 Bagas |
| HR       | **H1 Sari**: HR yang kewalahan       | H2 Andi                      |

Detail: [[Persona]].

## 3. Fitur
| Area                | Fitur                                                | Prioritas | User stories               |
| ------------------- | ---------------------------------------------------- | --------- | -------------------------- |
| **Profil kandidat** | Daftar minimal + unggah CV                           | MVP       | US-01                      |
|                     | Profil disusun AI dari CV, kandidat memeriksa        | MVP       | US-02                      |
|                     | Tanda ✅ terbukti / 💬 klaim + tambah bukti           | MVP       | US-03                      |
|                     | Profil dari cerita singkat (tanpa CV)                | Nanti     | US-04                      |
| **Lowongan**        | Jelajah & filter lowongan                            | MVP       | US-05                      |
|                     | Asisten AI pencari lowongan & penjelasan kecocokan   | Nanti     | US-06, 07                  |
|                     | Buat lowongan + **kriteria wajib / nilai tambah**    | MVP       | US-20, 21                  |
| **Alur rekrutmen**  | Susun alur dinamis (seleksi berkas, tes, interview)  | MVP       | US-22                      |
|                     | Template alur                                        | Nanti     | US-23                      |
|                     | Permintaan dokumen & penawaran sebagai jenis tahap   | Nanti     | (lihat [[Alur Rekrutmen]]) |
| **Lamaran**         | Melamar memakai profil (tanpa isi ulang)             | MVP       | US-08                      |
|                     | Kandidat melihat tahap & status saat ini             | MVP       | US-10                      |
| **Tes / tugas**     | HR membuat tes; kandidat mengerjakan                 | MVP       | US-24, 09                  |
| **Penilaian HR**    | Pelamar per tahap                                    | MVP       | US-25                      |
|                     | Penilaian per kriteria dengan bukti vs klaim         | MVP       | US-26                      |
|                     | Tanda ketidaksesuaian data                           | MVP       | US-27                      |
|                     | Mode penilaian tanpa identitas (pilihan per lowongan)                            | Nanti       | US-28                      |
|                     | Keputusan dengan alasan wajib                        | MVP       | US-29                      |
|                     | Tanda **"lihat sekali lagi"**                        | MVP       | US-30                      |
|                     | Catatan & nilai interview                            | MVP       | US-31                      |
| **Pemberitahuan** | Kabar ke kandidat di Portal (daftar, melamar, perubahan status) | MVP | (keputusan desain sistem) |
| | Pemberitahuan lewat email | Nanti | |
| **Master user** | Tambah perusahaan; buat & nonaktifkan akun HR | MVP | US-50, 51 |
| **Blacklist**       | Blacklist dengan alasan & bukti; banding             | Nanti     | US-11, 32, 33              |
| **Akses MCP**       | HR bertanya tentang pelamarnya lewat AI di luar JoBG | MVP       | US-40                      |
|                     | AI memindahkan tahap atas perintah HR                | Nanti     | US-41                      |

Detail: [[User Stories]] · data: [[Peta Data Kandidat]] · alur: [[Alur Rekrutmen]].

## 4. Peran AI (bahasa pengguna)
| Kemampuan AI | Untuk siapa | MVP |
|---|---|---|
| Menyusun profil dari CV | Kandidat | ✅ |
| Memisahkan klaim vs bukti per kriteria | HR | ✅ |
| Menandai data yang tidak konsisten | HR | ✅ |
| Memberi tanda "lihat sekali lagi" | HR | ✅ |
| Menjawab pertanyaan HR dari luar JoBG (MCP) | HR | ✅ |
| Asisten pencari lowongan untuk kandidat | Kandidat | Nanti |

**Batasan AI:**
- AI **tidak** mengambil keputusan lanjut / tidak lanjut / blacklist.
- AI **tidak** memberi skor tunggal tanpa penjelasan; selalu menunjuk ke bukti.
- AI **tidak** menilai dari data ⚠️ sensitif (nama, foto, jenis kelamin, sekolah, usia), meskipun HR bisa melihatnya.
- Isi CV/dokumen kandidat diperlakukan sebagai **data**, bukan perintah bagi AI.

## 5. Alur utama MVP (skenario demo)
```
Raka daftar + unggah CV → AI menyusun profil → Raka memeriksa & menambah bukti → melamar
  → Sari: seleksi berkas (bukti vs klaim per kriteria)
  → Sari tanpa sadar menghentikan Raka → JoBG memberi tanda "lihat sekali lagi"
  → Sari meninjau ulang → Raka lanjut ke Tes → hasil tes kuat → Interview
  → Sari bertanya lewat Claude (MCP): "ringkas kandidat yang lolos tes"
```
Skenario pembanding: **Dinda** dengan isian panjang tapi sebagian besar 💬 klaim.

## 6. Kebutuhan non-fungsional (garis besar)
- **Privasi:** hanya data dummy; HR hanya melihat pelamar perusahaannya sendiri; AI tidak memakai data ⚠️ sensitif.
- **Keadilan:** setiap keputusan "tidak lanjut" punya alasan tertulis.
- **Transparansi:** setiap penilaian AI bisa ditelusuri ke buktinya.
- **Kemudahan:** kandidat bisa melamar dalam beberapa langkah singkat; nyaman dibuka di HP.
- **Bahasa:** antarmuka berbahasa Indonesia.
- **Siap dipublikasikan:** tidak ada data asli atau rahasia di repository.

## 7. Di luar cakupan
Lihat [[Visi]] (bukan tujuan) dan [[Alur Rekrutmen]] (di luar lingkup). Ringkasnya: bukan untuk kandidat berpengalaman, tanpa pembayaran, tanpa psikotes/video interview/kontrak digital di dalam JoBG, tanpa aplikasi HP khusus.

## 8. Asumsi & risiko
| Risiko | Dampak | Cara mengurangi |
|---|---|---|
| AI salah membaca CV | Profil keliru | Kandidat selalu memeriksa & bisa mengubah |
| AI ikut bias | Penilaian tidak adil | Data sensitif disembunyikan; AI hanya menunjuk bukti, keputusan di HR |
| CV berisi teks untuk "mengakali" AI | Penilaian dimanipulasi | Isi dokumen diperlakukan sebagai data, bukan perintah |
| HR enggan menulis kriteria | Fitur penilaian tidak berjalan | Kriteria wajib sebelum lowongan dibuka; bisa dibantu contoh |
| Cakupan membengkak | Proyek tidak selesai | Pegang daftar MVP; fitur baru masuk "Nanti" |

## 9. Ukuran keberhasilan
Mengikuti [[Visi]]. Inti untuk MVP:
- [ ] Skenario demo di bagian 5 berjalan dari awal sampai akhir.
- [ ] Perbedaan Raka (terbukti) vs Dinda (klaim) terlihat jelas oleh HR.
- [ ] HR bisa bertanya tentang pelamarnya lewat Claude (MCP) dan hanya melihat datanya sendiri.

## ❓ Pertanyaan terbuka
- [ ] Ada fitur yang terlewat atau perlu dipindah prioritasnya?
- [ ] Skenario demo (bagian 5) sudah menggambarkan cerita yang ingin ditunjukkan?
