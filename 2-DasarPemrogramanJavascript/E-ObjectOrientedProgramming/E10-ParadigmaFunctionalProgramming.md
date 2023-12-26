## Paradigma Functional Programming

- Paradigma Functional Programming adalah paradigma pemrograman di mana **proses komputasi didasarkan pada fungsi matematika murni**.
- Functional Programming (selanjutnya akan kita singkat menjadi FP) ditulis dengan **gaya deklaratif**.
- Berfokus pada **“what to solve”** dibanding **“how to solve”** yang dianut oleh gaya imperatif.
- Sebagai gambaran buat Anda yang belum tahu apa itu **deklaratif** dan **imperatif** lebih jauh, silakan simak contoh kode berikut.

  ```
  const names = ['Harry', 'Ron', 'Jeff', 'Thomas'];

  const newNamesWithExcMark = [];

  for(let i = 0; i < names.length; i++) {
    newNamesWithExcMark.push(`${names[i]}!`);
  }

  console.log(newNamesWithExcMark);

  /* output:
    [ 'Harry!', 'Ron!', 'Jeff!', 'Thomas!' ]
  */
  ```

- Contoh kode di atas merupakan salah satu gaya penulisan kode imperatif.
- Di mana proses pengisian nilai array baru (newNames) berdasarkan array lama (names) dilakukan secara manual.
- Inilah maksud dari “how to solve”,
  - Di mana kita perlu memikirkan bagaimana cara melakukan perulangannya (for);
  - Kapan perulangannya harus berhenti (i < names.length);
  - Bagaimana cara memasukkan nilai baru ke dalam array (newNamesWithExcMark.push).
- Lantas bagaimana dengan gaya deklaratif? Mari kita lihat kode dengan fungsi yang sama namun dengan gaya deklaratif.

  ```
  const names = ['Harry', 'Ron', 'Jeff', 'Thomas'];

  const newNamesWithExcMark = names.map((name) => `${name}!`);

  console.log(newNamesWithExcMark);

  /* output:
  * [ 'Harry!', 'Ron!', 'Jeff!', 'Thomas!' ]
  */
  ```

- Coba bandingkan dengan kode sebelumnya, tentu ini jauh lebih mudah dibaca dan ringkas.
- Yap! Inilah yang disebut dengan gaya deklaratif.
- Kita tidak perlu pusing untuk memikirkan cara manual untuk mencapai sebuah tujuan.
- Tidak ada proses looping manual; Tidak perlu tahu kapan harus berhenti dari looping; Kita cukup fokus pada “what to solve” alias apa yang ingin kita selesaikan atau capai.
- JavaScript sendiri merupakan bahasa pemrograman yang mendukung paradigma FP.
- Banyak **Higher-Order Function** (kita akan bahas detail tentang ini nanti) yang bisa kita manfaatkan sebagai utilitas, salah satunya fungsi **array map()** di atas.
- Namun FP bukan hanya sekedar menggunakan High-Order Function bawaan saja.
- Untuk memahami paradigma FP secara mendalam, kita perlu tahu dulu konsep-konsep apa saja yang ada di dalamnya.
