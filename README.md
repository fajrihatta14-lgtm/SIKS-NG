# SIKS-NG UI

Implementasi HTML/CSS statis dari desain Figma "SIKS-NG" (alur login, verifikasi akun, lupa sandi, dan dasbor data DTKS).

## Struktur File

```
├── index.html        # Halaman login
├── verifikasi.html    # Halaman verifikasi akun (kode OTP)
├── lupa-sandi.html    # Halaman lupa kata sandi
├── dashboard.html     # Dasbor dengan sidebar, tabel data penerima manfaat
└── style.css          # Gaya bersama untuk index, verifikasi, dan lupa-sandi
```

`dashboard.html` menggunakan CSS-nya sendiri (inline `<style>`) karena tata letaknya berbeda (sidebar + tabel).

## Cara Menjalankan

Cukup buka `index.html` langsung di browser, atau gunakan GitHub Pages:

1. Push folder ini ke repository GitHub.
2. Masuk ke **Settings → Pages**.
3. Pilih branch `main` dan folder root (`/`), lalu simpan.
4. Situs akan tersedia di `https://<username>.github.io/<repo>/`.

## Alur Halaman

`index.html` (login) → `verifikasi.html` (jika akun baru) atau langsung → `dashboard.html`.
Tombol "Lupa kata sandi?" di halaman login mengarah ke `lupa-sandi.html`.

## Catatan

Semua proses submit form (login, OTP, reset sandi) masih berupa simulasi di sisi klien (JavaScript) — belum terhubung ke backend/API sungguhan. Ganti bagian tersebut dengan pemanggilan API asli sesuai kebutuhan.
