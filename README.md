
# Web-Forge
## Belajar HTML & CSS dari Nol

Pernah penasaran bagaimana sebuah website dibuat?

Kenapa ada website yang tampilannya keren, sementara website buatan kita pertama kali malah terlihat seperti dokumen Word tahun 2003?

Jawabannya: **HTML dan CSS.**

Di workshop ini, kita akan belajar membuat website dari nol. Bukan cuma menonton orang mengetik kode, tetapi langsung mencoba, mengubah, dan melihat hasilnya di browser.

Tidak perlu pengalaman coding sebelumnya. Yang penting punya laptop, browser, dan keberanian menghadapi titik koma.

---

## Tentang Workshop

| Detail | Keterangan |
|---|---|
| Materi | HTML & CSS Fundamentals |
| Durasi | 60 menit |
| Level | Pemula |
| Metode | Penjelasan + Live Coding |
| Tools | VS Code dan Browser |
| Final Project | Landing Page Sederhana |

### Apa yang Akan Kita Buat?

Sebuah landing page yang memiliki:

- Navigation bar
- Judul dan deskripsi website
- Tombol navigasi
- Card informasi
- Warna dan tipografi
- Layout yang responsif

### Rundown

| Waktu | Materi |
|---|---|
| 00:00–00:05 | Kenalan dengan Website |
| 00:05–00:20 | HTML: Tag dan Macam-Macam Tag |
| 00:20–00:30 | Live Coding HTML |
| 00:30–00:45 | CSS: Bikin Website Lebih Menarik |
| 00:45–00:55 | Layout dan Responsive Design |
| 00:55–01:00 | Mini Challenge |

---

# Chapter 1 — Kenalan dengan Website

**Durasi: 5 menit**

## 1.1 Website Itu Apa?

Website adalah kumpulan halaman yang bisa kita akses menggunakan browser seperti Chrome, Firefox, atau Edge.

Contoh website:

- Google untuk mencari informasi.
- YouTube untuk menonton video.
- GitHub untuk menyimpan dan mengelola kode.
- Website kampus untuk melihat informasi akademik.

Sebuah website umumnya menggunakan tiga teknologi utama.

| Teknologi | Tugas |
|---|---|
| HTML | Membuat struktur dan isi |
| CSS | Mengatur desain dan tampilan |
| JavaScript | Menambahkan logika dan interaksi |

Bayangkan kita sedang membangun rumah:

- **HTML** adalah struktur rumah: dinding, pintu, jendela.
- **CSS** adalah cat, dekorasi, dan penataan ruangan.
- **JavaScript** adalah sistem elektroniknya, seperti lampu otomatis dan pintu pintar.

Kalau cuma HTML, rumahnya bisa digunakan, tetapi mungkin belum menarik.

Kalau cuma CSS tanpa HTML, mau mendekorasi apa?

## 1.2 Persiapan

Buat folder baru:

```text
web-forge/
├── index.html
└── style.css
```

Penjelasan:

- `index.html` menyimpan struktur halaman.
- `style.css` menyimpan aturan desain.

Buka folder menggunakan VS Code.

Kita mulai dari HTML.

---

# Chapter 2 — HTML: Kenalan dengan Tag

**Durasi: 15 menit**

## 2.1 Apa Itu HTML?

HTML adalah singkatan dari **HyperText Markup Language**.

HTML digunakan untuk memberi struktur dan makna pada konten website.

HTML bukan bahasa pemrograman untuk membuat logika, melainkan bahasa markup.

Artinya, kita menggunakan penanda untuk memberi tahu browser:

"Hei, bagian ini judul, bagian ini paragraf, dan yang ini gambar."

Penanda tersebut disebut **tag**.

## 2.2 Apa Itu Tag?

Tag adalah penanda dalam HTML yang ditulis menggunakan tanda kurung sudut:

```html
<nama-tag>
```

Contoh:

```html
<h1>Halo Dunia!</h1>
```

Mari kita bongkar:

```text
<h1>       Halo Dunia!       </h1>
 |             |              |
Opening       Content        Closing
  Tag                         Tag
```

- `<h1>` adalah tag pembuka.
- `Halo Dunia!` adalah isi atau konten.
- `</h1>` adalah tag penutup.

