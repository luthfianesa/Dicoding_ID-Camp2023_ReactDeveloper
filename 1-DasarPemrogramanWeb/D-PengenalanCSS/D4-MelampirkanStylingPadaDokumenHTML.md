## Melampirkan Styling Pada Dokumen HTML

- Setelah kita menuliskan rules, maka tahapan selanjutnya adalah melampirkan atau menerapkan aturan tersebut pada berkas HTML.
- Terdapat **tiga cara** untuk menerapkan styling pada elemen HTML.

  - **External Style Sheet**
    - External Style Sheet merupakan **berkas terpisah** yang di dalamnya hanya terdapat sebuah rules.
    - Berkas ini harus berekstensi .css, dan berkas ini nantinya dihubungkan pada dokumen HTML.
    - Cara ini merupakan yang paling powerful dalam menerapkan styling.
    - Karena dengan cara ini, satu berkas styling (.css) dapat digunakan oleh banyak berkas HTML.
    - Untuk menyambungkan berkas .css dengan dokumen HTML, kita dapat menggunakan elemen `<link>` pada `<head>` berkas HTML.
  - **Internal Style Sheet**
    - Merupakan kumpulan rules yang dituliskan dalam berkas HTML dengan **menggunakan elemen `<style>`**.
    - Dengan begitu rules yang dituliskan hanya dapat dicakup oleh satu berkas HTML.
    - Penulisan rules harus dituliskan dalam elemen `<style>` dan ditempatkan di dalam `<head>` dari berkas HTML.
  - **Inline Style**

    - Inline Style merupakan styling yang diterapkan pada elemen HTML dengan **menggunakan atribut style**.
    - Untuk menambahkan styling properties lainnya (multiple properties), kita tuliskan dengan menggunakan semicolon (;) sebagai pemisah antar styling properties-nya.
    - Inline styles hanya diterapkan pada elemen di mana atribut style diterapkan.
    - Teknik ini seharusnya dihindari
