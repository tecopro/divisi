# Instruksi Pembelajaran

## Pengertian
HTML singkatan dari _Hyper Text Markup Language_, merupakan bahasa _markup_ standard untuk membangun website. Bahasa ini mendeskripsikan struktur atau kerangka dari sebuah website menggunakan serangkaian elemen. Elemen tersebut memberi tahu browser bagaimana cara menampilkan sebuah konten menggunakan label.

Saat ini, HTML5 memiliki sekitar 100 tag. Tag tersebut berfungsi sebagai penanda, beberapa diantaranya antara lain `judul`, `paragraf`, atau `tautan`. Secara berurutan, tag yang digunakan adalah **_heading_** (`h1` - `h6`), **_paragraph_** (`p`), dan **_anchor_** (`a`).

## Struktur
HTML sendiri memiliki 4 elemen yang harus ada pada setiap file/dokumen.

```html
<!DOCTYPE html>
<html>
  <head>
    ...
  </head>
  <body>
    ...
  </body>
</html>
```
1. Tag `<!DOCTYPE html>` merupakan bagian deklarasi yang menjelaskan bahwa dokumen ini ditulis menggunakan bahasa HTML5.
2. Tag `<html>` merupakan elemen utama / elemen akar, dari halaman HTML.
3. Tag `<head>` merupakan elemen yang menampung informasi tentang halaman HTML. Informasi yang sering ditampilkan adalah `<title>` biasanya tertera pada bagian judul tab browser, dan juga `<meta>` yang digunakan untuk mendeklarasikan sebuah informasi.
4. Tag `<body>` merupakan bagian deklarasi yang menjelaskan bahwa tag ini menjadi sebuah wadah untuk semua jenis konten yang dapat dilihat atau ditampilkan. Jenis konten tersebut antara lain judul, paragraf, gambar, video, musik, tautan, tabel, dan masih banyak lagi.
5. 
---

Adapun struktur HTML5 pada _template_ VS Code, sebagai berikut :

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>...</title>
  </head>
  <body>
    ...
  </body>
</html>
```

## Elemen HTML
Pada HTML5 pendeklarasian suatu tag diawali dengan tag pembuka (`<tag>`), kemudian diisi konten, dan ditutup dengan tag penutup (`</tag>`).

```html
<tag> Konten </tag>
```

Ada yang tahu, perbedaan elemen dan tag?

| Elemen |
| - |
| <table><tr><th>Tag Pembuka</th><th>Konten</th><th>Tag Penutup</th></tr><tr align="center"><td><code>&lt;tag&gt;</code></td><td>Lorem ipsum dolor...</td><td><code>&lt;&#47;tag&gt;</code></td></tr><tr align="center"><td><code>&lt;hr&gt;</code></td><td>-</td><td>-</td></tr></table> |

## Jenis-jenis Elemen HTML

### Heading
Tag _heading_ terdiri dari `<h1>` sampai `<h6>`. Tag `<h1>` merupakan judul halaman yang paling penting atau teratas, sedangkan tag `<h6>` merupakan judul halaman yang tidak terlalu penting.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

_Heading_ sering digunakan mesin pencari untuk mengindeks struktur dan konten dari halaman website. Hal ini selaras dengan seringnya pengguna yang hanya membaca sepintas suatu situs/website berdasarkan judulnya.

> Catatan : Gunakan _heading_ hanya untuk membuat judul. Jangan memakai _heading_ untuk membuat tulisan **BESAR** dan **TEBAL**

### Paragraph
Tag _paragraph_ atau `<p>` merupakan elemen yang berupa suatu paragraf. Elemen ini selalu membuat baris baru, dan biasanya browser memberikan jarak sebelum dan sesudah paragraf secara otomatis.

```html
<p>Lorem ipsum dolor sit amet...</p>

<p>Tempora nesciunt molestias minima est ut...</p>
```

### Horizontal Rules
Tag `<hr>` berfungsi untuk memisahkan konten (atau menentukan perubahan) pada halaman HTML.

```html
<p>Similique provident possimus numquam...</p>
<hr>
<p>Similique numquam incidunt in et odio quod alias...</p>
```

### Line Breaks
Tag `<br>` berfungsi untuk membuat jeda baris (baris baru) tanpa memulai paragraf baru.

```html
<p>Earum quidem libero nulla sapiente natus maxime unde ipsum nam.<br>Commodi quo soluta minima recusandae excepturi ea...</p>
```

### Preformatted Text
Teks di dalam tag `<pre>` ditampilkan dengan lebar tetap dan biasanya ditampilkan memakai font Courier, serta mempertahankan spasi dan jeda baris. Tag ini cocok digunakan untuk menulis puisi.

```html
<pre>
  Ayahku... suami ibuku,
  
  ayahnya kakakku, ayahnya adikku.
  
  Ayahku...
  
  anaknya kakekku, anaknya neneku.
  
  Ayahku... ialah ayahku.