Keseluruhan kode tersebut disebut **elemen HTML**.

### Apakah Semua Tag Harus Ditutup?

Tidak semuanya.

**1. Paired Tags**

Tag yang memiliki pembuka dan penutup.

```html
<h1>Judul</h1>
<p>Paragraf</p>
<button>Klik Saya</button>
```

**2. Void Elements**

Elemen yang tidak memiliki konten anak dan tidak memakai closing tag.

```html
<br>
<hr>
<img src="foto.jpg" alt="Foto">
<input type="text">
```

Jadi, jangan membuat `<img>Foto</img>`.

Browser mungkin berusaha memperbaiki kesalahan kita, tetapi bukan berarti kita boleh sengaja menyusahkannya.

---

## 2.3 Macam-Macam Tag HTML

HTML memiliki banyak tag dengan fungsi yang berbeda.

Kita akan mengenal tag yang paling sering digunakan.

### A. Tag untuk Struktur Dokumen

Tag ini digunakan untuk menyusun kerangka halaman.

| Tag | Fungsi |
|---|---|
| `<html>` | Elemen utama dokumen HTML |
| `<head>` | Menyimpan informasi dokumen |
| `<title>` | Menentukan judul tab browser |
| `<meta>` | Menyimpan metadata halaman |
| `<body>` | Menampung konten yang ditampilkan |
| `<link>` | Menghubungkan resource eksternal |

Contoh:

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Website Pertama</title>
</head>
<body>

  <h1>Hello World!</h1>

</body>
</html>
```

Catatan: `<!DOCTYPE html>` adalah deklarasi tipe dokumen, bukan tag HTML biasa.

**Live Demo**

1. Tulis struktur HTML di atas.
2. Buka menggunakan browser.
3. Ubah teks pada `<title>`.
4. Ubah teks pada `<h1>`.
5. Bandingkan posisi kedua hasilnya.

Pertanyaan untuk peserta:

"Kenapa teks di `<title>` muncul di tab browser, sedangkan `<h1>` muncul di halaman?"

---

### B. Tag untuk Teks

Tag ini digunakan untuk menampilkan dan memberi makna pada teks.

| Tag | Fungsi |
|---|---|
| `<h1>`–`<h6>` | Heading atau judul |
| `<p>` | Paragraf |
| `<strong>` | Penekanan penting |
| `<em>` | Penekanan pada teks |
| `<span>` | Membungkus bagian teks |
| `<br>` | Membuat baris baru |
| `<hr>` | Pemisah tematik |

**Contoh:**

```html
<h1>Judul Utama</h1>
<h2>Subjudul</h2>
<h3>Judul Bagian</h3>

<p>Ini adalah paragraf.</p>

<p>
  Saya sedang belajar
  <strong>HTML dan CSS</strong>.
</p>

<p>
  Jangan lupa <em>simpan file</em>.
</p>
```

### Heading Itu Bukan Sekadar Ukuran Font

Tag `<h1>` sampai `<h6>` digunakan untuk menunjukkan hierarki judul.

```html
<h1>Belajar Web Development</h1>

<h2>HTML</h2>
<h3>HTML Tags</h3>
<h3>HTML Attributes</h3>

<h2>CSS</h2>
<h3>CSS Selectors</h3>
```

Jadi, jangan memilih `<h6>` hanya karena ingin tulisan kecil.

Kalau mau mengubah ukuran tulisan, nanti ada CSS.

---

### C. Tag untuk Link dan Gambar

**Hyperlink**

Tag `<a>` digunakan untuk membuat tautan.

```html
<a href="https://google.com">
  Buka Google
</a>
```

Ketika diklik, browser akan membuka alamat yang tercantum pada `href`.

**Image**

Tag `<img>` digunakan untuk menampilkan gambar.

```html
<img
  src="foto.jpg"
  alt="Foto profil"
  width="200"
>
```

Penjelasan:

- `src` menentukan lokasi gambar.
- `alt` memberikan deskripsi alternatif.
- `width` mengatur lebar tampilan gambar.

**Live Demo**

Coba gunakan:

```html
<a href="https://github.com">
  Kunjungi GitHub
