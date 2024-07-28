# Aplikasi Web Sistem Absensi Sekolah Berbasis QR Code

[![Continuous Integration](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/actions/workflows/ci.yml/badge.svg)](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/actions/workflows/ci.yml)
![GitHub Repo stars](https://img.shields.io/github/stars/ikhsan3adi/absensi-sekolah-qr-code?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/ikhsan3adi/absensi-sekolah-qr-code?style=social)
![GitHub forks](https://img.shields.io/github/forks/ikhsan3adi/absensi-sekolah-qr-code?style=social)
![GitHub all releases](https://img.shields.io/github/downloads/ikhsan3adi/absensi-sekolah-qr-code/total?style=social)

![Preview](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/hero.png)

Aplikasi Web Sistem Absensi Sekolah Berbasis QR Code adalah sebuah proyek yang bertujuan untuk mengotomatisasi proses absensi di lingkungan sekolah menggunakan teknologi QR code. Aplikasi ini dikembangkan dengan menggunakan framework CodeIgniter 4 dan didesain untuk mempermudah pengelolaan dan pencatatan kehadiran siswa dan guru.

## Fitur Utama

- **QR Code scanner.** Setiap siswa/guru menunjukkan qr code kepada perangkat yang dilengkapi dengan kamera. Aplikasi akan memvalidasi QR code dan mencatat kehadiran siswa ke dalam database.
- **Login petugas.**
- **Dashboard petugas.** Petugas sekolah dapat dengan mudah memantau kehadiran siswa dalam periode waktu tertentu melalui tampilan yang disediakan.
- **QR Code generator.** Petugas yang sudah login akan men-generate qr code setiap siswa/guru secara otomatis. Setiap siswa akan diberikan QR code unik yang terkait dengan identitas siswa. QR code ini akan digunakan saat proses absensi.
- **Ubah data absen siswa/guru.** Petugas dapat mengubah data absensi setiap siswa/guru. Misalnya mengubah data kehadiran dari `tanpa keterangan` menjadi `sakit` atau `izin`.
- **Tambah, Ubah, Hapus(CRUD) data siswa/guru.**
- **Tambah, Ubah, Hapus(CRUD) data kelas.**
- **Lihat, Tambah, Ubah, Hapus(CRUD) data petugas.** (khusus petugas yang login sebagai **`superadmin`**).
- **Generate Laporan.** Generate laporan dalam bentuk pdf.

> [!NOTE]
>
> ## Framework dan Library Yang Digunakan
>
> - CodeIgniter 4
> - [Material Dashboard Bootstrap 4](https://www.creative-tim.com/product/material-dashboard-bs4)
> - [Myth Auth Library](https://github.com/lonnieezell/myth-auth)
> - [Endroid QR Code Generator](https://github.com/endroid/qr-code)
> - [ZXing JS QR Code Scanner](https://github.com/zxing-js/library)

## Screenshots

### Tampilan Halaman QR Scanner

![QR Scanner view](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_5_2023_204644.jpeg)

### Tampilan Absen Masuk dan Pulang

![QR Scanner absen](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/absen.jpg)

### Tampilan Login Petugas

![Login](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_4_2023_20573.jpeg)

### Tampilan Dashboard Petugas

![Dashboard](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/dashboard.png)

### Tampilan CRUD Data Absen

| Siswa (Dengan Data Kelas)                                                                                                   |                                                           Guru                                                           |
| --------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------: |
| ![CRUD Absen Siswa](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_11_2023_205146.jpeg) | ![CRUD Absen Guru](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_2_2023_20525.jpeg) |

### Tampilan Ubah Data Kehadiran

![Kehadiran](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_17_2023_205557.jpeg)

### Tampilan CRUD Data Siswa & Guru

| Siswa                                                                                                                      |                                                           Guru                                                            |
| -------------------------------------------------------------------------------------------------------------------------- | :-----------------------------------------------------------------------------------------------------------------------: |
| ![CRUD Data Siswa](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_12_2023_205221.jpeg) | ![CRUD Data Guru](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_14_2023_205256.jpeg) |

### Tampilan CRUD Data Kelas & Jurusan

![CRUD Data Siswa](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/kelas-jurusan.png)

### Tampilan Generate QR Code dan Generate Laporan

| Generate QR                                                                                                          |                                                      Generate Laporan                                                       |
| -------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------: |
| ![Generate QR](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_3_2023_20539.jpeg) | ![Generate Laporan](https://github.com/ikhsan3adi/absensi-sekolah-qr-code/raw/master/screenshots/image_15_2023_205322.jpeg) |

## Cara Penggunaan

### Persyaratan

- [Composer](https://getcomposer.org/).
- PHP 8.1+ dan MySQL/MariaDB atau [XAMPP](https://www.apachefriends.org/download.html) versi 8.1+ dengan mengaktifkan extension `intl` dan `gd`.
- Pastikan perangkat memiliki kamera/webcam untuk menjalankan qr scanner. Bisa juga menggunakan kamera HP dengan bantuan software DroidCam.

### Instalasi

- Unduh dan impor kode proyek ini ke dalam direktori proyek anda (htdocs).

> [!CAUTION]
>
> - Install dependencies yang diperlukan dengan cara menjalankan perintah berikut di terminal:
>
> ```shell
> composer install
> ```
>
> - Jika belum terdapat file `.env`, rename file `.env.example` menjadi `.env`

- (Opsional) Konfigurasi file `.env` untuk mengatur base url(terutama jika melakukan hosting), koneksi database dan pengaturan lainnya sesuai dengan lingkungan pengembangan Anda.
- (Opsional) Ganti/replace logo sekolah di `public/assets/img/logo_sekolah.jpg`.
- (Opsional) Ganti nama sekolah di `app/Config/AbsensiSekolah.php`.

> [!WARNING]
>
> - Buat database `db_absensi`(sesuaikan dengan yang terdapat di `.env`) di phpMyAdmin / mysql
>
> - Jalankan migrasi database untuk membuat struktur tabel yang diperlukan. Ketikkan perintah berikut di terminal:
>
> ```shell
> php spark migrate --all
> ```

> [!IMPORTANT]
>
> - Jalankan web server (contoh Apache, XAMPP, etc)
> - Atau gunakan `php spark serve` (atur baseURL di `.env` menjadi `http://localhost:8080/` terlebih dahulu).
> - Lalu jalankan aplikasi di browser.
> - Login menggunakan krendensial superadmin:
>
> ```txt
> username : superadmin
> password : superadmin
> ```

> [!TIP]
>
> Jika ingin mengubah email, username & password dari superadmin, buka file `app\Database\Migrations\2023-08-18-000004_AddSuperadmin.php` lalu ubah & sesuaikan kode berikut:
>
> ```php
> // INSERT INITIAL SUPERADMIN
> $email = 'adminsuper@gmail.com';
> $username = 'superadmin';
> $password = 'superadmin';
> ```

- Izinkan akses kamera.

### Konfigurasi

**Nama Sekolah**

Untuk mengubah identitas nama sekolah, buka file konfigurasi `app/Config/AbsensiSekolah.php` dan ubah pada:

```php
public string $namaSekolah = 'SMKN 4 KENDARI';
```

## Kesimpulan

Dengan aplikasi web sistem absensi sekolah berbasis QR code ini, diharapkan proses absensi di sekolah menjadi lebih efisien dan terotomatisasi. Proyek ini dapat diadaptasi dan dikembangkan lebih lanjut sesuai dengan kebutuhan dan persyaratan sekolah Anda.

