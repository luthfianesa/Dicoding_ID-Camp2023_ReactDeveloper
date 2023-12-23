## E4.1 Properti dan Method

- Kita sudah tahu bahwa class (function constructor dalam JavaScript)
- merupakan sebuah **object blueprint** yang dapat **membuat sebuah objek serupa lebih mudah**.
- Dengan menggunakan class, kita bisa terhindar dari banyak duplikasi kode dalam membuat banyak objek sekaligus.
- Di dalam sebuah class, kita dapat **mendefinisikan dua hal**, yaitu properti dan method.


### A. Properti

- Properti merupakan bagian dari class yang **mendefinisikan nilai-nilai yang terkandung dalam sebuah instance class**.
- Contohnya, jika Anda membuat class Car, properti adalah informasi yang sekiranya terdapat pada sebuah mobil seperti brand, color, maxSpeed, dan chassisNumber.
- Contoh lain, jika Anda membuat class Mail, secara umum propertinya adalah sender, receiver, subject, dan body.

  ```
  class Car {
    constructor(brand, color, maxSpeed, chassisNumber) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this.chassisNumber = chassisNumber;
    }
  }

  class Mail {
    constructor(sender, receiver, subject, body) {
      this.sender = sender;
      this.receiver = receiver;
      this.subject = subject;
      this.body = body;
    }
  }
  ```

- **Nilai dari properti biasanya diambil dari dari argumen constructor** agar nilainya dapat bervariasi setiap kali membuat instance.

  ```
  class Car {
    constructor(brand, color, maxSpeed, chassisNumber) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this.chassisNumber = chassisNumber;
    }
  }

  const car1 = new Car('BMW', 'red', 200, 'b-1');
  const car2 = new Car('Audi', 'blue', 220, 'a-1');
  const car3 = new Car('BMW', 'black', 250, 'b-2');

  console.log(car1);
  console.log(car2);
  console.log(car3);

  /* Output:
  Car { brand: 'BMW', color: 'red', maxSpeed: 200, chassisNumber: 'b-1' }
  Car { brand: 'Audi', color: 'blue', maxSpeed: 220, chassisNumber: 'a-1' }
  Car { brand: 'BMW', color: 'black', maxSpeed: 250, chassisNumber: 'b-2' }
  */
  ```

- Namun, adakalanya nilai properti juga bisa didefinisikan di dalam class itu sendiri.
- Contohnya, kita tidak ingin pengguna menentukan nomor rangka mobil secara mandiri,
- maka kita bisa memberi nilai properti chassisNumber langsung di dalam fungsi constructor.
  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      // Set a random chassis number
      this.chassisNumber = `${brand}-${Math.floor(Math.random() * 1000) + 1}`;
    }
  }
  ```

#### Properti Getter dan Setter

- Secara standar, **properti di dalam sebuah instance class bersifat mutable** atau dapat diubah nilainya.
- Meskipun kita sudah menetapkan nilai chassisNumber oleh sistem,
- nyatanya nilai tersebut dapat diubah dengan mudah ketika objek mobil telah dibuat.

  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this.chassisNumber = `${brand}-${Math.floor(Math.random() * 1000)}`;
    }
  }


  const car = new Car('BMW', 'red', 200);
  car.chassisNumber = 'BMW-1';

  console.log(car);

  /* Output:
  Car { brand: 'BMW', color: 'red', maxSpeed: 200, chassisNumber: 'BMW-1' }
  */
  ```

- Lalu, bagaimana cara memproteksi agar nilai dari **properti** chassisNumber **tidak dapat diubah**?
- Nah, ketika kita berhadapan dengan kasus seperti ini, kita bisa memanfaatkan properti **getter** dan **setter**.
- Sebelum memecahkan masalah di atas, ketahuilah bahwa ada **dua tipe properti**

  - **Data property**
  - **Accessor property**

