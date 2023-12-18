## B6.1 If Else Statemnt

- Ketika mengembangkan sebuah program, kita akan bertemu dengan alur bercabang tergantung pada kondisi yang terjadi.
- Untuk mengakomodasi dan mengecek sebuah kondisi dalam JavaScript, kita menggunakan kata kunci if.
- Statement if akan menguji suatu kondisi, jika kondisi bernilai true, maka blok kode di dalamnya akan dijalankan.
- Sebaliknya, jika bernilai false, maka proses yang ditentukan akan dilewatkan.
- Pada contoh kode berikut kita akan melakukan pengecekan kondisi menggunakan operator perbandingan.

  - `let x = 50;`

  - `if(x > 70) {`
    `console.log(x);`
    `} else {`
    `console.log("Nilai kurang dari 70");`
    `}`

    `/* output`
    `Nilai kurang dari 70 */`

- Kita juga bisa mengecek beberapa kondisi sekaligus dengan menggabungkan else dan if.
- Contohnya adalah seperti program berikut:

  - `let language = "French";`
    `let greeting = "Selamat Pagi"`

    `if(language === "English") {`
    `greeting = "Good Morning!";`
    `} else if(language === "French") {`
    `greeting = "Bonjour!"`
    `} else if(language === "Japanese") {`
    `greeting = "Ohayou Gozaimasu!"`
    `}`

    `console.log(greeting);`

    `/* output`
    `Bonjour! */`

- JavaScript juga mendukung ternary operator atau conditional expressions.
- Dengan ini, kita bisa menuliskan if-else statement hanya dalam satu baris.

  - `// condition ? true expression : false expression`

    `const isMember = false;`
    `const discount = isMember ? 0.1 : 0;`
    `console.log('Anda mendapatkan diskon sebesar ${discount * 100}%')`

    `/* output `
    `Anda mendapatkan diskon sebesar 0% */`

- Ternary operator membutuhkan tiga operand.
- Sebelum tanda tanya (?) berisi kondisi yang ingin kita evaluasi.
- Kemudian diikuti dengan expression apabila nilai kondisinya benar sebelum tanda titik dua.
- Terakhir adalah expression yang dieksekusi ketika kondisinya salah.
- Karena merupakan conditional expression, maka operand kedua dan ketiga harus mengembalikan nilai.

## B6.2 Truthy and Falsy

- Di dalam if statement kita perlu memasukkan expression yang akan dievaluasi.
- Umumnya, expression tersebut mengembalikan nilai boolean untuk menentukan kondisi true atau false.
- Lalu bagaimana jika kita menuliskan expression yang tidak mengembalikan nilai boolean? Jawabannya bisa.
- **Setiap nilai pada JavaScript pada dasarnya juga mewarisi sifat boolean**.
- Nilai ini dikenal dengan truthy atau falsy.
- Nilai truthy berarti nilai yang ketika dievaluasi akan menghasilkan nilai true, begitu pula falsy bernilai false.
- Tipe data atau nilai yang dianggap falsy, antara lain:
  - A. **Number 0**
  - B. **BigInt 0n**
  - C. **String kosong seperti “” atau ‘’**
  - D. **null**
  - E. **undefined**
  - F. **NaN, atau Not a Number**
    **Selain contoh di atas maka nilainya adalah truthy** dan ketika dievaluasi ke dalam if statement akan bernilai true.
- Berikut ini contohnya dalam kode:

  - `let name = "";`

  - `if (name) {`
    `console.log("Halo, " , name);`
    `} else {`
    `console.log("Nama masih kosong");`
    `}`

    `/* output:`
    `Nama masih kosong */`
