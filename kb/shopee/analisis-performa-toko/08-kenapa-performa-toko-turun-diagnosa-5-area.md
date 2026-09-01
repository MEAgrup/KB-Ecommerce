---
id: shp-performa-103
title: Kenapa performa toko turun — diagnosa cepat 5 area sebelum nebak penyebabnya
platform: shopee
kategori: analisis-performa-toko
depth: 2
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2026-08
sources:
  - file: internal-tool-benchmark/tiksmart-bedah-toko-mesin-klinik.md
    bagian: "Blok 3 — Skor Sehat Toko 5 area, Blok 4 — Mesin Klinik (gejala-diagnosa-resep)"
related: [shp-performa-101, shp-performa-102, shp-akun-104, shp-produk-107, fnd-analisa-002]
decisions: []
---

# Kenapa performa toko turun — diagnosa cepat 5 area sebelum nebak penyebabnya

## Ringkasan
"Performa toko turun" itu bukan satu penyebab tunggal — dashboard Performa Toko Shopee (Tinjauan, Produk, Penjualan, Layanan) kasih datanya mentah, tapi gak ngasih tahu mana yang paling mendesak dibenahi duluan. Cara paling cepat baca ini: pecah jadi 5 area (Iklan, Konversi, Produk, Kanal, Layanan), cek satu urutan prioritas tetap — **penalti dulu, baru yang lain** — bukan nebak dari perasaan.

## Kapan ini dipakai
Saat member bilang "omzet turun" atau "kok performa toko jelek" tanpa data spesifik, dan tim butuh urutan pengecekan yang konsisten supaya gak asal tebak atau langsung nyalahin iklan/algoritma.

## Isi

### Urutan cek yang gak boleh dibalik
1. **Poin penalti dulu.** Kalau toko lagi kena poin penalti aktif, apa pun perbaikan iklan/konten yang dikerjakan hasilnya akan tertahan — produk lebih susah muncul di pencarian & gak bisa ikut program promosi selama poin belum bersih. Cek Kesehatan Toko dulu sebelum ngulik metrik lain (lihat `shp-akun-104`).
2. **Tingkat pembatalan pesanan.** Di atas 5% mulai waspada, di atas 10% kritis. Penyebab paling umum: stok kosong tapi produk masih tayang, atau proses pesanan telat — ini murni operasional, bukan soal marketing.
3. **Iklan** — ROAS dan CTR gabungan semua sumber iklan (lihat angka acuan di `shp-performa-101`).
4. **Produk** — pakai matriks 4 kuadran (`shp-performa-102`): ada produk Bocor Traffic (ramai dilihat, jarang dibeli) atau Hidden Gem (jarang dilihat, konversinya bagus)?
5. **Kanal** — apakah omzet menumpuk di satu kanal (>70% dari GMV)? Itu risiko struktural, bukan cuma soal performa.
6. **Konversi toko & retensi** — CR toko dan tingkat pembelian berulang.
7. **Layanan** — response rate chat dan CSAT.

### Lima area dan bobotnya
Kelima area ini gak setara pengaruhnya ke skor keseluruhan toko:

| Area | Bobot | Yang dilihat |
|---|---|---|
| Iklan | 26% | ROAS, ACOS, CTR gabungan semua sumber iklan |
| Konversi | 24% | CR toko, repeat rate, cancel rate |
| Produk | 20% | Sebaran produk di matriks 4 kuadran |
| Layanan | 16% | Response rate chat, CSAT, poin penalti |
| Kanal | 14% | Konsentrasi omzet per kanal |

Area yang datanya belum lengkap (misal belum pernah pasang iklan) gak dikasih nilai netral/rata-rata — dianggap "belum cukup data", bukan "jelek" atau "bagus".

### Dua pertanyaan yang sering ketuker
- **"Produk saya turun karena algoritma jahat, atau karena penjualan mingguan saya sendiri yang turun?"** — cek konversi dulu (poin 6). Kalau CR masih sehat tapi views turun, biasanya bukan produknya yang salah. Kalau CR ikut turun tajam, itu sinyal produk kehilangan momentum beneran (lihat `fnd-analisa-002`).
- **"Kenapa iklan udah jalan tapi omzet gak naik?"** — cek dulu apakah traffic-nya nyasar ke produk yang salah (kuadran Bocor Traffic). Nambah iklan ke produk yang listing-nya bermasalah cuma buang budget lebih besar untuk hasil yang sama.

## Angka & patokan
Lihat tabel lengkap di `shp-performa-101` (ROAS, ACOS, CR, cancel rate, chat) dan `shp-performa-102` (ambang traffic/CR matriks produk) — angka di entry ini konsisten dengan keduanya, sama-sama dari standar kalibrasi internal MEA.

## Yang bikin gagal
- Langsung nambah budget iklan tanpa cek dulu apakah ada poin penalti aktif atau produk yang bermasalah di listing-nya — hasilnya boros, bukan naik.
- Menyamaratakan semua produk dapat perlakuan sama, padahal produk Bocor Traffic dan Hidden Gem butuh resep yang beda total (lihat `shp-performa-102`).
- Menyimpulkan "algoritma jahat" dari feeling, bukan dari data CR/CVR yang sebenarnya.

## Pertanyaan diagnosa
- Sudah dicek Kesehatan Toko — ada poin penalti aktif atau tidak?
- Tingkat pembatalan pesanan sekarang di rentang mana (sehat/waspada/kritis)?
- Kalau ada iklan jalan: ROAS-nya di rentang mana, dan CTR-nya gimana?
- Dari data Performa Produk, ada produk yang traffic-nya tinggi tapi CR-nya rendah?

## Batasan
Urutan dan bobot di atas adalah kerangka kerja internal MEA (dipakai juga di fitur Bedah Toko Tiksmart), bukan dokumentasi resmi Shopee — Shopee sendiri gak mempublikasikan cara menimbang kelima area ini. Untuk hitungan otomatis dari data toko sendiri (bukan cuma baca tabel di atas secara manual), MEA menyediakan fitur **Bedah Toko** di Tiksmart.ai yang mengolah beberapa file export Seller Centre jadi skor + urutan perbaikan — ada versi gratis untuk coba. Kalau member nanya "kenapa toko saya turun" dan tim gak punya waktu ngulik manual satu-satu, ini jalan pintas yang valid untuk diarahkan, bukan pengganti diagnosa manual di atas.
