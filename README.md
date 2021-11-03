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
console.log(greetingMorning + ", " + myName);
```

```console
Lerian
Good Morning, Lerian
```

### Updating Variable

```javascript
let name = "Lerian";
name = "Ayumi";

console.log(name);
```

```console
Ayumi
```

### Updating Variable 2

```javascript
let number = 2;

number = number + 3;

console.log(number);
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
console.log(`Hallo, nama saya ${name}.`);
console.log(`Saya dari ${region}.`);
```

```console
Hallo, nama saya Lerian.
Saya dari Indonesia.
```

## Conditional

Ini sangat penting dipelajari di dalam pemrograman. Disini kita bisa mengatur sebuah kondisi. Seperti contoh `12` adalah angka yang `lebih besar dari pada 10`.

Struktur If Statement adalah :

```javascript
if (condition) {
  // your code
}
```

```javascript
const number = 12;
if (number > 10) {
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

if (password === "codalecenter") {
  console.log("Login berhasil!");
}
```

```console
Login berhasil!
```

### Else

Jika kondisi tersebut tidak benar.

```javascript
if (condition) {
  true;
} else {
  false;
}
```

```javascript
const usia = 23;
if (usia > 25) {
  console.log("Usia saya lebih dari 25 tahun");
} else {
  console.log("Usia saya dibawah 25 tahun");
}
```

### ElseIf

Menambah sebuah kondisi.

```javascript
if (condition) {
  true;
} else if (condition) {
  false;
} else {
}
```

```javascript
const usia = 23;
if (usia > 25) {
  console.log("Usia saya lebih dari 25 tahun");
} else if (usia >= 10) {
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

if (usia >= 20 && usia < 30) {
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
switch (color) {
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
switch (color) {
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

# JavaScript Study II

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
while (condition) {
  //your code
}
```

Cara menggunakannya seperti ini untuk kasus yang kemarin.

```javascript
let number = 1;
while (number <= 100) {
  console.log(number);
  number += 1;
}
```

> Jika lupa menambahkan number += 1; maka akan terjadi `infinite loop` yaitu terus mencetak angka 1. Dan ini akan terjadi hang di browser anda.

### The for loop

```javascript
for (variable; condition; update) {
  // your code
}
```

```javascript
for (let number = 1; number <= 100; number += 1) {
  console.log(number);
}
```

### Shorthand operators

1. Increment(addition)

```javascript
number = number + 1;
number += 1;
number++;
```

2. Decrement(subsctraction)

```javascript
number = number - 1;
number -= 1;
number--;
```

### Latihan Iteration

```javascript
for (let number = 1; number <= 100; number++) {
  if (number % 3 === 0) {
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
const animals = ["cat", "dog", "sheep"];
console.log(animals);
```

```console
['cat', 'dog', 'sheep']
```

### Index number

```javascript
const animals = ["cat", "dog", "sheep"];
console.log(animals);
```

Jika kita menuliskan variabel animals dengan 3 values menggunakan array. Maka `cat` memiliki index number `0`. Nilai pertama akan selalu dimulai dengan angka `0` secara default.
Coba kita akan print `cat` dan `sheep`

```javascript
const animals = ["cat", "dog", "sheep"];

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
const animals = ["cat", "dog", "sheep"];
animals[1] = "elephant";
console.log(animals[1]);
```

```console
elephant
```

### Iterating with Arrays

Cara untuk mencetak nilai yang ada di dalam sebuah arrays dengan `for`.

```javascript
const animals = ["cat", "dog", "sheep"];

for (let i = 0; i < 3; i++) {
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
const animals = ["cat", "dog", "sheep"];

for (let i = 0; i < animals.length; i++) {
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
const item = { name: "Shuriken", price: 30 };
console.log(item);
```

```console
{name: 'Shuriken', price: '30'}
```

### Getting values

```javascript
const item = { name: "Shuriken", price: 30 };
console.log(item.name);
```

```console
Shuriken
```

### Updating values

```javascript
const item = { name: "Shuriken", price: 30 };
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
  { name: "Shuriken", price: 30 }, // index 0
  { name: "Kujang", price: 100 }, // index 1
];
```

### Getting object values within arrays

```javascript
const items = [
  { name: "Shuriken", price: 30 }, // index 0
  { name: "Kujang", price: 100 }, // index 1
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

## Undefined

Jika kita mengambil data yang tidak ada dalam `object` atau `arrays` maka hasilnya akan `undefined`

```javascript
const animals = ["cat", "dog", "sheep"];
console.log(animals[5]);
```

```console
undefined
```

### Handling undefined

Gunakan `if statement` untuk mengatasi undefined.

```javascript
if(character.age === undefined){
    ...
} else {
    ...
}
```

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

    if(character.age === undefined){
        console.log("Usia saya rahasia!");
    }else{
        console.log(`Usia saya ${character.age} tahun`);
    }
}
```

### Using Nested Object

```javascript
const character = {
  name: "Lerian Febriana",
  age: 23,
  favorite: {
    food: "Mie ayam",
    sport: "Taekwondo",
    color: "Green Black",
  },
};
```

## Latihan 1

Kita coba membuat Codale Coffee. Dimana di dalamnya terdapat nama perusahaan, waktu buka dan waktu tutup.

```javascript
const cafe = {
  name: "Codale Coffee",
  businessHours: {
    // Assign the provided object to businessHours
    opening: "10:00(AM)",
    closing: "8:00(PM)",
  },
  menus: ["Coffee", "Tea", "Milk shake"],
};

console.log(`Name: ${cafe.name}`);
console.log(`-------------------------------------`);
console.log(
  `Hours: From ${cafe.businessHours.opening} to ${cafe.businessHours.closing}`
);
console.log(`Menu Recommendations :`);

for (let i = 0; i < cafe.menus.length; i++) {
  console.log(cafe.menus[i]);
}
```

```console
Name: Codale Coffee
Hours: From 10:00(AM) to 8:00(PM)
-------------------------------------
Menu Recommendations :
Coffee
Tea
Milk shake
```

# JavaScript Study III

## Learning Function

Sebuah `function` adalah sebuah `set dari sebuah instructions`. Kita coba akan membuat `Greeting` dan `Say name`.

### Defining Function

```javascript
const FunctionName = function () {
  // block of statements
};
FunctionName();
```

Ini adalah salah satu contoh dari fungsi `function`

```javascript
const greet = function () {
  console.log("Hello!");
  console.log("Let's study functions!");
};

greet();
```

```console
Hello!
Let's study functions!
```

### Arrow functions

Jika functions menggunakan `function` tetapi jika `arrow function` diganti menjadi `() =>`

```javascript
const introduce = () => {
  // your statements
};
```

### Arguments

Nilai data yang dipassing ke `functions` disebut dengan `arguments`.

```javascript
const FunctionName = (parameter) => {
  // your code
};

FunctionName(value);
```

Parameter dapat digunakan dengan menggunakan `${parameter}`.

```javascript
const introduce = (name) => {
    console.log(`Hello, saya ${}`);
};
introduce("Lerian");
```

```console
Hello, saya Lerian
```

### Using Multiple Arguments

```javascript
const introduce = (name, age) => {
  // your code
};
```

```javascript
const add = (number1, number2) => {
  console.log(number1 + number2);
};
add(5, 7);
```

```console
12
```

### Return values

```javascript
const add = (a, b) => {
  return a + b;
};
const sum = add(1, 3);
console.log(sum);
```

```console
4
```

```javascript
const half = (number) => {
  return number / 2;
};

const result = half(130);

console.log(`Half of 130 is ${result}`);
```

### Using Return Values Types

```javascript
const check = (number) => {
  return number % 2 === 0;
};
console.log(check(6));
console.log(check(7));
```

```console
true
false
```

```javascript
const check = (number) => {
  // Check whether or not number is a multiple of 3 and return the result
  return number % 3 === 0;
};

// Call the check function in the condition of the if statement
if (check(123)) {
  console.log("Multiple of 3");
} else {
  console.log("Not a multiple of 3");
}
```

### Scope

```javascript
// Define the name constant
const name = "Ken the Ninja";

const introduce = (name) => {
  // Print "I am ____" in the console
  console.log(`I am ${name}`);
};

// Call the introduce function
introduce("Master Wooly");

// Print the value of the name constant
console.log(name);
```

```console
I am Master Wooly
Ken the Ninja
```

### getMax

```javascript
const number1 = 103;
const number2 = 72;
const number3 = 189;

// Write a function called getMax to get the maximum value
const getMax = (a, b, c) => {
  let max = a;

  if (b > max) {
    max = b;
  }
  if (c > max) {
    max = c;
  }
  return max;
};

// Print "The maximum value is __"
const max = getMax(number1, number2, number3);
console.log(`The maximum value is ${max}`);
```

```console.
The maximum value is 189
```

## Basic of Classes

### Objects and Functions

Object juga dapat menjadi sebuah functions. Caranya adalah dengan menulis syntax seperi di bawah ini, juga untuk memanggil sebuah fungsi, kita hanya menuliskan `constantName.propertyName()`. Sebagai catatan, kita membutuhkan `()` setelah propery name untuk mengindikasikan bahwa ini adalah nilai function.

```javascript
const constantName = {
  propertyName: () => {
    // your code
  },
};
```

```javascript
const user = {
  name: "Lerian Febriana",
  greet: () => {
    console.log("Hello!");
  },
};
console.log(user.name);
user.greet();
```

```console
Lerian Febriana
Hello!
```

### Apa itu Class?

Kelas bisa diibaratkan adalah sebuah blueprint sebagai contoh, kita bisa efisien untuk menambahkan user data jika blueprintnya sudah ada.

```javascript
class user {}
```

### Making Instances

Jika Class adalah sebuah blueprint, maka Instance bisa kita sebut adalah sebuah "object".

```javascript
class Animal {}
const animal = new Animal();
console.log(animal);
```

```console
Animal {}
```

### Constructors

Ini digunakan untuk memberikan sebuah initial values untuk instances baru. Untuk menambahkan `constructor` di class, maka kita bisa menuliskan `constructor() {}` di dalam `{}` brackets.

```javascript
class Animal {
  constructor() {
    console.log("Hello!");
  }
}
const animal1 = new Animal();
const animal2 = new Animal();
```

```console
Hello!
Hello!
```

### Adding Properties & Values

Di dalam constructor, kita tambahkan informasi yang berhubungan dengan instance yang telah kita buat. Untuk menambahkan properties dan values di dalam sebuah constructor, maka kita bisa menuliskan `this.property = value`

```javascript
class Animal {
  constructor() {
    this.name = "Leo";
    this.age = 3;
  }
}
const animal = new Animal();

console.log(`Name: ${animal.name}`);
console.log(`Age: ${animal.age}`);
```

```console
Name: Leo
Age: 3
```

### Changing Values for All Instances

Sebelumnya, kita telah memberikan intial values di dalam sebuah constructor. Namun masalahnya, sebuah instance yang kita buat semua nilainya akan sama `"Leo"` dan `"3"` nah sekarang, kita akan belajar bagaimana cara mengubah nilai tersebut sesuai dengan instancesnya.

```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
const animal = new Animal("Mocha", 8);

console.log(`Name: ${animal.name}`);
console.log(`Age: ${animal.age}`);
```

```console
Name: Mocha
Age: 8
```

### Methods

Functions yang ada di dalam class kita bisa sebut dengan `methods`. Methods itu seperti "actions" dalam sebuah instances.

```javascript
class ClassName {
  constructor() {
    // your code
  }
  methodName() {
    // your method
  }
}
```

```javascript
class Animal {
  constructor(name, age) {
    // your code
  }
  greet() {
    console.log("Hello!");
  }
}
const animal = new Animal("Leo", 3);
animal.greet();
```

```console
Hello!
```

### Using Values within Methods

```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  info() {
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);
  }
}
const animal = new Animal("Leo", 3);
animal.info();
```

```console
My name is Leo
I'm 3 years old
```

### Using Methods within Methods

```javascript
class Animal {
  greet() {
    console.log("Hello!");
  }
  info() {
    this.greet();
  }
}
```

```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);
  }
}
const animal = new Animal("Leo", 3);
animal.info();
```

```console
Hello!
My name is Leo
I'm 3 years old
```

## Class Inheritance

Kita telah membuat sebuah Animal class untuk mengatasi data animals. Sekarang, kita coba membuat sebuah Dog class spesifik untuk mengatasi data dogs. Ketika kamu akan membuat class yang sama dengan existing class, inheritance dapat sangat berguna!

```javascript
class Dog extends Animal {}
```

### Inherited Methods

Dog Class mewarisi semua thods yang ada pada Animal class. Karena itu, meskipun tidak ada methods yang di deklarasikan di dalam Dog class, itu bisa kita pakai dengan menggunakan `info` method karena itu didefinisikan di Animal class.

```javascript
class Animal {
  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);
  }
}
class Dog extends Animal {}

const dog = new Dog("Lee", 4);
dog.info();
```

### Adding Methods

```javascript
class Dog extends Animal {
  getHumanAge() {
    return this.age * 7;
  }
}
const dog = new Dog("Leo", 4);
const humanAge = dog.getHumanAge();
console.log(humanAge);
```

```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log("Hello");
  }

  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);
  }
}

