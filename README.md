# classroom

Kumpulan template & panduan untuk mengisi konten myITS Classroom (Moodle)
MK Pemrograman Web (ET234305) — Departemen Teknologi Informasi, ITS.
Dosen pengampu: Fuad Dary Rosyadi, S.Kom., M.Kom.

## Isi

- `info-kelas-pemrograman-web.html` — Kartu info mata kuliah versi standalone (styled, untuk dibuka di browser).
- `info-kelas-pemrograman-web-moodle.html` — Versi sama, inline-style penuh, siap tempel ke Moodle (Edit HTML source).
- `panduan-prompting-ai-myits-classroom.md` — Panduan 15 bagian: prompt AI + contoh hasil untuk tiap komponen wajib/anjuran & aktivitas myITS Classroom.
- `moodle-html-per-bagian/` — 15 file HTML fragment (inline style, siap tempel Moodle) untuk tiap bagian di panduan prompting.
- `screenshot-preview/` — Screenshot pratinjau dari tiap file di `moodle-html-per-bagian/`.
- `dekorasi-kelas-ti-its.html` — Template papan kelas + checklist standar mutu myITS Classroom (generik, bertema circuit/PCB).

## Cara pakai file HTML di Moodle

1. Buka file `.html`, salin semua isinya.
2. Di Moodle, buka Label/Page/Forum/Assignment yang relevan.
3. Klik ikon **`</>` Edit HTML source** di toolbar editor (Atto/TinyMCE).
4. Tempel kode HTML di kotak source tersebut, lalu klik Update/Save.

Jangan tempel langsung ke area teks biasa (tanpa lewat source editor) — Moodle
akan membersihkan/merusak markup-nya.
