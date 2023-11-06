## C16.1 Mengirim Data Formulir

- Formulir telah dibuat, user dapat mengisinya dengan benar, dan aplikasi pun mendapatkan data-data input yang dibutuhkan untuk dimanfaatkan.
- Biasanya, data-data tersebut akan dikirimkan ke server untuk diolah lebih lanjut.
- Pembahasan tentang pengiriman data ini memiliki hubungan dengan web server.
- Ketika client membutuhkan resources guna menampilkan halaman web ke pengguna, ia akan mengirimkan request ke server tentang kebutuhan yang dimaksud.
- HTML, CSS, JavaScript, serta aset-aset lainnya merupakan resources yang akan dikirimkan dan di-render oleh browser sehingga tampillah halaman web yang utuh.
- Berbicara mengenai mengirim data dari formulir ke server, kita membutuhkan satu elemen esensial dalam membangun formulir. - Ada satu elemen yang berfungsi sebagai wrapper (pembungkus) dari keseluruhan kolom input atau formulir, yaitu `<form>`.

## C16.2 Atribut Name di Elemen Input

- Dalam mengirimkan data ke server, kita wajib menerapkan atribut name pada seluruh kolom input dalam formulir.
- Contohnya, kita ingin membuat formulir untuk melakukan pemesanan kamar hotel.
- Kita harus memberi atribut name pada seluruh elemen input.
- Mengapa hal ini diperlukan? Seharusnya, setiap data dikirimkan dalam bentuk pasangan key dan value.
- Key merupakan identitas atau nama dari data yang dikirimkan, sedangkan value adalah data yang diisi oleh user.
- Hal ini akan memberikan kemampuan pada server untuk mengambil data berdasarkan key-nya.

## C16.3 Cara Membawa Data Formulir

- Elemen form memiliki atribut-atribut khusus yang menentukan konfigurasi request untuk dikirimkan ketika user menekan tombol submit.
- Ada **dua atribut**: action dan method.
  - **Atribut Action**
    - Atribut **action** akan **menentukan alamat tujuan dari pengiriman data**.
    - Kita bisa memberikannya URL yang mengarah pada suatu server atau kadang disebut sebagai **API**.
      Server yang dimaksud dapat server yang berada pada domain yang sama atau berbeda.
    - Dalam hal ini, kita bisa **memberikan URL yang relatif atau absolut**.
    - Bagaimana jika kita tidak menyertakan atau menentukan atribut ini pada elemen form?
    - Jika sampai demikian, data-data formulir akan dikirimkan ke alamat yang saat ini sedang diakses.
  - **Atribut Method**
    - Atribut ini akan **menentukan cara data dikirimkan ke server**.
    - Tidak hanya alamat yang kita butuhkan, ada beberapa cara atau proses dalam mengirimkan data ke server.
    - Semua ini dilakukan dengan menentukan metode pengiriman.
    - Ada dua buah metode yang bisa digunakan untuk mengirimkan data pada formulir HTML, yaitu **GET** dan **POST**.
      - **Metode GET**
        - Biasanya, metode ini digunakan untuk **mendapatkan data dari server**.
        - Data tersebut akan **diterima oleh browser melalui body response** (HTTP response).
        - Tidak hanya itu, HTTP request juga memiliki body request untuk mengirimkan data dari browser ke server.
          Namun, body request dengan metode GET akan kosong.
        - Hal ini karena setiap data yang dikirimkan akan diletakkan dalam URL parameters.
      - **Metode POST**
        - Ini merupakan metode untuk **mengirimkan data dari browser ke server**.
        - Umumnya, metode ini meminta server menanggapi terhadap data yang telah dikirimkan oleh browser dan **mengharapkan pengembalian dari hasil tanggapan tersebut** (response).
