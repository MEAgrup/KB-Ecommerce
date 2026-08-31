# Laporan Penyusunan Knowledge Base — Shopee (Kampung Seller)

## Ringkasan eksekutif

- **295 entry kanonik aktif** + **15 entry diarsipkan** = 310 entry total ditulis dari **308 file materi mentah** (277 artikel resmi Shopee, 25 transkrip YouTube Yohan, 5 slide deck internal MEA, 1 dokumen standar performa dari MEA Shopee Report Engine).
- Semua entry aktif berstatus `canonical`, sudah lolos validasi struktural (`scripts/validate.py`, 0 error setelah perbaikan; 12 flag "bahasa hype" dicek manual dan dikonfirmasi false positive dari filter kata kunci — konten resmi yang justru **melarang** klaim itu, bukan pelanggaran nyata).
- **1 video sengaja dikeluarkan** dari KB (opini soal kasus korupsi MBG — terlalu terikat berita/politik spesifik untuk jadi "knowledge" netral).
- **Semua keputusan di decision queue sudah diproses** sesuai arahan Yohan (2026-08-30): admin fee 10% diabaikan, folder pengumuman (15 entry) dipindah ke arsip, dan 68 entry kepanjangan sudah ditriase — 1 dipecah jadi 5 entry, 63 dikonfirmasi gak perlu dipecah, 3 masih di antrean.

## Peta cakupan (platform × sub-topik)

| Kategori | Jumlah entry | Sumber dominan |
|---|---|---|
| Akun & Toko | 60 | Artikel resmi |
| Pengiriman & Pesanan (termasuk jasa kirim) | 80 | Artikel resmi |
| Iklan & Promosi | 43 | Campuran resmi + transkrip (termasuk 5 entry hasil pecahan Iklan Shopee) |
| Produk | 35 | Campuran resmi + transkrip |
| Keuangan | 18 | Artikel resmi + 1 transkrip |
| Live & Video | 18 | Artikel resmi |
| Penjual Star & Mall | 12 | Artikel resmi + 1 transkrip |
| Layanan Pembeli | 9 | Artikel resmi |
| Analisis Performa Toko | 7 | Artikel resmi + benchmark internal |
| **Fundamental (lintas platform)** | **13** | Transkrip + slide |

**Diarsipkan (15 entry, `kb/_archive/pengumuman-dan-kebijakan-terbaru/`):** pengumuman & kebijakan bertanggal (PPh 22, perubahan tampilan UI, perubahan nama wilayah, dll) — sesuai keputusan Yohan, dianggap log historis, gak dipakai jawab member langsung.

Fundamental (13 entry) mencakup: psikologi pembeli, strategi harga (3), operasional (3), algoritma & data (2), retensi/repeat order, kondisi ekonomi, strategi produk (3) — semua ditandai `platform: lintas` karena ilmunya gak spesifik Shopee.

**Tipis/kandidat gap yang perlu diperhatikan:** kategori `algoritma-dan-data` dan `psikologi-pembeli` di fundamental cuma punya 1-2 entry — topik yang sebenarnya sering ditanya tapi materinya baru sedikit.

## Distribusi kedalaman

| Depth | Jumlah | Artinya |
|---|---|---|
| 1 — dasar | 64 | Konsep + langkah pokok, cocok seller baru |
| 2 — menengah | 201 | Mayoritas entry, butuh baca data/ada trade-off |
| 3 — lanjut | 30 | Butuh prasyarat/volume data cukup |

## Status entry

295 entry `canonical` (aktif, boleh dipakai jawab member) + 15 entry `archived` (log historis). **224 dari 295 entry aktif (76%) ditandai `sensitif_waktu: true`** — porsi besar ini wajar karena mayoritas materi memang seputar biaya, kebijakan, dan fitur platform yang berubah dari waktu ke waktu. Ini jadi daftar prioritas untuk review berkala.

## Decision queue — status akhir

Rincian lengkap di `kb/_decisions/DECISIONS.md`. **Semua keputusan yang diminta Yohan sudah diproses (2026-08-30):**

