---
id: shp-akun-104
title: Kenapa akun/toko dibatasi — cek poin penalti dulu sebelum nebak penyebab lain
platform: shopee
kategori: akun-dan-toko
depth: 2
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-08
sources:
  - file: umum---akun-dan-keamanan/mengapa-akun-saya-dibatasi.md
    bagian: "daftar penyebab pembatasan akun"
related: [shp-akun-101, shp-akun-103, shp-akun-010, shp-akun-009, shp-akun-014, shp-penalti-002, shp-penalti-003, shp-penalti-005, shp-toko-021, shp-toko-030, shp-produk-107]
decisions: []
---

# Kenapa akun/toko dibatasi — cek poin penalti dulu sebelum nebak penyebab lain

## Ringkasan
Pembatasan akun/toko di Shopee hampir selalu berujung ke satu sumber: **sistem poin penalti**. `shp-akun-010` mendaftar belasan penyebab spesifik (spam, promosi disalahgunakan, produk dihapus >20 kali, dll), tapi semuanya bermuara ke mekanisme yang sama — poin terkumpul di Kesehatan Toko sampai ambang tertentu, baru toko dibatasi. Diagnosa yang benar dimulai dari cek poin penalti, bukan dari menebak satu-satu dari daftar panjang penyebab.

## Kapan ini dipakai
Saat member laporan "akun/toko saya dibatasi" atau "kenapa saya gak bisa jualan lagi" — sebelum menebak dari daftar panjang kemungkinan penyebab, cek dulu apakah ada jejak poin penalti yang bisa dibaca langsung.

## Isi

### Langkah diagnosa
1. **Buka Kesehatan Toko → Poin Penalti** di Seller Centre. Kalau ada poin aktif, deskripsi pelanggarannya biasanya tertulis di sana — gak perlu nebak dari daftar panjang di `shp-akun-010`.
2. **Kalau poin penalti nol tapi masih gak bisa login/akses toko** — itu kemungkinan besar masalah teknis (OTP, password, verifikasi wajah, koneksi), bukan soal kebijakan. Cek `shp-akun-009` (login/OTP) atau `shp-akun-014` (kendala aplikasi) dulu — jangan buru-buru simpulkan "kena banned".
3. **Kalau poin penalti ada dan sudah tinggi** — baca `shp-penalti-005` (sistem & ketentuan poin) untuk tahu ambang batasnya, dan `shp-toko-021` untuk cara mencegah nambah poin baru sambil proses banding jalan.

### Kenapa "cek poin dulu" penting
Daftar penyebab pembatasan di `shp-akun-010` sangat panjang (>3 toko dengan data sama, penyalahgunaan promosi, chat melanggar, SPayLater nunggak, dll) — kalau tim langsung nebak satu-satu dari daftar itu tanpa cek poin penalti dulu, waktu diagnosa jadi lama dan gampang salah arah. Poin penalti di Kesehatan Toko adalah satu tempat yang merangkum SEMUA jenis pelanggaran itu jadi satu angka yang bisa dilihat langsung.

### Pola yang sering muncul di lapangan
Dari pengalaman lapangan (`shp-akun-101`, `shp-akun-103`): toko yang kena pembatasan mendadak biasanya sudah punya sinyal peringatan sebelumnya (poin penalti naik bertahap, notifikasi pelanggaran yang diabaikan) — bukan benar-benar "tiba-tiba" tanpa jejak. Rutin cek Kesehatan Toko (`shp-toko-030`) sebelum poin menumpuk adalah pencegahan yang lebih murah daripada mengurus banding setelah dibatasi.

## Yang bikin gagal
- Langsung mengajukan banding tanpa tahu pelanggaran spesifiknya apa — banding yang gak menjawab alasan pelanggaran biasanya ditolak.
- Menyalahkan masalah teknis (OTP/login) sebagai "kena banned" padahal poin penaltinya nol — dua masalah ini butuh solusi yang beda total.
- Menunggu sampai akun benar-benar dibatasi baru cek Kesehatan Toko, padahal poinnya bisa dipantau dari jauh-jauh hari.

## Pertanyaan diagnosa
- Sudah dicek Kesehatan Toko → Poin Penalti? Ada poin aktif atau nol?
- Kalau ada poin: pelanggaran apa yang tertulis di deskripsinya, dan sudah berapa lama?
- Kalau nol: masalahnya di login/OTP (masalah teknis) atau memang toko gak bisa diakses sama sekali (masalah pembatasan)?
- Toko ini sudah pernah dapat notifikasi pelanggaran sebelumnya yang belum ditindaklanjuti?

## Batasan
Entry ini kerangka diagnosa cepat, bukan pengganti baca detail tiap jenis pelanggaran — untuk daftar lengkap penyebab pembatasan tetap rujuk `shp-akun-010`, dan untuk mekanisme poin penalti secara resmi rujuk `shp-penalti-002/003/005`. Ambang berapa poin sampai toko dibatasi permanen gak dijelaskan detail di sumber yang tersedia — kalau member tanya angka pastinya, arahkan cek langsung di Seller Centre atau hubungi Customer Service Shopee.
