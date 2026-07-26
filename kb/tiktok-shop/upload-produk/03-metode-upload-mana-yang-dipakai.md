---
id: tts-upload-003
title: Kategori produk yang aturannya beda per platform
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
    bagian: "Artikel Terkait 8A — Upload Mechanism untuk Produk dengan Panduan Berbeda (2026-04-09)"
related: [tts-upload-001, tts-upload-005, tts-kebijakan-iklan-002]
decisions: []
---

# Kategori produk yang aturannya beda per platform

## Ringkasan

Empat kelompok kategori, dan **tiga dari empat aturannya beda antara Tokopedia dan TikTok Shop.** Yang paling penting dipahamin: ada produk yang **boleh dijual di Tokopedia tapi gak bisa di TikTok Shop** — dan solusinya bukan banding, tapi setel listing-nya jadi **Tokopedia only**.

## Kapan ini dipakai

Dipakai **sebelum** upload, buat mastiin produknya bisa masuk. Cek ini duluan buat produk yang sensitif: susu formula, produk bayi, obat, alkohol, barang bekas.

## Isi

| Kategori | Tokopedia | TikTok Shop |
|---|---|---|
**Invite-only** (mis. susu formula bayi, kartu SIM) | Bisa upload langsung | **Perlu apply authorization** |
**Restricted** (mis. pompa ASI, botol bayi) | Perlu isi atribut wajib | Perlu isi atribut wajib |
**Unsupported di TikTok Shop** | Bisa upload | **Gak bisa** — switch ke Tokopedia only |
**Prohibited** | Gak boleh | Gak boleh |

**Baris pertama** — invite-only: Tokopedia bisa langsung, TikTok Shop butuh izin. Apply lewat `Seller Center → Qualification Center`, dan **jangan upload sebelum izinnya turun.**

**Baris ketiga** yang paling sering bikin bingung. Produk yang "unsupported" di TikTok Shop bukan produk terlarang — cuma gak didukung di kanal itu. Contoh yang disebut sumber di bagian kesalahan upload: **alkohol, rokok, jasa (services), dan barang bekas (secondhand)**. Buat produk tipe itu, listing-nya diset **Tokopedia only** — bukan dipaksa masuk TikTok Shop.

Catatan nyambung: kondisi **New / Secondhand** cuma ada di Tokopedia (`tts-upload-001`), yang konsisten dengan barang bekas gak didukung TikTok Shop.

**Baris keempat** — prohibited: dua platform sama-sama nolak. Daftar industri terlarang dari sisi iklan di `tts-kebijakan-iklan-002`.

**Lima kesalahan upload yang disebut sumber**, plus cara benerinnya:

| Kesalahan | Cara benerin |
|---|---|
Listing produk yang gak didukung (alkohol, rokok, jasa, barang bekas) | Cek daftar kebijakan sebelum upload |
Gak lampirin dokumen yang diperlukan buat kategori restricted | Upload dokumen approval — expiry, **BPOM**, lisensi |
Jual barang bermerek tanpa otorisasi | Lengkapi Brand Authorization dulu (`tts-upload-005`) |
Upload produk invite-only tanpa izin | Apply lewat Seller Center → Qualification Center |
Ngabaikan update kebijakan | Cek update product policy secara rutin |

## Yang bikin gagal

**Maksa produk unsupported masuk TikTok Shop.** Solusinya Tokopedia only, bukan banding.

**Upload invite-only sambil nunggu izin.** Izin dulu, upload belakangan.

**Ngira dokumen BPOM cuma buat obat.** Kategori restricted lain juga bisa minta dokumen.

**Ngira aturan dua platform sama.** Tiga dari empat kelompok beda.

## Pertanyaan diagnosa

1. **Produknya masuk kelompok mana dari empat?** Cek ini sebelum apa pun.
2. **Kalau invite-only atau restricted — dokumen atau izinnya udah ada?**
3. **Kalau unsupported di TikTok Shop — listing-nya udah diset Tokopedia only?**
4. **Produknya bermerek orang lain?** Itu jalur terpisah (`tts-upload-005`).

## Batasan

Contoh kategori di tabel cuma dua per kelompok — daftar lengkapnya gak ada di materi. Buat produk yang gak jelas masuk kelompok mana, cek daftar kebijakan resmi di Seller Center, jangan ditebak dari kemiripan.
