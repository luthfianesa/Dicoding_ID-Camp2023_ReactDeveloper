## Konfigurasi Meta Tag Viewport untuk Responsibilitas Layout

- Pada browser, ada fitur inspeksi elemen.
- Fitur ini sangat banyak dan bermanfaat bagi developer web dalam membantu mengembangkan website.
- Hal yang pasti, pada inspector tersebut, ada fitur yang dapat mensimulasikan halaman website dalam tampilan yang lebih kecil, seperti perangkat mobile atau tablet.
- Untuk membuka fitur inspector, kita dapat gunakan keyboard shortcut, seperti “CTRL + SHIFT + I” atau klik kanan dan pilih “Inspect”/”Inspect Page”.
- Viewport merupakan **area yang dapat dilihat oleh pengguna kita pada halaman website**.
- Ukuran **viewport bervariasi berdasarkan device-nya**.
- Ukuran viewport pada sebuah peranti mobile lebih kecil dibandingkan dengan layar komputer desktop.
- Sebelum adanya tablet ataupun handphone, halaman website didesain hanya untuk ukuran layar komputer desktop. Dengan demikian, banyak sekali website yang menerapkan tampilan dan ukuran yang statis.
- Jadi, ketika halaman tersebut diakses melalui handphone atau tablet, tampilannya akan mengecil karena tidak disesuaikan.
- Untuk mengatasi masalah di atas, kita perlu menetapkan meta tag viewport untuk mengendalikan dan menentukan bentuk dari viewport browser, terutama pada perangkat mobile.
- Jadi, kita dapat melihat ukuran halaman web layaknya diakses pada desktop device.
- Mengatur viewport dapat dilakukan melalui tag **`<meta>`** yang disisipkan dalam elemen **`<head>`**.
- Contohnya :
  - **`<meta name="viewport" content="width=device-width, initial-scale=1">`**
