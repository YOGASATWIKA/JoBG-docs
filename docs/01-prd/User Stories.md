---
tags: [prd]
status: ✅ final
diperbarui: 2026-11-21
---
# User Stories

Format: **Sebagai** (peran), **saya ingin** (aksi), **agar** (manfaat).
Persona: lihat [[Persona]]. Prioritas: **MVP** = versi pertama · **Nanti** = setelah MVP.

## 🎓 Kandidat

### Profil tanpa ribet
| ID    | User story                                                                                                                                                                         | Persona | Prioritas | Kriteria diterima                                                              |
| ----- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- | --------- | ------------------------------------------------------------------------------ |
| US-01 | Sebagai kandidat, saya ingin **mendaftar dengan data seminimal mungkin** (email, HP, sekolah, minat, jenis kerja/magang) dan mengunggah CV, agar bisa mulai tanpa formulir panjang | K1      | MVP       | Pendaftaran selesai dalam satu halaman singkat                                 |
| US-02 | Sebagai kandidat, saya ingin **AI menyusun profil dari CV saya**, agar saya cukup memeriksa & membetulkan                                                                          | K1      | MVP       | Pendidikan, pengalaman, & skill terisi otomatis; setiap isian bisa diubah      |
| US-03 | Sebagai kandidat, saya ingin **melihat mana data saya yang masih klaim** dan menambahkan bukti (dokumen / link), agar profil saya lebih dipercaya                                  | K1, K2  | MVP       | Setiap data rawan klaim bertanda ✅ terbukti / 💬 klaim; bukti bisa ditambahkan |
| US-04 | Sebagai kandidat tanpa CV rapi, saya ingin **bercerita singkat** tentang diri saya, agar AI tetap bisa menyusun profil                                                             | K4      | Nanti     | Profil tersusun dari cerita singkat                                            |

### Menemukan lowongan
| ID | User story | Persona | Prioritas | Kriteria diterima |
|---|---|---|---|---|
| US-05 | Sebagai kandidat, saya ingin **menjelajah & memfilter lowongan** (jenis, sektor, lokasi, jenjang), agar menemukan yang relevan | K3 | MVP | Filter bekerja & hanya menampilkan lowongan aktif |
| US-06 | Sebagai kandidat, saya ingin **bertanya ke asisten AI dengan bahasa sehari-hari**, agar tidak perlu menebak kata kunci | K3 | Nanti | Jawaban hanya berisi lowongan yang ada di JoBG, tanpa mengarang |
| US-07 | Sebagai kandidat, saya ingin **tahu kenapa sebuah lowongan cocok / kurang cocok** dengan profil saya, agar bisa memutuskan melamar atau tidak | K1, K3 | Nanti | Penjelasan merujuk pada kriteria lowongan & data profil |

### Melamar & mengikuti proses
| ID | User story | Persona | Prioritas | Kriteria diterima |
|---|---|---|---|---|
| US-08 | Sebagai kandidat, saya ingin **melamar memakai profil yang sudah ada**, agar tidak mengisi ulang | K1 | MVP | Lamaran terkirim tanpa mengetik ulang data profil |
| US-09 | Sebagai kandidat, saya ingin **mengerjakan tes / tugas singkat** di JoBG, agar kemampuan saya terlihat langsung | K1 | MVP | Tes bisa dikerjakan & dikirim; hasilnya tercatat di lamaran |
| US-10 | Sebagai kandidat, saya ingin **melihat tahap yang sedang saya jalani & statusnya**, agar tidak menunggu tanpa kabar | K1, K3 | MVP | Hanya tahap saat ini yang terlihat (bukan seluruh alur) |
| US-11 | Sebagai kandidat yang di-blacklist, saya ingin **melihat alasannya & mengajukan banding** setelah memenuhinya, agar akses saya bisa dibuka kembali | K2 | Nanti | Banding hanya bisa diajukan dengan bukti perbaikan |

## 🧑‍💼 HR

### Menyiapkan lowongan
| ID | User story | Persona | Prioritas | Kriteria diterima |
|---|---|---|---|---|
| US-20 | Sebagai HR, saya ingin **membuat lowongan** (kerja / magang), agar kandidat bisa melamar | H1 | MVP | Lowongan tampil di daftar lowongan kandidat |
| US-21 | Sebagai HR, saya ingin **menulis kriteria penilaian** (wajib & nilai tambah) **sebelum** melihat pelamar, agar penilaian konsisten | H1 | MVP | Lowongan tidak bisa dibuka tanpa minimal satu kriteria wajib |
| US-22 | Sebagai HR, saya ingin **menyusun alur rekrutmen** dari jenis tahap yang tersedia, agar sesuai proses perusahaan saya | H1, H2 | MVP | Jenis tahap MVP: seleksi berkas, tes / tugas, interview; jumlah tahap bebas |
| US-23 | Sebagai HR, saya ingin **menyimpan alur sebagai template**, agar bisa dipakai ulang | H2 | Nanti | Template bisa dipilih saat membuat lowongan baru |
| US-24 | Sebagai HR, saya ingin **membuat tes / tugas singkat** untuk tahap tes, agar bisa melihat kemampuan langsung | H1, H2 | MVP | Tes terhubung ke tahap & lowongan tertentu; batas waktu bisa diaktifkan atau tidak |

