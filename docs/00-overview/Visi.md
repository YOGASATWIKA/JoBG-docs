---
tags: [overview]
status: ✅ final
diperbarui: 2026-11-21
---
# Visi

## Masalah
Masalah ini dialami **dua sisi sekaligus**. Masalah inti (⭐) berasal dari pengamatan langsung di dunia kerja HR.

**Sisi kandidat (pencari kerja pemula)**
- ⭐ **Lelah mengisi data.** Proses rekrutmen meminta terlalu banyak isian. Akibatnya, kandidat berpotensi besar justru **malas melamar atau berhenti di tengah jalan**.
- Lowongan untuk lulusan baru **tersebar** di banyak tempat dan sulit dicari.
- Banyak lowongan berlabel "entry level" ternyata **meminta pengalaman**.
- Kandidat sering **tidak tahu posisi apa yang cocok** dengan jurusan & kemampuannya.

**Sisi perekrut (HR)**
- ⭐ **Salah menilai kandidat (mismatch).** Kandidat yang lebih baik justru **dihentikan prosesnya atau di-blacklist**, sementara yang dilanjutkan kemampuannya jauh di bawah.
- ⭐ **Kelelahan menilai.** Banyaknya lamaran membuat HR menilai dengan terburu-buru dan tidak konsisten.
- Kandidat pemula **belum punya riwayat kerja**, sehingga sulit dinilai.

### 🎯 Akar masalah utama
> **HR menilai dari data yang diisi sendiri oleh kandidat, dan kualitas isian itu tidak mencerminkan kemampuan sebenarnya.**

| Tipe kandidat | Perilaku saat mengisi | Akibat di mata HR |
|---|---|---|
| **Mampu tapi malas mengisi** | Isian singkat, tidak lengkap | Terlihat lemah → **terlewat / dihentikan** |
| **Kurang mampu tapi rajin mengisi** | Isian panjang, dilebih-lebihkan | Terlihat kuat → **dilanjutkan** |

Jadi sistem saat ini **tanpa sengaja menilai usaha mengisi formulir, bukan kemampuan.**

### Akar masalah pendukung
| Gejala | Kemungkinan penyebab |
|---|---|
| Kandidat malas mengisi | Data diminta **sekaligus di awal** dan berulang di setiap lamaran |
| HR salah menilai | Kriteria penilaian **tidak tertulis**, sehingga menilai dengan "feeling" |
| HR salah menilai | **Kelelahan** & **bias kesan pertama** (kampus, foto, format CV) |
| Kandidat baik di-blacklist | Keputusan **tanpa alasan tertulis** dan tanpa pengecekan ulang |

## Prinsip solusi
> Solusinya **bukan sekadar memasang chatbot** yang menjawab "apakah saya cocok?" atau "apakah kandidat B layak lanjut?".
> Jawaban AI seperti itu hanya memindahkan "feeling" HR ke "feeling" AI, dan AI juga bisa salah atau bias.

JoBG memakai AI untuk **dua hal yang lebih mendasar**:

**1. Mengurangi beban kandidat** (agar yang mampu tapi malas tetap punya profil lengkap)
- Kandidat cukup **mengunggah CV / dokumen / bercerita singkat**; AI menyusun profil, kandidat tinggal **memeriksa & membetulkan**.
- **Satu profil untuk semua lamaran**: tidak perlu mengisi ulang.
- **Semua data tetap wajib**, tapi **cara & waktu pengumpulannya** diatur: sebagian terisi otomatis, sebagian diminta di tahap yang membutuhkannya. Detail di [[Peta Data Kandidat]].

**2. Menilai dari bukti, bukan dari klaim** (agar yang pandai mengisi tidak otomatis unggul)
- Setiap data ditandai: **✅ ada bukti** (sertifikat, transkrip, link portofolio, hasil tugas) atau **💬 klaim saja**.
- AI memberi tanda bila ada **ketidaksesuaian**: mis. mengaku mahir sesuatu tapi tidak ada bukti, atau tanggal yang bertabrakan.
- **Tugas / pertanyaan singkat** sesuai lowongan untuk melihat kemampuan langsung, lebih ringan daripada mengisi formulir panjang.
- **Kelengkapan isian ≠ kualitas kandidat**: HR melihat keduanya secara terpisah.

