# Decision Queue — KB Shopee Kampung Seller

Urutan berdasarkan dampak (blocking + sering ditanya → berpotensi rugi uang → kontradiksi → indikasi usang → gap → scope), sesuai `references/decision-queue.md`.

---

## 1. Kontradiksi & berpotensi bikin member rugi uang

### D-CONFLICT-001 · Klaim "Admin Fee 10%" di deck Shopee Mastery 2026 vs kebijakan resmi

**Status:** terbuka
**Entry terdampak:** tidak ada entry kanonik yang memuat klaim ini (sengaja dikeluarkan sebelum masuk KB — lihat `fnd-strategi-002`, yang cuma ambil bagian framework dari deck ini)

**Masalahnya:**
Slide "Shopee Mastery 2026" (materi internal MEA) menyebut "Admin Fee 10% (Jan 2026)" sebagai angka tunggal. Setelah dicek ke artikel resmi (`shp-biaya-001`, `shp-biaya-005`), Biaya Administrasi Shopee sebenarnya **bertingkat 2,5%-12,5%** tergantung kategori produk dan tipe penjual (Non-Star/Star/Star+/Mall), bukan angka flat 10%.

**Kalau salah diputuskan:**
Kalau angka "10%" ini terlanjur dipakai mentor untuk hitung-hitungan margin ke member, member bisa salah estimasi margin — bisa terlalu optimis (kalau kategori aslinya kena >10%) atau terlalu pesimis (kalau kategori aslinya <10%). Ini langsung menyentuh keputusan bisnis member.

**Opsi:**
- **A** — Buang klaim "10%" ini sepenuhnya dari materi apapun yang dipakai ke member; selalu arahkan ke tabel biaya administrasi resmi per kategori (`shp-biaya-001`).
- **B** — Ganti jadi rentang "2,5%-12,5% tergantung kategori & tipe penjual" di semua materi turunan dari deck ini.
- **C** — Biarkan deck asli sebagai materi internal (bukan buat member), tidak perlu diubah, asal tidak dipakai buat komunikasi ke member.

**Rekomendasi:** A + C. Deck training internal boleh tetap ada apa adanya untuk konteks internal, tapi jangan pernah diturunkan jadi materi member tanpa dikoreksi ke angka resmi.

**Keputusan Yohan (2026-08-30):** Abaikan. Klaim ini gak pernah masuk entry kanonik manapun (sudah dikeluarkan dari awal), dan deck sumbernya dibiarkan apa adanya sebagai materi internal — gak perlu tindakan lebih lanjut.
**Status:** ✅ tertutup

---

### D-CONFLICT-002 · `shp-iklan-101` (cara kerja GMV Max) — observasi lapangan, bukan dokumentasi resmi

**Status:** terbuka
**Entry terdampak:** `shp-iklan-101` (status: canonical, tapi confidence rendah + sensitif_waktu)

**Masalahnya:**
Entry ini menjelaskan cara kerja algoritma GMV Max berdasarkan pengalaman uji coba satu agency (Juli 2026), bukan dokumentasi resmi Shopee (yang memang tidak mempublikasikan detail algoritma). Narasumber sendiri berulang kali bilang "gua enggak tahu 100% benar."

**Kalau salah diputuskan:**
Kalau interpretasi ini keliru dan disampaikan sebagai fakta ke member, saran soal kenapa iklan mereka "gak jalan" bisa salah arah — member bisa audit hal yang salah padahal masalahnya di tempat lain.

**Opsi:**
- **A** — Biarkan `canonical` tapi selalu dibaca dengan disclaimer "berdasarkan pengamatan tim, bukan dokumentasi resmi" (sudah ada di bagian Batasan entry ini).
- **B** — Turunkan jadi `draft-ai` sampai ada konfirmasi tambahan dari dukungan resmi Shopee atau observasi berulang di klien lain.

**Rekomendasi:** B — mengingat ini topik yang berubah cepat (GMV Max baru diberlakukan penuh ~Juli 2026) dan dampaknya langsung ke budget iklan member, lebih aman jadi draft-ai dulu sampai diverifikasi lebih lanjut.

**Keputusan Yohan:** _(kosong)_

---

### D-CONFLICT-003 · `shp-mall-101` (Shopee Mall vs Star) — angka kenaikan order 30% dari pengalaman pribadi

**Status:** terbuka
**Entry terdampak:** `shp-mall-101` (status: canonical, confidence rendah, sensitif_waktu)

