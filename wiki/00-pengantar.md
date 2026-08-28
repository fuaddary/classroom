# 🏠 Panduan myITS Classroom — Pemrograman Web
### Studi kasus: ET234305 — Departemen Teknologi Informasi, ITS

> Dosen Pengampu: **Fuad Dary Rosyadi, S.Kom., M.Kom.**

Panduan ini berisi **prompt siap pakai untuk AI** (Claude/ChatGPT/Gemini) untuk mengisi setiap komponen myITS Classroom (Moodle), lengkap dengan contoh hasil HTML yang bisa langsung ditempel ke Moodle.

---

## ⚡ Quick Start — 3 Langkah

```
1. Pilih bagian yang ingin diisi dari daftar di bawah
2. Salin prompt yang tersedia → tempel ke AI (lampirkan RPS sebagai konteks)
3. Salin contoh hasil HTML → tempel ke Moodle via ikon </> Edit HTML source
```

> ⚠️ **Selalu verifikasi output AI** — terutama referensi/pustaka, bobot penilaian, dan detail teknis sebelum dipublikasikan ke mahasiswa.

---

## 📚 Daftar Halaman Wiki

### A. Konten Wajib / Anjuran

| # | Halaman | Komponen | Status |
|---|---------|----------|--------|
| 1 | [Identitas & Informasi Umum](01-identitas.md) | Nama MK, SKS, dosen, deskripsi, kontak | 🟢 Wajib |
| 2 | [RPS](02-rps.md) | Ringkasan CPL, CPMK, bahan kajian, evaluasi | 🟢 Wajib |
| 3 | [Kontrak Perkuliahan](03-kontrak.md) | Aturan kehadiran, pengumpulan, integritas akademik | 🟢 Wajib |
| 4 | [Materi per Pertemuan](04-materi.md) | Outline materi, subtopik, poin diskusi | 🟢 Wajib |
| 5 | [Referensi & Bacaan](05-referensi.md) | Kategori referensi, kata kunci pencarian | 🔵 Anjuran |
| 6 | [Rubrik Penilaian](06-rubrik.md) | Kriteria, level capaian, bobot per kriteria | 🟢 Wajib |
| 7 | [Pengumuman](07-pengumuman.md) | Template pengumuman tenggat, info kelas | 🟢 Wajib |
| 8 | [Jadwal & Linimasa](08-linimasa.md) | Tabel linimasa tugas & ujian per minggu | 🟢 Wajib |

### B. Aktivitas Pembelajaran

| # | Halaman | Komponen | Status |
|---|---------|----------|--------|
| 9 | [Forum Diskusi](09-forum.md) | Pertanyaan pemantik + sub-pertanyaan | 🟢 Wajib |
| 10 | [Penugasan (Assignment)](10-assignment.md) | Deskripsi, format, tenggat, rubrik | 🟢 Wajib |
| 11 | [Kuis / Evaluasi Formatif](11-kuis.md) | **7 jenis soal + Moodle XML siap import** | 🟢 Wajib |
| 12 | [Presensi Daring](12-presensi.md) | Kebijakan, batas waktu, konsekuensi | 🔵 Anjuran |
| 13 | [ETS & EAS](13-ets-eas.md) | Kisi-kisi, contoh soal, tabel materi | 🟢 Wajib |
| 14 | [Sesi Sinkron](14-live-session.md) | Agenda 90 menit BigBlueButton/Zoom | 🔵 Anjuran |
| 15 | [Survei & Umpan Balik](15-survei.md) | Skala Likert, pertanyaan terbuka | 🔵 Anjuran |

### C. Referensi & Tips

| Halaman | Isi |
|---------|-----|
| [Tips Prompting Efektif](tips-prompting.md) | 5 prinsip prompting untuk hasil optimal |

---

## 📁 Struktur Repositori

```
classroom/
├── wiki/                       ← Halaman panduan (Anda di sini)
├── moodle-html-per-bagian/     ← 15 file HTML fragment siap tempel Moodle
├── moodle-quiz-xml/            ← 8 file XML soal kuis siap import Moodle
│   ├── 00-bank-soal-lengkap.xml   ← Semua 21 soal dalam 1 file
│   ├── 01-pilihan-ganda.xml
│   ├── 02-checkbox-multi-jawaban.xml
│   ├── 03-mencocokkan.xml
│   ├── 04-benar-salah.xml
│   ├── 05-isian-singkat.xml
│   ├── 06-esai.xml
│   └── 07-drag-drop-teks.xml
├── screenshot-preview/         ← Pratinjau tampilan tiap bagian di Moodle
├── info-kelas-pemrograman-web.html
├── dekorasi-kelas-ti-its.html
└── README.md
```

---

## 🔖 Legenda Status

| Ikon | Arti |
|------|------|
| 🟢 Wajib | Komponen wajib menurut Standar Baku Mutu myITS Classroom 2026 |
| 🔵 Anjuran | Dianjurkan untuk meningkatkan kualitas kelas |
| 🟡 Kondisional | Bergantung pada jenis aktivitas/pertemuan |
