---
id: tts-produk-004
title: Baca kompetitor buat nentuin celah
platform: tiktok-shop
kategori: produk-dan-sku
depth: 3
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: false
valid_as_of: 2026-01
sources:
  - file: Library_Tiktok.md
    bagian: "§Product Analysis, Step 4 — Identify key competitors"
related: [tts-produk-002, tts-produk-003, tts-produk-005]
decisions: []
---

# Baca kompetitor buat nentuin celah

## Ringkasan

Dua angka per kompetitor, dan yang menarik justru kombinasinya: **pangsa GMV** (seberapa besar dia sekarang) dan **laju pertumbuhan GMV** (arahnya ke mana). Kompetitor yang besar tapi **menurun** itu peluang. Kompetitor yang kecil tapi **tumbuh cepat** itu ancaman yang harus dipantau. Ukuran sendiri gak ngasih tahu apa-apa.

## Kapan ini dipakai

Dipakai setelah kategori dan tier harga ketemu (`tts-produk-002`, `tts-produk-003`), sebelum nyusun listing. Ini `depth: 3` karena butuh data pesaing — kalau member belum punya akses datanya, langkah ini bisa dilewat dulu.

## Isi

**Rumus pangsa GMV**, dari sumber:

> GMV Share = GMV SKU ÷ GMV sub-kategori atau tier harga

Perhatiin pembaginya: **sub-kategori atau tier harga**, bukan seluruh pasar. Jadi ini pangsa di kolam yang relevan, bukan pangsa nasional. Ini yang bikin angkanya kepakai buat toko kecil — di sub-kategori dan tier harga yang sempit, pangsa 4% itu berarti.

**Cara nyimpulinnya**, contoh dari sumber:

| Kompetitor | Pangsa GMV | Pertumbuhan | Kesimpulan |
|---|---|---|---|
| Klien | 4% | +3% | Baseline |
| Kompetitor A | 6% | **−3%** | Pangsa lebih besar **tapi menurun** → peluang buat dilewatin |
| Kompetitor B | 2% | **+10%** | Pesaing potensial dengan momentum kuat → **pantau terus** |

Dua kesimpulan itu berlawanan dari yang biasanya orang ambil. Kompetitor A yang lebih besar bukan yang paling perlu dikhawatirin — dia yang paling mungkin dilewatin. Kompetitor B yang lebih kecil justru yang perlu dipantau, karena arahnya naik.

**Yang dibandingin juga harga satuannya.** Di contoh sumber: klien $9, Kompetitor A $8, Kompetitor B $10. Ini nyambung ke tier harga — kalau kompetitor yang tumbuh cepat harganya lebih tinggi, itu sinyal bahwa tier atas masih ada ruang.

**Cara pakainya praktis:** ambil 3–5 produk teratas di sub-kategori dan tier harga lu, catat empat hal per produk — harga satuan, pangsa GMV, laju pertumbuhan, dan judul produknya. Yang keempat buat langkah berikutnya (`tts-produk-005`).

## Yang bikin gagal

**Bandingin sama pemimpin pasar di kategori besar.** Pembaginya harus sub-kategori atau tier harga yang sama. Toko yang jualan hijab Rp 150 ribu gak dibandingin sama seluruh kategori Muslim Fashion.

**Fokus ke kompetitor terbesar.** Yang perlu dipantau yang tumbuh tercepat.

**Ngambil satu potret waktu.** Laju pertumbuhan butuh dua titik waktu. Tanpa itu, lu cuma punya separuh datanya — dan separuh yang kurang berguna.

## Pertanyaan diagnosa

1. **Sub-kategori dan tier harga lu apa persisnya?** Nentuin kolam pembandingnya.
2. **Lu punya akses data pangsa dan pertumbuhan pesaing, atau cuma bisa lihat listing-nya?** Kalau cuma listing, langkah ini terbatas dan mendingan langsung ke `tts-produk-005`.
3. **Ada pesaing kecil yang naik cepat di sub-kategori lu?** Itu yang perlu dipantau, bukan yang terbesar.

## Batasan

Data pangsa GMV dan laju pertumbuhan per kompetitor **bukan data yang semua member punya**. Di materi aslinya ini keluaran dashboard level agency. Member yang gak punya aksesnya bisa pakai kerangka bacanya buat observasi manual (harga, judul, ranking di pencarian) tapi gak bisa ngisi angka pangsanya.

Semua angka di contoh sumber ditandai "demo" — itu ilustrasi cara baca, bukan data pasar nyata.
