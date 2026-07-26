---
id: tts-pelanggaran-seller-001
title: SLA pengiriman dan kapan pesanan dibatalin sistem
platform: tiktok-shop
kategori: kebijakan-dan-kepatuhan/pelanggaran-seller
depth: 1
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: tidak-diketahui
sources:
  - file: Pedoman_Konten_TikTok.md
    bagian: "§Pelanggaran Seller: Pengiriman (Fulfillment) — Standar SLA Pengiriman Reguler"
related: [tts-pelanggaran-seller-002, tts-segmentasi-005]
decisions: [K1-D-OUTDATED-04]
---

# SLA pengiriman dan kapan pesanan dibatalin sistem

> 📌 **Di-unblock (K1-D-OUTDATED-04, opsi C):** bagian actionable dibuka. Target angka SLA riil (kirim ≤24 jam, keterlambatan ≤4%, pembatalan ≤2,5%) ada di `tts-segmentasi-005`. Nama menu/UI cek Seller Center terkini.

> ⛔ **Entry ini `blocked` — jangan kutip angka harinya ke member.**
> Materi sumbernya nol penanggalan, dan angka SLA jenis aturan yang kalau salah bikin
> member **kena penalti nyata** (Late Dispatch → poin pelanggaran → Order Volume Limit).
> Butuh satu screenshot tabel SLA dari halaman kebijakan TikTok Shop Indonesia buat
> dibuka. Lihat `D-OUTDATED-04`.
> Bagian **DO / AVOID** di bawah tetap aman dipakai — itu praktik operasional, bukan
> angka aturan, dan gak berubah walau SLA-nya geser.

## Ringkasan

Untuk pesanan yang dibayar **setelah jam 12 siang**, hitungan prosesnya mulai hari berikutnya. Kalau pesanan belum dikirim sampai akhir Hari ke-3, sistem **membatalkan otomatis**. Yang paling sering bikin member salah hitung: batas waktunya bukan "3 hari dari sekarang" — tergantung jam pembayaran.

## Kapan ini dipakai

Dipakai waktu member kena Late Shipment atau pesanannya kebatalan sendiri. Juga dipakai **sebelum** kampanye besar, buat ngitung kapasitas.

## Isi

Ilustrasi dari sumber, untuk pesanan dibayar setelah jam 12 siang hari Senin:

| Hari | Keterangan |
|---|---|
| **Senin (Day 0)** | Pesanan dibayar (setelah pukul 12 siang) |
| **Selasa (Day 1)** | Hari proses pesanan dimulai |
| **Rabu (Day 2)** | Hari pemrosesan masih diperbolehkan |
| **Kamis (Day 3)** | Batas akhir pengiriman tepat waktu (on-time shipment) |
| **Jumat (Day 4)** | Lewat batas → Late Shipment atau dibatalkan otomatis |

Dua konsekuensi yang disebut sumber:
- Kalau pesanan **gak dikirim sampai akhir Hari ke-3 (EOD)**, pesanan **dibatalkan otomatis oleh sistem**
- Seller yang **sering telat** kirim bisa kena sanksi atau penalti sesuai kebijakan platform

**Kapan pelanggaran fulfillment biasanya kejadian**, menurut sumber — ini bagian yang paling kepakai buat nyegah:
- Periode kampanye besar atau flash sale
- Produk tiba-tiba viral dan pesanan membludak, melebihi kapasitas tim operasional

Jadi risikonya gak tersebar rata. Risikonya numpuk di momen yang justru dikejar seller.

**Yang harus dilakukan (DO), dari sumber:**
- **Perkirakan jumlah pesanan dan tenaga kerja** yang dibutuhkan sejak awal, biar pemenuhan tetap sesuai SLA
- Aktifkan fitur **Pre-Order** kalau udah gak sanggup penuhin pesanan baru sesuai waktu
- Pastikan **pick-up dilakukan setelah semua paket discan**, bukan sebelumnya

**Yang harus dihindari (AVOID), dari sumber:**
- Ngisi angka **"99999"** di stok produk biar keliatan selalu tersedia
- Cuma ngejar peningkatan pesanan atau GMV tanpa mempertimbangkan kemampuan operasional
- **Membiarkan partner logistik (3PL) ngambil paket sebelum semuanya siap**
- Gak paham aturan SLA, yang bisa ganggu kelancaran operasional

## Yang bikin gagal

**Ngitung dari tanggal order, bukan dari jam pembayaran.** Pembayaran setelah jam 12 siang bikin Day 0 dan Day 1 beda hari. Ini sumber salah hitung yang paling sering.

**Ngejar viral tanpa ngitung kapasitas packing.** Dua momen yang paling sering bikin kena — kampanye dan viral — dua-duanya momen yang seller kejar. Yang bikin kena bukan kurang laku, tapi terlalu laku tanpa persiapan.

**Isi stok 99999.** Kelihatan bikin toko keliatan siap; hasilnya pesanan masuk melebihi barang yang ada, dan itu jadi Seller Fault Cancellation.

**Nyuruh 3PL pick-up sebelum semua paket discan.** Disebut eksplisit sebagai hal yang harus dihindari.

## Pertanyaan diagnosa

1. **Pesanan yang kena telat itu dibayar jam berapa?** Nentuin Day 0-nya kapan.
2. **Kejadiannya di periode kampanye, flash sale, atau ada produk yang viral?** Kalau iya, masalahnya kapasitas, bukan proses.
3. **Stoknya diisi angka realistis atau angka besar biar aman?** Cek ini walau member gak nyebut.
4. **Pre-Order udah dinyalain, atau masih terima pesanan reguler padahal udah kewalahan?**

## Batasan

Angka hari di entry ini **belum diverifikasi** dan itu sebabnya entry-nya `blocked`.

Ilustrasi di sumber cuma nyakup satu skenario: pesanan dibayar setelah jam 12 siang, di hari kerja. Sumbernya gak bahas pesanan sebelum jam 12, weekend, atau hari libur nasional. Jangan diturunkan sendiri — beda satu hari di sini artinya beda antara on-time dan penalti.
