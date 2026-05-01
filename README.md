# Seminar KP — Panduan Update Konten

## Struktur Folder

```
seminar-kp/
├── index.html                          ← Halaman utama (jangan diubah)
├── assets/
│   └── img/
│       └── logo-uii.png               ← Logo institusi (opsional)
├── berkas/
│   ├── laporan/
│   │   ├── template-laporan-kp.docx   ← Upload file di sini
│   │   └── panduan-penulisan-laporan-kp.pdf
│   ├── administrasi/
│   │   ├── form-persetujuan-dospem.pdf
│   │   ├── form-penilaian-penguji.pdf
│   │   ├── form-penilaian-instansi.pdf
│   │   └── surat-keterangan-selesai-kp.docx
│   └── presentasi/
│       └── template-presentasi-seminar-kp.pptx
└── README.md                           ← File ini
```

---

## Cara Upload Berkas / Template

1. Taruh file (PDF/DOCX/PPTX) ke subfolder yang sesuai di `berkas/`
2. Pastikan nama file **sama persis** dengan yang ada di tabel di bawah
3. Commit dan push ke GitHub — selesai

### Nama File yang Digunakan Website

| Folder | Nama File |
|--------|-----------|
| `berkas/laporan/` | `template-laporan-kp.docx` |
| `berkas/laporan/` | `panduan-penulisan-laporan-kp.pdf` |
| `berkas/administrasi/` | `form-persetujuan-dospem.pdf` |
| `berkas/administrasi/` | `form-penilaian-penguji.pdf` |
| `berkas/administrasi/` | `form-penilaian-instansi.pdf` |
| `berkas/administrasi/` | `surat-keterangan-selesai-kp.docx` |
| `berkas/presentasi/` | `template-presentasi-seminar-kp.pptx` |

> Jika nama file berbeda, tombol **Unduh** akan menampilkan error 404.

---

## Cara Menambah Berkas Baru

Buka `index.html`, cari bagian `const BERKAS = {` lalu tambahkan entri baru:

```js
{
  nama: 'Nama Berkas yang Ditampilkan',
  desc: 'Keterangan singkat berkas ini.',
  ikon: '📄',          // emoji ikon
  kategori: 'Laporan', // Laporan / Administrasi / Penilaian / Presentasi
  tipe: 'PDF',         // PDF / DOCX / PPTX / XLSX
  url: 'berkas/laporan/nama-file.pdf',
},
```

Upload file-nya ke folder yang sesuai, lalu push ke GitHub.

---

## Cara Update Jadwal Seminar

Jadwal dibaca otomatis dari Google Spreadsheet — **tidak perlu sentuh kode**.
Cukup update data di spreadsheet, website akan refresh otomatis tiap 5 menit.

Spreadsheet ID: `1d16ivv6ATY56Ny-SjBjrjyXEJj37fDAuKcYv0wK05wY`

---

## Cara Deploy ke GitHub Pages

1. Push seluruh folder `seminar-kp/` ke repository GitHub
2. **Settings → Pages → Source: Deploy from branch → main / `seminar-kp` folder**
3. Atau letakkan isi folder langsung di root repository