**3. Membuat penilaian HR lebih adil & konsisten**
- Setiap lowongan punya **kriteria penilaian yang tertulis** (wajib vs nilai tambah) **sebelum** melihat pelamar.
- AI menyajikan **bukti dari profil untuk tiap kriteria**, bukan sekadar skor misterius. HR bisa melihat *kenapa*.
- Opsi **penilaian tanpa identitas** (nama, foto, kampus disembunyikan) di tahap awal untuk mengurangi bias.
- **Alasan wajib** saat menghentikan proses.
- **Blacklist hanya untuk perilaku**, bukan karena dinilai kurang cocok (lihat di bawah).
- **"Lihat sekali lagi"**: AI memberi tanda bila kandidat yang dihentikan ternyata sangat sesuai kriteria, atau kandidat yang dilanjutkan jauh di bawah kriteria.

**Keputusan selalu di tangan manusia.** AI membantu bekerja lebih ringan dan lebih konsisten, bukan menggantikan penilaian.

### Blacklist
Tujuan: mencegah kandidat yang **bertindak semena-mena** dan **mengotori data** (mis. data palsu, spam lamaran, perilaku kasar).
- Yang berwenang: **HR perusahaan** (pengguna dashboard admin JoBG).
- Berlaku **di perusahaan tersebut saja**: kandidat langsung kehilangan akses untuk melamar ke lowongan perusahaan itu.
- Blacklist **wajib disertai alasan & bukti**, dan alasannya **bisa dilihat kandidat**.

**Banding (pengajuan pembukaan akses)**
```
HR blacklist + alasan → kandidat melihat alasan
   → kandidat memperbaiki / memenuhi alasan tersebut (mis. mengganti data palsu dengan bukti asli)
   → kandidat mengajukan banding dengan bukti perbaikan
   → HR meninjau → akses dibuka kembali / tetap diblokir (dengan alasan)
```
- Banding **hanya bisa diajukan** setelah kandidat menunjukkan bahwa alasan blacklist sudah dipenuhi.
- Blacklist **bukan** untuk kandidat yang "kurang cocok". Itu cukup dihentikan prosesnya. Pemisahan ini mencegah kandidat bagus ikut terblokir.

Chatbot & MCP tetap ada, tapi hanya sebagai **cara mengakses** kemampuan di atas, bukan solusinya itu sendiri.

## Solusi (satu kalimat)
> **JoBG** adalah portal lowongan kerja & magang untuk **pencari kerja pemula dari semua jenjang pendidikan, di semua sektor bisnis**, yang memakai AI agar **kandidat cukup sedikit usaha untuk melamar** dan **perekrut menilai berdasarkan bukti kemampuan, bukan isian formulir**, sehingga kandidat berpotensi tidak lagi terlewat.

## Target pengguna (garis besar)
1. **Pencari kerja pemula**, yaitu siapa pun yang **belum pernah bekerja** setelah lulus:
   - **Mahasiswa tingkat akhir**: mencari kerja atau magang menjelang lulus.
   - **Pencari magang**: mencari pengalaman kerja pertama.
   - **Fresh graduate**: sudah lulus, masih mencari kerja, dan **belum pernah mendapat pekerjaan** setelah lulus (tidak dibatasi tahun kelulusan).

   Dari **semua jenjang pendidikan**: SMA/SMK, D3/D4, S1, hingga S2.
2. **Perekrut (HR)**: HR dari perusahaan (semua sektor) yang memakai **dashboard admin JoBG** untuk membuat lowongan dan menjalankan seluruh proses rekrutmen, termasuk blacklist.

Detail di [[Persona]].

## Tujuan proyek
**Bagi pengguna**
- Kandidat bisa melamar dengan **usaha minimal** tanpa mengisi data berulang-ulang.
- Perekrut menilai kandidat dengan **kriteria jelas** dan **lebih sedikit salah pilih**.
- Kandidat berpotensi **tidak terlewat** hanya karena malas mengisi atau karena penilai lelah.

