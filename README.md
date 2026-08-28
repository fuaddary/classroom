# 🎓 myITS Classroom — Panduan Prompting AI

> **Pemrograman Web (ET234305)** — Departemen Teknologi Informasi, ITS
> Dosen Pengampu: Fuad Dary Rosyadi, S.Kom., M.Kom.

Kumpulan **prompt AI siap pakai + template HTML + soal XML** untuk mengisi setiap komponen myITS Classroom (Moodle) secara efisien.

---

## ⚡ Quick Start

```
1. Pilih komponen dari tabel di bawah
2. Buka halaman wiki → salin prompt → tempel ke AI (lampirkan RPS)
3. Salin HTML hasil → tempel ke Moodle via ikon </> Edit HTML source
```

> ⚠️ Selalu **verifikasi output AI** — terutama referensi, bobot penilaian, dan detail teknis.

---

## 📚 Wiki — Panduan Per Komponen

### A. Konten Wajib / Anjuran

| # | Komponen | Status | Halaman |
|---|----------|--------|---------|
| 1 | Identitas & Informasi Umum MK | 🟢 Wajib | [→ Buka](wiki/01-identitas.md) |
| 2 | RPS (Ringkasan Navigasi) | 🟢 Wajib | [→ Buka](wiki/02-rps.md) |
| 3 | Kontrak Perkuliahan / Tata Tertib | 🟢 Wajib | [→ Buka](wiki/03-kontrak.md) |
| 4 | Materi Pembelajaran per Pertemuan | 🟢 Wajib | [→ Buka](wiki/04-materi.md) |
| 5 | Referensi & Bacaan Tambahan | 🔵 Anjuran | [→ Buka](wiki/05-referensi.md) |
| 6 | Rubrik Penilaian | 🟢 Wajib | [→ Buka](wiki/06-rubrik.md) |
| 7 | Pengumuman | 🟢 Wajib | [→ Buka](wiki/07-pengumuman.md) |
| 8 | Jadwal & Linimasa Perkuliahan | 🟢 Wajib | [→ Buka](wiki/08-linimasa.md) |

### B. Aktivitas Pembelajaran

| # | Komponen | Status | Halaman |
|---|----------|--------|---------|
| 9 | Forum Diskusi | 🟢 Wajib | [→ Buka](wiki/09-forum.md) |
| 10 | Penugasan (Assignment) | 🟢 Wajib | [→ Buka](wiki/10-assignment.md) |
| 11 | Kuis / Evaluasi Formatif ⭐ | 🟢 Wajib | [→ Buka](wiki/11-kuis.md) |
| 12 | Presensi Daring | 🔵 Anjuran | [→ Buka](wiki/12-presensi.md) |
| 13 | ETS & EAS | 🟢 Wajib | [→ Buka](wiki/13-ets-eas.md) |
| 14 | Sesi Sinkron (Live Session) | 🔵 Anjuran | [→ Buka](wiki/14-live-session.md) |
| 15 | Survei & Umpan Balik | 🔵 Anjuran | [→ Buka](wiki/15-survei.md) |

### C. Referensi

| Halaman | Isi |
|---------|-----|
| [Tips Prompting Efektif](wiki/tips-prompting.md) | 5 prinsip prompting + alur kerja yang direkomendasikan |
| [Pengantar Wiki](wiki/00-pengantar.md) | Gambaran umum & struktur repositori |

---

## 🎮 Soal Kuis — Moodle XML (7 Jenis)

Direktori [`moodle-quiz-xml/`](moodle-quiz-xml/) berisi soal-soal siap import ke bank soal Moodle.

| File | Jenis Soal | Jumlah Soal |
|------|-----------|-------------|
| [`00-bank-soal-lengkap.xml`](moodle-quiz-xml/00-bank-soal-lengkap.xml) | **Semua jenis (gabungan)** | **21 soal** |
| [`01-pilihan-ganda.xml`](moodle-quiz-xml/01-pilihan-ganda.xml) | Pilihan Ganda (radio button) | 3 soal |
| [`02-checkbox-multi-jawaban.xml`](moodle-quiz-xml/02-checkbox-multi-jawaban.xml) | Checkbox / Multi-Jawaban | 2 soal |
| [`03-mencocokkan.xml`](moodle-quiz-xml/03-mencocokkan.xml) | Mencocokkan (Matching) | 3 soal |
| [`04-benar-salah.xml`](moodle-quiz-xml/04-benar-salah.xml) | Benar / Salah (True/False) | 5 soal |
| [`05-isian-singkat.xml`](moodle-quiz-xml/05-isian-singkat.xml) | Isian Singkat (Short Answer) | 4 soal |
| [`06-esai.xml`](moodle-quiz-xml/06-esai.xml) | Esai (dengan rubrik & template) | 2 soal |
| [`07-drag-drop-teks.xml`](moodle-quiz-xml/07-drag-drop-teks.xml) | Drag & Drop ke Teks | 2 soal |

**Cara import:** Moodle → Admin → Bank Soal → Import → Format: **Moodle XML** → Upload → Import

---

## 🗂️ Struktur Repositori

```
classroom/
├── README.md                   ← Anda di sini (hub navigasi)
├── wiki/                       ← 17 halaman panduan terstruktur
│   ├── 00-pengantar.md
│   ├── 01-identitas.md … 15-survei.md
│   └── tips-prompting.md
├── moodle-html-per-bagian/     ← 15 file HTML fragment siap tempel Moodle
├── moodle-quiz-xml/            ← 8 file XML soal kuis siap import
├── screenshot-preview/         ← Pratinjau tampilan tiap bagian
├── info-kelas-pemrograman-web.html
├── info-kelas-pemrograman-web-moodle.html
└── dekorasi-kelas-ti-its.html
```

---

## 📖 Cara Pakai File HTML di Moodle

1. Buka file `.html` di `moodle-html-per-bagian/` → salin semua isinya.
2. Di Moodle, buka Label / Page / Forum / Assignment yang relevan.
3. Klik ikon **`</>` Edit HTML source** di toolbar editor (Atto/TinyMCE).
4. Tempel kode HTML → klik Update/Save.

> Jangan tempel langsung ke area teks biasa — Moodle akan membersihkan/merusak markup.

---

🟢 Wajib · 🔵 Anjuran · 🟡 Kondisional — sesuai *Standar Baku Mutu Konten & Aktivitas Pembelajaran myITS Classroom (2026)*
