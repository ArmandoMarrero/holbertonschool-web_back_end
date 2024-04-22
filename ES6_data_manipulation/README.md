# ES6 Data Manipulation

In modern JavaScript, ES6 (ECMAScript 2015) introduced powerful tools for data manipulation in the form of array methods and new data structures. This README provides an overview of some key concepts and techniques for working with data in JavaScript.

## Array Manipulation with `map`, `filter`, and `reduce`

### `map`

The `map` method is used to transform each element of an array and create a new array based on the provided transformation function. Here's an example of how to use `map`:

```javascript
const originalArray = [1, 2, 3, 4, 5];
const transformedArray = originalArray.map((element) => element * 2);
console.log(transformedArray); // [2, 4, 6, 8, 10]
```

### `filter`

The `filter` method allows you to create a new array containing only the elements that satisfy a given condition. Here's an example of how to use `filter`:

```javascript
const numbers = [10, 15, 20, 25, 30];
const evenNumbers = numbers.filter((number) => number % 2 === 0);
console.log(evenNumbers); // [10, 20, 30]
```

### `reduce`

The `reduce` method is used to accumulate values from an array into a single result. It takes a callback function and an initial value. Here's an example of how to use `reduce` to calculate the sum of an array:

```javascript
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
console.log(sum); // 15
```

## Typed Arrays

Typed arrays provide a way to work with binary data in a structured manner. They are especially useful when dealing with low-level data such as binary files or network protocols. JavaScript offers various typed array types, including `Int8Array`, `Uint8Array`, `Int16Array`, and more.

```javascript
const buffer = new ArrayBuffer(4); // Create a buffer with 4 bytes
const int32View = new Int32Array(buffer); // Create a view on the buffer as 32-bit integers
int32View[0] = 42; // Set the value at index 0
console.log(int32View[0]); // 42
```

## Set, Map, and WeakMap Data Structures

JavaScript also introduced new data structures like `Set`, `Map`, and `WeakMap` in ES6.

### `Set`

A `Set` is a collection of unique values, which means it cannot contain duplicate elements. Here's how to use a `Set`:

```javascript
const mySet = new Set();
mySet.add(1);
mySet.add(2);
mySet.add(1); // Duplicate value, won't be added
console.log(mySet); // Set { 1, 2 }
```

### `Map`

A `Map` is a data structure that allows you to store key-value pairs and retrieve values by their keys. Here's an example:

```javascript
const myMap = new Map();
myMap.set('name', 'John');
myMap.set('age', 30);
console.log(myMap.get('name')); // John
```

### `WeakMap`

A `WeakMap` is similar to a `Map`, but it allows the garbage collector to collect its keys if they are not referenced elsewhere. This can be useful in some scenarios for managing memory efficiently.



### **Authors**
--- 

![GitHub Contributors Image](https://contrib.rocks/image?repo=RM92023/holbertonschool-low_level_programming)
Robinson Muñetón Jaramillo - <a href="https://github.com/RM92023" target="_blank"> @RM92023</a> ![Your Repository's Stats](https://github-readme-stats.vercel.app/api?username=RM92023&show_icons=true)