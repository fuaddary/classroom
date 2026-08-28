# 💡 Tips Prompting Efektif

**Status:** Referensi &nbsp;|&nbsp; [← Survei & Umpan Balik](15-survei.md) &nbsp;|&nbsp; [🏠 Daftar Isi](00-pengantar.md)

---

> Lima prinsip untuk mendapatkan hasil AI yang lebih akurat, konsisten, dan langsung bisa dipakai di myITS Classroom.

---

## 1. 📎 Selalu lampirkan RPS sebagai konteks

AI tidak tahu detail mata kuliah Anda — tanpa RPS, hasilnya generik dan sering tidak akurat.

```
# Cara terbaik:
Buka percakapan baru → lampirkan/paste RPS di awal → baru ketik prompt spesifik.

# Contoh pembuka percakapan:
"Berikut RPS MK Pemrograman Web saya: [paste isi RPS atau upload file PDF/DOCX].
Gunakan ini sebagai konteks untuk semua pertanyaan saya berikutnya."
```

**Mengapa penting:** Dengan RPS sebagai konteks, AI bisa mengisi CPMK yang benar, bobot penilaian yang akurat, dan topik materi yang sesuai — bukan mengarang.

---

## 2. 📐 Minta format output yang spesifik

Tentukan format output sejak awal agar tidak perlu diformat ulang sebelum ditempel ke Moodle.

```
# Untuk ditempel ke Moodle:
"Output dalam format HTML dengan inline style (siap ditempel ke Edit HTML source Moodle).
Jangan gunakan class CSS eksternal atau variabel CSS."

# Untuk kuis/bank soal:
"Output dalam format Moodle XML (<quiz>...</quiz>), encoding UTF-8,
siap di-import via Admin > Bank Soal > Import > Format Moodle XML."

# Untuk README/panduan:
"Output dalam format Markdown dengan heading ##, bullet point, dan tabel."
```

---

## 3. 🔍 Untuk referensi/pustaka — minta kata kunci, bukan judul jadi

AI sering "mengarang" judul buku, nama penulis, atau URL yang tidak ada. Hindari meminta tautan spesifik.

```
# ❌ Hindari:
"Berikan 5 referensi lengkap dengan judul, penulis, dan URL."

# ✅ Lakukan ini:
"Berikan 3 kategori referensi (dokumentasi resmi, artikel/tutorial, studi kasus) beserta
kata kunci pencarian yang bisa saya gunakan untuk mencari dan memverifikasi sumber aslinya.
JANGAN mengarang judul/penulis/URL."
```

Setelah mendapat kata kunci, cari sendiri di Google Scholar, MDN Web Docs, atau perpustakaan ITS.

---

## 4. 🧩 Iterasi per bagian kecil, bukan sekaligus

Meminta AI mengisi seluruh RPS atau 16 minggu sekaligus menghasilkan kualitas yang turun dan error yang sulit ditemukan.

```
# ❌ Kurang efektif:
"Buatkan konten myITS Classroom lengkap untuk 16 minggu MK Pemrograman Web."

# ✅ Lebih efektif:
"Buatkan outline materi untuk pertemuan minggu ke-6, topik JavaScript & DOM.
[Setelah selesai dan diverifikasi] Sekarang buatkan untuk minggu ke-7, topik AJAX."
```

**Untuk soal kuis:** Buat per topik/minggu (5–10 soal sekaligus), review dulu, baru lanjut ke topik berikutnya.

---

## 5. ✅ Verifikasi angka bobot penilaian

AI sering membuat kesalahan penjumlahan saat mengisi bobot evaluasi.

```
# Setelah AI menghasilkan komponen evaluasi, selalu cek:
- Apakah total bobot = 100%?
- Apakah bobot per CPMK sesuai dengan yang ada di RPS?
- Apakah komponen ETS/EAS/Tugas sudah sesuai proporsi yang ditetapkan?
```

**Contoh cek cepat:** Paste tabel komponen evaluasi dari hasil AI ke Excel/Sheets → sum kolom bobot → pastikan = 100.

---

## 🔁 Alur Kerja yang Direkomendasikan

```
Buka AI baru
    ↓
Lampirkan RPS (paste atau upload)
    ↓
Ketik prompt per bagian (pilih dari daftar isi wiki)
    ↓
Review output AI (periksa akurasi, bobot, referensi)
    ↓
Copy HTML → Paste ke Moodle via Edit HTML source
    ↓
Cek tampilan di preview Moodle sebelum publish
```

---

## 🆘 Jika Hasil AI Kurang Tepat

| Masalah | Solusi |
|---------|--------|
| Output terlalu generik | Tambahkan lebih banyak konteks dari RPS di prompt |
| Bobot evaluasi salah | Sebutkan angka persis di prompt: "Tugas 30%, ETS 20%, Tugas 2 25%, EAS 25%" |
| HTML tidak muncul di Moodle | Pastikan paste via ikon `</>` Edit HTML source, bukan di kotak teks biasa |
| Referensi terlihat karangan | Gunakan prompt tipe 3 (kata kunci pencarian), bukan judul jadi |
| Soal XML gagal diimport | Cek encoding UTF-8, pastikan tidak ada karakter khusus yang tidak di-escape |

---

[← Survei & Umpan Balik](15-survei.md) &nbsp;·&nbsp; [🏠 Daftar Isi](00-pengantar.md)
