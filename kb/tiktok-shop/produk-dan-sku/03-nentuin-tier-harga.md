---
id: tts-produk-003
title: Nentuin tier harga yang layak dimasukin
platform: tiktok-shop
kategori: produk-dan-sku
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: false
valid_as_of: 2026-01
sources:
  - file: Library_Tiktok.md
    bagian: "§Product Analysis, Step 3 — Pinpoint core price tier"
related: [tts-produk-002, tts-produk-008, tts-produk-004]
decisions: []
---

# Nentuin tier harga yang layak dimasukin

## Ringkasan

Angka yang paling penting di seluruh bagian produk: **tier harga $5+ nyumbang 61% GMV tapi cuma 21% pesanan.** Artinya mayoritas duit di TikTok Shop ada di produk di atas $5, sementara mayoritas *transaksi* ada di produk murah. Kalau lu jualan di tier bawah, lu ngejar banyak transaksi buat GMV yang kecil.

## Kapan ini dipakai

Dipakai waktu nentuin produk mana yang didorong, dan waktu member ngeluh "udah banyak yang laku tapi omzetnya segitu-segitu aja". Sering itu masalah tier harga, bukan masalah volume.

## Isi

**Sebaran GMV vs pesanan per tier harga:**

| Tier harga | Pangsa GMV | Pangsa pesanan |
|---|---|---|
| $0–1 | 4% | **27%** |
| $1–2 | 9% | 22% |
| $2–3 | 10% | 15% |
| $3–5 | 16% | 16% |
| **$5+** | **61%** | 21% |

Baca baris pertama dan terakhir bareng-bareng: tier $0–1 itu **27% dari semua pesanan tapi cuma 4% GMV**. Tier $5+ kebalikan — 21% pesanan, 61% GMV. Selisih efisiensinya besar sekali.

**Dua saran dari playbook, tergantung kondisi toko:**

- **Udah punya Hero SKU** → cek apakah Hero SKU-nya di atas $5. Kalau belum, pertimbangkan **bundling** buat naikin harga satuannya sampai masuk tier itu.
- **Belum punya Hero SKU** → tier **$5+ direkomendasikan sebagai titik masuk.**

Poin pertama itu yang paling kepakai buat UMKM Indonesia, karena banyak yang produknya memang di bawah $5 dan gak bisa dinaikin harganya begitu aja. Jalannya bukan naikin harga — jalannya **bundling**: gabungin jadi paket biar nilai per transaksinya masuk tier atas. Caranya di `tts-produk-008`.

**Konversi kasar buat konteks:** $5 itu sekitar Rp 80 ribuan. Jadi patokannya: produk atau bundle di atas ± Rp 80 ribu ada di tier yang nyumbang mayoritas GMV platform. Konversi ini gw hitung buat konteks — bukan angka dari sumber, dan gerak sama kurs.

## Angka & patokan

| Patokan | Nilai | Sumber |
|---|---|---|
| Pangsa GMV tier $5+ | 61% | Library_Tiktok §Step 3 |
| Pangsa pesanan tier $5+ | 21% | idem |
| Pangsa pesanan tier $0–1 | 27% (GMV cuma 4%) | idem |
| Rekomendasi titik masuk kalau belum ada Hero SKU | Tier $5+ | idem |

## Yang bikin gagal

**Naikin harga produk buat masuk tier.** Itu bukan yang disaranin. Yang disaranin bundling — nilai transaksinya naik karena isinya nambah, bukan karena marginnya digedein.

**Ngejar volume di tier bawah.** 27% pesanan buat 4% GMV artinya kerja packing dan risiko SLA-nya besar, hasilnya kecil. Dan risiko SLA itu nyata — lihat `tts-pelanggaran-seller-001`.

**Nganggep tier $5+ berarti produk mahal.** $5 itu sekitar Rp 80 ribu. Banyak produk UMKM udah di atas itu tanpa perlu diapa-apain.

## Pertanyaan diagnosa

1. **Harga satuan produk utama lu berapa?** Konversi ke USD kasar buat cocokin tier.
2. **Kalau di bawah $5 — bisa dibundle jadi paket di atas $5?** Ini pertanyaan kunci.
3. **GMV lu tinggi atau cuma jumlah pesanannya tinggi?** Dua hal beda, dan bedanya ada di tier harga.

## Batasan

Sebaran tier ini data platform, bukan data kategori. Kategori tertentu (Handphone, Jewellery) hampir semuanya di tier atas; kategori lain (Stationery, Food) mayoritas di bawah. Jadi angka 61% ini gambaran platform, dan buat kategori spesifik sebarannya bisa beda jauh. Sumbernya gak ngasih pecahan per kategori.

Semua tier dalam USD. Kurs bergerak, jadi batas rupiahnya bergerak juga.
