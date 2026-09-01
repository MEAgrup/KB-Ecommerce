---
id: shp-pengiriman-101
title: SOP dasar inbound-outbound biar gak gagal kirim tepat waktu
platform: shopee
kategori: pengiriman-dan-pesanan
depth: 2
status: canonical
confidence: sedang
sensitif_waktu: false
valid_as_of: 2026-09
sources:
  - file: riset-eksternal/sop-gudang-fulfillment-ecommerce-inbound-outbound.md
    bagian: "riset web — alur receiving-putaway-storage-picking-packing-shipping dan penyebab umum gagal kirim tepat waktu"
related: [shp-pengiriman-063, shp-pengiriman-065, shp-pengiriman-068, shp-pengiriman-069, shp-pengiriman-074]
decisions: []
---

# SOP dasar inbound-outbound biar gak gagal kirim tepat waktu

## Ringkasan
Artikel resmi Shopee (`shp-pengiriman-068`, `shp-pengiriman-069`, `shp-pengiriman-074`) jelasin APA yang perlu dioptimalkan di proses inbound/outbound, tapi gak selalu jelasin KENAPA gagal kirim tepat waktu sering terjadi meski gudangnya udah rapi. Tiga penyebab paling umum ternyata bukan soal stok atau kecepatan packing — tapi soal alur kerja antar orang yang gak jelas.

## Kapan ini dipakai
Saat member sudah rajin cek stok dan proses pesanan tapi masih sering telat kirim atau kena penalti keterlambatan — sebelum nyalahin kurir atau volume pesanan, cek dulu alur internal tokonya.

## Isi

### Alur dasar gudang: enam tahap
Proses fulfillment (baik gudang sendiri atau ruang kecil di rumah) idealnya ngikutin enam tahap ini secara berurutan, masing-masing dengan aturan yang jelas siapa yang tanggung jawab:

1. **Receiving** — barang masuk dari supplier dicek dulu kondisinya sebelum disimpan (lihat `shp-pengiriman-068` untuk versi resmi Shopee-nya).
2. **Putaway** — barang ditaruh di lokasi simpan yang konsisten, gampang ditemukan lagi.
3. **Storage** — penyimpanan tertata, bukan numpuk tanpa sistem.
4. **Picking** — ambil barang sesuai pesanan (lihat `shp-pengiriman-065`).
5. **Packing** — kemas sesuai standar (label, bukti pengiriman — lihat `shp-pengiriman-074`).
6. **Shipping** — serah terima ke kurir (lihat `shp-pengiriman-069` untuk optimasi outbound).

### Tiga penyebab paling umum gagal kirim tepat waktu
Bukan stok habis — meski itu penyebab yang paling gampang dituduh, tiga hal ini justru lebih sering jadi akar masalah:

1. **Komunikasi antarbagian terputus.** Pola paling umum: tim CS/admin sudah konfirmasi pembayaran, tapi info itu gak sampai ke yang packing. Atau sebaliknya, barang sudah siap kirim tapi belum ada instruksi resmi untuk diserahkan ke kurir. Solusinya bukan kerja lebih cepat, tapi bikin satu titik informasi yang semua orang cek (papan status pesanan, grup khusus update stok/pesanan, atau sistem pesanan yang statusnya otomatis ke-update).
2. **Pencatatan manual yang gak konsisten.** Toko kecil yang masih andalin catatan manual/Excel gampang kehilangan jejak begitu volume pesanan naik — pesanan yang sudah dibayar bisa kelewat, atau pesanan lama ke-duplikat proses. Minimal pakai satu sistem pencatatan yang semua orang akses yang sama (bukan catatan pribadi masing-masing).
3. **Semua pesanan diperlakukan sama, gak ada prioritas.** Tanpa aturan mana yang harus diproses duluan (misal: pesanan yang sudah lewat batas waktu SLA, atau pesanan dari promo besar), pesanan yang seharusnya dikirim duluan malah tertahan di antrian yang gak terurut.

### Cara mulai benerin alur ini
- Tentukan satu jam batas cut-off harian untuk proses pesanan (misal: semua pesanan masuk sebelum jam 14.00 harus diproses hari itu), dan siapa yang bertanggung jawab kalau lewat.
- Pisahkan pesanan berdasarkan urgensi (SLA hampir habis vs masih ada waktu), bukan diproses First In First Out mentah-mentah.
- Kalau tokonya sudah lebih dari satu orang yang pegang proses pesanan, pastikan status "sudah dibayar → sedang di-pack → siap kirim" bisa dilihat semua orang yang terlibat, bukan cuma di kepala satu orang.

## Yang bikin gagal
Menganggap keterlambatan kirim itu semata soal "kurang cepat kerja" — kalau akar masalahnya komunikasi/pencatatan yang putus, nambah orang atau kerja lembur gak menyelesaikan apa-apa; masalahnya di alurnya, bukan di kecepatan orangnya.

## Pertanyaan diagnosa
- Kapan terakhir kali ada pesanan telat kirim — penyebabnya stok, atau info yang gak sampai ke bagian packing?
- Toko ini masih pakai catatan manual/Excel untuk tracking pesanan, atau sudah ada sistem yang statusnya otomatis ke-update?
- Ada aturan prioritas pesanan (mana yang diproses duluan), atau semua pesanan diperlakukan sama urutan masuknya?
- Siapa yang bertanggung jawab kalau pesanan lewat batas waktu proses harian?

## Batasan
Ini kerangka SOP umum dari praktik fulfillment e-commerce (riset publik), bukan SOP resmi Shopee — untuk detail fitur dan aturan resmi tetap rujuk `shp-pengiriman-063/065/068/069/074`. Implementasinya perlu disesuaikan skala toko: toko rumahan dengan 1-2 orang gak perlu sistem gudang seketat toko dengan tim fulfillment sendiri, tapi prinsip "satu titik informasi yang jelas" tetap berlaku di skala manapun.

Sumber riset: [SPIL — Inbound Logistic Adalah](https://www.spil.co.id/blogs/inbound-logistic-adalah/), [Kompasiana — Mengapa Banyak Bisnis Online Gagal Kirim Pesanan Tepat Waktu](https://www.kompasiana.com/marketingdazo0944/6881d7bbed6415773c277da2/mengapa-banyak-bisnis-online-gagal-kirim-pesanan-tepat-waktu), [MuatMuat — Struktur Warehouse](https://muatmuat.com/blog/struktur-warehouse/).
