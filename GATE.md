# GATE: Presentasi Q-PULSE

Dijalankan dengan Puppeteer + Chrome headless. Tanggal 2026-11-15, diulang 2026-11-26 setelah pembaruan.

| Item | Hasil | Bukti |
|---|---|---|
| Jumlah slide | PASS | 15 |
| Gambar dimuat | PASS | 17 dimuat, 0 bermasalah, rasio sesuai atribut, dimensi cocok atribut width/height |
| Tanda pisah panjang (R-02) | PASS | 0 em dash |
| Kata terlarang | PASS | tidak ada |
| Kontras teks | PASS | 0 elemen kontras rendah di 14 slide |
| Batas bawah 1016px | PASS | slide konten <= 1016. Slide 1, 2, 14 memakai panel penuh 1080 (latar, bukan konten) |
| Gambar keluar panggung | PASS | hanya slide 1, disengaja |
| Overflow horizontal | PASS | 1366, 1024, 390, 844 lebar: scrollWidth sama dengan lebar |
| Request gagal / error JS | PASS | tidak ada |
| Panah kiri/kanan, Home, End | PASS | End 14/14 (uji 15-11), Home 1/14, dua kali kanan 2/14, kiri tetap di slide 2 (fragmen mundur) |
| Daftar `O` | PASS | terbuka, 14 item, klik item 7 pindah ke 7 dan menutup, Escape menutup dan fokus kembali |
| Catatan `N` | PASS | terbuka, berisi catatan slide |
| Tombol Sebelumnya / Berikutnya | PASS | berfungsi, tombol 44px |
| Slide tidak aktif | PASS | `inert` |
| Fokus keyboard | PASS | outline solid 3px, urutan Tab logis |
| Cetak PDF | PASS | 15 halaman |
| Judul slide 2 dan 14 setelah `text-wrap:balance` | PASS | dilihat langsung, pemenggalan wajar |
| Layar penuh `F` | TIDAK TERVERIFIKASI | ditolak oleh Chrome headless, perlu dicoba manual |
| Data asli di gambar | PASS | semua data contoh, berlabel "Data contoh" |

## Temuan di luar deck
Judul modal `Review Tiket Jira UQA` di aplikasi memakai warna inline `#0747a6`, kontras rendah di mode gelap. Terlihat di `assets/jira-atas.png`. Belum diperbaiki.

## Ulang 26-11-2026
| Item | Hasil | Bukti |
|---|---|---|
| Batas bawah 1016px slide 3 sampai 14 | PASS | maksimal 1016 |
| Error JS | PASS | tidak ada |
| Tanda pisah panjang | PASS | 0 |
| Slide 4, 5, 6, 14 dilihat langsung | PASS | tidak ada teks terpotong atau tumpang tindih |
| Navigasi keyboard, daftar, catatan | TIDAK DIULANG | logika navigasi tidak diubah, jumlah slide dibaca otomatis |

## Ulang setelah slide QCDSM, FRD, dan struktur
| Item | Hasil | Bukti |
|---|---|---|
| Jumlah slide | PASS | 18 |
| Gambar | PASS | semua dimuat, rasio sesuai |
| Batas bawah 1016px slide 3 sampai 17 | PASS | maksimal 1016 |
| PDF | PASS | 18 halaman |
| Error JS, em dash | PASS | 0 |
| Slide 3, 5, 9 dilihat langsung | PASS | tidak ada teks terpotong |
