# Undangan Pernikahan — Rendi & Boru

## Cara Deploy ke Vercel
1. Upload folder ini (index.html, vercel.json, folder images/) ke sebuah repo GitHub, atau
2. Drag & drop folder ini langsung ke [vercel.com/new](https://vercel.com/new) (New Project → tanpa framework / "Other").
3. `vercel.json` sudah diatur supaya URL seperti:
   `https://nama-project-kamu.vercel.app/budi-santoso`
   tetap membuka undangan ini dengan nama tamu otomatis terisi "Budi Santoso".
4. Tanpa nama tamu (`https://nama-project-kamu.vercel.app/`) akan menampilkan undangan umum tanpa nama.

## Cara Ganti Data (Nama, Tanggal, Alamat, Rekening)
Buka `index.html`, cari bagian:

```js
const CONFIG = {
  groom: { fullName: "Rendi Danu Prasetyo", parents: "Bapak & Ibu Orang Tua Mempelai 1" },
  bride: { fullName: "Boru Hotnida Samosir", parents: "Bapak & Ibu Orang Tua Mempelai 2" },
  akad: { day: "Senin", date: "7 September 2026", time: "08.00 WIB – Selesai" },
  resepsi: { day: "Selasa", date: "8 September 2026", time: "11.00 – 14.00 WIB" },
  address: "...",
  mapQuery: "...",
  countdownTarget: "2026-09-07T08:00:00+07:00",
  banks: [ ... ],
};
```

Semua teks di halaman otomatis mengikuti nilai di `CONFIG` ini — cukup edit di satu tempat.

## Foto
Foto ada di folder `images/`. Ganti file dengan nama yang sama (`couple-portrait.jpg`, dst.)
untuk mengganti foto tanpa perlu mengubah kode HTML.

## Nama Tamu Custom
Gunakan situs generator terpisah (`wedding-generator`) untuk membuat link
`.../nama-tamu` secara otomatis, lalu bagikan link tersebut ke tamu terkait.
