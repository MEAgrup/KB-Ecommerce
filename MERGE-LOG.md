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

---

# MERGE-LOG — Resolusi S-D-MERGE-01..09 & S-D-DEPTH (31 Agu 2026, lanjutan)

Yohan konfirmasi lewat chat: 9 duplikat fundamental memang dari sumber sama, dan 3 artikel
Shopee kepanjangan "dipecah kalau dibutuhkan" (kebijakan lama, bukan preemptif). Berikut eksekusinya.

## 1. Bug ditemukan & dibetulkan sebelum resolusi
- `fnd-psikologi-003`: frontmatter punya 2 baris `decisions:` (duplikat key YAML, bug dari edit
  sesi sebelumnya) — dibetulkan jadi satu baris.
- `fnd-analisa-005` (sebelum diarsipkan): section kedua "## Angka & patokan"-nya isinya boilerplate
  soal "artikel resmi Shopee" yang gak nyambung sama sekali ke entry ini (materi transkrip
  YouTube) — indikasi template/isi entry lain kebocor. Dicatat di keputusan S-D-MERGE-02.
- `fnd-harga-004`: judul & body bilang "lima pendekatan pricing" tapi isinya 6 poin (Bundling,
  Psychological, Promotional, Penetration, Premium, Value-Based) — dibetulkan jadi "enam" di
  semua tempat (title, H1, 2 baris body, Batasan).

## 2. Sembilan S-D-MERGE dieksekusi — semua ✅ tertutup
Pola umum: entry dengan `confidence` lebih tinggi ATAU cakupan lebih lengkap dipertahankan
sebagai kanonik, isi unik dari entry yang kalah digabung masuk (bukan dibuang), lalu entry yang
kalah dipindah ke `kb/_archive/fundamental-duplikat-batch-shopee/` dengan `status: archived` +
banner `[DIARSIPKAN]` yang nunjuk ke pengganti.

| Kode | Menang | Kalah (diarsipkan) | Catatan |
|---|---|---|---|
| S-D-MERGE-01 | `fnd-analisa-001` | `fnd-analisa-004` | +2 pertanyaan diagnosa digabung |
| S-D-MERGE-02 | `fnd-analisa-002` | `fnd-analisa-005` | +1 pertanyaan diagnosa; versi kalah ada bug copy-paste (lihat §1) |
| S-D-MERGE-03 | `fnd-mindset-003` | `fnd-mindset-005` | +1 insight (seller besar lebih rentan) |
| S-D-MERGE-04 | `fnd-operasional-001` | `fnd-operasional-005` | Gak ada isi unik untuk digabung |
| S-D-MERGE-05 | `fnd-operasional-002` | `fnd-operasional-006` | +1 pertanyaan diagnosa (ROAS) |
| S-D-MERGE-06 | `fnd-operasional-003` | `fnd-operasional-007` | +angka konkret (1-3 video/hari, live 3-5x/minggu) |
| S-D-MERGE-07 | `fnd-analisa-003` | `fnd-retensi-001` | +2 pertanyaan diagnosa + penjelasan segmentasi; folder `retensi-dan-repeat-order/` dihapus (kosong) |
| S-D-MERGE-08 | `fnd-psikologi-003` | `fnd-harga-003` | +1 trik (jelaskan harga saat live), jadi poin ke-8 |
| S-D-MERGE-09 | `fnd-harga-004` | `fnd-psikologi-004` | **Kebalik dari rekomendasi awal** — `fnd-harga-004` menang karena isinya lebih lengkap (5 prinsip Blue Ocean + 6 pendekatan pricing). Naik status jadi `canonical`. |

Catatan: 3 dari 9 keputusan (04, 05, 06, 09) hasilnya BEDA dari rekomendasi awal di DECISIONS.md
Bagian E — rekomendasi awal ditulis sebelum baca isi lengkap kedua versi; setelah dibaca, entry
yang lebih tinggi confidence-nya atau lebih lengkap yang menang, bukan otomatis yang lebih baru
atau lebih banyak kata.

## 3. Referensi menggantung yang dibetulkan
9 entry yang diarsipkan masih dirujuk `related:` dari 9 file lain (5 di luar pasangannya
langsung: `shp-akun-103`, `shp-iklan-102`, `fnd-strategi-001`, `fnd-strategi-002`,
`fnd-psikologi-005`) — semua diarahkan ulang ke ID pemenang.

## 4. Tiga S-D-DEPTH ditutup (`shp-ekspor-001/002`, `shp-mall-003`)
Opsi B — dibiarkan utuh, `decisions:` dikosongkan. Kebijakan: pecah kalau dibutuhkan (ada tanda
konkret dikutip sepotong / diminta tim), bukan preemptif.

## 5. Status & validasi akhir
- 458 entry aktif (450 canonical, semua blocked sudah tuntas jadi 0) + 24 archived (15 lama +
  9 baru dari resolusi ini).
