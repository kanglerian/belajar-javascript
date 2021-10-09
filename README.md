# Intro

Javascript adalah sebuah bahasa pemrograman yang digunakan dalam pengembangan website agar lebih dinamis dan interaktif. 
Javascript merupakan bahasa pemrograman jenis `interpreter` artinya kita tidak memerlukan `compiler` untuk menjalankannya.

Sumber : dicoding.com

# Kenapa harus Javascript?

1. JavaScript menjadi salah satu bahasa pemrograman yang populer dan banyak digunakan. Sumber: Stack overflow
Seperti contohnya: Facebook, LinkedIn, Trello, bahkan Google memakai JavaScript.
2. JavaScript bisa digunakan untuk logika data, bukan hanya digunakan untuk Front End.
3. General Purpose. Artinya, tidak hanya digunakan untuk client side saja (browser), kita bisa menggunakannya di luar browser untuk keperluan Back End (Server), program desktop, mobile, IoT, Game dan lainnya karena semenjak adanya Node.js.
4. Banyak perusahaan yang menggunakan bahasa pemrograman JavaScript.

# Tools yang dipakai

1. Web Browser (Google Chrome, Firefox, Safari dll)
2. Teks Editor (Visual Studio Code, Atom, Sublime Text dll)


# JavaScript Study I

## String & Integers

String & Integers adalah sebuah tipe data.
1. String adalah teks. Teks tidak bisa kita kalkulasikan, hanya bisa kita kombinasikan.
2. Integers adalah angka, yang mana setiap data integers bisa kita kalkulasikan.

### console.log()

Untuk menjalankan code javascript, pakai perintah `console.log("Hello World");`

```console
Hello World
```

1. Kita bisa memakai `'` ataupun `"`
2. Tida bisa tanpa kutip di point no 1.
3. Harus memakai `;` semicolon.
4. Untuk komentar bisa dibubuhi di awal code `//`

### Calculation

- `*` kali
- `/` bagi
- `-` kurang
- `%` remainder
- `+` tambah

```javascript
console.log(3);
console.log(2 + 3);
```

```console
3
5
```

### Combining String

```javascript
console.log("Hello " + "Lerian");
```

```console
Hello Lerian
```

Jika memakai kutip seperti `console.log("5 + 2");` maka yang akan muncul berbentuk string `5 + 2`

## Variable

Variabel adalah sebuah nama yang mewakili sebuah nilai. Variabel bisa diisi dengan string(teks), number(angka), objek, array dan lain-lain.

Kenapa harus pakai Variabel?

1. Mudah untuk menyebutkan sebuah nilai.
2. Data dapat digunakan di berbagai tempat.
3. Mudah untuk mengubah data.

```javascript
let myName = "Lerian";
let greetingMorning = "Good Morning";

console.log(myName);
console.log(greetingMorning + ", " + myName)

```
```console
Lerian
Good Morning, Lerian
```

### Updating Variable

```javascript
let name = "Lerian";
name = "Ayumi";

console.log(name)
```

```console
Ayumi
```

### Updating Variable 2

```javascript
let number = 2

number = number + 3

console.log(number)
```

```console
5
```

### Constant

Berbeda dengan `let` maka `const` datanya tidak bisa di ubah.

```javascript
const name = "Lerian";
name = "Ayumi";
console.log(name);
```

```console
Uncaught TypeError: Assignment to constant variable.
```

```javascript
const language = "Indonesia";
console.log("Saya dapat berbicara bahasa " + language);
```

```console
Saya dapat berbicara bahasa Indonesia
```

### Template Literals

Dengan `Template Literals` kita bisa menyisipkan variabel di dalam sebuah string. Dengan memakai `back quotation`

```javascript
const name = "Lerian";
const region = "Indonesia";
console.log(`Hallo, nama saya ${name}.`)
console.log(`Saya dari ${region}.`)
```

```console
Hallo, nama saya Lerian.
Saya dari Indonesia.
```

## Conditional

Ini sangat penting dipelajari di dalam pemrograman. Disini kita bisa mengatur sebuah kondisi. Seperti contoh `12` adalah angka yang `lebih besar dari pada 10`.

