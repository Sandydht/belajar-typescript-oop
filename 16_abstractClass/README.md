# Abstract Class
* Abstract Class merupakan deklarasi Class yang belum selesai.
* Abstract Class membolehkan memiliki properties atau method yang abstract atau belum di buat implementasinya.
* Abstract Class juga tidak bisa dibuat menjadi object menggunakan kata kunci ``` new ```.
* Kegunaan Abstract Class hanya digunakan sebagai Parent Class yang nanti diturunkan ke Child Class nya.
* Kode: Abstract Class
  ```TSX
  abstract class Customer {
    readonly id: number;
    abstract name: string;

    constructor(id: number) {
      this.id = id;
    }

    abstract sayHello(name: string): void;
  }
  ```
* Kode: Child Class dari Abstract Parent
  ```TSX
  class RegularCustomer extends Customer {
    name: string;

    constructor(id: number, name: string) {
      super(id);
      this.name = name;
    }

    sayHello(name: string): void {
      console.info(`Hello ${name}, my name is ${this.name}`);
    }
  }
  ```