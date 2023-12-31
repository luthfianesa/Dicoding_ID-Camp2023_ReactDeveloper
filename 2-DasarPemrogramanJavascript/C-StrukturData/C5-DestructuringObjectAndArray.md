## Destructuring Object & Array

- **Iterasi object dan array** adalah dua hal yang **paling banyak digunakan dalam mengelola data di JavaScript**.
- JSON (**JavaScript Object Notation**) merupakan **format data paling populer** yang digunakan **dalam transaksi data** saat ini.
  ```
  [
    {
      "id": 14,
      "title": "Belajar Fundamental Aplikasi Android",
      "author": "Google ATP"
    },
    {
      "id": 51,
      "title": "Belajar Membuat Aplikasi Android untuk Pemula",
      "author": "Google ATP"
    },
    {
      "id": 123,
      "title": "Belajar Dasar Pemrograman Web",
      "author": "Dicoding Indonesia"
    },
    {
      "id": 163,
      "title": "Belajar Fundamental Front-End Web Development",
      "author": "Dicoding Indonesia"
    }
  ]
  ```
- Jika kita lihat pada struktur JSON di atas, kita dapat menyimpulkan struktur tersebut dibangun dari array dan object.
- Karena kedua hal ini banyak digunakan untuk mengelola data pada JavaScript untuk memudahkan developer.
- ES6 menambahkan fitur untuk destructuring object dan array.
- **Destructuring dalam JavaScript** merupakan sintaksis yang dapat **mengeluarkan nilai dari array atau properties dari sebuah object** ke dalam satuan yang lebih kecil.
- Secara tidak sadar mungkin kita pernah melakukan destructuring.
- Namun, sebelum ES6 hal tersebut dilakukan dengan cara seperti ini :

  ```
  const profile = {
  firstName: "John",
  lastName: "Doe",
  age: 18
  }

  const firstName = profile.firstName
  const lastName = profile.lastName
  const age = profile.age

  console.log(firstName, lastName, age)

  /* output:
  John Doe 18
  */
  ```

- Perhatikan kode di atas,

  - Kode tersebut mengekstraksi nilai yang berada di dalam objek
  - Kemudian menyimpannya pada variabel lokal dengan nama yang sama seperti properti di dalam object profile.
  - Mungkin mengekstraksi nilai dari object dengan langkah ini terlihat mudah
  - Tetapi bayangkan jika object memiliki banyak properti dan harus melakukan hal tersebut secara manual satu persatu.
  - Terlalu banyak kode yang dituliskan berulang, bukan?

- Itulah alasan ES6 menambahkan fitur yang **memudahkan kita untuk destructuring object maupun array**.
- Ketika kita ingin memecah struktur data menjadi bagian-bagian yang lebih kecil, kita akan dipermudah untuk mendapatkan data yang diinginkan.