</a>
```

Kemudian klik tautannya.

Sekarang ubah alamat `href` menjadi website lain.

---

### D. Tag untuk List

Ada dua jenis list yang umum digunakan.

**Unordered List**

Daftar tanpa urutan angka.

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

Hasilnya berupa daftar dengan bullet.

**Ordered List**

Daftar dengan urutan angka.

```html
<ol>
  <li>Buka VS Code</li>
  <li>Buat file HTML</li>
  <li>Simpan file</li>
  <li>Buka di browser</li>
</ol>
```

Perbedaan:

- `<ul>` digunakan ketika urutan tidak penting.
- `<ol>` digunakan ketika urutan penting.
- `<li>` digunakan untuk setiap item daftar.

---

### E. Tag untuk Container dan Layout

Tag ini membantu mengelompokkan konten.

| Tag | Fungsi |
|---|---|
| `<div>` | Container generik |
| `<header>` | Bagian kepala halaman atau section |
| `<nav>` | Navigasi |
| `<main>` | Konten utama |
| `<section>` | Bagian konten bertema tertentu |
| `<article>` | Konten yang berdiri sendiri |
| `<footer>` | Bagian penutup halaman atau section |

Contoh:

```html
<header>
  <h1>Website Saya</h1>
</header>

<main>
  <section>
    <h2>Tentang Saya</h2>
    <p>Saya sedang belajar HTML.</p>
  </section>
</main>

<footer>
  <p>Website Pertama Saya</p>
</footer>
```

Tag seperti `<header>`, `<main>`, dan `<footer>` disebut elemen semantik karena memberikan makna pada bagian halaman.

Sementara `<div>` hanya digunakan sebagai container generik.

---

### F. Tag untuk Form

Form digunakan ketika website membutuhkan input dari pengguna.

| Tag | Fungsi |
|---|---|
| `<form>` | Membungkus formulir |
| `<label>` | Memberi label pada input |
| `<input>` | Menerima input pengguna |
| `<textarea>` | Input teks panjang |
| `<select>` | Pilihan dropdown |
| `<option>` | Item pilihan |
| `<button>` | Tombol |

Contoh:

```html
<form>
  <label for="nama">Nama:</label>

  <input
    type="text"
    id="nama"
    name="nama"
    placeholder="Masukkan nama"
  >

  <button type="submit">
    Kirim
  </button>
</form>
```

Untuk sekarang, form tersebut hanya digunakan sebagai contoh struktur input.

Memproses atau menyimpan datanya membutuhkan pembahasan lebih lanjut.

---

## 2.4 Apa Itu Attribute?

Selain memiliki nama dan konten, tag HTML juga dapat memiliki atribut.

Atribut memberikan informasi atau konfigurasi tambahan pada elemen.

Contoh:

```html
<a href="https://google.com">
  Google
</a>
```

Pada kode tersebut:

- `a` adalah nama tag.
- `href` adalah nama atribut.
- `https://google.com` adalah nilai atribut.

Contoh lainnya:

```html
<p class="deskripsi">
  Saya suka belajar HTML.
</p>
```

Atribut `class` memberikan pengenal yang bisa digunakan untuk styling CSS.

### Class vs ID

```html
<div class="card">Card Pertama</div>
<div class="card">Card Kedua</div>

<section id="tentang">
  Tentang Kami
</section>
```

| Class | ID |
|---|---|
| Dapat digunakan berulang | Harus unik dalam satu dokumen |
| Cocok untuk styling berulang | Cocok untuk elemen spesifik |
| CSS menggunakan `.` | CSS menggunakan `#` |

**Pertanyaan singkat:**

"Kalau kita punya 10 card dengan desain yang sama, lebih cocok menggunakan class atau ID?"

Jawaban: Class.

---

# Chapter 3 — Let's Build a Website!

**Durasi: 10 menit**

Sekarang kita akan membuat sebuah landing page.

Tidak perlu langsung terlihat bagus. Kita fokus pada strukturnya dulu.

## 3.1 Membuat index.html

Isi file `index.html` dengan kode berikut:

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport"
        content="width=device-width, initial-scale=1.0">

  <title>Web-Forge</title>

  <link rel="stylesheet" href="style.css">
