# Python Annotations and Duck Typing

This README provides a comprehensive guide to basic type annotations and complex type usage in Python. It covers topics such as basic operations with annotations, working with complex data types, and understanding duck typing.

## Table of Contents

- [Python Annotations and Duck Typing](#python-annotations-and-duck-typing)
  - [Table of Contents](#table-of-contents)
  - [Basic Annotations - `add`](#basic-annotations---add)
  - [Basic Annotations - `concat`](#basic-annotations---concat)
  - [Basic Annotations - `floor`](#basic-annotations---floor)
  - [Basic Annotations - `to_string`](#basic-annotations---to_string)
  - [Defining Variables](#defining-variables)
  - [Complex Types - List of Floats](#complex-types---list-of-floats)
  - [Complex Types - Mixed List](#complex-types---mixed-list)
  - [Complex Types - String and Int/Float to Tuple](#complex-types---string-and-intfloat-to-tuple)
  - [Complex Types - Functions](#complex-types---functions)
  - [Let's Duck Type an Iterable Object](#lets-duck-type-an-iterable-object)
    - [**Authors**](#authors)

## Basic Annotations - `add`

Illustrating how to use annotations for addition:

```python
def add(x: int, y: int) -> int:
    return x + y
```

## Basic Annotations - `concat`

Demonstrating annotations for string concatenation:

```python
def concat(a: str, b: str) -> str:
    return a + b
```

## Basic Annotations - `floor`

Annotating a function for floor division:

```python
def floor_divide(a: int, b: int) -> int:
    return a // b
```

## Basic Annotations - `to_string`

Converting a value to a string with annotations:

```python
def to_string(value: int) -> str:
    return str(value)
```

## Defining Variables

Defining variables with type annotations:

```python
name: str = "Alice"
age: int = 30
is_student: bool = True
```

## Complex Types - List of Floats

Working with complex data types like a list of floats:

```python
scores: List[float] = [98.5, 87.0, 94.5]
```

## Complex Types - Mixed List

Handling lists with mixed types using annotations:

```python
data: List[Union[int, str]] = [1, "two", 3, "four"]
```

## Complex Types - String and Int/Float to Tuple

Using annotations for tuples with mixed types:

```python
pair: Tuple[str, Union[int, float]] = ("value", 42)
```

## Complex Types - Functions

Annotating functions as types:

```python
from typing import Callable

def apply_function(func: Callable[[int], int], x: int) -> int:
    return func(x)
```

## Let's Duck Type an Iterable Object

Demonstrating duck typing by iterating through an iterable object:

```python
class DuckTypingExample:
    def __iter__(self):
        yield 1
        yield 2
        yield 3

duck_instance = DuckTypingExample()

for item in duck_instance:
    print(item)
```


### **Authors**
--- 

![GitHub Contributors Image](https://contrib.rocks/image?repo=RM92023/holbertonschool-low_level_programming)
Robinson Muñetón Jaramillo - <a href="https://github.com/RM92023" target="_blank"> @RM92023</a> ![Your Repository's Stats](https://github-readme-stats.vercel.app/api?username=RM92023&show_icons=true)