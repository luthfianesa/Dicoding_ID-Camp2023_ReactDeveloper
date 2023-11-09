## 18.1 Dimension

- Standarnya, sebuah box yang dihasilkan tiap elemen selalu cukup untuk menampung konten.
- Namun, kita dapat mengatur nilai dimensi dari box tersebut dengan properti **width** dan **height**.
- Cara yang paling banyak digunakan dalam menentukan dimensi kotak adalah menggunakan piksel (**px**), persentase, atau ems.
- Secara tradisional, piksel merupakan cara yang paling populer karena kita dapat merancang dan **mengontrol ukuran secara akurat**.
- Berbeda ketika kita menggunakan persentase, ukuran kotak akan relatif atau menyesuaikan dari ukuran lain, seperti ukuran jendela browser atau ukuran induk yang menaunginya.
- Namun ketika menggunakan ems, nilai dimensi kotak akan menyesuaikan berdasarkan ukuran teks yang ditampilkan pada konten elemen tersebut.
- Pada saat ini, **banyak developer mulai merancang menggunakan persentase dan ems** untuk menetapkan ukuran box agar dapat **menyesuaikan dengan berbagai macam ukuran layar**.

## 18.2 Limiting Dimension

- Beberapa website yang ada sekarang menampilkan layout yang dapat melebar dan menyempit mengikuti ukuran layar pengguna.
- Pada prinsip tampilan tersebut, mungkin kita memerlukan sebuah **limitasi ukuran** yang harus ditetapkan agar **konten selalu ditampilkan secara proporsional**.
- Untuk melakukannya kita manfaatkan properti **min-width** dan **max-width**.
  - **min-width**: menetapkan nilai lebar minimal yang harus dimiliki elemen.
  - **max-width**: menetapkan nilai lebar maksimal yang harus dimiliki elemen.
- Keduanya merupakan properti yang sangat membantu untuk memastikan konten halaman dapat terbaca oleh pengguna (terutama ketika pengguna menggunakan ponsel).
- Dengan cara yang sama, mungkin kita juga perlu membatasi ukuran panjang.
- Kita bisa gunakan **min-height** dan **max-height**.

## 18.3 Overflowing Content

- Dimensi box yang dihasilkan elemen selalu cukup untuk menampung konten, tetapi hal ini tidak berlaku jika kita tetapkan secara manual panjang dan lebarnya.
- Tak jarang terjadi overflow ketika kita menerapkan ukuran pada elemen dengan konten di dalamnya yang begitu banyak.
- Berikut nilai - nilai dari properti overflow :
  - **Visible**
    - Nilai default dari properti overflow
    - Konten yang tidak tertampung akan tetap terlihat
  - **Hidden**
    - Jika konten tidak tertampung, maka akan disembunyikan
  - **Scroll**
    - Memunculkan scroll bar walaupun konten tidak overflow
  - **Auto**
    - Sama seperti scroll, tetapi akan visible ketika konten tidak overflow

## 18.4 Box Sizing

- Sebelum CSS3, ukuran lebar dan panjang elemen mengacu pada konten elemen (content-box).
- Itu berarti ukuran elemen seluruhnya merupakan nilai panjang (width) dan lebar (height) yang kita spesifikasikan ditambah dengan nilai padding dan border yang diterapkan pada elemen.
- Hal tersebut membuat sebagian developer menjadi sulit dalam menetapkan ukuran dimensi.
- Pada CSS3, kita dapat memilih tipe pengukuran lain dalam menentukan dimensi elemen.
- Dengan menggunakan properti box-sizing, kita dapat menentukannya berdasarkan border box.
- Ukuran elemen sudah termasuk content, padding, dan border.
- Dengan metode ini, hasil elemen yang ditampilkan (termasuk padding dan border) akan memiliki dimensi yang sama persis seperti yang kita tentukan.
