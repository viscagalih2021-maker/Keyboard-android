# Pusca Selling Keyboard (Android IME)

Keyboard jualan Pusca sebagai keyboard sistem Android. Setelah dipasang dan diaktifkan,
keyboard ini muncul di WhatsApp, Instagram, SMS, dan aplikasi lain. Menu Template, Produk,
Buat Order, Invoice, Cek Order, Keuangan, dan Pelanggan memakai data Pusca Store yang sama.

## Isi proyek

- MainActivity: layar pengaturan (alamat aplikasi, tombol login, aktifkan keyboard).
- WebLoginActivity: WebView untuk login sekali ke aplikasi Pusca.
- PuscaKeyboardService: InputMethodService yang menampilkan halaman /keyboard-native
  dan mengirim teks ke aplikasi tujuan.

## Cara build APK

### Opsi A - Android Studio (komputer sendiri)

1. Pasang Android Studio (gratis) di Windows/Mac.
2. Buka folder proyek ini (File > Open > pilih folder PuscaKeyboard).
3. Tunggu Gradle sync selesai.
4. Menu Build > Build Bundle(s) / APK(s) > Build APK(s).
5. APK ada di app/build/outputs/apk/debug/app-debug.apk.
6. Kirim APK ke HP (WhatsApp/Drive), buka, izinkan "install dari sumber tidak dikenal", lalu pasang.

### Opsi B - GitHub Actions (tanpa komputer)

1. Buat akun GitHub, buat repository baru, unggah seluruh isi folder ini.
2. Buka tab Actions, jalankan workflow "Build APK".
3. Setelah selesai, unduh artifact pusca-keyboard-apk, isinya app-debug.apk.
4. Pasang APK di HP seperti langkah di atas.

## Cara pakai di HP

1. Buka aplikasi Pusca Keyboard.
2. Ketuk "Buka aplikasi untuk login" lalu login dengan akun Pusca Store.
3. Ketuk "Aktifkan keyboard Pusca" (Pengaturan akan terbuka, aktifkan Pusca Selling Keyboard).
4. Ketuk "Pilih keyboard Pusca" lalu pilih "Pusca Selling Keyboard".
5. Buka WhatsApp, ketuk kolom pesan: keyboard jualan tampil.

## Catatan

- Keyboard membutuhkan internet karena datanya dari aplikasi Pusca.
- URL keyboard bisa diubah di layar pengaturan aplikasi (default halaman /keyboard-native).
- Proyek ini dibuat oleh Base44; Base44 tidak bisa membuat file APK, jadi APK dibangun
  dari proyek ini di Android Studio atau GitHub Actions.
