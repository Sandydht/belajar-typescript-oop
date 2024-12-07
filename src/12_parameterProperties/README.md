# Parameter Properties
* Kadang, seringnya kita selalu membuat parameter di Constructor yang hanya digunakan sebagai nilai untuk properties.
* Pada kasus seperti ini, kita bisa menggunakan Parameter Properties, yang secara otomatis parameter di Constructor akan dijadikan sebagai Properties di Class nya.
* Untuk membuat Parameter Properties, kita bisa langsung menambahkan visibility pada parameter di Constructor.
* Kode: Parameter Properties
  ```TSX
  class Person {
    constructor(public name: string = '') {

    }
  }

  const person = new Person();
  person.name = 'Sandy';
  console.info(person);
  ```
