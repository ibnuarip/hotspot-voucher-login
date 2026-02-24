# FORONG HOTSPOT — Login Page MikroTik

Halaman login custom untuk hotspot MikroTik **FORONG HOTSPOT**. Template ini berbasis [Hotspot6 by Laksamadi Guko](https://laksa19.github.io) dengan fitur login voucher, member, dan scan QR code.

## Fitur

- **Login Voucher** — Masukkan kode voucher dan langsung terkoneksi WiFi (password otomatis disamakan dengan username)
- **Login Member** — Login menggunakan username dan password terpisah
- **Scan QR Code** — Scan QR voucher menggunakan [MyQR Scanner](https://laksa19.github.io/myqr/) dari Laksa19, otomatis redirect dan login
- **Tabel Paket** — Menampilkan daftar paket internet beserta harga
- **Halaman Status** — Menampilkan info koneksi (IP, MAC, upload, download, sisa waktu/kuota)
- **Halaman Logout** — Menampilkan ringkasan pemakaian setelah logout

## Struktur File

| File            | Keterangan                                |
| --------------- | ----------------------------------------- |
| `login.html`    | Halaman utama login (voucher, member, QR) |
| `status.html`   | Halaman status koneksi user               |
| `logout.html`   | Halaman logout                            |
| `alogin.html`   | Redirect otomatis setelah login berhasil  |
| `success.html`  | Halaman konfirmasi berhasil terkoneksi    |
| `error.html`    | Halaman error                             |
| `redirect.html` | Halaman redirect                          |
| `rlogin.html`   | Halaman re-login                          |
| `radvert.html`  | Halaman advert/iklan                      |
| `style.css`     | Stylesheet tampilan                       |
| `errors.txt`    | Pesan error (Bahasa Indonesia)            |
| `errors-en.txt` | Pesan error (English)                     |
| `font/`         | Font icon custom                          |

## Cara Upload ke MikroTik

### 1. Persiapan

Pastikan semua file sudah diuji coba menggunakan Laragon di lokal.

### 2. Upload via Winbox

1. Buka **Winbox** dan login ke router MikroTik
2. Klik menu **Files** → masuk ke folder `hotspot`
3. Drag & drop semua file dari komputer ke jendela Files
4. Replace file lama jika diminta

### 3. Konfigurasi Walled Garden

Tambahkan `laksa19.github.io` di **Walled Garden** agar fitur scan QR bisa diakses sebelum login:

- IP → Hotspot → Walled Garden
- Tambahkan rule: `Dst. Host = laksa19.github.io`, Action = `allow`

### 4. Testing

1. **Login manual** — Konek ke WiFi hotspot, masukkan kode voucher, pastikan berhasil login
2. **Login member** — Klik tombol Member, masukkan username & password, pastikan berhasil login
3. **Scan QR** — Klik tombol QR Code, scan QR voucher dari kertas yang dicetak via Mikhmon, pastikan otomatis login

## Kredit

- Template Hotspot6 by [Laksamadi Guko](https://laksa19.github.io)
- QR Scanner: [MyQR by Laksa19](https://laksa19.github.io/myqr/)
- Manajemen Voucher: [Mikhmon](https://laksa19.github.io/?mikhmon/v3)
