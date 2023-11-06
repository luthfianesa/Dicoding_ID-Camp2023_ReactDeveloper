## C14.1 Input Element

- Elemen `<input>` merupakan elemen yang sangat sering dipakai untuk **mendapatkan data dari user**. - - Mengapa hal tersebut terjadi? Hal ini karena **elemen input memiliki banyak sekali tipe-tipenya**, mulai dari teks, password, email, search, file, dsb.
- Tidak hanya itu, dari sekian tipe input, masing-masingnya juga **didukung oleh atribut khusus** sehingga pembuatan formulir semakin powerful.
- Beberapa tipe - tipe input pada html :

  - **`<input type="text">`**

    - Input teks yang berisi satu baris.
    - Ini adalah tipe default dari input elemen.

  - **`<input type="number">`**

    - Input teks yang hanya mengizinkan format angka.

  - **`<input type="password">`**

    - Setiap karakter akan ditampilkan sebagai bintang.

  - **`<input type="email">`**

    - Input ini dikhususkan untuk format email. Jika tidak, error akan muncul.

  - **`<input type="search">`**

    - Input untuk melakukan pencarian berdasarkan kata kunci.
    - Input ini memiliki ikon ✕ di tepi kanan elemen untuk melakukan clear text.

  - **`<input type="date">`**

    - Untuk mengambil data tanggal.
    - Tipe ini akan menyediakan popup penanggalan untuk mempermudah pengisian.

  - **`<input type="time">`**

    - Menentukan waktu (jam) yang ingin user isi.
    - Tipe input ini juga akan menampilkan visual dari jam.

  - **`<input type="datetime-local">`**

    - Sama seperti tipe date, tetapi ia menambahkan data waktu (jam).

  - **`<input type="checkbox">`**

    - Di-render sebagai sebuah kotak yang dapat dicek untuk active.

  - **`<input type="radio">`**

    - Melakukan pemilihan dari sekian opsi (radio button) yang ada.
    - Untuk melakukannya, input ini akan dikelompokkan dalam sebuah radio group.

  - **`<input type="range">`**

    - Menentukan nilai angka berdasarkan jangkauan nilai yang ditentukan.
    - User tidak akan bisa mengambil nilai diluar yang ditentukan.

  - **`<input type="color">`**

    - User dapat menentukan warna dengan tipe ini.
    - Menggunakan color picker atau memasukkan format nilai warna secara manual.

  - **`<input type="file">`**

    - Melakukan input satu atau lebih berkas dari penyimpanan data perangkatnya.

  - **`<input type="submit">`**

    - Input yang di-render sebagai tombol submit.
    - Jika tombol ini ditekan, formulir akan ter-submit dan dikirimkan ke tujuan pengiriman (atribut action).

  - **`<input type="hidden">`**

    - Biasanya, tipe ini tidak terlihat oleh user.
    - Namun, input ini akan sangat berguna bagi developer untuk memasukkan suatu data.

## C14.2 Non-Single Line Input Element

- Pernahkah Anda melihat kolom input yang dapat **menuliskan banyak baris teks**?
- Biasanya, ini dibutuhkan pada beberapa kasus, seperti membuat komentar, catatan, deskripsi, dsb. Nah,
- HTML memiliki elemen khusus yang **memungkinkan user menuliskan teks dalam banyak baris**.
- Elemen **`<textarea>`** ini berbeda dengan elemen input sebelumnya.
- Selain nama elemen yang menjadi pembeda, elemen **textarea memiliki tag penutup agar** dapat berfungsi dengan baik.

## C14.3 Label Element

- Elemen input yang berasosiasi dengan elemen label akan **memberikan kemampuan bagi screen reader untuk menjelaskan fungsi dari elemen input** tersebut.
- Dalam hal ini, akan **meningkatkan aksesibilitas**.
- Tentunya, ini akan sangat **bermanfaat bagi penyandang disabilitas**.
- Memberikan kemampuan bagi browser untuk mengalihkan langsung pada elemen input saat elemen label yang berasosiasi dengannya ditekan atau klik.
- Ada **dua langkah untuk menghubungkan elemen label dan input**.
  - Pertama, menambahkan **atribut id** pada elemen **input** beserta value-nya.
  - Kedua, menambahkan **atribut for** pada elemen **label** dan value-nya.
- Apakah sudah selesai sampai sini? Jawabannya, belum.
- Kita perlu memberikan value yang sama pada kedua atribut (id dan for).
- Dengan cara ini, elemen label akan berasosiasi dengan elemen input.
