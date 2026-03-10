# AdsIQ v2 — Deploy Guide

## Struktur File
```
adsiq-v2/
├── index.html        ← Frontend
├── api/
│   └── analyze.js    ← Vercel Function (backend)
├── vercel.json       ← Config Vercel
└── README.md
```

---

## 🚀 Cara Deploy ke Vercel (Step by Step)

### Step 1 — Upload ke GitHub
1. Buka github.com → login
2. Klik tombol hijau **"New"** → buat repo baru (misal: `adsiq`)
3. Klik **"uploading an existing file"**
4. Upload semua file dari folder `adsiq-v2` ini
5. Klik **"Commit changes"**

### Step 2 — Deploy ke Vercel
1. Buka vercel.com → login pakai GitHub
2. Klik **"Add New Project"**
3. Pilih repo `adsiq` yang baru kamu buat
4. Klik **Deploy** — tunggu ~1 menit

### Step 3 — Set API Key (PENTING!)
1. Di dashboard Vercel, buka project kamu
2. Klik **Settings** → **Environment Variables**
3. Tambah variable baru:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** `sk-ant-api03-...` (API key kamu dari console.anthropic.com)
4. Klik **Save**
5. Klik **Deployments** → **Redeploy** (agar env variable aktif)

### Step 4 — Selesai! 🎉
Buka URL Vercel kamu → AdsIQ sudah bisa analisis dengan AI!

---

## 💡 Cara Dapat API Key Anthropic
1. Buka https://console.anthropic.com
2. Daftar / login
3. Klik **API Keys** → **Create Key**
4. Copy key-nya (mulai dengan `sk-ant-...`)
5. Ada free credit $5 untuk mulai!

---

## ❓ FAQ

**Q: Apakah user bisa lihat API key saya?**
A: Tidak! API key tersimpan aman di server Vercel sebagai environment variable. User hanya berinteraksi dengan frontend.

**Q: Berapa biaya API per analisis?**
A: Sekitar $0.01–0.03 per analisis. Dengan $5 free credit bisa untuk ~200 analisis.

**Q: Bisa pakai file CSV apa?**
A: Laporan yang bisa di-download dari dashboard TikTok Ads Manager, Meta Ads Manager, Google Ads, atau Shopee Seller Center.
