# Contoh Laporan Bug (Bug Report) - Studi Kasus RMA

- **Bug ID:** RMA-BUG-01
- **Module:** Integrasi Odoo & Dashboard Customer
- **Severity / Priority:** Major / High
- **Environment:** Staging / Chrome v125 / Odoo Integration
- **Reporter:** Rochmat Wahyu (QA Engineer)

## 📝 Deskripsi Masalah
Status Fulfillment pada Dashboard Customer tidak sinkron secara *real-time* setelah diubah di Odoo oleh Admin. Customer harus melakukan *refresh* manual (`F5`) untuk melihat pembaruan status perbaikan perangkat.

## 🔄 Langkah Reproduksi (Steps to Reproduce)
1. Login ke **Dashboard Customer** (`https://trialrma.dwp.io`).
2. Buat tiket RMA baru dengan Serial Number `RD5S94611`.
3. Buka tab terpisah, login ke **Odoo RMA Module** sebagai Admin.
4. Ubah *Fulfillment Status* tiket tersebut menjadi `Replace`.
5. Kembali ke Dashboard Customer tanpa melakukan *refresh* halaman.

## ✅ Hasil yang Seharusnya (Expected Result)
Status pada Dashboard Customer harusnya berubah secara otomatis (*real-time update*).

## ❌ Hasil Aktual (Actual Result)
Status pada Dashboard Customer tetap tertulis status lama sebelum halaman di-refresh secara manual.
