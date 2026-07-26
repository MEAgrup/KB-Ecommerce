# MERGE-LOG — KB-1 + KB-2 (25 Jul 2026)

Audit persis apa yang diubah saat menggabung dua KB dari akun berbeda jadi satu tree kanonik.
**Base = KB-1** (root repo lama: `tiktok-shop/`, `fundamental/`, `shopee/`) — dipertahankan
apa adanya. **KB-2** (`kb/` lama: batch1 Canva + TSP) di-renumber & ditempatkan.

Hasil: **162 entry** (KB-1 97 + KB-2 65), 1 pohon, `validate.py`: **0 error entry**.

## 1. Tabrakan ID yang diselesaikan (renumber sisi KB-2)
Base KB-1 pegang nomornya; entry KB-2 lanjut dari nomor berikutnya. Semua `related:` yang
nunjuk ID lama sudah diperbarui (dicek validate.py: 0 broken link).

| Kategori | KB-2 (ID lama) | ID baru | Folder tujuan |
|---|---|---|---|
| konten | `tts-konten-001..003` | `tts-konten-010..012` | tiktok-shop/konten-dan-kreatif/ |
| live | `tts-live-001..007` | `tts-live-012..018` | tiktok-shop/live/ |
| produk | `tts-produk-001..008` | `tts-produk-010..017` | tiktok-shop/produk-dan-sku/ |
| affiliate→afiliasi | `tts-affiliate-001..003` | `tts-afiliasi-005..007` | tiktok-shop/afiliasi/ |

Total 21 ID direnumber (18 tabrakan literal + 3 penyamaan ejaan affiliate→afiliasi).

## 2. Taksonomi disamakan
- Ejaan `affiliate` (KB-2) → `afiliasi` (samakan dengan KB-1). Field `kategori:` ikut diubah.
- `kategori:` KB-2 diselaraskan ke folder KB-1: `konten`→`konten-dan-kreatif`, `produk`→`produk-dan-sku`.
- Folder KB-2 `produk-dan-toko` dilebur ke `produk-dan-sku` (KB-1). `konten-dan-video` dilebur ke `konten-dan-kreatif`.

## 3. Folder KB-2 yang MASUK sebagai folder baru (tanpa tabrakan)
- tiktok-shop/dasar (tts-dasar-001..003)
- tiktok-shop/script-jualan (tts-script-001..003)
- tiktok-shop/creative-dan-audience (tts-creative-001..002)
- tiktok-shop/metrik-dan-rumus (tts-metrik-001..004)
- tiktok-shop/traffic-dan-masalah-toko (tts-traffic-001..009)
- tiktok-shop/iklan/dasar-iklan (tts-iklan-001..003) — subfolder baru di dalam iklan/ KB-1
- fundamental/{analisa-dan-diagnosa, mindset-dan-kondisi-pasar, model-kerjasama-dan-komisi, operasional-dan-skala, psikologi-pembeli-dan-nilai, strategi-harga} (20 entry fnd-*)

KB-1 `fnd-001/002/003` DIBIARKAN di `fundamental/` root (base stabil, tak direnumber).

## 4. Kode keputusan (D-code) diberi prefix asal — mencegah bentrok
Dulu kedua KB sama-sama punya `D-CONFLICT-01`, `D-GAP-01`, `D-OUTDATED-01..04`, `D-DEPTH-01`,
`D-SCOPE-01` (8 bentrok). Solusi: prefix per asal.
- Semua D-code KB-1 → `K1-` (25 keputusan)
- Semua D-code KB-2 → `K2-` (21 keputusan)
- Field `decisions:` di 59 entry (48 KB-1 + 11 KB-2) ikut diprefix.

## 5. Referensi menggantung yang dipulihkan
- `K1-D-GAP-08` dirujuk entry `tts-afiliasi-002` (Kolaborasi Plus, blocked) tapi blok
  keputusannya gak pernah ditulis di DECISIONS.md KB-1. Dipulihkan sebagai blok penuh di
  bagian K1 supaya referensi resolve. (Bawaan KB-1, bukan cacat dari merge.)

## 6. Meta yang digabung
- `_decisions/DECISIONS.md`: queue master = **Bagian M** (9 keputusan merge baru) + **Bagian K1**
  (KB-1, prefix K1-) + **Bagian K2** (KB-2, prefix K2-). Total **55 keputusan**, semua TERBUKA.
- `_decisions/kamus-lokalisasi.md`: dibawa dari KB-2 (KB-1 tak punya).
- `_inbox/`: 2 scope-note KB-2 (TikTok GO, agency-ops TSP) + 2 txt mentah distage
  (`star-seller.txt`, `tokopedia-seller-university.txt`) + README.
- `_archive/`: README KB-1.
- `sources/`: `canva/` + `tsp/` (KB-2) + `knowledge_base_basic_seller.txt` (KB-1). Ditaruh
  SIBLING dari `kb/` supaya gak ikut di-scan validator.
- `_manifest/`: diregenerasi ulang meliputi 162 entry (CSV + JSON).

## 7. Yang TIDAK gw putuskan sendiri (Bagian M DECISIONS.md)
9 keputusan baru yang cuma kelihatan setelah dua KB disandingkan:
- `M-D-CONFLICT-01` durasi live (3–5 jam KB-1 vs angka TSP KB-2)
- `M-D-CONFLICT-02` urutan mulai iklan (urutan tetap KB-1 vs entry iklan KB-2)
- `M-D-MERGE-01..05` duplikat lintas-KB (afiliasi, produk/SKU, konten, live-metrik, benchmark-vs-metrik)
- `M-D-SCOPE-01` field `aksi_oleh` KB-2 belum ada
- `M-D-SCOPE-02` ingest `star-seller.txt` + `tokopedia-seller-university.txt` (batch berikutnya)

## 8. Status entry & validasi
- 148 canonical, 14 blocked (= KB-1 84/13 + KB-2 64/1). Cocok, tak ada entry hilang.
- validate.py pada `kb/`: **0 error entry**, 227 peringatan (bukan error).
  - 1 flag non-entry: `shopee/README.md` (penanda folder Shopee kosong, gap `K1-D-GAP-03`) —
    sama konvensi dengan KB-1 lama.
  - Peringatan terbanyak: 136 "sumber tanpa penunjuk bagian" (kualitas provenance bawaan,
    banyak di entry KB-2 yang kutip YouTube tanpa `bagian:`), 45 "canonical tapi decisions
    terbuka" (MEMANG sengaja — semua keputusan dibiarkan terbuka).
