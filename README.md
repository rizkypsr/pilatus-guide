# Pilatus Guide

### Cara Menjalankan Server
Buka project **pilatus-server** kemudian buka terminal pada VSCode. Jalankan perintah berikut pada terminal.
```
php artisan serve --host=0.0.0.0
```
Buka lagi terminal di VSCode dengan cara klik pada ikon tambah dibagian sebelah kanan terminal.

![alt text](/img1.png)

Jalankan perintah berikut pada terminal
```
php artisan ngrok --port=8000
```
Untuk membuka halaman admin, buka url http://localhost:8000/admin

### Cara Menjalankan Aplikasi Mobile
Cari tahu IP Address yang digunakan dengan cara, buka CMD, jalankan perintah berikut
```
ipconfig
```
Buka project **pilatus**, kemudian cari file

*lib/common/constants.dart*
```dart
const baseUrlApi = 'http://GANTI_DENGAN_IP_ADDRESS:8000/api/v1';
const baseUrl = 'http://GANTI_DENGAN_IP_ADDRESS:8000';
```
Misal IP Address 192.168.1.1, sehingga menjadi
```dart
const baseUrlApi = 'http://192.168.1.1:8000/api/v1';
const baseUrl = 'http://192.168.1.1:8000';
```
Jika semua sudah, jalankan aplikasi
