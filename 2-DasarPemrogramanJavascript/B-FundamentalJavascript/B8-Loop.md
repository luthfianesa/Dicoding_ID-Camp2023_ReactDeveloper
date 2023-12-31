## B8.1 For Loop

- Dari beberapa cara melakukan proses loop pada JavaScript, “for” merupakan salah satu cara yang banyak digunakan.
- Struktur dasar dari for tampak seperti berikut :
  - `for(inisialisasi variabel; test kondisi; perubahan nilai variabel) {`
    `// do something`
    `}`
- Terdapat tiga bagian utama dalam sintaks for di atas:
  - **Pertama**, variabel i sebagai index iterasi.
    - Pada variabel ini kita menginisialisasi nilai awal dari perulangan.
  - **Kedua**, operasi perbandingan.
    - Pada bagian ini, JavaScript akan melakukan pengecekan kondisi apakah perulangan masih perlu dilakukan.
    - Jika bernilai true, maka kode di dalam blok for akan dijalankan.
  - **Ketiga**, increment/decrement.
    - Di sini kita melakukan penambahan atau pengurangan variabel iterasi.
    - Jadi, pada contoh di atas variabel i akan ditambah dengan 1 di setiap akhir perulangan.
    - Perubahan nilai ini penting karena jika kita mengubah nilainya, proses perulangan dapat terus berjalan selama kondisinya terpenuhi.
- JIka diartikan, maka kode di atas bisa dimaknai dengan “Jika i kurang dari 5, maka tampilkan nilai i.”

## B8.2 For of Loop

- For of mulai hadir pada ECMAScript 2015 (ES6).
- Cara ini jauh lebih sederhana dan modern dibanding for loop biasa.
- Sintaks dasar dari for of loop adalah seperti ini:
  - `for(arrayItem of myArray) {`
    `// do something`
    `}`
- for of tidak membutuhkan banyak statement untuk melakukan looping pada array.
- Kita bisa menganggap array sebagai kumpulan nilai yang disimpan dalam satu variabel.
- Dengan for..of nilai tiap array akan diinisialisasi pada variabel baru yang kita tentukan pada tiap proses looping-nya.
- Jumlah proses looping-nya pun akan menyesuaikan dengan ukuran dari array.
- Sederhananya seperti kita melakukan perintah “Hei JavaScript! Lakukan perulangan pada myArray, akses tiap nilainya, dan simpan pada variabel arrayItem”.
- Pada proses looping kita gunakan variabel arrayItem untuk mengakses tiap nilai dari item myArray.

  - `let myArray = ["Luke", "Han", "Chewbacca", "Leia"];`

    `for(const arrayItem of myArray) {`
    `console.log(arrayItem)`
    `}`

    `/* output`
    `Luke`
    `Han`
    `Chewbacca`
    `Leia */`

## B8.3 While and Do-While

- Metode lain untuk melakukan looping adalah dengan statement while.
- Sama seperti for, instruksi while mengevaluasi ekspresi boolean dan menjalankan kode di dalam blok while ketika bernilai true.
- Untuk menampilkan angka 1 sampai 100 dengan while kita bisa menulis kode seperti berikut:

  - `let i = 1;`

    `while (i <= 100) {`
    `console.log(i);`
    `i++;`
    `}`

- Bisa dilihat pada kode di atas bahwa looping dengan while tidak memiliki ketergantungan dengan variabel iterasi seperti pada for loop.
- Karena itu, meskipun while dapat melakukan perulangan yang sama dengan for.
- while lebih cocok digunakan pada kasus di mana kita tidak tahu pasti berapa banyak perulangan yang diperlukan.
- Bentuk lain dari while adalah perulangan do-while.

  - `let i = 1;`

    `do {`
    `console.log(i);`
    `i++;`
    `} while (i <= 100);`

- Kondisi pada while akan dievaluasi sebelum blok kode di dalamnya dijalankan.
- Sedangkan do-while akan mengevaluasi boolean expression setelah blok kodenya berjalan.
- Ini artinya kode di dalam do-while akan dijalankan setidaknya satu kali.

## B8.4 Infinite Loop

- Ketika menerapkan perulangan pada program, ada satu kondisi yang perlu kita hindari yaitu infinite loop.
- Infinite loop atau endless loop adalah kondisi di mana program kita stucked di dalam perulangan.
- Ia akan berjalan terus hingga menyebabkan crash pada aplikasi dan komputer kecuali ada intervensi secara eksternal, seperti mematikan aplikasi.
- Kode berikut ini adalah contoh di mana kondisi infinite loop dapat terjadi :

  - `let i = 1;`

    `while (i <= 5) {`
    `console.log(i);`
    `}`

- Karena variabel i selalu bernilai 1. Alhasil, kondisi i <= 5 akan selalu bernilai true.
- Mmengakibatkan aplikasi akan terus mencetak 1 ke konsol sehingga mengalami crash.
