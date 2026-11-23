# Spotidown — Android

Aplikasi Android (Kotlin + Jetpack Compose) untuk mengunduh lagu Spotify sebagai MP3 lewat [spotidown.app](https://spotidown.app/). Versi mobile dari [ferrymehdi/spotidown](https://github.com/ferrymehdi/spotidown), berjalan mandiri di perangkat tanpa server pendamping.

## Unduh APK

Unduh berkas APK rilis terbaru langsung dari halaman **[Releases](https://github.com/ICR-1/spotidown/releases/latest)** (bagian kanan repositori ini).

- **Versi:** `1.0`
- **Minimum OS:** Android 10 (API 29) atau lebih baru

## Cara Kerja

Versi web/desktop asli memakai Puppeteer. Di Android peran itu dijalankan oleh **WebView 1×1 dp** yang memuat halaman `spotidown.app` lalu menjalankan skripnya secara same-origin:

```text
grecaptcha.execute() → POST /action → form per lagu (data/base/token)
                     → POST /action/track → https://rapid.spotidown.app/v2?token=…
                     → stream ke MediaStore Music/Spotidown
```

Parsing HTML dilakukan di dalam WebView dengan `DOMParser` (selektor semantik).

## Fitur

- Cari lagu berdasarkan judul, atau tempel link / URI / ID track Spotify.
- Progres unduh per lagu (cincin persentase), penamaan otomatis `Artis - Judul.mp3`.
- Metadata (judul, artis, album, durasi) ditulis ke MediaStore; berkas tersimpan di `Music/Spotidown`.
- Tab **Unduhan**: putar/jeda, bagikan, dan hapus lagu yang sudah diunduh.
- Menerima share teks langsung dari aplikasi lain (misalnya tombol Bagikan dari aplikasi Spotify).
- Tanpa akun, tanpa API key, tanpa izin penyimpanan tambahan (Scoped Storage API 29+).

## Catatan

Aplikasi hanya mengambil tautan yang disediakan oleh `spotidown.app`; tidak ada bypass reCAPTCHA karena permintaan dikirim dari halaman aslinya. Gunakan hanya untuk konten yang berhak kamu unduh, serta patuhi Ketentuan Layanan Spotify dan hukum yang berlaku.
