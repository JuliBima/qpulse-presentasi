# DESIGN: Presentasi Q-PULSE

## Identitas
Deck satu file (`index.html`, CSS dan JS inline) plus `assets/*.png`. Menjual dua fitur: Alur A (test case dengan jenis fitur, Test Jira dan halaman Confluence sekali klik, tiket Jira UQA, WhatsApp) dan Alur B (Compare Defect). 15 slide, panggung tetap 1920x1080 yang diskalakan ke layar.

## Palet (dari chat pengguna)
| Hex | Peran |
|---|---|
| `#080B16` | latar utama |
| `#31205C` | panel kedua, latar slide pembuka dan penutup |
| `#6D28D9` | aksen tombol dan garis |
| `#8B5CF6` | aksen teks dan nomor |
| `#2563EB` | warna Alur B (Compare Defect) |

Alur A memakai ungu, Alur B memakai biru, supaya penonton tahu sedang di alur mana. Gradien hanya di wordmark Q-PULSE dan progress bar.

## Tipografi
Font sistem. Alasan: tidak ada jaringan saat presentasi, dan tidak ada file font yang harus ikut dibawa. Mono hanya untuk nilai literal (misalnya `.env`).

## Dial
ENERGY 2, RHYTHM 3, MOTION 2. Gerak hanya untuk memunculkan fragmen dan pindah slide, dan mati saat `prefers-reduced-motion`.

## Keputusan utama
- Semua gambar adalah tampilan aplikasi asli yang ditangkap dengan Puppeteer memakai respons API tiruan. Tiap gambar diberi tab "Data contoh". Alasan: tidak boleh ada data Jira atau BRI asli di slide.
- Tanpa ikon emoji atau pustaka ikon, tanpa angka statistik karangan, tanpa slide ajakan bertindak. Alasan: tidak ada data yang mendukungnya.
- Tanpa janji "online". Slide 14 menyebut lokal dulu, online setelah izin keamanan, sesuai keputusan pengguna.
- Mode terang memakai gradien ungu, bukan putih, sesuai arahan pengguna.
- Slide 1 punya gambar yang sengaja keluar panggung di sisi kanan.
- Merek di deck: "Q-PULSE" dan "QMDxKiro", dari `buatAkunNs/public/index.html` milik pengguna.

## Cara menyajikan
| Tombol | Fungsi |
|---|---|
| `→` / `Spasi` / klik | fragmen berikutnya, lalu slide berikutnya |
| `←` | mundur |
| `Home` / `End` | slide pertama / terakhir |
| `O` | daftar slide |
| `N` | catatan pembicara |
| `F` | layar penuh |
| `#n` di URL | langsung ke slide n |

Cetak ke PDF: ukuran 1920x1080, satu slide per halaman (CSS cetak sudah disiapkan).
Buka: `open presentasi-qpulse/index.html`.

## Pembaruan 26-11-2026
- Slide 4: pilihan jenis fitur Transaksi atau Non-transaksi, gambar `testcase-input.png` diganti.
- Slide 5: tiga tombol keluaran (Download CSV, Auto Create Confluence Page, Buat Jira UQA), gambar `testcase-review.png` diganti.
- Slide 6 baru: Epic, Test Set, Test, folder Test Repository, dan halaman Confluence dengan nomor Jira. Gambar `auto-modal.png` dan `auto-hasil.png`, data contoh project `DEMO`.
- Slide 3 dan 14 menyesuaikan alur baru. Nomor langkah Alur A bergeser satu.
- Slide 3 dan 4: requirement bisa dari FRD plus sampai 5 dokumen Confluence tambahan. `testcase-input.png` diganti, lebar gambar di slide 4 jadi 860px supaya muat.
