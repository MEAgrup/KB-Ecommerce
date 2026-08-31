# Laporan Penyusunan Knowledge Base — Merge KB-1 + KB-2

## Ringkasan eksekutif
Dua KB dari akun berbeda digabung jadi satu tree kanonik: **162 entry** (KB-1 97 + KB-2 65),
**148 canonical + 14 blocked**, **0 error entry** di `validate.py`. **55 keputusan** disatukan
ke satu queue master (K1: 25, K2: 21, M: 9 baru) — semua **terbuka**, siap diputus Yohan sekali
di akhir. Dua materi mentah (Shopee/Star Seller + Tokopedia SU) distage di `_inbox/`, jadi batch
ingest berikutnya. Yang perlu dibaca duluan: **Bagian M** di DECISIONS.md — 9 konflik/duplikat
yang cuma muncul karena dua KB ketemu.

## Peta cakupan (platform × sub-topik)

| Platform | Sub-topik | Entry | Catatan |
|---|---|---|---|
| tiktok-shop | dasar, produk-dan-sku (17), konten-dan-kreatif (12), live (18+5), iklan (2+3+3+5+7), campaign (6), afiliasi (7), segmentasi-toko (5), upload-produk (6), traffic-dan-masalah-toko (9), metrik-dan-rumus (4), benchmark-dan-pengukuran (2), creative-dan-audience (2), script-jualan (3), kebijakan-dan-kepatuhan (19) | 139 | inti KB |
| lintas (fundamental) | psikologi, harga, analisa, operasional, mindset, komisi + 3 dasar KB-1 | 23 | berlaku dua platform |
| **shopee** | — | **0** | **gap paling menganggu** (K1-D-GAP-03), penanda README |

Tipis (kandidat gap): `creative-dan-audience` (2, K2-D-GAP-004), `benchmark-dan-pengukuran` (2),
`strategi-harga` (2).

## Distribusi kedalaman
- depth 1 (dasar): 51 · depth 2 (menengah): 88 · depth 3 (lanjut): 23
- Berat di menengah — wajar untuk KB operasional seller. Lanjut (23) mostly di produk/live/iklan.

## Status entry
- canonical: 148 · blocked: 14 (jangan dikutip; ada peringatan di atas entry masing-masing)
- confidence: tinggi 68 · sedang 80 · rendah 14

## Decision queue (55 total, semua terbuka)
Per tipe: GAP 27 · OUTDATED 25 · CONFLICT 19 · SCOPE 18 · MERGE 12 · DEPTH 11.

**10 paling mendesak** (urut by dampak — blocking/rugi-uang/kontradiksi dulu):
1. `M-D-CONFLICT-01` — durasi live 3–5 jam vs angka TSP (bikin mentor jawab beda soal jam kerja member)
2. `M-D-CONFLICT-02` — urutan mulai iklan; pastikan entry iklan KB-2 gak lawan urutan tetap KB-1
3. `K1-D-CONFLICT-05` — toko nol pesanan: PSA dulu atau langsung GMV Max (nentuin urutan seluruh KB)
4. `K1-D-CONFLICT-04` — boleh mulai GMV Max tanpa video?
5. `K1-D-CONFLICT-03` — GMV Max Net Sales entry sendiri atau varian?
6. `M-D-MERGE-02` — dua versi "SKU Hero" (KB-1 ID vs KB-2 TSP) di satu folder
7. `M-D-MERGE-01` — afiliasi: cek entry kembar lintas-KB
8. `K2-D-OUTDATED-004` — new-product boost (nge-block `tts-produk-017`)
9. `K1-D-OUTDATED-02` — fitur/UI GMV Max per Okt 2025 (mungkin sudah berubah)
10. `M-D-SCOPE-02` — ingest Star Seller (Shopee) + Tokopedia SU sebagai batch berikutnya

## Gap paling menganggu (urut by seberapa sering ditanya, bukan gampangnya diisi)
1. **Shopee — nol entry** (`K1-D-GAP-03` / `K2-D-GAP-01`). Paling sering ditanya, nol jawaban.
   Kandidat isi: `star-seller.txt` yang sudah distage. **Prioritas #1.**
2. **Basic Seller — 9 kriteria, nol ambang angka** (`K1-D-GAP-06`). Butuh halaman Seller Center.
3. **Benchmark angka khas seller ID** (`K2-D-GAP-001`) — patokan sehat buat diagnosa mentor.
4. **Kalender kampanye/festival ID** (`K2-D-GAP-002`).
5. **Seksi "Livestream Room" nol teks** (`K1-D-GAP-01`) — butuh PDF/OCR, gak kebuka dari markdown.

## Materi yang dibuang / diparkir (biar bisa dibantah)
- `_inbox/tiktok-go-dialihkan-ke-mcn-meago.md` — TikTok GO di luar scope KB seller, ke MCN MEAGO!.
- `_inbox/PARKIR-agency-ops-tsp.md` — materi agency-ops TSP (Day 1 Part 1 & Part 4) diparkir.
- Tidak ada entry yang dihapus saat merge — semua 162 dipertahankan.

## Urutan kerja yang disaranin
1. **Putuskan 5 CONFLICT teratas** (`M-D-CONFLICT-01/02`, `K1-D-CONFLICT-03/04/05`) — kelima
   nyentuh SATU rantai: urutan mulai jualan + durasi live. Selama terbuka, tiap entry
   produk/live/iklan berisiko saling bantah. Ini penentu isi, bukan tempat — putuskan dulu.
