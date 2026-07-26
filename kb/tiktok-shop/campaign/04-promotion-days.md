---
id: tts-campaign-004
title: Promotion Days — naikin budget otomatis di momen belanja
platform: tiktok-shop
kategori: campaign
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: tinggi
sensitif_waktu: true
valid_as_of: 2025-10
sources:
  - file: knowledge_base_basic_seller.txt
    bagian: "Artikel Terkait 1G — Hari Promosi pada GMV Max (2025-10-28)"
related: [tts-gmvmax-002, tts-gmvmax-005, tts-campaign-003, fnd-002]
decisions: []
---

# Promotion Days — naikin budget otomatis di momen belanja

## Ringkasan

Toggle di dalam campaign GMV Max yang otomatis **nurunin target ROI** dan **naikin budget** selama jendela momen belanja. Default: ROI turun **10%**, budget naik **50%**. Dan satu aturan yang nentuin berhasil atau nggak: **aktifkan 3–5 hari sebelum event**, biar sistem punya waktu belajar dulu.

## Kapan ini dipakai

Dipakai buat momen belanja — tanggal kembar, payday, mega sale. Kalender momennya di `fnd-002`.

**Kenapa ROI-nya diturunin, bukan dinaikin:** di momen ramai, kompetisi buat traffic naik, jadi biaya per konversi naik. Target ROI yang dipertahankan ketat bikin sistem nahan belanja justru waktu peluangnya paling besar. Nurunin target ROI = ngizinin sistem bayar lebih mahal buat traffic yang memang lebih mahal.

## Isi

**Lima langkah:**

1. **Aktifkan** — waktu bikin atau ngedit campaign GMV Max, toggle on **Promotion Days**
2. *(Opsional)* **Edit jadwal** — pakai kalender buat include/exclude event belanja preset, atau tambah tanggal sendiri
3. *(Opsional)* **Edit target ROI** — default pengurangan **10%**; bisa dipilih **20%** atau **30%**
4. *(Opsional)* **Edit budget** — default kenaikan **50%**
5. **Review status pelaporan**

**Tiga status:**

| Status | Artinya |
|---|---|
`Off` | Promotion Days gak diaktifkan |
`On / Active` | Campaign jalan pakai setelan Promotion Days |
`On / Inactive` | Diaktifkan tapi **di luar jendela promo** |

Status ketiga sering bikin bingung: kelihatan "On" tapi setelannya belum jalan karena tanggalnya belum masuk.

**Empat best practice dari sumber:**
- **Aktifkan lebih awal** — minimal **3–5 hari sebelum event**, biar sistem bisa belajar dan ngoptimasi dulu
- **Set target ROI realistis** — masukkan yang mencerminkan performa campaign sebenarnya, bukan yang lu harapkan
- **Pastikan budget cukup** — Promotion Days naikin budget otomatis (default +50%)
- **Refresh kreatif** — upload video atau aset live baru sebelum event

## Angka & patokan

| Setelan | Default | Opsi lain |
|---|---|---|
Pengurangan target ROI | **10%** | 20% atau 30% |
Kenaikan budget | **+50%** | — |
Kapan diaktifkan | **3–5 hari sebelum event** | — |

## Yang bikin gagal

**Nyalain di hari H.** Sistem butuh 3–5 hari buat belajar. Nyalain hari H artinya jendela promo dipakai buat fase belajar.

**Lupa dananya naik 50% otomatis.** Kalau saldo gak cukup, campaign berhenti di momen paling ramai.

**Bingung karena statusnya `On / Inactive`.** Itu normal di luar jendela promo.

**Refresh kreatif setelah event mulai.** Sumbernya bilang sebelum.

## Pertanyaan diagnosa

1. **Event-nya kapan, dan sekarang udah masuk H-3 sampai H-5?**
2. **Saldo cukup buat budget +50% selama jendela promo?**
3. **Pengurangan ROI-nya masih default 10% atau udah diubah?** Kalau diubah ke 30% tanpa alasan, itu perlu dicek.
4. **Ada video atau aset live baru yang diupload sebelum event?**

## Batasan

Sumbernya gak nyebut **kapan sebaiknya pakai 20% atau 30%** ketimbang default 10% — cuma nyebut opsinya ada. Jangan diturunkan sendiri; kalau member nanya, jawaban aman: mulai dari default.

Daftar "event belanja preset" di kalender juga gak dirinci di sumber.