class Dog extends Animal {
  // Add the getHumanAge method
  getHumanAge() {
    return this.age * 7;
  }
}

const dog = new Dog("Leo", 4);
dog.info();

// Call the dog instance's getHumanAge method
const humanAge = dog.getHumanAge();

// Output 「I am __ years old in human years」
console.log(`I am ${humanAge} years old in human years`);
```

```console
Hello,
My name is Leo
I'm 4 years old
I'm 28 years old in human years
```

### Methods of the Same Name

Jika ada methods yang sama, maka diutamakan class yang dipanggil atau childnya.

```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log("Hello");
  }

  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);
  }
}

class Dog extends Animal {
  // Add the info method
  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);

    const humanAge = this.getHumanAge();
    console.log(`I am ${humanAge} years old in human years`);
  }

  getHumanAge() {
    return this.age * 7;
  }
}

const dog = new Dog("Leo", 4);
dog.info();
```

```console
Hello,
My name is Leo
I'm 4 years old
I'm 28 years old in human years
```

### Overriding Constructor

Jika kita ingin menggunakan Constructor yang ada pada parent dan ingin menggunakannya pada child class, maka gunakan `super()` di dalam constructor.

```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
```

```javascript
class Dog extends Animal {
  constructor(name, age, breed) {
    super(name, age);

    this.breed = breed;
  }
}
```

```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log("Hello");
  }

  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);
  }
}

