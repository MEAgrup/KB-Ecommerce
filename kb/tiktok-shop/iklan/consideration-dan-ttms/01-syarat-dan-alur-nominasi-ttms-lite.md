---
id: tts-ttms-001
title: Syarat dan alur nominasi TTMS Lite
platform: tiktok-shop
kategori: iklan/consideration-dan-ttms
depth: 3
audience: member
aksi_oleh: via-agency
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: 2026-01
sources:
  - file: Library_Tiktok.md
    bagian: "§[TTMS Lite Version] Market Scope — Important, Nomination Submission, Step to Activate"
related: [tts-ttms-002, tts-ttms-003, tts-segmentasi-003]
decisions: [K1-D-OUTDATED-03]
---

# Syarat dan alur nominasi TTMS Lite

## Ringkasan

TTMS (TikTok Market Scope) itu alat data level brand. Yang paling penting diketahui sebelum apa pun: **begitu onboard ke Lite, gak bisa pindah ke versi full.** Itu keputusan sekali seumur hidup per brand, dan satu-satunya bagian dari entry ini yang gak bisa dibalik kalau salah.

## Kapan ini dipakai

Dipakai waktu toko udah belanja iklan besar dan butuh data pasar level brand. Muncul di daftar prioritas mulai **S2**, dengan syarat belanja **$3.000/bulan**.

## Isi

**Syarat yang disebut sumber:**
- Diproses dalam **14–20 hari kerja** setelah semua informasi lengkap dikirim TikTok
- Periode nominasi: **tanggal 1 dan 15** tiap bulan
- Cuma **Enterprise Agency dengan perwakilan TikTok khusus** yang bisa mengajukan
- Ditujukan buat brand dengan kehadiran kuat di TikTok Shop
- TikTok berhak menolak aplikasi yang gak memenuhi kriteria
- **Diajukan di level BRAND**, bukan level toko
- **Sekali onboard ke Lite, gak bisa pindah ke full version.** Pastikan pilih versi yang tepat dari awal

**Ambang belanja:** submit allowlist kalau klien udah belanja **$3.000/bulan**. Klien yang belum jalanin Consideration Ads bisa dinominasikan, tapi link TTMS-nya baru dibagikan setelah nyampe **$1.000 dalam satu bulan** atau **$3.000 dalam tiga bulan** — mana yang lebih dulu.

**Beda Lite dan full yang disebut sumber:** cuma versi full yang punya data **NSR (Non-Sales Revenue)**. TTMS Lite gak punya fitur itu. Ini yang paling perlu dipertimbangin sebelum milih, karena pilihannya permanen.

**Data yang harus disiapin buat nominasi:**

*Informasi dasar (wajib):* nama resmi brand (bukan gabungan dua brand), logo brand (rasio mendekati persegi, jpg/png/jpeg, di bawah 5MB), Level 1 Vertical, negara operasi brand.

*Binding Account ID (wajib):* TTAM Advertiser ID, TTCM & TTO Account ID, TTBA User ID, TikTok Shop ID.

Untuk semua ID kecuali Shop ID, versi Lite cuma dukung **Fully Captured** — artinya semua aktivitas di bawah ID itu punya satu brand saja, akunnya dimiliki dan dioperasikan brand itu sendiri, dan gak ada risiko brand lain kecampur. Cuma **Shop ID** yang punya opsi Partially Captured (buat toko multi-brand).

**Dua hal yang bikin data hilang** dan gampang kelewat:
- ID yang **gak ada di TikTok Business Center** lu bakal dikecualikan dan bikin data bolong
- Advertiser ID agency juga **harus di-bind ke BC brand**

**Satu langkah teknis yang penting:** buat tiap akses TTMS, bikin **Shell BC (dummy BC)** di bawah brand-nya. Jangan sambungin TTMS ke BC utama agency (yang dipakai bareng brand lain) atau ke BC klien langsung.

Alasannya, dari sumber: **orang yang approve invite link TTMS otomatis jadi owner akses TTMS Lite-nya.** Jadi tim lu yang harus bikin Shell BC-nya, lalu share akses ke agency dan klien.

## Angka & patokan

| Patokan | Nilai | Sumber |
|---|---|---|
| Ambang belanja buat submit allowlist | $3.000/bulan | Library_Tiktok §TTMS Lite |
| Alternatif ambang | $1.000 dalam 1 bulan **atau** $3.000 dalam 3 bulan | idem |
| Waktu proses | 14–20 hari kerja | idem |
| Periode nominasi | Tanggal 1 dan 15 tiap bulan | idem |
| Ukuran maks logo | 5MB | idem |

## Yang bikin gagal

**Milih Lite tanpa mikirin butuh NSR atau nggak.** Gak bisa dibalik.

**Sambungin TTMS ke BC utama agency.** Bikin akses TTMS kecampur antar brand.

**Orang yang salah approve invite link-nya.** Yang approve jadi owner. Ini kesalahan permanen yang gampang kejadian.

**Ngirim ID yang belum di-bind ke Business Center.** Datanya bolong dan gak ketahuan sampai dashboard-nya kebuka.

**Nominasi di level toko, bukan level brand.** Diajukan di level BRAND.

## Yang butuh agency

Seluruh entry ini lewat agency, dan itu bukan pilihan — **cuma Enterprise Agency dengan perwakilan TikTok khusus yang bisa mengajukan.** Toko gak bisa daftar sendiri, seberapa besar pun belanja iklannya. Yang agency lakuin: nominasi, submit allowlist, bikin Shell BC, dan share aksesnya ke brand.

**Kapan ini gak relevan:** ambang belanjanya **$3.000/bulan** (sumber patok dalam USD). Di bawah itu, TTMS bukan pilihan yang tertunda, tapi pilihan yang belum ada. Buat toko yang belanja iklannya di bawah angka itu, seluruh entry ini informasi tentang apa yang ada di tahap lanjut — bukan sesuatu yang bisa dikejar sekarang. Yang ngangkat toko sampai ke ambang itu tiga hal dasar di `tts-segmentasi-003`, dan tiga-tiganya dikerjain sendiri.

## Batasan

Semua angka di entry ini jenis yang paling cepat geser: ambang belanja, waktu proses, tanggal nominasi. Sumbernya Januari 2026, enam bulan sebelum sekarang. Lihat `D-OUTDATED-03`.

Sumber mematok ambang dalam **USD** ($3.000). Konversi rupiah sengaja gak ditulis karena gerak sama kurs dan gampang jadi angka presisi palsu (`K1-D-OUTDATED-03`, opsi C).
