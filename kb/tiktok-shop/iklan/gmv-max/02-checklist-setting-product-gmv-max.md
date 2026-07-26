---
id: tts-gmvmax-002
title: Checklist setting Product GMV Max
platform: tiktok-shop
kategori: iklan/gmv-max
depth: 2
audience: member
aksi_oleh: member
status: canonical
confidence: sedang
sensitif_waktu: true
valid_as_of: 2026-01
sources:
  - file: Library_Tiktok.md
    bagian: "§Product GMV Max Campaign Setting Checklist"
related: [tts-gmvmax-001, tts-gmvmax-003, tts-gmvmax-007, tts-produk-001, tts-segmentasi-002, tts-metrik-007]
decisions: [K1-D-OUTDATED-02, K1-D-CONFLICT-03]
---

# Checklist setting Product GMV Max

> 📌 **Dibuka (K1-D-OUTDATED-02, opsi B).** Logika lima hal yang dicek tetap berlaku —
> itu desain sistem, bukan setelan. **Nama toggle & lokasinya bisa beda**: cek di
> **Seller Center → Dasbor iklan → GMV Max** (lihat `tts-metrik-007` buat peta menu).
> Penagihan prabayar/pascabayar: seller bebas pilih (`K1-D-CONFLICT-03`).

## Ringkasan

Lima hal yang dicek, dan satu di antaranya punya aturan angka yang jelas: **kalau ROI achievement rate lu di bawah 90%, turunin setelan ROI-nya.** Empat lainnya cek biner — nyala/mati, ada/nggak.

## Kapan ini dipakai

Dipakai waktu audit kampanye yang udah jalan, dan waktu bikin kampanye baru. Lima poin ini urutan yang dipakai playbook agency buat ngecek toko klien.

## Isi

**1. Tanggal kampanye** — cek apakah Product GMV Max **always on**.
Bukan dinyalain waktu mau kampanye. Nyala terus.

**2. Produk** — cek apakah kampanyenya **dipisah berdasarkan siklus hidup produk atau produk dengan ROI mirip**.
Ini poin yang paling sering dilewat. Alasannya: kalau produk Hero dan produk baru digabung satu kampanye, sistem ngoptimasi ke rata-ratanya. Yang kuat kurang didorong, yang baru kurang dites. Nyambung ke aturan di `tts-produk-001`: bundling Hero SKU dan Growing SKU **di kampanye yang beda**.

**3. Setelan ROI** — cek apakah ngikutin ROI yang direkomendasikan sistem.
Dan ini aturan angkanya: **kalau ROI rekomendasi keliatan terlalu rendah**, cek ROI aktual sebelumnya dan **ROI achievement rate**-nya. Kalau achievement rate **di bawah 90%**, sangat disarankan **turunin** setelan ROI.

Logikanya berlawanan dari insting: kalau lu gak nyampe target ROI, jangan naikin targetnya — turunin. Target ROI yang terlalu tinggi bikin sistem nahan pengeluaran, dan kampanye yang gak belanja gak dapat data buat belajar.

**4. Best practice kreatif** — tiga hal yang harus nyala:
- **Auto select** nyala
- **Enable affiliate creatives** nyala
- **Otorisasi** kelar

Tiga-tiganya nambah jumlah kreatif yang bisa dipakai sistem. Ini bahan bakarnya (`tts-gmvmax-001`).

**5. Budget** — cek dua hal:
- Ngikutin rekomendasi budget harian, atau budget-nya cukup
- **Saldo akun cukup**

Yang kedua kedengeran remeh tapi disebut eksplisit di checklist agency — kampanye yang berhenti karena saldo habis itu penyebab yang paling gak perlu.

> ⚠️ **Baris saldo ini cuma berlaku buat varian prabayar.** Ada varian ketiga —
> **GMV Max Net Sales Optimization** (Jun 2026) — yang **gak butuh saldo awal sama
> sekali**; biayanya ditagih setelah pesanan selesai. Kalau member pakai varian itu,
> jangan suruh dia top up. Cek `tts-gmvmax-007` dan `D-CONFLICT-03` dulu sebelum
> ngomongin saldo.

## Angka & patokan

| Patokan | Nilai | Sumber |
|---|---|---|
| Ambang ROI achievement rate | Di bawah 90% → turunin setelan ROI | Library_Tiktok §Campaign Setting Checklist |
| Status kampanye Product GMV Max | Always on | idem |

## Yang bikin gagal

**Naikin target ROI waktu hasilnya kurang.** Kebalikan dari yang disaranin. Di bawah 90% achievement → turunin.

**Satu kampanye buat semua produk.** Sistem ngoptimasi ke rata-rata.

**Matiin affiliate creatives.** Itu ngurangin kolam kreatif yang bisa dipakai sistem, dan di data benchmark, kreatif dari kreator afiliasi nyumbang mayoritas GMV (`tts-konten-002`).

**Nyalain kampanye cuma waktu momen kampanye.** Always on.

## Pertanyaan diagnosa

1. **ROI achievement rate-nya berapa?** Ini satu angka yang nentuin setelan ROI-nya perlu diturunin atau nggak.
2. **Kampanyenya kepisah per siklus hidup produk?** Cek, jangan diasumsi.
3. **Tiga toggle kreatif nyala — auto select, affiliate creatives, otorisasi kelar?** Sering satu ketinggalan.
4. **Saldo akun cukup buat budget harian sampai akhir bulan?**

## Batasan

Nama setelan (Auto select, Enable affiliate creatives) dan lokasinya di TTAM belum diverifikasi per Juli 2026. Ambang 90% juga angka operasional internal yang bisa direvisi.

Sumbernya nampilin sebagian checklist ini dalam bentuk screenshot yang gak bisa diekstrak, jadi ada kemungkinan ada poin yang gak ketangkep di entry ini.
