# Portofolio — Technical Analyst & EA Developer

Website portofolio statis (HTML + CSS + JS, tanpa framework/build step), responsif untuk desktop, tablet, dan mobile.

## Sebelum deploy — bagian yang WAJIB diedit

Buka `index.html`, cari dan ganti bagian berikut:

1. **Nama**
   - `<title>Nama Anda — ...</title>`
   - `<span id="year"></span> Nama Anda` (di footer)
2. **Pengalaman AI Builder** — ganti `[nama website]` dengan nama platform aslinya (contoh: "Bolt.new", "Lovable", dsb).
3. **Kontak** (di section `#kontak`):
   - `mailto:email@anda.com` → email asli
   - `https://t.me/username` → username Telegram asli
   - `https://wa.me/62xxxxxxxxxx` → nomor WhatsApp asli (format internasional tanpa "+" atau "0" di depan)

Tips: gunakan Ctrl+F / Cmd+F di editor untuk mencari teks di atas dengan cepat.

## Cara deploy ke Vercel (gratis)

### Opsi A — tanpa GitHub (paling cepat)
1. Install Vercel CLI: `npm install -g vercel`
2. Di folder ini, jalankan: `vercel`
3. Ikuti instruksi di terminal (login akun Vercel jika diminta).
4. Setelah selesai, Vercel akan memberi URL publik (contoh: `nama-anda.vercel.app`).
5. Untuk update berikutnya cukup jalankan `vercel --prod`.

### Opsi B — lewat GitHub (lebih mudah untuk update jangka panjang)
1. Buat repo baru di GitHub, upload semua file di folder ini.
2. Buka [vercel.com](https://vercel.com) → Add New Project → Import repo tersebut.
3. Biarkan pengaturan default (tidak perlu build command, karena ini HTML statis) → Deploy.
4. Setiap kali push ke GitHub, Vercel otomatis deploy ulang.

## Struktur file
```
index.html     -> seluruh halaman (HTML + CSS + JS jadi satu file)
vercel.json    -> konfigurasi ringan untuk Vercel
```

## Kustomisasi lanjutan
- Warna diatur lewat CSS variable di bagian atas `<style>` (`:root`), gampang diganti tanpa menyentuh bagian lain.
- Section "Pengalaman" bergaya tabel watchlist trading — tinggal tambah/kurangi blok `.ticker-row` kalau mau menambah pengalaman lain.
- Grafik candlestick di hero dibuat otomatis oleh JavaScript, tidak perlu gambar/aset eksternal.
