---
id: tts-gmvmax-003
title: Baca status video di GMV Max dan apa tindakannya
platform: tiktok-shop
kategori: iklan/gmv-max
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: 2025-10
sources:
  - file: Library_Tiktok.md
    bagian: "§Creative practices for each video status — tabel 9 status"
related: [tts-gmvmax-001, tts-gmvmax-004, tts-gmvmax-006, tts-konten-001, tts-metrik-007]
decisions: [K1-D-OUTDATED-02]
---

# Baca status video di GMV Max dan apa tindakannya

> 📌 **Dibuka (K1-D-OUTDATED-02, opsi B).** Logika sistemnya yang dipakai: sistem cuma
> alokasiin porsi kecil budget buat nyoba kreatif baru — itu desain fundamental, bukan setelan.
> **Nama status memang bergerak** (mis. "Unselected" sudah dilebur ke "Excluded"), jadi
> cocokin ke label yang muncul di Seller Center; jangan hafalin daftarnya mentah-mentah.

## Ringkasan

Sembilan status, tapi yang perlu diinget cuma **logikanya**: sistem cuma alokasiin porsi kecil budget buat nyoba kreatif baru, dan video "lulus" kalau dia belanja di atas **$1 dalam 3 hari** dalam target ROI. Dari situ semua status lain bisa diturunkan. Dan satu hal penting yang sering bikin panik: **wajar kalau mayoritas video statusnya Not delivering.**

## Kapan ini dipakai

Dipakai waktu member ngeluh videonya "gak jalan" di GMV Max, dan waktu mau tahu video mana yang perlu diperbaiki vs mana yang perlu didorong.

## Isi

**Logika intinya, dan ini yang paling penting:**
- Sistem **prioritasin ROI kampanye**, jadi cuma sebagian kecil budget yang dialokasiin buat eksplorasi kreatif baru
- Video pindah ke **Delivering** kalau dia belanja **> $1 dalam 3 hari terakhir** dalam target ROI
- Video pindah ke **Not delivering** kalau dia **gak bisa** belanja $1 dalam 3 hari dalam target ROI

Jadi semua status itu turunan dari satu mekanisme: **bisa nggak video ini belanja dalam target ROI.**

**Sembilan status dan tindakannya:**

| Status | Artinya | Tindakan |
|---|---|---|
| 😴 **Not active** | Diupload > 30 hari lalu dan **nol pendapatan** 30 hari terakhir. Sistem nurunin prioritasnya | Upload kreatif baru dengan visual/pesan yang di-refresh. Cek performa kreatif serupa buat tahu polanya |
| ⏳ **In queue** | Belum pernah dipakai iklan, masih nunggu dieksplorasi | Pakai **Creative Boost** buat video potensi tinggi — terutama yang gross revenue organiknya kuat. Atau nyalain toggle percepatan tes kreatif baru |
| 🔍 **Learning** | Udah bikin iklan, sedang fase tes awal (± 3 hari) | **Tunggu.** Jangan hapus atau edit video selama fase ini — bikin hasil tesnya gak stabil |
| 🚀 **Delivering** | Lulus fase learning, ditayangin dalam skala | Analisis video Delivering yang gross revenue-nya kuat, **produksi lebih banyak yang mirip**. Jangan di-boost kecuali tujuannya impresi |
| 🛑 **Not delivering** | Gak bisa belanja $1 dalam 3 hari dalam target ROI | Produksi lebih banyak video mirip yang Delivering. Refresh kreatif terus buat lawan fatigue. Pakai Creative Boost buat tes ulang yang potensinya tinggi |
| 🚫 **Excluded** | Dikeluarin manual dari kampanye | Review berkala — bisa relevan lagi kalau kondisi kampanye atau produk berubah. **Hindari bulk exclusion** kecuali benar-benar perlu |
| ⚠️ **Unavailable** | Ada masalah di video, link produk, akun TikTok, atau di luar masa otorisasi | Hover tooltip status buat lihat alasan spesifik, lalu benerin. Ada jeda ± 20 menit setelah diperbaiki |
| ❌ **Rejected** | Ditolak tim moderasi karena pelanggaran kebijakan iklan | Baca alasan penolakan, perbaiki kreatif. Bisa ajukan **Appeal**. Jangan pakai ulang format yang pernah ditolak |
| 🗂️ **Unselected** | **[Deprecated]** — udah dilebur ke Excluded | — |

**Penyebab Unavailable yang paling sering** (dari daftar panjang di sumber) — berguna karena ini yang paling gampang dibenerin:
- Otorisasi iklan kreator dimatiin atau kedaluwarsa
- Toggle affiliate posts dimatiin di kampanye
- Link produk gak tersedia, ditolak, delisted, atau stok habis
- Kreator ngubah akunnya jadi private
- Kode otorisasi video kedaluwarsa
- Video punya link produk dari beberapa toko berbeda

Satu catatan penting dari sumber: kalau masalahnya di **link produk** (ditolak, delisted, stok habis), itu masalah di sisi TikTok Shop — jadi ceknya di Seller Center, bukan ke tim ads.

**Untuk Rejected**, alasannya ngacu ke kebijakan iklan TikTok — lihat `tts-kebijakan-iklan-003` buat empat kategori penyebab penolakan.

## Angka & patokan

| Patokan | Nilai | Sumber |
|---|---|---|
| Ambang video masuk Delivering | Belanja > $1 dalam 3 hari, dalam target ROI | Library_Tiktok §video status |
| Durasi fase Learning | ± 3 hari | idem |
| Ambang Not active | > 30 hari sejak upload, nol pendapatan 30 hari | idem |
| Jeda update status setelah fix Unavailable | ± 20 menit | idem |

## Yang bikin gagal

**Panik karena banyak video Not delivering.** Sumbernya nyatain terang-terangan: GMV Max ngambil **semua** video yang tersedia, termasuk yang diposting setahun lalu, jadi kolamnya besar dan tingkat pemakaian kreatifnya rendah — dan **metrik itu gak bermakna**. Yang perlu diliat: insight dari video Delivering.

**Ngedit atau hapus video yang sedang Learning.** Bikin hasil tesnya gak stabil. Tunggu.

**Boost video yang udah Delivering.** Sumbernya bilang ini sering **nurunin ROI kampanye**, kecuali tujuannya impresi atau pre-heating afiliasi.

**Bulk exclusion.** Disebut dua kali di sumber sebagai hal yang dihindari.

**Nyari bantuan ke tim ads buat masalah link produk.** Itu sisi TikTok Shop. Cek Seller Center.

## Pertanyaan diagnosa

1. **Berapa video yang statusnya Delivering?** Ini angka yang penting, bukan berapa yang Not delivering.
2. **Ada video Unavailable? Tooltip-nya bilang apa?** Ini yang paling cepat dibenerin.
3. **Video yang Delivering itu polanya apa — siapa yang bikin, formatnya apa?** Jawaban ini yang nentuin video berikutnya diproduksi kayak apa.
4. **Ada video yang statusnya Learning dan barusan diedit?** Kalau iya, itu sebabnya hasilnya gak stabil.

## Batasan

Daftar status ini **udah kebukti bergerak** dalam dokumennya sendiri. Nama status, jumlahnya, dan ambang $1/3 hari semuanya bisa udah beda per Juli 2026.

Sumbernya juga nyebut dua fitur yang **belum ada waktu dokumen dibuat**: performance reporting buat Creative Boost, dan metrik Video Gross Revenue. Kalau dua itu udah rilis, cara evaluasi di `tts-gmvmax-004` perlu diperbarui.
