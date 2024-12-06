# Visibility
* Di JavaScript dan TypeScript secara default setiap membuat properties atau method, maka sifatnya adalah bisa diakses di dalam class, atau diluar class (public).
* Di JavaScript, kita mengenal private properties atau method, dimana menggunakan prefix ``` # ```, yang secara otomatis hanya bisa diakses di dalam class.
* Di TypeScript, visibility ini dipermudah, dengan mengenalkan tiga kata kunci, public, private, dan protected.

# Visibilty di TypeScript
| Visibility (Properties & Methid) | Keterangan                             | 
| -------------------------------- | -------------------------------------- |
| public                           | Bisa diakses dimanapun, secara default |
|                                  | jika tidak menyebutkan visibility      |
|                                  | maka akan menggunakan visibility       | 
|                                  | public                                 |
| -------------------------------- | -------------------------------------- |
| private                          | Hanya bisa diakses oleh class nya      | 
|                                  | sendiri                                |
| -------------------------------- | -------------------------------------- |
| protected                        | Sama seperti private, tapi bisa juga   |
|                                  | diakses oleh class turunannya          |
| -------------------------------- | -------------------------------------- |

* Kode: Counter
  ```TSX
  class Counter {
    private counter: number = 0;

    public increment(): void {
      this.counter++;
    }

    public getCounter(): number {
      return this.counter;
    }
  }
  ```
* Kode: Double Counter
  ```TSX
  class Counter {
    protected counter: number = 0;

    public increment(): void {
      this.counter++;
    }

    public getCounter(): number {
      return this.counter;
    }
  }

  class DoubleCounter extends Counter {
    public increment(): void {
      this.counter += 2;
    }
  }
  ```