# Python - Variable Annotations

This repository provides examples and explanations of using type annotations in Python 3 for specifying variable types, function signatures, and the concept of duck typing. It also demonstrates how to validate your code using **mypy**, a popular static type checker for Python.

## Table of Contents

- [Python - Variable Annotations](#python---variable-annotations)
  - [Table of Contents](#table-of-contents)
  - [Introduction to Type Annotations](#introduction-to-type-annotations)
  - [Variable Type Annotations](#variable-type-annotations)
  - [Function Signature Annotations](#function-signature-annotations)
  - [Understanding Duck Typing](#understanding-duck-typing)
  - [Validating Code with Mypy](#validating-code-with-mypy)
    - [**Authors**](#authors)

## Introduction to Type Annotations

Type annotations are a way to explicitly specify the expected types of variables and function return values in Python. While Python is dynamically typed, meaning you don't have to declare types explicitly, type annotations can provide better code clarity and help catch errors early.

## Variable Type Annotations

In this section, you will find examples of how to use type annotations to specify the types of variables:

```python
name: str = "Alice"
age: int = 30
is_student: bool = True
```

## Function Signature Annotations

Type annotations can also be applied to function signatures to indicate the expected types of parameters and return values:

```python
def greet(name: str) -> str:
    return f"Hello, {name}!"
```

## Understanding Duck Typing

Duck typing is a concept in programming where the type or the class of an object is less important than the methods and properties it exposes. If an object walks like a duck and quacks like a duck, it's considered a duck.

For example:

```python
class Dog:
    def speak(self):
        return "Woof!"

class Cat:
    def speak(self):
        return "Meow!"

def pet_speak(pet):
    print(pet.speak())

dog = Dog()
cat = Cat()

pet_speak(dog)  # Output: "Woof!"
pet_speak(cat)  # Output: "Meow!"
```

## Validating Code with Mypy

[Mypy](http://mypy-lang.org/) is a static type checker for Python that can be used to analyze your code and catch type-related errors before runtime. To use mypy, first, install it:

```bash
pip install mypy
```

Then, run mypy to check your code:

```bash
mypy your_code.py
```

Make sure to replace `your_code.py` with the actual filename.

---


### **Authors**
--- 

![GitHub Contributors Image](https://contrib.rocks/image?repo=RM92023/holbertonschool-low_level_programming)
Robinson Muñetón Jaramillo - <a href="https://github.com/RM92023" target="_blank"> @RM92023</a> ![Your Repository's Stats](https://github-readme-stats.vercel.app/api?username=RM92023&show_icons=true)