**Bagi saya (tujuan utama: portofolio)**
- Menunjukkan kemampuan sebagai **fullstack AI developer**: website + AI + MCP.
- Menunjukkan **pemikiran produk**: berangkat dari masalah nyata di dunia HR, bukan sekadar menempel AI.
- Menunjukkan **proses kerja yang rapi**: PRD, desain, keputusan, dan konvensi yang terdokumentasi.

**Rencana akses**
1. **Sekarang:** dijalankan & didemokan dari laptop sendiri.
2. **Nanti (jika hasilnya bagus):** repository dibuka publik dan tampilannya bisa diakses online sebagai demo portofolio.

> Karena berpotensi dipublikasikan, sejak awal **tidak boleh ada data pribadi asli** atau rahasia (password, kunci akses) di repository.

## Bukan tujuan (di luar cakupan)
- ❌ Bukan untuk orang yang sudah pernah bekerja setelah lulus / level berpengalaman.
- ❌ Bukan produk komersial: tidak ada pembayaran atau paket berlangganan.
- ❌ Tidak memakai data pribadi asli; semua lowongan & pelamar adalah **data contoh (dummy)**.
- ❌ AI **tidak** mengambil keputusan menerima / menolak / mem-blacklist kandidat secara otomatis.
- ❌ AI **tidak** memberi skor tunggal tanpa penjelasan.
- ❌ Belum ada aplikasi HP khusus (cukup website yang nyaman dibuka di HP).

## Ukuran keberhasilan (sebagai portofolio)
- [ ] **Kandidat:** dari unggah CV sampai lamaran terkirim hanya butuh beberapa langkah singkat.
- [ ] **Perekrut:** setiap kandidat dinilai terhadap kriteria tertulis, lengkap dengan bukti dari profil.
- [ ] **Skenario "klaim vs bukti":** demo dua kandidat (mampu tapi isian singkat vs isian panjang tanpa bukti), dan JoBG menampilkan perbedaannya dengan jelas.
- [ ] **Skenario "kandidat terlewat":** demo di mana kandidat bagus yang dihentikan berhasil ditandai untuk dilihat ulang.
- [ ] AI menjawab berdasarkan data di portal, **tanpa mengarang**.
- [ ] AI (mis. Claude) bisa mengakses kemampuan portal dari luar website lewat MCP.
- [ ] Dokumentasi lengkap dan bisa dibaca orang lain untuk memahami proyek ini.

## ❓ Pertanyaan terbuka
- [x] Batasan fresh graduate → mahasiswa tingkat akhir, pencari magang, dan lulusan yang belum pernah bekerja setelah lulus
- [x] Jenjang pendidikan → semua jenjang
- [x] Akses demo → lokal dulu, publik bila hasilnya bagus
- [x] Nama produk → **JoBG**
- [x] Penyebab utama salah menilai → kualitas isian kandidat tidak mencerminkan kemampuan (malas vs melebih-lebihkan)
- [x] Data wajib → semua data wajib dan saling berkaitan; dipetakan di [[Peta Data Kandidat]]
- [x] Blacklist → perlu, untuk kandidat yang semena-mena / mengotori data; akses langsung dicabut
- [x] Fokus MVP → **satu alur kecil yang mencakup kandidat & perekrut**
- [x] Wewenang blacklist → HR perusahaan, berlaku di perusahaan tersebut
- [x] Banding → bisa, setelah kandidat memenuhi alasan blacklist; HR yang memutuskan

## 🧭 Fokus MVP (konsep)
Satu alur kecil dari ujung ke ujung:
```
Kandidat unggah CV → AI menyusun profil → kandidat periksa & melamar
   → HR menilai dengan kriteria + bukti (klaim vs terbukti)
   → keputusan HR → AI memberi tanda "lihat sekali lagi" bila tidak sesuai kriteria
```
Detail fitur di [[PRD]].
