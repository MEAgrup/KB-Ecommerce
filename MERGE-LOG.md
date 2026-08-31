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

---

# MERGE-LOG — Batch Shopee (31 Agu 2026)

Audit persis apa yang diubah saat menggabung batch `push-ready/` (hasil sesi terpisah skill
`mea-knowledge-architect`, isi gap Shopee) ke tree kanonik di atas.

Hasil: **467 entry aktif+blocked** (450 canonical + 17 blocked, 8 blocked di antaranya bawaan
`tiktok-shop` yang tak disentuh sesi ini — lihat §8 untuk rincian per platform) + **15
entry baru diarsipkan**, 1 pohon, `validate.py`: **0 error** (12 flag "bahasa hype" — semua
false positive, dicek manual satu-satu, lihat §5).

## 1. Tabrakan ID yang diselesaikan (renumber sisi batch Shopee)
Base (`kb/fundamental/` lama) pegang nomornya; entry baru lanjut dari nomor berikutnya.
Semua `related:` yang nunjuk ID lama sudah diperbarui.

| Kategori | ID lama (push-ready) | ID baru | Folder tujuan |
|---|---|---|---|
| algoritma-dan-data | `fnd-algoritma-001..002` | `fnd-analisa-004..005` | fundamental/analisa-dan-diagnosa/ |
| kondisi-ekonomi | `fnd-ekonomi-001` | `fnd-mindset-005` | fundamental/mindset-dan-kondisi-pasar/ |
| operasional | `fnd-operasional-001..003` | `fnd-operasional-005..007` | fundamental/operasional-dan-skala/ |
| psikologi-pembeli | `fnd-psikologi-001` | `fnd-psikologi-005` | fundamental/psikologi-pembeli-dan-nilai/ |
| strategi-harga | `fnd-harga-001..002` | `fnd-harga-003..004` | fundamental/strategi-harga/ |

`shp-*` (Shopee) gak ada tabrakan sama sekali — namespace kosong sebelumnya. Satu referensi
menggantung ditemukan & diperbaiki: `shp-akun-103` masih nunjuk id lama `fnd-algoritma-002`
(sudah jadi `fnd-analisa-005`).

## 2. Taksonomi disamakan
- Folder `operasional` → `operasional-dan-skala` (samakan pola nama folder lama).
- Folder `psikologi-pembeli` → `psikologi-pembeli-dan-nilai`.
- Folder `kondisi-ekonomi` → dilebur ke `mindset-dan-kondisi-pasar` (1 entry).
- 1 file salah folder di sumbernya: `strategi-harga/02-fokus-satu-pasar-daripada-nyebar.md`
  (frontmatter `kategori: strategi-produk`, tapi fisiknya ada di folder `strategi-harga`) —
  dipindah ke `strategi-produk/` biar folder & kategori sinkron.
- `retensi-dan-repeat-order/` dan `strategi-produk/` MASUK sebagai folder `fundamental/` baru
  (sebelumnya gak ada) — 1 dan 3 entry.

## 3. Folder yang MASUK sebagai folder baru (tanpa tabrakan)
- `shopee/{akun-dan-toko, analisis-performa-toko, iklan-dan-promosi, keuangan, layanan-pembeli,
  live-dan-video, pengiriman-dan-pesanan, penjual-star-dan-mall, produk}` — 282 entry, mengisi
  `K1-D-GAP-03`/`K2-D-GAP-01`.
- `_archive/pengumuman-dan-kebijakan-terbaru/` — 15 entry (`status: archived`), sesuai
  `S-D-OUTDATED-001` yang sudah diputus Yohan (2026-08-30) sebelum sesi ini.

## 4. Kode keputusan (D-code) diberi prefix asal
Decision queue batch Shopee (`push-ready/_decisions/DECISIONS-shopee.md`, 10 keputusan, format
tanpa prefix + 1 gaya `D-<TIPE>-<id-entry>` di beberapa frontmatter) digabung ke
`DECISIONS.md` master:
- Semua kode `D-CONFLICT-*`, `D-OUTDATED-*`, `D-GAP-*`, `D-SCOPE-*`, `D-DEPTH-shp-*` → prefix
  `S-` (10 keputusan, 4 sudah tertutup sebelumnya).
- Field `decisions:` di 6 entry Shopee yang masih pakai kode gaya lama ikut diprefix.
- Ditambah **9 keputusan baru** `S-D-MERGE-01..09` (lihat §5) yang gw angkat sendiri dari hasil
  `overlap.py` — bukan bagian decision queue asli batch Shopee.

## 5. Duplikat lintas-batch yang KETANGKEP overlap.py (bukan ditebak manual)
`overlap.py` dijalankan 3 kali: (a) `fundamental/` gabungan lama+baru, (b) `shopee/` internal,
(c) `shopee/` + `tiktok-shop/` gabungan.

