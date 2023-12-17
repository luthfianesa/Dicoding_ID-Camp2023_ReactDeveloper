## Operator

- Operator dalam bahasa pemrograman sendiri adalah simbol yang memberi tahu interpreter untuk melakukan operasi seperti matematika, relasional, atau logika untuk memberikan hasil tertentu.

- Terdapat 3 Operator :
  - A. **Assignment Operator**
  - B. **Comparison Operator**
  - C. **Logical Operator**
    <br>
- **A. Assignment Operator**

  - Operator ini digunakan untuk **memberikan nilai pada variabel**.
  - Pada dasarnya operator ini adalah tanda sama dengan (=), di mana tanda ini digunakan untuk menginisialisasi nilai pada variabel.
  - Ada beberapa assignment **operator tambahan** lain dalam menginisialisasikan nilai pada variabel.
  - Kita bisa menyebutnya sebagai **shortcut** dalam menentukan nilai. Contohnya:

    - `let x = 10;`
      `let y = 5`
      `x += y;`

      `console.log(x);`

      `/* output`
      `15 */`

  - Pada contoh kode di atas, terdapat expression x += y;
  - Artinya, Assignment operator tersebut digunakan sebagai shortcut dari x = x + y.
  - Cara ini juga dapat digunakan pada operator aritmatika lain seperti, perkalian, pengurangan, pembagian, dan lainnya.

- **B. Comparison Operator**
- Terdapat serangkaian karakter khusus yang disebut dengan operator pembanding/komparasi yang dapat **mengevaluasi dan membandingkan dua nilai**.
- Berikut daftar operator dan fungsinya:
  - `==` -> Membandingkan kedua nilai apakah sama (tidak identik)
  - `===` -> Membandingkan kedua nilai apakah sama (identik)
  - `!=`-> Membandingkan kedua nilai apakah tidak sama (tidak identik).
  - `!==` -> Membandingkan kedua nilai apakah tidak identik.
  - `>` -> Membandingkan dua nilai apakah nilai pertama lebih dari nilai kedua.
  - `>=` -> Membandingkan dua nilai apakah nilai pertama lebih atau sama dengan nilai kedua.
  - `<` -> Membandingkan dua nilai apakah nilai pertama kurang dari nilai kedua.
  - `<=` -> Membandingkan dua nilai apakah nilai pertama kurang atau sama dengan nilai kedua.
- Ketika kita melakukan perbandingan antara dua nilai, JavaScript akan mengevaluasi kedua nilai tersebut.
- Dan mengembalikan boolean dengan nilai hasil perbandingan tersebut, baik false atau true.
- Dalam operator komparasi di JavaScript, hal yang menjadi sedikit “tricky” adalah membedakan antara “sama” (==) dan “identik” (===).
- Jika kita ingin membandingkan hanya dari **kesamaan nilainya** kita bisa gunakan **==** tapi jika kita ingin membandingkan dengan memperhatikan **tipe datanya** kita gunakan **===**.
- Contohnya seperti berikut:

  - `const aString = '10';`
    `const aNumber = 10;`

    `console.log(aString == aNumber) // true, karena nilainya sama-sama 10`
    `console.log(aString === aNumber) // false, karena walaupun nilainya sama, tetapi tipe datanya berbeda`

    `/* output`
    `true`
    `false */`

- **C. Logical Operator**
- Dengan logical operator, kita dapat menggunakan kombinasi dari dua nilai boolean atau bahkan lebih dalam menetapkan logika.
- Pada JavaScript terdapat **tiga buah karakter khusus** yang berfungsi sebagai logical operator.
- Berikut macam-macam logical operator dan fungsinya:

  - `&&` -> Operator dan (**and**). Logika akan menghasilkan nilai true apabila semua kondisi terpenuhi (bernilai true).
  - `!!`-> Operator atau (**or**). Logika akan menghasilkan nilai true apabila ada salah satu kondisi terpenuhi (bernilai true).
  - `!` -> Operator tidak (**not**). Digunakan untuk membalikkan suatu kondisi.
  - Contoh :

    - `let a = 10;`
    - `let b = 12;`

      `/* AND operator */`
      `console.log(a < 15 && b > 10); // (true && true) -> true`
      `console.log(a > 15 && b > 10); // (false && true) -> false`

      `/* OR operator */`
      `console.log(a < 15 || b > 10); // (true || true) -> true`
      `console.log(a > 15 || b > 10); // (false || true) -> true`

      `/_ NOT operator _/`
      `console.log(!(a < 15)); // !(true) -> false`
      `console.log(!(a < 15 && b > 10)); // !(true && true) -> !(true) -> false`

      `/_ output`
      `true`
      `false`
      `true`
      `true`
      `false`
      `false _/`
