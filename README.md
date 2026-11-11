# PUTRA PRO V21 — Android APK project

Project Android WebView yang membungkus website PUTRA PRO V21 menjadi aplikasi Android.
Ikon launcher memakai gambar Gojo / GG PUTRA yang dikirim di chat.

## Cara paling mudah build APK lewat GitHub
1. Buat repository GitHub baru atau buka repository milikmu.
2. Upload seluruh isi ZIP ini ke root repository (folder `.github` juga harus ikut).
3. Commit/push ke branch `main`.
4. Buka tab **Actions**. Jalankan workflow **Build PUTRA PRO V21 APK** atau tunggu otomatis.
5. Setelah selesai hijau, buka run workflow tersebut, scroll ke **Artifacts**.
6. Download `PUTRA-PRO-V21-debug-apk.zip`, ekstrak, lalu ambil `app-debug.apk`.
7. Install APK di Android. Jika diminta, izinkan instalasi dari sumber yang kamu pilih.

## Build lokal di AndroidIDE / Android Studio
- Buka folder project ini sebagai project Gradle.
- Gunakan JDK 17 dan Gradle 8.9, Android SDK Platform 35.
- Jalankan task `:app:assembleDebug`.
- APK debug ada di `app/build/outputs/apk/debug/app-debug.apk`.

## Detail
- Nama aplikasi: PUTRA PRO V21
- Package: `com.putra.pro`
- Minimum Android: 6.0 (API 23)
- Target SDK: 35
- Website dibundel di `app/src/main/assets/index.html`.
- Geolocation runtime permission ditangani untuk fitur GPS/kiblat.

## Catatan penting
- Ini project source siap build, bukan file APK yang sudah dikompilasi di sini. Lingkungan pembuatan ini tidak memiliki Android SDK / Gradle terpasang.
- Workflow GitHub Actions akan mengompilasi APK setelah project di-push.
- APK yang dihasilkan workflow adalah **debug APK**, cocok untuk uji coba. Untuk distribusi publik jangka panjang, buat release APK yang ditandatangani dengan keystore milikmu sendiri dan simpan keystore/password secara rahasia.
- Jangan menaruh API key rahasia di HTML atau repository publik.
