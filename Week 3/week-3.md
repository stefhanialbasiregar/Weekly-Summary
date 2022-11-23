# JavaScript Intermediate

## **Array**

Array -> tipe data list order yg bisa menyimpan **banyak data** beserta **bermacam tipe data** sekaligus

Cara mendefinisikan array pada JS adalah dengan menggunakan **square brackets**.

```javascript
let hewan = ["sapi", "burung", "tikus"];
```

Contoh di atas adalah array yang menyimpan satu tipe data, yaitu tipe data **String**.

```javascript
let wanita = ["melinda", 20, true];
```

Sedangkan contoh di atas adalah contoh array yang menyimpan **banyak tipe data** sekaligus.

Pada JS array dimulai dari index ke-0.

<img src="week 3/gambar-1.jpeg"/>

Cara memanggil nilai array adalah dengan memanggil sesuai indexnya.

```javascript
let wanita = ["melinda", 20, true];

console.log(wanita[1]);
//Output: 20
```

Cara mengupdate nilai tertentu pada array adalah dengan cara:

```javascript
let wanita = ["melinda", 20, true];

console.log(wanita[1]);
//Output: 20

//wanita[1] akan diubah nilainya

wanita[1] = ["meja"];

console.log(wanita[1]);
//Output: meja
```

apabila ada array yang didefinisikan dengan menggunakan `const`, maka nilai di dalam array tersebut masih bisa diubah.

```javascript
const cars = ["tesla", "honda", "toyota"];

cars[2] = ["mercedes"];

console.log(cars);
// Output: ['tesla', 'honda', 'mercedes']
```

Array Properties -> fitur yg disedaikan JS untuk memudahkan developer. Beberapa di antaranya adalah:

- constructor -> Returns the function that created the Array object's prototype
- length -> mengembalikan nilai dari panjang data array
- prototype -> Allows you to add properties and methods to an Array object

```javascript
const cars = ["tesla", "honda", "toyota"];

console.log(cars.length);
// Output: 3
```

Array Built-in Methods -> **method yang sudah tersedia** untuk memanipulasi isi array

- .push() -> **menambahkan** item array pada **urutan paling terakhir**

- .pop() -> **menghapus** item array pada **urutan paling terakhir**

- .shift() -> **menghapus** item array pada **urutan pertama**

- .unshift() -> **menambahkan** item array pada **urutan pertama**

- .sort() -> mengurutkan secara ascending/discending

Looping pada Array -> Looping pada array dilakukan dengan menggunakan built-in method, yaitu **.map()** dan **.forEach()**

- .map() -> looping utk membuat array baru

Gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

```javascript
let arr = [1, 2, 3, 4, 5];

arr.forEach((num, index) => {
  return (arr[index] = num * 2);
});

console.log(arr);
//Output : [2, 4, 6, 8, 10]
```

- .forEach() -> loop untuk setiap elemennya sendiri

gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.

```javascript
let arr = [1, 2, 3, 4, 5];

let doubled = arr.map((num) => {
  return num * 2;
});

console.log(doubled);
//Output : [2, 4, 6, 8, 10]
```

## **Multidimensional Array**

Multidimensional Array bisa dianalogikan dengan array of array.

Ada array didalam array.

```javascript
let siswaTinggiBadan = [["Adam", 169], ["Melissa", 155][("Zaki", 167)]];
```

Array dimensional bisa dibayangkan seperti sebuah tabel.

Cara mengakses nilai pada array multidimensional adalah dengan memanggil nilai index dari baris dan kolomnya.

```javascript
let siswaTinggiBadan = [["Adam", 169], ["Melissa", 155][("Zaki", 167)]];

console.log(siswaTinggiBadan[2][1]);
//Output : 167
```

Sama halnya dengan array satu dimensional, array multidimensional juga memiliki built-in method dan looping yang dapat dilakukan terhadap array multidimensional.

## **Object pada JavaScript**

Object pada bahasa pemrograman adalah sesuatu yang memiliki atribut (properti) dan method (fungsi).

Contohnya: Apel memiliki atribut seperti warna: merah, jenis: fuji.

**Object** termasuk ke dalam **tipe data** pada JavaScript.

Cara membuat object pada JavaScript.

```javascript
let person = {}; //person is an empty object

let person = {
    name: 'Farrah',
    age: 20
    isMarried: false,
}
```

Sama seperti array, didalam object kita dapat menyimpan properti dengan tipe data apapun.

Mengakses Objek dan Mengakses Properti Objek

- mengakses seluruh objek vs mengakses properti pada objek

```javascript
let person = {
    name: 'Farrah',
    age: 20
    isMarried: false,
}

//mengakses seluruh properti pada objek
console.log(person);

//mengakses properti name pada objek
console.log(person.name);

//mengakses objek dgn menggunakan bracket notation
console.log(person['name']);
```

**Update data object**

```javascript
let person = {
    name: 'Farrah',
    age: 20
    isMarried: false,
}

person.name = 'Andin';

console.log(person.name);
//Output : Andin
```

**update seluruh data pada object**

update keseluruhan data pada object hanya berlaku pada object yang didefinisikan menggunakan keyword **let**. object yang didefinisikan menggunakan **const** tidak bisa diganti keseluruhan datanya, namun tetap bisa diupdate beberapa data di dalamnya.

```javascript
const person = {
    name: 'Farrah',
    age: 20
    isMarried: false,
}

person = {
    motherName: 'Riana'
}

console.log(person);
//Output : Uncaught TypeError: Assignment to constant variable
```

Jadi jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel.

```javascript
let person = {
    name: 'Farrah',
    age: 20
    isMarried: false,
}

person = {
    motherName: 'Riana'
}

console.log(person);
// Output : {
//     motherName: 'Riana'
// }
```