</head>

<body>

  <header>
    <nav class="navbar container">
      <a href="#" class="logo">Web-Forge</a>
      <a href="#materi">Materi</a>
    </nav>
  </header>

  <main>

    <section class="hero">
      <div class="container">

        <h1>Hello, Future Developer!</h1>

        <p>
          Belajar membuat website
          menggunakan HTML dan CSS.
        </p>

        <a href="#materi" class="button">
          Mulai Belajar
        </a>

      </div>
    </section>

    <section id="materi" class="container">

      <h2>Yang Akan Kita Pelajari</h2>

      <div class="card-grid">

        <article class="card">
          <h3>HTML</h3>
          <p>
            Membuat struktur halaman website.
          </p>
        </article>

        <article class="card">
          <h3>CSS</h3>
          <p>
            Membuat website lebih menarik.
          </p>
        </article>

        <article class="card">
          <h3>Responsive</h3>
          <p>
            Menyesuaikan tampilan di berbagai layar.
          </p>
        </article>

      </div>

    </section>

  </main>

</body>
</html>
```

## 3.2 Jalankan Website

Buka `index.html` menggunakan browser.

Hasil yang terlihat:

- Website memiliki judul.
- Ada tombol menuju bagian materi.
- Ada tiga informasi materi.
- Semua konten masih menggunakan tampilan dasar browser.

**Pertanyaan:**

"Kenapa website kita masih terlihat seperti dokumen biasa?"

Karena kita belum menambahkan styling.

Tenang, website-nya bukan rusak. Dia cuma belum berdandan.

---

# Chapter 4 — CSS: Saatnya Website Berdandan

**Durasi: 15 menit**

## 4.1 Apa Itu CSS?

CSS adalah singkatan dari **Cascading Style Sheets**.

CSS digunakan untuk mengatur bagaimana elemen HTML ditampilkan.

Contohnya:

- Mengubah warna teks.
- Mengubah background.
- Mengatur ukuran huruf.
- Mengatur jarak.
- Membuat tombol.
- Menyusun layout.

Tanpa CSS, browser akan menggunakan tampilan bawaannya.

## 4.2 Cara Menulis CSS

Struktur CSS:

```css
selector {
  property: value;
}
```

Contoh:

```css
h1 {
  color: blue;
  font-size: 36px;
}
```

Penjelasan:

- `h1` merupakan selector.
- `color` merupakan property.
- `blue` merupakan value.
- `font-size` mengatur ukuran teks.

CSS menggunakan tanda `{ }` untuk membungkus deklarasi, dan `;` untuk mengakhiri deklarasi.

## 4.3 Macam-Macam CSS Selector

### Element Selector

Memilih berdasarkan nama tag.

```css
p {
  color: gray;
}
```

Semua paragraf akan memiliki warna abu-abu.

### Class Selector

Memilih berdasarkan class.

```css
.card {
  background: white;
}
```

Tanda `.` berarti kita sedang memilih class.

### ID Selector

Memilih berdasarkan ID.

```css
#materi {
  padding: 40px;
}
```

Tanda `#` berarti kita sedang memilih ID.

## 4.4 Mengenal CSS Properties

| Property | Fungsi |
|---|---|
| `color` | Warna teks |
| `background` | Background elemen |
| `font-size` | Ukuran teks |
| `font-weight` | Ketebalan teks |
| `width` | Lebar |
| `height` | Tinggi |
| `padding` | Jarak di dalam elemen |
| `margin` | Jarak di luar elemen |
| `border` | Garis tepi |
| `border-radius` | Kelengkungan sudut |

### Margin vs Padding

Bayangkan sebuah kotak berisi tulisan.

```text
+-----------------------------+
|           MARGIN            |
|  +-----------------------+  |
|  |        BORDER         |  |
|  |  +-----------------+  |  |
|  |  |     PADDING     |  |  |
|  |  |   +---------+   |  |  |
|  |  |   | CONTENT |   |  |  |
|  |  |   +---------+   |  |  |
|  |  +-----------------+  |  |
|  +-----------------------+  |
+-----------------------------+
```

**Margin:** Jarak di luar border.

**Padding:** Jarak antara border dan konten.

