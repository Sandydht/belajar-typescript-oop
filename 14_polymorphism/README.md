# Polymorphism
* Polymorphism berasal dari bahasa Yunani yang berarti banyak bentuk.
* Dalam OOP, polymorphism adalah kemampuan sebuah object berubah bentuk menjadi bentuk lain.
* Polymorphism erat hubungannya dengan inheritance.
* Kode: Class Inheritance
  ```TSX
  class Employee {
    constructor(public name: string) {

    }
  }

  class Manager extends Employee {

  }

  class VicePrecident extends Manager {

  }
  ```
* Kode: Polymorphism
  ```TSX
  let employee: Employee = new Employee('Budi');
  console.info(employee);

  employee = new Manager('Dwi');
  console.info(employee);

  employee = new VicePrecident('Sandy');
  console.info(employee);
  ```

# Method Polymorphism
* Saat kita membuat function / method dengan parameter, kita juga bisa mengirim data polymorphism pada parameter tersebut.
* Misal kita membuat sebuah function dengan parameter class Employee, kita bisa mengirim object dalam bentuk Employee, Manager ataupun VicePrecident.
* Hal ini karena Manager dan VicePrecident merupakan turunan dari Employee, sehingga kita bisa mengirim data seluruh turunan dari Employee.
* Kode: Method Polymorphism
  ```TSX
  function sayHello(employee: Employee): void {
    console.info(`Hello ${employee.name}`);
  }

  sayHello(new Employee('Budi'));
  sayHello(new Manager('Dwi'));
  sayHello(new VicePrecident('Sandy'));
  ```