- **(a) 9 pasang overlap nyata** — fundamental baru (materi YouTube Yohan) ternyata banyak
  beririsan sama `fundamental/` lama, kemungkinan sumber video sama yang ke-transkrip dua kali
  di batch berbeda. Kesembilan entry BARU ditandai `status: blocked` + `decisions:
  [S-D-MERGE-0N]`, entry lama tetap `canonical` jalan terus (lihat DECISIONS.md Bagian E untuk
  detail per pasang + rekomendasi).
- **(b) & (c) gak ada duplikat topik nyata.** Klaster besar (254 & 264 file) yang muncul di
  laporan overlap.py itu FALSE POSITIVE — kesamaan kosakata boilerplate bahasa resmi Shopee
  ("Penjual", "Pembeli", "Seller Centre"), bukan topik yang sama. Klaster kecil (2-8 file) yang
  tersisa semuanya sudah relasi yang diketahui dari merge KB-1×KB-2 sebelumnya (mis.
  `K2-D-MERGE-01/02/03`), gak ada yang baru dari batch Shopee.

Validate.py juga sempat menandai 15 error "bahasa hype" (`rahasia`, `dijamin`, `tanpa modal`) di
12 entry Shopee — semua dicek manual ke konteksnya: **false positive** dari filter kata kunci.
Konteksnya kutipan kebijakan resmi Shopee soal kerahasiaan OTP/password ("bersifat rahasia,
jangan dibagikan"), atau contoh klaim yang justru **DILARANG** ditulis di judul/gambar produk
("dijamin langsung kaya", "Dijamin Asli"). Gak diedit — mengubah kutipan kebijakan resmi biar
lolos filter kata kunci malah ngerusak akurasinya.

## 6. Meta yang digabung
- `_decisions/DECISIONS.md`: + Bagian D (10 keputusan `S-`, dari batch Shopee) + Bagian E (9
  keputusan `S-D-MERGE`, baru dari audit merge ini). Total **74 keputusan** di master queue.
- `_archive/README.md`: + 1 baris baru untuk `pengumuman-dan-kebijakan-terbaru/`.
- `shopee/README.md` (penanda "folder kosong") **dihapus** — gapnya sudah keisi, gak ada
  konvensi README per-folder lain di `kb/` (tiktok-shop juga gak punya).
- `LAPORAN-KB.md`: + section "Update — Batch Shopee (2026-08)" di bawah laporan Fase 6 lama.
- `MERGE-README.md`: ditulis ulang — namespace table + `shp-*` lengkap, catatan seri ganda
  (`001-0xx` resmi vs `1xx`/`2xx` strategis) untuk kategori yang punya dua sumber.
- `_manifest/`: diregenerasi ulang meliputi 467 entry (CSV + JSON), exclude folder `_*` (ikut
  konvensi `validate.py`).

## 7. Yang TIDAK gw putuskan sendiri
- **9 duplikat baru** (`S-D-MERGE-01..09`, §5 di atas) — mana yang jadi versi utama, mana yang
  diarsipkan. Rekomendasi udah gw kasih per pasang di DECISIONS.md, keputusan final Yohan.
- **3 artikel resmi Shopee masih kepanjangan** (`shp-ekspor-001/002`, `shp-mall-003`,
  `S-D-DEPTH-*`) — udah diidentifikasi sesi batch Shopee sebelumnya, belum dipecah, butuh sesi
  baca+tulis ulang terpisah (bukan keputusan ya/tidak).
- **Taksonomi `retensi-dan-repeat-order` jadi kategori sendiri atau tetap subset `analisa`** —
  disebut eksplisit di `S-D-MERGE-07` karena nyambung ke pertanyaan penamaan folder, bukan cuma
  soal isi mana yang menang.

## 8. Status entry & validasi
- Per `_manifest/MANIFEST.csv` (467 baris, sumber angka pasti — jangan hitung manual):
  `tiktok-shop` 149 (141 canonical + 8 blocked, tak disentuh sesi ini), `shopee` 282 (semua
  canonical, seluruhnya baru), `fundamental` 36 (27 canonical + 9 blocked — 9 blocked itu
  seluruhnya entry baru dari §5 di atas). Plus 15 `archived` di `_archive/` (di luar manifest).
- `validate.py` pada `kb/`: **0 error entry** (setelah 1 referensi menggantung diperbaiki dan
  12 flag hype dikonfirmasi false positive), **1.204 peringatan** (naik dari 227 — mayoritas
  peringatan baru adalah "gak ada bagian '## Kapan ini dipakai'" dan "'## Pertanyaan diagnosa'"
  di entry Shopee hasil scraping artikel resmi, yang memang ditulis format ringkasan-artikel,
  bukan format lengkap ala `tiktok-shop`. Ini bukan error dan entry tetap `canonical`, tapi
  dicatat di `LAPORAN-KB.md` sebagai kandidat kerja lanjutan kalau mau kualitasnya sejajar.