class Dog extends Animal {
  // Add the constructor
  constructor(name, age, breed) {
    super(name, age);

    this.breed = breed;
  }

  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    // Ouptut 「I am a ____」
    console.log(`I am a ${this.breed}`);

    console.log(`I'm ${this.age} years old`);
    const humanAge = this.getHumanAge();
    console.log(`I am ${humanAge} years old in human years`);
  }

  getHumanAge() {
    return this.age * 7;
  }
}

// Pass the string "Chihuahua" as an argument
const dog = new Dog("Leo", 4, "Chihuahua");
dog.info();
```

```console
Hello,
My name is Leo
I am a Chihuahua
I'm 4 years old
I'm 28 years old in human years
```

# JavaScript Study V

Disini kita akan belajar menggunakan npm packages dan membuat sebuah project dengan beberapa file.

In this lesson, you will learn how to divide JavaScript code into multiple files and combine them.
By splitting the code into multiple files, you will be able to write code that is easy to maintain and update.
You will also learn how to use a convenient feature called packages.

## Separating Files

As you add more code, it becomes difficult to manage in just one file. Because of this, multiple files are often used to manage a program and keep it organized. Here, we will split the code into three files: script.js that runs the main program, animal.js that defines the Animal class, and dog.js that defines the Dog class.

![](/img/v-separatingfiles.png)

animal.js
```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log("Hello");
  }

  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);
  }
}
```

dog.js
```javascript
class Dog extends Animal {
  // Add the constructor
  constructor(name, age, breed) {
    super(name, age);

    this.breed = breed;
  }

  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    // Ouptut 「I am a ____」
    console.log(`I am a ${this.breed}`);

