# Properties atau Fields
* Properties atau Fields adalah atribut yang dimiliki oleh Class.
* Pada JavaScript, kita bisa langsung saja membuat atribut tanpa harus mendeklarasikan atribut nya.
* Di TypeScript, kita perlu mendeklarasikan propertiesnya terlebih dahulu, beserta dengan tipe data nya.
* Sama seperti ketika membuat attribute di Type atau Interface, kita juga bisa menjadikan properties sebagai optional, mandatory, atau readonly.
* Properties yang mandatory, wajib ditambahkan nilainya di Constructor.
* Kode: Properties
  ```TSX
  class Customer {
    readonly id: number;
    name: string;
    age?: number;

    constructor(id: number, name: string) {
      this.id = id;
      this.name = name;
    }
  }

  const customer = new Customer(1, 'Sandy');
  customer.age = 20;

  console.info(customer);
  ```

# Properties Default Value
* Properties juga bisa memiliki default value, kita bisa tambahkan menggunakan operator = (sama dengan) pada properties yang ingin kita tambahkan default value nya.
* Kode: Properties Default Value
  ```TSX
  class Customer {
    readonly id: number;
    name: string = '';
    age?: number;

    constructor(id: number) {
      this.id = id;
    }
  }
  ```