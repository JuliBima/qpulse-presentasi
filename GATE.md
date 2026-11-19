# GATE: Presentasi Q-PULSE

Dijalankan dengan Puppeteer + Chrome headless. Tanggal 2026-11-15.

| Item | Hasil | Bukti |
|---|---|---|
| Jumlah slide | PASS | 14 |
| Gambar dimuat | PASS | 15 dimuat, 0 bermasalah, dimensi cocok atribut width/height |
| Tanda pisah panjang (R-02) | PASS | 0 em dash |
| Kata terlarang | PASS | tidak ada |
| Kontras teks | PASS | 0 elemen kontras rendah di 14 slide |
| Batas bawah 1016px | PASS | slide konten <= 1016. Slide 1, 2, 14 memakai panel penuh 1080 (latar, bukan konten) |
| Gambar keluar panggung | PASS | hanya slide 1, disengaja |
| Overflow horizontal | PASS | 1366, 1024, 390, 844 lebar: scrollWidth sama dengan lebar |
| Request gagal / error JS | PASS | tidak ada |
| Panah kiri/kanan, Home, End | PASS | End 14/14, Home 1/14, dua kali kanan 2/14, kiri tetap di slide 2 (fragmen mundur) |
| Daftar `O` | PASS | terbuka, 14 item, klik item 7 pindah ke 7 dan menutup, Escape menutup dan fokus kembali |
| Catatan `N` | PASS | terbuka, berisi catatan slide |
| Tombol Sebelumnya / Berikutnya | PASS | berfungsi, tombol 44px |
| Slide tidak aktif | PASS | `inert` |
| Fokus keyboard | PASS | outline solid 3px, urutan Tab logis |
| Cetak PDF | PASS | 14 halaman, 5066 KB |
| Judul slide 2 dan 14 setelah `text-wrap:balance` | PASS | dilihat langsung, pemenggalan wajar |
| Layar penuh `F` | TIDAK TERVERIFIKASI | ditolak oleh Chrome headless, perlu dicoba manual |
| Data asli di gambar | PASS | semua data contoh, berlabel "Data contoh" |

## Temuan di luar deck
Judul modal `Review Tiket Jira UQA` di aplikasi memakai warna inline `#0747a6`, kontras rendah di mode gelap. Terlihat di `assets/jira-atas.png`. Belum diperbaiki.
