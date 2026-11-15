🚀 DEPLOY HTML ZIP

<p align="center">
  <img src="https://img.shields.io/badge/DEPLOY-HTML%20ZIP-ff69b4?style=for-the-badge" alt="Deploy HTML ZIP">
  <img src="https://img.shields.io/badge/VERSION-1.0.0-blue?style=for-the-badge" alt="Version 1.0.0">
  <img src="https://img.shields.io/badge/NODE.JS-18%2B-green?style=for-the-badge" alt="Node.js 18+">
  <img src="https://img.shields.io/badge/PLATFORM-VERCEL-black?style=for-the-badge" alt="Vercel">
  <img src="https://img.shields.io/badge/LICENSE-COPYRIGHT-red?style=for-the-badge" alt="Copyright">
</p><p align="center">
  <strong>🌐 Simple • Fast • Direct Website Deployment</strong>
  <br>
  Developed & Created by <strong>XIYU CODEX</strong>
</p>---

📖 ABOUT PROJECT

DEPLOY HTML ZIP adalah sebuah tool deployment berbasis Node.js yang dirancang untuk mempermudah proses publikasi website statis ke platform Vercel.

Dengan tool ini, pengguna dapat melakukan deployment website secara langsung melalui terminal tanpa harus mengunggah file secara manual melalui dashboard Vercel.

Pengguna cukup menyiapkan folder website, file HTML, atau arsip ZIP, kemudian menjalankan perintah deployment.

Seluruh proses upload dan deployment dilakukan melalui Vercel REST API menggunakan Access Token milik pengguna sendiri.

🎯 Project ini dibuat untuk menghadirkan pengalaman deployment yang praktis, sederhana, efisien, dan mudah digunakan.

---

✨ FEATURES

Berikut fitur utama yang tersedia:

Feature| Description
📁 Folder Deployment| Deploy website langsung dari folder lokal
📄 HTML Deployment| Mendukung deployment file HTML
📦 ZIP Deployment| Upload dan ekstraksi website dari ZIP
🧹 Path Normalization| Normalisasi struktur direktori ZIP
🔐 Token Verification| Validasi Vercel Access Token
☁️ Direct API Upload| Upload file langsung ke Vercel API
🚀 Automatic Deployment| Membuat deployment secara otomatis
📊 Deployment Monitoring| Memantau status deployment
🏷️ Project Naming| Normalisasi nama project otomatis
👥 Team Support| Mendukung konfigurasi Vercel Team ID
🌍 Production Mode| Mendukung deployment Production
🛡️ File Validation| Validasi jumlah dan ukuran file

---

🧰 REQUIREMENTS

Pastikan perangkat sudah memiliki:

- 🟢 Node.js versi 18 atau lebih baru.
- 📦 NPM.
- 🔑 Vercel Access Token.
- 🌐 Koneksi internet.
- 📚 Package "jszip".

💻 Supported Environments

- 📱 Android + Termux
- 🐧 Linux
- 🪟 Windows
- 🍎 macOS
- ☁️ VPS / Node.js Environment

---

📥 INSTALLATION

1️⃣ Clone Repository

git clone https://github.com/USERNAME/REPOSITORY.git

Masuk ke direktori project:

cd REPOSITORY

2️⃣ Install Dependencies

npm install

Atau instal dependency yang diperlukan secara langsung:

npm install jszip

3️⃣ Verify Installation

node --version
npm --version

Pastikan Node.js sudah terpasang dengan benar.

4️⃣ Check Application

node --check deployhtmlzip.js

Jika tidak muncul error, source code berhasil melewati pemeriksaan sintaks.

---

🔑 VERCEL CONFIGURATION

DEPLOY HTML ZIP menggunakan Vercel Access Token untuk mengakses akun Vercel pengguna.

🔐 1. Generate Vercel Token

