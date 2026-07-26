---
id: tts-traffic-010
title: After-sales — balas chat, komplain, retur, dan CRM pembeli
platform: tiktok-shop
kategori: traffic-dan-masalah-toko
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-07
sources:
  - file: seller-center-extract.md
    bagian: "Pembeli (CRM) · Analitik pascapembelian · Program jaminan dan layanan · Rating Kinerja Penjual (metrik layanan)"
related: [tts-segmentasi-005, tts-metrik-007, tts-metrik-003, tts-pelanggaran-seller-001]
decisions: []
---

# After-sales — balas chat, komplain, retur, dan CRM pembeli

## Ringkasan
Kerjaan setelah pesanan masuk sama nentuinnya dengan jualan itu sendiri: **customer service
menyumbang 30% Rating Toko**, dan retur tinggi nurunin trafik. Entry ini kumpulin target angka,
alat yang tersedia, dan urutan nanganinnya.

## Kapan ini dipakai
Waktu member nanya "gimana nanganin komplain/retur", "kenapa rating toko gw turun padahal jualan
jalan", atau mau otomatisasi follow-up pembeli.

## Target angka yang wajib dijaga
| Metrik layanan | Target |
|---|---|
| Tingkat respons 12 jam | ≥ 85% |
| Waktu respons rata-rata | < 1 jam |
| Tingkat kepuasan atas chat | ≥ 70% |
| Ulasan negatif krn masalah penjual / layanan | ≤ 0,6% |
| Retur & dana krn kesalahan penjual | ≤ 1,5% |
| Pembatalan krn kesalahan penjual | ≤ 2,5% |

Detail lengkap + Rating Toko & Power Shop ada di `tts-segmentasi-005`.

## Urutan kerja harian
1. **Balas chat dulu** — kejar respons <1 jam. Ini metrik paling gampang jeblok dan
   bobotnya besar (CS = 30% Rating Toko).
2. **Kirim tepat waktu** — maks. **24 jam**; pembatalan otomatis juga maks. 24 jam. Stok harus akurat
   biar gak batal/telat (`tts-pelanggaran-seller-001`).
3. **Pantau pascapembelian** — Seller Center → Analitik → **Analitik pascapembelian**: waktu tiap
   tahap (menunggu pengiriman → pengambilan → transit → tiba) dibanding rata-rata industri.
4. **Tangani retur cepat** — retur tinggi bukan cuma rugi uang, tapi **nurunin trafik ke live &
   SKU** (`tts-metrik-003`).

## Alat yang tersedia di Seller Center
- **CRM (menu Pembeli)** — program chat berbasis templat, sekali-waktu atau otomatis. Templat
  konversi tinggi: ingatkan produk di keranjang, ingatkan checkout, ucapan terima kasih pasca-beli,
  ingatkan harga turun, **minta ulasan**. Bisa kelola segmen pembeli & broadcast.
  (Akses CRM kebuka di Rating Toko **3.5**.)
- **Voucher ulasan / voucher chat** — dorong ulasan positif & konversi dari chat (lihat `tts-campaign-007`).
- **Asuransi Pengiriman Pengembalian Barang Pembeli** — penggantian ongkir hingga **Rp10.000**
  untuk pengiriman gagal / retur karena masalah pembelian. Biaya **Rp65 per pesanan**, bisa berhenti kapan saja.

## Pertanyaan diagnosa
1. Rating toko turun tapi penjualan naik? Cek komponen CS dulu (respons 12 jam & waktu penanganan purnajual).
2. Retur tinggi di satu SKU? Cek deskripsi/foto produk — biasanya ekspektasi gak cocok, bukan barangnya.
3. Ulasan sedikit? Pakai voucher ulasan + templat CRM "minta ulasan".

## Batasan
Angka target & biaya (Rp65/pesanan, Rp10.000) sensitif waktu — konfirmasi di Seller Center.
