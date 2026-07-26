---
id: tts-ads-001
title: Dapetin penjualan pertama SKU baru pakai PSA
platform: tiktok-shop
kategori: iklan/shopping-ads
depth: 1
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: 2024-Q2
sources:
  - file: TSP_Roadshow_Deck_Final.md
    bagian: "slide 13–16 — PSA solusi penjualan pertama + studi kasus"
related: [tts-ads-002, tts-produk-009, tts-produk-006]
decisions: [K1-D-OUTDATED-01, K1-D-CONFLICT-05]
---

# Dapetin penjualan pertama SKU baru pakai PSA

> ⚠️ **Update kebijakan iklan (Jul 2026): PSA sudah tidak ada lagi.** Semua jenis iklan lama
> (PSA, VSA, LSA) sekarang dilebur ke **GMV Max** — GMV Max adalah titik masuk beriklan.
> Mekanisme di bawah tetap ditulis sebagai konteks logika, tapi **jangan arahkan member mulai
> dari PSA** — arahkan langsung ke GMV Max. GMV Max butuh minimal 1 video yang sudah ada.
> Lihat `M-D-CONFLICT-02` & `K1-D-OUTDATED-01`.


## Ringkasan

PSA (Product Shopping Ads) itu alat buat **nembus penjualan pertama**, bukan buat scaling. Dia nongol di **hasil pencarian dan tab "Toko"** — tempat orang yang udah niat beli lagi nyari. Yang lu butuhin cuma listing produk, gak perlu bikin video. Dan kenapa penjualan pertama itu penting: **SKU yang cepat terjual punya peluang tumbuh lebih tinggi.**

> **PSA duluan, GMV Max belakangan.** Materi Seller University (Jun 2026) ngasih syarat
> siap GMV Max: **5+ pesanan dalam 14 hari**, min 3 video ber-views tinggi, produk hero
> stok stabil. Toko nol pesanan belum lolos syarat itu — dan PSA justru alat yang gak
> butuh video dan gak butuh riwayat pesanan. Jadi urutan yang dipakai KB ini:
> **PSA → kumpulin 3 video → 5+ pesanan → baru GMV Max.** Lihat `D-CONFLICT-05`.

## Kapan ini dipakai

Dipakai buat SKU yang belum pernah laku — kolam **Break Zero** di `tts-produk-006`, yang di benchmark isinya 53% katalog. Juga cocok buat toko yang produknya lebih banyak dibeli **berdasarkan pencarian** daripada dari FYP.

**Kapan PSA bukan pilihan terbaik:** kalau produknya butuh dijelasin atau didemoin buat orang mau beli. Produk yang orang gak nyari namanya gak akan ketemu di pencarian.

## Isi

**Tiga alasan PSA cocok buat penjualan pertama**, dari sumber:

1. **Penjualan pertama lebih cepat** — otomatis pakai gambar dari listing produk, jadi gak ada tahap produksi kreatif
2. **ROAS SKU baru lebih tinggi** — ROAS produk baru **38% lebih tinggi** dibanding pakai VSA
3. **7 hari lebih cepat** nyampe 1 pesanan/hari — dengan PSA **5 hari**, tanpa PSA **12 hari**

**Di mana PSA nongol:** traffic di **hasil pencarian** dan traffic di **tab "Toko"**. Ini bedanya paling penting dari VSA yang main di FYP. PSA nangkep orang yang **aktif nyari produk**; VSA nangkep orang yang sedang scroll.

**Kenapa penjualan pertama itu titik kritis:** sumbernya nunjukkin dua SKU dengan lintasan beda — SKU yang laku lebih cepat di hari-hari awal punya peluang pertumbuhan yang lebih tinggi ke depan. Jadi penjualan pertama bukan cuma "sekali laku"; itu sinyal awal yang ikut nentuin lintasannya.

**Rekomendasi pemakaian dari sumber:** jalanin PSA **always-on**, dan **gandain di produk hero** selama periode kampanye.

**Studi kasus dari materi** (toko alat tulis kantor / ATK): toko ini pernah jalanin iklan Video, PSA, dan LIVE. Hasilnya CPA/CPR buat LIVE dan Video **mahal**, mengingat produk ATK harga dan marginnya kecil. Kesimpulannya: **PSA jadi opsi terbaik buat toko yang produknya lebih banyak dibeli berdasarkan pencarian produk dan rekomendasi**, bukan dari konten.

Itu pola diagnosa yang berguna: **produk margin kecil + dibeli lewat pencarian → PSA duluan, bukan video.** Produk ATK, kebutuhan harian, sparepart, dan barang fungsional biasanya masuk pola ini.

## Angka & patokan

| Patokan | Nilai | Sumber |
|---|---|---|
| ROAS SKU baru dengan PSA vs VSA | +38% | Data Internal TTS, SEA, Q2 2024 |
| Waktu ke 1 pesanan/hari dengan PSA | 5 hari | idem |
| Waktu ke 1 pesanan/hari tanpa PSA | 12 hari | idem |
| Rekomendasi status | Always-on | TSP deck slide 14 |

## Yang bikin gagal

**Pakai PSA buat produk yang orang gak nyari namanya.** PSA main di pencarian. Produk baru yang kategorinya belum dikenal gak ada yang nyari.

**Nyalain PSA cuma waktu kampanye.** Rekomendasinya always-on.

**Ngarepin PSA jadi mesin utama.** Ini alat penjualan pertama. Buat naikin dari situ ke Hero SKU, yang dipakai VSA dan kreator (`tts-ads-002`).

**Maksa video buat produk margin kecil.** Studi kasus ATK-nya persis soal ini — CPA video kemahalan buat produk margin kecil.

## Pertanyaan diagnosa

1. **Produk lu dibeli orang karena nyari, atau karena ketemu?** Ini yang nentuin PSA atau VSA duluan.
2. **Berapa produk lu yang belum pernah laku?** Itu kolam kandidat PSA.
3. **Margin produknya berapa?** Margin kecil bikin CPA video mahal.
4. **PSA-nya nyala terus atau dinyalain-matiin?**

## Batasan

Semua angka di entry ini dari Q2 2024 — **dua tahun sebelum sekarang, dan sebelum GMV Max jadi default**. Perbandingan "PSA vs VSA" itu perbandingan antar iklan manual; sekarang Product GMV Max nangani kartu produk dan video sekaligus secara otomatis (`tts-gmvmax-001`).

Artinya: mekanismenya masih valid (PSA main di pencarian, cocok buat penjualan pertama), tapi pertanyaan "PSA atau VSA" mungkin bukan lagi pertanyaan yang relevan kalau kampanye utamanya GMV Max. **Angkanya jangan dikutip ke member sebagai ekspektasi** — cuma sebagai arah. Lihat `D-OUTDATED-01`.
