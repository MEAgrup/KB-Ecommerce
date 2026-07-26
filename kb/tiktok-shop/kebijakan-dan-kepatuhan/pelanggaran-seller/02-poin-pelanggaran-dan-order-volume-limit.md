---
id: tts-pelanggaran-seller-002
title: Poin Pelanggaran Seller dan Order Volume Limit
platform: tiktok-shop
kategori: kebijakan-dan-kepatuhan/pelanggaran-seller
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: tidak-diketahui
sources:
  - file: Pedoman_Konten_TikTok.md
    bagian: "§Catatan Penting (pembuka) — Poin Pelanggaran Seller"
  - file: Pedoman_Konten_TikTok.md
    bagian: "§Pelanggaran Seller: Pemenuhan Pesanan (Fulfillment) — metrik inti"
related: [tts-pelanggaran-seller-001, tts-pelanggaran-konten-001, tts-segmentasi-005]
decisions: [K1-D-OUTDATED-04]
---

# Poin Pelanggaran Seller dan Order Volume Limit

> 📌 **Di-unblock (K1-D-OUTDATED-04, opsi C):** bagian actionable dibuka. Sistem poin (Rating Kinerja Penjual, default 200) + kategori pelanggaran ada di `tts-segmentasi-005`. Nama menu/UI cek Seller Center terkini.

> ⛔ **Entry ini `blocked` — jangan dikutip ke member.**
> Ini entry konsekuensi, dan sumbernya cuma nyebut mekanismenya tanpa satu angka pun:
> gak ada jumlah poin per jenis pelanggaran, gak ada ambang batas, gak ada masa berlaku
> poin, gak ada besaran pembatasan OVL. Nulis entry lengkap dari sini artinya ngarang
> angka. Lihat `D-OUTDATED-04`.

## Ringkasan

Dua mekanisme hukuman yang jalan bareng. **Poin Pelanggaran Seller** terakumulasi dari tiap pelanggaran, dan akumulasinya bisa berdampak serius ke kegiatan operasional toko. **Order Volume Limit (OVL)** = pembatasan jumlah pesanan, dikenakan kalau seller ngelanggar metrik inti fulfillment. Yang penting dipahamin: pelanggaran konten dan pelanggaran operasional **numpuk di kolam yang sama**.

## Isi

**Yang dinyatakan sumber, apa adanya:**

- Setiap pelanggaran **berkontribusi terhadap Poin Pelanggaran Seller**
- Akumulasi poin **bisa berdampak serius terhadap kegiatan operasional toko**
- Menjaga performa dan mematuhi kebijakan platform **sangat penting** buat mempertahankan hak istimewa dan kepercayaan pembeli
- Seller bisa kena **Poin Pelanggaran dan Order Volume Limit (OVL)** kalau ngelanggar metrik inti berikut:
  - **Tingkat Pengiriman Terlambat** (Late Dispatch Rate)
  - **Tingkat Pembatalan karena Kesalahan Penjual** (Seller Fault Cancellation Rate)

Itu seluruh yang ada di sumber. Tiga hal yang **gak ada** dan gak boleh diisi sendiri:
- Berapa poin per jenis pelanggaran
- Berapa ambang batas sebelum kena tindakan
- Berapa lama poin bertahan sebelum hangus

**Satu implikasi yang penting dan bisa dipakai sekarang:** karena semua pelanggaran nyumbang ke satu kolam poin yang sama, toko yang udah punya riwayat pelanggaran konten (klaim menyesatkan, redirection) punya ruang lebih sempit buat kesalahan operasional. Jadi buat member yang pernah kena teguran konten, urusan SLA jadi lebih genting — bukan urusan terpisah.

Ini juga yang bikin entry-entry `pelanggaran-konten` bukan cuma soal "video ditolak". Video ditolak itu gejalanya; poin yang numpuk itu risikonya.

## Yang bikin gagal

**Nganggep pelanggaran konten dan operasional dua dunia terpisah.** Sumbernya nulis "setiap pelanggaran berkontribusi" — satu kolam.

**Nganggep teguran ringan gak ada efek.** Efeknya akumulatif, dan yang kelihatan cuma waktu ambangnya kelewat.

## Pertanyaan diagnosa

1. **Toko ini pernah kena teguran sebelumnya, jenis apa aja?** Nentuin seberapa genting kesalahan berikutnya.
2. **Yang kena sekarang Late Dispatch Rate atau Seller Fault Cancellation Rate?** Dua metrik yang berbeda penanganannya.
3. **Ada notifikasi pembatasan pesanan (OVL) di Seller Center?** Kalau ada, ini bukan lagi peringatan.

## Batasan

Confidence-nya **rendah** dan itu jujur: sumbernya cuma nyebut mekanisme, nol angka. Entry ini sengaja dibiarin tipis daripada dilengkapi tebakan.

Yang dibutuhin buat naikin ini ke `canonical`: halaman kebijakan Poin Pelanggaran TikTok Shop Indonesia — jumlah poin per jenis pelanggaran, ambang batas tindakan, dan masa berlaku poin.
