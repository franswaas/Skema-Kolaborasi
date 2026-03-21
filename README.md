# 🤝 Skema Kolaborasi

**Aplikasi web untuk memetakan, menganalisis, dan memvisualisasikan hubungan kolaboratif antar-stakeholder dalam suatu proyek atau program pembangunan.**

> Dikembangkan oleh **Frans Waas** · Versi 2.0 · 2026

---

## ✨ Fitur Utama

- 🗺 **Kanvas interaktif** — drag, zoom, pan, auto-layout
- 👥 **Manajemen stakeholder** — SHP (pengelola) & SHF (fasilitator) dengan 6 tipe sektor
- ↔ **Aliran sumber daya** — 5 jenis: Finansial, Tangible, Intangible, Barang Publik, Eksternalitas
- 📅 **Fase kolaborasi** — Pra-Kolaborasi, Operasi, Pasca
- ✅ **Validasi otomatis** — 8 kaidah kolaborasi dicek real-time
- 💰 **Analisis nilai** — rasio, net value, proporsi, skenario simulasi
- 📊 **12 template** siap pakai (4 skala: Kecil hingga Sangat Besar)
- 🖼 **Icon picker** — 200+ emoji + upload gambar lokal
- ⬇ **Export** — PNG, JPEG (full canvas), JSON, Laporan HTML
- 🌐 **Bilingual** — Indonesia & Inggris
- 📴 **100% offline** — tidak perlu server atau database

---

## 🚀 Cara Menggunakan

### Opsi 1 — Langsung dari browser (termudah)

1. Unduh file [`index.html`](index.html)
2. Klik dua kali untuk membuka di browser
3. Selesai — tidak perlu instalasi apapun

### Opsi 2 — GitHub Pages (akses online)

Setelah fork/clone repository ini:

1. Buka **Settings** → **Pages**
2. Source: `main` branch → folder `/` (root)
3. Klik **Save**
4. Aplikasi tersedia di: `https://username.github.io/skema-kolaborasi`

---

## 📁 Struktur Repository

```
skema-kolaborasi/
├── index.html          # Aplikasi utama (self-contained)
├── README.md           # Dokumentasi ini
├── JUKNIS.md           # Petunjuk teknis lengkap
├── CHANGELOG.md        # Riwayat perubahan
├── LICENSE             # Lisensi MIT
└── docs/
    └── juknis.html     # Juknis versi HTML (bisa dicetak)
```

---

## 🏗 Teknologi

| Komponen | Teknologi |
|---|---|
| Bahasa | HTML5, CSS3, Vanilla JavaScript |
| Visualisasi | SVG + CSS Transform |
| Export gambar | [html2canvas](https://html2canvas.hertzen.com/) v1.4.1 |
| Font | Google Fonts (Syne, Mulish, JetBrains Mono) |
| Penyimpanan | File JSON lokal |
| Server/Backend | **Tidak ada** |

> Seluruh aplikasi terdapat dalam **satu file HTML** — tidak ada dependensi eksternal yang perlu diinstal.

---

## 📖 Konsep Dasar

### Stakeholder
| Istilah | Peran | Posisi |
|---|---|---|
| **SHP** (Stakeholder Pengelola) | Mengelola & mengoperasikan program | Dalam kotak biru |
| **SHF** (Stakeholder Fasilitator) | Menyediakan sumber daya/regulasi | Luar kotak |

### Jenis Aliran
| Jenis | Warna | Contoh |
|---|---|---|
| Finansial | Hijau `——` | Dana hibah, kredit, pajak |
| Non-Fin Tangible | Biru `——` | Lahan, peralatan, infrastruktur |
| Non-Fin Intangible | Oranye `——` | Pelatihan, izin, pengetahuan |
| Barang Publik | Ungu `- - -` | Layanan publik, manfaat bersama |
| Eksternalitas | Merah `····` | Polusi, dampak negatif |

---

## 🗂 Template yang Tersedia

| Skala | Template | Jumlah SH |
|---|---|---|
| 🟢 Kecil | Usaha Mikro & Pembina | 3 |
| 🟢 Kecil | Petani & Tengkulak Koperatif | 3 |
| 🟢 Kecil | CSR Perusahaan & Komunitas | 4 |
| 🟡 Menengah | Sentra Industri Batik | 6 |
| 🟡 Menengah | Pariwisata Berbasis Komunitas | 6 |
| 🟡 Menengah | Kolaborasi Riset Kampus-Industri | 6 |
| 🟡 Menengah | Pengelolaan Sampah Terpadu | 6 |
| 🔴 Besar | KPBU/PPP Infrastruktur | 6 |
| 🔴 Besar | Value Chain Komoditas Pertanian | 10 |
| 🔴 Besar | Ekosistem Start-up Daerah | 8 |
| 🟣 Sangat Besar | Kawasan Industri Terpadu | 12 |
| 🟣 Sangat Besar | Pengembangan Wilayah Terpadu | 12 |

---

## ⌨ Shortcut Keyboard

| Tombol | Fungsi |
|---|---|
| `V` | Mode pilih |
| `C` | Mode hubungkan |
| `F` | Fit view (semua node terlihat) |
| `Space` (tahan) | Pan kanvas |
| `Del` | Hapus yang dipilih |
| `Esc` | Batalkan / batal pilih |
| `Scroll` | Zoom in/out |

---

## 🤝 Kontribusi

Kontribusi sangat disambut! Silakan:

1. Fork repository ini
2. Buat branch baru: `git checkout -b fitur/nama-fitur`
3. Commit perubahan: `git commit -m 'Tambah fitur X'`
4. Push: `git push origin fitur/nama-fitur`
5. Buat Pull Request

### Ide pengembangan
- [ ] Mode presentasi (full-screen tanpa UI)
- [ ] Export ke PDF langsung
- [ ] Kolaborasi real-time (multi-user)
- [ ] Integrasi data dari spreadsheet (CSV/Excel)
- [ ] Versi mobile (responsive)

---

## 📄 Lisensi

Didistribusikan di bawah **Lisensi MIT**. Lihat [`LICENSE`](LICENSE) untuk detail.

---

## 👤 Pengembang

**Frans Waas**

---

*Dibuat dengan ❤ untuk mendukung penelitian dan perencanaan kolaborasi multi-stakeholder*