1. Buka halaman "Vercel Tokens" (https://vercel.com/account/settings/tokens).
2. Login ke akun Vercel.
3. Pilih Create Token.
4. Masukkan nama token.
5. Pilih scope yang sesuai.
6. Tentukan masa berlaku.
7. Buat dan salin token.

⚠️ Simpan token dengan aman. Jangan membagikannya kepada siapa pun.

👥 2. Vercel Team ID (Optional)

Jika menggunakan akun Team:

1. Buka Vercel Dashboard.
2. Pilih Team yang ingin digunakan.
3. Masuk ke pengaturan Team.
4. Cari bagian Team ID.
5. Salin ID tersebut.

Pengguna akun personal tidak wajib mengatur Team ID.

---

⚙️ ENVIRONMENT VARIABLES

Tersedia dua environment variable:

Variable| Required| Description
"VERCEL_TOKEN"| ✅ Yes| Vercel Access Token
"VERCEL_TEAM_ID"| ❌ Optional| Vercel Team ID

📝 Set Vercel Token

Linux / Termux / macOS:

export VERCEL_TOKEN="YOUR_VERCEL_TOKEN"

📝 Set Team ID

export VERCEL_TEAM_ID="team_xxxxxxxxx"

Jika menggunakan akun personal, cukup gunakan "VERCEL_TOKEN".

💡 Apabila VERCEL_TOKEN tidak diatur melalui environment variable, aplikasi akan meminta token secara langsung ketika dijalankan.

---

🚀 HOW TO USE

📦 1. Deploy ZIP File

node deployhtmlzip.js ./website.zip my-website

📁 2. Deploy Folder

node deployhtmlzip.js ./website my-website

📄 3. Deploy HTML File

node deployhtmlzip.js ./index.html my-website

🌍 4. Production Deployment

node deployhtmlzip.js ./website.zip my-website --production

❓ 5. Display Help

node deployhtmlzip.js --help

---

🔄 DEPLOYMENT WORKFLOW

Berikut gambaran proses deployment:

       📁 WEBSITE SOURCE
              |
              ▼
      📦 FILE / ZIP INPUT
              |
              ▼
      🧹 FILE EXTRACTION
              |
              ▼
      🔍 FILE VALIDATION
              |
              ▼
       🔐 TOKEN VERIFICATION
              |
              ▼
       ☁️ UPLOAD TO VERCEL
              |
              ▼
       🚀 CREATE DEPLOYMENT
              |
              ▼
       📊 MONITOR STATUS
              |
              ▼
       ✅ DEPLOYMENT READY
              |
              ▼
          🌐 WEBSITE URL

---

📏 FILE LIMITATIONS

Untuk menjaga batas pemrosesan, aplikasi memiliki konfigurasi berikut:

Limitation| Maximum
📄 Maximum Files| 120 files
📦 ZIP File Size| 8 MiB
📁 Individual File| 4 MiB
💾 Total File Content| 6.5 MiB

🗂️ Supported ZIP Structure

Contoh struktur website:

website/
├── index.html
├── about.html
├── contact.html
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── script.js
│   └── images/
│       └── logo.png
└── favicon.ico

💡 Pastikan file "index.html" berada di root direktori website agar halaman utama dapat dikenali secara langsung.

---

🛡️ SECURITY

Keamanan token merupakan salah satu hal penting dalam penggunaan aplikasi ini.

🔐 Beberapa hal yang perlu diperhatikan:

- Gunakan Access Token milik sendiri.
- Jangan membagikan token kepada publik.
- Jangan mengunggah token ke repository GitHub.
- Jangan menyimpan token langsung di source code.
- Gunakan environment variable untuk konfigurasi token.
- Gunakan scope dan masa berlaku token seperlunya.
- Hapus atau cabut token jika sudah tidak digunakan.

⚠️ DEPLOY HTML ZIP menggunakan kredensial Vercel pengguna untuk melakukan operasi deployment. Pengguna bertanggung jawab menjaga keamanan kredensial tersebut.

---

🧯 TROUBLESHOOTING

❌ Error: Cannot find module 'jszip'

Solusi:

npm install jszip

❌ Error: Invalid Token / Unauthorized

Kemungkinan token tidak valid atau sudah kedaluwarsa.

Solusi:

1. Periksa token.
2. Buat token baru jika diperlukan.
3. Pastikan token memiliki akses yang sesuai.

❌ Error: File Limit Exceeded

Jumlah atau ukuran file melebihi batas aplikasi.

Solusi:

- Kurangi jumlah file.
- Kompres atau optimalkan aset.
- Hapus file yang tidak diperlukan.

❌ Error: Deployment Failed

Periksa:

- Status akun Vercel.
- Hak akses token.
- Konfigurasi Team ID jika digunakan.
- Respons error dari Vercel API.
- Status deployment melalui Vercel Dashboard.

❌ Error: index.html Not Found

Pastikan website memiliki file "index.html" pada direktori utama.

---

📚 TECHNOLOGIES

Project ini menggunakan beberapa teknologi berikut:

Technology| Purpose
🟢 Node.js| Runtime environment
📦 JSZip| ZIP extraction
🔐 Crypto| SHA-1 file digest
🌐 Fetch API| HTTP requests
☁️ Vercel REST API| File upload and deployment

---

🌐 OFFICIAL LINKS

- 🌍 "Vercel Website" (https://vercel.com/)
- 📚 "Vercel Documentation" (https://vercel.com/docs)
- 🔑 "Vercel Access Tokens" (https://vercel.com/account/settings/tokens)
- 🔌 "Vercel REST API Reference" (https://vercel.com/docs/rest-api)
- 📦 "JSZip Documentation" (https://stuk.github.io/jszip/)

---

👨‍💻 DEVELOPER

<p align="center">
  <img src="https://img.shields.io/badge/DEVELOPER-XIYU%20CODEX-ff69b4?style=for-the-badge" alt="Developer XIYU CODEX">
  <br><br>
  <strong>XIYU CODEX</strong>
  <br>
  💻 Developer & Project Creator
  <br>
  🚀 Building practical tools and automation solutions.
  <br><br>
  <strong>CREATED WITH ❤️ BY XIYU CODEX</strong>
</p>---

©️ COPYRIGHT & LICENSE

Copyright © 2026 XIYU CODEX

All Rights Reserved.

DEPLOY HTML ZIP merupakan project yang dikembangkan oleh XIYU CODEX.

Seluruh hak atas source code asli, identitas project, dokumentasi, dan branding XIYU CODEX dilindungi oleh ketentuan hak cipta yang berlaku.

Dilarang mengklaim kepemilikan karya asli XIYU CODEX atau mendistribusikan ulang source code dengan menghapus atribusi pengembang.

Penggunaan Vercel REST API dan package pihak ketiga tetap mengikuti ketentuan serta lisensi masing-masing pemilik.

---

<p align="center">
  <img src="https://img.shields.io/badge/DEPLOY%20HTML%20ZIP-V1.0.0-ff69b4?style=for-the-badge" alt="Deploy HTML ZIP Version 1.0.0">
  <br><br>
  <strong>🚀 DEVELOPED & CREATED BY XIYU CODEX</strong>
  <br>
  ❤️ Thank you for using this project!
</p>
