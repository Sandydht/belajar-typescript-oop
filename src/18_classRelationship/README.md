# Class Relationship
* Karena implementasi dari object di TypeScript adalah JavaScript object.
* Jadi sebenarnya jika terdapat dua object walaupun berbeda class, tetapi secara properties dan function sama, secara struktur JavaScript object adalah sama.
* Pada kasus seperti itu, kita bisa membuat object untuk tipe data A, dengan membuat object dari tipe data B, asal secara properties dan method sama.
* Kode: Class Relationship
  ```TSX
  class Person {
    constructor(public name: string) {

    }
  }

  class Customer {
    constructor(public name: string) {

    }
  }

  const person: Person = new Customer('Sandy');
  ```