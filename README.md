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
Buka link **Web Interface** pada browser.

<img width="362" alt="img2" src="https://user-images.githubusercontent.com/44289663/178902024-a02d6613-0f25-48d3-bb50-c9c70b4d9fde.png">

Klik url yang sudah digenerate.

<img width="595" alt="img3" src="https://user-images.githubusercontent.com/44289663/178902079-26d6845d-9d4d-41ca-97c0-e262642bb933.png">

Klik **Visit Site**

<img width="979" alt="img4" src="https://user-images.githubusercontent.com/44289663/178902106-a3ec255a-fe32-4d12-9a0f-ac487860dd16.png">

Maka URL sudah dapat digunakan untuk Midtrans.

Buka website [midtrans](https://midtrans.com). Login menggunakan akun yang ada.
Ganti **Environment** menjadi Sandbox

<img width="251" alt="img5" src="https://user-images.githubusercontent.com/44289663/178901354-23540649-235f-42ec-be70-1b91a602d851.png">

Pergi ke *Settings - Configuration*. Ganti url sesuai url ngrok.
Misal url ngrok https://1481-202-67-35-11.ap.ngrok.io, maka menjadi https://1481-202-67-35-11.ap.ngrok.io/api/midtrans/callback

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
