---
id: shp-iklan-104
title: Pilih SKU yang siap diiklankan dulu, baru soal budget
platform: shopee
kategori: iklan-dan-promosi
depth: 2
status: canonical
confidence: sedang
sensitif_waktu: false
valid_as_of: 2026-09
sources:
  - file: internal-tool-benchmark/tiksmart-cek-sku-ready.md
    bagian: "logika kesiapan SKU untuk diiklankan"
related: [shp-iklan-205, shp-iklan-103, shp-performa-102, shp-produk-107]
decisions: []
---

# Pilih SKU yang siap diiklankan dulu, baru soal budget

## Ringkasan
Pertanyaan "iklan saya kok boncos" sering dijawab dengan ngoprek budget dan bidding duluan, padahal masalahnya lebih sering ada di SKU yang diiklankan itu sendiri — belum siap ditawar iklan sama sekali. Sebelum ngatur budget, cek dulu dua lapis: **relevansi** (SKU, judul, deskripsi, gambar nyambung ke keyword yang dibidik atau nggak) dan **performa** (CTR/CVR-nya udah kebukti bagus secara organik atau belum).

## Kapan ini dipakai
Saat member mau mulai/nambah iklan tapi bingung produk mana yang harus didorong duluan, atau saat iklan udah jalan tapi hasilnya jelek dan mau tahu apa yang perlu dibenerin sebelum nambah budget.

## Isi

### Lapis 1 — Relevansi: apakah SKU ini "nyambung" ke keyword yang dibidik?
Iklan pencarian di Shopee muncul karena sistem mencocokkan keyword yang dibidik dengan data produk. Kalau datanya gak relevan, iklan bisa tayang ke orang yang salah (CTR rendah) atau malah gak tayang optimal sama sekali. Empat titik yang menentukan relevansi:

1. **Judul produk** — apakah kata kunci utama yang mau dibidik memang ada di judul? Judul yang cuma nama brand tanpa kata kunci pencarian gak akan matching ke keyword yang relevan.
2. **Deskripsi** — apakah detail produk (bahan, ukuran, fungsi) mendukung kata kunci yang sama, atau cuma template generik yang gak spesifik ke produk ini?
3. **Gambar** — apakah gambar utama menunjukkan produk yang sesuai dengan apa yang dicari orang lewat keyword itu? Gambar yang ambigu (gak jelas produk apa) bikin orang yang klik dari iklan langsung bounce begitu masuk halaman.
4. **Kategori & atribut** — kategori yang salah bikin produk gak muncul untuk pencarian yang seharusnya relevan, sekalipun sudah diiklankan (lihat `shp-produk-107` soal produk yang diturunkan karena kategori salah — masalah yang sama juga bikin iklan gak efektif).

### Lapis 2 — Performa: apakah CTR/CVR-nya udah kebukti bagus?
Relevansi doang gak cukup — SKU yang paling siap diiklankan adalah yang **sudah kebukti performanya secara organik** dulu, baru diperbesar lewat iklan:

- **CTR rendah** (di bawah rata-rata toko) → biasanya masalah di gambar utama atau judul, bukan di budget. Ganti materinya dulu, jangan naikkan bid.
- **CTR oke tapi CVR rendah** → orang tertarik klik tapi gak jadi beli. Ini tanda halaman produknya yang bermasalah (harga, ongkir, review, deskripsi kurang meyakinkan) — bukan soal iklan/bid, benerin listing-nya dulu. Ini sama persis dengan kategori "Bocor Traffic" di matriks 4 kuadran (`shp-performa-102`).
- **CTR & CVR sudah bagus secara organik** → ini SKU yang paling aman untuk diiklankan, karena sudah kebukti duluan lewat traffic gratis sebelum ditambah biaya iklan.

### Urutan yang disarankan
1. Cek performa organik SKU dulu (CTR, CVR, sudah berapa order) sebelum diiklankan.
2. Kalau CVR-nya masih rendah, benerin listing dulu (foto, judul, deskripsi) — jangan iklankan produk yang halamannya belum siap "menutup" pembeli.
3. Setelah CVR terbukti sehat, baru masuk ke keputusan budget dan bidding (lihat `shp-iklan-205` untuk cara evaluasi ROAS/ACOS setelah iklan jalan).

## Yang bikin gagal
- Mengiklankan produk yang CVR-nya belum terbukti hanya karena "stoknya banyak" atau "margin-nya besar" — traffic yang dibeli lewat iklan cuma nyampe ke halaman yang gak siap convert, hasilnya ROAS jelek meski keyword-nya relevan.
- Menganggap masalah rendahnya performa iklan selalu soal bid/budget, padahal akar masalahnya sering di lapis relevansi (judul/gambar gak nyambung ke keyword) atau lapis konversi (halaman produk yang lemah).
- Menaikkan budget di SKU yang CTR-nya rendah, alih-alih benerin gambar/judulnya dulu — budget lebih besar untuk materi yang sama cuma mempercepat boncos, bukan memperbaiki hasil.

## Pertanyaan diagnosa
- SKU yang mau diiklankan ini — judul dan gambarnya sudah mengandung keyword yang mau dibidik?
- Sebelum diiklankan, CTR dan CVR organiknya gimana dibanding rata-rata toko?
- Kalau CTR rendah: materi (judul/gambar) yang perlu dibenahi, atau memang keyword-nya kurang relevan?
- Kalau CTR oke tapi CVR rendah: halaman produknya (harga, ongkir, review) yang perlu dicek dulu sebelum nambah budget iklan?

## Batasan
Kerangka dua-lapis di atas adalah cara berpikir umum untuk menilai kesiapan SKU sebelum diiklankan, bukan skor otomatis dari Shopee. Untuk cek relevansi dan performa SKU secara sistematis dari data toko sendiri (bukan cuma dilihat manual satu-satu), tim bisa arahkan member ke fitur cek SKU siap iklan di Tiksmart.ai — ada versi gratis untuk coba sebelum member atau mentor mengulik manual dari dashboard Shopee.