**Masalahnya:**
Klaim "order naik ~30% setelah jadi Mall" dan "selisih admin gak sampai 5%" adalah pengalaman satu toko/agency, bukan data resmi Shopee atau rata-rata industri. Entry sudah punya bagian Batasan yang menjelaskan ini, tapi karena dampaknya ke keputusan besar (ajukan Mall atau tidak, yang prosesnya bisa makan waktu ~1 tahun karena HAKI), perlu keputusan eksplisit soal boleh/tidaknya dipakai buat konsultasi member.

**Kalau salah diputuskan:**
Member bisa mengejar status Mall dengan ekspektasi kenaikan order yang gak sesuai realita kategori produknya sendiri, padahal effort HAKI-nya besar (proses ~1 tahun).

**Opsi:**
- **A** — Tetap dipakai sebagai referensi kualitatif ("banyak yang ngerasain kenaikan order"), tanpa menyebut angka 30% spesifik ke member.
- **B** — Simpan angka 30% tapi selalu dibingkai eksplisit sebagai "pengalaman satu toko, bukan jaminan."

**Rekomendasi:** B (entry sudah dibingkai begitu) — cukup pastikan tim gak drop bagian Batasan-nya waktu dipakai ke member.

**Keputusan Yohan:** _(kosong)_

---

## 2. Indikasi usang (D-OUTDATED)

### D-OUTDATED-001 · Seluruh folder `pengumuman-dan-kebijakan-terbaru` (15 entry)

**Status:** terbuka
**Entry terdampak:** `shp-pengumuman-001` s.d. `shp-pengumuman-015`

**Masalahnya:**
Ini bukan artikel "cara kerja fitur" yang stabil, tapi pengumuman kebijakan/perubahan bertanggal (PPh Pasal 22, perubahan nama wilayah, update tampilan Kesehatan Toko, dll). Sifatnya inherently sementara — begitu kebijakannya berubah lagi atau sudah settled jadi kebijakan permanen, isi pengumuman ini jadi basi duluan dibanding kategori lain.

**Kalau salah diputuskan:**
Kalau dibiarkan berstatus `canonical` selamanya tanpa jadwal recheck, tim bisa kasih info pajak/kebijakan yang sudah kadaluarsa ke member — khusus soal pajak (PPh 22) ini bisa berdampak ke kepatuhan pajak member.

**Opsi:**
- **A** — Semua entry di folder ini dikasih review cycle pendek (submit `D-OUTDATED` ulang tiap 3 bulan), tetap `canonical` untuk sekarang.
- **B** — Pindahkan folder ini ke `_archive/` sepenuhnya — anggap sebagai log historis, bukan entry yang dipakai jawab member langsung (member yang tanya soal pajak/kebijakan terbaru diarahkan cek langsung ke Seller Centre / pengumuman resmi Shopee terbaru).
- **C** — Biarkan `canonical` tapi entry-nya ditandai jelas "cek tanggal, kebijakan bisa sudah berubah" di setiap judul.

**Rekomendasi:** B untuk yang murni pengumuman sesaat (perubahan nama wilayah, update tampilan UI), A untuk yang masih relevan sebagai konteks kebijakan berkelanjutan (PPh 22, perizinan berbasis risiko) — tapi keputusan mana masuk grup mana perlu baca sekilas Yohan sendiri, bukan ditebak skill.

**Keputusan Yohan (2026-08-30):** Opsi B untuk semua 15 entry — dipindah ke `_archive/`, status diubah jadi `archived`. Dianggap log historis, gak dipakai jawab member langsung.
**Status:** ✅ tertutup — 15 entry sudah dipindah ke `kb/_archive/pengumuman-dan-kebijakan-terbaru/`

---

### D-OUTDATED-002 · Klaim kebijakan 2026 lain di deck Shopee Mastery yang belum dicek satu-satu

**Status:** terbuka
**Entry terdampak:** tidak ada entry kanonik (materi mentah masih di `materi/slide-mea-internal/shopee-mastery-2026-training-deck.md`, sengaja belum dikanonikkan)

