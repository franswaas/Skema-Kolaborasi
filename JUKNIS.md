# Petunjuk Teknis — Skema Kolaborasi

> Dokumen ini menjelaskan cara penggunaan, pengembangan, dan berbagi aplikasi Skema Kolaborasi secara lengkap.

---

## Daftar Isi

1. [Pendahuluan](#1-pendahuluan)
2. [Cara Menjalankan](#2-cara-menjalankan)
3. [Antarmuka & Navigasi](#3-antarmuka--navigasi)
4. [Fitur Utama](#4-fitur-utama)
5. [Sistem Validasi](#5-sistem-validasi)
6. [Ekspor & Simpan](#6-ekspor--simpan)
7. [Pemilihan Icon](#7-pemilihan-icon)
8. [Berbagi ke Orang Lain](#8-berbagi-ke-orang-lain)
9. [Pengembangan Lanjutan](#9-pengembangan-lanjutan)
10. [Troubleshooting](#10-troubleshooting)

---

## 1. Pendahuluan

**Skema Kolaborasi** adalah aplikasi web untuk memetakan dan menganalisis hubungan kolaboratif antar-stakeholder dalam suatu program atau proyek pembangunan.

### Konsep SHP & SHF

| Istilah | Kepanjangan | Peran | Posisi |
|---|---|---|---|
| **SHP** | Stakeholder Pengelola | Pihak utama yang mengelola program | Di dalam kotak biru |
| **SHF** | Stakeholder Fasilitator | Pihak pendukung sumber daya/regulasi | Di luar kotak |

### Jenis Aliran Sumber Daya

| Jenis | Warna | Contoh |
|---|---|---|
| Finansial | Hijau | Dana hibah, kredit, pajak, retribusi |
| Non-Fin Tangible | Biru | Lahan, peralatan, infrastruktur |
| Non-Fin Intangible | Oranye | Pelatihan, izin, pengetahuan |
| Barang Publik | Ungu (putus-putus) | Layanan publik, manfaat sosial |
| Eksternalitas | Merah (titik-titik) | Polusi, dampak negatif |

---

## 2. Cara Menjalankan

### Persyaratan

- Browser: Chrome 90+, Firefox 88+, atau Edge 90+ (rekomendasi: Chrome terbaru)
- Tidak perlu instalasi, tidak perlu internet setelah pertama kali dibuka

> **Catatan:** Saat pertama dibuka, browser mengunduh font dari Google Fonts dan library html2canvas. Setelahnya bisa digunakan offline.

### Langkah

1. Unduh file `index.html`
2. Klik dua kali untuk membuka di browser
3. Aplikasi langsung siap digunakan

---

## 3. Antarmuka & Navigasi

### Tata Letak

| Area | Fungsi |
|---|---|
| **Header (atas)** | Logo, tombol fase, status simpan, bahasa, tombol aksi |
| **Panel Kiri** | Tab: SH · Aliran · Grup · Template |
| **Kanvas Tengah** | Area gambar node dan aliran |
| **Panel Kanan** | Tab: Info · Nilai · Chart · Skenario · Waktu · Valid |

### Shortcut Keyboard

| Tombol | Fungsi |
|---|---|
| `V` | Mode pilih/seleksi |
| `C` | Mode hubungkan node |
| `F` | Fit view |
| `Space` (tahan) | Pan kanvas |
| `Del` | Hapus yang dipilih |
| `Esc` | Batalkan / batal pilih |
| `Scroll` | Zoom in/out |

---

## 4. Fitur Utama

### 4.1 Menambah Stakeholder

1. Panel kiri → tab **SH** → klik **+ Tambah Stakeholder**
2. Isi: Nama, Icon, Tipe, Peran (SHP/SHF), Nilai Kontribusi (Rp), Fase Aktif
3. Klik **Simpan** — node muncul di kanvas, bisa digeser

### 4.2 Menambah Aliran

**Cara 1:** Klik node → klik tombol "↔ Hubungkan" → klik node tujuan → isi form

**Cara 2:** Tekan `C` → klik node sumber → klik node tujuan → isi form

### 4.3 Fase Kolaborasi

| Fase | Keterangan |
|---|---|
| **Pra-Kolaborasi** | Penjajakan, MoU, persiapan |
| **Operasi** | Pelaksanaan aktif, transaksi berjalan |
| **Pasca** | Evaluasi, distribusi akhir, laporan |

Node yang redup di suatu fase = stakeholder tidak aktif di fase tersebut.

### 4.4 Template

12 template tersedia di tab **Template** (panel kiri), dari skala Kecil (3 SH) hingga Sangat Besar (12 SH). Muat template lalu edit sesuai kebutuhan.

### 4.5 Auto-Layout

Di tab Grup: tersedia 4 layout otomatis — Lingkaran, Hierarki, Force, Grid.

---

## 5. Sistem Validasi

Validasi berjalan otomatis. Badge di bawah kanvas menunjukkan status:
- ✅ **Skema Valid** — semua kaidah terpenuhi
- ⚠ **N peringatan** — perlu diperhatikan
- ❌ **N error** — perlu diperbaiki

### 8 Kaidah yang Dicek

1. Ada minimal 1 SHP
2. Ada minimal 1 SHF
3. Semua SH terhubung (punya aliran)
4. Aliran tertutup (SHP beri dan terima)
5. Label aliran terisi
6. Nilai diterima ≥ dikeluarkan (rasio ≥ 1)
7. Proporsi sharing = 100%
8. Fase kolaborasi terdefinisi

> **Pengecualian rasio:** Stakeholder tipe `Pemerintah` dan `Masyarakat/Publik` dikecualikan dari cek rasio karena sifatnya yang memberi tanpa mengharapkan imbalan finansial langsung.

---

## 6. Ekspor & Simpan

### Menyimpan Proyek

Klik **💾 Simpan** → file `.json` terunduh. Buka kembali dengan **📂 Buka**.

> Tidak ada autosave — simpan secara manual secara berkala.

### Format Ekspor

| Format | Kegunaan |
|---|---|
| **JSON** | Backup / berbagi proyek untuk dilanjutkan |
| **PNG** | Presentasi, laporan (resolusi 2×, full canvas) |
| **JPEG** | Berbagi cepat, ukuran lebih kecil |
| **Laporan HTML** | Dokumentasi penelitian |

---

## 7. Pemilihan Icon

Klik area **Icon** di form stakeholder → panel picker terbuka.

### Kategori Emoji
- 🏛 **Gov** — pemerintahan, gedung, lembaga
- 🏢 **Bisnis** — korporat, keuangan, teknologi  
- 🤝 **Sosial** — komunitas, lingkungan
- 🎓 **Edu** — pendidikan, riset, sains
- 🏗 **Infra** — infrastruktur, transportasi

### Upload Gambar Lokal

Tab **📁 Upload** → klik area upload → pilih gambar (PNG/JPG/SVG/WebP/GIF, maks 500KB).

Gambar disimpan sebagai base64 di dalam file `.json` — tidak perlu file eksternal.

---

## 8. Berbagi ke Orang Lain

### Berbagi Aplikasi

Kirim file `index.html` → penerima buka di browser → langsung bisa digunakan.

### Berbagi Skema

1. Klik 💾 Simpan → unduh file `.json`
2. Kirim `index.html` + file `.json` ke penerima
3. Penerima buka `index.html` → klik 📂 Buka → pilih `.json`

### Hosting Online (GitHub Pages)

1. Fork/upload repository ini ke GitHub
2. Settings → Pages → Source: `main` branch → Save
3. Aplikasi tersedia di: `https://username.github.io/skema-kolaborasi`
4. Bagikan URL — siapapun bisa akses tanpa mengunduh

---

## 9. Pengembangan Lanjutan

### Menambah Template Baru

Buka `index.html` dengan text editor. Cari `const TEMPLATES = [`. Tambahkan objek:

```javascript
{
  scale: 'kecil',          // kecil | menengah | besar | sangat_besar
  scaleLabel: '🟢 Kecil',
  nameID: 'Nama Template',
  nameEN: 'Template Name',
  descID: 'Deskripsi singkat',
  icon: '🏘',
  nodes: [
    {
      name: 'Nama Stakeholder',
      type: 'pemerintah',  // pemerintah|swasta|ngo|akademisi|komunitas|publik
      role: 'shp',         // shp | shf
      resources: 'Sumber daya yang dikontribusikan',
      interest: 'Kepentingan/manfaat yang diharapkan',
      valRp: 50000000,
      phases: { 0: true, 1: true, 2: false },
      icon: '🏛'
    },
    // node lainnya...
  ],
  flows: [
    {
      fromId: 0,           // index node sumber (mulai dari 0)
      toId: 1,             // index node tujuan
      label: 'Dana hibah',
      type: 'financial',   // financial|tangible|intangible|public|eksternalitas
      dir: 'one',          // one | two
      valRp: 30000000,
      phases: { 0: true, 1: true, 2: false }
    },
    // aliran lainnya...
  ]
},
```

### Mengubah Warna Tema

Edit variabel CSS di bagian `:root { ... }` di awal file:

```css
:root {
  --bg: #0a0e1a;          /* Warna latar belakang */
  --accent: #00d4aa;      /* Warna aksen utama (hijau toska) */
  --blue: #3b82f6;        /* Warna biru */
  /* dst... */
}
```

---

## 10. Troubleshooting

| Masalah | Solusi |
|---|---|
| Aplikasi tidak terbuka | Gunakan Chrome/Firefox versi terbaru |
| Font tidak tampil | Buka sekali dengan koneksi internet |
| Export gambar terpotong | Pastikan menggunakan versi 2.0+ |
| Icon picker tidak terbuka | Pastikan menggunakan versi 2.0+ |
| File `.json` tidak bisa dibuka | File harus valid JSON dan mengandung field `nodes` |
| Error rasio terus muncul | Tambah aliran balik realistis (pajak, return investasi) |
| Proporsi tidak 100% | Cek nilai Rp — v2.0 sudah ada toleransi ±0.01% otomatis |
| Performa lambat | Gunakan Chrome, tutup tab lain |

---

*Skema Kolaborasi v2.0 · Dikembangkan oleh Frans Waas · 2026*
