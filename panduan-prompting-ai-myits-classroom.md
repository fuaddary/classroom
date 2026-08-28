# Panduan Prompting AI untuk Mengisi Konten myITS Classroom
### Studi kasus: Pemrograman Web (ET234305) — Departemen Teknologi Informasi, ITS

Panduan ini berisi prompt siap pakai untuk setiap komponen **wajib/anjuran/kondisional** pada *Standar Baku Mutu Konten & Aktivitas Pembelajaran myITS Classroom (2026)*, lengkap dengan contoh hasil. Alur kerjanya: **tempel prompt ke AI (Claude/ChatGPT/dst) → tempel RPS sebagai lampiran/konteks → edit hasilnya → unggah ke myITS Classroom.**

> ⚠️ **Prinsip penting:** AI membantu menyusun draf dan mempercepat kerja, tapi dosen tetap wajib memverifikasi — terutama untuk referensi/pustaka (AI bisa mengarang judul/tautan), angka bobot penilaian, dan ketepatan materi teknis sebelum dipublikasikan ke mahasiswa.

---

## Daftar Isi

**A. Konten Wajib/Anjuran (Bagian 2.1)**
1. [Identitas & Informasi Umum Mata Kuliah](#1-identitas--informasi-umum-mata-kuliah)
2. [RPS](#2-rps-rencana-pembelajaran-semester)
3. [Kontrak Perkuliahan / Tata Tertib](#3-kontrak-perkuliahan--tata-tertib-kelas)
4. [Materi Pembelajaran per Pertemuan](#4-materi-pembelajaran-per-pertemuan)
5. [Referensi / Bacaan Tambahan](#5-referensi--bacaan-tambahan)
6. [Rubrik Penilaian](#6-rubrik-penilaian)
7. [Pengumuman](#7-pengumuman)
8. [Jadwal & Linimasa Perkuliahan](#8-jadwal--linimasa-perkuliahan)

**B. Aktivitas Pembelajaran (Bagian 2.2)**
9. [Forum Diskusi](#9-forum-diskusi)
10. [Penugasan (Assignment)](#10-penugasan-assignment)
11. [Kuis / Evaluasi Formatif](#11-kuis--evaluasi-formatif)
12. [Presensi Daring](#12-presensi-daring)
13. [ETS & EAS](#13-ets--eas)
14. [Sesi Sinkron (Live Session)](#14-sesi-sinkron-live-session)
15. [Survei / Umpan Balik](#15-survei--umpan-balik)

---

## A. Konten Wajib/Anjuran

### 1. Identitas & Informasi Umum Mata Kuliah

**Prompt:**
```
Saya dosen pengampu MK "Pemrograman Web" (ET234305) di Departemen Teknologi
Informasi ITS. Berikut RPS mata kuliah saya [tempel/lampirkan RPS].

Buatkan blok "Identitas & Informasi Umum Mata Kuliah" untuk halaman utama
myITS Classroom, mencakup: nama MK, kode, SKS, dosen pengampu, deskripsi
singkat (maks. 3 kalimat, bahasa mudah dipahami mahasiswa), dan format
kontak/jam konsultasi. Tulis dalam format yang siap tempel ke Moodle (teks
biasa, bukan HTML).
```

**Contoh hasil:**
```
Pemrograman Web (ET234305) — 4 SKS (T=3, P=1)
Dosen Pengampu: Fuad Dary Rosyadi, S.Kom., M.Kom.

Mata kuliah ini membahas konsep, teknologi, dan keterampilan untuk
mengembangkan aplikasi web modern — mulai dari HTML, CSS, dan JavaScript,
hingga framework front-end/server-side, manajemen data, dan hosting.
Mahasiswa akan berlatih membangun aplikasi web interaktif dan responsif
melalui praktikum dan proyek CRUD.

Kontak & Jam Konsultasi: [rosyadi@its.ac.id] · [Hari, jam, ruang/tautan]
```

---

### 2. RPS (Rencana Pembelajaran Semester)

**Prompt:**
```
Berikut file RPS resmi MK Pemrograman Web [lampirkan PDF/DOCX RPS].

Tolong buatkan ringkasan RPS dalam bentuk poin-poin terstruktur untuk
ditampilkan di section pengantar myITS Classroom (bukan menggantikan
dokumen RPS aslinya, hanya ringkasan navigasi): CPL yang dibebankan, daftar
CPMK, daftar materi pembelajaran (bahan kajian), dan komponen evaluasi
beserta bobotnya. Format markdown dengan heading per bagian.
```

**Contoh hasil:**
```markdown
## Ringkasan RPS — Pemrograman Web

**CPL yang dibebankan:** CPL-3 — Mampu menyelesaikan masalah dengan
mengimplementasikan TIK, memperhatikan prinsip keberlanjutan, serta
memahami kewirausahaan berbasis teknologi.

**CPMK:**
- CPMK-1 — Menjelaskan konsep pemrograman web (bobot 10%)
- CPMK-2 — Menganalisis permasalahan dengan pendekatan web (bobot 40%)
- CPMK-3 — Memodelkan solusi dengan pendekatan aplikasi web (bobot 40%)
- CPMK-4 — Mengimplementasikan & menghosting aplikasi web (bobot 10%)

**Bahan Kajian:**
HTML · CSS · Bootstrap · JavaScript · DOM · AJAX · Vue.js · Hosting ·
Front-End · Back-End · CRUD · Data & Query · Report

**Komponen Evaluasi:** Tugas 1 (30%) · ETS (20%) · Tugas 2 (25%) · EAS (25%)

📄 Dokumen RPS lengkap: [tautan/file RPS]
```

---

### 3. Kontrak Perkuliahan / Tata Tertib Kelas

**Prompt:**
```
Buatkan draf kontrak perkuliahan / tata tertib kelas untuk MK Pemrograman
Web di ITS (kelas dengan komponen praktikum), mencakup: aturan kehadiran,
etika kelas, kebijakan keterlambatan pengumpulan tugas/source code, dan
sanksi akademik (pelanggaran integritas akademik/plagiarisme kode).
Gaya bahasa formal tapi tidak kaku, maksimal 6 poin, siap tempel ke
myITS Classroom.
```

**Contoh hasil:**
```
1. Kehadiran minimal 80% dari total pertemuan (termasuk praktikum) untuk
   dapat mengikuti EAS.
2. Toleransi keterlambatan masuk kelas/praktikum: 15 menit.
3. Tugas dan source code dikumpulkan melalui myITS Classroom sebelum
   tenggat; keterlambatan dikenai pengurangan nilai 5% per hari, maksimal
   3 hari.
4. Laptop wajib dibawa saat sesi praktikum.
5. Plagiarisme kode (menyalin penuh milik orang lain tanpa modifikasi/
   pemahaman) diproses sesuai peraturan akademik ITS yang berlaku.
6. Pertanyaan teknis di luar jam kelas disampaikan melalui forum diskusi
   atau kanal resmi kelas, dijawab maksimal dalam 2x24 jam kerja.
```

---

### 4. Materi Pembelajaran per Pertemuan

**Prompt:**
```
Berdasarkan RPS minggu ke-6 dengan topik "Membuat Aplikasi Web dengan
JavaScript dan DOM" (sub-CPMK: mahasiswa mampu mengimplementasikan
JavaScript dan DOM untuk membuat aplikasi web), buatkan outline
materi/slide untuk pertemuan ini: judul section Moodle, 4-6 subtopik
berurutan, dan 1 poin diskusi pemantik di akhir. Format markdown dengan
heading.
```

**Contoh hasil:**
```markdown
## Pertemuan 6 — Membuat Aplikasi Web dengan JavaScript & DOM

1. Recap: sintaks dasar JavaScript dan struktur DOM
2. Manipulasi elemen DOM (selecting, modifying, event listener)
3. Menghubungkan JavaScript dengan elemen HTML/CSS
4. Studi kasus: membuat form interaktif dengan validasi sederhana
5. Hands-on praktikum: aplikasi web sederhana berbasis JavaScript & DOM
6. **Poin diskusi:** Kapan sebaiknya manipulasi DOM dilakukan langsung
   dengan JavaScript murni, dan kapan sebaiknya menggunakan framework
   seperti Vue.js?

📎 Sumber belajar: [slide/PDF pertemuan 6], [modul praktikum JavaScript & DOM]
```

---

### 5. Referensi & Bacaan Tambahan

**Prompt:**
```
Untuk topik "JavaScript dan DOM" pada MK Pemrograman Web, sarankan 3
kategori referensi tambahan (dokumentasi resmi, artikel/tutorial teknis,
dan studi kasus industri) beserta alasan singkat relevansinya. JANGAN
mengarang judul/penulis/tautan spesifik — beri kategori dan kata kunci
pencarian saja agar saya cari & verifikasi sendiri sumber aslinya.
```

**Contoh hasil:**
```
1. Dokumentasi resmi — cari: "MDN Web Docs JavaScript DOM manipulation"
   → acuan sintaks & API DOM yang selalu diperbarui.
2. Artikel/tutorial teknis — cari: "JavaScript DOM event handling best
   practices" → pola penulisan kode yang lebih rapi.
3. Studi kasus industri — cari studi kasus performa web (mis. penggunaan
   Vanilla JS vs framework) di blog engineering perusahaan teknologi →
   konteks penerapan nyata.

⚠️ Semua judul, penulis, dan tautan di atas perlu dicari & diverifikasi
manual sebelum dicantumkan ke myITS Classroom.
```

---

### 6. Rubrik Penilaian

**Prompt:**
```
Buatkan rubrik penilaian untuk Tugas 2 MK Pemrograman Web (topik: aplikasi
web sederhana dengan CRUD, bobot 25% dari nilai akhir). 4 kriteria
penilaian, 4 level capaian (Kurang/Cukup/Baik/Sangat Baik), dan bobot
skor tiap kriteria. Format tabel markdown.
```

**Contoh hasil:**
```markdown
| Kriteria                      | Bobot | Kurang (1)        | Cukup (2)            | Baik (3)                | Sangat Baik (4)                        |
|--------------------------------|-------|---------------------|------------------------|---------------------------|-------------------------------------------|
| Fungsionalitas CRUD lengkap    | 35%   | <2 fungsi jalan     | 2–3 fungsi jalan       | Semua fungsi jalan        | Semua fungsi jalan + validasi input       |
| Struktur kode & database       | 25%   | Tidak terstruktur   | Cukup terstruktur      | Terstruktur rapi          | Terstruktur & mengikuti best practice     |
| Tampilan front-end             | 20%   | Tidak responsif     | Sebagian responsif     | Responsif                 | Responsif & estetik                       |
| Ketepatan waktu                | 20%   | Terlambat >3 hari   | Terlambat 1–3 hari     | Tepat waktu                | Lebih awal                                |
```

---

### 7. Pengumuman

**Prompt:**
```
Buatkan draf pengumuman untuk forum Announcement myITS Classroom MK
Pemrograman Web, isinya: pengingat tenggat Tugas 1 (H-3, proyek halaman
web HTML & CSS), nada profesional tapi ramah, sertakan poin teknis apa
saja yang wajib ada dalam proyek. Maksimal 100 kata.
```

**Contoh hasil:**
```
📢 Pengingat: Tenggat Tugas 1 — 3 Hari Lagi

Halo semua, Tugas 1 (Membuat Halaman Web Sederhana dengan HTML & CSS)
akan ditutup pada [tanggal, jam]. Pastikan proyek kalian memuat: (1)
struktur HTML semantik, (2) styling CSS (layout, warna, tipografi), (3)
tampilan responsif dasar, dan (4) source code rapi dengan komentar.
Unggah dalam format ZIP/repository melalui menu Assignment di myITS
Classroom.

Ada kendala? Silakan tulis di Forum Diskusi ya. Semangat coding! 💻
```

---

### 8. Jadwal & Linimasa Perkuliahan

**Prompt:**
```
Berdasarkan RPS 16 minggu MK Pemrograman Web [lampirkan RPS], susun tabel
linimasa yang menandai minggu mana saja ada tenggat tugas/ujian beserta
bobotnya, untuk ditempel di section pengantar myITS Classroom. Format
tabel markdown.
```

**Contoh hasil:**
```markdown
| Minggu | Aktivitas                | Bobot |
|--------|----------------------------|-------|
| 2      | Tugas 1 dibuka (HTML)      | 10%   |
| 3      | Tugas 1 lanjutan (CSS)     | 10%   |
| 6      | Tugas 1 ditutup (JS & DOM) | 10%   |
| 8      | ETS (Evaluasi 1)           | 20%   |
| 13     | Tugas 2 ditutup (CRUD)     | 25%   |
| 16     | EAS (Evaluasi 2)           | 25%   |
```

---

## B. Aktivitas Pembelajaran

### 9. Forum Diskusi

**Prompt:**
```
Buatkan 1 topik forum diskusi untuk materi "JavaScript dan DOM" (minggu
5–6), berupa 1 pertanyaan pemantik utama + 2 sub-pertanyaan pendukung
yang mendorong mahasiswa berargumen, bukan sekadar menjawab definisi.
```

**Contoh hasil:**
```
💻 Diskusi Minggu 5–6 — JavaScript & DOM

Pertanyaan utama: Dalam kasus apa memanipulasi DOM langsung dengan
JavaScript lebih masuk akal dibanding memakai framework seperti Vue.js,
dan sebaliknya?

- Sub-pertanyaan 1: Apa risiko performa jika manipulasi DOM dilakukan
  berlebihan tanpa framework?
- Sub-pertanyaan 2: Fitur reactive data binding pada framework
  menyelesaikan masalah apa yang sulit ditangani JavaScript murni?

Balas minimal 1 argumen orisinal + 1 tanggapan ke argumen teman sekelas.
```

---

### 10. Penugasan (Assignment)

**Prompt:**
```
Buatkan instruksi lengkap Tugas 1 MK Pemrograman Web (topik: halaman web
sederhana dengan HTML & CSS, bobot 30%), mencakup: deskripsi tugas,
format pengumpulan, dan tenggat. Gunakan rubrik penilaian yang sudah
dibuat sebelumnya sebagai acuan kriteria.
```

**Contoh hasil:**
```
📌 Tugas 1 — Halaman Web Sederhana dengan HTML & CSS (Bobot: 30%)

Deskripsi:
Bangun 1 halaman web profil/portofolio sederhana menggunakan HTML dan
CSS murni (boleh memanfaatkan Bootstrap pada bagian layout). Halaman
wajib memuat: header/navigasi, bagian konten utama (minimal 2 section),
dan footer, dengan tampilan responsif dasar (desktop & mobile).

Format pengumpulan: ZIP source code atau tautan repository, melalui menu
Assignment.
Tenggat: [tanggal, jam] — minggu ke-6.
Penilaian: mengikuti rubrik 4 kriteria pada tugas terkait.
```

---

### 11. Kuis / Evaluasi Formatif

**Prompt:**
```
Buatkan 5 soal pilihan ganda untuk kuis formatif topik "Dasar HTML dan
CSS", tingkat kesulitan menengah, sertakan kunci jawaban dan penjelasan
singkat tiap jawaban.
```

**Contoh hasil:**
```markdown
1. Tag HTML yang tepat untuk membuat daftar bernomor adalah...
   a) <ul>  b) <ol>  c) <li>  d) <dl>
   **Jawaban: b** — <ol> (ordered list) menghasilkan daftar bernomor.

2. Properti CSS untuk mengatur jarak antar elemen di dalam border adalah...
   a) margin  b) padding  c) gap  d) spacing
   **Jawaban: b** — padding mengatur jarak di dalam elemen, margin di
   luar elemen.

3. (dst. — total 5 soal dengan pola serupa)
```

---

### 12. Presensi Daring

**Prompt:**
```
Buatkan draf kebijakan singkat presensi daring untuk dicantumkan di
myITS Classroom: cara presensi (modul Attendance), batas waktu presensi
dibuka per sesi kuliah/praktikum, dan konsekuensi jika tidak presensi.
```

**Contoh hasil:**
```
📋 Kebijakan Presensi

Presensi dilakukan melalui modul Attendance di myITS Classroom, dibuka
15 menit sebelum sesi kuliah/praktikum dimulai hingga 15 menit setelah
sesi berakhir. Mahasiswa yang tidak presensi dalam rentang waktu tersebut
dianggap tidak hadir kecuali ada konfirmasi tertulis (sakit/izin)
maksimal 2x24 jam setelah sesi.
```

---

### 13. ETS & EAS

**Prompt:**
```
Berdasarkan CPMK-1 dan CPMK-2 (materi minggu 1–7) MK Pemrograman Web,
buatkan kisi-kisi ETS (tabel: minggu, materi, bentuk soal) dan 2 contoh
soal yang mengukur pemahaman konsep + penerapan praktik.
```

**Contoh hasil:**
```markdown
| Minggu | Materi                     | Bentuk Soal              |
|--------|-----------------------------|----------------------------|
| 1–3    | Teknologi web, HTML, CSS    | Pilihan ganda + praktik    |
| 4      | Framework Bootstrap         | Pilihan ganda              |
| 5–6    | JavaScript & DOM            | Praktik (studi kasus)      |
| 7      | AJAX                        | Esai singkat               |

**Contoh soal:**
1. Jelaskan perbedaan elemen HTML block-level dan inline, beserta
   contohnya.
2. Buat potongan kode JavaScript untuk mengambil elemen dengan id
   "form-login" dan menampilkan pesan validasi saat tombol submit ditekan.
```

---

### 14. Sesi Sinkron (Live Session)

**Prompt:**
```
Buatkan agenda sesi sinkron (BigBlueButton/Zoom) 90 menit untuk topik
"Membangun Back-End" (minggu 12), dengan pembagian waktu jelas dan sesi
tanya-jawab.
```

**Contoh hasil:**
```
🖥️ Agenda Sesi Sinkron — Minggu 12: Membangun Back-End
Tautan: [BigBlueButton/Zoom link] · Durasi: 90 menit

00:00–10:00  Pembukaan & recap materi Front-End
10:00–40:00  Pemaparan struktur Back-End & routing API
40:00–65:00  Demo langsung: membuat endpoint API sederhana
65:00–80:00  Praktik mandiri: menghubungkan endpoint ke front-end
80:00–90:00  Tanya-jawab & pengumuman Tugas 2 (CRUD)
```

---

### 15. Survei / Umpan Balik

**Prompt:**
```
Buatkan survei umpan balik pembelajaran menjelang akhir semester untuk MK
Pemrograman Web: 3 pertanyaan skala Likert 1–5 dan 2 pertanyaan terbuka,
fokus pada kejelasan materi, kecukupan praktikum, dan saran perbaikan.
```

**Contoh hasil:**
```markdown
**Skala 1 (Sangat Tidak Setuju) – 5 (Sangat Setuju):**
1. Materi perkuliahan disampaikan dengan jelas dan mudah dipahami.
2. Sesi praktikum cukup membantu memahami implementasi teknis.
3. Umpan balik atas tugas diberikan tepat waktu dan membantu.

**Pertanyaan terbuka:**
4. Bagian materi mana yang menurut Anda paling sulit dipahami? Mengapa?
5. Apa saran Anda untuk perbaikan MK ini di semester berikutnya?
```

---

## Tips Prompting Efektif

1. **Selalu lampirkan RPS** sebagai konteks di awal percakapan — hasilnya jauh lebih akurat dibanding hanya menyebut nama topik.
2. **Minta format keluaran spesifik** (markdown/tabel/teks polos) agar tidak perlu diformat ulang manual sebelum ditempel ke Moodle.
3. **Untuk referensi/pustaka**, minta AI hanya memberi kata kunci pencarian — jangan minta judul/tautan jadi, karena AI bisa mengarang.
4. **Iterasi per bagian kecil** (per minggu/per komponen) lebih akurat daripada minta AI mengisi seluruh RPS sekaligus.
5. **Verifikasi angka bobot** hasil AI terhadap RPS asli — kesalahan penjumlahan bobot penilaian sering terjadi.
