## A4.1 Web Server

- Ketika kita mencari sesuatu dalam internet, katakanlah search engine seperti google.com, ada data yang ditampilkan pada kita berdasarkan hasil pencariannya.
- Contoh lain, kita sedang membeli suatu produk di e-commerce. kita perlu mencarinya dalam kolom pencarian pada platform tersebut dan daftar produk yang relevan akan disajikan untuk kita.
- Namun, tahukah kita apa yang terjadi di belakang?
- Bagaimana data dapat diperoleh dan ditampilkan dalam website? Hal ini termasuk pada halaman web yang sedang kita akses.

## A4.2 Siklus Request dan Response

- Broswer dapat menampilkan website dengan baik karena mendapatkan data dari komputer lain yang biasa disebut dengan server.
- Bagi komputer yang mengakses website kita disebut sebagai client, atau dalam hal ini adalah browser yang melakukan permintaan data.
- Browser akan **mengirimkan sesuatu yang bernama request** pada server dan **menerima data dalam sesuatu yang bernama response** sebagai hasil tanggapan dari server. Data-data tersebut dapat berupa berkas HTML, CSS, JavaScript, dan aset-aset lain yang dibutuhkan untuk menampilkan website.
- Proses di atas dapat direpresentasikan dalam proses pemesanan makanan di suatu restoran.
- Untuk mendapatkan sajian makanan dan minuman (website), kita (client/user) perlu melakukan pesanan kepada pelayan restoran.
  - Pelayan tersebut dapat diwakili sebagai browser yang akan membuat pesanan (request) dan meneruskannya kepada seorang koki (server).
  - Hal ini seperti browser membuat request ke server saat user menggunakan URL pada address bar browser. Koki akan memproses pesanan tersebut dan segera menyediakan hasilnya (response).
  - Dalam waktu ini, kita harus menunggu beberapa saat.
  - Setelah itu, koki memberikan hasil pesanan kepada pelayan dan menyajikannya kepada kita.
  - Sekarang, kita dapat menikmati hasil hidangan tersebut (website).

## A4.3 Peranan Web Server

- Tidak sedikit orang mengira bahwa server adalah sebuah komputer dengan performa tinggi dan berukuran besar.
- Hal tersebut tidak sepenuhnya salah karena komputer server umumnya seperti demikian.
- Pengertian dari web server sebenarnya lebih merujuk pada **sebuah software yang dapat menghubungkan sebuah komputer dengan komputer lain**.
- Jadi, **peranan server mengacu pada fungsi dari sebuah komputer tersebut**.
- Berbicara mengenai **web server**, ia dapat **terbagi menjadi dua** hal, yaitu **hardware dan software**.
- Bukan berarti kedua hal tersebut bekerja secara terpisah, tetapi saling melengkapi dan bekerja sama.

  - Dari sisi **hardware**, web server merupakan **komputer dengan spesifikasi yang disesuaikan berdasarkan layanannya**.

    - Contohnya, kapasitas hard drive yang besar akan dibutuhkan jika Anda memiliki website yang menyimpan banyak gambar,
    - Processor bertenaga tinggi akan diperlukan ketika Anda ingin membuat website yang memiliki proses kalkulasi kompleks, dan sebagainya.

  - Dari sisi **software**, web server merupakan **komputer yang menjalankan sebuah program agar dapat melayani (menerima atau mengirim) data melalui jenis protokol bernama HTTP**.
    - Ini merupakan protokol standar dalam melakukan transaksi data oleh browser.
    - Ada banyak program agar komputer kita dapat berkomunikasi dengan HTTP, yakni NGINX, Apache, ataupun membuatnya sendiri dengan menggunakan bahasa pemrograman server-side.

## DNS Server

- Setiap perangkat, baik komputer, smartphone, modem, maupun router yang terkoneksi internet akan memiliki IP Address.
- Contohnya, komputer yang menjadi server dari dicoding.com memiliki alamat IP sendiri.
- Jika menggunakan IP tersebut untuk mengakses halaman Dicoding, tentu kita akan sulit mengingat dan mungkin akan berubah dari waktu ke waktu.
- Mengingat beberapa alamat IP mungkin masih mampu dilakukan. Namun, bagaimana jika harus mengingat 10 alamat IP?
- Untuk mengatasinya, kita menggunakan **alamat yang mudah dibaca oleh manusia** dan disebut **domain name**.
- Sebenarnya, nama domain tidak akan menggantikan peran dari IP address.
- Komputer tetap menggunakan alamat IP untuk mengakses website.
- Namun, **bagaimana caranya nama domain dapat diterjemahkan menjadi alamat IP?** Berikut jawabannya.
  - Ketika user membuka website Dicoding menggunakan domain dicoding.com, browser akan menanyakan pada komputer, apakah ia mengenali dan dapat memberikan IP address-nya berdasarkan nama domain tersebut?
  - Dia akan memeriksa berdasarkan DNS cache yang ada.
  - Jika ada, browser akan diberikan alamat IP-nya dan menampilkan website yang diminta.
  - Jika komputer tidak mengenali nama domain tersebut, dia akan menanyakan pada DNS server yang secara singkat bertugas untuk memberi tahu alamat IP yang sesuai dari nama domain yang terdaftar padanya.
  - Jika sudah, browser akan diberikan alamat IP-nya dan meneruskan permintaan konten halaman web ke web server.
    <br>
    References :
    - What is a web server https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_web_server
    - How DNS Works https://howdns.works/