Struktur If Statement adalah :

```javascript
if(condition){
    // your code
}
```

```javascript
const number = 12;
if(number > 10){
    console.log("Benar!, 12 lebih besar dari pada 10");
}
```

### Printing Conditional Expressions

macam-macam `Comparison Operator`
1. `<` lebih kecil dari
2. `>` lebih besar dari
3. `<=` lebih kecil atau sama dengan dari
4. `>=` lebih besar atau sama dengan dari

```javascript
const number = 12;
console.log(number > 12);
console.log(number < 30);
console.log(number <= 12);
console.log(number >= 12);
```

```console
false
true
true
true
```

### Comparison Operator 2
Digunakan untuk membandingkan nilai dan tipe data `string` atau `integers`.

macam-macam `Comparison Operator`
1. `a === b` nilai dan tipe data sama.
2. `a !== b` nilai dan tipe data tidak sama.

Contoh:

```javascript
let password = "codalecenter";

if(password === "codalecenter"){
    console.log("Login berhasil!");
}
```

```console
Login berhasil!
```

### Else
Jika kondisi tersebut tidak benar.

```javascript
if(condition){
    true
} else {
    false
}
```

```javascript
const usia = 23;
if(usia > 25){
    console.log("Usia saya lebih dari 25 tahun");
} else {
    console.log("Usia saya dibawah 25 tahun");
}
```

### ElseIf
Menambah sebuah kondisi.

```javascript
if(condition){
    true
} else if(condition) {
    false
} else {

}
```

```javascript
const usia = 23;
if(usia > 25){
    console.log("Usia saya lebih dari 25 tahun");
} else if( usia >= 10 ) {
    console.log("Usia saya dibawah 25 tahun tetapi lebih dari 10 tahun");
} else {
    console.log("Usia saya dibawah 25 tahun");
}
```

### Multiple Condition

Menggunakan `&&` jika kedua jawaban harus benar.

1. `true` && `true` adalah `true`
2. `true` && `false` adalah `false`
3. `false` && `true` adalah `false`
4. `false` && `false` adalah `false`

Menggunakan `||` jika kedua jawaban salah satunya harus benar.

1. `true` && `true` adalah `true`
2. `true` && `false` adalah `true`
3. `false` && `true` adalah `true`
4. `false` && `false` adalah `false`


```javascript
const usia = 24;

if(usia >= 20 && usia < 30){
    console.log("usia saya sekitar 20 tahunan");
}
```

### Switch
Seperti lampu lalu lintas. Untuk mengatur flow.

```javascript
switch(condition value){
    // your code
}
```

```javascript
const color = "red";
switch(color){
    case "red":
        console.log("Stop");
        break;
    case "yellow":
        console.log("Slow Down!");
        break;
    case "green":
        console.log("GO!!");
        break;
}
```

### Switch Statement Default

```javascript
const color = "red";
switch(color){
    case "red":
        console.log("Stop");
        break;
    case "yellow":
        console.log("Slow Down!");
        break;
    case "green":
        console.log("GO!!");
        break;
    default:
        console.log("Warna tidak ada!");
        break;
}
```

## Iteration
Digunakan untuk menulis nomor secara berurutan.

```javascript
let number = 1;
console.log(number);

number += 1;
console.log(number);

number += 1;
console.log(number);

number += 1;
console.log(number);

number += 1;
console.log(number);

number += 1;
console.log(number);

number += 1;
console.log(number);
```

```console
1
2
3
4
5
6
```

### The while loop

Salah satu cara untuk mempermudah iteration adalah dengan menggunakan `while loops`

```javascript
while(condition){
    //your code
}
```

Cara menggunakannya seperti ini untuk kasus yang kemarin.

```javascript
let number = 1;
while(number <= 100){
    console.log(number);
    number += 1;
}
```

> Jika lupa menambahkan number += 1; maka akan terjadi `infinite loop` yaitu terus mencetak angka 1. Dan ini akan terjadi hang di browser anda.

### The for loop

```javascript
for(variable;condition;update){
    // your code
}
```

```javascript
for(let number = 1; number<=100; number += 1){
    console.log(number);
}
```

### Shorthand operators

1. Increment(addition)

