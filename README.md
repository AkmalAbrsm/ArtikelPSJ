# Artikel Pengamanan Sistem Jaringan

Artikel untuk UAS Mata Kuliah Pengantar Sistem Jaringan (PSJ)

## Panduan Deploy ke Vercel

### Cara 1: Deploy via Vercel Dashboard (Paling Mudah)

1. **Buat Akun Vercel**
   - Kunjungi https://vercel.com/signup
   - Daftar menggunakan akun GitHub, GitLab, atau Bitbucket (direkomendasikan)
   - Atau daftar dengan email

2. **Push Project ke GitHub**
   ```powershell
   # Inisialisasi git repository
   cd "c:\College\PSJ\UAS"
   git init
   
   # Tambahkan semua file
   git add .
   git commit -m "Initial commit - Artikel Pengamanan Jaringan"
   
   # Buat repository di GitHub (via web browser)
   # Kemudian hubungkan dengan repository lokal
   git remote add origin https://github.com/USERNAME/REPO-NAME.git
   git branch -M main
   git push -u origin main
   ```

3. **Deploy di Vercel**
   - Login ke https://vercel.com/dashboard
   - Klik tombol "Add New..." → "Project"
   - Pilih repository GitHub yang baru dibuat
   - Klik "Import"
   - Vercel akan otomatis mendeteksi sebagai static site
   - Klik "Deploy"
   - Tunggu beberapa detik, website Anda akan live!

### Cara 2: Deploy via Vercel CLI

1. **Install Vercel CLI**
   ```powershell
   npm install -g vercel
   ```

2. **Login ke Vercel**
   ```powershell
   vercel login
   ```

3. **Deploy Project**
   ```powershell
   cd "c:\College\PSJ\UAS"
   vercel
   ```
   
   Ikuti instruksi yang muncul:
   - Set up and deploy? Y
   - Which scope? [pilih akun Anda]
   - Link to existing project? N
   - What's your project's name? [beri nama]
   - In which directory is your code located? ./
   - Want to override the settings? N

4. **Deploy ke Production**
   ```powershell
   vercel --prod
   ```

### Cara 3: Deploy Tanpa Git (Drag & Drop)

1. Login ke https://vercel.com/dashboard
2. Klik "Add New..." → "Project"
3. Pilih tab "Import Third-Party Git Repository"
4. Atau gunakan fitur drag & drop dengan:
   - Zip semua file (index.html dan vercel.json)
   - Drag & drop ke dashboard Vercel
   - Tunggu hingga deployment selesai

## Setelah Deploy

Setelah berhasil deploy, Anda akan mendapatkan URL seperti:
- `https://nama-project.vercel.app`
- `https://nama-project-username.vercel.app`

### Custom Domain (Opsional)

Jika ingin menggunakan domain custom:
1. Buka project di Vercel Dashboard
2. Klik tab "Settings" → "Domains"
3. Tambahkan domain Anda
4. Ikuti instruksi untuk konfigurasi DNS

## Kriteria Penilaian

✅ **Artikel dimuat di website/blog pribadi** - Deployed di Vercel (gratis)
✅ **Hyperlink ke upnyk.ac.id** - 2 link di artikel
✅ **Minimal 1000 kata** - ~1,450 kata
✅ **Topik sesuai PSJ** - Pengamanan Sistem Jaringan

## File dalam Project

- `index.html` - Halaman utama artikel dengan styling yang menarik
- `vercel.json` - Konfigurasi deployment Vercel
- `artikel_pengamanan_jaringan.md` - Versi markdown dari artikel
- `README.md` - Panduan deployment (file ini)

## Troubleshooting

### Jika deployment gagal:
1. Pastikan file `index.html` ada di root folder
2. Cek apakah ada error di build logs
3. Pastikan tidak ada karakter khusus di nama folder

### Jika tampilan tidak sesuai:
1. Clear cache browser (Ctrl + Shift + R)
2. Coba buka di browser lain atau mode incognito

## Support

Jika ada masalah, cek dokumentasi Vercel:
- https://vercel.com/docs

---

**Dibuat untuk:** UAS Mata Kuliah Pengantar Sistem Jaringan (PSJ)
**Tanggal:** 25 Desember 2025