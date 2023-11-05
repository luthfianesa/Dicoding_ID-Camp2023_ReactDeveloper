## C7.1 Anchor

- Apa itu anchor? Anchor (jangkar) merupakan elemen yang digunakan untuk **membuat sebuah hyperlink ke halaman atau website lain**, file, alamat email, atau URL lainnya.
- Untuk menggunakan elemen ini kita gunakan `<a> `sebagai tag pembuka dan `</a>` sebagai tag penutup. - - Selain itu, ada atribut wajib agar elemen ini berfungsi dengan baik, yaitu **href** untuk **menetapkan sebuah target yang dituju**.
- Berikut adalah daftar atribut khusus yang dapat digunakan pada elemen ini.
  - Download -> Menginstruksikan browser untuk mengunduh pada URL yang ditetapkan daripada mengarahkannya.
  - **href** -> Menetapkan target yang akan diarahkan/unduh ketika pengguna menekan hyperlink.
  - **hreflang** -> Menetapkan bahasa dari dokumen target.
  - **ping** -> Menetapkan URL yang akan diberitahu dengan mengirimkan post request ping pada body oleh browser (berjalan di belakang layar) ketika target URL pada hyperlink ditekan. Biasanya atribut ini digunakan untuk pelacakan.
  - **referrerpolicy** -> Menetapkan referensi untuk dikirim pada target
  - **rel** -> Menetapkan hubungan antara halaman yang ditampilkan dengan target.
  - **target** -> Menetapkan lokasi ketika membuka target contohnya pada sebuah tab, window, atau tab itu sendiri.
  - **media** -> Menetapkan tipe media yang digunakan pada target.

## C7.2 Emphasized Text

- Gunakan elemen `<em>` untuk menunjukkan bagian kata yang perlu kita tekankan. 
- Elemen ini menunjukkan stress emphasis atau konten/kata yang perlu mendapatkan penekanan atau 
- Standarnya, pada browser sebuah kata yang ditekankan akan ditampilkan dalam *gaya miring* pada teksnya.

## C7.3 Important Text
- Gunakan elemen `<strong>` untuk menunjukkan sebuah teks yang begitu penting (strong importance), serius ataupun mendesak. 
- Artinya, teks tersebut harus dapat perhatian lebih dari teks biasa lainnya.
- Standarnya, pada browser sebuah teks yang diberi markup `<strong>` akan ditampilkan **tebal**.

## C7.4 Short Quotation

- Gunakan elemen `<q>` untuk menandai sebuah kutipan dalam sebuah teks. 
- Elemen ini berbeda dengan `<blockquote>`. 
- Elemen ini digunakan untuk **kutipan pendek** yang terletak di dalam baris (inline).
- Standarnya, sebuah teks yang diberi markup <q> akan ditampilkan di dalam **tanda kutip** (quotation marks) pada browser.