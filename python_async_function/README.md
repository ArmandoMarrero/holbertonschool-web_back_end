# Asynchronous Programming in Python

This README.md file provides a brief overview of asynchronous programming in Python using the `async` and `await` syntax, along with the `asyncio` library. It covers topics such as executing asynchronous programs, running concurrent coroutines, creating asyncio tasks, and utilizing the `random` module.

## Table of Contents
- [Asynchronous Programming in Python](#asynchronous-programming-in-python)
  - [Table of Contents](#table-of-contents)
  - [Introduction to Asynchronous Programming](#introduction-to-asynchronous-programming)
  - [Executing an Async Program with asyncio](#executing-an-async-program-with-asyncio)
  - [Running Concurrent Coroutines](#running-concurrent-coroutines)
  - [Creating Asyncio Tasks](#creating-asyncio-tasks)
  - [Using the Random Module](#using-the-random-module)
    - [**Authors**](#authors)

## Introduction to Asynchronous Programming

Asynchronous programming allows you to write code that can perform multiple tasks concurrently without blocking the execution of other code. This is particularly useful for I/O-bound operations, such as network requests and file operations, where waiting for a response can be inefficient.

## Executing an Async Program with asyncio

Python's `asyncio` library provides tools for writing asynchronous code using the `async` and `await` syntax. To execute an asynchronous program, follow these steps:

1. Import the `asyncio` module.
2. Define an asynchronous function using the `async def` syntax.
3. Use the `await` keyword to pause execution until an asynchronous operation completes.

Example:
```python
import asyncio

async def main():
    print("Hello")
    await asyncio.sleep(1)
    print("World")

asyncio.run(main())
```

## Running Concurrent Coroutines

In asynchronous programming, you can run multiple coroutines concurrently to maximize efficiency. The `asyncio.gather()` function allows you to run multiple coroutines concurrently and await their completion.

Example:
```python
async def foo():
    # ...

async def bar():
    # ...

async def main():
    await asyncio.gather(foo(), bar())

asyncio.run(main())
```

## Creating Asyncio Tasks

Asyncio tasks are units of work that can be managed by the `asyncio` event loop. They allow you to concurrently execute multiple asynchronous functions.

Example:
```python
async def task1():
    # ...

async def task2():
    # ...

async def main():
    t1 = asyncio.create_task(task1())
    t2 = asyncio.create_task(task2())
    await t1
    await t2

asyncio.run(main())
```

## Using the Random Module

The `random` module can be used in asynchronous programs to generate random numbers asynchronously. Remember to use `await` when invoking asynchronous functions.

Example:
```python
import asyncio
import random

async def generate_random_number():
    await asyncio.sleep(1)
    return random.randint(1, 10)

async def main():
    num = await generate_random_number()
    print(f"Random number: {num}")

asyncio.run(main())
```

Feel free to explore further and integrate these concepts into your own projects!

Remember that this README is just a starting point, and you should refer to the official Python documentation and other resources for more in-depth information on asynchronous programming and the `asyncio` library.



### **Authors**
--- 

![GitHub Contributors Image](https://contrib.rocks/image?repo=RM92023/holbertonschool-low_level_programming)
Robinson Muñetón Jaramillo - <a href="https://github.com/RM92023" target="_blank"> @RM92023</a> ![Your Repository's Stats](https://github-readme-stats.vercel.app/api?username=RM92023&show_icons=true)