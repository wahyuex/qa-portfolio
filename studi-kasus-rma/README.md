# Studi Kasus: UAT Sistem RMA (Return Merchandise Authorization) - DWP Group

## 1. Project Overview
- **Project Name:** RMA (Return Merchandise Authorization)
- **Client / Company:** PT Spectrum Indowibawa (DWP Group)
- **UAT Date:** 2 August 2024
- **Description:** Platform manajemen perbaikan dan garansi perangkat keras yang melibatkan 6 *role* pengguna dan integrasi dengan **Odoo ERP**.

## 2. Role & Responsibility Coverage
Pengujian dilakukan secara *end-to-end* mencakup 6 peran utama:
1. **Customer:** Registrasi, Login, Reset Password, Buat Tiket RMA, Edit Data Resi/Cargo, Rating.
2. **Admin (Dashboard & Odoo):** Verifikasi tiket masuk, ubah *Fulfillment Status* (OK, Replace, Unrepair), Validasi Delivery Order.
3. **Technician:** Terima Tiket, Tambah Solusi Perbaikan (*Service Monitoring*), Export *Service History*.
4. **Purchasing Manager:** Approval pergantian perangkat (*Verify Replace*) dan unit tidak dapat diperbaiki (*Verify Unrepair*).
5. **Technician Manager:** Approval tiket unrepair dari teknisi.
6. **Accounting:** Verifikasi bukti bayar atas penawaran service perangkat *Out of Warranty*.

## 3. Data Testing Validation Summary
- **Fulfillment Status: OK** (In Warranty / Out of Warranty - Perangkat berhasil diperbaiki).
- **Fulfillment Status: Replace** (Penggantian unit baru dengan pencatatan Serial Number pengganti).
- **Fulfillment Status: Unrepair** (Penanganan perangkat tidak bisa diperbaiki dengan status *Reject* / *Approve* oleh customer).