</pre>
```

### Formatting Elements

#### Bold and Important
- Tag `<b>` menampilkan teks dalam huruf tebal, tanpa memiliki arti penting.

- Sedangkan tag `<strong>` membuat teks memiliki arti penting yang tidak bisa diabaikan, biasanya konten ditampilkan dalam huruf tebal.

```html
Nama kucing-ku adalah <b>anjing</b>

<strong>Anjing</strong> adalah nama dari kucing-ku
```

#### Italic and Emphasized
- Tag `<i>` menampilkan teks yang dalam huruf miring. Biasanya digunakan untuk menunjukkan istilah teknis, frasa dari bahasa asing, pemikiran, nama kapal, dan lain-lain.

- Sedangkan tag `<em>` membuat teks memiliki penekanan suara dalam pengucapan, biasanya konten ditampilkan dalam huruf miring.

```html
Pada kasus polisi tembak polisi, diduga tersangka FS melakukan <i>obstruction of justice</i>

Harga BBM kembali naik, <em>apakah ekonomi rakyat akan jatuh</em>?
```

#### Underline and Insert
- Tag `<u>` menampilkan teks yang bergaris bawah, tanpa memiliki arti penting.

- Sedangkan tag `<ins>` menampilkan teks yang bergaris bawah dan menandakan bahwa elemen ini baru ditambahkan pada dokumen.

```html
Siapa sangka? <u>Marshel Widianto</u> dan <u>Celine Evangelista</u> dikabarkan akan menikah!

Selain kasus penembakan, terdakwa FS diduga merangkap ke ranah judi online <ins>dan LGBT?!</ins>
```

#### Striked and Deleted
- Tag `<s>` menampilkan teks yang dicoret garis lurus, tanpa memiliki arti penting.

- Sedangkan tag `<del>` menampilkan teks yang dicoret garis lurus dan menandakan bahwa elemen ini telah dihapus dari dokumen.

```html
Buanglah sampah pada <s>temannya</s> tempatnya

Sofa <del>Mahabrata</del> Machabba Haeta
```

#### Subscript and Superscript
- Tag `<sub>` menampilkan teks subskrip dimana posisinya setengah karakter di bawah garis normal serta ditampilkan dengan ukuran yang lebih kecil. Tag ini bisa digunakan untuk menulis rumus kimia.
- Tag `<sup>` menampilkan teks superskrip dimana posisinya setengah karakter di atas garis normal serta ditampilkan dengan ukuran yang lebih kecil. Tag ini bisa digunakan untuk menulis catatan kaki.

```html
Thomsonite :<br>
NaCa<sub>2</sub>(Al<sub>5</sub>Si<sub>5</sub>O<sub>20</sub>) · 6H<sub>2</sub>O

Carbonate Ion :<br>
CO<sub>3</sub><sup>2−</sup>
```

### Blockquote
Tag `<blockquote>` menampilkan teks yang dikutip dari sumber lain.

```html
<blockquote cite="http://www.worldwildlife.org/who/index.html">
For 50 years, WWF has been protecting the future of nature. The world's leading conservation organization, WWF works in 100 countries and is supported by 1.2 million members in the United States and close to 5 million globally.
</blockquote>
```

### List
Tag `<ul>`, `<ol>`, dan `<li>` berfungsi untuk mengelompokkan satu set item ke dalam suatu daftar. Elemen ini terbagi menjadi 2 jenis, yaitu berurutan (_ordered_) dan tidak berurutan (_unordered_).

Perbedaan dari kedua jenis tersebut hanya pada penandaan, jika daftar berurutan menggunakan variasi angka, huruf, atau romawi sedangkan daftar tidak berurutan menggunakan lingkaran, kotak atau gambar.

```html
<ul>
  <li>Java</li>
  <li>Website</li>
  <li>Grafis</li>
  <li>Office</li>
  <li>MyOB</li>
  <li>Animasi</li>
  <li>Jaringan</li>
</ul>

<ol>
  <li>Java</li>
  <li>Website</li>
  <li>Grafis</li>
  <li>Office</li>
  <li>MyOB</li>
  <li>Animasi</li>
  <li>Jaringan</li>
</ol>
```

### Table
Ada 4 tag yang digunakan untuk membuat elemen ini yakni `<table>`, `<tr>`, `<th>`, dan `<td>`.

```html
<table>
  <tr>
    <th>...</th>
  </tr>
  <tr>
    <td>...</td>
  </tr>
</table>
```

Berikut merupakan contoh penggunaan elemen tabel :
```html
<table>
  <tr>
    <th>#</th>
    <th>Nama Lengkap</th>
    <th>Negara</th>
  </tr>
  <tr>
    <td>1.</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>2.</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>
```

Adapun cara lain untuk membuat tabel, dengan menambahkan tag `<thead>` dan `<tbody>` agar mudah dikategorikan.

```html
<table>
  <thead>
    <tr>
      <th>...</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>...</td>
    </tr>
  </tbody>
</table>
```