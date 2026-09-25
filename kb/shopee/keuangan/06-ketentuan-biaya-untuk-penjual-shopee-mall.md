---
id: shp-biaya-006
title: Ketentuan Biaya untuk Penjual Shopee Mall
platform: shopee
kategori: keuangan
depth: 2
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-07
sources:
  - file: keuangan---biaya-penjual/ketentuan-biaya-untuk-penjual-shopee-mall.md
    bagian: "artikel penuh"
related: [shp-biaya-001, shp-keuangan-003]
decisions: [S-D-CONFLICT-004]
---
# Ketentuan Biaya untuk Penjual Shopee Mall

## Ringkasan
Penjual Shopee Mall kena 2 biaya wajib: Biaya Administrasi (lihat `shp-biaya-001`) dan Biaya Pembayaran 1,8% (maks. Rp50.000/kuantitas produk, flat semua kategori, sudah termasuk PPN). Selama periode SKB PPh 23 aktif, gak perlu potong/setor PPh 23 sendiri.

## Kapan ini dipakai
Dipakai buat rincian Biaya Pembayaran khusus Shopee Mall (1,8%) — beda dari Biaya Administrasi yang juga berlaku buat semua status Penjual. Kalau soal Biaya Administrasi, arahkan ke `shp-biaya-001`.

## Isi

**1. Biaya Administrasi Penjual Shopee Mall**

Penjual yang telah bergabung dalam program Penjual Shopee Mall akan dikenakan biaya Administrasi Shopee Mall. Pelajari lebih lanjut tentang perhitungan dan ilustrasi[ Biaya Administrasi Penjual Shopee Mall](https://seller.shopee.co.id/edu/article/1344).

  

**2. Biaya Pembayaran Penjual Shopee Mall**

Biaya Pembayaran Penjual Shopee Mall adalah biaya yang dibebankan ke Penjual Shopee Mall sebesar 1,8% (dengan batas maksimum Rp50.000 per kuantitas produk) dari harga produk yang berhasil terjual dan berlaku **sama rata** untuk semua kategori produk. Total harga produk adalah **harga asli produk dikurangi total diskon dan/atau voucher diskon dari Penjual Shopee Mall**.

  

Biaya Pembayaran **tidak** akan dikenakan ke ongkir, diskon produk, dan/atau voucher diskon dari Penjual Shopee Mall. Biaya ini dipotong secara otomatis melalui sistem Shopee saat dana hasil penjualan dilepaskan ke Saldo Penjual.

  

Biaya Pembayaran Final Shopee Mall = (Harga Asli Produk – Diskon Produk dan/atau Voucher Diskon dari Penjual Shopee Mall) x 1,8% (dengan batas maksimum Rp50.000 per kuantitas produk).

  

*\*Biaya Pembayaran final sudah termasuk biaya Pajak Pertambahan Nilai (PPN) sesuai dengan Peraturan Pemerintah tentang Perpajakan yang berlaku.*

PT Shopee International Indonesia saat ini telah memiliki Surat Keterangan Bebas Pajak Penghasilan dengan No KET-00012/PPUT-CT/KPP.3010/2025 yang berlaku dari tanggal 3 Februari 2025 hingga 31 Desember 2025, di mana Anda tidak perlu melakukan pemotongan atau penyetoran PPh 23 atas biaya yang dibayarkan dan meminta pengembalian pembayaran PPh 23 tersebut kepada Shopee. 

  

Namun jika pembayaran pajak yang akan dilakukan berada diluar periode 13 Februari 2025 hingga 31 Desember 2025, maka Anda harus tetap melakukan kewajiban membayar pajak. Pelajari lebih lanjut terkait Surat Keterangan Bebas Pajak Penghasilan dan[ Bagaimana cara mengajukan pengembalian PPh 23?](https://seller.shopee.co.id/edu/article/20363).

  
  

**⚠️ Catatan**

  - Biaya Pembayaran sebesar 1,8% (dengan batas maksimum Rp50.000 per kuantitas produk) berlaku sama rata untuk semua kategori produk.
  - Biaya Pembayaran sudah termasuk biaya Pajak Pertambahan Nilai (PPN) sesuai dengan Peraturan Pemerintah tentang Perpajakan yang berlaku.
  - Pemotongan PPh 23 tidak berlaku untuk toko yang berbentuk individu.
  - Biaya Pembayaran **tidak** akan dikenakan ke ongkir, diskon produk, dan/atau voucher diskon dari Penjual Shopee Mall.
  - Penjual bisa mengecek Biaya Pembayaran final di Rincian Pesanan dan Rincian Penghasilan, baik melalui aplikasi atau pun Seller Centre.
  - Untuk menjadi Penjual Shopee Mall, Anda dapat mengajukan pendaftaran Shopee Mall melalui[ Seller Centre](https://seller.shopee.co.id/portal/settings/shop/profile) atau[ Portal Pendaftaran](https://seller.shopee.co.id/portal/os-onboarding). Pelajari lebih lanjut mengenai[ kriteria Shopee Mall](https://seller.shopee.co.id/edu/article/1806).

## Angka & patokan

| Patokan | Nilai |
|---|---|
| Biaya Pembayaran Shopee Mall | 1,8% (maks. Rp50.000/kuantitas produk), flat semua kategori |
| Periode SKB PPh 23 disebut entry ini | 3 Feb 2025 – 31 Des 2025 (No. KET-00012/PPUT-CT/KPP.3010/2025) |

## Pertanyaan diagnosa

1. **Ini pertanyaan soal Biaya Pembayaran (1,8%) atau Biaya Administrasi?** Dua biaya beda yang SAMA-SAMA wajib buat Shopee Mall — Biaya Administrasi ada di `shp-biaya-001`.
2. **Biaya Pembayaran dihitung dari ongkir atau diskon?** Enggak — cuma dari (Harga Asli Produk − Diskon/Voucher ditanggung Penjual), ongkir gak masuk hitungan.
3. **Toko individu atau Badan Usaha?** Pemotongan PPh 23 gak berlaku buat toko individu, sama seperti kebijakan SKB lainnya.
4. **Soal PPh 23 — cek dulu periode SKB yang sedang berlaku!** Lihat Batasan di bawah — ada 2 nomor SKB berbeda tercatat di KB ini.

## Batasan
**Perlu dicek:** entry ini (valid_as_of Juli 2026) menyebut SKB PPh 23 No. KET-00012 berlaku 3 Feb–31 Des **2025**, sementara `shp-keuangan-003` (valid_as_of Januari 2026) menyebut SKB No. KET-00002 berlaku 15 Jan–31 Des **2026**. Kemungkinan besar entry ini isinya belum ter-update pas re-scraping Juli 2026 (masih nyantol ke SKB tahun sebelumnya). **Jangan pakai nomor/periode SKB dari entry ini** — rujuk ke `shp-keuangan-003` buat info SKB PPh 23 terkini, atau cek langsung ke sumber resmi Shopee.
