## C10.1 Header dan Footer

- Sebuah header dan footer utama yang muncul pada **awal** dan **akhir** di sebuah halaman `<body>`.
  - Header: pengantar atau pembuka konten dalam sebuah elemen `<article>` atau `<section>`.
  - Footer: catatan kaki pada sebuah elemen `<article>` atau `<section>`.
- Selain itu, elemen `<header>` dan `<footer>` dapat digunakan pada sebuah elemen `<article>` atau `<section>`.
- Header biasanya menampung judul dan penulis, footer dapat menampung sebuah link untuk membagikan artikel pada sebuah sosial media.
- Elemen `<header>` dan `<footer>` tidak boleh ditulis di dalam elemen `<header>` dan `<footer>` lainnya (bertumpuk/nested).

## C10.2 Main

- Element `<main>` digunakan untuk menampung/mewadahi **konten utama (dominan)** dalam `<body>`.
- Konten main dapat terdiri dari banyak section, ataupun artikel, atau konten apa pun di dalam elemen main, selama ia termasuk konten utama yang dimiliki oleh website.
- Karena elemen `<main>` berisi inti konten pada website, **jangan gunakan elemen main lebih dari satu pada berkas HTML**.

## C10.3 Nav

- Elemen `<nav>` digunakan untuk **menampung sebuah navigasi yang sifatnya penting (mayor)**, contohnya navigasi utama pada sebuah website.
- Namun, tidak menjamin pada sebuah website hanya ada satu navigasi. Contohnya, sebuah akhir artikel pada blog terdapat tautan navigasi menuju artikel yang dianggap relevan dengan artikel yang telah kita baca.
- Navigasi tersebut tidak dianggap sebagai navigasi yang penting sehingga kita tidak perlu menggunakan elemen `<nav>` untuk menampilkannya.
- Sebuah navigation sangat berguna untuk aksesibilitas website kita.
- Contohnya ketika pengguna website kita menggunakan screen reader dalam mengunjungi website, pengguna akan mudah mencari bagian yang dia inginkan tanpa harus menelusuri seluruh konten website.
