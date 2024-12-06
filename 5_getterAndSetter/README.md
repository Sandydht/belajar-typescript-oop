# Getter and Setter
* Sampai sekarang, ketika kita ingin mengubah data properties, kita bisa langsung gunakan operator = (sama dengan), dan ketika ingin mengambil data cukup gunakan . (titik).
* JavaScript memiliki fitur bernama Getter dan Setter, begitu juga di TypeScript, dimana kita bisa membuat method untuk mengubah properties dan juga method untuk mengambil properties.
* Karena bentuknya adalah method, maka kita bisa menambahkan validasi apapun pada method tersebut sebelum properties aslinya diubah.
* Kode: Getter dan Setter
  ```TSX
  class Category {
    _name?: string;

    get name(): string {
      if (this._name) {
        return this._name;
      } else {
        return 'empty';
      }
    }

    set name(value: string) {
      if (value !== '') {
        this._name = value;
      }
    }
  }

  const category = new Category();
  console.info(category.name);

  category.name = 'Food';
  console.info(category.name);

  category.name = '';
  console.info(category.name);
  ```