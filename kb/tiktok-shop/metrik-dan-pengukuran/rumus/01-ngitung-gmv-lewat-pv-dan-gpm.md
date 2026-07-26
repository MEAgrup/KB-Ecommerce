---
id: tts-metrik-001
title: Ngitung GMV lewat PV dan GPM
platform: tiktok-shop
kategori: metrik
depth: 1
status: canonical
confidence: tinggi
sensitif_waktu: false
valid_as_of: 2026-04
sources:
  - file: Day_1_part_2_3_TSP.md, bagian "CORE Methodology — GMV=PV*GPM/1000"
  - file: Day_2_TSP__1_.md, bagian "Total livestreaming GMV — traffic end x receiving end"
related: [tts-metrik-002, tts-metrik-004]
decisions: []
---

# Ngitung GMV lewat PV dan GPM

## Ringkasan
GMV di TikTok Shop dipecah jadi dua mesin: PV (jumlah tayangan/exposure) dan GPM (rupiah yang dihasilkan tiap 1.000 tayangan). Rumusnya GMV = PV × GPM / 1000. Kalau GMV mandek, jangan langsung nambah budget — cari tahu dulu yang lemah PV-nya atau GPM-nya, karena dua ini butuh perbaikan yang beda.

## Kapan ini dipakai
Tiap kali seller nanya "kenapa GMV gw turun/stuck". Ini kerangka diagnosa paling dasar sebelum masuk ke channel spesifik (live, short video, product card).

## Isi
1. PV = seberapa banyak orang/tayangan yang kena exposure. Naik lewat trafik (konten, search, iklan).
2. GPM = seberapa efisien tiap 1.000 tayangan dikonversi jadi rupiah. Dipecah lagi: GPM = AOV × CVR × 1000 (harga rata-rata × conversion rate).
3. Diagnosa cepat: PV rendah → masalah di sisi trafik/exposure. GPM rendah → masalah di sisi penawaran (harga, produk, konversi, script).

## Angka & patokan

| Rumus | Bentuk | Sumber |
|---|---|---|
| GMV | PV × GPM / 1000 | Day_1_part_2_3_TSP.md, slide CORE |
| GPM | AOV × CVR × 1000 | Day_1_part_2_3_TSP.md, slide CORE |

## Pertanyaan diagnosa
1. GMV turunnya barengan sama tayangan turun, atau tayangan tetap tapi yang beli berkurang?
2. Lu udah misahin: ini masalah narik orang (PV) atau masalah ngonversi orang (GPM)?
3. Kalau GPM turun, yang gerak harga rata-ratanya (AOV) atau conversion rate-nya (CVR)?

## Batasan
Rumus ini universal, tapi label metrik di dashboard TikTok Shop ID bisa beda. Pastikan padanan istilah di TikTok Seller Center sebelum ngajarin ke seller.
