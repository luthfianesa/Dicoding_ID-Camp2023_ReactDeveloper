## Alasan Flexbox Hadir

- Sebelum hadirnya flexbox, satu-satunya cara untuk membuat layout halaman web adalah **float** dan **positioning**.
- Namun, dalam beberapa kasus, penggunaan kedua properti CSS ini terbatas dan menyulitkan.
- Beberapa contoh kasus yang mungkin menyulitkan dan tidak fleksibel untuk dicapai dari penggunaan float dan positioning:
  - Membuat konten berada di tengah secara vertikal dalam parent element-nya.
    - Dari beberapa kasus, hal ini bisa dicapai menggunakan line-height.
    - Namun, ini hanya berguna jika konten berada dalam satu baris serta kita harus mengetahui secara eksplisit tinggi dari parent element.
  - Membuat semua child element memenuhi ruang dari parent element-nya secara dinamis dan merata.
    - Hal ini mungkin bisa tercapai menggunakan ukuran nilai persentase.
    - Namun, jika jumlah child element berjumlah ganjil, kita harus memikirkan nilai persentase yang tepat.
    - Bahkan, tetap akan meninggalkan celah ruang sedikit (tidak penuh).
  - Membentuk child element dalam layout multiple-column memiliki ukuran height yang sama, meskipun jumlah content di dalamnya tidak sama.