2. **Audit 5 M-D-MERGE** — gw baca pasangan entry lintas-KB, lebur yang benar kembar.
3. **Ingest Star Seller → isi gap Shopee** (`M-D-SCOPE-02`), batch Fase 1–6 terpisah.
4. **Beresin peringatan provenance** (136 "sumber tanpa penunjuk bagian") — mayoritas entry
   fundamental KB-2 yang kutip YouTube tanpa `bagian:`. Bukan error, tapi bikin klaim susah dilacak.
5. **Selaraskan `aksi_oleh`** (`M-D-SCOPE-01`) setelah `K1-D-SCOPE-04` final.

## Buat penggabungan dengan KB lain (batch ke-3+)
- Prefix ID yang sudah kepakai: `tts-*` (per kategori), `fnd-*`, `fnd-001..003` (bare, KB-1).
- Prefix D-code: `K1-`, `K2-`, `M-`. Batch berikutnya pakai tag baru (mis. `K3-`).
- `_manifest/MANIFEST.json` = indeks 162 ID buat deteksi tabrakan di merge berikutnya.
- Field non-standar: `aksi_oleh`, `audience` (cuma di entry KB-1), `confidence`, `platform`.

---

## Update — Batch Shopee (2026-08)

Batch `push-ready/` (skill `mea-knowledge-architect`, sesi terpisah) digabung ke tree kanonik ini.
Mengisi gap **Shopee — nol entry** yang jadi prioritas #1 di laporan Fase 6 di atas.

### Yang masuk
- **282 entry Shopee** (`kb/shopee/`): akun-dan-toko, analisis-performa-toko, iklan-dan-promosi,
  keuangan, layanan-pembeli, live-dan-video, pengiriman-dan-pesanan, penjual-star-dan-mall, produk.
  Semua `canonical`. Sumber dominan artikel resmi Shopee Seller Centre + beberapa transkrip
  YouTube Yohan dan slide training internal MEA (konten strategis, id seri `-1xx`).
- **15 entry diarsipkan** (`kb/_archive/pengumuman-dan-kebijakan-terbaru/`) — pengumuman/kebijakan
  bertanggal (PPh 22, perubahan UI, dll), keputusan `S-D-OUTDATED-001` sudah tertutup.
- **13 entry fundamental tambahan** ke `kb/fundamental/` — psikologi pembeli, strategi harga (2),
  strategi produk (3, kategori baru), operasional (3), analisa (2, gabung ke `analisa-dan-diagnosa`),
  mindset (1), retensi-dan-repeat-order (1, folder baru).
- Decision queue batch ini (10 keputusan, 4 sudah tertutup) digabung ke `DECISIONS.md` master
  dengan prefix `S-`.

### Temuan audit merge (bukan dari laporan batch aslinya)
Saat fundamental baru disandingkan ke `kb/fundamental/` lama pakai `overlap.py`, ketemu
**9 pasang entry yang topiknya sama/nyaris identik** — kemungkinan besar sumber video/slide yang
sama, ditranskrip ulang di dua batch berbeda dan gak ketangkep dedup di batch asalnya. Sempat
ditandai `status: blocked` sambil nunggu keputusan Yohan; **per 2026-08-31 kesembilannya sudah
diputus** — Yohan konfirmasi sumbernya memang sama, lalu tiap pasang digabung (versi paling
lengkap/confidence tertinggi dipertahankan, isi unik dari versi yang kalah digabung masuk,
sisanya diarsipkan). Detail per pasang di `DECISIONS.md` Bagian E (`S-D-MERGE-01` s.d. `09`,
semua ✅ tertutup) dan `MERGE-LOG.md`.
Overlap shopee-vs-tiktok-shop dan overlap internal shopee juga dicek (`overlap.py`) — gak ada
duplikat lintas-platform yang nyata, cuma satu klaster besar semu (kesamaan kosakata boilerplate
artikel resmi Shopee, bukan duplikat topik beneran).

### Status entry (kb/ gabungan, per 2026-08-31)
| Status | Jumlah | Catatan |
|---|---|---|
| canonical | 450 | shopee 282 + tiktok-shop 141 + fundamental 27 |
| blocked | 8 | tiktok-shop lama, tak disentuh sesi ini |
| archived | 24 | 15 `pengumuman-dan-kebijakan-terbaru` + 9 duplikat fundamental (`S-D-MERGE-01..09`, sudah diputus Yohan 2026-08-31 — lihat DECISIONS.md Bagian E) |

### Yang belum dikerjakan (di luar scope sesi ini)
- 4 baris decision queue batch Shopee masih `terbuka` (`S-D-CONFLICT-002/003`, `S-D-OUTDATED-002`,
  `S-D-GAP-001/002/003`) — semuanya kualitatif/non-blocking, gak nyentuh koreksi konten mendesak.
  3 `S-D-DEPTH` artikel resmi kepanjangan (`shp-ekspor-001/002`, `shp-mall-003`) sudah ditutup
  2026-08-31: dibiarkan utuh, dipecah nanti kalau memang kelihatan dibutuhkan (bukan preemptif).
- Sebagian besar entry Shopee (hasil scraping artikel resmi Shopee Seller Centre) ditulis sebagai
  ringkasan artikel, **belum** melalui pass "Kapan ini dipakai" / "Pertanyaan diagnosa" penuh
  seperti template `tiktok-shop` — `validate.py` menandai ini sebagai **peringatan** (bukan error,
  jadi tetap `canonical`), tapi ini kandidat kerja lanjutan kalau mau kualitasnya sejajar dengan
  entry TikTok Shop yang sudah full-template.
