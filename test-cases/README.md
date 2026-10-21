# Test Cases & Scenarios

| Test Case ID | Modul | Test Scenario | Test Steps | Expected Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC_RMA_01** | Customer | Verifikasi pembuatan tiket RMA baru | 1. Login Dashboard Customer<br>2. Klik Buat Tiket<br>3. Masukkan Serial Number & Deskripsi<br>4. Submit | Tiket berhasil dibuat dan masuk ke antrean Admin. | **Passed** |
| **TC_RMA_02** | Admin / Odoo | Verifikasi perubahan Fulfillment Status | 1. Buka Odoo RMA Module<br>2. Pilih tiket customer<br>3. Ubah status jadi 'Replace'<br>4. Save | Status terupdate dan meneruskan tugas ke Purchasing Manager. | **Passed** |
| **TC_AUTH_01** | Login | Verifikasi login dengan kredensial valid | 1. Buka halaman login<br>2. Masukkan email & password valid<br>3. Klik Login | User berhasil masuk ke Dashboard dan token session tersimpan. | **Passed** |
| **TC_TRANS_01**| Transaksi | Validasi input nominal cicilan kavling | 1. Buka menu Transaksi<br>2. Pilih ID Customer & masukkan nominal<br>3. Klik Simpan | Data cicilan tersimpan di database dan saldo piutang ter-update. | **Passed** |
