---
id: tts-upload-004
title: Product Media Center — penyimpanan gambar dan video
platform: tiktok-shop
kategori: upload-produk
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: 2024-03
sources:
  - file: knowledge_base_basic_seller.txt
    bagian: "Artikel Terkait 8C — Pusat Media Produk, Seller Center (2024-03-14)"
related: [tts-upload-001, tts-upload-002, tts-produk-005]
decisions: []
---

# Product Media Center — penyimpanan gambar dan video

## Ringkasan

Penyimpanan aset di Seller Center yang gunanya nyelesaiin masalah upload lambat dan format yang gak ketrima. Yang paling berguna: bisa **export URL gambar secara massal** lalu URL-nya dipakai di template batch upload — jadi gak perlu upload gambar satu-satu di dua tempat.

**Perhatiin: spesifikasinya beda dari spesifikasi listing produk.** Di sini gambar maks **5MB**, di listing maks **10MB**.

## Kapan ini dipakai

Dipakai kalau member sering upload produk (batch), atau kalau ngeluh upload gambarnya lambat dan sering gagal.

## Isi

**Manfaat yang disebut sumber:**
- Penyimpanan buat gambar dan video
- Nyelesaiin masalah upload lambat dan format yang gak tersedia
- Bisa langsung dipakai waktu listing atau maintain produk

**Spesifikasi upload:**

| | Spesifikasi |
|---|---|
**Gambar** | JPG, PNG, atau JPEG · maks **5MB** · ukuran **> 300 × 300** |
**Video** | MP4 · maks **20MB** · rasio 9:16 sampai 16:9 · durasi **< 60 detik** |

**Alur pakai bareng batch upload** — ini bagian yang paling menghemat waktu:
1. Copy URL gambar yang di-generate
2. Pilih beberapa gambar, klik **Export URLs**
3. Isi URL-nya di kolom template: Main product image / size chart / qualification / SKU images

Jadi buat batch upload 500 produk, gambarnya diupload sekali ke Media Center, URL-nya diexport, lalu ditempel ke template. Bukan upload 500 gambar dua kali.

**Beda spesifikasi yang perlu diperhatiin:**

| | Media Center | Listing produk |
|---|---|---|
Maks gambar | 5MB | 10MB |
Minimum resolusi | > 300 x 300 | 600 x 600 |
Durasi video | < 60 detik | (gak disebut) |

Gambar yang lolos spesifikasi Media Center (300×300) **belum tentu memenuhi rekomendasi listing** (600×600). Jadi pakai 600×600 sebagai patokan biar aman di dua tempat.

## Yang bikin gagal

**Pakai 300 x 300 karena itu minimum Media Center.** Rekomendasi listing 600 x 600. Pakai yang lebih besar.

**Upload gambar > 5MB ke Media Center.** Batasnya beda dari batas listing.

**Video lebih dari 60 detik.** Ditolak di Media Center walau ukurannya kecil.

**Upload gambar dua kali** — sekali ke Media Center, sekali ke listing. Pakai Export URLs.

## Pertanyaan diagnosa

1. **Member upload produk secara batch?** Kalau iya, alur Export URLs yang paling ngirit.
2. **Gambar-gambarnya ukuran berapa?** Batas 5MB di sini lebih ketat dari listing.
3. **Ada video yang lebih dari 60 detik?**

## Batasan

Sumbernya **Maret 2024** — vintage tertua di batch 2, dua tahun lebih. Spesifikasi ukuran dan format jenis hal yang direvisi berkala. Cek di layar sebelum dipakai buat keputusan.

Sumbernya juga gak nyebut **batas total penyimpanan** — berapa gambar atau berapa GB yang bisa disimpan. Itu yang paling wajar ditanya buat toko dengan ribuan SKU.
