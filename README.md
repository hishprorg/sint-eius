<p align="center">
  <a href="https://www.npmjs.com/package/@hishprorg/sint-eius" rel="noopener">
 <img width=100px height=100px src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" alt="SL Code LORDS"></a>
</p>

<h2 align="center">JS Extra Types</h2>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hishprorg/sint-eius.svg)](https://github.com/hishprorg/sint-eius/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hishprorg/sint-eius.svg)](https://github.com/hishprorg/sint-eius/pulls)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

<p align="center"> Extra Types For JavaScript
    <br> 
</p>

## 📝 Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Usage](#usage)
- [Contributing](../CONTRIBUTING.md)
- [Authors](#authors)

## 🧐 About <a name = "about"></a>

Extra Types For JavaScript

## 🏁 Getting Started <a name = "getting_started"></a>

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes

### Installing


```sh
yarn add @hishprorg/sint-eius
```

or

```sh
npm i @hishprorg/sint-eius
```

## 🎈 Usage <a name="usage"></a>

```ts
const extra_types = require('@hishprorg/sint-eius')
extra_types.init()

```
## Strings
```ts
// ----------------String----------------
var data = ''

//bind strings
data = '{} I {} Ravindu {}'.bind('Hello','Am','Manoj')
console.log(data) // => Hello I Am Ravindu Manoj

//split strings without error
data = 'Hello I Am Ravindu Manoj'.cut('Am')
console.log(data) // => [ 'Hello I ', ' Ravindu Manoj' ]

//split strings without error
data = 'Hello I Am Ravindu Manoj'.cut('Sl')
console.log(data) // => [ 'Hello I Am Ravindu Manoj' ]

//includes function without error
data = 'Hello I Am Ravindu Manoj'.have('Ravindu')
console.log(data) // => true

//reverse text
data = 'Hello I Am Ravindu Manoj'.reverse()
console.log(data) // => jonaM udnivaR mA I olleH

//replace again and again one line
data = 'Hello I Am Ravindu Manoj'.replacer('Hello%hi',' Ravindu % ')
console.log(data) // => hi I Am Manoj

//get strings between 2 place
data = '{Hello} {I Am} {Ravindu} {Manoj}'.getBetween('{','}')
console.log(data) // => [ 'Hello', 'I Am', 'Ravindu', 'Manoj' ]

//encrypt strings with crypto
data = 'Hello I Am Ravindu Manoj'.encrypt('Ravindu1234')
console.log(data) // => U2FsdGVkX18IWCpLQUxEeNU1O/vZqBAZMebwpLEGk8J9xWGzAKJ1oif1QkOfe3U/

//decrypt strings with crypto
data = 'U2FsdGVkX18IWCpLQUxEeNU1O/vZqBAZMebwpLEGk8J9xWGzAKJ1oif1QkOfe3U/'.decrypt('Ravindu1234')
console.log(data) // => Hello I Am Ravindu Manoj

//to base64 encode
data = 'Hello I Am Ravindu Manoj'.base(true)
console.log(data) // => SGVsbG8gSSBBbSBSYXZpbmR1IE1hbm9q

//base64 decode
data = 'SGVsbG8gSSBBbSBSYXZpbmR1IE1hbm9q'.base()
console.log(data) // => Hello I Am Ravindu Manoj

//encodeURIComponent function as type function
data = 'Hello @ I Am Ravindu Manoj'.tourl()
console.log(data) // => Hello%20%40%20I%20Am%20Ravindu%20Manoj
// ---------------------------------------
```

## Array
```ts
// ----------------Array----------------

// get random element
data = ['banana','mango','apple','orange'].sample()
console.log(data) // => mango

// includes function without error
data = ['banana','mango','apple','orange'].have('apple')
console.log(data) // => true

// get difference item in 2 array
data = ['banana','mango','apple','orange'].difference(['apple','mango','rambutan','pine-apple'])
console.log(data) // => [ 'banana', 'orange', 'rambutan', 'pine-apple' ]

// get difference item in 1st array
data = ['banana','mango','apple','orange'].diff(['apple','mango','rambutan','pine-apple'])
console.log(data) // => [ 'banana', 'orange' ]

// get common item in 2 array
data = ['banana','mango','apple','orange'].common(['apple','mango','rambutan','pine-apple'])
console.log(data) // => [ 'mango', 'apple' ]

// get last item in array
data = ['banana','mango','apple','orange'].last()
console.log(data) // => orange

// remove item with function check
data = ['banana','mango','apple','orange'].rm((item)=> item.have('ng'))
console.log(data) // => [ 'banana', 'apple' ]

// remove item in argument
data = ['banana','mango','apple','orange'].remove('mango','apple')
console.log(data) // => [ 'banana', 'orange' ]

// remove undefined null or empty item in array
data = [null,'banana',undefined,'mango','','apple','orange'].fix()
console.log(data) // => [ 'banana', 'mango', 'apple', 'orange' ]

// remove duplicate item in array
data = ['banana','mango','apple','mango','apple'].fixDuplicate()
console.log(data) // => [ 'banana', 'mango', 'apple' ]

// encrypt array with crypto
data = ['banana','mango','apple','orange'].encrypt('Ravindu1234')
console.log(data) // => U2FsdGVkX18bN6nFeZZx0UrOaeP0smRjAHkY3g2st7zWRT6Fdz/tgZRKc6eh23/1VtoIommjbygCbNdDqiYTzA==

// ---------------------------------------
```

## Object
```ts
// ----------------Object-----------------

// encrypt Object with crypto
data = {name:'Ravindu',country : 'sri lanka',age : 21}.encrypt('Ravindu1234')
console.log(data) // => U2FsdGVkX18u/7Y6j8tX/ZA2tDTQzzce0Zs87Saw5gUBQAOhIfyATR2nLQH0oflaxAVuTGYLXjVXLkbuC9VhFsJj8h6RLmWvGUlY2fVTx30=

// get keys length
data = {name:'Ravindu',country : 'sri lanka',age : 21}.length()
console.log(data) // => 3

// get key from value
data = {name:'Ravindu',country : 'sri lanka',age : 21}.getKeyByValue('sri lanka')
console.log(data) // => country

// locate value with argument location
data = {name:{full : { cap : {sir : 'JAYASUNDARA'}}}}.go('name','full','cap','sir')
console.log(data) // => JAYASUNDARA
// ---------------------------------------
```

## Number
```ts
// ----------------Number-----------------

// includes function without error
data = Number(123456789).have('2')
console.log(data) // => true

// reverse number
data = Number(123456789).reverse()
console.log(data) // => 987654321

// split numbers
data = Number(123456789).cut('2')
console.log(data) // => [ 1, 3456789 ]

// encrypt numbers with crypto
data = Number(123456789).encrypt('Ravindu1234')
console.log(data) // => U2FsdGVkX18Ly1ll+3fZuaOMtXjy2oVj/Nds09b1f1Y=
// ---------------------------------------
```


## ✍️ Authors <a name = "authors"></a>

- [@ravindu01manoj](https://github.com/ravindu01manoj) Project Author

See also the list of [contributors](https://github.com/SL-CODE-LORDS/Esana-News/contributors) who participated in this project.