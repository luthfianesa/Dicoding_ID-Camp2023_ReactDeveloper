## D5.1 Inheritance

- Styling HTML bersifat inheritance yang dapat **mewarisi properti style “tertentu”** pada suatu elemen ke elemen-elemen di dalamnya (**child-elements**).
- Contohnya, CSS rules yang ditetapkan untuk elemen `<body>` akan diterapkan pada seluruh child-elements secara otomatis.
- Contoh lainnya, CSS rules yang diterapkan pada elemen `<footer>` dengan properti color: white akan diterapkan pada seluruh elemen yang ada di dalamnya.
- Hal ini menjadi alasan memahami struktur dokumen itu penting.

## D5.2 Group Selector

- Jika beberapa selector yang berbeda **memiliki penerapan properti-propeti yang sama**, kita dapat menggabungkan selector tersebut menggunakan group selector.
- Hal ini dapat **meminimalisir penulisan kode yang berulang**.

## D5.3 Rule Order

- Sesuai dengan namanya, cascading artinya “mengalir”.
- Demikian halnya dengan alur kerja CSS dalam membaca kode, **mengalir dari atas ke bawah**.
- Oleh karena itu, kita harus **memperhatikan urutan dalam penulisan rules**, terutama saat terjadi sebuah konflik.
- Konflik dapat terjadi karena kita menerapkan beberapa styling pada satu dokumen HTML dan menimpa styling yang telah diterapkan sebelumnya.
- Contohnya, apa yang akan ditampilkan oleh browser ketika eksternal css mengharuskan elemen `<p> `menampilkan warna merah, tetapi pada internal css `<p>` harus menampilkan warna biru?
- Kembali pada alur kerja CSS yang membaca dari atas ke bawah sehingga warna yang akan diterapkan adalah warna yang paling akhir didefinisikan.
- Kita bisa membuat sebuah property styling dianggap penting oleh browser untuk diterapkan dan tidak memperhatikan urutan dengan menambahkan keyword !important pada akhir nilai propertinya.
- Gunakan !important ketika memang benar-benar dibutuhkan saja.
- Sebaiknya kita pahami aturan urutan pada CSS dengan baik sehingga meminimalisir penggunaan tanda tersebut.
