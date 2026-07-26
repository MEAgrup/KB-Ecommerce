---
id: tts-segmentasi-002
title: Ngitung target belanja iklan dari Take Rate
platform: tiktok-shop
kategori: segmentasi-toko
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: 2026-04 (benchmark) / 2026-01 (aturan per tahap)
sources:
  - file: TikTok Benchmark (Google Sheets)
    bagian: "kolom TR benchmark, update 26 April 2026"
  - file: Library_Tiktok.md
    bagian: "§tabel S1–S4 baris Take rate; §How agencies can use this playbook"
related: [tts-segmentasi-000, tts-segmentasi-001, tts-benchmark-001, tts-gmvmax-002, tts-benchmark-003]
decisions: [K1-D-CONFLICT-02]
---

# Ngitung target belanja iklan dari Take Rate

## Ringkasan

**Take Rate = belanja iklan ÷ GMV.** Cara pakainya: ambil TR benchmark kategori lu, sesuaikan sesuai tahap toko, lalu itu jadi patokan berapa persen dari GMV yang wajar dibelanjain buat iklan. Ini satu-satunya cara di materi ini buat ngitung budget iklan yang gak asal tebak.

> **Catatan tangga toko.** Pengali per tahap di entry ini pakai tangga **S1–S4**, yang
> sekarang diposisikan sebagai **lensa agency** — member gak punya cara ngecek dia S berapa.
> Tangga utama member-facing sekarang **Basic Seller** (`tts-segmentasi-000`). Cara hitung
> TR-nya tetap berlaku dan kepakai; yang perlu hati-hati cuma jangan bilang "toko lu S2"
> ke member.

## Kapan ini dipakai

Dipakai waktu member nanya "budget iklan gw harusnya berapa" atau "iklan gw kemahalan gak". Juga dipakai buat nyetel ROI target di GMV Max.

**Yang perlu diperhatiin:** ini patokan **rasio**, bukan angka rupiah. Kalau GMV naik, budget wajarnya naik. Jadi jangan diterjemahin jadi "budget iklan Rp X per bulan" terus dipatok.

## Isi

**Langkahnya empat:**

1. **Cari Level 3 Category** produk lu di Seller Center. Bukan kategori menurut lu.
2. **Ambil TR benchmark** kategori itu dari `tts-benchmark-001`.
3. **Sesuaikan sesuai tahap toko** (`tts-segmentasi-001`):
   - S1 → benchmark **+50%**
   - S2 → **sama dengan** benchmark
   - S3 → benchmark **−20%**
   - S4 → benchmark **−30%**
4. **Kali GMV** buat dapat angka rupiahnya.

**Contoh hitungan** — toko Beauty & Personal Care, GMV Rp 20 juta/hari:

- TR benchmark Beauty = **13%**
- GMV Rp 20 juta/hari ≈ $1.180/hari → masuk **S2**
- S2 → target TR = sama dengan benchmark = **13%**
- Budget iklan wajar ≈ Rp 20 juta × 13% = **Rp 2,6 juta/hari**

Kalau toko yang sama masih S1 (misal GMV Rp 5 juta/hari): TR target = 13% × 1,5 = **19,5%**, jadi budget wajar ≈ Rp 975 ribu/hari. Persentasenya lebih besar, angkanya lebih kecil — dan itu memang cara kerjanya.

**Kenapa toko baru targetnya lebih tinggi:** toko baru belum punya data organik, belum punya video yang perform, belum punya pembeli lama. Iklan yang jadi mesinnya. Toko besar punya traffic organik dan konten kreator yang jalan sendiri, jadi porsi iklannya boleh lebih kecil.

**Catatan penting soal angka di materi sumber:** `Library_Tiktok.md` (Januari 2026) ngasih contoh "brand Beauty perlu readjust TR ke **16%**". Benchmark terbaru (April 2026) buat Beauty = **13%**. Angka 16% itu kemungkinan besar dari versi benchmark yang lebih lama. **Pakai 13%**, dan kalau ada mentor yang ngutip 16% dari materi Library, itu yang perlu dikoreksi.

## Angka & patokan

| Patokan | Nilai | Sumber |
|---|---|---|
| Definisi Take Rate | Ads spend ÷ GMV | Library_Tiktok §tabel S1–S4 |
| Pengali per tahap | S1 +50% / S2 =benchmark / S3 −20% / S4 −30% | idem |
| TR benchmark per kategori | 1%–13% tergantung kategori | TikTok Benchmark, 26 Apr 2026 |

## Yang bikin gagal

**Baca TR benchmark sebagai desimal.** Beauty = **13%**, bukan 0,13%. Di beberapa versi tabel yang udah dikonversi, angkanya muncul sebagai `0.13`. Salah baca di sini bikin budget salah 100×.

**Pakai TR sebagai target yang harus dicapai.** TR itu patokan kewajaran, bukan KPI. Toko yang TR-nya di bawah target dan GMV-nya tumbuh sehat gak perlu "dinaikin belanjanya".

**Ngitung TR dari GMV iklan aja.** Pembaginya **total GMV toko**, bukan GMV yang datang dari iklan. Ini kesalahan hitung yang paling sering, dan hasilnya bikin TR keliatan jauh lebih besar dari sebenernya.

**Pakai benchmark kategori tetangga.** Rentangnya 1% (Jewellery, Handphone) sampai 13% (Beauty). Salah kategori artinya salah 13×.

## Pertanyaan diagnosa

1. **Level 3 Category resminya apa?** Cek di Seller Center, jangan dari member.
2. **GMV harian rata-rata 30 hari berapa?** Buat nentuin tahap.
3. **TR sekarang berapa — dan pembaginya total GMV atau GMV dari iklan?** Cek cara hitungnya sebelum nilai angkanya.
4. **Angka TR yang dipakai persen atau desimal?** Satu pertanyaan yang nyegah salah 100×.

## Batasan

Pengali per tahap (+50%, −20%, −30%) masih nyangkut di `D-CONFLICT-02` karena tangga tahapnya belum diputuskan. Yang aman dipakai sekarang: benchmark kategorinya dan cara hitungnya. Pengalinya pakai dengan catatan bahwa penentuan tahapnya masih bisa geser.