Contoh:

```css
.card {
  padding: 20px;
  margin: 10px;
}
```

Coba ubah:

```css
padding: 20px;
```

Menjadi:

```css
padding: 50px;
```

Apa yang terjadi?

Ruang di dalam card menjadi lebih besar.

## 4.5 Live Demo — Styling Website

Buka file `style.css`.

### Step 1 — Global Styling

```css
* {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f8fafc;
  color: #1e293b;
}

a {
  text-decoration: none;
}
```

Perhatikan perubahan font dan margin pada halaman.

### Step 2 — Container

```css
.container {
  width: 90%;
  max-width: 1000px;
  margin: 0 auto;
}
```

Container membantu membatasi lebar konten agar tidak memenuhi seluruh layar desktop.

### Step 3 — Hero Section

```css
.hero {
  background: #dbeafe;
  padding: 80px 0;
}

.hero h1 {
  font-size: 44px;
  margin-bottom: 16px;
}

.hero p {
  font-size: 18px;
  color: #475569;
  margin-bottom: 30px;
}
```

Sekarang bagian hero sudah memiliki background dan teks yang lebih besar.

### Step 4 — Button

```css
.button {
  display: inline-block;
  background: #2563eb;
  color: white;
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: bold;
}

.button:hover {
  background: #1d4ed8;
}
```

Coba arahkan mouse ke tombol.

Warna tombol akan berubah karena selector `:hover`.

**Eksperimen:**

Ubah warna tombol menjadi merah, hijau, atau warna pilihan masing-masing.

---

# Chapter 5 — Layout: Biar Nggak Berantakan

**Durasi: 10 menit**

Kita sudah membuat website dengan HTML dan memberinya styling menggunakan CSS.

Namun, beberapa elemen masih tersusun secara default.

Sekarang kita akan belajar mengatur posisinya.

## 5.1 Flexbox

Flexbox adalah sistem layout CSS untuk mengatur elemen dalam satu arah utama.

Contoh:

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

Penjelasan:

- `display: flex` mengaktifkan Flexbox.
- `justify-content` mengatur distribusi pada sumbu utama.
- `align-items` mengatur posisi pada sumbu silang.

### Live Demo

Tambahkan kode berikut ke `style.css`:

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
}

.navbar a {
  color: #1e293b;
}

.logo {
  font-size: 20px;
  font-weight: bold;
}
```

Sekarang logo berada di kiri dan menu berada di kanan.

Coba ubah:

```css
justify-content: space-between;
```

Menjadi:

```css
justify-content: center;
```

Perhatikan perubahannya.

## 5.2 CSS Grid

CSS Grid digunakan untuk membuat layout berbasis baris dan kolom.

Contoh:

```css
.card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}
```

Penjelasan:

- `display: grid` mengaktifkan CSS Grid.
- `repeat(3, 1fr)` membuat tiga kolom sama lebar.
- `gap` membuat jarak antar-card.

### Live Demo — Card Layout

Tambahkan:

```css
#materi {
  padding: 50px 0;
}

.card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.card {
  background: white;
  padding: 24px;
  border: 1px solid #e2e8f0;
  border-radius: 12px;
}

.card h3 {
  margin-top: 0;
}