- Data property merupakan properti yang sejauh ini kita lihat,
- properti yang langsung menampung sebuah nilai di dalam sebuah objek.
- Sedangkan **accessor property** merupakan **properti yang dikontrol oleh sebuah getter dan setter**.
- Nilai yang didapatkan dari properti tersebut dikontrol oleh **method get**
- dan cara menetapkan nilai tersebut dikontrol oleh **method set**.
- Berikut contoh dari accessor property :

    ```
    class User {
      constructor(firstName, lastName) {
      this.firstName = firstName;
      this.lastName = lastName;
    }

      get fullName() {
        return `${this.firstName} ${this.lastName}`;
      }

      set fullName(fullName) {
        const [firstName, lastName] = fullName.split(' ');
        this.firstName = firstName;
        this.lastName = lastName;
      }
    }

    const user = new User('John', 'Doe');
    console.log(user);
    console.log(user.fullName);

    user.fullName = 'Fulan Fulanah';
    console.log(user);
    console.log(user.fullName);

    /* Output:
    User { firstName: 'John', lastName: 'Doe' }
    John Doe
    User { firstName: 'Fulan', lastName: 'Fulanah' }
    Fulan Fulanah
    */
    ```

- Di dalam class User, Anda bisa melihat bahwa terdapat data property firstName dan lastName.
- Nilai dari properti tersebut ditetapkan via **argumen constructor**.
- Selain itu, Anda juga bisa melihat sebuah method get fullName dan set fullName.
- Method tersebut merupakan accessor property yang mengatur cara akses dari properti fullName.
- Sebab kita menetapkan getter dan setter untuk properti fullName, maka kita bisa mengakses properti tersebut melalui instance User.
- Ketika kita coba mendapatkan nilai properti fullName dengan cara user.fullName,
- method getter akan dijalankan dan nilai yang dikembalikan akan menjadi nilai dari properti tersebut.
- Begitu juga ketika kita coba menetapkan nilai properti fullName dengan cara user.fullName = “Fulan Fulanah”,
- kode di dalam method setter akan dijalankan.
- Catatan penting yang perlu Anda ketahui mengenai getter setter adalah:
  - 1. method getter harus mengembalikan sebuah nilai dan nilai tersebut akan menjadi nilai properti
  - 2. method setter harus menerima satu argumen yang nilainya diambil dari operand ke dua ketika melakukan assignment operator.
- Mari kita kembali ke masalah perubahan nilai properti chassisNumber.
- Bagaimana getter dan setter dapat memproteksi perubahan properti chassisNumber?
- Di JavaScript, pola yang sering diterapkan untuk memecahkan masalah ini adalah
- dengan memanfaatkan **getter setter sebagai “wrapper”** dari properti aslinya.
- Tujuannya agar getter setter bisa mengontrol akses seperti mendapatkan dan menetapkan nilai properti.
- Untuk menerapkan pola ini, pertama kita perlu mengubah nama dari properti chassisNumber, misalnya dengan **menambahkan tanda garis bawah** di depannya menjadi `_chassisNumber`.
  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this._chassisNumber = `${brand}-${Math.floor(Math.random() * 1000)}`;
    }
  }
  ```
- Lalu, kita tetapkan getter dan setter untuk properti chassisNumber.
- Untuk getter, kita kembalikan dengan nilai properti `_chassisNumber`.

  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this._chassisNumber = `${brand}-${Math.floor(Math.random() * 1000)}`;
  }

    get chassisNumber() {
      return this._chassisNumber;
    }
  }
  ```

- Kita tidak ingin nilai chassisNumber dapat diubah sehingga untuk setter properti chassisNumber,
- cetak saja teks peringatan menggunakan console.log() seperti ini.

  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this._chassisNumber = `${brand}-${Math.floor(Math.random() * 1000)}`;
    }

    get chassisNumber() {
      return this._chassisNumber;
    }

    set chassisNumber(chassisNumber) {
      console.log('you are not allowed to change the chassis number');
    }
  }
  ```

- Lantas, ketika kita membuat instance Car, nilai chassisNumber tidak dapat diubah.

  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this._chassisNumber = `${brand}-${Math.floor(Math.random() * 1000)}`;
    }

    get chassisNumber() {
      return this._chassisNumber;
    }

    set chassisNumber(chassisNumber) {
      console.log('you are not allowed to change the chassis number');
    }
  }

  const car = new Car('BMW', 'red', 200);
  console.log(car.chassisNumber);
  car.chassisNumber = 'BMW-1';
  console.log(car.chassisNumber);

  /* Output:
  BMW-232
  you are not allowed to change the chassis number
  BMW-232
  */
  ```

