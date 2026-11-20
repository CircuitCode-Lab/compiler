# C Lab Compiler

Compiler C dalam pelayar untuk pelajar **DEC20313 C Programming** — sebahagian daripada [C Programming Learning Lab](https://circuitcode-lab.github.io/clab/), JKE Politeknik Kota Bharu.

**Laman langsung:** https://circuitcode-lab.github.io/compiler/

Repo ini berasingan daripada `clab` supaya compiler boleh dipasang sebagai **app sendiri** (ikon "C Compiler") walaupun app C Lab sudah dipasang. App PWA meliputi semua halaman di bawah folder skopnya, jadi compiler di bawah `/clab/` dianggap sebahagian daripada app C Lab.

## Fail
```
index.html      → editor, input, output + interpreter PicoC (WebAssembly) dibenamkan, dijalankan dalam Web Worker
manifest.json   → maklumat app (id /compiler/, nama "C Compiler")
sw.js           → service worker: simpan semua fail supaya boleh guna offline
favicon.png, apple-touch-icon.png, icon-192.png, icon-512.png, icon-maskable-192.png, icon-maskable-512.png
```

## Nota teknikal
- Tiada server: kod dijalankan dalam telefon/laptop pelajar.
- `scanf`: nilai diisi dalam kotak Input (satu nilai setiap baris). `%f` ditukar automatik kepada `%lf` kerana `float` = `double` dalam PicoC.
- `conio.h`, `getch()`, `system("pause")` diabaikan. Had masa 8 saat (gelung tak terhingga).
- Tema light/dark dikongsi dengan Laman Utama (kunci `clab-tema`, asal yang sama).

## Cara kemas kini
Ubah `index.html`, kemudian **naikkan nombor `CACHE` dalam `sw.js`** (cth. `c-compiler-v2`) supaya telefon pelajar memuat turun versi baharu.

## Lesen
PicoC — lesen BSD, © 2009–2011 Zik Saleeba, © 2015 Joseph Poirier.

## Sejarah
- **20 Nov 2026:** Ikon baharu "C Coding Orbit" (favicon, ikon app, ikon maskable Android, apple-touch-icon). Cache v2.
- **20 Nov 2026:** Dipindah dari `clab/compiler/` ke repo sendiri. Alamat lama melencong ke sini.

---
Hak Cipta & Idea © 2026 Wan Fazlini Idayu · Jabatan Kejuruteraan Elektrik, Politeknik Kota Bharu