```javascript
number = number + 1;
number += 1;
number++
```

2. Decrement(subsctraction)

```javascript
number = number - 1;
number -= 1;
number--
```

### Latihan Iteration

```javascript
for(let number = 1; number <= 100; number++){
    if(number % 3 === 0){
        console.log("Kelipatan 3");
    } else {
        console.log(number);
    }
}
```

```console
1
2
Kelipatan 3
4
5
Kelipatan 3
```

## Arrays

Arrays bisa kita akan adalah `multiples value`. Contohnya, jika kamu memiliki `fruits` maka di dalamnya ada beberapa macam buah. Disini kita tidak perlu membuat variabel satu per satu untuk setiap buah.

```javascript
const animals = ["cat","dog","sheep"];
console.log(animals);
```

```console
['cat', 'dog', 'sheep']
```

### Index number

```javascript
const animals = ["cat","dog","sheep"];
console.log(animals);
```

Jika kita menuliskan variabel animals dengan 3 values menggunakan array. Maka `cat` memiliki index number `0`. Nilai pertama akan selalu dimulai dengan angka `0` secara default.
Coba kita akan print `cat` dan `sheep`

```javascript
const animals = ["cat","dog","sheep"];

console.log(animals[0]);
console.log(animals[2]);
```

```console
cat
sheep
```

### Updating Arrays

Kita tinggal menuliskan array dan index ke berapa nilai tersebut mau di ubah.

```javascript
const animals = ["cat","dog","sheep"];
animals[1] = "elephant";
console.log(animals[1]);
```

```console
elephant
```

### Iterating with Arrays
Cara untuk mencetak nilai yang ada di dalam sebuah arrays dengan `for`.

```javascript
const animals = ["cat","dog","sheep"];

for(let i = 0; i < 3; i++){
    console.log(animals[i]);
}
```
```console
cat
dog
sheep
```

### Length property

Supaya angka `3` ini tidak kita tulis manual, sesuai dengan berapa banyak nilai yang ada di dalam sebuah arrays maka gunakan fungsi `variable.length`

```javascript
const animals = ["cat","dog","sheep"];

for(let i = 0; i < animals.length; i++){
    console.log(animals[i]);
}
```
```console
cat
dog
sheep
```

## Object
Objek mirip dengan arrays digunakan untuk menyatukan atau mengatur values. Jika looping arrays menggunakan index number. Tetapi object bisa kita beri nama yang disebut dengan properties.

```console
["value1", "value2", "value3"]

{property1: value1, property2: value2}
```

```javascript
const item = {name: "Shuriken", price: 30};
console.log(item);
```

```console
{name: 'Shuriken', price: '30'}
```

### Getting values

```javascript
const item = {name: "Shuriken", price: 30};
console.log(item.name);
```

```console
Shuriken
```

### Updating values

```javascript
const item = {name: "Shuriken", price: 30};
item.name = "Kujang";
console.log(item.name);
```

```console
Kujang
```


### Object as Arrays Element

```javascript
[{property1: value...},{property2: value...}]
```

```javascript
const items = [
    {name: "Shuriken", price: 30}, // index 0
    {name: "Kujang", price: 100} // index 1
];
```

### Getting object values within arrays

```javascript
const items = [
    {name: "Shuriken", price: 30}, // index 0
    {name: "Kujang", price: 100} // index 1
];
console.log(items[1].name);
```

```console
Kujang
```

### Arrays & Iteration

```javascript
const characters = [
    {name: "Ken the Ninja", age: 14},
    {name: "Master Wooly", age: 100},
    {name: "Ben the Ninja Ninja", age: Ben the Ninja Ninja}
];

for(let i = 0; i < characters.length; i++){
    console.log("-----------------------");

    const character = characters[i];

    console.log(`Nama saya adalah ${character.name}`);
    console.log(`Usia saya ${character.age} tahun`);
}
```

```console
-----------------------
Nama saya adalah Ken the Ninja
Usia saya 14 tahun
-----------------------
Nama saya adalah Master Wooly
Usia saya 100 tahun
-----------------------
Nama saya adalah Ben the Ninja Ninja
Usia saya 5 tahun
```