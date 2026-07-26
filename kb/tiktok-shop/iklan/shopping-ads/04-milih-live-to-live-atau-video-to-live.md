---
id: tts-ads-004
title: Milih LIVE-to-LIVE atau Video-to-LIVE
platform: tiktok-shop
kategori: iklan/shopping-ads
depth: 2
audience: member
aksi_oleh: member
status: blocked
confidence: sedang
sensitif_waktu: true
valid_as_of: 2024-Q2
sources:
  - file: TSP_Roadshow_Deck_Final.md
    bagian: "slide 32–33 — LIVE-to-LIVE vs Video-to-LIVE + rasio alokasi anggaran"
related: [tts-ads-003, tts-live-007, tts-segmentasi-001]
decisions: [K1-D-CONFLICT-02, K1-D-OUTDATED-01]
---

# Milih LIVE-to-LIVE atau Video-to-LIVE

> ⚠️ **Update kebijakan iklan (Jul 2026): PSA sudah tidak ada lagi.** Semua jenis iklan lama
> (PSA, VSA, LSA) sekarang dilebur ke **GMV Max** — GMV Max adalah titik masuk beriklan.
> Mekanisme di bawah tetap ditulis sebagai konteks logika, tapi **jangan arahkan member mulai
> dari PSA** — arahkan langsung ke GMV Max. GMV Max butuh minimal 1 video yang sudah ada.
> Lihat `M-D-CONFLICT-02` & `K1-D-OUTDATED-01`.


> ⛔ **`blocked` untuk tabel alokasi budget-nya.** Tabel itu pakai skema segmentasi toko
> yang belum diputuskan (`D-CONFLICT-02`). Bedanya dua format dan siapa yang cocok pakai
> apa — itu aman dipakai.

## Ringkasan

Dua format, dan pembagiannya soal pengalaman. **LIVE-to-LIVE** nampilin live room yang sedang jalan — cocok buat **seller baru** karena gak perlu bikin konten tambahan. **Video-to-LIVE** ngarahin traffic dari video pendek ke live room — cocok buat **seller berpengalaman** yang udah punya arsip video yang perform.

## Kapan ini dipakai

Dipakai waktu mau mulai LSA dan bingung format mana. Juga dipakai waktu member udah lama pakai satu format dan performanya mentok.

## Isi

**LIVE-to-LIVE — nampilin live room aktual.**

Cocok buat: seller baru **dan** seller yang udah berpengalaman live.

Kelebihannya, dari sumber:
- **Gak perlu bikin konten tambahan** — yang diiklanin live room-nya sendiri
- **Bisa manfaatin tren** — karena real-time
- **Bisa ngajak kreator atau selebritas** dalam live

**Video-to-LIVE — ngarahin traffic dari video pendek ke live room.**

Cocok buat: seller berpengalaman.

Kelebihannya:
- **Pakai video populer dari kampanye sebelumnya** buat ngarahin traffic ke live
- **Edit ulang video lama** buat bikin video baru

**Kenapa Video-to-LIVE butuh pengalaman:** dia butuh **arsip**. Kalau lu belum punya video yang kebukti perform, gak ada yang bisa dipakai buat ngarahin traffic. Jadi ini bukan soal skill — ini soal punya bahan atau nggak.

**Arah perkembangannya**, dari sumber: seller yang baru aktif live bisa mulai dengan **LIVE-to-LIVE**. Tapi seiring GMV naik, akan lebih optimal kalau pakai **Video-to-LIVE**.

Perhatiin arah pergeserannya: makin besar toko, makin besar porsi Video-to-LIVE. Di tabel alokasi sumber, rasio LIVE-to-LIVE : Video-to-LIVE geser dari **4:6** ke **8:2** — tapi arah pergeserannya di sumber ambigu soal mana yang naik, dan tabelnya pakai skema segmentasi yang belum diputuskan. Itu bagian yang `blocked`.

**Yang bisa dipakai sekarang tanpa tabelnya:** mulai dari LIVE-to-LIVE, dan begitu lu punya beberapa video yang kebukti perform, tambahin Video-to-LIVE. Jangan pindah total — dua-duanya jalan bareng dengan porsi yang bergeser.

**Prasyarat Video-to-LIVE** dari materi live: volume video baru **L30d > 30 upload**, dan tiap teaser harus punya info produk, info promo, dan **CTA yang kuat ke livestream**. Detailnya di `tts-live-007`.

## Yang bikin gagal

**Mulai dari Video-to-LIVE waktu belum punya arsip video.** Gak ada bahannya.

**Pindah total dari satu format ke satu format.** Rasionya bergeser, bukan berganti.

**Video-to-LIVE tanpa CTA ke live.** Video yang bagus tapi gak ngajak masuk live room cuma jadi video biasa.

**Ngiklanin live room yang lagi kosong atau host-nya gak siap.** LIVE-to-LIVE nampilin apa yang sedang terjadi. Kalau yang sedang terjadi jelek, itu yang diiklanin.

## Pertanyaan diagnosa

1. **Ada berapa video yang kebukti perform di 30 hari terakhir?** Ini yang nentuin Video-to-LIVE mungkin atau nggak.
2. **Live-nya udah konsisten?** LIVE-to-LIVE ngiklanin yang sedang jalan.
3. **Kalau udah pakai Video-to-LIVE — teasernya ada info produk, promo, dan CTA ke live?** Tiga-tiganya, bukan salah satu.
4. **Sekarang porsinya berapa-berapa?** Buat tahu arah geserannya.

## Batasan

Tabel alokasi anggaran per tipe toko masih `blocked`. Angka rasionya (4:6 sampai 8:2) ada di sumber tapi pemetaan ke tipe toko-nya ambigu di hasil ekstraksi, dan skema segmentasinya sendiri belum diputuskan.

Semua ini dari Q2 2024, sebelum Live GMV Max. Sekarang pilihan iklan live gak cuma dua format LSA ini — lihat `tts-gmvmax-005`. Lihat juga `D-OUTDATED-01`.
