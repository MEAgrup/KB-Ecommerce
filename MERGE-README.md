# MERGE-README — KB E-Commerce (GABUNGAN: KB-1 + KB-2 + Batch Shopee)

Paket ini hasil gabungan **KB-1** (root repo lama: materi seller ID + TikTok Shop platform,
97 entry) + **KB-2** (`kb/` lama: batch1 Canva/Jawara + TSP/Douyin, 65 entry) + **Batch Shopee**
(2026-08: 282 entry Shopee + 13 fundamental tambahan + 15 arsip), dibuat pakai skill
`mea-knowledge-architect`. **SIAP digabung lagi** dengan KB lain dari skill yang sama.

## Isi paket
- `kb/` — **467 entry aktif+blocked** (458 canonical, 9 blocked) + 15 archived, `validate.py`:
  **0 error** (12 flag "bahasa hype" dicek manual — semua false positive, kutipan kebijakan resmi
  Shopee soal kerahasiaan OTP/password atau contoh klaim yang justru DILARANG, bukan pelanggaran)
  - `tiktok-shop/` (149) — dasar, produk-dan-sku, konten-dan-kreatif, live, iklan (5 sub),
    campaign, afiliasi, segmentasi-toko, upload-produk, traffic-dan-masalah-toko,
    metrik-dan-rumus, benchmark-dan-pengukuran, creative-dan-audience, script-jualan,
    kebijakan-dan-kepatuhan (4 sub)
  - `shopee/` (282, semua canonical) — akun-dan-toko, analisis-performa-toko, iklan-dan-promosi,
    keuangan, layanan-pembeli, live-dan-video, pengiriman-dan-pesanan, penjual-star-dan-mall,
    produk. Sumber dominan artikel resmi Shopee Seller Centre + sebagian transkrip YouTube Yohan
    dan slide training internal MEA (id seri `-1xx`)
  - `fundamental/` (36: 27 canonical, 9 blocked) — psikologi, harga, analisa, operasional,
    mindset, komisi, strategi-produk (baru), retensi-dan-repeat-order (baru) + 3 dasar
  - `_archive/` — 15 entry (`pengumuman-dan-kebijakan-terbaru`, batch Shopee) + 3 potongan
    truncated lama
  - `_decisions/DECISIONS.md` — **74 keputusan** (M: 9, K1: 25, K2: 21, S: 19 baru dari batch
    Shopee), mayoritas masih TERBUKA
  - `_decisions/kamus-lokalisasi.md` — kamus Douyin→TikTok Shop (dari KB-2)
  - `_inbox/` — 2 scope-note + 2 txt mentah distage (Star Seller — **sudah masuk lewat Batch
    Shopee**, Tokopedia SU — masih nunggu) + README
  - `_manifest/MANIFEST.csv` & `.json` — indeks 467 ID (buat deteksi tabrakan merge berikutnya)
- `sources/` — file sumber KB-1 (`knowledge_base_basic_seller.txt`) + KB-2 (`canva/`, `tsp/`)
- `MERGE-LOG.md` — audit persis apa yang diubah
- `LAPORAN-KB.md` — laporan Fase 6 KB-1+KB-2, + update cakupan Batch Shopee di bagian bawah

## Namespace ID gabungan (buat cegah tabrakan di merge berikutnya)
Semua namespace sudah kontigu (tanpa lubang) setelah renumber.

