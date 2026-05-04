# 🎬 Alat Analisis Video Bilibili

> Alat yang ringan, cepat, dan serbaguna untuk mengekstrak konten video dari Bilibili (Versi Pembelajaran & Penelitian)

[🌐 Demo Online](https://twittervideodownloaderx.com/bilibili_downloader_in) • [📝 Panduan Penggunaan](#-panduan-penggunaan) • [❓ Pertanyaan Umum](#-pertanyaan-umum)

---

## 📋 Gambaran Proyek

Proyek ini adalah alat analisis video berbasis web yang dirancang untuk mengekstrak metadata sumber daya media dari video publik di platform Bilibili (哔哩哔哩) dengan aman, serta menyediakan opsi konversi format dan penyimpanan lokal. Tidak memerlukan instalasi perangkat lunak klien atau pendaftaran akun: gunakan langsung melalui browser Anda.

> ⚠️ **Peringatan Penting**: Alat ini dirancang khusus untuk tujuan pembelajaran pribadi, penelitian teknis, dan penggunaan dalam batas yang wajar. Harap patuhi [Pedoman Komunitas Bilibili](https://www.bilibili.com/blackboard/protocol.html), 《Undang-Undang Hak Cipta Republik Rakyat Tiongkok》 serta peraturan terkait lainnya. Hormati karya para kreator; jangan gunakan konten yang diunduh untuk tujuan komersial atau untuk melanggar hak pihak ketiga.

---

## ✨ Fitur Utama

- 🔗 **Analisis Tautan**: Mendukung URL video/animasi Bilibili standar; deteksi otomatis episode dan opsi resolusi yang tersedia
- 📥 **Ekspor Multi-Format**:
  - Aliran video asli (mendukung resolusi publik seperti 1080P/720P, dll.)
  - Ekstraksi audio → Format MP3 (praktis untuk mendengarkan kuliah/musik secara offline)
  - Klip video → Konversi ke GIF animasi (ideal untuk membuat meme/demonstrasi edukasi)
- 🌍 **Antarmuka Multibahasa**: Dukungan untuk bahasa Indonesia, Inggris, Mandarin, Jepang, Korea, dan banyak bahasa lainnya
- 📱 **Kompatibilitas Lintas Platform**: Berfungsi sempurna di Chrome / Firefox / Safari / Edge; pengalaman optimal untuk perangkat seluler dan tablet
- 🔒 **Privitas Diutamakan**: Tidak perlu login akun Bilibili, tidak mengumpulkan data pribadi; proses analisis sepenuhnya anonim
- ⚡ **Pemrosesan Cepat**: Analisis selesai rata-rata dalam waktu 5-10 detik; dukungan untuk permintaan simultan dan pemrosesan batch

---

## 🚀 Memulai dengan Cepat

### Penggunaan Online (direkomendasikan)
1. Kunjungi [https://twittervideodownloaderx.com/bilibili_downloader_in](https://twittervideodownloaderx.com/bilibili_downloader_in)
2. Salin tautan video target (contoh: `https://www.bilibili.com/video/BV1xx411c7mD`)
3. Tempel tautan ke kolom input → Klik tombol 「Analisis」
4. Pilih resolusi dan format yang diinginkan → Simpan file mengikuti petunjuk browser

### Penyebaran Lokal (untuk pengembang)
```bash
# Clone repositori
git clone https://github.com/your-repo/bili-video-parser.git

# Instal dependensi
cd bili-video-parser && npm install

# Konfigurasi variabel lingkungan (opsional)
cp .env.example .env

# Jalankan server pengembangan
npm run dev
```

> 💡 Catatan: Proyek ini menggunakan arsitektur berbasis Node.js + Express. Silakan lihat dokumentasi penyebaran lengkap di `/docs/DEPLOY.md`

---

## 🛠 Tumpukan Teknologi

| Modul | Teknologi yang Digunakan |
|-------|--------------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Pemrosesan Video | ffmpeg.wasm (konversi ringan di sisi klien) |
| Proxy Penerusan | Cloudflare Workers / Middleware Kustom |
| Internasionalisasi | vue-i18n + Paket Bahasa JSON |

---

## 📚 Panduan Penggunaan

### Alur Kerja Dasar
```
1. Dapatkan tautan video
   └─ Buka video target di Bilibili → Salin URL dari bilah alamat browser

2. Kirim permintaan analisis
   └─ Tempel tautan ke kolom input alat → Klik 「Mulai Analisis」

3. Pilih konfigurasi output
   ├─ 🎬 Unduh Video: Pilih resolusi (360P/720P/1080P, dll. - hanya opsi publik)
   ├─ 🎵 Ekstrak Audio: Hasilkan file MP3 (ideal untuk mendengarkan kuliah/musik offline)
   └─ 🎞 Buat GIF: Buat animasi dari rentang waktu yang ditentukan (direkomendasikan: ≤15 detik)

4. Simpan file
   └─ Sumber daya akan terbuka di tab baru → Klik kanan/menu → 「Simpan sebagai」
```

### Tips Penggunaan di Perangkat Seluler
- iOS Safari: Tombol Bagikan → 「Simpan ke File」
- Android Chrome: Tekan lama pada pratinjau video → 「Unduh video」
- Jika video diputar otomatis: Klik `⋮` di sudut kanan atas pemutar → Pilih 「Unduh」

---

## ❓ Pertanyaan Umum

**T: Di mana file yang diunduh disimpan?**  
J: File disimpan di folder unduhan yang dikonfigurasi di browser Anda. Anda dapat memeriksa atau mengubah jalur ini di pengaturan browser.

**T: Bisakah saya menganalisis konten eksklusif untuk anggota atau yang memerlukan login?**  
J: Tidak. Alat ini hanya berfungsi dengan video yang diatur sebagai publik dan menghormati pengaturan akses konten asli.

**T: Apakah kualitas gambar/audio berkurang setelah konversi?**  
J: Unduhan video mempertahankan bitrate asli dari resolusi yang dipilih. Format MP3 menggunakan pengodean standar 128 kbps. Format GIF mengoptimalkan frame rate sesuai durasi untuk menyeimbangkan ukuran file dan kelancaran.

**T: Apakah riwayat unduhan atau cache disimpan?**  
J: Tidak. Semua sumber daya ditransmisikan langsung ke perangkat pengguna melalui proxy sementara; server tidak menyimpan permintaan atau file media apa pun.

**T: Apa yang harus dilakukan jika analisis gagal?**  
J: Harap periksa: ① Apakah tautan mengarah ke video publik yang valid ② Apakah koneksi internet Anda stabil ③ Coba gunakan browser lain. Jika masalah berlanjut, jangan ragu untuk melaporkannya melalui Issue.

---

## ⚖️ Kepatuhan Regulasi dan Penyangkalan Tanggung Jawab

- Alat ini **tidak melewati atau melanggar langkah perlindungan teknis apa pun** dari platform; alat ini hanya memperoleh metadata melalui antarmuka publik
- Pengguna bertanggung jawab untuk memverifikasi bahwa penggunaan mereka sesuai dengan hukum setempat dan ketentuan layanan platform
- Skenario penggunaan yang direkomendasikan: Pengarsipan pribadi untuk pembelajaran, demonstrasi edukasional, materi referensi untuk pembuatan konten... selalu dalam kerangka penggunaan wajar (Fair Use)
- Jika Anda menemukan konten yang diduga melanggar hak, silakan hubungi saluran resmi [Bilibili melalui formulir pelaporan hak cipta ini](https://www.bilibili.com/blackboard/help.html#copyright)

---

## 🤝 Panduan Berkontribusi

Kami menyambut Pull Request dan laporan Issue Anda! Sebelum berkontribusi, silakan baca:
- [Standar Kode](/CONTRIBUTING.md)
- [Panduan Terjemahan Multibahasa](/locales/README.md)
- [Persyaratan Keamanan dan Kepatuhan](/SECURITY.md)

---

## 📄 Lisensi

Proyek ini diterbitkan di bawah [Lisensi MIT](/LICENSE). Dapat digunakan secara gratis untuk tujuan pendidikan dan penelitian. Untuk penggunaan komersial, harap periksa dengan cermat kepatuhan terhadap regulasi hukum yang berlaku.

---

> 🌟 Jika alat ini bermanfaat bagi Anda, jangan ragu untuk ✨memberikan Bintang (Star)! Dukungan Anda adalah motivasi terbesar bagi kami untuk terus memelihara dan meningkatkan proyek ini~

*Pembaruan terakhir: Mei 2026 | Versi: v1.0.0*