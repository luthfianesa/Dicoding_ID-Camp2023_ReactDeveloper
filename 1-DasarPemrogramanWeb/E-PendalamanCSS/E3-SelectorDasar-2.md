## E3.1 ID Selector

- Sama seperti class, atribut id dapat diterapkan pada seluruh elemen HTML, dan kebanyakan atribut ini digunakan untuk memberikan sebuah arti pada generic element seperti `<div>` dan `<span>`.
- Namun, atribut id ini tidak bersifat shareable, yang artinya nilai id ini harus unik dan digunakan pada satu elemen saja.
- Untuk menetapkan selector dengan menggunakan id, kita gunakan tanda **octothorpe** (#) atau lebih familiar disebut dengan hash.

## E3.2 Attribut Selector

- Attribute selector merupakan cara menetapkan target elemen berdasarkan sebuah atribut yang digunakan atau bahkan bisa lebih spesifik dengan nilainya.

  - **`[attr]`** -> Menargetkan elemen yang menerapkan atribut attr.
  - **`[attr=value]`** -> Menargetkan elemen yang menerapkan atribut attr dengan nilai value.
  - **`[attr~=value]`** -> Menargetkan elemen yang menerapkan atribut attr dan salah satu nilainya adalah value.
  - **`[attr^=value]`** -> Menargetkan elemen yang menerapkan atribut attr dan nilainya diawali dengan nilai value.
  - **`[attr$=value]`** -> Menargetkan elemen yang menerapkan atribut attr dan nilainya diakhiri dengan value.
  - **`[attr*=value]`
    ** -> Menargetkan elemen yang menerapkan atribut attr dan nilainya mengandung value.

## E3.3 Universal Selector

- Universal selector digunakan untuk diterapkan pada seluruh elemen.
- Namun, selector ini juga bisa secara spesifik menargetkan sebuah elemen dengan menggabungkannya bersama selector yang lain.
