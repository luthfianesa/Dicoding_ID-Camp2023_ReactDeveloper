## Specific Style Dengan Media Query

- Walaupun sudah menetapkan meta tag, viewport tampilan pada mobile device belum baik.
- CSS menyediakan sebuah fitur untuk menentukan styling hanya pada kondisi browser dan device tertentu sesuai dengan aturan yang kita tetapkan.
- Contohnya, kita memerintahkan ke CSS bahwa “tolong terapkan kode styling ini jika ukuran viewport lebih lebar dari 480 piksel”.
- Fitur tersebut dinamakan CSS **Media Query**.
- Berikut adalah aturan penulisan media query.
  ```
        @media media-type and (media-feature-rule) {
        /* CSS rules apa pun ada di sini */
        }
  ```
  - Pada aturan di atas, kita dapat jabarkan sebagai berikut.
    - **Media-type**:
    - Jenis media sebagai acuan bagi browser dalam menerapkan kode styling.
      - Tipe yang dapat diberikan adalah print, screen, atau semuanya.
    - **Media-feature-rule**:
      - Aturan atau kondisi yang harus terpenuhi agar kode styling dapat diterapkan.
      - Kondisi yang dimaksud seperti ukuran viewport, orientasi layar, dan jenis penggunaan perangkat tunjuk (touchsceen, keyboard navigation, atau mouse).
    - **Media-block**:
      - Sekumpulan CSS rule yang akan diterapkan jika kedua poin sebelumnya terpenuhi.`
  - Contoh :
    ```
      @media screen and (min-width: 400px) {
        h1 {
          color: red;
        }
      }
    ```
