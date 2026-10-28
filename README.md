# NOTO — Productivity Workspace & Customer App (Repositori Apps)

> Repositori Aplikasi Produktivitas & Customer Platform **NOTO — Get Things Done**.
> Menggabungkan Today Dashboard, Tasks Engine, Calendar, Focus Mode, Reference Hub, Analytics, AI Coach, QRIS Store, dan Staff Admin Portal.

Proyek ini dibangun murni menggunakan **HTML5 semantik, CSS3 responsif, dan Vanilla JavaScript (ES6+)** tanpa framework atau build tools.

---

## 📁 Isi Repositori Ini (`apps`)

```
noto-apps/
├── index.html        # Entrypoint aplikasi utama (Autentikasi & Workspace Shell)
├── app.js            # Controller logika aplikasi, state management, & koneksi ke web
├── styles.css        # Desain UI komponen workspace, modal, & tema
├── admin.html        # Portal Staff Admin Operations (PIN Gate: noto2026 / admin123)
├── admin.js          # Controller operasional staf admin
├── manifest.json     # PWA Manifest untuk instalasi HP & Desktop
├── service-worker.js # Cache offline PWA
├── vercel.json       # Konfigurasi routing Vercel
├── assets/           # Ikon PWA, QRIS merchant image, qrcode.min.js
└── README.md
```

---

## ⚠️ CARA UPLOAD KE GITHUB AGAR VERCEL TIDAK 404!

Penyebab utama error **404 NOT_FOUND** di Vercel adalah karena file `index.html` terbungkus di dalam folder `apps/`.

**Langkah yang Benar:**
1. Buat repository baru di GitHub bernama **`noto-apps`**.
2. Di laptop Anda, buka folder: **`C:\Users\HP\Documents\NOTO\apps`**.
3. **MASUK KE DALAM FOLDER `apps` TERSEBUT**.
4. Blok / pilih **semua file dan folder yang ada di dalamnya**:
   - `index.html`
   - `app.js`
   - `styles.css`
   - `admin.html`
   - `admin.js`
   - `manifest.json`
   - `service-worker.js`
   - `vercel.json`
   - folder `assets`
5. **Drag & Drop** file-file tersebut ke halaman upload GitHub.
6. Klik **Commit changes**.
   *(Pastikan di halaman GitHub, file `index.html` berada langsung di halaman depan repository, BUKAN di dalam folder `apps/`)*.
7. Di Vercel, buat project baru dan import repository `noto-apps` tersebut. Vercel akan langsung aktif tanpa 404!

---

## 🔗 Cara Menghubungkan ke Repositori Website (`noto-web`)

Di file `app.js`, sistem sudah memiliki **fitur auto-detect**:
* Jika URL aplikasi Anda adalah `https://noto-apps.vercel.app`, tombol *"Kembali ke Website"* akan **otomatis** mengarah ke `https://noto-web.vercel.app`!
* Jika URL website Anda berbeda, cukup buka file `app.js` baris ke-11 dan isi alamatnya:
  ```javascript
  const CUSTOM_WEB_URL = 'https://alamat-vercel-website-anda.vercel.app';
  ```