    console.log(`I'm ${this.age} years old`);
    const humanAge = this.getHumanAge();
    console.log(`I am ${humanAge} years old in human years`);
  }

  getHumanAge() {
    return this.age * 7;
  }
}
```

script.js
```javascript
const dog = new Dog("Leo", 4, "Chihuahua");
dog.info();
```

```console
Error...
```

### Kenapa Error?
In the last exercise, an error occurred when you tried to split the file. This happened because values necessary to the file were removed when splitting it up. In the example below, an error message is displayed because the Animal class is not inside dog.js.

The error when splitting files can be resolved by linking each of the files and passing the necessary values. In this case, you must enable the Animal class to be used in dog.js, and the Dog class to be used in script.js. From the next slide, let's look at how to link the files.

![](/img/v-separatingfiles2.png)

Export dari animal.js
```javascript
class Animal {
.
.
.
}
export default Animal;
```

Import dari dog.js
```javascript
import Animal from "./animal";
.
.
.
```

Jadi, seperti ini kode yang benar

animal.js
```javascript
class Animal {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log("Hello");
  }

  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    console.log(`I'm ${this.age} years old`);
  }
}
export default Animal;
```

dog.js
```javascript
import Animal from "./animal";

class Dog extends Animal {
  // Add the constructor
  constructor(name, age, breed) {
    super(name, age);

    this.breed = breed;
  }

