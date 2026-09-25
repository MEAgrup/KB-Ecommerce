---
id: shp-produk-107
title: Produk turun, diblokir, atau dihapus — dua penyebab yang sering ketuker
platform: shopee
kategori: produk
depth: 2
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-08
sources:
  - file: daftar-produk---kebijakan-pelanggaran-produk/tentang-pelanggaran-produk.md
    bagian: "bagian Diturunkan vs Diblokir/Dihapus"
related: [shp-produk-009, shp-produk-011, shp-produk-013, shp-produk-017, shp-produk-018, shp-produk-019, shp-produk-020, shp-produk-029, shp-akun-104, shp-performa-103, fnd-analisa-002]
decisions: []
---

# Produk turun, diblokir, atau dihapus — dua penyebab yang sering ketuker

## Ringkasan
Member sering nyamain semua "produk turun" jadi satu masalah, padahal ada dua jalur penyebab yang mekanismenya beda total: **(A) pelanggaran kebijakan** (dapat poin penalti, ada tenggat perbaikan, tercatat di Kesehatan Toko) atau **(B) penjualan mingguan turun** (murni performa, algoritma pencarian menurunkan eksposur karena sinyal permintaan melemah — bukan hukuman). Salah diagnosa jalur ini bikin member benerin hal yang salah: sibuk cek pelanggaran padahal masalahnya di funnel, atau sebaliknya nyalahin "algoritma" padahal ada pelanggaran tercatat yang belum dibenerin.

## Kapan ini dipakai
Saat member laporan "produk saya turun/hilang dari pencarian" atau "produk saya dihapus/diblokir", sebelum kasih saran perbaikan — pastikan dulu jalur mana yang berlaku, karena resepnya beda.

## Isi

### Cara membedakan cepat
Cek satu tempat dulu: **Kesehatan Toko** di Seller Centre, bagian **Poin Penalti**.

- **Ada poin penalti tercatat / produk masuk daftar Diturunkan-Diblokir-Dihapus** → ini jalur A (pelanggaran). Penyebabnya sudah pasti tertulis di kolom "Alasan pelanggaran", bukan misteri.
- **Tidak ada poin penalti, tapi traffic/penjualan produk tetap turun** → ini kemungkinan besar jalur B (performa), bukan pelanggaran.

### Jalur A — Pelanggaran kebijakan
Tiga level tindakan Shopee, beda dampak:

| Tindakan | Kenapa | Dampak | Cara benerin |
|---|---|---|---|
| **Diturunkan** | Kategori salah, atau foto/video mengandung konten gak sesuai ketentuan (mis. terindikasi vulgar/tidak pantas) | Produk tetap tayang & bisa dicari, tapi peringkat pencarian turun sementara (maks. ±1 hari kerja untuk pulih setelah diperbaiki) | `shp-produk-009` — ajukan banding (maks. 14 hari kerja) atau perbaiki fotonya |
| **Diblokir** | Pelanggaran yang butuh perbaikan sebelum tenggat (mis. label Shopee tidak resmi, spam nama/deskripsi, harga dinaikkan sebelum promo) | Produk gak tayang sampai diperbaiki; kalau lewat tenggat → dihapus | `shp-produk-011`, `shp-produk-018` sesuai jenis pelanggarannya |
| **Dihapus** | Barang dilarang/dibatasi secara hukum, HAKI, atau pelanggaran berat lainnya | Permanen, dapat poin penalti, bisa berujung pembatasan akun kalau berulang | `shp-produk-013` — daftar lengkap kategori barang terlarang; sebagian besar TIDAK bisa di-banding, cuma bisa dicegah ke depan |

**Catatan taksonomi:** `shp-produk-013` judulnya "Meningkatkan Kualitas Daftar Produk yang Dihapus/Diblokir", tapi isinya sebenarnya daftar barang terlarang/kebijakan (satu keluarga dengan `shp-produk-011` dan `shp-produk-017`) — bukan tips kualitas listing seperti `shp-produk-019/020/029`. Kalau member nanya soal ini, jangan diarahkan ke tips foto/judul; arahkan ke daftar kebijakan.

### Jalur B — Performa mingguan turun
Kalau gak ada pelanggaran tercatat, penurunan biasanya karena sinyal performa produk itu sendiri melemah — pencarian Shopee mengutamakan produk dengan sinyal permintaan yang masih hidup (klik, konversi, kecepatan jual). Dua kemungkinan:

1. **Fatik sementara** — konten/kreatif mulai jenuh, tapi conversion rate masih sehat. Solusinya refresh foto/video, bukan ganti produk. Lihat `fnd-analisa-002` untuk cara bedain ini dari poin 2.
2. **Momentum beneran hilang** — CR turun tajam, kompetitor sejenis juga ikut turun (tanda pasar bergeser, bukan cuma toko ini). Ini saatnya siapkan produk pengganti, bukan maksa produk lama.

Cek posisi produk di matriks 4 kuadran (`shp-performa-102`) — produk yang mulai jadi "Evaluasi" (traffic & CR sama-sama rendah) adalah kandidat paling jelas untuk jalur B ini.

## Yang bikin gagal
- Menganggap semua penurunan sebagai "algoritma jahat" tanpa cek Kesehatan Toko dulu — kalau ternyata ada poin penalti, waktu yang dipakai memperbaiki foto/konten sia-sia sampai pelanggarannya dibereskan duluan.
- Sebaliknya, langsung menuduh "pasti ada pelanggaran" padahal Kesehatan Toko bersih — penyebabnya performa, bukan kebijakan, jadi solusinya beda (refresh konten / ganti produk, bukan ajukan banding).
- Mengajukan banding untuk kategori "Dihapus" yang sebenarnya gak bisa dibanding (barang terlarang secara hukum) — buang waktu, mending fokus ke produk lain.

## Pertanyaan diagnosa
- Sudah dicek halaman Kesehatan Toko / Pelanggaran Produk — ada poin penalti atau catatan pelanggaran untuk produk ini?
- Kalau ada pelanggaran: statusnya Diturunkan, Diblokir, atau Dihapus? (beda tenggat dan beda apakah bisa banding)
- Kalau gak ada pelanggaran: CR produk ini masih sehat atau ikut turun tajam? Kompetitor sejenis juga turun?
- Konten/foto produk ini sudah berapa lama gak di-refresh?

## Batasan
Entry ini nge-mapping penyebab, bukan pengganti baca detail tiap jenis pelanggaran — untuk daftar lengkap kategori pelanggaran dan cara perbaikannya, tetap rujuk `shp-produk-011`, `shp-produk-013`, `shp-produk-017`, `shp-produk-018`. Deteksi jalur B (performa) di entry ini adalah kerangka umum, bukan formula pasti — Shopee gak mempublikasikan detail algoritma pencarian organiknya.
