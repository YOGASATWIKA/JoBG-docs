---
tags: [desain, ui]
status: ✅ final
diperbarui: 2026-11-21
---
# Design System

> Prinsip: **simpel, mudah, berkesan.** Sedikit warna, satu huruf, tidak ada hiasan yang tidak perlu.
> Nilai di sini adalah acuan desain; penerapan di kode dibahas saat breakdown teknis.

## 1. Tiga tone warna saja
| Tone | Arti | Terang | Gelap |
|---|---|---|---|
| **Biru** | Aksi utama & hal yang **terbukti / positif** | `#1D4ED8` | `#7AA7FF` |
| **Netral** | Semua yang lain: teks, latar, garis, status biasa | teks `#0F172A` · redup `#64748B` · garis `#E2E8F0` · latar `#FFFFFF` / `#F8FAFC` | teks `#E5EAF3` · redup `#94A3B8` · garis `#243049` · latar `#0B1220` / `#111A2E` |
| **Jingga** | **Butuh perhatian / tindakan** | `#C2410C` | `#FDBA74` |

Mode **terang & gelap** tersedia sejak awal.

### Status memakai tone yang sama
| Status | Tampilan |
|---|---|
| Terbukti | **Biru** + ikon centang + teks "Terbukti" |
| Klaim | **Netral** (garis tepi) + teks "Klaim" |
| Tidak ada | **Netral redup** + teks "Tidak ada" |
| Lihat sekali lagi | **Jingga** + ikon bendera |
| Lamaran: diproses | Netral |
| Lamaran: lanjut / diterima | Biru |
| Lamaran: tidak lanjut | Netral gelap + teks (bukan merah) |
| Lamaran: menunggu kandidat (mis. tes) | Jingga |

**Aturan warna:**
- Jingga hanya untuk hal yang **benar-benar perlu perhatian**. Kalau semuanya jingga, tidak ada yang menonjol.
- Status selalu **ikon + teks**, tidak hanya warna.
- Merah hanya untuk **pesan kesalahan** formulir.

## 2. Satu huruf: Plus Jakarta Sans
Dipakai untuk judul **dan** teks. Satu keluarga huruf = tampilan lebih rapi.
- Dirancang desainer Indonesia: ada cerita lokal untuk JoBG.
- Lebih berkarakter daripada Roboto, yang terasa seperti tampilan bawaan Android.
- Angka di tabel memakai angka rata (*tabular*) agar sejajar.

Ukuran: judul halaman 28 · judul bagian 20 · teks 15 · keterangan 13.

## 3. Bentuk
- Sudut sedikit membulat (kartu 12, tombol & input 8).
- Pemisah cukup **garis tipis**; tanpa bayangan, tanpa gradasi.
- Jarak kelipatan 4. Ruang kosong yang cukup lebih penting daripada hiasan.

## 4. Komponen inti
| Komponen | Aturan |
|---|---|
| Tombol | **Satu** tombol biru per layar; sisanya bergaris tepi |
| Chip status | Ikon + teks; bentuk & ukuran sama di semua halaman |
| Kotak "lihat sekali lagi" | Garis kiri jingga + kalimat singkat, di atas halaman Penilaian |
| Isian hasil AI | Tanda kecil "dari CV" + [Benar] [Ubah] |
| Tabel pelamar | Di HP berubah menjadi daftar kartu |

## 5. Yang dihindari (agar tidak terasa "AI slop")
- ❌ Emoji di tampilan. Pakai **ikon garis sederhana** dari satu set ikon saja.
- ❌ Gradasi warna, efek kaca, bayangan tebal, animasi berlebihan.
- ❌ Banyak warna aksen atau label warna-warni.
- ❌ Semua elemen dibungkus kartu membulat. Kartu hanya untuk benda yang berdiri sendiri (lowongan, lamaran).
- ❌ Hero besar di beranda. Langsung tampilkan hal yang berguna: cari lowongan.
- ❌ Kalimat promosi berlebihan. Tulis apa adanya.

## 6. Bahasa
- Bahasa Indonesia sopan, sapa "Anda".
- Kandidat: **menyemangati**. "Tambahkan bukti agar HR lebih yakin dengan kemampuan Anda."
- HR: **ringkas & faktual**. "Memenuhi 2/2 syarat wajib dengan bukti, tetapi dihentikan."
- Tombol menyebut aksinya: "Kirim lamaran", "Buka lowongan".

> Catatan: simbol ✅ 💬 ❌ ⚑ di dokumen lain hanya **notasi dokumen**. Di tampilan nyata diganti ikon garis + teks.

## Keputusan
- [x] Palet → **A · Biru Tepercaya**, disederhanakan menjadi **3 tone**: biru, netral, jingga
- [x] Mode gelap → **ada sejak awal**
- [x] Huruf → **Plus Jakarta Sans** saja
- [x] Gaya → simpel, tanpa emoji, gradasi, atau hiasan berlebihan
