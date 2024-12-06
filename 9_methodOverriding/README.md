# Method Overriding
* Saat kita membuat child class, kita bisa mendeklarasikan ulang method yang terdapat di parent class.
* Jika semua deklarasi method sama, maka itu adalah method overriding.
* Pada kasus tertentu, kadang kita sering melakukan hal ini.
* Kode: Method Overriding
  ```TSX
  class Employee {
    name: string;

    constructor(name: string) {
      this.name = name;
    }

    sayHello(name: string): void {
      console.info(`Hello ${name}, my name is ${this.name}`);
    }
  }

  class Manager extends Employee {
    sayHello(name: string): void {
      console.info(`Hello ${name}, my name is ${this.name}, I am your manager`);
    }
  }
  ```