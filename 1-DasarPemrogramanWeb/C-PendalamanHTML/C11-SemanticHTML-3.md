## C11.1 Article

- Elemen `<article>` bertindak sebagai **container untuk independent content** pada sebuah halaman.
- Artinya konten utuh yang tidak terkait dengan konten lain, bisa saja sebuah artikel blog, komentar, forum post dan konten lainnya.
- Jika dalam sebuah halaman terdapat beberapa artikel, tiap artikel tersebut seharusnya berada pada elemen `<article>`nya masing-masing.
- Elemen `<article>` dapat berada pada elemen `<article>` lainnya (nested) selama artikel tersebut berkaitan dengan induk elemen `<article>` yang menampungnya.

## C11.2 Aside

- Elemen `<aside>` memiliki dua tujuan, tergantung kita menempatkannya di dalam sebuah elemen `<article>` atau tidak.
- Ketika elemen ini ditempatkan di dalam elemen `<article>`, elemen ini dapat berisi informasi yang berhubungan dengan artikel tersebut, tetapi bukan bagian dari konten artikelnya itu sendiri (dipisahkan dari konten utama).
- Ketika ditempatkan di luar elemen `<article>`, elemen ini dapat berisi informasi yang berhubungan pada keseluruhan halaman.
- Elemen `<aside>` **biasanya terletak di samping dari sebuah elemen yang menampungnya**.

## C11.3 Section

- Sebuah elemen yang \*\*memiliki kesamaan konten dan sebuah heading di dalamnya dapat dikelompokkan dengan menggunakan elemen `<section>`.
- Dengan begitu elemen ini dapat digunakan pada sebuah elemen `<article>` yang memiliki konten panjang dan berpotensi untuk dikelompokkan.
- Dalam sebuah `<section>` **sebaiknya terdapat elemen heading (h1-h6)**, yang menjadi elemen pertama yang dituliskan pada sebuah section untuk menunjukkan judul atau tema dari bagian konten yang dikelompokkan.
