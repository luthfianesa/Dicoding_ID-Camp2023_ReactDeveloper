## C7.1 Destructuring Array

- Destructuring array serupa dengan destructuring object.
- Object menggunakan tanda kurung kurawal { } sedangkan array menggunakan **tanda kurung siku [ ]**.
- Perbedaan lainnya adalah destructuring array bekerja **berdasarkan posisi** daripada penamaan propertinya.
- Berikut contoh dari destructuring array pada ES6 :

  ```
  const favorites = ["Seafood", "Salad", "Nugget", "Soup"];

  const [firstFood, secondFood, thirdFood, fourthFood] = favorites;

  console.log(firstFood);
  console.log(secondFood);
  console.log(thirdFood);
  console.log(fourthFood);

  /* output:
  Seafood
  Salad
  Nugget
  Soup
  */
  ```

- Kode di atas merupakan contoh proses destructuring array.
- Di dalam array favorites terdapat 4 (empat) nilai string yang masing-masing nilainya dimasukkan ke variabel lokal firstFood, secondFood, thirdFood, dan fourthFood.
- Nilai dari array yang dimasukkan ke variabel lokal dipilih berdasarkan posisi di mana ia dideklarasikan pada array.
- Sebenarnya kita **bebas untuk menentukan nama dari variabel** lokal.
- **Yang terpenting adalah urutan ketika deklarasi variabelnya** saja.
- Kita juga bisa memilih nilai pada index tertentu untuk destrukturisasi pada array.
- Contohnya, jika ingin mengambil nilai ketiga dari array, kita tidak perlu menyiapkan variabel lokal untuk menampung nilai array pertama, kedua, atau pun keempat.
- Kita bisa melakukannya dengan membiarkan index array yang tidak kita inginkan tetap kosong (tanpa menulis variabel lokal).
- Lebih lanjut, tanda koma (,) tetap diperlukan untuk menunjukkan posisi index-nya seperti ini:

  ```
  const favorites = ["Seafood", "Salad", "Nugget", "Soup"];

  const [ , , thirdFood ] = favorites;

  console.log(thirdFood);

  /* output:
  Nugget
  */
  ```

## C7.2 Destructuring Assignment

- Kita juga bisa melakukan destructuring assignment pada array.
- Namun, tidak seperti object, kita tidak perlu membungkusnya dengan tanda kurung.
- Contohnya seperti berikut :

  ```
  const favorites = ["Seafood", "Salad", "Nugget", "Soup"];

  let myFood = "Ice Cream";
  let herFood = "Noodles";

  [myFood, herFood] = favorites;

  console.log(myFood);
  console.log(herFood);
  ```

- Array destructuring assignment sangat berguna ketika kita hendak menukar nilai antara dua variabel.
- Sebelum ES6, untuk melakukan hal ini kita menggunakan cara manual menggunakan algoritma seperti ini :

  ```
  var a = 1;
  var b = 2;
  var temp;

  console.log("Sebelum swap");
  console.log("Nilai a: " + a);
  console.log("Nilai b: " + b);

  temp = a;
  a = b;
  b = temp;

  console.log("Setelah swap");
  console.log("Nilai a: " + a);
  console.log("Nilai b: " + b);

  /* output
  Sebelum swap
  Nilai a: 1
  Nilai b: 2
  Setelah swap
  Nilai a: 2
  Nilai b: 1
  */
  ```

- Untuk melakukan pertukaran nilai, kita membutuhkan variabel penengah.
- Pada contoh kode di atas menggunakan variabel temp.
- Variabel penengah dibutuhkan untuk menyimpan data sementara pada variabel yang akan ditukar.
- Hal ini menjadi kurang efektif karena kita harus membuat variabel baru yang sebenarnya hanya bersifat sementara.
- Dengan array destructuring assignment, kita bisa menukar nilai variabel dengan mudah tanpa membuat variabel tambahan.

  ```
  let a = 1;
  let b = 2;

  console.log("Sebelum swap");
  console.log("Nilai a: " + a);
  console.log("Nilai b: " + b);

  [a, b] = [b, a] // menetapkan nilai a dengan nilai b dan nilai b dengan nilai a.

  console.log("Setelah swap");
  console.log("Nilai a: " + a);
  console.log("Nilai b: " + b);

  /* output
  Sebelum swap
  Nilai a: 1
  Nilai b: 2
  Setelah swap
  Nilai a: 2
  Nilai b: 1
  */
  ```

## C7.3 Default Values

- Ketika melakukan destructuring array, tetapi terdapat variabel yang posisinya tidak dapat terjangkau oleh array.
- Maka variabel tersebut akan bernilai undefined. Contohnya :

  ```
  const favorites = ["Seafood"];
  const [myFood, herFood] = favorites

  console.log(myFood);
  console.log(herFood);

  /* output:
  Seafood
  undefined
  */
  ```

- Sama seperti object, pada destructuring array kita juga dapat memberikan nilai default
- Pada variabel yang tidak dapat terjangkau oleh array, sehingga nilai pada variabel tidak akan menjadi undefined.

  ```
  const favorites = ["Seafood"];

  const [myFood, herFood = "Salad"] = favorites

  console.log(myFood);
  console.log(herFood);

  /* output:
  Seafood
  Salad
  ```
