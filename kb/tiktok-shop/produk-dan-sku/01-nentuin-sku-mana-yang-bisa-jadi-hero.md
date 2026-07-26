---
id: tts-produk-001
title: Nentuin SKU mana yang udah jadi Hero
platform: tiktok-shop
kategori: produk-dan-sku
depth: 1
audience: member
aksi_oleh: member
status: canonical
confidence: tinggi
sensitif_waktu: false
valid_as_of: 2024-Q2 (data) / 2026-01 (playbook)
sources:
  - file: TSP_Roadshow_Deck_Final.md
    bagian: "slide 9–11 — indikasi penentu SKU unggulan"
  - file: Library_Tiktok.md
    bagian: "§Product Analysis - Find the Hero SKU, Step 1"
related: [tts-produk-006, tts-produk-007, tts-produk-008, tts-gmvmax-002]
decisions: []
---

# Nentuin SKU mana yang udah jadi Hero

## Ringkasan

Dua ambang, dan dua-duanya diukur dari **rata-rata pesanan harian dalam 30 hari terakhir**. Lewat **30 pesanan/hari** = Hero SKU. Lewat **100 pesanan/hari** = Super Hero SKU. Yang bikin dua angka ini penting bukan labelnya — tapi kenyataan bahwa produk yang lewat ambang itu **tumbuh lebih cepat setelahnya**, jadi ini titik di mana lu tambah dorongan, bukan titik di mana lu santai.

## Kapan ini dipakai

Dipakai sebagai langkah pertama waktu ngeliat toko: ada Hero SKU atau nggak. Jawabannya nentuin seluruh arah saran berikutnya. Kalau ada → rawat dan perpanjang umurnya. Kalau nggak ada → bikin satu (`tts-produk-002`).

## Isi

**Ambang pertama: 30 pesanan/hari.** Kalau rata-rata pesanan harian dalam 30 hari terakhir lebih dari 30, pesanan/hari di 30 hari berikutnya naik rata-rata **+36%** (data Asia Tenggara).

**Ambang kedua: 100 pesanan/hari.** Kalau rata-rata pesanan harian 30 hari terakhir lebih dari 100, pesanan/hari 30 hari berikutnya naik **+60%**.

Jadi ini bukan dua label — ini dua **titik infleksi**. Semakin tinggi ambang yang dilewatin, semakin cepat pertumbuhan setelahnya. Sumbernya nyebut ini "indikasi pertama SKU unggulan yang sedang terbentuk".

**Dua hal wajib begitu Hero SKU teridentifikasi**, dari playbook:
1. **Hero SKU harus selalu ada di Product GMV Max.** Bukan kadang — selalu.
2. **Bundling Hero SKU dan Growing SKU di kampanye yang beda.** Jangan dicampur satu kampanye.

Poin kedua sering dilewat. Alasannya: produk di tahap siklus hidup berbeda punya ROI berbeda, dan kalau digabung satu kampanye, sistem ngoptimasi ke rata-ratanya — yang bikin Hero-nya kurang didorong dan yang lemah kurang dites. Detail setelannya di `tts-gmvmax-002`.

**Kenapa "rata-rata 30 hari", bukan hari terbaik.** Produk yang sehari kena 50 order karena flash sale lalu balik 5 order/hari bukan Hero SKU. Yang diukur konsistensi.

## Angka & patokan

| Patokan | Nilai | Sumber |
|---|---|---|
| Ambang Hero SKU | > 30 pesanan/hari (rata-rata 30 hari) | TSP deck slide 9; Library §Step 1 |
| Ambang Super Hero SKU | > 100 pesanan/hari (rata-rata 30 hari) | TSP deck slide 10 |
| Pertumbuhan setelah lewat 30/hari | +36% pesanan/hari di 30 hari berikutnya | Data Internal TTS, SEA, Q2 2024 |
| Pertumbuhan setelah lewat 100/hari | +60% pesanan/hari di 30 hari berikutnya | idem |

## Yang bikin gagal

**Ngukur dari GMV, bukan dari jumlah pesanan.** Ambangnya pesanan/hari. Produk mahal bisa GMV besar dengan 5 order — itu bukan Hero SKU menurut definisi ini.

**Ngambil hari terbaik sebagai patokan.** Rata-rata 30 hari.

**Nganggep Hero SKU artinya aman.** Kebalikan — ini titik di mana lu harusnya nambah dorongan. Dan umurnya terbatas; lihat `tts-produk-007`.

**Nyampur Hero SKU sama produk baru di satu kampanye GMV Max.** Dilarang eksplisit di playbook.

## Pertanyaan diagnosa

1. **Rata-rata pesanan harian 30 hari terakhir per SKU berapa?** Per SKU, bukan total toko.
2. **Ada SKU yang lewat 30/hari? Lewat 100/hari?** Dua angka, dua penanganan.
3. **Kalau ada Hero SKU — dia ada di kampanye Product GMV Max yang nyala terus?** Ini yang paling sering belum.
4. **Kampanye Hero SKU-nya kepisah dari produk baru?** Cek, jangan diasumsi.

## Batasan

Angka +36% dan +60% dari data Q2 2024 — dua tahun sebelum sekarang, dan sebelum GMV Max jadi default. Arahnya (produk yang lewat ambang tumbuh lebih cepat) masih kepakai; besarannya jangan dikutip ke member sebagai ekspektasi. Lihat `D-OUTDATED-01`.

Ambang 30 dan 100 sendiri gak berlabel tanggal di sumber dan konsisten muncul di dua dokumen dengan vintage beda, jadi confidence-nya tinggi.
