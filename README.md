# Food-Delivery---FINAL-SOURCECODE-FIC18---MARET-2025
# Food Delivery Order & Live Tracking App  
Aplikasi pemesanan makanan dengan **Live Tracking** untuk **User, Resto, dan Driver**.  
Backend menggunakan **Laravel**, pembayaran terintegrasi dengan **Xendit Payment Gateway**.  

---

## 📌 Fitur Utama  
### User App (Customer)
- Registrasi & login dengan autentikasi aman.
- Cari restoran, pilih menu, lakukan pemesanan.
- Pembayaran online (Xendit: E-Wallet, VA, QRIS, kartu).
- Notifikasi status pesanan (diproses, diantar, selesai).
- Live tracking driver secara real-time.

### Resto App (Merchant)
- Registrasi & kelola profil restoran.
- Manajemen menu & stok.
- Penerimaan & konfirmasi order.
- Riwayat transaksi & laporan penjualan.

### Driver App (Courier)
- Registrasi & verifikasi driver.
- Daftar pesanan tersedia, terima/ambil order.
- Update status pengiriman.
- Live navigation & tracking GPS.
- Riwayat pengiriman & laporan pendapatan.

### Backend (Laravel)
- API RESTful untuk komunikasi aplikasi.
- Manajemen user, resto, driver, dan order.
- Integrasi **Xendit Payment Gateway**.
- Sistem notifikasi real-time (Laravel Echo / WebSocket).
- Dashboard admin untuk monitoring.

---

## 🛠️ Teknologi
- **Laravel 10** – Backend Framework
- **MySQL / PostgreSQL** – Database
- **Xendit API** – Payment Gateway
- **Pusher / Laravel Echo** – Real-time notification
- **Google Maps API / Mapbox** – Live Tracking
- **JWT / Laravel Sanctum** – Authentication

---

## ⚡ Instalasi Backend
1. Clone repository:
   ```git clone https://github.com/username/food-delivery-app.git```
   kemudian pindah directory   ```cd food-delivery-app```
2. Install Dependencies
   ```composer install```
3. Copy .env file dan sesuaikan konfigurasi
   ```cp .env.example .env```
4. Ubah konfigurasi berikut sesuai kebutuhan:
   ``` DB_CONNECTION=mysql
        DB_HOST=127.0.0.1
        DB_PORT=3306
        DB_DATABASE=food_delivery
        DB_USERNAME=root
        DB_PASSWORD=
   Xendit
   XENDIT_SECRET_KEY=your_xendit_secret_key```
5. Generate Key dan Migrate Database
``` php artisan key:generate```
```php artisan migrate --seed```
<br>

## 🚚 Flow Aplikasi
1. **User** melakukan pemesanan → memilih metode pembayaran melalui **Xendit**.  
2. **Restoran** menerima pesanan → memproses order.  
3. **Driver** menerima notifikasi → mengambil & mengantar pesanan.  
4. **User** dapat melihat **live tracking** posisi driver secara real-time.  
5. **Sistem** mencatat transaksi & memperbarui laporan secara otomatis.  

---

## ⚠️ Kendala (Challenges)
- **Integrasi Xendit Payment**: perlu sinkronisasi status pembayaran dengan status order.  
- **Live Tracking Driver**: butuh optimasi agar update lokasi real-time tetapi tetap hemat data & baterai.  
- **Notifikasi Real-Time**: menggunakan WebSocket / Laravel Echo, memerlukan server tambahan (Pusher atau Redis).  
- **Sinkronisasi Order**: memastikan status order konsisten antara **User – Resto – Driver**.  
- **Security**: menjaga keamanan data (token, informasi pembayaran, dan lokasi).  
- **Scalability**: aplikasi harus tetap ringan & cepat meskipun jumlah user dan transaksi meningkat.
  
Food Delivery role nya [ User, Resto, Driver ]
1. <img width="375" height="776" alt="Daftar Pesanan Status (Complete)-1" src="https://github.com/user-attachments/assets/cbbd925e-a287-4df4-9c8f-2f06e3baa2b4" />
2. <img width="375" height="812" alt="History -_ List History" src="https://github.com/user-attachments/assets/9548c761-c7b5-49f6-a248-602162624222" />
3. <img width="375" height="812" alt="Sign Up" src="https://github.com/user-attachments/assets/ecad39d8-9c42-45e8-ba48-07ef965ba95d" />
4. <img width="375" height="812" alt="Sign In" src="https://github.com/user-attachments/assets/ebc13c74-e537-457c-ad74-ba667999e559" />
5. <img width="375" height="812" alt="Payment-_ Payment Method" src="https://github.com/user-attachments/assets/d8dbf6a8-4163-4df7-aa98-7e7e14a76748" />
6. <img width="375" height="812" alt="Payment Status (Sukses)" src="https://github.com/user-attachments/assets/c5f0ac0f-c5fd-4c63-a6e0-0942e8b13235" />
7. <img width="375" height="812" alt="Take Delivery-_Delivery Order" src="https://github.com/user-attachments/assets/eac13785-cf85-45e9-a7fd-a3604481123a" />
8. <img width="375" height="812" alt="Order Status (waiting)" src="https://github.com/user-attachments/assets/a52c5082-319f-4b17-8b02-b6d220d09ea6" />
9. <img width="375" height="812" alt="Menu-_ Add  New Menu" src="https://github.com/user-attachments/assets/66de029e-f552-4773-ae11-a8bf6ddaceba" />
10. <img width="375" height="812" alt="Menu -_ Deleted Success" src="https://github.com/user-attachments/assets/8e70fae0-c6c7-4914-a80f-51fd6b91a238" />
11. <img width="375" height="812" alt="Lihat Pesanan -_ Order status" src="https://github.com/user-attachments/assets/b6ffb78d-f4e6-4573-b891-5c0874b8b72c" />
12. <img width="375" height="812" alt="Home-1" src="https://github.com/user-attachments/assets/0c90c181-105d-470d-8365-7e64ed728e32" />
13. <img width="375" height="812" alt="Home-_Selected address" src="https://github.com/user-attachments/assets/fad42de2-0c84-44ae-bf0b-866f20fb36c5" />
14. <img width="375" height="1062" alt="History -_ Processing Order" src="https://github.com/user-attachments/assets/d6e0997e-9dac-4b90-82eb-53d6e3507364" />
15. <img width="375" height="812" alt="Splashscreen" src="https://github.com/user-attachments/assets/9ac6a6bc-4ff9-4eca-b0b8-a1d22a08f584" />
