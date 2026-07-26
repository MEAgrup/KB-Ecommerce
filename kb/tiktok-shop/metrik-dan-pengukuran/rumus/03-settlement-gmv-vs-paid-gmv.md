---
id: tts-metrik-003
title: Beda Settlement GMV dan Paid GMV
platform: tiktok-shop
kategori: metrik
depth: 3
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: 2026-04
sources:
  - file: Day_1_part_2_3_TSP.md, bagian "Shift from Paid GMV to Settlement GMV; refund before/after shipment"
related: [tts-metrik-001]
decisions: []
---

# Beda Settlement GMV dan Paid GMV

## Ringkasan
Paid GMV itu nilai yang dibayar saat checkout; Settlement GMV itu yang beneran settle setelah refund dipotong. Rumusnya Settlement GMV = Paid GMV × settlement rate. Poinnya: refund tinggi bukan cuma makan angka penjualan — refund tinggi juga nurunin trafik ke live atau ke SKU yang refund-nya banyak. **Aturan ini dikonfirmasi berlaku di TikTok Shop Indonesia** (`K2-D-OUTDATED-003`) — bukan cuma pola Douyin.

## Kapan ini dipakai
Buat seller yang GMV-nya keliatan bagus tapi profit tipis, atau yang ngeluh trafik live-nya tiba-tiba turun padahal penjualan sempet ramai.

## Isi
1. Bedain dua angka: yang checkout (paid) vs yang settle setelah refund.
2. Settlement rate = porsi order yang nggak di-refund. Makin banyak refund, makin kecil GMV efektif.
3. Refund itu dua skenario: sebelum barang dikirim vs sesudah dikirim — dampak biayanya beda.
4. Menurut sumber, refund tinggi di satu sesi live bisa nekan trafik live itu, dan refund tinggi di satu SKU bisa nekan trafik link produk itu.

## Angka & patokan

| Rumus | Bentuk | Sumber |
|---|---|---|
| Settlement GMV | Paid GMV × settlement rate | Day_1_part_2_3_TSP.md |

## Pertanyaan diagnosa
1. Seller ngukur performa dari angka checkout atau angka yang udah settle?
2. Refund numpuk di produk tertentu, di sesi live tertentu, atau merata?
3. Refund-nya kebanyakan sebelum kirim atau sesudah kirim?

## Batasan
Peralihan platform ke "Settlement GMV sebagai metrik utama" itu konteks China 2025–2026. Perlu diverifikasi apakah TikTok Shop ID sudah pakai metrik yang sama. Lihat D-OUTDATED-003.