- Sebenarnya nilai chassisNumber masih bisa berubah jika kita mengubah langsung melalui properti `_chassisNumber`.
- Namun, ketahuilah bahwa **mengubah atau mendapatkan nilai properti objek yang diawali dengan tanda underscore tidak direkomendasikan**. - - Alasanya, komunitas JavaScript menyepakati bahwa hal **properti yang diberi tanda underscore bukan untuk diakses**, alias bersifat privat.
- JavaScript versi **ES2022 hadir dengan fitur private identifier**.
- Dengan fitur tersebut, kita bisa membuat private property.
- Ini akan memecahkan masalah di atas.

### B. Method

- Method adalah sebuah **fungsi yang berada di dalam sebuah class**
- dan dapat **diakses melalui instance Class** tersebut.
- Method biasanya **mengindikasikan hal yang dapat dilakukan oleh sebuah class**.
- Bila kita berbicara tentang class Car, method yang ada bisa drive(), reverse(), dan turn().
- Jika pada class Mail, method bisa berupa send(), sendLater(), saveAsDraft().

  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this._chassisNumber = `${brand}-${Math.floor(Math.random() * 1000)}`;
    }

    get chassisNumber() {
      return this._chassisNumber;
    }

    set chassisNumber(chassisNumber) {
      console.log('you are not allowed to change the chassis number');
    }

    // Methods
    drive() {
      console.log(`${this.brand} ${this.color} is driving`);
    }

    reverse() {
      console.log(`${this.brand} ${this.color} is reversing`);
    }

    turn(direction) {
      console.log(`${this.brand} ${this.color} is turning ${direction}`);
    }
  }

  class Mail {
    constructor(sender, receiver, subject, body) {
      this.sender = sender;
      this.receiver = receiver;
      this.subject = subject;
      this.body = body;
    }

    // Methods
    send() {
      console.log(`Sending mail from ${this.sender} to ${this.receiver}`);
    }

    sendLater(delay) {
      console.log(`Sending after ${delay} ms`);

      setTimeout(() => {
        this.send();
      }, delay);
    }

    saveAsDraft() {
      console.log('Saving mail as draft');
    }
  }
  ```

- Sama seperti fungsi JavaScript, **method bisa menerima sebuah argumen**.
- Contohnya pada method turn() di class Car dan sendLater di class Mail, kami memanfaatkan argumen direction dan delay untuk menetapkan arah dan waktu delay dalam menjalankan method-nya.
- Selain argumen, method juga dapat memiliki akses ke nilai properti atau method lainnya melalui keyword this.
- Method di dalam class hanya bisa dijalankan melalui instance dari class tersebut.

  ```
  const car = new Car('BMW', 'red', 200);

  car.drive();
  car.turn('left');
  car.reverse();

  /* Output:
  BMW red is driving
  BMW red is turning left
  BMW red is reversing
  */
  ```

- Method memang kental dengan “kemampuan” yang bisa dilakukan oleh sebuah class,
- tetapi praktik nyatanya membuat method tidak hanya untuk itu.
- Method juga biasa dibuat ketika kita perlu mengekstraksi sebuah kode agar lebih mudah untuk dibaca
- dan method tersebut hanya digunakan untuk kebutuhan internal saja.
- Contoh, pada class Car, kita menetapkan nilai `_chassisNumber` dengan nilai random yang ditulis di dalam constructor.
- Hal itu membuat kode di dalam constructor menjadi sulit dibaca karena dicampuri dengan logika dalam menghasilkan angka acak.
- Agar kode di dalam constructor lebih rapi,
- kita bisa membuat method yang digunakan internal yang menampung kode random tersebut.
- Biasanya method yang hanya digunakan secara internal disebut dengan **private** dan namanya diawali dengan **tanda underscore**.

  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this._chassisNumber = this._generateChassisNumber();
    }

    get chassisNumber() {
      return this._chassisNumber;
    }

    set chassisNumber(chassisNumber) {
      console.log('you are not allowed to change the chassis number');
    }

    // Methods
    drive() {
      console.log(`${this.brand} ${this.color} is driving`);
    }

    reverse() {
      console.log(`${this.brand} ${this.color} is reversing`);
    }

    turn(direction) {
      console.log(`${this.brand} ${this.color} is turning ${direction}`);
    }

    _generateChassisNumber() {
      return `${this.brand}-${Math.floor(Math.random() * 1000)}`;
    }
  }
  ```

