## Atribut Pada Elemen Input

- **name**
  - Untuk semua tipe input
  - Menamai elemen input.
  - Data yang diisikan oleh user akan dikirimkan saat formulir di-submit.
  - Jika tidak menyertakannya, data input tidak akan dikirim ke server.
- **placeholder**
  - Untuk tipe text, search, url, tel, email, password dan number.
  - Teks “samar” yang muncul pada kolom input.
  - Teks ini biasanya digunakan sebagai petunjuk atau contoh data yang perlu diisi.
- **required**
  - Untuk semua tipe kecuali hidden, range, color dan button.
  - Atribut ini menyebabkan elemen input wajib diisi untuk di-submit.
  - Merupakan atribut boolean.
- **value**
  - Semua tipe kecuali image.
  - Memberikan data awal atau default pada elemen input.
- **autocomplete**
  - Semua tipe kecuali checkbox, radio dan button.
  - Fitur melengkapi input secara otomatis.
  - Biasanya, ini terjadi ketika kita pernah meng-input sesuatu dan pada kesempatan berikutnya, data tersebut akan ditampilkan lagi oleh browser sebagai autocomplete.
- **maxlength**
  - Untuk tipe text, search, url, tel, email dan password.
  - Menentukan maksimal panjang karakter pada kolom input.
- **max**
  - Untuk tipe date, month, week, time, datetime-local, number, range.
  - Menentukan maksimal nilai yang diperbolehkan.
- **minlength**
  - Untuk tipe text, search, url, tel, email, password.
  - Menentukan minimal panjang karakter yang diperbolehkan pada kolom input.
- **min**
  - Untuk tipe date, month, week, time, datetime-local, number, range.
  - Menentukan minimal nilai yang diperbolehkan.
- **checked**
  - Untuk tipe checkbox dan radio.
  - Mengaktifkan atau mencentangkan input checkbox.
- **accept**
  - Untuk tipe file.
  - Panduan atau batasan format berkas apa yang diperbolehkan pada input berkas.
- **multiple**
  - Untuk tipe email dan file.
  - Memungkinkan pemilihan ganda pada elemen input.
- **pattern**
  - Untuk tipe text, search, url, tel, email dan password.
  - Menentukan pola yang wajib dipatuhi pada data yang diisi agar dapat valid.
- **readonly**
  - Semua tipe, kecuali hidden, range, color, checkbox, radio, dan button.
  - Tidak memiliki akses edit nilai.
- **disabled**
  - Untuk semua tipe
  - Memberikan efek tidak aktif pada elemen input
    <br>
- Tidak hanya memberikan fitur lebih, beberapa atribut lainnya dapat **mengaktifkan proses validasi** terhadap data yang dimasukkan user, seperti required, pattern, max, maxlength, dsb.
- Menentukan tipe pada elemen input merupakan salah satu penerapan validasi. Contohnya, jika Anda
- Menerapkan tipe email dan tidak mengisi data dengan email valid, sebuah popup error akan muncul untuk memberi petunjuk pada user agar data yang dimasukkan valid.
