# Changelog

Semua perubahan penting pada proyek ini didokumentasikan di sini.

Format mengikuti [Keep a Changelog](https://keepachangelog.com/id/1.0.0/).

---

## [2.0.0] - 2026-03-21

### Ditambahkan
- Icon picker lengkap dengan 5 kategori emoji (200+ ikon)
- Upload gambar lokal sebagai icon node (PNG/JPG/SVG/WebP/GIF, maks 500KB)
- 12 template siap pakai (4 skala: Kecil, Menengah, Besar, Sangat Besar)
- Aliran balik pajak/retribusi di semua template (konsistensi model kolaborasi)
- Panel validasi dengan saran perbaikan per error
- Penjelasan fase kolaborasi di tab Validasi
- Indikator status simpan di header (Tersimpan / Belum tersimpan)
- Logo kustom dan kredit pengembang di header
- Recalculate `nextId` dari max ID setelah load JSON (mencegah ID duplikat)
- `scenarioMult` di-reset saat buka proyek baru
- `sh_other_total` breakdown proporsi SH lain di form

### Diperbaiki
- **Export PNG/JPEG**: gambar tidak lagi terpotong — mencakup seluruh node di kanvas
- **Export PNG/JPEG**: label aliran (`fl.label`) kini tampil di gambar hasil export
- **Icon picker**: panel tidak lagi terpotong oleh overflow modal
- **Icon picker**: panel dipindahkan ke luar DOM modal untuk menghindari clipping z-index
- **Icon picker**: menutup otomatis saat modal SH ditutup
- **Proporsi floating point**: `100.0100...%` tidak lagi memicu warning palsu (toleransi ±0.01%)
- **recalcProportions**: menggunakan teknik "last node gets remainder" — total selalu tepat 100%
- Autosave dihapus — simpan hanya saat user klik 💾 manual
- Tab panel kanan tidak lagi terpotong (dibagi 2 baris dengan ikon)
- Judul halaman browser diperbarui menjadi "Skema Kolaborasi"

### Diubah
- Logika validasi rasio: tipe `pemerintah` dan `publik` dikecualikan dari cek rasio < 1
- `openProject` sekarang menghitung ulang `nextId` dari max ID aktual
- `closeModal` sekarang juga menutup icon picker

---

## [1.0.0] - 2025

### Rilis Awal
- Kanvas interaktif dengan drag, zoom, pan
- Manajemen stakeholder SHP & SHF
- 5 jenis aliran sumber daya
- 3 fase kolaborasi
- Validasi dasar
- Export PNG, JPEG, JSON, HTML
- Dukungan bahasa Indonesia & Inggris
- Template awal
