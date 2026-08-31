---
id: fnd-analisa-004
title: Sebelum nyalahin algoritma, cek dulu data toko lu
platform: lintas
kategori: analisa
depth: 2
status: blocked
confidence: sedang
sensitif_waktu: false
valid_as_of: tidak-diketahui
sources:
  - file: transkrip-yohan-youtube/algoritma-e-commerce-jahat-gak-berpihak-ke-seller-kecil.md
    bagian: video penuh
related: [fnd-analisa-001, fnd-analisa-005, fnd-retensi-001]
decisions: [S-D-MERGE-01]
---

# Sebelum nyalahin algoritma, cek dulu data toko lu

## Ringkasan
Algoritma marketplace gak peduli seller itu besar atau kecil, lama atau baru — yang dinilai cuma apakah user suka sama apa yang ditampilkan. Kalau traffic/omset turun, biasanya bukan algoritma yang "jahat", tapi ada sinyal di data (rating turun, kompetisi naik, produk kehilangan momentum) yang belum dicek.

## Kapan ini dipakai
Dipakai saat toko ngerasa traffic atau order turun drastis dan mulai menyalahkan platform/algoritma, sebelum benar-benar cek data toko sendiri.

## Isi
Prinsip yang dipegang: tugas algoritma cuma satu — bikin user betah (buka aplikasi lebih lama, lihat lebih banyak iklan, belanja lebih banyak). Algoritma bukan "membenci" seller kecil, tapi juga bukan "berpihak" pada siapapun.

Yang perlu dicek sebelum nyalahin algoritma:
1. **Standar kompetisi naik gak dari waktu ke waktu?** Dulu video biasa bisa viral, sekarang ratusan kreator bikin konten serupa — kalau kualitas konten lu masih setara "tahun lalu", value-nya relatif turun di mata algoritma.
2. **Produk masih ada momentumnya atau udah lewat?** Tiap produk ada masanya. Kalau bertahan pakai produk yang sama terus padahal sinyalnya (review mulai jelek, konversi turun, affiliate mulai ninggalin) udah nunjukkin turun, itu bukan algoritma yang salah.
3. **View tinggi tapi order rendah — cek CVR, bukan cuma view.** View besar tapi CVR jelek artinya orang penasaran tapi gak percaya/gak butuh. Traffic besar tanpa konversi bagus itu boros, bukan prestasi.
4. **Rating/review toko gimana?** Traffic besar dengan kualitas produk buruk cuma bikin orang coba sekali lalu kapok — algoritma "membuktikan" produknya di awal, tapi setelah itu penurunan review yang bikin performa jangka panjang anjlok.
5. **Daya beli pasar secara umum lagi turun gak?** Kalau kondisi ekonomi lagi berat, orang mengurangi belanja non-esensial — ini bukan salah algoritma atau produk, tapi kondisi makro.

Matriks cek cepat kalau toko mulai turun: CTR (masih ada yang klik?), conversion rate (masih ada yang beli?), repeat order (pelanggan lama masih balik?), aktivitas kompetitor (ada yang nawarin lebih baik?), kualitas konten (jujur masih bagus atau cuma dipertahankan karena males bikin baru?).

## Yang bikin gagal
Terus-menerus menyalahkan algoritma tanpa cek data konkret — ini bikin seller gak pernah benerin akar masalah yang sebenarnya (produk, konten, atau rating) dan cuma nunggu "keberuntungan" algoritma berubah.

## Pertanyaan diagnosa
- CVR toko sekarang dibanding beberapa bulan lalu gimana — naik, stabil, atau turun?
- Kompetitor dengan produk serupa juga lagi turun, atau cuma toko ini?
- Kapan terakhir kali konten/kreatif produk di-refresh?
- Rating dan review toko trennya gimana belakangan ini?
