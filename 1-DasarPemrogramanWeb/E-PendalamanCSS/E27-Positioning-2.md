## Perbedaan Static Flow dan Non-Static

- CSS memiliki dua buah flow yang bisa digunakan untuk menampilkan elemen, yakni **static** dan **non-static**.
- Bayangkan kita memiliki **tiga buah elemen `<div>`** berukuran 200 piksel ✕ 200 piksel yang masing-masingnya memiliki warna **hijau**, **biru** dan **kuning**.
- Sebab kita tidak mengatur properti position dari ketiga elemen tersebut, tiap elemen akan ditampilkan dengan static flow.
- Ketika ingin mengubah letak kotak biru (kotak kedua) dengan menggunakan margin-top: 20px, tentu akan berpengaruh pada posisi elemen di bawahnya.
- Kotak yang berwarna oranye ikut bergeser ke bawah.
- Berbeda ketika kita menerapkan properti position yang dapat membuat elemen keluar dari static flow.
- Contohnya, kita menerapkan properti position dengan nilai relative
- Dalam tampilan browser mungkin tidak terdapat perbedaan apa pun setelah menerapkan nilai static pada atribut position.
- Namun, sebenarnya elemen yang menerapkannya akan **diangkat dari luar static flow**.
- Jadi, elemen tersebut dapat leluasa berpindah posisi tanpa memengaruhi elemen yang berada pada static flow.
- Untuk mengubah posisi elemen yang berada di **non-static** flow, kita dapat menggunakan properti **top**, **right**, **bottom**, ataupun **left**.
- Perlu diingat bahwa properti **top**, **left**, **right**, dan **bottom** hanya akan berpengaruh pada elemen yang menerapkan **non-static** flow, yaitu elemen yang menerapkan nilai **relative**, **absolute**, dan **fixed** pada properti **position**.
