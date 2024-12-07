# Type Cast
* Di TypeScript dasar, kita pernah belajar tentang type assertions, dimana kita bisa mengubah tipe data dari satu tipe data lainnya yang lebih specific atau detail.
* Ini juga bisa kita lakukan pada kasus Method Polymorphism.
* Kita bisa kombinasikan operator instanceof dan type assertions.
* Kode: Type Cast
  ```TSX
  function sayHello(employee: Employee): void {
    if (employee instanceof VicePresident) {
      const vp = employee as VicePresident;
      console.info(`Hello VP ${vp.name}`);
    } else if (employee instanceof Manager) {
      const manager = employee as Manager;
      console.info(`Hello Manager ${manager.name}`);
    } else {
      console.info(`Hello Employee ${employee.name}`);
    }
  }
  ```

# Perlu Diingat
* Saat melakukan Type Cast, pastikan posisi Child paling bawah dilakukan pengecekan di awal.
* Hal ini agar tidak terjadi kesalahan konversi.
* Contoh, jika kita ubah posisi pengecekan instanceof Manager dan VicePresident, maka ketika kita mengirim VicePresident, dia akan berhenti di Manager, hal ini karena hasil instanceof bernilai true, karena VicePresident adalah turunan dari Manager.
* Kode: Type Cast Salah
  ```TSX
  function sayHelloWrong(employee: Employee): void {
    if (employee instanceof Manager) {
      const manager = employee as Manager;
      console.info(`Hello Manager ${manager.name}`);
    } else if (employee instanceof VicePresident) {
      const vp = employee as VicePresident;
      console.info(`Hello VP ${vp.name}`);
    } else {
      console.info(`Hello Employee ${employee.name}`);
    }
  }

  sayHello(new Employee('Budi'));
  sayHello(new Manager('Dwi'));
  sayHello(new VicePresident('Sandy'));
  ```