**Masalahnya:**
Selain admin fee (sudah dicek, lihat D-CONFLICT-001) dan subsidi Gratis Ongkir XTRA (sudah dicek, akurat), deck ini masih punya klaim lain yang belum di-cross-check ke artikel resmi: batas COD/Pos Reguler Rp1.000.000, atribusi klik GMV Max 7 hari/tampilan 1 hari, kategori produk sensitif (senjata tajam, obat tanpa BPOM digital, emas, bulky item), dan klaim "10k+ Sellers Trained / 150% Avg GMV Growth" (statistik marketing MEA sendiri, tanpa sumber/metodologi disebutkan).

**Kalau salah diputuskan:**
Kalau salah satu angka ini keliru dan terlanjur disampaikan ke member sebagai fakta, dampaknya bervariasi — dari sekadar informasi yang kurang tepat sampai ke keputusan produk (misal soal kategori terlarang) yang salah.

**Opsi:**
- **A** — Cross-check semua klaim tersisa satu-satu ke artikel resmi sebelum deck ini dipakai sumber entry apapun.
- **B** — Anggap deck ini murni materi internal training (bukan sumber KB member), cukup dipakai sebagai konteks internal tanpa perlu dikanonikkan lebih jauh.

**Rekomendasi:** B untuk sekarang (sudah sesuai keputusan sebelumnya — cuma bagian framework evergreen yang diambil jadi `fnd-strategi-002`), A kalau nanti mau dipakai lebih jauh sebagai sumber member-facing.

**Keputusan Yohan:** _(kosong)_

---

## 3. Gap yang kelihatan waktu ditanya

### D-GAP-001 · `shp-iklan-103` (Shopee Ads mentor deck) — 4 dari 8 section-nya kosong

**Status:** terbuka
**Entry terdampak:** `shp-iklan-103`

**Masalahnya:**
Materi sumbernya (slide) untuk section "Jenis-Jenis Iklan Shopee & Kegunaannya", "Tips Memilih Produk yang Siap Diiklankan", "Fitur-Fitur dalam Dashboard Iklan Shopee", dan "Strategi Penggunaan Shopee Ads" isinya visual/diagram yang gak ke-ekstrak jadi teks — cuma judul section yang kebaca.

**Kalau salah diputuskan:**
Gak langsung bikin salah jawab, tapi tim bisa mengira topik ini "sudah ada" di KB padahal isinya bolong — kalau member tanya detail jenis-jenis iklan Shopee, entry ini gak akan cukup.

**Opsi:**
- **A** — Minta slide asli (bukan hasil ekstraksi teks) untuk dilihat manual dan dilengkapi.
- **B** — Biarkan gap ini, andalkan artikel resmi Shopee soal iklan (`shp-iklan-006` dst) untuk isi yang hilang.

**Rekomendasi:** B untuk sekarang (artikel resmi sudah cukup mendetail soal iklan Shopee), A kalau ternyata konten di slide itu ada insight khas MEA yang gak ada di sumber resmi.

**Keputusan Yohan:** _(kosong)_

---

### D-GAP-002 · Video "Menghadapi KONDISI BURUK" (kasus korupsi MBG) — sengaja tidak dikanonikkan

**Status:** terbuka — bukan blocking, tapi perlu keputusan scope
**Entry terdampak:** tidak ada (materi mentah masih ada di `materi/transkrip-yohan-youtube/`)

**Masalahnya:**
Video ini isinya opini/analisis narasumber tentang dampak kasus dugaan korupsi program MBG (Juni 2026) ke ekonomi & bisnis online. Kontennya campuran antara pelajaran bisnis yang transferable (transparansi, jangan bergantung satu sumber pendapatan) dengan komentar politik/berita spesifik yang berisiko kalau disajikan sebagai "knowledge" netral.

**Opsi:**
- **A** — Biarkan di luar KB sepenuhnya (keputusan saya sekarang).
- **B** — Ekstrak cuma prinsip bisnis transferable-nya (diversifikasi, transparansi) jadi entry pendek tanpa menyebut kasus spesifik.
- **C** — Masukkan penuh sebagai konteks historis di `_archive/`.

**Rekomendasi:** A (sudah dijalankan) — video sejenis ini kemungkinan akan muncul lagi dari channel YouTube Yohan ke depannya (konten reaktif terhadap berita), jadi perlu kebijakan baku: video "reaksi berita/politik" secara default gak masuk KB kecuali Yohan yang putuskan sebaliknya.

**Keputusan Yohan:** _(kosong — sekaligus jadi kebijakan buat batch KB berikutnya)_

---

### D-GAP-003 · JAWARA 20 (promo event) — cuma daftar topik, gak ada isi materi

