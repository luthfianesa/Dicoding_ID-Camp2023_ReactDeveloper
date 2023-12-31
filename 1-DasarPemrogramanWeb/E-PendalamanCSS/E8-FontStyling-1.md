## E8.1 Font Family

- Digunakan untuk menetapkan jenis font yang akan diterapkan pada target.
- Untuk menuliskan lebih dari satu nilai font, berikut adalah aturan yang harus kita perhatikan.
  - font-family: value1, value2, value3;
  - Seluruh nilai font yang bukan merupakan generic font families harus dituliskan secara kapital
    - Contohnya, “Arial” bukan dituliskan “arial”.
  - Gunakan tanda koma (,) untuk memisahkan antara nilai font yang digunakan.
  - Selalu tanda kutip (“) untuk membungkus nilai font yang memiliki spasi pada namanya.
    - Contohnya “Open Sans”.
- Mungkin kita bertanya-tanya mengapa **perlu memberikan lebih dari satu nilai pada font-family**?
- Hal tersebut penting karena **tidak semua browser mendukung semua jenis font**.
- Bagaimana urutan prioritasnya? Dimulai dari jenis font yang pertama dituliskan.
- Jika font pertama didukung oleh browser, ia akan digunakan.
- Jika tidak, lantas browser akan memeriksa nilai font yang kedua dst
- Hal yang perlu kita perhatikan adalah pastikan untuk **menggunakan generic font families pada akhir nilai properti font-family**.
- Nilai ini dipastikan didukung oleh seluruh browser saat ini.
- Berikut adalah nilai-nilai generic font families yang dapat kita gunakan untuk **fallback mechanism**.
  - **Serif**: jenis font yang memiliki runcing pada garis akhir karakternya. Times New Roman merupakan salah satu jenis serif font.
  - **Sans-serif**: jenis font yang tidak meruncing pada garis akhir karakternya. Contohnya, “Open Sans”, “Fira Sans” dan lainnya.
  - **Monospace**: jenis font yang memiliki nilai lebar tiap karakternya sama. Consolas merupakan salah satu jenisnya.
  - **Cursive**: jenis font yang tampak seperti handwriting atau hasil tulisan tangan.
  - **Fantasy**: jenis font yang merepresentasikan karakteristik yang menyenangkan.
  - **System-ui**: jika menerapkan nilai ini maka font yang diterapkan akan sama seperti font yang digunakan pada sistem operasi kita.
  - **Math**: jenis font yang digunakan untuk penulisan rumus-rumus matematika.
  - **Emoji**: jenis font yang digunakan untuk menampilkan emoji.
  - **Fangsong**: jenis font yang menampilkan gaya penulisan Chinese.

## E8.2 Font Size

- Digunakan untuk menentukan ukuran pada teks.
- Hal yang perlu kita perhatikan adalah ketika menuliskan nilai dan satuannya. Pastikan tidak ada jarak (spasi) di antaranya.
- Satuan dalam menetapkan ukuran font terbagi **dua jenis**.
  - **Relative Unit**
    - Satuan yang nilainya **tergantung pada suatu hal**. Contohnya, ukuran viewport, induk elemen, atau ukuran teks standar.
  - **Absolute Unit**
    - Satuan yang nilainya telah ditentukan atau **digunakan dalam dunia nyata**.
- Berikut adalah daftar satuan dalam menetapkan ukuran font.
  - **Relative Unit**
    - **em**
      - Relatif terhadap font size
      - Jika 2em berarti 2 kali lebih besar dari ukuran font
    - **ex**
      - Relatif terhadap font height
      - Sangat jarang digunakan
    - **rem**
      - Relatif terhadap font size
      - Mirip em, rem satuan relatif terhadap font dari root element
    - **ch**
      - Relatif terhadap font width
      - Satuan relatif terhadap lebar dari karakter "0"
    - **vw**
      - Relatif terhadap viewport width
      - Satuan relatif terhadap 1% lebar viewport.
      - Contoh : 1vw = 1% dari lebar viewport
      - Tidak didukung browser IE8 kebawah
    - **vh**
      - Relatif terhadap viewport height
      - Satuan relatif terhadap 1% tinggi viewport.
      - Contoh : 1vh = 1% dari tinggi viewport
      - Tidak didukung browser IE8 kebawah
  - **Absolute Unit**
    - **px**
      - Nilai font berdasarkan ukuran pixel
    - **pt**
      - Nilai font berdasarkan points (1/72 inch di CSS2.1)
    - **pc**
      - Nilai font berdasarkan picas (1 pica = 12 point)
    - **mm**
      - Nilai font berdasarkan milimeters
    - **cm**
      - Nilai font berdasarkan centimeters
    - **in** - Nilai font berdasarkan inches
      <br>
- Kita juga bisa menetapkan nilai ukuran font dengan persentase %
- Hal yang terakhir, kita juga bisa menentukan ukuran font dengan menuliskan kata kunci secara spesifik yang tersedia pada CSS.
- Kata kunci tersebut: xx-small, x-small, small, medium, large, x-large, dan xx-large.
- Kata kunci di atas tidak ada kaitannya dengan pengukuran tertentu (bukan ukuran yang absolute), tetapi nilainya diubah secara konsisten satu sama lain.
- Kita bisa lihat bahwa **standarnya browser menampilkan teks dengan nilai medium**.
