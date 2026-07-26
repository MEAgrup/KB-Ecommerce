---
id: tts-segmentasi-005
title: Rating toko, Rating kinerja penjual & Power Shop — target angka
platform: tiktok-shop
kategori: segmentasi-toko
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-07
sources:
  - file: seller-center-extract.md
    bagian: "Rating Toko, Rating Kinerja Penjual, Power Shop, Analitik pascapembelian"
related: [tts-segmentasi-000, tts-segmentasi-001, tts-afiliasi-008]
decisions: [K1-D-OUTDATED-04, K1-D-GAP-06]
---

# Rating toko, Rating kinerja penjual & Power Shop — target angka

## Ringkasan
Tiga sistem penilaian toko di Seller Center, lengkap dengan **angka target-nya** (ID, Jul 2026).
Ini yang nentuin toko buka benefit atau kena penalti.

## Kapan ini dipakai
Waktu member nanya "target metrik toko berapa biar aman/naik", atau mentor mau diagnosa kenapa
benefit toko kekunci.

## 1. Rating Toko (skor dinamis 0–5)
Tiga komponen (bobot contoh, beda per kategori):
- **Kepuasan Produk (40%)** — ulasan negatif 60 hari; retur/refund krn kesalahan penjual 60 hari.
- **Pemenuhan Pesanan & Logistik (40%)** — pengiriman cepat 30 hari; % pembatalan krn kesalahan penjual 30 hari.
- **Customer Service (30%)** — waktu penanganan purnajual 60 hari; % respons 12 jam dalam 30 hari.

Skor buka benefit bertingkat: **2.5** pemasangan iklan · **3.5** afiliasi & akses CRM · **4.0**
Flash Sale & Akselerator · **4.3** Power Shop · **4.5** peningkatan trafik +30%.
Toko baru: selesaikan **30 pesanan valid dalam 60 hari** buat mulai dapat skor.

## 2. Rating Kinerja Penjual (poin, default 200, skala 0–1000)
Target lolos tiap metrik:

| Metrik | Target |
|---|---|
| Pembatalan krn kesalahan penjual | ≤ 2,5% |
| Keterlambatan pengiriman | ≤ 4% |
| Kecepatan pengiriman | ≥ 90% |
| Pengiriman besok tiba | ≥ 90% |
| Keterlambatan Instan / Same-day | ≤ 5% |
| Ulasan negatif krn masalah penjual | ≤ 0,6% |
| Ulasan negatif krn masalah layanan | ≤ 0,6% |
| Retur & dana krn kesalahan penjual | ≤ 1,5% |
| Respons 12 jam | ≥ 85% |
| Waktu respons rata-rata | < 1 jam |
| Kepuasan atas chat | ≥ 70% |

**Settlement (pencairan) = 3 hari** (Indonesia).

## 3. Power Shop (predikat penjual)
Syarat kualifikasi:
- Penjualan **≥ Rp10.000.000 ATAU 200 pesanan**
- Pembeli unik **≥ 15**
- Rating toko **≥ 4,0**
- Rating kinerja akun **> 150**
- Pelanggaran penipuan **0**

Manfaat: visibilitas Rekomendasi, eksposur Pencarian, fitur eksklusif.

## Pertanyaan diagnosa
1. Benefit toko kekunci? Cek skor Rating Toko vs tingkat benefit di atas.
2. Poin kinerja turun? Cek metrik mana yang lewat target di tabel Rating Kinerja Penjual.

## Batasan
Angka & bobot bisa berubah dan beda per kategori (sensitif waktu) — konfirmasi di Seller Center.
Catatan: "Basic Seller sembilan kriteria" (`K1-D-GAP-06`) kemungkinan merujuk gabungan metrik di
sini + Power Shop — **perlu Nerissa konfirmasi pemetaan pastinya** sebelum dipakai sebagai "9 kriteria".
