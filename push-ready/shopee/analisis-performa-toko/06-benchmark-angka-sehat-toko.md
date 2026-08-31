---
id: shp-performa-101
title: Benchmark angka sehat toko — ROAS, ACOS, CR, cancel rate, chat
platform: shopee
kategori: analisis-performa-toko
depth: 2
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-08
sources:
  - file: internal-tool-benchmark/standar-skor-performa-toko-shopee-mea-report-engine.md
    bagian: "Benchmark ROAS & ACOS", "Benchmark Traffic & Konversi", "Benchmark Repeat Order & Cancel Rate", "Benchmark Layanan Chat"
related: [shp-performa-102]
---

# Benchmark angka sehat toko — ROAS, ACOS, CR, cancel rate, chat

## Ringkasan
Angka-angka acuan ini adalah **standar kerja internal MEA Agency** yang dipakai untuk menilai kesehatan performa toko klien — bukan angka resmi yang dipublikasikan Shopee (Shopee sendiri tidak menerbitkan angka "sehat/tidak sehat" untuk metrik-metrik ini). Berguna sebagai kerangka acuan cepat, tapi standar sehat sebenarnya bisa berbeda tergantung kategori produk dan strategi toko.

## Isi

| Metrik | Batas sehat | Catatan |
|---|---|---|
| ROAS iklan | ≥4x sehat, ≥2x masih efisien, <2x butuh audit | ROAS = omzet iklan ÷ biaya iklan |
| ACOS iklan | ≤25% sehat, ≤40% waspada, >40% tidak sehat | ACOS = biaya iklan ÷ omzet iklan (kebalikan ROAS) |
| CTR iklan | ≥0,5% sehat | Rasio klik dibanding tayangan |
| Conversion Rate (CR) toko | ≥1,5% sehat | Standar bisa beda jauh per kategori produk |
| Repeat order rate | >25% kuat, >15% moderat, ≤15% lemah | Dari total pembeli |
| Cancel rate | <5% sehat, 5-10% waspada, >10% kritis | Dari total pesanan |
| Retur | <1% dari total pesanan | |
| Tingkat chat direspon | >95% | |
| Konversi order dari chat | >20% | Pembeli ÷ penanya |
| CSAT chat | >85% | |
| Waktu respon chat | <1 jam | |

## Kapan ini dipakai
Untuk mentor/tim yang membantu member membaca dashboard performa toko dan butuh angka acuan cepat, bukan pengganti target yang disesuaikan per kategori produk dan tahap bisnis toko.

## Batasan
**Ini bukan angka resmi dari Shopee.** Shopee tidak mempublikasikan threshold "sehat/tidak sehat" untuk ROAS, ACOS, CR, atau cancel rate — angka di atas adalah kalibrasi internal MEA dari pengalaman menangani banyak klien, dan bisa berbeda untuk kategori produk yang sangat spesifik (misalnya kategori dengan margin tipis vs tebal butuh ROAS target yang beda). Kalau dipakai untuk member, sampaikan sebagai "standar yang biasa kami pakai", bukan sebagai aturan resmi Shopee.

## Pertanyaan diagnosa
- ROAS dan ACOS toko ini sekarang di rentang mana dari tabel di atas?
- Cancel rate toko ini masih di bawah 5%, atau sudah masuk zona waspada/kritis?
- Kategori produk toko ini termasuk yang marginnya tipis atau tebal — apakah target ROAS standar di atas masih masuk akal, atau perlu disesuaikan?
