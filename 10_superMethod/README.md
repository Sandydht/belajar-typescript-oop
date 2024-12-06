# Super Method
* Sama seperti constructor, saat kita membuat method overriding, kita juga bisa memanggil method yang sama yang terdapat di parent class dengan menggunakan kata kunci ``` super ```, lalu diikuti dengan method yang ingin kita panggil.
* Kode: Super Method
  ```TSX
  class Manager extends Employee {
    sayHello(name: string): void {
      super.sayHello(name);
      console.info('And, I am your manager');
    }
  }
  ```