Kita dapat **menghapus properti** dari object menggunakan **delete** operator.

```javascript
let person = {
    name: 'Farrah',
    age: 20
    isMarried: false,
}

delete person.isMarried;

console.log(person);
// Output : {
//     name: 'Farrah',
//     age: 20
// }
```

**Membuat method untuk Object**

Kita bisa membuat method custom untuk kita gunakan pada aplikasi kita loh. Kita akan membuat method untuk **greeting** pada aplikasi ecommerce misalnya.

```javascript
const greeting = {
    welcome: function () {
        return 'Halo Selamat Datang!';
    }

    afterTransaction: function ( {
        return 'Terima kasih sudah berbelanja di sini!';
    })
};

console.log(greeting.welcome());
//Output: 'Halo Selamat Datang!'
```

**Nested Object**

Pada real application nanti kalian pasti menemukan data object yang kompleks, misalnya Object yang berasal dari **turunan object lainnya**.

**Passed by Referenced**

Kita bisa mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function.

Ini biasa disebut **passed by reference**.

```javascript
let number = {
  originA: 2,
  originB: 3,
};

function changeData(obj) {
  obj.originA = 4;
  obj.originB = 6;
}

changeData(number);
console.log(number.originA); // 4
console.log(number.originB); // 6
```

**Looping Object**

Jika kita ingin menampilkan seluruh object properti, kita bisa menggunakan looping.

Jadi tidak perlu mengakses secara manual memanggil setiap propertinya.

```javascript
for (let key in object) {
  // ..
}
```

contohnya:

```javascript
let person = {
    name: 'Farrah',
    age: 20
    isMarried: false,
}

for(let data in person) {
    console.log(person[data]);
};
// 'Farrah'
// 20
// false
```

**Array of Object**

Array sama halnya dengan Object, dapat menyimpan lebih dari satu data dan tipe data. Karena Object adalah tipe data, maka Array juga dapat menampung tipe data Object di dalamnya.

contoh:

```javascript
let students = [
  {
    name: "John Doe",
    age: 23,
  },
  {
    name: "Citra",
    age: 18,
  },
  {
    name: "Adam",
    age: 40,
  },
];

//gunakan forEach jika array mengandung object
students.forEach((listStudent) => {
  console.log(listStudent);
});
```

## **Recursive**

Recursive adalah function yang **memanggil dirinya sendiri** sampai kondisi tertentu.

Ciri fungsi rekursif

- memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti
- memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya

contohnya adalah fungsi untuk mencari nilai dari suatu angka (misal x) yang akan dipangkatkan dengan suatu angka lain (misal n)

```javascript
function pow(x, n) {
  if ((n = 1)) {
    return x;
  } else {
    return x * pow(x, n - 1);
  }
}

console.log(pow(2, 3)); // 8
```

## **Asyncronous**

Javascript adalah bahasa pemrograman yang bersifat

- single thread (satu jalur)

<img src="gambar-2.png">

- non blocking (jika suatu proses dijalankan dan memakan waktu, maka proses yang lain dapat langsung diproses alias tidak perlu menunggu)

- asynchronous (suatu proses bisa disela. apabila suatu proses belum selesai maka proses lain dapat langsung dipanggil)

Pada asynchronous terdapat 3 kunci utama:

- Callback
- Promise
- Async await

### Callback

Callback adalah function yang dijadikan sebagai argumen. Callback (dipanggil kembali) akan menyimpan suatu proses ke dalam callback queue baru setelah itu akan dipanggil kembali.

```javascript
() => {}; //bentuk callback

//callback yang dijadikan sebuah argumen (dimasukkan dalam parameter sebuah function lain)
function( () => {
    //code
});
```

```javascript
console.log("A");

// ini adalah callback
setTimeout(() => {
  console.log("B");
}, 1000);

console.log("C");
```

Output:

```
A
C
B
```

Contoh di atas menunjukkan bahwa code akan dieksekusi secara tidak berurutan. Dimana harusnya A-B-C (jika sesuai baris), namun karena diterapkan callback (bentuk asynchronous) maka instruksi yg dieksekusi menjadi A-C-B.

### Promise

State yg ada pada promise :

- pending
- rejected
- fulfilled

analogi promise:

<img src="analogi-promise.png">

Promise syntax :

```javascript
let myPromise = new Promise(function (myPromise, myReject) {
  // *producing code

  myResolve(); // when successful
  myReject(); // when error
});

//consuming code
myPromise.then(
  function (value) {
    /*code if successful */
  },
  function (error) {
    /*code if some error */
  }
);
```

contoh:

```javascript
let Promise = new Promise((resolbve, reject) => {
  setTimeout(() => {
    resolve("B");
  }, 2000);
});

console.log("A");

Promise.then((result) => {
  console.log(result);
});

console.log("C");
```

output:

```
A
C
B
```

## **Web Storage**

Browser memiliki storagenya tersendiri. Penyimpanan (storage) pada website disebut **Web Storage**.

Data user akan disimpan ke dalam storage browser menggunakan web storage seperti cookies, local storage, dan session storage.

Cookies -> data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah.

Biasanya data yang disimpan di cookies adalah access token pengguna saat login atau data pencarian saat melakukan pencarian pada situs web tertentu. Hal ini yang biasanya dilakukan oleh situs pencarian untuk melacak pencarian kita dan menampilkan iklan yang berhubungan dengan pencarian kita sebelumnnya.

Namun ada beberapa kekurangan sehingga kita dapat memanfaatkan jenis web storage yang lain seperti **Local Storage** dan **Session Storage**.
