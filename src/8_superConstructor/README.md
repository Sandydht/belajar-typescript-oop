# Super Constructor
* Pada kasus pewarisan antar class, kadang di child class kita ingin membuat constructor juga, baik itu sama seperti di parent class, ataupun berbeda.
* Pada kasus kita membuat constructor di child class, maka secara otomatis kita harus memanggil constructor di parent class.
* Hal ini sebenarnya sama seperti di JavaScript.
* Kita bisa menggunakan kata kunci ``` super ``` untuk memanggil constructor di parent class.
* Kode: Super Constructor
  ```TSX
  class Person {
    name: string;

    constructor(name: string) {
      this.name = name;
    }
  }

  class Employee extends Person {
    department: string;

    constructor(name: string, department: string) {
      super(name);
      this.department = department;
    }
  }
  ```