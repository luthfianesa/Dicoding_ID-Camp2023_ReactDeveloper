## C13.1 Tabel

- Ada beberapa jenis informasi yang perlu ditampilkan dalam bentuk tabel, contohnya klasemen olahraga atau sebuah jadwal layaknya kalender.
- Ketika kita membuat sebuah tabel, pastinya kita akan banyak bermain dengan **baris** dan **kolom**.
- Elemen `<table>` pada HTML merepresentasikan data tabular, yaitu informasi yang disajikan dalam sebuah tabel.

## C13.2 Struktur Dasar Tabel

- Tabel pada HTML disusun dari **tiga buah elemen**, yaitu
  - `<table>`
  - `<tr>`
  - `<td>` atau `<th>`.
- Elemen **`<table>`** digunakan untuk **menandakan dimulainya dan diakhirinya sebuah konten tabel** dan juga sebagai **wadah untuk tabel** itu sendiri.
- Kemudian elemen **`<tr>`** digunakan untuk **membuat sebuah baris baru** yang di dalamnya terdapat elemen `<td>` atau `<th>` sehingga menghasilkan sebuah sel.
- Elemen **`<td>`** berarti “table data”. Selain membuat sel, elemen ini juga merupakan tempat **menampung data pada tabel**, dan elemen **`<th>`** atau “table header” digunakan untuk **menentukan sebuah header pada kolom datanya**.

## C13.3 Spanning Cell

- Terkadang kita membutuhkan sebuah sel untuk **mencakup dua kolom ataupun dua baris sekaligus**.
- Dalam aplikasi seperti Microsoft Word, hal ini biasa kita kenal sebagai **merging cell** atau **menggabungkan sebuah sel**.
- Pada HTML hal ini lebih dikenal sebagai spanning cell, yang artinya **menjangkau atau merentangkan sebuah ukuran sel lebih dari ukuran yang biasanya**.
- Dengan spanning cell, kita dapat membuat sebuah tabel yang lebih kompleks, tetapi akan membuat markup yang kita tulis menjadi sedikit sulit dibaca.

## C13.4 Column Spans

- Untuk merentangkan sebuah kolom (column spanning) kita bisa menggunakan **atribut colspan** pada elemen `<td>` atau `<th>`
- Sebuah elemen yang menggunakan atribut colspan akan mencakup ruang kolom sesuai nilai dari atribut itu sendiri.

## C13.5 Row Spans

- Untuk merentangkan sebuah baris (row spanning) kita dapat menggunakan **atribut rowspan**.
- Mirip seperti column spanning, tetapi atribut ini akan **merentangkan sebuah sel ke bawah**.

## C13.6 Elemen dan Atribut Pada Tabel

- **table** -> Menetapkan elemen tabel
- **td** -> Menetapkan sebuah sel dalam baris tabel
  - _colspan_="number" -> Jumlah kolom yang dicakup oleh sel
  - _rowspan_="number" -> Jumlah baris yang dicakup oleh sel
  - _headers_="nama header" -> Mengasosiasikan data sel dengan header
- **th** -> Menetapkan header yang terkait dengan baris atau kolom
  - _colspan_="number" -> Jumlah kolom yang dicakup oleh header
  - _rowspan_="number" -> Jumlah baris yang dicakup oleh header
  - _headers_="nama header" -> Mengasosiasikan header dengan header lain
  - _scope_=”row|col|rowgroup|colgroup” -> Mengasosiasikan header dengan baris, kelompok baris, kolom, atau kelompok kolom.
- **tr** -> Menetapkan sebuah baris pada tabel.
- **caption** ->Memberikan judul pada sebuah tabel.
- **col** -> Menetapkan sebuah kolom.
- **colgroup** -> Menetapkan sebuah kelompok kolom.
- **tbody** -> Mengidentifikasi sebuah body dalam tabel.
- **tfoot** -> Mengidentifikasi sebuah footer dalam tabel.
- **thead** -> Mengidentifikasi sebuah header dalam tabel.
