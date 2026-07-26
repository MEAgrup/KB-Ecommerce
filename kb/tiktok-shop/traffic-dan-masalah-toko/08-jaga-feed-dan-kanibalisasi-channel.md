---
id: tts-traffic-008
title: Deteksi kanibalisasi antar channel dan jaga trafik For You
platform: tiktok-shop
kategori: traffic
depth: 3
status: canonical
confidence: sedang
sensitif_waktu: false
valid_as_of: 2026-04
sources:
  - file: Day_2_TSP__1_.md, bagian "Attribution among channels cannibalize; safeguard FEED; detect via single-channel GPM; how to understand FEED disrupted"
related: [tts-metrik-001, tts-traffic-006]
decisions: []
---

# Deteksi kanibalisasi antar channel dan jaga trafik For You

## Ringkasan
Channel trafik bisa saling makan: iklan berbayar atau search kadang cuma nyerap konversi yang sebenernya bakal datang gratis dari For You feed. Cara deteksinya: pantau GPM per channel. Kalau satu channel naik pas channel lain turun, kemungkinan lagi terjadi kanibalisasi — bukan pertumbuhan beneran. Prioritas jaga trafik For You feed karena itu sumber organik paling gede.

## Kapan ini dipakai
Buat seller yang udah main banyak channel (organik + berbayar) dan mau tahu apakah belanja iklannya nambah kue atau cuma mindahin kue. Butuh data cukup per channel — nggak relevan buat yang baru mulai.

## Isi
1. Baca GPM per channel, bukan cuma GPM total.
2. Sinyal kanibalisasi: satu channel naik, channel lain turun di periode sama, sementara total nggak nambah banyak.
3. Prioritaskan For You feed: kalau trafik berbayar naik tapi organik feed anjlok, cek apakah lu bayar buat orang yang tadinya gratis.

## Angka & patokan

| Konsep | Rumus | Sumber |
|---|---|---|
| Sinyal deteksi | pantau GPM per channel; satu naik–satu turun = indikasi tekanan | Day_2_TSP__1_.md |
| Contoh conversion rate per channel (ilustrasi sumber) | 20%, 50%, 33,3%, 0% antar channel berbeda | Day_2_TSP__1_.md |

## Pertanyaan diagnosa
1. Waktu iklan dinyalain, trafik organik For You-nya ikut turun nggak?
2. Total GMV beneran nambah, atau cuma pindah dari organik ke berbayar?
3. Lu udah misahin GPM per channel, atau masih baca angka gabungan?

## Batasan
Mekanisme atribusi & apakah channel saling nekan bisa beda antara platform China dan TikTok Shop ID. Perlakukan sebagai kerangka diagnosa, konfirmasi pola aktual dari data toko sendiri.