## E4.2 Member Visibility

- Member visibility bisa disebut juga sebagai **hak akses pada sebuah properti dan method di dalam class**.
- Secara **default**, seluruh properti dan method yang dibuat di dalam **class bersifat public**,
- alias dapat diakses di luar dari kode class via instance.
- Selain public, kita juga bisa membuat properti dan method bersifat private,
- terutama ketika kita ingin properti atau method tersebut
- hanya digunakan dalam cakupan kode di dalam class saja (penggunaan internal).
- Pemberian tanda underscore pada properti atau method bisa dijadikan sebagai penanda bahwa ia dianggap private.
- Masalahnya adalah cara tersebut tidak benar-benar memproteksi hak aksesnya.
- Contoh, pada class Car, kita sudah membuat properti `_chassisNumber` dan method `_generateChassisNumber()` dengan tanda underscore.
- Namun, kedua member tersebut tetap saja masih bisa di akses via instance, bahkan kita bisa mengubah nilainya.

  ```
  class Car {
    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this._chassisNumber = this._generateChassisNumber();
    }

    get chassisNumber() {
      return this._chassisNumber;
    }

    set chassisNumber(chassisNumber) {
      console.log('you are not allowed to change the chassis number');
    }

    // Methods
    drive() {
      console.log(`${this.brand} ${this.color} is driving`);
    }

    reverse() {
      console.log(`${this.brand} ${this.color} is reversing`);
    }

    turn(direction) {
      console.log(`${this.brand} ${this.color} is turning ${direction}`);
    }

    _generateChassisNumber() {
      return `${this.brand}-${Math.floor(Math.random() * 1000)}`;
    }
  }

  const car = new Car('BMW', 'red', 200);

  console.log(car._chassisNumber);
  car._chassisNumber = 'BMW-1';
  console.log(car._chassisNumber);
  console.log(car._generateChassisNumber());

  /* Output:
  BMW-85
  BMW-1
  BMW-667
  */
  ```

- Untuk menyelesaikan masalah ini, JavaScript versi ES2022 secara resmi mengenalkan cara
- dalam menetapkan hak akses private pada properti dan method objek,
- yakni dengan menambahkan tanda # di awal penamaan properti atau method.

  ```
  class Car {
    #chassisNumber = null;

    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this.#chassisNumber = this.#generateChassisNumber();
  }

    get chassisNumber() {
      return this.#chassisNumber;
    }

    set chassisNumber(chassisNumber) {
      console.log('you are not allowed to change the chassis number');
    }

    // Methods
    drive() {
      console.log(`${this.brand} ${this.color} is driving`);
    }

    reverse() {
      console.log(`${this.brand} ${this.color} is reversing`);
    }

    turn(direction) {
      console.log(`${this.brand} ${this.color} is turning ${direction}`);
    }

    #generateChassisNumber() {
      return `${this.brand}-${Math.floor(Math.random() * 1000)}`;
    }
  }
  ```

- Khusus untuk properti yang sifatnya private,
- Anda harus mendeklarasikan propertinya di enclosing class seperti ini :

  ```
  class Car {
    #chassisNumber = null; // enclosing class

    constructor(brand, color, maxSpeed) {
      this.brand = brand;
      this.color = color;
      this.maxSpeed = maxSpeed;
      this.#chassisNumber = this.#generateChassisNumber();
    }

  // ... kode lainnya.
  }
  ```

- Dengan begitu, properti dan method yang sifatnya private
- tidak dapat diakses di luar dari cakupan kode class, misalnya via instance.
