---
layout: post
title: Python Essential Basics Summary
date: 2025-04-22 12:50:0 +0000
categories: [python]
tags: [python, study]
---
# Python Essential Basics Summary (Compressed Review)

This document summarizes the core syntax of Python necessary for understanding and writing code for data analysis and processing.

## 1. Variables and Data Types

* Variables are containers for storing values. Use the `=` sign to assign values.
* Python does not require explicit type declaration when defining variables (dynamic typing).
* **Key Built-in Data Types:**
    * **Numeric Types:** `int` (integers), `float` (floating-point numbers)
        ```python
        age = 24          # integer
        height = 180.2    # float
        ```
    * **String:** `str` Enclosed in quotes (' ', " ", ''' ''', """ """)
        ```python
        name = "John Kim"
        greeting = 'Hello there'
        multiline_text = """A long string that
        can span multiple lines."""
        ```
    * **Boolean:** `bool` Represents logical values `True` or `False`.
        ```python
        is_student = True
        is_employed = False
        ```
    * **None Type:** `NoneType` Represents the absence of a value. Can be similar to missing values (`NaN`) in Pandas sometimes.
        ```python
        result = None
        ```

## 2. Operators

* **Arithmetic Operators:** `+`, `-`, `*`, `/`, `%` (modulo), `//` (floor division), `**` (exponentiation)
    ```python
    a = 10 + 5     # 15
    b = 10 / 3     # 3.333...
    c = 10 // 3    # 3
    d = 10 % 3     # 1
    e = 2 ** 3     # 8
    ```
* **Comparison Operators:** `==` (equal), `!=` (not equal), `<`, `>`, `<=`, `>=` Return boolean results.
    ```python
    print(5 == 5)   # True
    print(5 != 3)   # True
    print(10 > 20)  # False
    ```
* **Logical Operators:** `and`, `or`, `not` Perform logical operations on boolean values.
    ```python
    print(True and False) # False
    print(True or False)  # True
    print(not True)       # False
    ```
* **Assignment Operators:** `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `//=`, `**=` Assign values to variables or perform operation then assign.
    ```python
    x = 10
    x += 5 # Same as x = x + 5, x becomes 15
    ```

## 3. Data Structures (Collections)

Containers for holding multiple values.

* **List:** Defined with `[]`, **ordered and mutable** (changeable)
    ```python
    my_list = [1, "apple", 3.14, True]
    print(my_list[0])       # Indexing: 1
    print(my_list[1:3])     # Slicing: ["apple", 3.14]
    my_list.append("banana") # Add element
    print(len(my_list))     # Length: 5
    ```
* **Tuple:** Defined with `()`, **ordered but immutable** (unchangeable)
    ```python
    my_tuple = (10, 20, 30)
    print(my_tuple[1])      # Indexing: 20
    # my_tuple.append(40)   # Will cause an error
    ```
* **Dictionary:** Defined with `{}` storing `Key: Value` pairs, **ordered (since Python 3.7) and mutable**
    ```python
    my_dict = {'name': 'Kim', 'age': 30, 'city': 'Seoul'}
    print(my_dict['name'])      # Access value by key: 'Kim'
    my_dict['age'] = 31        # Change value
    my_dict['job'] = 'Engineer' # Add new key-value pair
    print(my_dict.keys())    # List of keys: dict_keys(['name', 'age', 'city', 'job'])
    print(my_dict.values())  # List of values: dict_values(['Kim', 31, 'Seoul', 'Engineer'])
    print(my_dict.items())   # List of key-value pairs: dict_items([('name', 'Kim'), ...])
    ```
* **Set:** Defined with `{}` (use `set()` for an empty set), **unordered and does not allow duplicate elements**
    ```python
    my_set = {1, 2, 3, 3, 4}
    print(my_set)          # {1, 2, 3, 4} (Duplicates removed)
    my_set.add(5)          # Add element
    my_set.remove(1)       # Remove element
    ```

## 4. Control Flow

Controls the execution flow of code. Python uses **indentation** to define code blocks.

* **Conditional Statements (if, elif, else):** Execute different code blocks based on a condition's result.
    ```python
    score = 85
    if score >= 90:
        print("Grade: A")
    elif score >= 80:
        print("Grade: B")
    else:
        print("Grade: C")
    ```
* **Loops (for):** Iterate over elements of an **iterable object** (like lists, tuples, strings) or repeat a block of code a fixed number of times using `range()`.
    ```python
    fruits = ["apple", "banana", "cherry"]
    for fruit in fruits:
        print(fruit)

    # Using range() to repeat a specific number of times
    for i in range(5): # Repeats 5 times (for i = 0, 1, 2, 3, 4)
        print(i)
    ```
* **Loops (while):** Repeat a code block as long as a condition is `True`.
    ```python
    count = 0
    while count < 3:
        print("Count:", count)
        count += 1
    ```

## 5. Functions

Group specific tasks into reusable blocks of code.

* Defined using the `def` keyword.
* Can accept arguments (parameters) and return values using the `return` keyword.
    ```python
    def greet(name):
        """Function to print a greeting""" # Docstring (function description)
        print(f"Hello, {name}!") # f-string (string formatting)

    def add_numbers(a, b):
        """Function to return the sum of two numbers"""
        return a + b

    # Calling functions
    greet("John") # Output: Hello, John!
    result = add_numbers(10, 20)
    print(result) # Output: 30
    ```

## 6. Comments

Used to add explanations or notes to code. Python interpreters ignore comments.

* `#` : Single-line comment
* `''' '''` or `""" """` : Multi-line comments (often used as docstrings for functions/classes)
    ```python
    # This is a single-line comment.

    '''
    This is a multi-line
    comment or docstring.
    '''
    ```

## 7. Output

* `print()`: Outputs values to the console (screen). Can output multiple values separated by commas.
    ```python
    print("Hello, World!")
    print("Name:", "John", "Age:", 24)
    ```

## 8. Indentation

* The **only way** to define code blocks in Python. Code dependent on `if`, `for`, `while`, `def`, `class`, etc., must be indented consistently (typically **4 spaces**).
    ```python
    if True:
        print("This code belongs to the if block.") # Indented
        print("So it runs when the if condition is True.") # Same indentation level
    else:
        print("This code belongs to the else block.") # Indented
    print("This code is independent of the if-else block.") # Not indented
    ```

---

