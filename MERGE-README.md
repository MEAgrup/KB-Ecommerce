# MERGE-README — KB E-Commerce (GABUNGAN: KB-1 + KB-2)

Paket ini hasil gabungan **KB-1** (root repo lama: materi seller ID + TikTok Shop platform,
97 entry) + **KB-2** (`kb/` lama: batch1 Canva/Jawara + TSP/Douyin, 65 entry), dibuat pakai
skill `mea-knowledge-architect`. **SIAP digabung lagi** dengan KB lain dari skill yang sama.

## Isi paket
- `kb/` — **162 entry** (148 canonical, 14 blocked), `validate.py`: **0 error entry**
  - `tiktok-shop/` (139) — dasar, produk-dan-sku, konten-dan-kreatif, live, iklan (5 sub),
    campaign, afiliasi, segmentasi-toko, upload-produk, traffic-dan-masalah-toko,
    metrik-dan-rumus, benchmark-dan-pengukuran, creative-dan-audience, script-jualan,
    kebijakan-dan-kepatuhan (4 sub)
  - `fundamental/` (23) — psikologi, harga, analisa, operasional, mindset, komisi + 3 dasar
  - `shopee/` — **kosong** (gap `K1-D-GAP-03`, ada README penanda)
  - `_decisions/DECISIONS.md` — **55 keputusan** (M: 9 merge baru, K1: 25, K2: 21), semua TERBUKA
  - `_decisions/kamus-lokalisasi.md` — kamus Douyin→TikTok Shop (dari KB-2)
  - `_inbox/` — 2 scope-note + 2 txt mentah distage (Star Seller, Tokopedia SU) + README
  - `_manifest/MANIFEST.csv` & `.json` — indeks 162 ID (buat deteksi tabrakan merge berikutnya)
- `sources/` — file sumber KB-1 (`knowledge_base_basic_seller.txt`) + KB-2 (`canva/`, `tsp/`)
- `MERGE-LOG.md` — audit persis apa yang diubah
- `LAPORAN-KB.md` — laporan Fase 6 (cakupan, gap, urutan kerja)

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
| fnd-mindset / fnd-operasional / fnd-psikologi | 001-004 | 005 |
| fnd-analisa / fnd-komisi / fnd (bare, KB-1) | 001-003 | 004 |
| fnd-harga | 001-002 | 003 |

**Shopee (`shp-`) masih kosong — aman, gak tabrakan.**

## Aturan penamaan D-code
D-code diberi prefix asal biar gak bentrok: `K1-` (KB-1), `K2-` (KB-2), `M-` (keputusan merge).
**Batch berikutnya pakai tag baru** (mis. `K3-D-OUTDATED-01`).

## 4 titik WAJIB dicek saat merge berikutnya
1. **Tabrakan ID** — diff `_manifest/MANIFEST.json` paket ini vs KB baru; renumber satu sisi
   dari kolom "Mulai batch berikutnya" di atas, lalu update semua `related`/`decisions`.
2. **Duplikat topik** — jalankan `overlap.py` pada tree gabungan. overlap.py berbasis kata:
   overlap lintas-batch beda kosakata BISA lolos — cek manual, jadikan `D-MERGE`.
3. **Link `related:` lintas-KB** — jalankan `validate.py` sampai 0 error entry.
4. **Taksonomi & ejaan kategori** — samakan ejaan sebelum gabung (di merge ini
   `affiliate`→`afiliasi`, `produk-dan-toko`→`produk-dan-sku`, `konten-dan-video`→`konten-dan-kreatif`).

## Keputusan
Semua 55 keputusan sengaja TERBUKA — disatukan & diputus sekali setelah semua batch masuk
(sesuai arahan). Baca **Bagian M** dulu: itu konflik/duplikat yang cuma kelihatan setelah
KB-1 & KB-2 disandingkan.
