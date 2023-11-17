## Properti - Properti Pada Flex Items

- Berikut adalah properti - properti pada flex items :

  - **1. Order**
    - Secara default, flex items akan diletakkan sesuai dengan urutan penulisan kode.
    - Namun, dengan properti order, kita bisa mengatur urutan susunan flex items.
  - **2. Flex Grow**

    - Ketika kita membuat layout dengan flexbox, flex item akan dijejerkan serta memiliki lebar sesuai dengan ukuran kontennya.
    - Bisa saja flex container akan meninggalkan sisa ruang meski ukuran konten dari flex items tidak memenuhi flex container.
    - Kita dapat mengatur flex items agar selalu memenuhi flex container.
    - Properti ini akan melakukan grow pada main axis sehingga tidak akan menyisakan ruang kosong pada flex container.
    - Flex grow akan melakukan pendistribusian sisa ruang dalam container kepada seluruh child element dengan porsi yang sama (adil).
    - Jika salah satu child elemen memiliki flex grow dengan nilai dua, child element tersebut akan mendapatkan pembagian porsi dua kali lebih besar dibanding child element yang hanya memiliki satu porsi.
    - Nilai yang diberikan pada properti ini adalah angka tanpa satuan (unitless).

  - **3. Flex Shrink**
    - Properti ini memiliki kemampuan untuk menyusutkan atau menciutkan ukuran child element jika ukurannya tidak mencukupi ruang container.
    - Nilai yang diberikan pada properti ini adalah angka tanpa satuan (unitless).
    - Secara default, nilai dari properti ini adalah 1.
    - Jika kita memberikan nilai 0, ukuran child element tidak akan menciut.
  - **4. Flex Basis**

    - Properti ini akan memberikan ukuran default sebelum sisa ruang container didistribusikan kepada flex items.
    - Nilai yang didukung untuk properti ini terkait ukuran dimensi (width dan height), yaitu 2rem, 20%, dan lainnya.

  - **5. Align Self**
    - Properti ini memiliki tingkah laku yang sama dengan properti align items.
    - Properti ini dapat mengatur posisi child element secara cross-axis.
    - Namun, properti ini hanya berlaku untuk child element.
    - Jika kita ingin mengecualikan child element di antara child element lainnya, gunakanlah properti ini.
