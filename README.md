# Convert Tools

Aplikasi web sederhana berbasis HTML, CSS, dan JavaScript untuk dua kebutuhan konversi file secara langsung di browser — tanpa upload ke server.

## Fitur

### 1. PNG to PDF
- Upload banyak gambar sekaligus (PNG, JPG, WEBP) lewat drag & drop atau klik tombol.
- Preview tiap gambar lengkap dengan nomor halaman, nama file, dan ukuran file.
- Hapus gambar satu per satu atau hapus semua.
- Gabungkan semua gambar menjadi satu file PDF, dengan setiap gambar otomatis diatur agar pas di tengah halaman.
- Nama file PDF bisa diatur sendiri sebelum diunduh.

### 2. MP4 to MP3 (WAV)
- Upload satu file video (MP4 dan format video lain yang didukung browser) lewat drag & drop atau klik tombol.
- Preview informasi file: nama dan ukuran.
- Ekstraksi audio dilakukan langsung di browser menggunakan Web Audio API — tidak ada file yang dikirim ke server.
- Hasil ekstraksi diunduh otomatis dalam format `.wav` dengan nama acak (`tools.dap.XXXXX.wav`).
- Progress bar menampilkan tahapan proses (membaca file → decode audio → konversi ke WAV → simpan).

## Cara Pakai

1. Buka file `convert-tools.html` di browser.
2. Pilih tab sesuai kebutuhan: **PNG to PDF** atau **MP4 to MP3**.
3. Upload file dengan drag & drop atau klik area upload.
4. Atur/preview file yang sudah diupload.
5. Klik tombol aksi (**Konversi ke PDF** / **Ekstrak Audio**) untuk memproses dan mengunduh hasil.

## Teknologi

- **HTML/CSS** — struktur dan tampilan, didesain minimalis dengan tema warna biru (`#4f6ef7`).
- **JavaScript (vanilla)** — logika upload, preview, dan konversi.
- **[jsPDF](https://github.com/parallax/jsPDF)** (via CDN) — untuk membuat file PDF dari gambar.
- **Web Audio API** — untuk decode dan konversi audio video ke WAV secara native di browser.

## Catatan

- Semua proses konversi berjalan 100% di sisi klien (browser), sehingga aman untuk privasi dan tidak membutuhkan backend/server.
- Dukungan format video untuk fitur MP4 to MP3 bergantung pada codec yang didukung oleh browser pengguna.
- Tidak ada dependensi instalasi — cukup buka file HTML secara langsung.
