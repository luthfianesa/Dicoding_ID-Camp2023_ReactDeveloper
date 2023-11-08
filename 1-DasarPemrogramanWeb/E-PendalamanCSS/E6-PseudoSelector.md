## E6.1 Pseudo Selector

- CSS masih memiliki dua selector lagi yang dapat kita manfaatkan untuk membantu menyeleksi elemen dalam menerapkan sebuah rule, yakni **pseudo-class** dan **pseudo-element**.
- Selector ini **menargetkan elemen pada bagian yang “tidak terlihat”**, seperti sifat pada elemen sehingga untuk menetapkannya tidak bisa menggunakan selector biasa.
- Salah satu contoh yang paling sering kita terapkan adalah :hover

## E6.2 Pseudo-Class Selector

- Pseudo-class merupakan sebuah class “semu” yang sebenarnya ada pada tiap elemen HTML.
- Dengan menggunakan selector ini kita dapat memilih elemen berdasarkan class yang tidak tampak pada dokumen.
- Kita bisa menetapkan rule hanya ketika sebuah tautan telah dikunjungi **:visited** atau ketika sebuah elemen diarahkan dengan kursor **:hover**.
- Untuk menggunakan pseudo-class, kita gunakan tanda **titik dua (:)** pada basic selector dan diikuti dengan pseudo-class-nya.

## E6.3 Pseudo-Elemen Selector

- Sama seperti pseudo-class, pseudo-element merupakan sebuah elemen “semu” yang sebenarnya ada, tetapi tidak tampak secara tertulis pada berkas HTML.
- Selector ini biasa digunakan ketika kita ingin menambahkan konten tepat sebelum dan setelah sebuah elemen paragraf.
- Yup, kita tidak perlu menuliskan elemen/konten baru pada berkas HTML untuk menambahkan konten.
- Namun, kita dapat memanfaatkan pseudo-element untuk melakukannya.
- Pseudo-element yang dimaksud adalah **::before** dan **::after**.