### Menilai & memutuskan
| ID | User story | Persona | Prioritas | Kriteria diterima |
|---|---|---|---|---|
| US-25 | Sebagai HR, saya ingin **melihat daftar pelamar per tahap**, agar tahu siapa yang perlu dinilai | H1 | MVP | Pelamar dikelompokkan per tahap |
| US-26 | Sebagai HR, saya ingin **melihat penilaian per kriteria lengkap dengan bukti vs klaim**, agar tahu *kenapa* kandidat sesuai atau tidak | H1 | MVP | Tiap kriteria menampilkan bukti dari profil; tidak ada skor tunggal tanpa penjelasan |
| US-27 | Sebagai HR, saya ingin **diberi tahu bila ada ketidaksesuaian** di data kandidat, agar tidak tertipu klaim | H1 | MVP | AI menandai klaim tanpa bukti / data yang bertentangan |
| US-28 | Sebagai HR, saya ingin **bisa menyalakan mode penilaian tanpa identitas** per lowongan, agar tidak bias kampus, foto, atau nama | H1 | Nanti | Bawaan: identitas terlihat. Bila dinyalakan: nama, foto, jenis kelamin, sekolah disembunyikan di seleksi berkas |
| US-29 | Sebagai HR, saya ingin **memutuskan lanjut / tidak lanjut dengan alasan**, agar keputusan bisa dipertanggungjawabkan | H1 | MVP | Keputusan "tidak lanjut" tidak bisa disimpan tanpa alasan |
| US-30 | Sebagai HR, saya ingin **mendapat tanda "lihat sekali lagi"** bila keputusan saya tampak tidak sesuai kriteria, agar kandidat bagus tidak terlewat | H1 | MVP | Tanda muncul bila kandidat yang dihentikan memenuhi kriteria wajib dengan bukti, atau yang dilanjutkan jauh di bawah kriteria |
| US-31 | Sebagai HR, saya ingin **mencatat interview** (jadwal, catatan, nilai per kriteria), agar hasilnya tersimpan rapi | H1 | MVP | Catatan & nilai tersimpan di lamaran |
| US-32 | Sebagai HR, saya ingin **mem-blacklist kandidat dengan alasan & bukti**, agar kandidat semena-mena tidak mengotori data | H1 | Nanti | Hanya untuk perilaku; berlaku di perusahaan itu saja |
| US-33 | Sebagai HR, saya ingin **meninjau banding blacklist**, agar akses bisa dibuka bila alasan sudah dipenuhi | H1 | Nanti | Keputusan banding wajib disertai alasan |

## 🛡️ Master user
| ID | User story | Persona | Prioritas | Kriteria diterima |
|---|---|---|---|---|
| US-50 | Sebagai master user, saya ingin **menambahkan perusahaan**, agar HR perusahaan itu bisa memakai JoBG | M | MVP | Perusahaan tersimpan dengan nama, sektor, lokasi |
| US-51 | Sebagai master user, saya ingin **membuat & menonaktifkan akun HR** untuk sebuah perusahaan, agar hanya HR resmi yang bisa masuk | M | MVP | HR menerima undangan email; akun nonaktif tidak bisa masuk |

## 🤖 Akses lewat AI dari luar JoBG (MCP)
| ID | User story | Persona | Prioritas | Kriteria diterima |
|---|---|---|---|---|
| US-40 | Sebagai HR, saya ingin **bertanya ke asisten AI (mis. Claude) di luar JoBG** tentang pelamar saya, mis. *"ringkas pelamar lowongan Admin Keuangan yang lolos tes"*, agar bekerja lebih cepat | H1 | MVP | AI hanya bisa melihat data lowongan milik perusahaan HR tersebut |
| US-41 | Sebagai HR, saya ingin **AI bisa memindahkan tahap kandidat atas perintah saya**, agar tidak perlu membuka dashboard | H1 | Nanti | Setiap aksi tulis meminta konfirmasi & tercatat |

## Ringkasan MVP (20 stories)
**Kandidat:** US-01, 02, 03, 05, 08, 09, 10
**HR:** US-20, 21, 22, 24, 25, 26, 27, 29, 30, 31
**Master user:** US-50, 51
**MCP:** US-40

> Asisten AI (chatbot) untuk kandidat **ditunda** (US-06, 07).
> AI tetap dipakai di MVP untuk: menyusun profil dari CV, menandai klaim vs bukti & ketidaksesuaian, tanda "lihat sekali lagi", dan akses MCP untuk HR.

## ❓ Pertanyaan terbuka
- [x] Ukuran MVP → **cukup**, dipertahankan
- [x] Asisten AI kandidat (US-06, 07) → **ditunda ke Nanti**
- [x] US-28 penilaian tanpa identitas → **jadi pilihan per lowongan, ditunda ke Nanti** (keputusan di [[Gambaran Sistem]])
