# Tutorial: Install 4:6 Method Calculator di Android

## File yang Kamu Butuhkan

Pastikan semua file ini ada dalam **satu folder yang sama**:

```
📁 46-method/
├── 46-calculator.html
├── manifest.json
├── sw.js
├── icon-192.png   ← buat sendiri (lihat langkah 1)
└── icon-512.png   ← buat sendiri (lihat langkah 1)
```

---

## Langkah 1 — Buat Icon App

Kamu perlu 2 file icon PNG:
- `icon-192.png` ukuran 192×192 px
- `icon-512.png` ukuran 512×512 px

**Cara paling gampang:**
1. Buka [favicon.io](https://favicon.io/favicon-generator/) atau [realfavicongenerator.net](https://realfavicongenerator.net)
2. Buat icon dengan teks "4:6" atau upload gambar cangkir kopi
3. Download, rename sesuai nama di atas
4. Taruh di folder yang sama dengan HTML

> Kalau malas buat icon dulu, app tetap bisa jalan — hanya iconnya akan default/kosong.

---

## Langkah 2 — Host File-nya

PWA harus diakses lewat **HTTPS** (bukan buka file langsung). Ada beberapa opsi gratis:

### Opsi A — GitHub Pages (Rekomendasi)
1. Buat akun di [github.com](https://github.com) kalau belum punya
2. Buat repository baru → nama bebas, misal `46-calculator`
3. Upload semua file ke repository
4. Masuk ke **Settings → Pages**
5. Di bagian *Source*, pilih `main` branch → Save
6. Tunggu 1-2 menit → URL kamu akan jadi:
   `https://username.github.io/46-calculator/46-calculator.html`

### Opsi B — Netlify Drop (Paling Cepat)
1. Buka [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag & drop seluruh folder `46-method/` ke halaman tersebut
3. Selesai — kamu langsung dapat URL HTTPS

### Opsi C — Vercel
1. Buka [vercel.com](https://vercel.com)
2. Import dari GitHub atau upload folder
3. Deploy otomatis

---

## Langkah 3 — Install di Android

1. Buka **Chrome** di HP Android
2. Ketik URL app kamu (hasil dari langkah 2)
3. Tunggu halaman terbuka sempurna
4. Tap ikon **⋮ (tiga titik)** di pojok kanan atas Chrome
5. Pilih **"Add to Home screen"** atau **"Install app"**
6. Konfirmasi → tap **Install** atau **Add**
7. Icon app akan muncul di home screen Android kamu ✅

---

## Langkah 4 — Verifikasi Offline

Setelah install:
1. Matikan WiFi dan data
2. Buka app dari home screen
3. App tetap harus bisa terbuka → berarti offline mode berhasil

> Font (DM Serif & DM Mono) butuh internet pertama kali. Setelah itu, font juga ter-cache otomatis oleh browser.

---

## Troubleshooting

| Masalah | Solusi |
|---|---|
| Tidak muncul "Add to Home screen" | Pastikan akses lewat HTTPS, bukan `file://` |
| App tidak bisa offline | Coba buka dulu lewat browser, tunggu beberapa detik, baru matikan internet |
| Icon tidak muncul | Pastikan `icon-192.png` ada di folder dan nama file persis sama |
| Layar putih saat dibuka | Clear cache Chrome, buka lagi lewat browser dulu |

---

## Catatan

- App ini **tidak perlu Play Store** — langsung dari browser
- Update app: upload ulang file ke hosting, lalu di HP buka lewat browser sekali → cache otomatis update
- Kalau pakai Netlify/Vercel, update cukup upload file baru ke platform tersebut
