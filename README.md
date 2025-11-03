<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>


# 🚗 RentLy - Sistem Rental Kendaraan

Website rental kendaraan berbasis Laravel 10.49.1 dengan fitur lengkap untuk user dan admin.

## 📋 Fitur

### User
- Landing page dengan hero section
- Daftar kendaraan dengan filter & search
- Detail kendaraan dengan badge trusted
- Form pemesanan dengan perhitungan otomatis
- Dashboard riwayat pemesanan
- Login & Register

### Admin
- Dashboard dengan statistik
- CRUD Kendaraan lengkap
- Kelola pemesanan (approve/reject/complete)
- Filter dan search

## 🛠️ Instalasi

### 1. Clone & Setup
```bash
composer install
cp .env.example .env
php artisan key:generate
```

### 2. Konfigurasi Database
Edit `.env`:
```
DB_DATABASE=rently
DB_USERNAME=root
DB_PASSWORD=
```

### 3. Migrasi & Seed
```bash
php artisan migrate
php artisan db:seed
php artisan storage:link
```

### 4. Jalankan Server
```bash
php artisan serve
```

Akses: `http://localhost:8000`

## 👤 Akun Default

**Admin:**
- Email: admin@rently.com
- Password: password

**User:**
- Email: user@rently.com
- Password: password

## 📁 Struktur File

```
app/
├── Http/
│   ├── Controllers/
│   │   ├── Admin/
│   │   │   ├── AdminController.php
│   │   │   ├── KendaraanAdminController.php
│   │   │   └── PemesananAdminController.php
│   │   ├── DashboardController.php
│   │   ├── KendaraanController.php
│   │   ├── LandingController.php
│   │   └── PemesananController.php
│   └── Middleware/
│       └── RoleMiddleware.php
├── Models/
│   ├── Kendaraan.php
│   ├── Pemesanan.php
│   └── User.php

resources/views/
├── layouts/app.blade.php
├── landing.blade.php
├── auth/
│   ├── login.blade.php
│   └── register.blade.php
├── kendaraan/
│   ├── index.blade.php
│   └── show.blade.php
├── pemesanan/
│   └── create.blade.php
├── dashboard/
│   └── user.blade.php
└── admin/
    ├── dashboard.blade.php
    ├── kendaraan/
    │   ├── index.blade.php
    │   ├── create.blade.php
    │   └── edit.blade.php
    └── pemesanan/
        ├── index.blade.php
        └── show.blade.php

public/
├── css/style.css
└── js/script.js
```

## 🎨 Teknologi

- **Backend:** Laravel 10.49.1, PHP 8
- **Database:** MySQL
- **Frontend:** HTML, CSS, JavaScript (Vanilla)
- **Design:** Modern, Responsive, Gradient



## 📧 Support

Email: info@rently.com

---

© 2024 RentLy. All rights reserved.
