## Array

- Array merupakan tipe data yang dapat mengelompokkan lebih dari satu nilai dan menempatkannya dalam satu variabel.
- Contoh :

  - `let myArray = ["Cokelat", 42.5, 22, true, "Programming"];`
    `console.log(myArray);`

    `/* output:`
    `[ 'Cokelat', 42.5, 22, true, 'Programming' ] */`

- Perbedaan array dengan object adalah data pada array disusun secara berurutan dan **diakses menggunakan index**.
- Untuk mengakses nilai di dalam array, kita gunakan **tanda kurung siku []**
- Di dalamnya berisi angka yang merupakan posisi nilai yang ingin diakses.
- Dalam sebuah array, **indeks dimulai dari 0**.
- Ketika kita mengakses data pada myArray yang berada pada indeks ke-1 artinya data tersebut merupakan data pada posisi ke-2. Jadi nilai yang akan ditampilkan pada konsol adalah 42.5.
- Jika kita **mengakses nilai array lebih dari index-nya**, maka hasilnya akan **undefined**.
- Index terakhir array selalu jumlah nilai array - 1.
- Untuk **menambahkan data ke akhir array**., kita bisa menggunakan metode **push()**.

  - `const myArray = ["Cokelat", 42.5, 22, true, "Programming"];`

    `myArray.push('JavaScript');`
    `console.log(myArray);`

    `/* output`
    `[ 'Cokelat', 42.5, 22, true, 'Programming', 'JavaScript' ] */`

- Sedangkan untuk **mengeluarkan data atau elemen terakhir dari array**, kita bisa gunakan metode **pop()**.

  - `const myArray = ["Cokelat", 42.5, 22, true, "Programming"];`

    `myArray.pop();`
    `console.log(myArray);`

    `/* output`
    `[ Cokelat, 42.5, 22, true ] */`

- Metode **shift()** digunakan untuk **mengeluarkan elemen pertama dari array**,
- Sementara **unshift()** digunakan untuk **menambahkan elemen di awal array**.

  - `const myArray = ["Cokelat", 42.5, 22, true, "Programming"];`

    `myArray.shift();`
    `myArray.unshift("Apple");`

    `console.log(myArray);`

    `/* output`
    `[ 'Apple', 42.5, 22, true, 'Programming' ] */`

- Sama seperti object, kita bisa menggunakan keyword **delete** untuk menghapus data dalam array

  - `const myArray = ["Cokelat", 42.5, 22, true, "Programming"];`
    `delete myArray[1];`
    `console.log(myArray);`

    `/* output`
    `[ 'Cokelat', <1 empty item>, 22, true, 'Programming' ] */`

- keyword delete hanya menghapus data pada index yang ditentukan lalu membiarkan posisi tersebut kosong.
- Untuk menghapus elemen, gunakan metode **splice()** seperti ini :

  - `const myArray = ["Cokelat", 42.5, 22, true, "Programming"];`

    `myArray.splice(2, 1);   // Menghapus dari index 2 sebanyak 1 elemen`
    `console.log(myArray);`

    `/* output`
    `[ 'Cokelat', 42.5, true, 'Programming' ] */`

- Selain untuk menghapus elemen pada array, **splice() juga dapat digunakan untuk menambahkan elemen pada array tersebut**.
- Caranya dengan memberikan argumen ke-3 (atau selanjutnya, bersifat variadic) sebagai nilai yang akan dimasukan pada index yang diberikan pada argumen pertama.

  - `const month = ['January', 'March', 'April', 'May'];`
    `console.log('before splice: ', month);`

    `month.splice(1, 1, 'February');`
    `console.log('after splice: ', month);`