| Tipe | Status |
|---|---|
| D-CONFLICT-001 (admin fee 10%) | ✅ Tertutup — diabaikan, klaim gak pernah masuk entry manapun |
| D-CONFLICT-002/003 (GMV Max, Shopee Mall observasi lapangan) | Terbuka — masih confidence rendah, dibingkai jelas di entry masing-masing |
| D-OUTDATED-001 (folder pengumuman) | ✅ Tertutup — 15 entry dipindah ke `_archive/` |
| D-OUTDATED-002 (klaim 2026 belum dicek) | Terbuka — materi belum dikanonikkan, gak mendesak |
| D-GAP-001/002/003 | Terbuka — gak blocking, dicatat buat referensi |
| D-DEPTH (68 entry kepanjangan) | ✅ Diproses — 1 dipecah jadi 5 entry (`shp-iklan-006` → 5 entry Iklan Shopee), 63 dikonfirmasi gak perlu dipecah, 3 masih di antrean (`shp-ekspor-001`, `shp-ekspor-002`, `shp-mall-003`) |
| D-SCOPE (benchmark, JAWARA 20) | ✅ Tertutup sejak sebelumnya |

## Gap paling mengganggu

Diurutkan berdasarkan seberapa sering kemungkinan ditanya tim, bukan gampangnya diisi:

1. **Detail jenis-jenis iklan Shopee & cara pilih produk yang siap diiklankan** — ini pertanyaan yang hampir pasti sering ditanya, tapi sumber slide mentor deck-nya kosong (D-GAP-001). Untungnya artikel resmi (`shp-iklan-006` dkk) sudah cukup menutup sebagian besar ini.
2. **Psikologi pembeli & cara baca algoritma** — cuma 1-2 entry fundamental, padahal ini pertanyaan yang sering muncul di sesi mentoring ("kenapa toko gua sepi", "kenapa algoritma jahat").
3. **Angka benchmark yang solid untuk kategori produk spesifik** — benchmark ROAS/ACOS/CR yang ada sifatnya general (semua kategori dipukul rata), padahal beberapa entry sendiri menyebut standar sehat beda-beda per kategori.

## Materi yang dibuang (biar bisa dibantah)

- **JAWARA 20 (promo event)** — hook marketing dan harga promo dibuang sesuai keputusan Yohan; sisa 5 topik silabus tanpa isi gak dipaksa jadi entry (lihat D-GAP-003).
- **Video "Menghadapi KONDISI BURUK" (kasus MBG)** — dikeluarkan sepenuhnya, terlalu terikat berita/politik spesifik (lihat D-GAP-002). Materi mentah masih tersimpan, gak dihapus.
- **Klaim marketing tanpa sumber** di deck Shopee Mastery 2026 ("10k+ Sellers Trained", "150% Avg. GMV Growth") — gak dimasukkan ke entry manapun karena gak ada rincian metodologi/sumber datanya.
- **Bagian kebijakan 2026 yang belum di-cross-check** dari deck Shopee Mastery 2026 (COD limit, atribusi GMV Max, kategori sensitif) — sengaja belum dikanonikkan sampai dicek satu-satu (D-OUTDATED-002).

## Urutan kerja yang disarankan

1. **Putuskan D-CONFLICT-001 (admin fee) dan D-OUTDATED-001 (folder pengumuman) duluan** — dua ini yang paling berpotensi bikin tim kasih info keliru ke member soal uang.
2. **Isi gap psikologi pembeli & algoritma** — kalau ada lebih banyak materi (transkrip lain, catatan Q&A grup), prioritaskan topik ini karena keliatan sering ditanya tapi materinya tipis.
3. **Jadwalkan sesi baca manual untuk 68 entry D-DEPTH** — gak mendesak, tapi akan bikin entry lebih gampang dipakai kalau ada waktu tim.
4. **Setelah decision queue diputuskan**, KB ini siap dipakai fase lanjut: SOP tim, kurikulum member, atau potongan retrieval buat Sebari.

---

*Laporan ini dan seluruh KB (306 entry + decision queue) tersedia di file yang saya lampirkan.*
