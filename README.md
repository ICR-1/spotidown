# Spotidown — Android

Aplikasi Android (Kotlin + Jetpack Compose) untuk mengunduh lagu menjadi MP3 dan memutarnya langsung sebagai pemutar musik lokal dengan dukungan lirik sinkron.

## Unduh APK

Unduh berkas APK rilis terbaru langsung dari halaman **[Releases](https://github.com/ICR-1/spotidown/releases/latest)** di panel kanan repositori ini.

- **Versi:** `1.1`
- **Minimum OS:** Android 10 (API 29) atau lebih baru

## Fitur Utama

- **Cari & Unduh MP3:** Cari lagu berdasarkan judul atau tempel tautan / URI / ID lagu Spotify langsung dari clipboard atau menu Bagikan (*Share*) aplikasi lain.
- **Metadata & Sampul Otomatis:** Progres unduh per lagu, penamaan berkas otomatis `Artis - Judul.mp3`, serta penanaman tag ID3 (judul, artis, album, sampul album, dan lirik) ke folder `Music/Spotidown`.
- **Perpustakaan Musik:** Tampilan grid dengan sampul album; ketuk untuk memutar, tekan lama untuk membagikan atau menghapus berkas.
- **Pemutar Latar Belakang:** Didukung Media3/ExoPlayer dan `MediaSessionService` dengan kontrol penuh di notifikasi serta *lock screen*.
- **Layar Now Playing:** Sampul berlatar blur, *seek bar*, *shuffle* dan *repeat*, serta *mini player* persisten saat menjelajah aplikasi.
- **Lirik Sinkron:** Lirik diambil dari [LRCLIB](https://lrclib.net) (gratis, tanpa API key) dengan sorotan baris aktif dan gulir otomatis—ketuk baris lirik untuk melompat ke bagian lagu tersebut, serta disematkan di tag `USLT`.
- **Ringan & Privat:** Tanpa login akun, tanpa API key, dan tanpa izin penyimpanan tambahan (Scoped Storage Android 10+).

## Catatan

Pemutaran musik dibatasi pada berkas lokal hasil unduhan di folder `Music/Spotidown` (tanpa *streaming*). Gunakan aplikasi ini hanya untuk konten yang berhak kamu unduh serta patuhi ketentuan layanan dan hukum yang berlaku.
