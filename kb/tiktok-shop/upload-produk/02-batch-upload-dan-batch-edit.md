---
id: tts-upload-002
title: Batch upload dan batch edit produk
platform: tiktok-shop
kategori: upload-produk
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-04
sources:
  - file: knowledge_base_basic_seller.txt
    bagian: "Artikel Terkait 8A — Batch Publish / Batch Edit / Batch Edit Images (2026-04-09); 8B (2025-09-22)"
related: [tts-upload-001, tts-upload-004, tts-produk-006]
decisions: []
---

# Batch upload dan batch edit produk

## Ringkasan

Tiga alat batch dengan batas yang beda-beda: **batch publish** (satu template = satu kategori), **batch edit** (pilih maks 50.000 produk, tapi maks 5.000 per template), **batch edit images** (maks 200 produk). Aturan yang paling sering bikin gagal: **jangan tambah atau hapus baris/kolom di template.**

## Kapan ini dipakai

Dipakai kalau SKU-nya banyak dan mau hemat waktu. Buat volume kecil atau mau cepat go live, single upload lebih cepat (`tts-upload-001`).

Ini juga alat utama buat naikin **Pertumbuhan Basic Product** — salah satu kriteria Basic Seller (`tts-segmentasi-000`).

## Isi

**Batch Publish — tiga langkah:**

1. **Download template** — pilih platform (**Tokopedia only / TikTok Shop only / Both**) dan kategori produk. **Cuma bisa 1 kategori per template.**
2. **Isi informasi** — **jangan tambah atau hapus baris/kolom.** Field wajib ditandai **kotak merah**. Yang wajib: Product Name, Product Description, Main Product Image, Parcel Weight, Variation 1, Retail Price, Warehouse, Quantity
3. **Upload template**

**Batch Edit Product:**
- Filter produk berdasarkan status, kategori, nama/ID/SKU
- Pilih produk — maks **50.000**
- Download template, ada **5 jenis**: Sale info, Basic info, Shipping info, Images info, Product properties info — atau All info
- **Maks 5.000 produk per template**
- Upload template yang udah dimodifikasi

Perhatiin dua batas yang beda: bisa **pilih** 50.000, tapi tiap template maks **5.000**. Jadi 50.000 produk = 10 template.

**Batch Edit Images:**
- Pilih sampai **200 produk**
- Upload gambar produk, deskripsi, video, gambar variasi secara bulk

**Kapan pakai yang mana**, dari sumber:

| Metode | Kapan |
|---|---|
Single Upload | Volume produk kecil, mau go live lebih cepat |
Bulk Upload | Banyak SKU, mau hemat waktu |

## Angka & patokan

| | Nilai |
|---|---|
Kategori per template batch publish | 1 |
Maks produk dipilih buat batch edit | 50.000 |
Maks produk per template batch edit | 5.000 |
Jenis template batch edit | 5 (+ All info) |
Maks produk batch edit images | 200 |

## Yang bikin gagal

**Nambah atau hapus baris/kolom di template.** Disebut eksplisit sebagai hal yang gak boleh.

**Campur beberapa kategori di satu template batch publish.** Satu template satu kategori.

**Pilih 50.000 produk lalu heran templatenya nolak.** Maks 5.000 per template.

**Lupa isi field kotak merah.** Itu yang wajib, dan upload-nya gagal kalau kosong.

**Salah pilih platform di template.** Tokopedia only / TikTok Shop only / Both — dipilih di awal, dan nentuin kolom apa yang muncul.

## Pertanyaan diagnosa

1. **Berapa SKU, dan berapa kategori?** Kategori nentuin berapa template yang perlu.
2. **Yang mau diedit apa — harga, gambar, atau info dasar?** Nentuin jenis template mana.
3. **Template-nya pernah dibuka di Excel dan disave ulang?** Kadang itu yang ngubah struktur kolomnya.
4. **Platform tujuannya Tokopedia, TikTok Shop, atau dua-duanya?**

## Batasan

Sumbernya nyebut bagian "Common Upload Issues & How to Fix Them" tapi isinya cuma satu kalimat: "cek, perbaiki, dan coba lagi". **Daftar error uploadnya gak ada.** Kalau member kena error spesifik, gak ada rujukannya di materi ini.