  info() {
    this.greet();
    console.log(`My name is ${this.name}`);
    // Ouptut 「I am a ____」
    console.log(`I am a ${this.breed}`);

    console.log(`I'm ${this.age} years old`);
    const humanAge = this.getHumanAge();
    console.log(`I am ${humanAge} years old in human years`);
  }

  getHumanAge() {
    return this.age * 7;
  }
}
export default Dog;
```

script.js
```javascript
import Dog from "./dog";

const dog = new Dog("Leo", 4, "Chihuahua");
dog.info();
```

```console
Hello,
My name is Leo
I am a Chihuahua
I'm 4 years old
I'm 28 years old in human years
```

### Exporting values

Although we practiced exporting classes, classes are not all that you can export. Any kind of value such as strings, integers, or even functions can be exported. When exporting, export default constantName is written as you can see below. When importing, import constantName from "./fileName" is written.

sample1.js
```javascript
const text = "Hello World!";
export default text;
```

sample2.js
```javascript
import text from "./sample1.js";
console.log(text);
```

```console
Hello World!
```

Sebagai contoh, saya akan mengganti kode ini

script.js
```javascript
import Dog from "./dog";

const dog = new Dog("Leo", 4, "Chihuahua");
dog.info();
```

dengan menambahkan file baru ```dogData.js```

dogData.js
```javascript
import Dog from "./dog";
const dog = new Dog("Leo", 4, "Chihuahua");
export default dog;
```

script.js
```javascript
import dog from "./dogData";
dog.info();
```

### Named Export

The export default statement is called a default export. With default export, when a file is imported, the export default value is automatically imported. Because of this, the value name when exporting and importing can be different.

![](/img/v-exportdefault.png)

Kita bisa mengatasi ini dengan struktur code seperti ini:

![](/img/v-namedexport2.png)

dogData.js
```javascript
import Dog from "./dog";

// Note the 2 constants dog1 and dog2 below
const dog1 = new Dog("Leo", 4, "Chihuahua");
const dog2 = new Dog("Ben", 2, "Poodle");

// Rewrite the below and export the constants dog1 and dog2
export {dog1, dog2};
```

script.js
```javascript
// Rewrite the below and import the constants dog1 and dog2
import {dog1, dog2} from "./dogData";

// Copy from the instructions and rewrite it so that the constants dog1 and dog2 are printed
console.log("---------");
dog1.info();
console.log("---------");
dog2.info();
```

console
```
// Rewrite the below and import the constants dog1 and dog2
import {dog1, dog2} from "./dogData";