.card p {
  color: #64748b;
}
```

Sekarang ketiga card tersusun berdampingan.

### Eksperimen

Ubah:

```css
grid-template-columns: repeat(3, 1fr);
```

Menjadi:

```css
grid-template-columns: repeat(2, 1fr);
```

Amati bagaimana jumlah kolom berubah.

## 5.3 Responsive Design

Bagaimana kalau website dibuka melalui HP?

Kalau layout desktop dipaksakan ke mobile, konten bisa menjadi terlalu sempit.

Solusinya adalah responsive design.

Kita dapat menggunakan media query.

```css
@media (max-width: 768px) {
  .card-grid {
    grid-template-columns: 1fr;
  }

  .hero {
    padding: 50px 0;
  }

  .hero h1 {
    font-size: 30px;
  }
}
```

Kode di atas akan diterapkan ketika viewport berukuran 768px atau kurang.

### Live Demo — Desktop vs Mobile

1. Buka website di browser.
2. Tekan `F12`.
3. Aktifkan Device Toolbar.
4. Ubah ukuran layar ke mobile.
5. Perhatikan bagaimana tiga card menjadi satu kolom.

Website yang tadinya tiga kolom sekarang menyesuaikan ukuran layar.

---

# Chapter 6 — Mini Challenge

**Durasi: 5 menit**

Sekarang giliran kalian.

Kita sudah membuat website bersama. Berikutnya, ubah tampilannya sesuai kreativitas masing-masing.

## Challenge 1 — Ganti Identitas Website

Ubah:

```html
<h1>Hello, Future Developer!</h1>
```

Menjadi judul pilihan kalian.

Contoh:

```html
<h1>Selamat Datang di Website Saya!</h1>
```

## Challenge 2 — Ganti Warna

Ubah:

```css
.hero {
  background: #dbeafe;
}
```

Menjadi warna lain.

Contoh:

```css
.hero {
  background: #fce7f3;
}
```

## Challenge 3 — Buat Card Lebih Menarik

Tambahkan efek hover:

```css
.card {
  transition: transform 0.2s;
}

.card:hover {
  transform: translateY(-5px);
}
```

Arahkan mouse ke card dan perhatikan perubahannya.

## Challenge 4 — Tambahkan Card Baru

Tambahkan satu card HTML:

```html
<article class="card">
  <h3>JavaScript</h3>
  <p>
    Membuat website menjadi interaktif.
  </p>
</article>
```

Perhatikan bagaimana CSS Grid mengatur card baru tersebut.

---

# Quick Review

Sebelum selesai, coba jawab pertanyaan berikut.

**1. Apa itu tag HTML?**

Tag adalah penanda yang digunakan untuk membentuk elemen HTML.

**2. Apa perbedaan `<h1>` dan `<p>`?**

`<h1>` digunakan untuk heading utama, sedangkan `<p>` digunakan untuk paragraf.

**3. Apa fungsi `class`?**

Memberikan pengenal yang dapat digunakan berulang untuk memilih elemen, termasuk saat menulis CSS.

**4. Apa perbedaan HTML dan CSS?**

HTML mengatur struktur dan makna konten, sedangkan CSS mengatur tampilannya.

**5. Apa perbedaan margin dan padding?**

Margin mengatur jarak luar elemen, sedangkan padding mengatur jarak dalam elemen.

**6. Apa fungsi `display: flex`?**

Mengaktifkan Flexbox untuk mengatur layout elemen.

**7. Apa fungsi media query?**

Menerapkan aturan CSS berdasarkan kondisi tertentu, seperti lebar viewport.

---

# Troubleshooting

### Website Tidak Berubah?

Pastikan sudah menyimpan file menggunakan `Ctrl + S`, kemudian refresh browser.

### CSS Tidak Berfungsi?

Periksa apakah file CSS sudah dihubungkan:

```html
<link rel="stylesheet" href="style.css">
```

### Class Tidak Sesuai?

HTML:

```html
<div class="card"></div>
```

CSS:

```css
.card {
  background: white;
}
```

Nama class harus sesuai.

### Layout Berantakan?

Periksa kembali:

- Nama class HTML dan CSS.
- Penulisan `{` dan `}` pada CSS.
- Penggunaan `display: flex` atau `display: grid`.
- Aturan media query.
- CSS lain yang mungkin menimpa styling.

---

# What's Next?

Setelah memahami HTML dan CSS, kita bisa melanjutkan ke:

1. HTML Forms
2. Advanced Flexbox & CSS Grid
3. CSS Animation
4. JavaScript Fundamentals
5. DOM Manipulation
6. Membuat Website Interaktif

## References

- [MDN — HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [MDN — CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [MDN — HTML Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements)
- [MDN — Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout)
- [MDN — CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout)

---

## Final Project

```text
web-forge/
├── index.html
└── style.css
```

Dalam 60 menit, kita telah membuat website yang memiliki struktur HTML, styling CSS, navigasi, card, dan layout responsif.

Dari halaman polos menjadi landing page yang dapat ditampilkan di desktop maupun mobile.

**HTML membuatnya ada. CSS membuatnya enak dilihat.**
