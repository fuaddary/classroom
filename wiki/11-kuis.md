# 🎮 Kuis / Evaluasi Formatif

**Status:** 🟢 Wajib &nbsp;|&nbsp; [← Penugasan](10-assignment.md) &nbsp;|&nbsp; [Presensi Daring →](12-presensi.md)

---

> **Apa ini?** Panduan lengkap membuat berbagai jenis soal evaluasi formatif di myITS Classroom (Moodle), mulai dari pilihan ganda hingga drag & drop — semua tersedia dalam format **Moodle XML siap import**.

---

## Jenis Soal yang Tersedia

| # | Jenis | Cocok untuk | File XML |
|---|-------|-------------|----------|
| 1 | [Pilihan Ganda](#1-pilihan-ganda-single-answer) | Pemahaman konsep, analisis pilihan terbaik | [`01-pilihan-ganda.xml`](../moodle-quiz-xml/01-pilihan-ganda.xml) |
| 2 | [Checkbox / Multi-Jawaban](#2-checkbox--multi-jawaban) | Soal dengan >1 jawaban benar | [`02-checkbox-multi-jawaban.xml`](../moodle-quiz-xml/02-checkbox-multi-jawaban.xml) |
| 3 | [Mencocokkan](#3-mencocokkan-matching) | Pasangan konsep-definisi, istilah-contoh | [`03-mencocokkan.xml`](../moodle-quiz-xml/03-mencocokkan.xml) |
| 4 | [Benar / Salah](#4-benar--salah-truefalse) | Validasi miskonsepsi | [`04-benar-salah.xml`](../moodle-quiz-xml/04-benar-salah.xml) |
| 5 | [Isian Singkat](#5-isian-singkat-short-answer) | Recall istilah/sintaks spesifik | [`05-isian-singkat.xml`](../moodle-quiz-xml/05-isian-singkat.xml) |
| 6 | [Esai](#6-esai-essay) | Analisis mendalam, evaluasi, studi kasus | [`06-esai.xml`](../moodle-quiz-xml/06-esai.xml) |
| 7 | [Drag & Drop ke Teks](#7-drag--drop-ke-teks-ddwtos) | Melengkapi kode/teks, urutan logis | [`07-drag-drop-teks.xml`](../moodle-quiz-xml/07-drag-drop-teks.xml) |
| — | **Bank Soal Lengkap** | Semua 21 soal dalam 1 file import | [`00-bank-soal-lengkap.xml`](../moodle-quiz-xml/00-bank-soal-lengkap.xml) |

> **Cara Import:** Moodle Admin → Bank Soal → Import → Pilih format **"Moodle XML"** → Upload file → Import

---

## 1. Pilihan Ganda (Single Answer)

**Kapan digunakan:** Soal dengan 1 jawaban benar yang jelas — cocok untuk menguji pemahaman konsep, sintaks, dan terminologi.

**Karakteristik Moodle XML:**
- `<single>true</single>` → tampil sebagai radio button
- `fraction="100"` → jawaban benar
- `fraction="0"` → pengecoh

### 💡 Prompt AI

```
Buatkan [N] soal pilihan ganda (single answer) topik "[TOPIK]" untuk
MK Pemrograman Web, tingkat kesulitan [mudah/menengah/sulit].
Setiap soal: 1 jawaban benar (fraction="100") dan 3 pengecoh masuk akal
(fraction="0"), plus umpan balik singkat tiap opsi.
Output Moodle XML (<quiz>...</quiz>), encoding UTF-8.
```

### 📋 Contoh XML

```xml
<question type="multichoice">
  <name><text>CSS Box Model — Properti jarak dalam elemen</text></name>
  <questiontext format="html">
    <text><![CDATA[<p>Properti CSS untuk mengatur jarak <em>di dalam</em> elemen adalah...</p>]]></text>
  </questiontext>
  <single>true</single>
  <shuffleanswers>true</shuffleanswers>
  <answernumbering>abc</answernumbering>
  <answer fraction="100" format="html">
    <text><![CDATA[<code>padding</code>]]></text>
    <feedback format="html"><text><![CDATA[<p>✅ Benar! padding = jarak dalam border elemen.</p>]]></text></feedback>
  </answer>
  <answer fraction="0" format="html">
    <text><![CDATA[<code>margin</code>]]></text>
    <feedback format="html"><text><![CDATA[<p>❌ margin = jarak di luar elemen.</p>]]></text></feedback>
  </answer>
  <answer fraction="0" format="html">
    <text><![CDATA[<code>gap</code>]]></text>
    <feedback format="html"><text><![CDATA[<p>❌ gap digunakan pada flex/grid container.</p>]]></text></feedback>
  </answer>
  <answer fraction="0" format="html">
    <text><![CDATA[<code>spacing</code>]]></text>
    <feedback format="html"><text><![CDATA[<p>❌ spacing bukan properti CSS standar.</p>]]></text></feedback>
  </answer>
</question>
```

📥 **File lengkap:** [`01-pilihan-ganda.xml`](../moodle-quiz-xml/01-pilihan-ganda.xml) — 3 soal siap import

---

## 2. Checkbox / Multi-Jawaban

**Kapan digunakan:** Soal di mana lebih dari 1 pilihan benar — menguji kemampuan mahasiswa mengenali *semua* opsi yang valid.

**Karakteristik Moodle XML:**
- `<single>false</single>` → tampil sebagai checkbox
- Partial credit: total fraction jawaban benar = 100, pengecoh diberi fraction negatif
- Contoh 3 jawaban benar: tiap jawaban benar `fraction="33.33333"`, pengecoh `fraction="-33.33333"`

### 💡 Prompt AI

```
Buatkan [N] soal checkbox (multi-jawaban, lebih dari 1 jawaban benar)
topik "[TOPIK]" untuk MK Pemrograman Web. Setiap soal: 2–3 jawaban
benar dengan skor terbagi rata (fraction total = 100 sebelum penalti),
dan 2 pengecoh (fraction negatif). Gunakan <single>false</single>.
Output Moodle XML.
```

### 📋 Contoh XML

```xml
<question type="multichoice">
  <name><text>CSS Flexbox — Properti yang berlaku pada flex container</text></name>
  <questiontext format="html">
    <text><![CDATA[<p>Pilih <strong>semua</strong> properti yang berlaku pada flex <em>container</em>:</p>]]></text>
  </questiontext>
  <single>false</single>
  <shuffleanswers>true</shuffleanswers>
  <answer fraction="33.33333" format="html">
    <text><![CDATA[<code>justify-content</code>]]></text>
    <feedback format="html"><text><![CDATA[<p>✅ Benar!</p>]]></text></feedback>
  </answer>
  <answer fraction="33.33333" format="html">
    <text><![CDATA[<code>align-items</code>]]></text>
    <feedback format="html"><text><![CDATA[<p>✅ Benar!</p>]]></text></feedback>
  </answer>
  <answer fraction="-33.33333" format="html">
    <text><![CDATA[<code>flex-grow</code>]]></text>
    <feedback format="html"><text><![CDATA[<p>❌ flex-grow adalah properti flex item.</p>]]></text></feedback>
  </answer>
</question>
```

📥 **File lengkap:** [`02-checkbox-multi-jawaban.xml`](../moodle-quiz-xml/02-checkbox-multi-jawaban.xml) — 2 soal siap import

---

## 3. Mencocokkan (Matching)

**Kapan digunakan:** Menguji kemampuan menghubungkan konsep dengan definisi, tag dengan fungsi, method HTTP dengan operasi CRUD, dll.

**Karakteristik Moodle XML:**
- Setiap pasangan dalam `<subquestion>`
- Kiri = `<text>`, kanan = `<answer><text>`
- Moodle otomatis acak urutan pilihan kanan

### 💡 Prompt AI

```
Buatkan [N] soal mencocokkan (matching) topik "[TOPIK]" untuk MK
Pemrograman Web. Setiap soal: 4–5 pasangan konsep↔definisi atau
istilah↔contoh. Format: setiap pasangan dalam tag <subquestion> berisi
<text> (item kiri) dan <answer><text> (pasangan kanan).
Output Moodle XML dengan <question type="matching">.
```

### 📋 Contoh XML

```xml
<question type="matching">
  <name><text>HTTP Method — Cocokkan dengan operasi CRUD</text></name>
  <questiontext format="html">
    <text><![CDATA[<p>Cocokkan HTTP Method dengan operasi CRUD yang sesuai:</p>]]></text>
  </questiontext>
  <shuffleanswers>true</shuffleanswers>
  <subquestion format="html">
    <text><strong>GET</strong></text>
    <answer format="html"><text>Read — Mengambil data dari server</text></answer>
  </subquestion>
  <subquestion format="html">
    <text><strong>POST</strong></text>
    <answer format="html"><text>Create — Mengirim data baru ke server</text></answer>
  </subquestion>
  <subquestion format="html">
    <text><strong>DELETE</strong></text>
    <answer format="html"><text>Delete — Menghapus data dari server</text></answer>
  </subquestion>
</question>
```

📥 **File lengkap:** [`03-mencocokkan.xml`](../moodle-quiz-xml/03-mencocokkan.xml) — 3 soal siap import

---

## 4. Benar / Salah (True/False)

**Kapan digunakan:** Meluruskan miskonsepsi umum — sajikan pernyataan yang campuran benar dan salah.

**Karakteristik Moodle XML:**
- Jawaban hanya `true` atau `false`
- Jawaban yang benar diberi `fraction="100"`, yang salah `fraction="0"`
- `<penalty>1</penalty>` agar jawaban salah mendapat penalti penuh

### 💡 Prompt AI

```
Buatkan [N] pernyataan Benar/Salah topik "[TOPIK]" untuk MK
Pemrograman Web. Campurkan pernyataan yang benar dan salah (bukan
semua salah atau semua benar). Sertakan penjelasan singkat di
<generalfeedback> mengapa pernyataan itu benar/salah.
Output Moodle XML dengan <question type="truefalse">.
```

### 📋 Contoh XML

```xml
<question type="truefalse">
  <name><text>B/S — let dan var memiliki scope yang sama</text></name>
  <questiontext format="html">
    <text><![CDATA[<p>Variabel yang dideklarasikan dengan <code>let</code> dan
    <code>var</code> memiliki <em>scope</em> yang persis sama di JavaScript.</p>]]></text>
  </questiontext>
  <generalfeedback format="html">
    <text><![CDATA[<p>SALAH. <code>let</code> = block scope,
    <code>var</code> = function scope. Keduanya berbeda.</p>]]></text>
  </generalfeedback>
  <answer fraction="0"><text>true</text>
    <feedback format="html"><text><![CDATA[<p>❌ Tidak tepat. Scopenya berbeda.</p>]]></text></feedback>
  </answer>
  <answer fraction="100"><text>false</text>
    <feedback format="html"><text><![CDATA[<p>✅ Benar bahwa pernyataan itu SALAH!</p>]]></text></feedback>
  </answer>
</question>
```

📥 **File lengkap:** [`04-benar-salah.xml`](../moodle-quiz-xml/04-benar-salah.xml) — 5 soal siap import

---

## 5. Isian Singkat (Short Answer)

**Kapan digunakan:** Menguji recall istilah teknis, nama properti, nama method — jawaban harus tepat dan spesifik.

**Karakteristik Moodle XML:**
- `<usecase>0</usecase>` = case-insensitive (direkomendasikan)
- Daftarkan semua variasi jawaban yang diterima (dengan/tanpa tanda baca, dll.)
- Bisa partial credit dengan `fraction="50"` untuk jawaban hampir benar

### 💡 Prompt AI

```
Buatkan [N] soal isian singkat (short answer) topik "[TOPIK]" untuk
MK Pemrograman Web. Setiap soal: jawaban berupa 1 kata/frase pendek
yang spesifik dan tidak ambigu. Sertakan variasi penulisan yang
diterima. Gunakan <usecase>0</usecase> (case-insensitive).
Output Moodle XML dengan <question type="shortanswer">.
```

### 📋 Contoh XML

```xml
<question type="shortanswer">
  <name><text>CSS — Properti untuk warna teks</text></name>
  <questiontext format="html">
    <text><![CDATA[<p>Properti CSS untuk mengubah <strong>warna teks</strong>
    sebuah elemen? (Tulis nama properti saja)</p>]]></text>
  </questiontext>
  <usecase>0</usecase>
  <answer fraction="100">
    <text>color</text>
    <feedback format="html"><text><![CDATA[<p>✅ Benar!</p>]]></text></feedback>
  </answer>
  <answer fraction="100">
    <text>color:</text>
    <feedback format="html"><text><![CDATA[<p>✅ Benar (dengan titik dua juga diterima).</p>]]></text></feedback>
  </answer>
</question>
```

📥 **File lengkap:** [`05-isian-singkat.xml`](../moodle-quiz-xml/05-isian-singkat.xml) — 4 soal siap import

---

## 6. Esai (Essay)

**Kapan digunakan:** Soal analisis/evaluasi mendalam — dinilai manual oleh dosen. Cocok untuk studi kasus, perbandingan, atau evaluasi desain.

**Fitur penting:**
- `<responsetemplate>` = kerangka jawaban yang muncul di kotak teks mahasiswa
- `<graderinfo>` = rubrik penilaian yang hanya terlihat oleh grader/dosen
- `<responsefieldlines>` = tinggi kotak teks (baris)
- `<attachments>` = apakah mahasiswa bisa upload file

### 💡 Prompt AI

```
Buatkan [N] soal esai topik "[TOPIK]" untuk MK Pemrograman Web yang:
1. Mengukur kemampuan analisis/evaluasi (bukan sekadar definisi)
2. Dilengkapi <responsetemplate> sebagai kerangka jawaban mahasiswa
3. Disertai rubrik penilaian di <graderinfo>
Output Moodle XML dengan <question type="essay">.
```

### 📋 Contoh XML (ringkas)

```xml
<question type="essay">
  <name><text>Esai — Analisis: Kapan gunakan Vanilla JS vs Framework</text></name>
  <questiontext format="html">
    <text><![CDATA[<p>Analisis kapan Vanilla JS lebih tepat vs framework front-end.
    Berikan minimal 2 skenario untuk masing-masing dengan alasannya.</p>]]></text>
  </questiontext>
  <responsetemplate format="html">
    <text><![CDATA[<p><strong>1. Faktor penentu:</strong></p><p>[...]</p>
    <p><strong>2. Skenario:</strong></p><p>[...]</p>]]></text>
  </responsetemplate>
  <graderinfo format="html">
    <text><![CDATA[<p>Rubrik: Kelengkapan (25%) · Ketepatan skenario (40%) · Trade-off (25%) · Bahasa (10%)</p>]]></text>
  </graderinfo>
  <responseformat>editor</responseformat>
  <responsefieldlines>15</responsefieldlines>
  <attachments>0</attachments>
</question>
```

📥 **File lengkap:** [`06-esai.xml`](../moodle-quiz-xml/06-esai.xml) — 2 soal dengan rubrik lengkap

---

## 7. Drag & Drop ke Teks (ddwtos)

**Kapan digunakan:** Melengkapi kode program atau paragraf — mahasiswa menyeret kata/frasa ke dalam celah kosong. Lebih interaktif dari isian singkat.

**Karakteristik Moodle XML:**
- `[[1]]`, `[[2]]` dst. di dalam teks = posisi celah
- `<dragbox>` mendefinisikan pilihan yang tersedia (disertai pengecoh)
- `<no>` pada dragbox harus sesuai dengan urutan [[n]] di teks soal

### 💡 Prompt AI

```
Buatkan [N] soal drag-and-drop ke teks (ddwtos) topik "[TOPIK]" untuk
MK Pemrograman Web. Soal berupa kode/paragraf dengan kata kunci dihapus,
diganti [[1]], [[2]], dst. Sediakan pilihan kata yang tepat dan pengecoh
yang menarik. Output Moodle XML dengan <question type="ddwtos">.
```

### 📋 Contoh XML

```xml
<question type="ddwtos">
  <name><text>Drag &amp; Drop — Lengkapi CSS Flexbox</text></name>
  <questiontext format="html">
    <text><![CDATA[<p>Lengkapi kode CSS berikut:</p>
    <pre>.container {
  display: [[1]];
  flex-direction: [[2]];
  align-items: [[3]];
}</pre>]]></text>
  </questiontext>
  <shuffleanswers>1</shuffleanswers>
  <dragbox><no>1</no><text>flex</text></dragbox>
  <dragbox><no>2</no><text>row</text></dragbox>
  <dragbox><no>3</no><text>center</text></dragbox>
  <!-- Pengecoh -->
  <dragbox><no>4</no><text>grid</text></dragbox>
  <dragbox><no>5</no><text>column</text></dragbox>
  <dragbox><no>6</no><text>flex-start</text></dragbox>
</question>
```

📥 **File lengkap:** [`07-drag-drop-teks.xml`](../moodle-quiz-xml/07-drag-drop-teks.xml) — 2 soal siap import

---

## 📦 Bank Soal Lengkap

File [`00-bank-soal-lengkap.xml`](../moodle-quiz-xml/00-bank-soal-lengkap.xml) berisi **21 soal dari semua 7 jenis** dalam satu file — import sekali langsung ke bank soal Moodle.

---

## 🖼️ Preview Tampilan di myITS Classroom

![Preview Kuis](../screenshot-preview/11-kuis.png)

---

[← Penugasan](10-assignment.md) &nbsp;·&nbsp; [🏠 Daftar Isi](00-pengantar.md) &nbsp;·&nbsp; [Presensi Daring →](12-presensi.md)
