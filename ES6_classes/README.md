# ES6 Classes

This README will provide you with a concise overview of ES6 classes, a fundamental feature of modern JavaScript. It covers how to define classes, add methods, work with static methods, extend classes, and introduces you to metaprogramming using symbols.

## Table of Contents
- [ES6 Classes](#es6-classes)
  - [Table of Contents](#table-of-contents)
  - [1. Introduction to ES6 Classes](#1-introduction-to-es6-classes)
  - [2. Defining a Class](#2-defining-a-class)
  - [3. Adding Methods to a Class](#3-adding-methods-to-a-class)
  - [4. Static Methods](#4-static-methods)
  - [5. Extending Classes](#5-extending-classes)
  - [6. Metaprogramming and Symbols](#6-metaprogramming-and-symbols)
    - [**Authors**](#authors)

## 1. Introduction to ES6 Classes

ES6 (ECMAScript 2015) introduced a more structured way to define and work with objects in JavaScript through classes. Classes provide a blueprint for creating objects with shared properties and methods, making your code more organized and maintainable.

## 2. Defining a Class

To define a class in ES6, use the `class` keyword followed by the class name. Here's a basic example:

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
}
```

In this example, we've defined a `Animal` class with a constructor that sets the `name` property when a new object is created.

## 3. Adding Methods to a Class

You can add methods to a class by defining functions within the class. For example:

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}
```

The `speak` method can be called on instances of the `Animal` class.

## 4. Static Methods

Static methods are methods that belong to the class itself, rather than instances of the class. They are defined using the `static` keyword. Here's an example:

```javascript
class MathUtils {
  static add(x, y) {
    return x + y;
  }
}
```

You can call the `add` method directly on the `MathUtils` class without creating an instance:

```javascript
const result = MathUtils.add(5, 3);
console.log(result); // Output: 8
```

## 5. Extending Classes

Inheritance allows you to create a new class based on an existing one. You can extend a class using the `extends` keyword. Here's an example:

```javascript
class Dog extends Animal {
  constructor(name, breed) {
    super(name); // Call the parent class constructor
    this.breed = breed;
  }

  bark() {
    console.log(`${this.name} (${this.breed}) barks loudly.`);
  }
}
```

In this example, `Dog` is a subclass of `Animal` and inherits its `name` property. The `super` keyword is used to call the parent class constructor.

## 6. Metaprogramming and Symbols

Metaprogramming is the ability of a program to modify its own structure and behavior. Symbols are a unique data type in JavaScript that can be used for metaprogramming. You can create symbols and use them as property keys in objects to add or modify properties dynamically.

```javascript
const mySymbol = Symbol('description');

const obj = {
  [mySymbol]: 'This is a symbol property',
};

console.log(obj[mySymbol]); // Output: This is a symbol property
```

Symbols are often used in advanced JavaScript programming to create private properties or to customize object behavior.


### **Authors**
--- 

![GitHub Contributors Image](https://contrib.rocks/image?repo=RM92023/holbertonschool-low_level_programming)
Robinson Muñetón Jaramillo - <a href="https://github.com/RM92023" target="_blank"> @RM92023</a> ![Your Repository's Stats](https://github-readme-stats.vercel.app/api?username=RM92023&show_icons=true)