// Copy from the instructions and rewrite it so that the constants dog1 and dog2 are printed
console.log("---------");
dog1.info();
console.log("---------");
dog2.info();
```

### Relative Path

./ with one dot means the current directory of the file where the relative path is written. The relative path shown below on the right, "./dogData" is for the dogData.js file in the same src directory as script.js.

![](/img/v-relativepath1.png)

In order to practice relative paths, let's try changing the directory structure we have used up until now. As shown on the left, let's look at the relative path when importing dogData.js from the data directory to script.js.

![](/img/v-relativepath2.png)

When going back one level use "../" with two dots.
When importing "dog.js" from the class directory to "dogData.js" as shown on the left, the relative path will be as shown on the right.

![](/img/v-relativepath3.png)

![](/img/v-path.png)

script.js
```javascript
// Rewrite "./dogData" (relative path)
import { dog1, dog2 } from "./data/dogData";

console.log("---------");
dog1.info();
console.log("---------");
dog2.info();
```

dogData.js
```javascript
// Rewrite "./dog" (relative path)
import Dog from "../class/dog";

const dog1 = new Dog("Leo", 4, "Chihuahua");
const dog2 = new Dog("Ben", 2, "Poodle");

export { dog1, dog2 };
```

## Packages

In the world of JavaScript, many people make their code open and publicly available as packages. With JavaScript, you can use packages by importing them to your own code. In this lesson, you will learn to use packages like the ones below.

### Importing Packages

In order to use packages in your own program, use import to import the package. When importing packages, specify the package name rather than the file name. Here, we will import a package called chalk.

```javascript
import chalk from "chalk";
```

How to use chalk package?

```javascript
import chalk from "chalk";
console.log(chalk.yellow("Hello World!"));
console.log(chalk.bgCyan("Hello World!"));
```

Example:

dog.js
```javascript
// Import the chalk package
import chalk from "chalk";

import Animal from "./animal";

class Dog extends Animal {
  constructor(name, age, breed) {
    super(name, age);
    this.breed = breed;
  }

  info() {
    const humanAge = this.getHumanAge();
    
    this.greet();
    // Rewrite the content of console.log using chalk
    console.log(chalk.yellow(`My name is ${this.name}`));
    
    // Rewrite the content of console.log using chalk
    console.log(chalk.bgCyan(`I am a ${this.breed}`));
    
    console.log(`I'm ${this.age} years old`);
     console.log(`I am ${humanAge} years old in human years`);
  }
  
  getHumanAge() {
    return this.age * 7;
  }
}

export default Dog;
```

### readline-sync

Importing the readline-sync package, you will be able to enter values in the console and use those values in your program.
Import the package as shown on the left, then write readlineSync.question(question). When the question is printed, the code pauses until a value is entered.

dogData.js
```javascript
import readlineSync from "readline-sync";
readlineSync.question("Enter your name: ");
```

```console
Enter your name:
```

dogData.js
```javascript
import readlineSync from "readline-sync";
const name = readlineSync.question("Enter your name: ");
console.log(`${name} was entered`)
```

```console
Enter your name: Ken
Ken was entered
```

### Inserting Integer on readline-sync

Although we used question in the previous slide, when you want to enter integers, questionInt can be used. All you have to do is create a Dog instance using the input value!

dogData.js
```javascript
const name = readlineSync.question("Enter your name: ");
const age = readlineSync.questionInt("Enter your age: ");
```

Coba praktekan menggunakan readline-sync

dogData.js
```javascript
// Import readline-sync
import readlineSync from "readline-sync";

import Dog from "../class/dog";

const dog1 = new Dog("Leo", 4, "Chihuahua");

// Rewrite using readlineSync.question
const name = readlineSync.question("Enter your name:");

// Rewrite using readlineSync.questionInt
const age = readlineSync.questionInt("Enter your age:");

// Rewrite using readlineSync.question
const breed =  readlineSync.question("Enter your breed:");

const dog2 = new Dog(name, age, breed);

