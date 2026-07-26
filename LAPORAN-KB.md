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
