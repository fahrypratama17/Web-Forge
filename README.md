# WEB FORGE

## Daftar Isi

1. [Orientasi Workshop](#1-orientasi-workshop)
2. [What Is a Website?](#2-what-is-a-website)
3. [Web Anatomy: HTML, CSS, dan JavaScript](#3-web-anatomy-html-css-dan-javascript)
4. [HTML: The Foundation](#4-html-the-foundation)
5. [Inside an HTML Document](#5-inside-an-html-document)
6. [Essential HTML Tags](#6-essential-html-tags)
7. [Semantic HTML](#7-semantic-html)
8. [CSS: The Visual Language](#8-css-the-visual-language)
9. [CSS Styling Essentials](#9-css-styling-essentials)
10. [CSS Box Model](#10-css-box-model)
11. [CSS Colors & Typography](#11-css-colors-typography)
12. [Understanding CSS Flexbox](#12-understanding-css-flexbox)
13. [Flexbox in Practice](#13-flexbox-in-practice)
14. [Responsive Design & Media Query](#14-responsive-design-media-query)
15. [Final Project: Landing Page Web Forge](#15-final-project-landing-page-web-forge)
16. [Mini Challenges](#16-mini-challenges)
17. [Bonus: Pengantar JavaScript](#17-bonus-pengantar-javascript)
18. [Troubleshooting, Review, dan Referensi](#18-troubleshooting-review-dan-referensi)

---

# 1. Orientasi Workshop

## 1.1 Apa yang akan dipelajari?

Setelah mengikuti sesi ini, peserta diharapkan mampu:

- Menjelaskan peran **HTML, CSS, dan JavaScript** dalam sebuah website.
- Membaca struktur dokumen HTML dan memahami hubungan antara **tag**, **element**, serta **attribute**.
- Memilih tag HTML berdasarkan **makna konten**, bukan hanya tampilannya.
- Menggunakan elemen semantik seperti `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, dan `<footer>`.
- Menghubungkan file CSS dengan HTML dan memahami cara penulisan aturan CSS.
- Membedakan `margin`, `border`, `padding`, dan `content` pada **box model**.
- Mengatur warna, tipografi, dan layout menggunakan **CSS custom properties** dan **Flexbox**.
- Membuat tampilan yang menyesuaikan lebar layar menggunakan **media query**.
- Menghasilkan satu **landing page** sederhana yang bisa dibuka di desktop dan mobile.

---

# 2. What Is a Website?

Website adalah kumpulan halaman atau sumber daya web yang dapat diakses melalui browser, umumnya menggunakan alamat (URL) dan saling terhubung dengan tautan. Sebuah **webpage** merupakan satu halaman; **website** dapat terdiri dari satu atau banyak halaman.

Contoh yang kita gunakan sehari-hari:

- Website informasi kampus yang menampilkan berita, jadwal, dan pengumuman.
- Website portofolio yang memperkenalkan profil dan karya seseorang.
- Website organisasi yang menampilkan acara, anggota, dan pendaftaran.
- Website layanan yang memiliki katalog, tombol, dan formulir.

## 2.1 Bagaimana halaman tampil di browser?

Secara sederhana:

```text
Pengguna mengetik URL
         │
         ▼
Browser meminta halaman
         │
         ▼
Browser membaca HTML
         │
         ├── Membaca CSS untuk tampilan
         │
         └── Menjalankan JavaScript untuk perilaku
         │
         ▼
Halaman terlihat dan bisa digunakan
```

Browser mengubah dokumen HTML menjadi struktur yang dapat ditampilkan. CSS digunakan untuk menghitung gaya dan tata letak, sedangkan JavaScript dapat mengubah isi halaman atau merespons tindakan pengguna.

**Poin penting:** website sederhana dapat berjalan hanya dengan HTML dan CSS. JavaScript diperlukan ketika kita ingin menambahkan perilaku atau interaksi tertentu.

**Pertanyaan pembuka:** Saat melihat sebuah tombol di website, teknologi manakah yang membuat tombolnya ada, memberinya warna, dan menjalankan aksi ketika diklik?

---

# 3. Web Anatomy: HTML, CSS, dan JavaScript

Untuk mempermudah pemahaman, bayangkan ketiga teknologi ini sebagai bagian tubuh manusia:

| Teknologi | Analogi | Peran sebenarnya | Contoh |
|---|---|---|---|
| **HTML** (*HyperText Markup Language*) | Kerangka / skeleton | Menentukan **isi, struktur, dan makna** halaman | Heading, paragraf, gambar, tombol |
| **CSS** (*Cascading Style Sheets*) | Pakaian | Menentukan **tampilan** dan susunan visual | Warna, font, jarak, ukuran, layout |
| **JavaScript** | Otak | Menentukan **logika dan perilaku** | Menu interaktif, validasi form, klik tombol |

Bayangkan sebuah halaman profil:

```html
<h1>Halo, saya Naya!</h1>
<button type="button">Lihat Portofolio</button>
```

Kode di atas adalah **HTML**: judul dan tombol sudah ada, tetapi tidak diberi desain khusus.

```css
h1 {
  color: #1f4db3;
}

button {
  background: #1f4db3;
  color: white;
  border: 0;
  padding: 12px 20px;
  border-radius: 8px;
}
```

Kode tersebut adalah **CSS**: teks berubah warna dan tombol memiliki tampilan.

Pada tahap ini, tombol HTML tersebut belum menjalankan aksi ketika diklik. **JavaScript** dapat menambahkan aksi tersebut, tetapi kode dan praktiknya dibahas secara terpisah pada **Bab 17 — Bonus: Pengantar JavaScript**. Dengan demikian, contoh HTML dan CSS di atas dapat dipahami tanpa harus menulis JavaScript lebih dahulu.

**Ringkasan konsep:** HTML menjelaskan *apa* yang ada, CSS menjelaskan *bagaimana tampilannya*, dan JavaScript menjelaskan *apa yang terjadi saat pengguna berinteraksi*. Masing-masing teknologi akan dibahas dalam bagiannya sendiri, tanpa mencampur sintaks pada bab HTML.

---

# 4. HTML: The Foundation

## 4.1 Apa itu HTML?

HTML adalah singkatan dari **HyperText Markup Language**. HTML menggunakan penanda berupa **tag** untuk menjelaskan konten website kepada browser.

Ada empat konsep penting yang perlu dipahami:

1. **HyperText Markup Language:** HTML menyusun konten melalui tag dan elemen.
2. **Bukan bahasa pemrograman:** HTML tidak menyediakan alur logika pemrograman seperti percabangan dan perulangan umum.
3. **Struktur dokumen:** elemen HTML tersusun dalam hierarki yang dibaca browser.
4. **Semantic HTML:** beberapa elemen menjelaskan peran atau makna bagiannya.

### Markup language vs programming language

**Markup language** digunakan untuk menandai struktur atau makna suatu konten. **Programming language** digunakan untuk menyatakan langkah, perhitungan, logika, atau perilaku yang dapat dieksekusi.

Contoh markup HTML:

```html
<h1>Belajar Web Development</h1>
<p>Hari ini kita belajar HTML dan CSS.</p>
```

Browser memahami bahwa baris pertama adalah heading dan baris berikutnya paragraf.

Perbedaannya dapat dilihat dari tujuan masing-masing: HTML menandai bahwa suatu teks adalah **judul** atau **paragraf**, sedangkan bahasa pemrograman dapat digunakan untuk mengolah data, memeriksa kondisi, dan menentukan tindakan berdasarkan hasil pemeriksaan tersebut.

**Fokus bab ini hanya HTML.** Kita mempelajari struktur dan makna konten tanpa menambahkan kode pemrograman ke contoh HTML.

## 4.2 Tag, element, dan attribute

Perhatikan:

```html
<p class="deskripsi">Selamat datang!</p>
```

| Bagian | Nama | Fungsi |
|---|---|---|
| `<p>` | Opening tag | Menandai awal paragraf |
| `class="deskripsi"` | Attribute | Memberi informasi tambahan pada elemen |
| `Selamat datang!` | Content | Isi yang ditampilkan |
| `</p>` | Closing tag | Menandai akhir paragraf |
| Seluruh rangkaian | HTML element | Satu elemen lengkap |

**Paired element** memiliki tag pembuka dan penutup, misalnya `<h1>...</h1>` atau `<p>...</p>`.

**Void element** tidak memiliki konten anak dan tidak menggunakan closing tag, misalnya:

```html
<img src="foto.jpg" alt="Foto kegiatan">
<br>
<hr>
<input type="text" name="nama">
```

### Atribut yang perlu dikenali

| Attribute | Contoh | Kegunaan |
|---|---|---|
| `href` | `<a href="/kontak">` | Tujuan tautan |
| `src` | `<img src="foto.jpg">` | Sumber media |
| `alt` | `<img alt="Siswa berdiskusi">` | Alternatif teks gambar |
| `class` | `<div class="card">` | Mengelompokkan elemen, sering dipakai untuk CSS |
| `id` | `<section id="materi">` | Identitas unik dalam satu dokumen |
| `type` | `<input type="email">` | Jenis kontrol/input |
| `lang` | `<html lang="id">` | Bahasa utama dokumen |

**Class vs ID:** beberapa elemen boleh memakai `class` yang sama, tetapi sebuah nilai `id` harus unik dalam satu dokumen. Di CSS, `.card` menargetkan class dan `#materi` menargetkan ID.

## 4.3 Hierarki elemen (*nesting*)

Elemen HTML dapat berisi elemen lain:

```html
<section>
  <h2>Materi Workshop</h2>
  <p>Kita akan belajar <strong>HTML</strong> dan CSS.</p>
</section>
```

Di sini, `<section>` merupakan **parent** dari `<h2>` dan `<p>`. Elemen `<strong>` berada di dalam `<p>`.

Jangan menyusun penutup secara silang:

```html
<!-- Tidak benar -->
<p>Halo <strong>semuanya</p></strong>

<!-- Benar -->
<p>Halo <strong>semuanya</strong></p>
```

**Coba sendiri:** buat paragraf yang memiliki satu kata penting dan tandai dengan `<strong>`.

---

# 5. Inside an HTML Document

Setiap halaman HTML memiliki struktur dasar. Buat file `index.html` dan masukkan kode berikut:

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Pertamaku</title>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>Ini website pertama saya.</p>
</body>
</html>
```

## 5.1 Mengenal setiap bagian

| Kode | Fungsi | Apakah terlihat langsung di halaman? |
|---|---|---|
| `<!DOCTYPE html>` | Mendeklarasikan dokumen HTML5 dan membantu browser memakai *standards mode* | Tidak |
| `<html lang="id">` | Elemen akar dari dokumen dan menyatakan bahasa utama | Tidak langsung |
| `<head>` | Menampung metadata dan referensi resource | Tidak |
| `<meta charset="UTF-8">` | Mengatur encoding karakter | Tidak |
| `<meta name="viewport" ...>` | Membantu layout mengikuti ukuran layar perangkat | Tidak |
| `<title>` | Mengatur judul tab browser | Di tab browser |
| `<body>` | Menampung konten halaman | Ya, untuk elemen yang terlihat |

**Catatan:** `<!DOCTYPE html>` adalah deklarasi, bukan elemen HTML biasa. `<head>` tidak sama dengan `<header>`: `<head>` berisi informasi dokumen, sedangkan `<header>` adalah konten yang tampil di dalam halaman.

### Live demo

1. Simpan file dengan `Ctrl + S`.
2. Buka `index.html` di browser.
3. Ubah isi `<title>` dan lihat tab browser.
4. Ubah isi `<h1>` dan lihat konten halaman.
5. Hapus sementara salah satu `<meta>` lalu diskusikan peran metadata (jangan lupa mengembalikannya).

**Pertanyaan:** Mengapa judul pada `<title>` tidak muncul sebagai heading di tengah halaman? Karena `<title>` adalah metadata, bukan konten `<body>`.

---

# 6. Essential HTML Tags

HTML memiliki banyak tag. Daripada menghafal semuanya, kelompokkan berdasarkan **fungsi**.

## 6.1 Text & Formatting

| Tag | Fungsi | Contoh penggunaan |
|---|---|---|
| `<h1>`–`<h6>` | Heading berjenjang | Judul halaman dan subbagian |
| `<p>` | Paragraf | Deskripsi suatu topik |
| `<strong>` | Penekanan kepentingan | Peringatan atau informasi penting |
| `<em>` | Penekanan dalam kalimat | Kata yang ingin ditekankan |
| `<span>` | Pembungkus inline generik | Mewarnai sebagian teks |
| `<br>` | Baris baru pada teks | Alamat atau puisi, bila memang perlu |
| `<hr>` | Pemisah tematik | Peralihan topik |

```html
<h1>Selamat Datang di Web Forge</h1>
<h2>Belajar HTML</h2>
<p>Ini adalah <strong>workshop dasar</strong> untuk membuat website.</p>
<p>Jangan lupa <em>praktik langsung</em>.</p>
<p>Materi: <span class="highlight">HTML dan CSS</span></p>
```

**Heading adalah hierarki, bukan ukuran font.** Jangan menggunakan `<h6>` hanya agar tampilannya kecil; ukuran teks dapat diatur menggunakan CSS.

### Block vs inline secara sederhana

- Elemen seperti `<h1>`, `<p>`, dan `<div>` secara bawaan biasanya tampil sebagai **block**: mengambil baris baru.
- Elemen seperti `<a>`, `<strong>`, `<em>`, dan `<span>` biasanya tampil sebagai **inline**: mengikuti aliran teks.
- `<img>` merupakan **replaced element** yang secara bawaan berperilaku inline, tetapi punya dimensi intrinsik dan dapat diubah layout-nya dengan CSS.

Istilah ini menjelaskan **cara tampil bawaan**, bukan makna semantik. CSS dapat mengubah `display` suatu elemen.

## 6.2 Links, Images & Lists

### Hyperlink (`<a>`)

```html
<a href="https://developer.mozilla.org/" target="_blank" rel="noopener noreferrer">
  Buka dokumentasi MDN
</a>

<a href="#materi">Lihat Materi</a>
```

- `href` menentukan tujuan tautan.
- Awalan `#` mengarah ke elemen dengan `id` yang sesuai pada halaman yang sama.
- `target="_blank"` biasanya membuka tab baru; `rel="noopener noreferrer"` sering digunakan sebagai langkah pengamanan dan privasi tambahan.

### Image (`<img>`)

```html
<img src="foto-workshop.jpg" alt="Peserta sedang mengikuti workshop" width="320">
```

- `src` adalah alamat file gambar.
- `alt` menjelaskan gambar bagi pengguna yang tidak dapat melihatnya atau saat gambar gagal dimuat.
- `width` mengatur lebar yang dicantumkan pada HTML. Ukuran tampilan juga dapat dikendalikan dengan CSS.

**Tips:** jangan memakai `alt="gambar"` untuk semua gambar; tulis deskripsi yang relevan. Jika gambar murni dekoratif, `alt=""` bisa lebih tepat.

### Lists (`<ul>`, `<ol>`, `<li>`)

```html
<h3>Materi Workshop</h3>
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>Responsive Design</li>
</ul>

<h3>Langkah Menjalankan Project</h3>
<ol>
  <li>Buat file index.html.</li>
  <li>Tulis struktur HTML.</li>
  <li>Simpan file.</li>
  <li>Buka di browser.</li>
</ol>
```

Gunakan `<ul>` jika urutan tidak penting, dan `<ol>` jika urutan merupakan bagian dari maknanya. Setiap item memakai `<li>`.

## 6.3 Containers: `<div>` dan `<span>`

`<div>` adalah **container generik tanpa makna semantik khusus**. Cocok untuk kebutuhan pengelompokan visual atau layout ketika tidak ada elemen yang lebih bermakna.

```html
<div class="card">
  <h3>HTML</h3>
  <p>Membentuk struktur halaman.</p>
</div>
```

`<span>` juga generik, tetapi biasanya digunakan untuk membungkus bagian kecil dari teks:

```html
<p>Harga: <span class="price">Gratis</span></p>
```

**Aturan praktis:** gunakan tag semantik jika bagian tersebut memiliki peran yang jelas. Pilih `<div>` atau `<span>` untuk pengelompokan yang hanya berkaitan dengan layout atau styling.

## 6.4 Forms & Tables

Form digunakan untuk mengumpulkan input pengguna. Tabel dipakai untuk **data tabular**, bukan menyusun layout seluruh halaman.

```html
<form>
  <label for="nama">Nama peserta</label>
  <input id="nama" name="nama" type="text" placeholder="Nama lengkap" required>

  <label for="kelas">Kelas</label>
  <select id="kelas" name="kelas">
    <option value="html">HTML</option>
    <option value="css">CSS</option>
  </select>

  <button type="submit">Daftar</button>
</form>
```

```html
<table>
  <thead>
    <tr><th scope="col">Materi</th><th scope="col">Fungsi</th></tr>
  </thead>
  <tbody>
    <tr><td>HTML</td><td>Struktur</td></tr>
    <tr><td>CSS</td><td>Tampilan</td></tr>
  </tbody>
</table>
```

Tag inti untuk membuat formulir dan tabel meliputi `<form>`, `<input>`, `<button>`, `<table>`, `<tr>`, dan `<td>`. Elemen seperti `<label>`, `<select>`, `<thead>`, dan `<th>` membantu membuat struktur lebih jelas, mudah digunakan, dan mudah dipahami.

> **Batasan latihan:** contoh ini bertujuan mengenalkan struktur dan atribut formulir. Form belum terhubung ke tujuan pengiriman atau penyimpanan data.

---

# 7. Semantic HTML

## 7.1 Apa itu semantic HTML?

*Semantic* berarti **bermakna**. Semantic HTML adalah penggunaan elemen yang menjelaskan **peran konten** dalam sebuah halaman.

Bandingkan:

```html
<!-- Sulit dipahami tanpa melihat class -->
<div class="bagian-atas">...</div>
<div class="bagian-menu">...</div>
<div class="konten-utama">...</div>
```

Dengan:

```html
<!-- Peran tiap bagian lebih jelas -->
<header>...</header>
<nav>...</nav>
<main>...</main>
```

Keduanya dapat dibuat tampak sama dengan CSS, tetapi contoh kedua memberikan informasi struktur yang lebih jelas.

## 7.2 Mengapa harus memakai semantic HTML?

### Untuk browser dan teknologi bantu

Browser dan teknologi bantu seperti *screen reader* dapat mengenali beberapa landmark atau peran dokumen, sehingga struktur halaman lebih mudah dinavigasi. Semantic HTML juga memudahkan pemrosesan konten; tetapi **bukan jaminan otomatis untuk SEO atau aksesibilitas**—isi, urutan heading, label, dan implementasinya tetap harus benar.

### Untuk developer

Kode lebih mudah dibaca, dirawat, dan dikembangkan bersama tim. Ketika menemukan `<nav>`, developer langsung memahami bahwa bagian tersebut berisi navigasi, tanpa harus menebak dari nama class.

## 7.3 Mengenal elemen semantik

| Tag | Fungsi | Contoh |
|---|---|---|
| `<header>` | Bagian pengantar suatu halaman/section | Logo, nama website, judul |
| `<nav>` | Sekumpulan tautan navigasi utama | Menu Beranda, Materi, Kontak |
| `<main>` | Konten utama yang khas dari halaman | Hero, daftar materi, isi profil |
| `<section>` | Kelompok konten berdasarkan satu topik | Tentang kami, layanan, materi |
| `<article>` | Konten mandiri yang dapat berdiri sendiri | Artikel, berita, card artikel |
| `<aside>` | Konten tambahan atau terkait | Sidebar, tautan terkait |
| `<footer>` | Informasi penutup halaman/section | Kontak, hak cipta, tautan |

**Nuansa penting:** `<header>` dan `<footer>` juga dapat dipakai di dalam elemen konten tertentu, bukan hanya di paling atas/bawah halaman. Sebuah `<section>` biasanya sebaiknya memiliki heading yang mengidentifikasi topiknya. Pada umumnya, hanya ada satu `<main>` yang terlihat untuk konten utama halaman.

## 7.4 Struktur halaman semantik

```text
<body>
├── <header>
│   └── <nav>      Menu navigasi
├── <main>
│   ├── <section>  Hero / perkenalan
│   ├── <section>  Kelompok materi
│   │   └── <article> Informasi mandiri
│   └── <aside>    Informasi tambahan (jika relevan)
└── <footer>       Penutup halaman
```

Contoh kode:

```html
<header>
  <nav aria-label="Navigasi utama">
    <a href="#beranda">Beranda</a>
    <a href="#materi">Materi</a>
  </nav>
</header>

<main id="beranda">
  <section aria-labelledby="intro-title">
    <h1 id="intro-title">Selamat Datang di Web Forge</h1>
    <p>Tempat belajar membuat website dari nol.</p>
  </section>

  <section id="materi" aria-labelledby="materi-title">
    <h2 id="materi-title">Materi Pembelajaran</h2>
    <article>
      <h3>HTML Fundamentals</h3>
      <p>Mempelajari struktur dan makna konten.</p>
    </article>
  </section>

  <aside aria-label="Informasi tambahan">
    <p>Tips: praktikkan setiap contoh di browser.</p>
  </aside>
</main>

<footer>
  <p>Web Forge Workshop</p>
</footer>
```

### Kapan menggunakan `<div>`?

Gunakan `<div>` ketika tujuannya hanya membuat pembungkus untuk layout, misalnya `.container`, `.hero-content`, atau `.card-list`. Jangan memaksakan `<section>` untuk setiap kotak visual.

**Mini challenge:** buat struktur halaman yang memiliki header, navigasi, main berisi dua section, dan footer. Setelah itu jelaskan mengapa setiap tag dipilih.

---

# 8. CSS: The Visual Language

## 8.1 Apa itu CSS?

CSS adalah singkatan dari **Cascading Style Sheets**. CSS menentukan bagaimana elemen HTML ditampilkan: warna, font, ukuran, jarak, posisi, hingga perilaku layout pada ukuran layar berbeda.

Bayangkan HTML sebagai struktur rumah dan CSS sebagai desain interiornya. HTML menetapkan mana ruang tamu dan pintu; CSS menentukan warna cat, besar ruangan, jarak antarfurnitur, dan cara penataannya.

### Struktur satu aturan CSS

```css
h1 {
  color: #1e293b;
  font-size: 40px;
}
```

- `h1` = **selector**, elemen yang ingin dipilih.
- `color` dan `font-size` = **property**.
- `#1e293b` dan `40px` = **value**.
- Bagian `property: value;` disebut **declaration**.
- Kurung kurawal `{ ... }` berisi deklarasi yang berlaku untuk selector tersebut.

## 8.2 Three Ways to Apply CSS

### A. Inline CSS

Ditempatkan langsung pada atribut `style`:

```html
<h1 style="color: blue;">Halo, Web Forge!</h1>
```

Cepat untuk demonstrasi kecil, tetapi sulit dikelola jika dipakai pada banyak elemen.

### B. Internal CSS

Diletakkan di dalam `<style>` pada bagian `<head>`:

```html
<head>
  <style>
    h1 {
      color: blue;
    }
  </style>
</head>
```

Cocok untuk percobaan satu halaman atau contoh yang sangat kecil.

### C. External CSS

CSS disimpan pada file terpisah:

```html
<!-- index.html, di dalam <head> -->
<link rel="stylesheet" href="style.css">
```

```css
/* style.css */
h1 {
  color: blue;
}
```

**Rekomendasi workshop:** gunakan **external CSS** agar struktur HTML dan styling terpisah serta kode lebih mudah dirawat.

## 8.3 Mengenal selector

```css
/* Element selector: semua elemen <p> */
p {
  color: #475569;
}

/* Class selector: semua elemen class="card" */
.card {
  background: white;
}

/* ID selector: elemen id="materi" */
#materi {
  padding: 48px 0;
}

/* Descendant selector: h2 di dalam section */
section h2 {
  font-size: 28px;
}

/* Pseudo-class: ketika pointer berada di atas tautan */
a:hover {
  text-decoration: underline;
}
```

Gunakan **class** sebagai pilihan utama untuk styling komponen yang berulang. Hindari membuat seluruh aturan CSS bergantung pada ID atau inline style.

## 8.4 Apa maksud *Cascading*?

Beberapa aturan CSS dapat menargetkan elemen yang sama. Browser menentukan gaya akhir melalui mekanisme **cascade**, yang mempertimbangkan antara lain asal dan tingkat kepentingan deklarasi, *specificity*, serta urutan aturan.

Contoh sederhana:

```html
<p class="intro">Halo dunia!</p>
```

```css
p {
  color: gray;
}

.intro {
  color: blue;
}
```

Teks menjadi **biru** karena aturan `.intro` lebih spesifik daripada `p` (dengan asumsi keduanya memiliki tingkat kepentingan dan konteks cascade yang sama).

Contoh jika dua aturan memiliki specificity setara:

```css
.intro { color: green; }
.intro { color: purple; }
```

Aturan terakhir berlaku, sehingga teks menjadi ungu.

**Coba sendiri:** tambahkan dua aturan dengan selector yang sama, ubah urutannya, kemudian perhatikan hasil. Ini cara termudah mengenali efek cascade.

---

# 9. CSS Styling Essentials

Empat topik utama yang diperlihatkan: **global reset**, **box model & spacing**, **visual styling**, dan **typography**.

## 9.1 Global reset

Browser sudah memiliki styling bawaan (*user agent stylesheet*), seperti margin pada `<body>` dan heading. Agar perilaku dasar lebih konsisten, kita dapat membuat reset minimal:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

- `margin: 0` menghapus margin bawaan pada elemen.
- `padding: 0` menghapus padding bawaan pada elemen.
- `box-sizing: border-box` membuat `width` dan `height` mencakup content, padding, dan border.

**Perhatian:** reset yang agresif juga menghapus jarak bawaan pada heading, paragraf, dan list. Setelah reset, kita perlu menambah spacing secara sadar. Untuk project di bawah, kita menggunakan reset yang lebih ringan agar tetap nyaman bagi pemula.

## 9.2 Spacing: jarak internal dan eksternal

```css
.card {
  margin: 20px;
  padding: 24px;
}
```

- `margin`: jarak **di luar border** elemen terhadap elemen lain.
- `padding`: ruang **di dalam border**, antara konten dan border.

Kita akan mengupasnya pada bab **CSS Box Model**.

## 9.3 Visual styling

```css
.card {
  background-color: #ffffff;
  border: 1px solid #e2e8f0;
  border-radius: 12px;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
}
```

| Properti | Fungsi |
|---|---|
| `background-color` | Warna latar belakang |
| `border` | Garis tepi |
| `border-radius` | Membulatkan sudut |
| `box-shadow` | Memberikan efek bayangan |
| `width`, `height` | Ukuran elemen |
| `max-width` | Membatasi lebar maksimum |

## 9.4 Typography

```css
body {
  font-family: Arial, sans-serif;
  font-size: 16px;
  color: #1e293b;
  line-height: 1.6;
}
```

`line-height` menambah ruang antarbaris sehingga teks panjang lebih nyaman dibaca. Selanjutnya, kita akan mengenal variabel warna dan properti tipografi lain.

---

# 10. CSS Box Model

Browser memperlakukan elemen sebagai sebuah **kotak** (*box*). Kotak tersebut terdiri atas empat lapisan:

```text
┌──────────────────────────── MARGIN ────────────────────────────┐
│                                                               │
│   ┌──────────────────────── BORDER ─────────────────────────┐   │
│   │                                                        │   │
│   │   ┌────────────────── PADDING ──────────────────────┐   │   │
│   │   │                                                │   │   │
│   │   │                   CONTENT                      │   │   │
│   │   │                                                │   │   │
│   │   └────────────────────────────────────────────────┘   │   │
│   │                                                        │   │
│   └────────────────────────────────────────────────────────┘   │
│                                                               │
└───────────────────────────────────────────────────────────────┘
```

| Lapisan | Penjelasan |
|---|---|
| **Content** | Isi seperti teks atau gambar |
| **Padding** | Ruang antara konten dan border |
| **Border** | Garis tepi yang mengelilingi padding dan content |
| **Margin** | Ruang di luar border, memisahkan elemen dari lingkungan sekitar |

## 10.1 Contoh box model

```html
<div class="card">Belajar CSS itu menyenangkan!</div>
```

```css
.card {
  width: 320px;
  box-sizing: border-box;
  padding: 24px;
  border: 3px solid #4772f2;
  margin: 32px;
  background-color: white;
  border-radius: 12px;
}
```

Dengan `box-sizing: border-box`, lebar **border box** adalah `320px`. Padding dan border berada **di dalam** 320px tersebut. Margin berada di luar dan tidak dihitung ke dalam width.

Tanpa `border-box` (yaitu dengan `box-sizing: content-box`), total lebar border box pada contoh ini menjadi:

```text
320px (content) + 24px × 2 (padding) + 3px × 2 (border)
= 374px
```

Jika ada margin kiri dan kanan masing-masing 32px, ruang horizontal keseluruhan yang ditempati dalam kondisi sederhana menjadi `374 + 64 = 438px`.

## 10.2 Eksperimen langsung

1. Ubah `padding: 24px` menjadi `padding: 48px`. Apa yang terjadi pada ruang di dalam card?
2. Ubah `margin: 32px` menjadi `margin: 8px`. Apakah kontennya berubah atau posisi card terhadap sekitarnya?
3. Tambahkan `box-sizing: content-box` lalu bandingkan lebar visualnya.
4. Buka **DevTools → Elements → Computed** untuk melihat diagram box model yang dihitung browser.

**Kesalahan yang sering terjadi:** mengubah `margin` untuk memperbesar ruang di dalam kotak. Untuk jarak antara isi dan border, gunakan **padding**.

---

# 11. CSS Colors & Typography

## 11.1 Menyimpan warna dengan CSS custom properties

Jika warna yang sama dipakai di banyak tempat, jangan menuliskan nilainya berulang-ulang. Kita dapat membuat **custom properties** di selector `:root`.

```css
:root {
  --primary-color: #2e2a26;
  --accent-color: #c97b4a;
  --bg-color: #ffffff;
}

body {
  color: var(--primary-color);
  background-color: var(--bg-color);
}

button {
  background-color: var(--accent-color);
  color: white;
}
```

Kelebihan pendekatan ini: ketika warna brand ingin diganti, cukup ubah satu nilai variabel.

### Cara membaca contoh

- `--accent-color` adalah nama custom property.
- `var(--accent-color)` mengambil nilai yang disimpan.
- `:root` menunjuk elemen akar dokumen (pada HTML biasanya `<html>`), sehingga nilainya mudah digunakan di seluruh halaman melalui pewarisan.

## 11.2 Mengenal format warna

```css
h1 {
  color: #1e293b;          /* Hexadecimal */
}

button {
  background-color: rgb(37, 99, 235);   /* RGB */
}

.card {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12); /* Transparansi */
}
```

Untuk workshop ini, gunakan **hex** untuk warna biasa dan `rgba()` jika memerlukan transparansi sederhana.

## 11.3 Properti tipografi

| Properti | Contoh | Fungsi |
|---|---|---|
| `font-family` | `Arial, sans-serif` | Jenis font |
| `font-size` | `36px` | Ukuran teks |
| `font-weight` | `700` atau `bold` | Ketebalan font |
| `font-style` | `italic` | Gaya teks |
| `text-align` | `center`, `right`, `left` | Perataan teks |
| `color` | `#1e293b` | Warna teks |
| `line-height` | `1.6` | Tinggi baris |

```css
.hero-title {
  font-family: Arial, sans-serif;
  font-size: 48px;
  font-weight: 700;
  font-style: normal;
  text-align: left;
  line-height: 1.15;
}

.description {
  font-size: 16px;
  line-height: 1.7;
  color: #475569;
}
```

**Tips desain:** pilih satu atau dua jenis font, buat hierarki heading yang jelas, dan gunakan kontras warna yang cukup agar teks mudah dibaca.

## 11.4 Mengenal satuan ukuran

- `px`: satuan CSS pixel, mudah dipahami untuk ukuran tertentu.
- `%`: relatif terhadap ukuran yang relevan dari parent atau konteks properti.
- `rem`: relatif terhadap ukuran font elemen akar.
- `em`: relatif terhadap ukuran font elemen atau parent, tergantung propertinya.
- `vw` / `vh`: relatif terhadap dimensi viewport.

Untuk pemula, `px`, `%`, dan `rem` sudah cukup untuk mempraktikkan layout sederhana. Gunakan `max-width` agar konten tidak terlalu lebar di desktop.

---

# 12. Understanding CSS Flexbox

Flexbox adalah sistem layout CSS **satu dimensi** yang memudahkan kita menyusun elemen dalam arah **row** atau **column**. Fleksibilitasnya berguna untuk navigasi, kelompok tombol, card, dan bagian hero.

## 12.1 Mengaktifkan Flexbox

```html
<div class="kotak-container">
  <div class="kotak">A</div>
  <div class="kotak">B</div>
  <div class="kotak">C</div>
</div>
```

```css
.kotak-container {
  display: flex;
  gap: 20px;
}

.kotak {
  padding: 20px;
  background: #dbeafe;
  border-radius: 8px;
}
```

Elemen `.kotak-container` disebut **flex container**, sedangkan A, B, dan C disebut **flex items**.

## 12.2 `flex-direction`

Menentukan arah sumbu utama (*main axis*):

```css
.kotak-container {
  display: flex;
  flex-direction: row; /* horizontal: A B C */
}
```

```css
.kotak-container {
  display: flex;
  flex-direction: column; /* vertikal */
}
```

`row` merupakan nilai default. Ketika arah berubah, **main axis** dan **cross axis** ikut berubah.

## 12.3 `justify-content`

Mengatur distribusi item **sepanjang sumbu utama**.

| Nilai | Hasil |
|---|---|
| `flex-start` | Items berkumpul di awal sumbu utama |
| `center` | Items dikelompokkan di tengah |
| `flex-end` | Items berkumpul di akhir |
| `space-between` | Item pertama dan terakhir di ujung; ruang dibagi di antaranya |
| `space-around` | Ruang di sekitar tiap item |
| `space-evenly` | Ruang kosong dibagi rata |

```css
.kotak-container {
  display: flex;
  justify-content: space-between;
}
```

Jika `flex-direction: row`, sumbu utamanya biasanya horizontal. Jika `column`, sumbu utamanya vertikal.

## 12.4 `align-items`

Mengatur posisi item **di sepanjang sumbu silang** (*cross axis*).

```css
.kotak-container {
  display: flex;
  align-items: center;
}
```

Nilai yang sering digunakan:

- `flex-start`: dekat awal sumbu silang.
- `center`: sejajar di tengah sumbu silang.
- `flex-end`: dekat akhir sumbu silang.
- `stretch`: item meregang pada sumbu silang jika ukuran terkait masih `auto` dan tidak dibatasi.

**Perhatikan:** `justify-content` tidak selalu berarti horizontal dan `align-items` tidak selalu berarti vertikal. Keduanya mengikuti arah sumbu yang ditentukan `flex-direction`.

## 12.5 `gap`

`gap` memberi jarak **antar flex items** tanpa menambahkan margin manual pada tiap item.

```css
.kotak-container {
  display: flex;
  gap: 20px;
}
```

Jangan lupa satuan pada angka bukan nol: gunakan `gap: 20px`, bukan `gap: 20`.

## 12.6 `flex-wrap` dan `flex`

**Pengayaan:** dua properti berikut sangat membantu agar flex layout lebih fleksibel.

```css
.card-list {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  flex: 1 1 220px;
}
```

`flex-wrap: wrap` memungkinkan item turun baris ketika ruang tidak cukup. `flex: 1 1 220px` secara ringkas menentukan bahwa card boleh membesar, boleh menyusut, dan memiliki ukuran dasar sekitar `220px` sebelum distribusi ruang.

**Latihan:** coba ganti `row` ke `column`, `space-between` ke `center`, lalu ubah `gap`. Catat perubahan yang terlihat di browser.

---

# 13. Flexbox in Practice

Dua penerapan Flexbox yang umum ditemui adalah **navbar** dan **hero section**.

## 13.1 Navbar: logo kiri, menu kanan

```html
<nav class="navbar">
  <a href="#beranda" class="logo">Web Forge</a>

  <div class="nav-links">
    <a href="#materi">Materi</a>
    <a href="#kontak">Kontak</a>
  </div>
</nav>
```

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 24px;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 20px;
}
```

**Mengapa berhasil?** Navbar memiliki dua kelompok flex items: logo dan kumpulan link. `space-between` menempatkan kedua kelompok berjauhan, sedangkan `align-items: center` menyelaraskannya pada sumbu silang.

## 13.2 Hero: teks dan visual berdampingan

```html
<section class="hero">
  <div class="hero-content">
    <h1>Start Building Your Website</h1>
    <p>Belajar HTML dan CSS melalui praktik.</p>
  </div>

  <div class="hero-visual" aria-hidden="true">&lt;/&gt;</div>
</section>
```

```css
.hero {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 32px;
}

.hero-content {
  flex: 1;
}

.hero-visual {
  flex: 0 0 200px;
  padding: 40px;
  background: #dbeafe;
  border-radius: 16px;
  text-align: center;
}
```

**Perbedaan dari navbar:** pada hero, kita biasanya ingin menyelaraskan area teks dan visual dalam satu baris. Gunakan `gap` agar keduanya tidak saling berhimpitan.

---

# 14. Responsive Design & Media Query

Responsive design adalah pendekatan untuk membuat tampilan tetap nyaman digunakan pada berbagai ukuran layar, seperti desktop, tablet, dan smartphone.

## 14.1 Masalah yang ingin diselesaikan

Sebuah layout dengan dua card berdampingan mungkin terlihat baik di laptop, tetapi terlalu sempit jika dipaksakan pada layar smartphone. Kita dapat mengubah susunannya menjadi vertikal ketika layar lebih kecil.

## 14.2 Pengertian media query

*Media query* adalah aturan CSS yang menjalankan deklarasi tertentu ketika kondisi media/viewport terpenuhi.

Contoh penerapan:

```css
/* Desktop */
.card-container {
  display: flex;
  flex-direction: row;
  gap: 20px;
}

.card {
  flex: 1;
  min-height: 150px;
  background: #0ea5e9;
  border-radius: 12px;
}

/* Pada viewport 768px atau lebih kecil */
@media (max-width: 768px) {
  .card-container {
    flex-direction: column;
  }
}
```

Pada layar lebih lebar dari `768px`, card tersusun **sejajar**. Pada layar `768px` atau lebih kecil, card berubah menjadi **bertumpuk**.

**Apa itu breakpoint?** Batas ukuran yang dipilih sebagai titik perubahan layout. `768px` hanya contoh yang digunakan di workshop, bukan ukuran wajib untuk semua website.

## 14.3 Hal yang perlu diperhatikan

- Tambahkan `<meta name="viewport" content="width=device-width, initial-scale=1.0">` pada `<head>`.
- Hindari memberi `width` tetap yang membuat konten meluber di layar kecil.
- Gunakan `max-width: 100%` untuk gambar agar tidak keluar dari container.
- Susun ulang navbar, hero, dan card ketika memang dibutuhkan.
- Uji pada beberapa lebar viewport; jangan hanya mengandalkan satu preset HP.

## 14.4 Cara mengetes di browser

1. Jalankan `index.html`.
2. Buka Developer Tools (`F12` atau `Ctrl + Shift + I`, tergantung browser).
3. Aktifkan **Device Toolbar / Responsive Design Mode**.
4. Bandingkan lebar sekitar `1200px`, `768px`, dan `390px`.
5. Pastikan teks dapat dibaca, tombol mudah diklik, dan tidak ada horizontal scroll yang tidak diinginkan.

**Pertanyaan diskusi:** apakah responsive design hanya memperkecil font? Tidak. Responsive design juga menyangkut **susunan elemen, jarak, ukuran, serta pengalaman penggunaan**.

---

# 15. Final Project: Landing Page Web Forge

Pada proyek ini, kita menggabungkan **struktur HTML, semantic HTML, external CSS, global styling, box model, warna, tipografi, Flexbox, dan media query** menjadi sebuah landing page. Proyek dibuat tanpa framework agar setiap bagian kodenya mudah dipelajari.

## 15.1 Target hasil

Kita akan membuat satu landing page yang terdiri dari:

- **Header** dengan logo dan menu navigasi.
- **Hero section** yang memuat judul, deskripsi, CTA, dan elemen visual.
- **Section materi** berisi tiga card.
- **Footer** sederhana.
- Layout yang menyesuaikan layar besar dan kecil.

Buat dua file berikut:

```text
web-forge/
├── index.html
└── style.css
```

## 15.2 Langkah A — Tulis `index.html`

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Web Forge: belajar HTML dan CSS dari nol.">
  <title>Web Forge — Belajar Web Development</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header class="site-header">
    <nav class="navbar container" aria-label="Navigasi utama">
      <a class="logo" href="#beranda">WEB FORGE</a>

      <div class="nav-links">
        <a href="#beranda">Beranda</a>
        <a href="#materi">Materi</a>
        <a href="#kontak">Kontak</a>
      </div>
    </nav>
  </header>

  <main id="beranda">
    <section class="hero" aria-labelledby="hero-title">
      <div class="hero-inner container">
        <div class="hero-content">
          <p class="eyebrow">YOUR FIRST STEP INTO WEB DEVELOPMENT</p>
          <h1 id="hero-title">Build Your First Website.</h1>
          <p class="hero-description">
            Pelajari bagaimana HTML menyusun konten dan CSS
            menjadikannya menarik, rapi, dan responsif.
          </p>
          <a class="button" href="#materi">Explore the Materials</a>
        </div>

        <div class="hero-visual" aria-hidden="true">
          <span>&lt;HTML&gt;</span>
          <span>{ CSS }</span>
          <span>WEB FORGE</span>
        </div>
      </div>
    </section>

    <section class="materials container" id="materi" aria-labelledby="materi-title">
      <p class="eyebrow">WHAT YOU WILL LEARN</p>
      <h2 id="materi-title">Mulai dari Fundamental</h2>
      <p class="section-description">
        Pahami dasar website melalui tiga topik yang saling terhubung.
      </p>

      <div class="card-list">
        <article class="card">
          <span class="card-number">01</span>
          <h3>HTML</h3>
          <p>Menyusun struktur dan memberikan makna pada konten.</p>
        </article>

        <article class="card">
          <span class="card-number">02</span>
          <h3>CSS</h3>
          <p>Mengatur warna, tipografi, spacing, dan layout.</p>
        </article>

        <article class="card">
          <span class="card-number">03</span>
          <h3>Responsive</h3>
          <p>Menyesuaikan tampilan website di desktop dan mobile.</p>
        </article>
      </div>
    </section>
  </main>

  <footer class="site-footer" id="kontak">
    <div class="container footer-inner">
      <p>Web Forge Workshop</p>
      <a href="#beranda">Kembali ke atas</a>
    </div>
  </footer>
</body>
</html>
```

### Apa yang sudah dipraktikkan?

- `<head>` menyimpan metadata dan menghubungkan stylesheet.
- `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, dan `<footer>` mendeskripsikan peran konten.
- `<div>` dipakai ketika kita memerlukan pengelompokan visual (`.container`, `.nav-links`, `.hero-content`).
- `class` menghubungkan HTML dengan aturan CSS.
- `id="materi"` menjadi tujuan navigasi `<a href="#materi">`.

**Jalankan sekarang.** Hasilnya mungkin masih sederhana karena belum ada styling dari `style.css`. Itu normal.

## 15.3 Langkah B — Tulis `style.css`

```css
/* =====================================
   1. COLOR SYSTEM & GLOBAL STYLES
   ===================================== */
:root {
  --color-bg: #f8fafc;
  --color-surface: #ffffff;
  --color-text: #1e293b;
  --color-muted: #475569;
  --color-accent: #1674d9;
  --color-accent-hover: #0f5dae;
  --color-hero: #e8f2ff;
  --color-border: #dbe4ee;
}

* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  background: var(--color-bg);
  color: var(--color-text);
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.6;
}

a {
  color: inherit;
  text-decoration: none;
}

/* =====================================
   2. REUSABLE CONTAINER
   ===================================== */
.container {
  width: min(100% - 32px, 1080px);
  margin-inline: auto;
}

/* =====================================
   3. HEADER & NAVBAR (FLEXBOX)
   ===================================== */
.site-header {
  background: var(--color-surface);
  border-bottom: 1px solid var(--color-border);
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 24px;
  padding-block: 22px;
}

.logo {
  color: var(--color-accent);
  font-size: 20px;
  font-weight: 800;
  letter-spacing: 1px;
}

.nav-links {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 24px;
}

.nav-links a:hover,
.site-footer a:hover {
  color: var(--color-accent);
}

/* =====================================
   4. HERO (FLEXBOX)
   ===================================== */
.hero {
  background: var(--color-hero);
  padding-block: 88px;
}

.hero-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 48px;
}

.hero-content {
  flex: 1 1 520px;
}

.eyebrow {
  margin: 0 0 12px;
  color: var(--color-accent);
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 1.5px;
}

.hero h1 {
  max-width: 640px;
  margin: 0 0 20px;
  font-size: clamp(36px, 5vw, 58px);
  line-height: 1.1;
}

.hero-description {
  max-width: 570px;
  margin: 0 0 30px;
  color: var(--color-muted);
  font-size: 18px;
}

.button {
  display: inline-block;
  padding: 13px 24px;
  border-radius: 9px;
  background: var(--color-accent);
  color: #ffffff;
  font-weight: 700;
  transition: background-color 0.2s ease;
}

.button:hover {
  background: var(--color-accent-hover);
}

.hero-visual {
  display: flex;
  flex: 0 1 330px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 16px;
  min-height: 260px;
  padding: 28px;
  border: 2px solid var(--color-border);
  border-radius: 20px;
  background: var(--color-surface);
  box-shadow: 0 18px 40px rgba(30, 41, 59, 0.09);
  text-align: center;
}

.hero-visual span {
  display: block;
  font-size: 24px;
  font-weight: 800;
  color: var(--color-accent);
}

/* =====================================
   5. MATERIAL CARDS (FLEXBOX)
   ===================================== */
.materials {
  padding-block: 72px;
}

.materials h2 {
  margin: 0 0 12px;
  font-size: 36px;
  line-height: 1.2;
}

.section-description {
  margin: 0 0 32px;
  color: var(--color-muted);
}

.card-list {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  flex: 1 1 220px;
  padding: 28px;
  border: 1px solid var(--color-border);
  border-radius: 14px;
  background: var(--color-surface);
  box-shadow: 0 8px 22px rgba(30, 41, 59, 0.05);
  transition: transform 0.2s ease;
}

.card:hover {
  transform: translateY(-5px);
}

.card-number {
  color: var(--color-accent);
  font-size: 14px;
  font-weight: 800;
}

.card h3 {
  margin: 12px 0;
  font-size: 24px;
}

.card p {
  margin: 0;
  color: var(--color-muted);
}

/* =====================================
   6. FOOTER
   ===================================== */
.site-footer {
  border-top: 1px solid var(--color-border);
  background: var(--color-surface);
}

.footer-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  padding-block: 20px;
}

.footer-inner p {
  margin: 0;
}

/* =====================================
   7. RESPONSIVE / MEDIA QUERY
   ===================================== */
@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .nav-links {
    gap: 16px;
  }

  .hero {
    padding-block: 56px;
  }

  .hero-inner {
    flex-direction: column;
    align-items: stretch;
    gap: 28px;
  }

  .hero-content,
  .hero-visual {
    flex: auto;
  }

  .hero-visual {
    min-height: 180px;
  }

  .hero-description {
    font-size: 16px;
  }

  .materials {
    padding-block: 48px;
  }

  .materials h2 {
    font-size: 30px;
  }

  .card-list {
    flex-direction: column;
  }

  .card {
    flex: auto;
  }

  .footer-inner {
    flex-direction: column;
    align-items: flex-start;
  }
}
```

## 15.4 Langkah C — Amati hasilnya secara bertahap

Jangan hanya *copy-paste*. Lakukan beberapa percobaan:

1. **Global style:** ubah `--color-accent`. Bagian apa saja yang berubah sekaligus?
2. **Box model:** ubah `padding: 28px` pada `.card` menjadi `padding: 48px`.
3. **Typography:** ubah `font-size` di `.materials h2`.
4. **Navbar:** ganti `justify-content: space-between` dengan `center` pada `.navbar`.
5. **Hero:** ubah `align-items: center` menjadi `flex-start` pada `.hero-inner`.
6. **Cards:** ubah `gap: 20px` menjadi `gap: 40px` pada `.card-list`.
7. **Responsive:** kecilkan viewport di DevTools dan lihat perubahan layout ketika mencapai `768px`.

## 15.5 Checklist keberhasilan

- [ ] Halaman dapat dibuka tanpa error yang mengganggu.
- [ ] CSS sudah terhubung dan seluruh bagian ter-styling.
- [ ] Menu “Materi” berpindah ke section dengan `id="materi"`.
- [ ] Hero terdiri dari teks dan elemen visual yang berdampingan pada layar lebar.
- [ ] Tiga card tertata rapi pada desktop.
- [ ] Navbar, hero, dan card tersusun sesuai ruang layar kecil.
- [ ] Tidak ada konten utama yang terpotong secara horizontal.
- [ ] Teks, warna, dan jarak tetap nyaman dibaca.

---

# 16. Mini Challenges

Setelah project berhasil, coba modifikasi **tanpa langsung melihat contoh solusinya**.

## Challenge 1 — Change the Identity (HTML)

Ganti judul, deskripsi hero, dan tiga card agar menjadi website tentang topik pilihanmu: profil, komunitas, acara kampus, atau portofolio.

**Kriteria:** struktur HTML tetap semantik dan hierarki heading tetap masuk akal.

## Challenge 2 — Build Your Color System (CSS)

Ubah seluruh warna visual hanya melalui custom properties pada `:root`.

**Kriteria:** konsisten, kontras teks memadai, dan tidak perlu mengubah warna satu per satu di tiap selector.

## Challenge 3 — Fix the Layout (Flexbox)

Atur navbar dengan menu di kanan, tambahkan satu card baru, dan pastikan jarak antarelemen tidak saling berhimpitan.

**Kriteria:** memakai `display: flex`, `justify-content`, `align-items`, atau `gap` dengan tujuan yang jelas.

## Challenge 4 — Mobile First Check (Responsive)

Uji halaman pada lebar `390px`, `768px`, dan `1200px`. Ubah nilai breakpoint atau spacing jika diperlukan.

**Kriteria:** seluruh konten dapat dibaca dan diakses tanpa horizontal scroll yang tidak diinginkan.

## Challenge 5 — Explain Your Code

Pilih tiga potongan kode dan jelaskan:

1. Mengapa `<nav>` lebih tepat daripada `<div>` untuk kelompok menu navigasi?
2. Mengapa `padding` dipakai di dalam card, bukan `margin`?
3. Mengapa `flex-direction` diubah menjadi `column` pada layar kecil?

**Tujuannya:** menunjukkan pemahaman, bukan sekadar kemampuan menyalin kode.

---

# 17. Bonus: Pengantar JavaScript

> **Materi opsional:** bagian ini dapat dipelajari setelah menyelesaikan HTML dan CSS. JavaScript dibahas secara terpisah agar setiap bahasa tetap dipahami sesuai fungsinya.

JavaScript digunakan untuk menambahkan **perilaku dan interaksi** ke halaman. Pada contoh ini, kita akan membuat tombol untuk mengganti tema.

## 17.1 Tambahkan tombol pada HTML

Letakkan tombol berikut di dalam `<div class="nav-links">`, setelah tautan “Kontak”:

```html
<button id="theme-toggle" class="theme-button" type="button" aria-pressed="false">
  Ganti Tema
</button>
```

`id="theme-toggle"` adalah penanda yang nanti dipakai JavaScript untuk menemukan tombol.

## 17.2 Tambahkan styling pada `style.css`

```css
.theme-button {
  border: 1px solid var(--color-accent);
  border-radius: 8px;
  background: transparent;
  padding: 10px 14px;
  color: var(--color-accent);
  font: inherit;
  cursor: pointer;
}

body.dark-mode {
  --color-bg: #0f172a;
  --color-surface: #1e293b;
  --color-text: #f8fafc;
  --color-muted: #cbd5e1;
  --color-accent: #93c5fd;
  --color-accent-hover: #60a5fa;
  --color-hero: #172554;
  --color-border: #334155;
}
```

Agar tombol CTA tetap kontras pada tema gelap, tambah penyesuaian:

```css
body.dark-mode .button {
  color: #0f172a;
}
```

## 17.3 Buat file `script.js`

```javascript
// 1. Variable: menyimpan referensi tombol.
const themeButton = document.querySelector("#theme-toggle");

// 2. Function: mengubah class dan keterangan tombol.
function toggleTheme() {
  const isDark = document.body.classList.toggle("dark-mode");

  themeButton.setAttribute("aria-pressed", String(isDark));
  themeButton.textContent = isDark ? "Tema Terang" : "Ganti Tema";
}

// 3. Event listener: menjalankan fungsi ketika tombol diklik.
themeButton.addEventListener("click", toggleTheme);
```

Hubungkan file tersebut tepat sebelum `</body>` pada `index.html`:

```html
<script src="script.js"></script>
```

### Membaca JavaScript secara bertahap

- `const` membuat binding variabel yang tidak dapat ditugaskan ulang; dalam contoh ini menyimpan referensi tombol.
- `document.querySelector("#theme-toggle")` memilih elemen menggunakan CSS selector.
- `function toggleTheme()` mendefinisikan fungsi yang dapat dijalankan ketika dibutuhkan.
- `classList.toggle("dark-mode")` menambah atau menghapus class pada `<body>` dan mengembalikan status class setelah perubahan.
- `isDark ? "Tema Terang" : "Ganti Tema"` adalah ekspresi kondisional (*ternary*).
- `addEventListener("click", toggleTheme)` mendaftarkan fungsi agar dipanggil saat event klik terjadi.

**Catatan:** contoh mengasumsikan tombol `#theme-toggle` memang ada dan `script.js` dimuat setelah HTML tombol tersedia. Jika mengubah urutan file, pastikan kode tetap dijalankan setelah elemen terbentuk (misalnya dengan atribut `defer`).

**Mini challenge:** ganti teks tombol, tambahkan warna tema lain, atau buat tombol yang mengubah isi paragraf saat diklik.

---

# 18. Troubleshooting, Review, dan Referensi

## 18.1 Troubleshooting

| Masalah | Kemungkinan penyebab | Cara memeriksa |
|---|---|---|
| Website tidak berubah | File belum disimpan / browser belum memuat ulang | Simpan `Ctrl + S`, refresh tab |
| CSS tidak terbaca | Nama/path stylesheet salah | Cek `<link rel="stylesheet" href="style.css">` dan posisi file |
| Selector tidak bekerja | Penulisan class atau ID berbeda | Samakan `class="card"` dengan `.card` |
| Teks atau card terlalu rapat | `padding`/`margin`/`gap` belum sesuai | Inspeksi box model di DevTools |
| Navbar menumpuk tidak sesuai | Flex container atau arah sumbu tidak tepat | Cek `display`, `flex-direction`, `justify-content`, `align-items` |
| Mobile tetap seperti desktop | Media query salah atau meta viewport belum ada | Cek `@media` dan `<meta name="viewport">` |
| Ada scroll horizontal | Elemen terlalu lebar atau lebar fixed | Cek `width`, `min-width`, `max-width`, serta overflow |
| Klik tombol tema tidak bereaksi | File JS belum terhubung / selector tidak menemukan elemen | Cek `<script src="script.js">`, ID tombol, dan Console |

## 18.2 Quick Review

Coba jawab tanpa membuka materi:

1. Apa perbedaan peran HTML, CSS, dan JavaScript?
2. Apa bedanya markup language dan programming language?
3. Mengapa `<title>` tidak tampil sebagai heading di halaman?
4. Apa perbedaan tag, element, dan attribute?
5. Kapan kita sebaiknya menggunakan `<div>` dibanding `<section>`?
6. Mengapa semantic HTML membantu developer dan teknologi bantu?
7. Bagaimana cara menghubungkan CSS eksternal ke file HTML?
8. Apa yang dimaksud dengan *CSS cascade*?
9. Apa bedanya `margin` dan `padding`?
10. Apa kegunaan `box-sizing: border-box`?
11. Mengapa kita menggunakan CSS custom properties untuk warna?
12. Apa fungsi `flex-direction`, `justify-content`, `align-items`, dan `gap`?
13. Mengapa `justify-content` tidak selalu berarti pengaturan horizontal?
14. Bagaimana media query membantu responsive design?
15. Dalam bonus JavaScript, apa fungsi `addEventListener`?

### Kunci konsep singkat

- **HTML:** struktur dan makna konten; **CSS:** tampilan; **JavaScript:** logika dan interaksi.
- **Semantic HTML:** elemen dipilih berdasarkan peran, bukan penampilan.
- **External CSS:** dihubungkan menggunakan `<link>` pada `<head>`.
- **Box model:** content → padding → border → margin.
- **Flexbox:** layout satu dimensi yang berorientasi pada *main axis* dan *cross axis*.
- **Responsive:** aturan layout berubah sesuai kondisi viewport dan kebutuhan konten.

## 18.3 Apa langkah selanjutnya?

Setelah memahami dasar HTML dan CSS, kamu bisa melanjutkan ke topik berikut:

1. **Form HTML dan accessibility** yang lebih lengkap.
2. **CSS Grid** untuk layout dua dimensi (baris dan kolom).
3. **Transitions dan animations** untuk micro-interaction.
4. **JavaScript fundamentals**: variabel, tipe data, operator, percabangan, perulangan, dan fungsi.
5. **DOM manipulation dan events** untuk mengubah halaman secara dinamis.
6. **Project deployment** untuk memublikasikan halaman statis.

## 18.4 References

Dokumentasi resmi berikut bisa menjadi rujukan ketika mempelajari sintaks atau mengecek perilaku browser:

- [MDN — HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [MDN — HTML Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements)
- [MDN — CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [MDN — Introduction to the CSS Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_cascade/Cascade)
- [MDN — CSS Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_box_model)
- [MDN — CSS Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout)
- [MDN — Media Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries)
- [MDN — Introduction to JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

---

## Selesai — Dari Kode ke Website

Mulai dari dokumen HTML kosong, sekarang kamu sudah memiliki halaman yang memakai struktur semantik, warna konsisten, spacing yang terencana, Flexbox, dan responsive layout. Nilai utama workshop ini bukan seberapa cepat kamu mengetik, melainkan seberapa baik kamu memahami **mengapa setiap elemen dan aturan CSS digunakan**.

**Tantangan terakhir:** buat versi website milikmu sendiri, lalu coba jelaskan struktur HTML dan layout CSS-nya kepada orang lain.

