# Constructor
* Constructor adalah method atau function yang dipanggil ketika pertama kali object dibuat dari class.
* Constructor sama seperti Function biasanya, bisa memiliki parameter, yang membedakan adalah pada constructor, kita tidak perlu mengembalikan value.
* Kode: Constructor
  ```TSX
  class Customer {
    constructor() {
      console.info('Create new customer');
    }
  }

  new Customer();
  new Customer();
  ```