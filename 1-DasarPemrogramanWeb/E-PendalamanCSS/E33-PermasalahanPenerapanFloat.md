## Permasalahan Penerapan Float

- Properti float terlihat sangat mudah untuk digunakan, baik dalam text wrapping maupun dalam penyusunan layout.
- Namun, masalah yang akan ditimbulkan adalah jika sebuah elemen induk yang hanya memiliki satu elemen dengan menerapkan properti float akan memiliki nilai tinggi 0px.
- Elemen yang menerapkan float “tidak dianggap ada” oleh induk elemen yang menaunginya karena dengan menggunakannya **float elemen akan dikeluarkan dari normal flow**.
- Ada dua cara untuk menangani hal tersebut, menggunakan properti **clear** dan menetapkan nilai **overflow: auto** pada container.
