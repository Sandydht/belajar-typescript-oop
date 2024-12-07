# Namespace
* Selain menggunakan JavaScript Modules, di TypeScript ada cara lain untuk mengorganisir kode program kita, yaitu menggunakan Namespace.
* Namespace biasanya digunakan untuk mengorganisir kode ketika dalam satu module terdapat banyak sekali kode, sehingga bisa kita kelola dalam Namespace.
* Jika Module kita anggap sebuah folder, maka Namespace adalah sub folder di dalam Module.
* Untuk membuat Namespace, kita bisa gunakan kata kunci ``` namespace ```, dan kita bisa tambahkan class function, dan lain - lain di dalam Namespace tersebut.
* Kode: Namespace
  ```TSX
  export namespace MathUtil {
    export const PI: number = 3.14;

    export function sum(...value: number[]): number {
      let total = 0;

      for (let value of values) {
        total += value;
      }

      return total;
    }
  }
  ```
* Kode: Menggunakan Namespace
  ```TSX
  console.info(MathUtil.PI);
  console.info(MathUtil.sum(1, 2, 3, 4, 5));
  ```