| Namespace | Rentang | Mulai batch berikutnya |
|---|---|---|
| tts-live | 001-018 | 019 |
| tts-produk | 001-017 | 018 |
| tts-konten | 001-012 | 013 |
| tts-traffic | 001-009 | 010 |
| tts-pelanggaran-konten | 001-008 | 009 |
| tts-afiliasi | 001-007 | 008 |
| tts-gmvmax | 001-007 | 008 |
| tts-campaign | 001-006 | 007 |
| tts-upload | 001-006 | 007 |
| tts-ads / tts-diversity / tts-segmentasi | 001-005 (segmentasi mulai 000) | 006 |
| tts-metrik / tts-kebijakan-iklan / tts-pelanggaran-seller | 001-004 | 005 |
| tts-dasar / tts-iklan / tts-kategori-khusus / tts-script / tts-ttms | 001-003 | 004 |
| tts-benchmark / tts-branding / tts-creative | 001-002 | 003 |
| tts (intro) | 000 | — |
| fnd-operasional | 001-007 | 008 |
| fnd-psikologi | 001-005 | 006 |
| fnd-mindset | 001-005 | 006 |
| fnd-analisa | 001-005 | 006 |
| fnd-harga | 001-004 | 005 |
| fnd-komisi / fnd (bare, KB-1) | 001-003 | 004 |
| fnd-strategi (baru) | 001-003 | 004 |
| fnd-retensi (baru) | 001 | 002 |
| shp-iklan | 001-029, 101-102, 201-205 (lihat catatan seri ganda) | 030 / 103 / 206 |
| shp-pengiriman | 001-074 | 075 |
| shp-produk | 001-029, 101-106 | 030 / 107 |
| shp-toko | 001-035 | 036 |
| shp-akun | 001-018, 101-103 | 019 / 104 |
| shp-promosi | 001-023 | 024 |
| shp-keuangan | 001-009, 101 | 010 / 102 |
| shp-mall | 001-006, 101 | 007 / 102 |
| shp-live | 001-011 | 012 |
| shp-biaya | 001-009 | 010 |
| shp-video | 001-007 | 008 |
| shp-afiliasi | 001-006 | 007 |
| shp-penalti | 001-005 | 006 |
| shp-pesanan | 001-006 | 007 |
| shp-performa | 001-002, 101-102 | 003 / 103 |
| shp-layanan / shp-chat / shp-enabler | 001-003 | 004 |
| shp-star / shp-ekspor / shp-edukasi | 001-002 | 003 |
| shp-partner / shp-kampanye | 001 | 002 |
| shp-pengumuman | 001-015 (semua **archived**, jangan dipakai kutip) | — |

**Catatan seri ganda `shp-*`:** beberapa kategori (iklan, produk, akun, keuangan, mall, performa)
punya dua seri nomor — `001-0xx` untuk artikel resmi Shopee Seller Centre, `1xx`/`2xx` untuk
materi strategis (transkrip YouTube Yohan, slide internal MEA, atau hasil pecahan D-DEPTH). Kalau
nambah entry baru, pilih seri sesuai jenis sumbernya, jangan disisipkan di seri yang salah.

## Aturan penamaan D-code
D-code diberi prefix asal biar gak bentrok: `K1-` (KB-1), `K2-` (KB-2), `M-` (keputusan merge
KB-1×KB-2), `S-` (batch Shopee, termasuk `S-D-MERGE-01..09` — duplikat baru yang ketahuan pas
Batch Shopee digabung ke `fundamental/` lama). **Batch berikutnya pakai tag baru** (mis.
`K3-D-OUTDATED-01`).

## 4 titik WAJIB dicek saat merge berikutnya
1. **Tabrakan ID** — diff `_manifest/MANIFEST.json` paket ini vs KB baru; renumber satu sisi
   dari kolom "Mulai batch berikutnya" di atas, lalu update semua `related`/`decisions`. Batch
   Shopee kemarin nemu 6 tabrakan (`fnd-operasional-001..003`, `fnd-psikologi-001`, `fnd-harga-001..002`)
   karena materi YouTube Yohan sempat di-re-ingest di dua batch berbeda — selalu cek prefix
   `fnd-*` dulu, itu yang paling sering numpuk.
2. **Duplikat topik** — jalankan `overlap.py` pada tree gabungan. overlap.py berbasis kata:
   overlap lintas-batch beda kosakata BISA lolos — cek manual, jadikan `D-MERGE`. Juga awas
   klaster raksasa palsu (ratusan file) kalau isinya dominan artikel resmi platform — itu
   kesamaan boilerplate bahasa formal, bukan duplikat topik beneran.
3. **Link `related:` lintas-KB** — jalankan `validate.py` sampai 0 error entry.
4. **Taksonomi & ejaan kategori** — samakan ejaan sebelum gabung (di merge KB-1×KB-2:
   `affiliate`→`afiliasi`, `produk-dan-toko`→`produk-dan-sku`, `konten-dan-video`→`konten-dan-kreatif`;
   di Batch Shopee: folder `operasional`→`operasional-dan-skala`, `psikologi-pembeli`→
   `psikologi-pembeli-dan-nilai`, `kondisi-ekonomi`→masuk `mindset-dan-kondisi-pasar`).

## Keputusan
55 keputusan lama (M/K1/K2) masih TERBUKA — disatukan & diputus sekali setelah semua batch
masuk (sesuai arahan). Baca **Bagian M** dulu: itu konflik/duplikat yang cuma kelihatan setelah
KB-1 & KB-2 disandingkan. 19 keputusan baru dari Batch Shopee ada di **Bagian D–E** (prefix `S-`):
4 dari Bagian D sudah tertutup (Yohan sudah jawab 2026-08-30), sisanya + semua `S-D-MERGE-01..09`
di Bagian E masih terbuka.
