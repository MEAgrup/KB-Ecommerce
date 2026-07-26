---
id: tts-live-011
title: Voucher LIVE penjual dan aturan pin
platform: tiktok-shop
kategori: live
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-06
sources:
  - file: knowledge_base_basic_seller.txt
    bagian: "Artikel Terkait 4C — Voucher LIVE Penjual (2026-06-05)"
related: [tts-live-009, tts-live-010, tts-live-006, tts-live-004]
decisions: []
---

# Voucher LIVE penjual dan aturan pin

## Ringkasan

Voucher khusus penonton live. Dua batas yang nentuin cara pakainya: **maksimum 1 seller coupon per order**, dan di aplikasi TikTok **cuma 1 kupon yang bisa dipin** pada satu waktu — dan **nge-pin kupon menggantikan kartu produk yang sedang dipin.** Jadi lu harus milih: kupon atau produk yang nempel di layar.

## Kapan ini dipakai

Salah satu tips di kriteria "Konsistensi LIVE Seller" Basic Seller: pakai voucher promo dan aktif berinteraksi (`tts-segmentasi-000`). Juga tuas buat Click-to-Order (`tts-live-003`).

## Isi

**Setup di Seller Center PC:**
1. Buka halaman **Promotions**
2. Klik **LIVE Coupon**
3. Konfigurasi informasi dasar:
   - **Nama kupon**
   - **Periode klaim**
   - **Eligibilitas** — **All viewers** atau **Followers only**
   - **Periode validitas**

Perhatiin bedanya **periode klaim** dan **periode validitas**: yang pertama kapan kuponnya bisa diambil, yang kedua kapan bisa dipakai. Dua hal beda.

Pilihan **Followers only** itu tuas yang sering dilewat — bisa dipakai buat ngedorong orang follow dulu sebelum dapat kupon.

**Pengaturan kupon:**

| Setelan | Isinya |
|---|---|
**Discount type** | Amount off atau Percentage off |
**Minimum spend** | Minimal pembelian buat dapat diskon |
**Maximum discount per order** | Buat percentage off |
**Usage Quantity** | Jumlah kupon yang bisa diklaim |
**Number of claims per customer** | Maks **1 seller coupon per order** |

**Di aplikasi TikTok — dua aturan yang bikin ini jadi keputusan taktis:**
- Seller harus **pin** kupon biar tersedia selama livestream
- **Cuma 1 kupon** yang bisa dipin pada satu waktu
- **Nge-pin kartu kupon akan menggantikan kartu produk yang sedang dipin**

Aturan ketiga itu yang paling penting buat host: layar cuma bisa nampung satu pin. Kalau lu pin kupon, kartu produk yang sedang disorot hilang dari pin. Jadi ritmenya harus direncanain — nyambung ke skrip 3 menit (`tts-live-004`): pin produk waktu jelasin, pin kupon waktu CTA.

## Angka & patokan

| | Nilai |
|---|---|
Maks seller coupon per order | **1** |
Maks kupon yang dipin bareng | **1** |
Efek nge-pin kupon | Menggantikan kartu produk yang dipin |

## Yang bikin gagal

**Bikin kupon tapi lupa di-pin.** Kalau gak dipin, gak tersedia selama livestream.

**Pin kupon terus dibiarin.** Kartu produk hilang dari pin selama itu. Rencanain kapan pin kupon, kapan pin produk.

**Bikin beberapa kupon dan ngarepin dipakai barengan.** Maks 1 per order.

**Ketuker periode klaim dan periode validitas.** Kupon yang periode klaimnya kelewat gak bisa diambil walau masih valid.

## Pertanyaan diagnosa

1. **Kuponnya udah di-pin di aplikasi?** Ini yang paling sering kelupaan.
2. **Eligibilitas-nya All viewers atau Followers only?** Kalau tujuannya nambah follower, pilih yang kedua.
3. **Host tahu bahwa pin kupon ngilangin pin produk?** Perlu masuk skrip.
4. **Minimum spend-nya realistis dibanding harga produk?**

## Batasan

Sumbernya gak nyebut apakah LIVE Coupon bisa digabung dengan Flash Sale atau harga campaign — dan itu pertanyaan yang wajar mengingat aturan prioritas harga di `tts-campaign-002`. Kalau member mau numpuk kupon di atas harga campaign, eskalasi.
