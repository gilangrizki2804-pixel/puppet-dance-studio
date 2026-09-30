# 🕺 2D Puppet Skeleton Studio & Stop-Motion Dance Animator

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?logo=github)](https://pages.github.com/)
[![Pure JavaScript](https://img.shields.io/badge/JavaScript-Vanilla%20ES6+-yellow?logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML5 Canvas](https://img.shields.io/badge/HTML5-Canvas%202D%20Deformation-E34F26?logo=html5)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![Web Audio API](https://img.shields.io/badge/Web%20Audio%20API-Synthesizer-blue)](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
[![No Build Required](https://img.shields.io/badge/Zero%20Dependencies-Standalone%20HTML-blueviolet)]()

Aplikasi web interaktif tanpa build-step (*Zero Build / Plug & Play*) untuk membuat karakter 2D apa pun menari secara luwes (*puppet skeletal deformation*) dan memutar animasi stop-motion melingkar. Siap dijalankan langsung di browser lokal maupun dihosting di **GitHub Pages**!

---

## 🌟 Demo Animasi / Preview

| 🕺 Funk Groove Dance | 🔄 Circular Dance Rhythm |
| :---: | :---: |
| ![Funk Groove](character_dance_funk.gif) | ![Circle Dance](character_dance_circle.gif) |

| 🏃 Stop-Motion Dancers | ⚡ Circular Matisse Animation |
| :---: | :---: |
| ![Stop Motion](dancing_stop_motion.gif) | ![Circular Stop Motion](dancing_circle_rhythm.gif) |

---

## ✨ Fitur Unggulan (Key Features)

1. **🎨 Upload Gambar Bebas (Multi-input):**
   - Mendukung klik tombol unggah, **Drag and Drop** langsung ke canvas, maupun **Paste dari Clipboard (`Ctrl + V`)**.
   - Otomatis melakukan *rescaling* cerdas agar performa rendering tetap 60 FPS.

2. **🪄 Client-Side Auto Background Removal:**
   - Algoritma flood-fill BFS berbasis *Typed Array* yang aman dan cepat langsung di browser untuk membersihkan latar belakang gambar (putih/kontras) tanpa perlu server backend.

3. **🦴 Skeleton & Bone Rigging Editor:**
   - **Mode Edit Skeleton**: Geser titik sendi (Head, Neck, Torso, Hips, Elbows, Wrists, Knees, Feet) secara interaktif.
   - **Fitur Pin Tambahan**: Tambahkan pin kustom (*Add Pin*) dan hapus pin (*Delete Pin*) untuk titik deformasi fleksibel.
   - **Auto-Snap to Body**: Menempatkan kerangka tubuh secara proporsional otomatis di atas gambar karakter.

4. **💃 4 Koreografi Tarian Halus:**
   - **Funk Groove**: Goyangan pinggul, kepala berirama, dan lambaian tangan bergaya funk.
   - **Circle Dance**: Gerakan menari berputar melingkar yang dinamis.
   - **Wild Leap**: Lompatan ekspresif ke udara dengan ayunan kaki dan tangan.
   - **Body Wave**: Gelombang tubuh fluida elastis (*liquid wave motion*).

5. **🎵 Built-in Web Audio API Synthesizer:**
   - Drum beat synthesizer 4/4 dinamis (Kick, Snare, Hi-hat, Bass synth) yang sinkron dengan tempo tarian (BPM slider).

6. **🎥 Ekspor & Snapshot:**
   - Perekaman video langsung ke format **WebM** via `MediaRecorder`.
   - Tombol **Snapshot (PNG)** untuk menangkap pose terbaik dalam resolusi tinggi.

7. **🔄 Stop-Motion Player (`stop_motion_player.html`):**
   - Pemutar stop-motion melingkar dengan kontrol kecepatan frame, reverse, dan trail effect.

---

## 🚀 Cara Menjalankan Secara Lokal (Local Run)

Aplikasi ini dibuat dengan prinsip **Zero Configuration & Zero Build Step**:
1. Clone atau download repository ini.
2. Klik ganda file [`index.html`](index.html) atau klik kanan > *Open with* browser favorit Anda (Chrome, Edge, Firefox, Brave, Safari).
3. Aplikasi langsung berjalan 100% tanpa perlu Node.js, npm, atau server lokal!

---

## 🌐 Cara Mengunggah & Mengaktifkan di GitHub Pages

Ikuti langkah cepat berikut untuk mengunggah ke akun GitHub Anda dan menjadikannya web app online yang bisa diakses siapa saja:

### 1. Buat Repository Baru di GitHub
1. Buka [GitHub New Repository](https://github.com/new).
2. Beri nama repository (misalnya: `puppet-dance-studio`).
3. Pilih **Public**, lalu klik **Create repository** (jangan centang *Initialize with README* karena file sudah siap di lokal).

### 2. Hubungkan & Push dari Terminal / PowerShell
Buka terminal pada folder proyek ini, lalu jalankan perintah:

```bash
# Tambahkan alamat remote repository GitHub Anda (ganti USERNAME dan REPO_NAME)
git remote add origin https://github.com/<USERNAME>/<REPO_NAME>.git

# Pastikan branch utama bernama main
git branch -M main

# Unggah seluruh file ke GitHub
git push -u origin main
```

### 3. Aktifkan GitHub Pages
1. Masuk ke halaman repository Anda di GitHub.
2. Klik tab **Settings** (di sebelah kanan atas repo).
3. Pada menu navigasi sebelah kiri, klik **Pages** (di bawah *Code and automation*).
4. Di bagian **Build and deployment**:
   - **Source**: Pilih `Deploy from a branch`.
   - **Branch**: Pilih `main` dan folder `/(root)`.
5. Klik **Save**.
6. Tunggu sekitar 1–2 menit. Website Anda akan aktif di URL:
   ```
   https://<USERNAME>.github.io/<REPO_NAME>/
   ```

---

## 📁 Struktur File (Repository Structure)

```
Visual Project/
│
├── index.html                   # Halaman utama (Puppet Skeleton Studio) untuk GitHub Pages
├── puppet_skeleton_studio.html  # File studio rigging & tarian (identik dengan index.html)
├── stop_motion_player.html      # Player stop-motion lingkaran
├── README.md                    # Dokumentasi lengkap proyek & panduan deploy
├── .gitignore                   # Konfigurasi pengabaian file sampah sistem
│
├── character_dance_funk.gif     # Render animasi GIF: Funk Groove Dance
├── character_dance_circle.gif   # Render animasi GIF: Circle Dance
├── dancing_stop_motion.gif      # Render animasi GIF: Stop-Motion
├── dancing_circle_rhythm.gif    # Render animasi GIF: Circular Stop-Motion
│
├── dancing_character.jpg        # Gambar karakter awal
├── dancing_character_cutout.png # Versi cutout transparan hasil pengolahan
└── Daniel Zendor drawing...     # Asset referensi pose
```

---

## 💻 Lisensi & Kredit

- **Teknologi**: HTML5 Canvas, Web Audio API, Moving Least Squares (MLS) / Affine Mesh Deformation.
- **Lisensi**: Open Source (MIT) — bebas dimodifikasi, dikembangkan, dan dibagikan.
