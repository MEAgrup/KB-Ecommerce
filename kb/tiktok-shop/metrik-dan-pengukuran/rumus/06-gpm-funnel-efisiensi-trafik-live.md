---
id: tts-metrik-006
title: Rumus GPM dan funnel efisiensi trafik live
platform: tiktok-shop
kategori: metrik-dan-pengukuran/rumus
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: tinggi
sensitif_waktu: false
valid_as_of: 2026-07
sources:
  - file: canva/live-stream-traffic-efficiency-ID.md
    bagian: "slide 5–9 — perjalanan pembeli, 4 indikator kunci, rumus GPM, contoh Creator A vs B"
related: [tts-metrik-001, tts-metrik-004, tts-metrik-005, tts-live-003, tts-live-017, tts-live-019]
decisions: [M-D-MERGE-04]
---

# Rumus GPM dan funnel efisiensi trafik live

## Ringkasan
GPM (Gross per Mille — penjualan per 1.000 tayangan) itu ukuran efisiensi live yang paling
dipakai TikTok buat nentuin apakah live lu layak dikasih trafik lebih. GPM bukan angka tunggal:
dia hasil kali empat rate sepanjang perjalanan pembeli. Naikin salah satu rate = naikin GPM =
dapat trafik lebih. **Makin tinggi angkanya, makin besar peluang dapat trafik positif ke live.**

## Kapan ini dipakai
Waktu member nanya "kenapa live gw sepi/gak dikasih trafik", atau mau tahu metrik mana yang
harus dinaikin duluan. Pakai bareng entry taktiknya (`tts-live-019`).

## Perjalanan pembeli (funnel live)
Urutan orang dari scroll sampai bayar:
scroll TikTok → lihat preview live → masuk live → nonton → klik produk → klik keranjang kuning →
menempatkan pesanan → bayar → terima + after-sale. Tiap loncatan antar-tahap punya rate-nya
sendiri — itu yang diukur di bawah.

## Empat indikator kunci
1. **Enter Room Rate (ERR)** — rasio orang yang masuk live dari yang lihat preview.
2. **Click Through Rate (CTR)** — rasio yang klik produk dari yang nonton.
3. **Click to Order (C_O)** — rasio yang menempatkan pesanan dari yang klik produk.
4. **Average Order Value (AOV)** — nilai rata-rata per pesanan.

Prinsip loop: **lebih banyak pembelian menarik lebih banyak penonton, lebih banyak penonton
menarik lebih banyak pembelian.**

## Rumus
```
GPM = ERR × CTR × C_O × AOV × 1000
```
GPM = efisiensi trafik. Ini melengkapi rumus GMV di `tts-metrik-001` (GMV = PV × GPM ÷ 1000):
di sana GPM dipakai jadi input; di sini GPM dibongkar jadi empat rate yang bisa digarap satu-satu.

## Angka & patokan (contoh dari sumber)
Kenapa GPM > jumlah tayangan (PV):

| | PV | GPM | ERR | CTR | C_O | AOV | Sales |
|---|---|---|---|---|---|---|---|
| Creator A | 61.015.703 | 1,25 | 0,04 | 0,61 | 0,014 | 3,19 | 76.265 |
| Creator B | 31.555.076 | 6,66 | 0,09 | 0,13 | 0,005 | 9,49 | 210.190 |

Creator B cuma punya ½ PV Creator A, tapi karena GPM-nya jauh lebih tinggi, B menerima komisi/
penjualan ~3× lebih besar. **Artinya: kejar GPM, bukan sekadar jumlah penonton.**

## Pertanyaan diagnosa
1. Dari empat rate, mana yang paling rendah dibanding patokan? Itu yang digarap duluan.
2. PV besar tapi Sales kecil? Berarti GPM rendah — cek ERR/CTR/C_O/AOV mana yang bocor
   (pakai `tts-live-003` atau `tts-live-017`).