- `validate.py`: 0 error nyata (12 flag hype false-positive yang sama, tidak berubah).
- `_manifest/` diregenerasi ulang (458 entry).

---

# MERGE-LOG — Pengisian gap Shopee Tier 1/2 (01 Sep 2026)

Yohan minta 6 topik spesifik dari daftar prioritas di `LAPORAN-KB.md` diisi dengan entry diagnostik
baru, dengan arahan konten spesifik per topik (lihat brief lengkap di riwayat chat). Semua entry
baru masuk namespace `-1xx` (strategis, bukan hasil scraping artikel resmi).

## Entry baru (6)

| ID | Judul | Inti logika |
|---|---|---|
| `shp-performa-103` | Kenapa performa toko turun — diagnosa 5 area | Dibongkar dari kode aplikasi Bedah Toko Tiksmart (5 area berbobot: Iklan 26%/Konversi 24%/Produk 20%/Layanan 16%/Kanal 14%; urutan prioritas penalti→pembatalan→iklan→produk→kanal→konversi→layanan) — bukan link yang dibagikan, cuma logikanya. Arahkan ke fitur Bedah Toko gratis Tiksmart.ai untuk hitungan otomatis. |
| `shp-produk-107` | Produk turun/dihapus/diblokir — dua penyebab | Pisah 2 jalur: (A) pelanggaran/poin penalti (link ke `shp-produk-009/011/013/017/018`) vs (B) penjualan mingguan turun → algoritma nurunin eksposur organik (link ke `fnd-analisa-002`, `shp-performa-102`). Ketemu 1 temuan taksonomi (`shp-produk-013` judulnya nyasar) — dicatat sebagai `S-D-SCOPE-001`, bukan diputus sendiri. |
| `shp-akun-104` | Akun/toko dibatasi — cek poin penalti dulu | Nyambungin gejala (`shp-akun-009/010/014`) ke akar masalah (`shp-penalti-002/003/005`, `shp-toko-021/030`) yang sudah ada di KB tapi belum di-link. |
| `shp-live-101` | Strategi Live Shopee beda dari TikTok | Riset web: Shopee search-based (traffic dari yang udah niat cari) vs TikTok discovery-based (algoritma nyebar ke penonton baru) — strategi jadi maksimalkan fitur & konsistensi jadwal, bukan kejar reach viral. |
| `shp-pengiriman-101` | SOP dasar inbound-outbound | Riset web: 3 penyebab gagal kirim tepat waktu paling umum (komunikasi antar-bagian putus, pencatatan manual, gak ada prioritas pesanan) — bukan soal stok/kecepatan kerja. |
| `shp-iklan-104` | Pilih SKU siap diiklankan | Dua lapis kesiapan SKU: relevansi (judul/deskripsi/gambar nyambung ke keyword) dan performa (CTR/CVR organik sudah kebukti). Arahkan ke fitur cek SKU siap iklan di Tiksmart.ai. |

## Sumber non-Shopee yang dipakai
- **Kode aplikasi Bedah Toko Tiksmart** (file HTML internal MEA, diakses lewat Google Drive) — dibaca
  logikanya (fungsi skor 5 area, mesin klinik gejala-diagnosa-resep, ambang numerik) untuk
  `shp-performa-103` dan `shp-iklan-104`. **Link Drive-nya sendiri sengaja TIDAK dicantumkan** di
  entry KB manapun sesuai arahan Yohan — cuma logikanya yang dipakai buat nulis ulang jadi bahasa
  KB, dan entry mengarahkan ke Tiksmart.ai sebagai next step, bukan ke file internal.
- **Riset web publik** (WebSearch) untuk `shp-live-101` (perbandingan model traffic Shopee vs
  TikTok Shop) dan `shp-pengiriman-101` (SOP fulfillment e-commerce) — sumber dicantumkan sebagai
  link di bagian Batasan tiap entry, `confidence: sedang` (bukan `tinggi`) karena bukan data
  internal MEA atau dokumentasi resmi Shopee.

## Cross-link yang ditambahkan
9 entry existing (`shp-performa-101/102`, `shp-akun-010`, `shp-produk-011/013/017`, `shp-live-010`,
`shp-pengiriman-068/069/074`, `shp-iklan-205`, `fnd-analisa-002`) di-update `related:`-nya biar
nyambung dua arah ke entry baru — bukan cuma entry baru yang nunjuk ke lama.

## Keputusan baru yang diangkat (bukan diputus sendiri)
`S-D-SCOPE-001` di `DECISIONS.md` Bagian F — `shp-produk-013` judulnya nyasar (bilang "tingkatkan
kualitas listing" tapi isinya daftar kebijakan pelanggaran). Rekomendasi: biarkan judul asli
(sesuai sumber resmi Shopee), cukup dijembatani lewat `related:`.

## Validasi
464 entry (458 + 6 baru). `validate.py`: 0 error baru (12 flag hype false-positive yang sama,
gak berubah). Semua entry baru dicek related-nya resolve, gak ada broken link.
