## 19.1 Border

- Border merupakan sebuah garis yang mengelilingi area konten dan padding.
- Kita bisa mengatur tipe, ketebalan, serta warna garis yang ditampilkan sesuai dengan yang kita inginkan.
- Kita juga bisa mengatur dalam menampilkan sebagian atau keseluruhan garis pada elemen.

## 19.2 Border Width

- Properti border-width digunakan untuk mengatur ketebalan dari border
- Nilai dari properti ini dapat berupa piksel atau menggunakan predefined names value, seperti thin, medium, dan thick.
- Kita **tidak bisa menggunakan nilai persentase** (%) pada properti ini.
- Properti border-width dapat ditentukan dengan menggunakan satu, dua, tiga, atau empat nilai. Berikut penjelasannya :
  - Ketika **satu nilai** ditentukan, nilai berlaku untuk **empat sisi**.
  - Ketika **dua nilai** ditentukan, nilai pertama berlaku untuk **sisi atas dan bawah**, nilai kedua untuk sisi kiri dan kanan.
  - Ketika **tiga nilai** ditentukan, nilai pertama berlaku untuk **sisi atas**, nilai yang kedua untuk **sisi kiri** dan **kanan**, nilai ketiga untuk **sisi bawah**.
  - Ketika empat nilai ditentukan, nilai pertama berlaku untuk **sisi atas**, nilai yang kedua untuk **sisi kanan**, nilai yang ketiga untuk **sisi bawah**, dan nilai yang keempat untuk **sisi kiri**. Urutan tersebut berdasarkan arah jarum jam (**clockwise**).

## 19.3 Border Style

- Berikut adalah nilai-nilai yang dapat digunakan pada properti ini :

  - **solid**

    - Tipe garis padat (tidak terputus-putus).

  - **dotted**

    - Garis yang dibentuk dari serangkaian titik-titik
    - Jika ketebalan garis 2px, titik-titik akan berukuran 2px dan memiliki jarak 2px antar titiknya.

  - **dashed**

    - Garis yang dibentuk dari serangkaian garis pendek.

  - **double**

    - Garis yang dibentuk dari dua buah garis padat.

  - **groove**

    - Tipe garis yang berbentuk seperti frame.

  - **hidden**
    - Digunakan untuk menyembunyikan garis pada elemen.

## 19.4 Border Color

- Properti terakhir adalah border-color.
- Properti ini digunakan untuk menentukan warna pada garis dengan menggunakan nilai RGB, Hex, atau nama warna pada CSS.

## 19.5 Shorthand

- CSS menyediakan jalan pintas (shorthand) untuk membuat border dengan satu properti saja.
- Properti border memiliki tiga buah nilai yang digunakan untuk menentukan ketebalan, tipe, dan warna pada border.
- Perlu kita perhatikan bahwa penulisan urutan harus benar
- border: **type**,**width**,**color**;
- border: 4px dashed #00a2c6;
