---
id: tts-upload-001
title: Upload satu produk — empat bagian yang harus diisi
platform: tiktok-shop
kategori: upload-produk
depth: 1
audience: member
aksi_oleh: member
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-04
sources:
  - file: knowledge_base_basic_seller.txt
    bagian: "Artikel Terkait 8A — Menambahkan dan Mengelola Produk, Add Single Product (2026-04-09)"
related: [tts-upload-002, tts-upload-004, tts-produk-005, tts-upload-005]
decisions: []
---

# Upload satu produk — empat bagian yang harus diisi

## Ringkasan

Empat bagian: **Basic Information, Product Details, Sales Information, Shipping.** Yang paling sering bikin gagal bukan isinya, tapi spesifikasi gambar — rasio **1:1**, minimum **600 × 600 px**, maks **9 gambar**, maks **10MB**. Ada Image Editor di Seller Center buat benerin rasio tanpa aplikasi lain.

## Kapan ini dipakai

Dipakai buat volume produk kecil atau kalau mau cepat go live. Buat banyak SKU, pakai batch upload (`tts-upload-002`).

Entry point: `Products > Manage Products`.

## Isi

**1. Basic Information**
- Product Name, Category, Brand, Attributes
- **Gambar:** maks **9** per produk, rasio **1:1**, minimum **600 × 600 px**, maks **10MB**
- **Video** (opsional): rasio 1:1, 9:16, atau 16:9; maks **20MB**
- **Image Editor** — bisa langsung edit di Seller Center: hapus background, ganti warna background, atur rasio

**2. Product Details**
- Deskripsi dengan teks dan bullet points
- Sampai **30 banner atau gambar terkait**
- **Size chart** kalau perlu
- **Khusus Tokopedia:** pilih kondisi **New** atau **Secondhand**

**3. Sales Information**
- Setup variasi produk — **cuma variasi pertama yang bisa nambah gambar**
- **Discount** waktu listing, default berlaku **30 hari**
- **Pre-order** lewat ikon settings
- **Product Purchase Limit** — batas beli minimum dan maksimum per produk

**4. Shipping**
- Berat paket **1–100 kilogram**
- **Instant dan Sameday cuma di Tokopedia**
- **Shipping Insurance cuma di Tokopedia**

## Angka & patokan

| | Nilai |
|---|---|
Maks gambar per produk | 9 |
Rasio gambar | 1:1 |
Minimum resolusi | 600 x 600 px |
Maks ukuran gambar | 10MB |
Maks ukuran video | 20MB |
Maks banner di deskripsi | 30 |
Berat paket | 1-100 kg |
Durasi default diskon listing | 30 hari |

## Yang bikin gagal

**Upload gambar rasio bebas.** 1:1 itu spesifikasi. Pakai Image Editor kalau salah.

**Naruh gambar di variasi kedua atau ketiga.** Cuma variasi pertama yang bisa.

**Lupa diskon listing default cuma 30 hari.** Habis itu balik harga normal tanpa pemberitahuan.

**Ngarepin Instant/Sameday jalan di TikTok Shop.** Cuma Tokopedia.

**Upload produk bermerek tanpa Brand Authorization.** Lihat `tts-upload-005`.

## Pertanyaan diagnosa

1. **Berapa SKU yang mau diupload?** Kalau banyak, pakai batch.
2. **Gambar produknya udah 1:1 dan minimal 600x600?**
3. **Produknya bermerek orang lain?** Cek otorisasi dulu.
4. **Ada variasi?** Ingat cuma variasi pertama yang bisa nambah gambar.

## Batasan

Nama field dan lokasi menu bisa geser. Sumbernya juga gak nyebut **jumlah maksimum variasi** per produk dan gak nyebut batas panjang judul produk — dua hal yang sering ditanya.
