---
id: tts-produk-002
title: Bikin Hero SKU dari nol pakai data kategori
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
    bagian: "§Product Analysis - Find the Hero SKU, Step 2"
related: [tts-produk-001, tts-produk-003, tts-produk-004, tts-produk-009]
decisions: []
---

# Bikin Hero SKU dari nol pakai data kategori

## Ringkasan

Kalau toko belum punya Hero SKU, jangan nunggu ada yang laku sendiri. Cara playbook-nya: pakai **insight kategori dan benchmark kompetitor** buat milih kandidat, bukan nebak dari produk favorit sendiri. Alat bacanya satu grafik dua sumbu: **pangsa pasar GMV** di sumbu X, **laju pertumbuhan GMV** di sumbu Y.

## Kapan ini dipakai

Dipakai buat toko yang gak punya SKU lewat 30 pesanan/hari. Juga dipakai waktu Hero SKU lama udah lewat umurnya dan belum ada pengganti (`tts-produk-007`).

## Isi

**Bacanya dua sumbu:**
- **Sumbu X = GMV Market Share** — seberapa besar kategori itu di pasar
- **Sumbu Y = GMV Growth Rate** — seberapa cepat kategori itu tumbuh

Dari kombinasi dua itu, kategori dikelompokkan jadi prioritas:

| Prioritas | Ciri | Artinya |
|---|---|---|
| **P0** | Kontribusi GMV kuat **dan** pertumbuhan solid | Prioritaskan |
| **P1** | Salah satu kuat: basis GMV besar tapi tumbuh lambat, **atau** basis kecil tapi tumbuh cepat | Layak dijajaki |

Contoh yang dipakai sumber (demo, bukan rekomendasi buat semua toko): Beauty & Personal Care jadi **P0** karena kontribusi GMV kuat plus momentum pertumbuhan solid. Food & Beverage punya basis GMV besar, Home Appliance punya potensi pertumbuhan menjanjikan — dua-duanya **P1**.

**Habis dapat kategori, tiga langkah lanjutan:**
1. **Tentuin tier harga** yang layak dimasukin — `tts-produk-003`
2. **Identifikasi kompetitor utama** di tier itu — `tts-produk-004`
3. **Optimasi selling point dan setup** listing-nya — `tts-produk-005`

Empat langkah itu berurutan, dan urutannya penting: kategori → harga → kompetitor → listing. Mulai dari listing tanpa tahu tier harganya itu ngoptimasi hal yang mungkin salah dari awal.

**Yang sering keliru dipahamin:** ini bukan nyuruh member pindah kategori. Ini nyuruh member milih **produk mana dari katalognya** yang paling mungkin jadi Hero, berdasarkan kategori mana yang lagi bergerak. Kalau katalognya cuma satu kategori, gunanya buat nentuin sub-kategori dan tier harga mana yang didorong.

## Yang bikin gagal

**Milih kategori yang paling cepat tumbuh saja.** Pertumbuhan tinggi di basis kecil itu P1, bukan P0. Kategori kecil yang tumbuh 200% bisa tetap terlalu kecil buat nampung Hero SKU.

**Milih berdasarkan produk favorit sendiri.** Ini yang paling sering, dan yang paling mahal — karena produk yang seller paling suka biasanya yang paling dia rasa "beda", dan "beda" bukan sinyal permintaan.

**Skip langkah tier harga.** Kategori bener tapi harga di tier yang salah bikin produknya gak ketemu pembeli. Lihat `tts-produk-003`.

## Pertanyaan diagnosa

1. **Katalog lu nyentuh berapa kategori?** Nentuin analisisnya di level kategori atau sub-kategori.
2. **Ada produk yang pesanannya naik pelan tapi konsisten?** Kandidat terbaik biasanya di situ, bukan di produk yang belum pernah laku.
3. **Udah tahu tier harga mayoritas GMV di kategori itu?** Kalau belum, itu langkah berikutnya.

## Batasan

Data kategori (grafik market share vs growth rate) itu **data yang gak semua member punya aksesnya** — sumbernya nampilin ini sebagai dashboard, dan yang ada di materi cuma contoh Q4'25 dalam bentuk gambar yang gak bisa diekstrak. Jadi kerangka bacanya bisa dipakai, tapi angka kategorinya perlu dicari dari sumber lain: Seller Center, Business Accelerator (`tts-benchmark-002`), atau riset manual.

Contoh P0/P1 di sumber ditandai "demo" — jangan dikutip sebagai rekomendasi kategori buat 2026.
