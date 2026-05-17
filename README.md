# Static Portfolio Template

Portfolio statis one-page yang clean, modern, dan siap di-deploy ke GitHub Pages.
Dibuat dengan Jekyll tanpa framework JS atau build-step kompleks. Tersedia CMS admin gratis (Decap CMS + Netlify Identity).

## Fitur Utama
- 🚀 Sangat Cepat (Hanya HTML, CSS Murni, Vanilla JS)
- 📱 Responsive Design (Mobile First)
- 🌓 Dark/Light Mode
- ✨ Animasi Scroll Halus
- 🗄️ Terstruktur menggunakan Data (YAML)
- 📝 Siap digunakan dengan Admin Panel (Decap CMS)

## Struktur Folder
- `_config.yml`: Konfigurasi utama Jekyll
- `_data/`: Berisi file YAML untuk data Profile, Skills, Testimonials
- `_projects/`: Koleksi markdown berisi proyek-proyek yang pernah Anda buat
- `_layouts/default.html`: Struktur HTML dasar (Header, Footer, Main layout)
- `assets/css/style.css`: File CSS styling
- `assets/js/main.js`: Logika interaksi (Dark mode, Hamburger menu, Scroll animation)
- `admin/`: Berisi konfigurasi untuk Decap CMS

## Cara Edit Konten (Manual)

Untuk mulai mengisi data Anda, cari dan edit bagian yang ditandai dengan `# GANTI:` atau `<!-- GANTI: -->` pada file-file berikut:
1. `_data/profile.yml` (Nama, Role, Bio, Social Links)
2. `_data/skills.yml` (Keahlian)
3. `_data/testimonials.yml` (Review klien)
4. `_projects/*.md` (Portofolio proyek)
5. `assets/images/` (Ganti dengan aset gambar yang sesuai)
   - profil.jpg (400x400)
   - about.jpg (600x800)

## Cara Deploy ke GitHub Pages

1. Buat repository baru di GitHub dengan nama: `KaajiItsMe.github.io` (Penting agar menjadi root website).
2. Upload/push semua file dalam folder ini ke branch `main` di repository tersebut.
3. Buka tab **Settings** di repository GitHub Anda.
4. Pergi ke menu **Pages** (di sidebar kiri).
5. Pada bagian **Build and deployment**, pilih **Source: GitHub Actions** atau biarkan default Jekyll, karena GitHub otomatis mendeteksi. Jika menggunakan branch, pilih branch `main`, root `/`, lalu klik **Save**.
6. Tunggu beberapa menit, website Anda akan live di `https://kaajiitsme.github.io`.

## Setup Admin Panel (Decap CMS via Netlify Identity)

Anda bisa mengedit konten dari browser (tanpa coding) menggunakan Decap CMS. Berikut langkah setup-nya:

1. **Hubungkan Repo ke Netlify**:
   - Buat akun di [Netlify](https://www.netlify.com/).
   - Klik **Add new site** > **Import an existing project** dari GitHub.
   - Deploy situs Anda.
2. **Aktifkan Netlify Identity**:
   - Di dashboard Netlify, ke **Site settings** > **Identity** > klik **Enable Identity**.
3. **Konfigurasi Git Gateway**:
   - Di menu Identity, scroll ke bawah ke bagian **Services** > **Git Gateway**, klik **Enable Git Gateway**. (Akan menghubungkan akun GitHub Anda).
4. **Izinkan Pendaftaran Admin**:
   - Di tab **Identity** di menu atas Netlify, klik **Invite users** dan kirim ke email Anda, atau buka website Anda langsung di Netlify dan daftar lewat widget.
5. **Login**:
   - Buka URL website yang terdeploy (Netlify atau GitHub Pages), dan tambahkan `/admin` di belakangnya (contoh: `https://.../admin`).
   - Login menggunakan email yang sudah didaftarkan. Anda sekarang dapat mengubah isi `profile`, `skills`, `projects`, dll langsung dari browser!

## Local Development (Opsional)
Jika ingin menjalankan secara lokal untuk testing:
1. Pastikan Ruby dan Bundler terinstall.
2. Jalankan `bundle exec jekyll serve`.
3. Buka `http://localhost:4000`.