export { dog1, dog2 };
```

# JavaScript Study VI (Handling Arrays)

Let's learn about methods for working with arrays! With these methods, you'll be able to easily handle data with JavaScript.
The methods we'll cover in this lesson are very useful and essential knowledge for practical JavaScript development.

## Push Method

```javascript
const numbers = [1,2,3];
console.log(numbers);
number.push(4);
console.log(numbers);
```

```console
[1,2,3]
[1,2,3,4]
```

## forEach Method

```javascript
const numbers = [1,2,3];
numbers.forEach((number) => {
  console.log(number)
});
```

```console
1
2
3
```

## find Method

```javascript
const numbers = [1,3,5,7];
const foundNumber = numbers.find((number) => {
  return number > 3;
});
console.log(foundNumber);
```

```console
5
```

```javascript
const characters = [
  {id:1, name:"Uzumaki Boruto"},
  {id:2, name:"Uchiha Sarada"},
];
const foundCharacter = characters.find((character) => {
  return character.id === 1;
});
console.log(foundCharacter.name);
```

```console
Uzumaki Boruto
```

## filter Method

```javascript
const numbers = [1,3,5,7];
const filteredNumbers = numbers.filter((number) => {
  return number > 3;
});
console.log(filteredNumbers);
```

```console
[5,7]
```

```javascript
const characters = [
  {name:"Uzumaki Boruto",age:16},
  {name:"Uzumaki Himawari",age:5},
  {name:"Tsunade Senju",age:80}
];
const filteredCharacters = characters.filter((character) => {
  return character.age > 10;
});
console.log(filteredharacters[0].name);
```

```console
Uzumaki Boruto
```

## map Method

```javascript
const numbers = [1,2,3];
const doubledNumbers = numbers.map((number) => {
  return number * 2;
});
console.log(doubledNumbers);
```

```console
[2,4,6]
```

```javascript
const characters = [
  {firstName:"Uzumaki", lastName:"Boruto"},
  {firstName:"Uchiha", lastName:"Sarada"},
  {firstName:"Senju", lastName:"Tsunade"}
];
const fullNames = characters.map((name) => {
  return name.firstName + " " + name.lastName;
});
console.log(fullNames[0]);
```

```console
Uzumaki Boruto
```

# JavaScript VII (callback Function)

In this lesson, you will learn about callback functions.
They may seem hard until you get used to them at first, but relax and take your time.

"Callback functions frequently appear when using JavaScript. They are useful when creating web applications." - Master Wooly
"I would expect so. Functions that are passed to other functions as arguments are called callback functions." - Master Wooly

![](/img/vii-typesArguments.png)

![](/img/vii-passedArgument.png)

![](/img/vii-calling.png)

![](/img/vii-flow.png)

```javascript
const printKen = () => {
  console.log("Ken the Ninja");
};

// Add a parameter named callback to call
const call = (callback) => {
  console.log("Calling the callback function.");
  // Call the function callback
  callback();
};

// Pass printKen as the argument and run call
call(printKen);
```

```console
Calling the callback function.
Ken the Ninja
```

## Declaring the Function with Argument

![](/img/vii-declaringWithArgument.png)


```javascript
const call = (callback) => {
  console.log("Calling the callback function.");
  callback();
};

call(() => {
  console.log("Ken the Ninja");
});
```

```console
Calling the callback function.
Ken the Ninja
```

```javascript
const printKen = () => {
  console.log("Ken the Ninja");
};

const call = (callback) => {
  console.log("Calling the callback function.");
  callback();
};

call(printKen);

// Declare the function in the argument and pass it
call(() => {
  console.log("Master Wooly");
});
```

```console
Calling the callback function.
Ken the Ninja
Calling the callback function.
Master Wooly
```

## Arguments of Callback Function

![](/img/vii-normalFunctions.png)

![](/img/vii-callbackFunction.png)

### Normal Function

```javascript
const introduce = (name) => {
  console.log(name);
};
introduce("Ken the Ninja");
```

```console
Ken the Ninja
```

```javascript
const introduce = (name,age) => {
  console.log(`${name} is ${age} years old.`);
};
introduce("Ken the Ninja",14);
```

```console
Ken the Ninja is 14 years old.
```

### Callback Function

```javascript
const introduce = (callback) => {
  callback("Ken the Ninja");
};
introduce((name) => {
  console.log(name);
});
```

```console
Ken the Ninja
```

```javascript
const introduce = (callback) => {
  callback("Ken the Ninja",14);
};
introduce((name,age) => {
  console.log(`${name} is ${age} years old.`);
});
```

```console
Ken the Ninja is 14 years old.
```
