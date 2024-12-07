# Interface Inheritance
* Di bahasa pemrograman seperti Java, kadang interface digunakan sebagai kontrak.
* Di TypeScript, hal itu juga bisa dilakukan, kita bisa membuat class yang mengikuti kontrak sebuah interface, caranya dengan menggunakan kata kunci ``` implements ```.
* Karena sebenarnya ini bukanlah pewarisan, oleh karena itu untuk ``` implements ```, kita bisa melakukan implements ke lebih dari satu interface, dimana pada extends hal ini tidak bisa dilakukan.
* Kode: Interface
  ```TSX
  interface HasName {
    name: string;
  }

  interface CanSayHello {
    sayHello(name: string): void;
  }
  ```
* Kode: Implements Interface
  ```TSX
  class Person implements HasName, CanSayHello {
    name: string;

    constructor(name: string) {
      this.name = name;
    }

    sayHello(name: string): void {
      console.info(`Hello ${name}, my name is ${this.name}`);
    }
  }
  ```