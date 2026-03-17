# Crisis Monitor — Cara Deploy ke Vercel

Website pantauan bencana & konflik real-time.
Sumber data: BMKG, USGS, NASA EONET, ReliefWeb (UN)

---

## Deploy dalam 5 menit (gratis)

### Langkah 1 — Daftar Vercel
Buka https://vercel.com → klik "Sign Up" → pilih "Continue with GitHub"
(Buat akun GitHub dulu kalau belum punya, juga gratis)

### Langkah 2 — Upload proyek
1. Di halaman Vercel, klik tombol "Add New..." → "Project"
2. Pilih "Upload" (bukan import dari GitHub)
3. Drag & drop FOLDER "crisis-monitor-deploy" ini ke kotak upload
4. Klik "Deploy"
5. Tunggu ~1 menit

### Langkah 3 — Selesai
Vercel akan memberikan URL seperti: https://crisis-monitor-abc123.vercel.app
Website sudah live dan bisa diakses siapa saja!

---

## Struktur file

```
crisis-monitor-deploy/
  index.html        ← tampilan website
  api/
    events.js       ← ambil data dari BMKG, USGS, NASA, ReliefWeb
  vercel.json       ← konfigurasi Vercel
  README.md         ← panduan ini
```

---

## Data diperbarui otomatis

- Data di-cache 5 menit (tidak spam ke API sumber)
- Frontend refresh otomatis setiap 5 menit
- Semua sumber bisa dilihat status-nya di sidebar

## Sumber data

| Sumber | Data | Frekuensi |
|--------|------|-----------|
| BMKG | Gempa Indonesia | Real-time |
| USGS | Gempa global M4.5+ | Real-time |
| NASA EONET | Kebakaran, badai, gunung api | Harian |
| ReliefWeb (UN) | Laporan krisis kemanusiaan | Harian |