**Status:** terbuka — bukan blocking
**Entry terdampak:** tidak ada (materi mentah di `materi/slide-mea-internal/jawara20-promo-banjir-orderan-produk-hero-shopee.md`)

**Masalahnya:**
Sesuai keputusan Yohan (hook & harga promo dibuang), tapi setelah dibuang yang tersisa cuma 5 bullet topik ("Riset market & kompetitor", "Strategi pemilihan konten", dst) tanpa penjelasan — materinya sendiri gak pernah tertangkap di slide (isinya disampaikan lisan waktu event).

**Opsi:**
- **A** — Biarkan sebagai gap, gak dipaksa jadi entry kosong.
- **B** — Kalau ada rekaman/notulen event JAWARA 20 yang lebih lengkap, bisa dipakai buat isi entry ini nanti.

**Rekomendasi:** A untuk sekarang.

**Keputusan Yohan:** _(kosong)_

---

## 4. D-DEPTH — 68 artikel resmi kepanjangan (>1.200 kata)

**Status:** ✅ diproses (2026-08-30) sesuai keputusan Yohan "pecah kalau dibutuhkan"

**Yang sudah dikerjakan:**
Saya baca satu-satu ke-68 entry (bukan cuma judul), pakai tes dari skill: "apakah bisa dipecah jadi dua pertanyaan yang berdiri sendiri?"

- **1 entry dipecah** — `shp-iklan-006` (Tentang Iklan Shopee, 5.594 kata) beneran menggabungkan 4 produk iklan berbeda (GMV Max, Live, Toko, Banner) plus evaluasi performa — tiap bagian jawab pertanyaan member yang beda-beda. Dipecah jadi **5 entry baru**: `shp-iklan-006` (overview: jenis/syarat/kebijakan konten), `shp-iklan-201` (cara buat & atribusi GMV Max), `shp-iklan-202` (cara buat Iklan Toko), `shp-iklan-203` (cara buat Iklan Live & Banner), `shp-iklan-205` (cara evaluasi performa: CTR/ACOS/ROAS).
- **63 entry dikonfirmasi TIDAK perlu dipecah** — flag `D-DEPTH` dihapus dari frontmatter-nya. Ini termasuk tabel referensi (biaya per kategori produk, subsidi ongkir per kategori) yang panjang karena mencakup banyak kategori untuk SATU pertanyaan ("berapa biaya kategori X"), dan panduan proses yang panjang karena banyak langkah untuk SATU tugas (mis. upload produk, kelola chat) — bukan beberapa topik yang tercampur.
- **3 entry masih direkomendasikan dipecah, belum dikerjakan** (kehabisan waktu di sesi ini): `shp-ekspor-001` (Program Ekspor Shopee FLEXI, 6.634 kata — bundling overview/biaya/cara gabung-berhenti/product sync/top up saldo iklan/fitur diskon), `shp-ekspor-002` (Tentang Program Ekspor Shopee, 5.234 kata), `shp-mall-003` (Penjual Shopee Mall, 5.033 kata — bundling keuntungan/syarat/biaya/cara gabung-berhenti/monitoring performa/kebijakan pelanggaran). Ketiganya masih ditandai `decisions: [D-DEPTH-<id>]` di frontmatter.

**Keputusan Yohan:** Sudah dijalankan ("pecah kalau dibutuhkan") — 1 dipecah, 63 dikonfirmasi gak perlu, 3 sisanya masih di antrean kalau mau dilanjutin.

---

## 5. D-SCOPE (sudah diputuskan, dicatat untuk jejak)

### D-SCOPE-001 · Standar skor performa dari MEA Shopee Report Engine — boleh masuk KB member

**Status:** ✅ tertutup (2026-08-30)
**Entry terdampak:** `shp-performa-101`, `shp-performa-102`

**Keputusan Yohan:** Boleh di-share ke KB member. Sebagian data platform, sebagian pengalaman agency — sudah dilabel di masing-masing entry (bagian "Batasan" tiap entry menjelaskan ini bukan angka resmi Shopee, tapi standar internal MEA).

### D-SCOPE-002 · JAWARA 20 — hook & harga promo dibuang

**Status:** ✅ tertutup (2026-08-30)
**Keputusan Yohan:** Setuju, silabus masuk KB (kalau ada isinya — lihat D-GAP-003), hook/harga dibuang.
