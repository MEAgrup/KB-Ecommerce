---
id: tts-afiliasi-004
title: Lacak komisi kreator dan biaya iklan afiliasi
platform: tiktok-shop
kategori: afiliasi
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: 2025-07
sources:
  - file: knowledge_base_basic_seller.txt
    bagian: "Artikel Terkait 1F — Mengatur GMV Max untuk Konten Afiliasi (2025-07-03)"
related: [tts-afiliasi-001, tts-gmvmax-007, tts-gmvmax-002]
decisions: []
---

# Lacak komisi kreator dan biaya iklan afiliasi

## Ringkasan

Dua biaya di tempat berbeda: **ad spend** di akun Ads, **komisi kreator** di Affiliate Center. Dan ada satu hal yang paling sering bikin salah hitung margin: **rate komisi kreator beda tergantung traffic-nya organik atau dari iklan** — traffic organik dapat *standard commission*, traffic iklan dapat *Shop Ads commission*.

## Kapan ini dipakai

Dipakai waktu member ngitung margin dari penjualan afiliasi, dan waktu bingung kenapa komisi yang keluar gak sesuai rate yang dia setel.

## Isi

**Di mana lihat biayanya:**

| Biaya | Tempatnya |
|---|---|
**Ad spend** | Akun Ads |
**Komisi ke kreator** | `Affiliate Center > Analytics > Creator` |

**Dua rate komisi, tergantung sumber traffic:**

| Sumber traffic | Kreator dapat |
|---|---|
Traffic **organik** | **Standard commission** |
Traffic **ads** | **Shop Ads commission** |

Ini yang bikin hitungan margin sering keliru: satu produk dengan satu kreator bisa ngasilin dua rate komisi berbeda dalam periode yang sama, tergantung penjualannya datang dari video organik kreator atau dari video yang diiklanin.

Sumbernya gak nyebut mana yang lebih tinggi, jadi jangan diasumsi.

**Kalau GMV Max Net Sales nyala**, ada lapis ketiga: pesanan yang selesai dari video afiliasi juga kena **biaya iklan GMV Max per pesanan selesai** (`tts-gmvmax-007`). Jadi total biaya per pesanan afiliasi bisa terdiri dari:
1. Komisi kreator (standard atau Shop Ads rate)
2. Biaya iklan GMV Max
3. Biaya platform lain yang berlaku

**Setup GMV Max buat konten afiliasi** — empat catatan dari sumber:
- Saat ini **cuma beberapa seller** yang punya akses buat setup GMV Max buat konten afiliasi
- GMV Max di Open Collaboration **cuma eligible buat produk yang belum diiklankan**
- Bisa diatur buat produk yang udah ada di Open Collaboration maupun yang belum
- Buat ROI beda per produk: edit satu per satu. Buat ROI sama di banyak produk: aktifkan **secara bulk**

Catatan pertama itu jenis batasan akses yang sama dengan "penjual terpilih" di `tts-gmvmax-007` — sumbernya gak jelasin kriterianya.

## Yang bikin gagal

**Ngitung margin pakai satu rate komisi.** Ada dua rate, tergantung sumber traffic.

**Nyari komisi kreator di dashboard Ads.** Tempatnya di Affiliate Center > Analytics > Creator.

**Lupa biaya iklan di pesanan afiliasi.** Kalau GMV Max nyala, itu lapis biaya tambahan.

**Nyalain GMV Max buat produk yang udah diiklankan di Open Collaboration.** Cuma eligible buat produk yang belum diiklankan.

## Pertanyaan diagnosa

1. **Penjualan afiliasi ini datang dari video organik atau video yang diiklanin?** Nentuin rate komisinya.
2. **Member udah cek dua tempat — Ads dan Affiliate Center?**
3. **GMV Max nyala di produk afiliasi?** Kalau iya, ada biaya per pesanan selesai.
4. **Ada akses setup GMV Max buat konten afiliasi?** Cuma sebagian seller.

## Batasan

Sumbernya **Juli 2025** — setahun sebelum sekarang, dan sebelum GMV Max Net Sales muncul. Jadi bagian setup-nya mungkin udah beda.

Yang gak ada di materi dan paling wajar ditanya: **berapa selisih standard commission dan Shop Ads commission.** Tanpa itu, member gak bisa ngitung margin dengan pasti. Kalau ada yang nanya, arahin ke Affiliate Center buat lihat angka aktualnya, jangan diperkirakan.
