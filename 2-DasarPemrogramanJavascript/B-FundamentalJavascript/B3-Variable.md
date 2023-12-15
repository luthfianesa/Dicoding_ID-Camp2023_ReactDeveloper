## Variable

- Ketika menulis sebuah program, kita memberi tahu komputer cara memproses informasi seperti mencetak teks ke layar atau melakukan operasi perhitungan.
- Untuk lebih mudah dalam penggunaan dan pemanggilan data, kita bisa memanfaatkan variabel.
- Variabel umumnya digunakan untuk **menyimpan informasi atau nilai** yang akan dikelola dalam sebuah program.
- Pada JavaScript setidaknya ada tiga cara untuk mendeklarasikan sebuah variabel, yaitu menggunakan keyword **var**, **let**, dan **const**.
- Pada versi ECMAScript 2015 (ES6) dikenalkan deklarasi variabel dengan let dan const untuk menggantikan **var yang dinilai kontroversial dan rawan menimbulkan bug**.

- contoh `let lasName;`
- Kode untuk **mendeklarasikan variabel** seperti di atas juga dikenal dengan **declaration statement**.
- Selanjutnya, kita bisa mengisi nilai variabel di atas menggunakan tanda sama dengan (=).
- Anda juga bisa langsung menginisialisasi nilai variabel setelah mendeklarasikannya seperti berikut :
  - `let lastName = "Sani"`
- Kode untuk **menginisialisasikan nilai** ke dalam sebuah variabel dengan tanda sama dengan (=) ini disebut dengan **assignment expression**.
- Karena **expression pasti menghasilkan nilai**, sehingga mereka bisa muncul di mana pun dalam program JavaScript.
- Sementara itu, **statement merujuk pada aksi**. Sehingga, pada bagian kode tertentu yang membutuhkan nilai tidak bisa kita isi dengan sebuah statement. Contohnya seperti kode berikut:
  - `let fullName = let lastName;` // Error karena let lastName adalah sebuah statement untuk deklarasi variabel.
  - Statement tidak bisa berada di posisi expression.
  - `let fullName = (lastName = "Skywalker");` // (lastName = "Skywalker") merupakan expression, sehingga kode ini tidak error.
  - `let fullName = "Luke" + "Skywalker";` // "Luke" + "Skywalker" juga merupakan expression, sehingga kode ini tidak error.
- Melalui contoh kode di atas, kita bisa bayangkan **variabel** sebagai sebuah **kotak atau wadah yang menyimpan nilai**.
- Proses **inisialisasi atau assignment berarti kita memasukkan nilai ke dalam kotak** tersebut.
