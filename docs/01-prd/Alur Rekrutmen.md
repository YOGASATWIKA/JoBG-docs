---
tags: [prd, alur]
status: ✅ final
diperbarui: 2026-11-21
---
# Alur Rekrutmen (dinamis)

> Setiap perusahaan punya proses rekrutmen berbeda. JoBG **tidak memaksakan satu alur**: HR menyusun alurnya sendiri dari **jenis tahap yang tersedia**, tapi tetap dalam lingkup JoBG.

## Bentuk alur
```
[Tetap]   ① Daftar akun → ② Melamar
[Dinamis] → Tahap A → Tahap B → ... (disusun HR per lowongan)
[Tetap]   → Hasil akhir: Diterima / Tidak lanjut
```
- Bagian **tetap** sama untuk semua perusahaan.
- Bagian **dinamis** disusun HR: urutan, jumlah, dan isi tahap bebas diatur.
- HR bisa menyimpan alur sebagai **template** untuk dipakai ulang di lowongan lain.

## Jenis tahap yang tersedia (lingkup JoBG)
| Jenis tahap            | Contoh di dunia nyata                            | Yang bisa dilakukan di JoBG                                                       |
| ---------------------- | ------------------------------------------------ | --------------------------------------------------------------------------------- |
| **Seleksi berkas**     | Screening CV, cek syarat minimum                 | HR menilai profil terhadap kriteria + bukti                                       |
| **Permintaan dokumen** | Transkrip, sertifikat, surat magang, KTP         | Kandidat mengunggah dokumen yang diminta                                          |
| **Tes / tugas**        | Studi kasus, tes kemampuan, tes bahasa, psikotes | Tugas singkat dikerjakan di JoBG, **atau** hasil tes dari luar dicatat / diunggah |
| **Interview**          | Interview HR, user, panel; online / offline      | Mencatat jadwal, catatan, & penilaian per kriteria                                |
| **Penawaran**          | Offering letter, negosiasi                       | Mengirim penawaran & mencatat jawaban kandidat                                    |

Satu jenis bisa dipakai berkali-kali (mis. Interview HR → Tes → Interview User).

## Isi setiap tahap (diatur HR)
| Bagian | Keterangan |
|---|---|
| Nama tahap | Bebas, mis. "Interview User" |
| Jenis tahap | Salah satu jenis di atas |
| Data / dokumen yang diminta | Diambil dari [[Peta Data Kandidat]] |
| Kriteria penilaian | Apa yang dinilai di tahap ini (wajib / nilai tambah) |
| Keputusan | **Lanjut** atau **Tidak lanjut** (+ alasan wajib); **Blacklist** hanya untuk perilaku |

**Berlaku di setiap tahap:**
- AI menyajikan **bukti vs klaim** untuk kriteria tahap tersebut.
- Tanda **"lihat sekali lagi"** bila keputusan tampak tidak sesuai kriteria.
- Kandidat hanya dimintai **data yang diperlukan tahap itu**.

## Tentang "Tes / tugas"
Tes/tugas adalah **tugas kecil sesuai lowongan** untuk melihat kemampuan **langsung**, bukan dari isian.
Contoh:
- Lowongan admin keuangan → mengolah tabel transaksi sederhana
- Lowongan desain grafis → membuat konsep untuk brief singkat
- Lowongan marketing → menulis ide konten untuk satu produk

Ini menjawab masalah kandidat **jago tapi malas mengisi**: kemampuannya terlihat dari hasil kerja, bukan panjangnya isian.
HR yang menentukan apakah sebuah lowongan memakai tahap Tes atau tidak.

## Di luar lingkup (untuk saat ini)
- ❌ Menjalankan psikotes resmi di dalam JoBG (cukup mencatat hasil dari luar)
- ❌ Video interview di dalam JoBG (cukup mencatat jadwal & tautan)
- ❌ Tanda tangan kontrak digital

## Keputusan
- **Kandidat tidak bisa melihat seluruh alur** sebuah lowongan sebelum melamar. *(Asumsi: setelah melamar, kandidat hanya melihat tahap yang sedang dijalaninya & statusnya.)*
- **Tidak ada batas maksimal** jumlah tahap per lowongan.
- **Jenis tahap untuk MVP:** Seleksi berkas, Tes / tugas, Interview.
  Permintaan dokumen & Penawaran menyusul setelah MVP.

## ❓ Pertanyaan terbuka
- [x] Kandidat melihat seluruh alur sebelum melamar → **tidak**
- [x] Batas maksimal tahap → **tidak ada**
- [x] Jenis tahap MVP → **Seleksi berkas, Tes / tugas, Interview**
