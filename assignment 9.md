Topic 1: Modules / Packages

## Research: 
- Investigate the difference between a module and a package in Python. Provide examples to illustrate how they are used and their significance in Python programming. You can explain by writing an 
article and providing relevant examples. 


Ans-In Python, a module is a single file containing Python code, whereas a package is a collection of modules that are organized in a directory hierarchy1. A module can define functions, classes, and variables, and can also include runnable code2. For example, you can create a module named example.py that contains the following code:

# Python Module example
def add(a, b):
    result = a + b
    return result

This module defines a function named add that takes two arguments and returns their sum. You can then use this module in another Python script by importing it using the import statement:

import example
print(example.add(3, 4))

A package, on the other hand, is a collection of modules organized into a directory hierarchy. To be considered a package, the directory must contain an __init__.py file1. For example, you can create a package named mymath that contains two modules: basic.py and advanced.py. The directory structure would look like this:

mymath/
    __init__.py
    basic.py
    advanced.py

The basic.py module could contain basic mathematical functions like addition and subtraction, while the advanced.py module could contain more advanced functions like integration and differentiation. You can then use the modules in this package by importing them using the from ... import ... statement:

from mymath.basic import add, subtract
from mymath.advanced import integrate, differentiate

print(add(3, 4))
print(integrate(lambda x: x**2, 0, 1))

Modules and packages are important constructs in Python that promote code modularization. By organizing code into modules and packages, you can make your code easier to understand, maintain, and reuse3. Additionally, modules typically define a separate namespace, which helps avoid collisions between identifiers in different areas of a program3. This makes it easier to work collaboratively on large applications.


## Implementation: 
- Create a Python module named "math_operations.py" that contains functions for basic mathematical operations such as addition, subtraction, multiplication, and division. Import this module into another Python script and demonstrate the usage of its functions.

Ans-
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        raise ValueError('Cannot divide by zero')
    return x / y

You can save this code to a file named math_operations.py. Then, you can import this module into another Python script and use its functions like this:

import math_operations as mo

print(mo.add(3, 4)) # 7
print(mo.subtract(3, 4)) # -1
print(mo.multiply(3, 4)) # 12
print(mo.divide(3, 4)) # 0.75

## Exploration: 
- Research and explore popular third-party packages available in the Python Package Index (PyPI). Choose one package that interests you and explain its purpose, functionality, and how to install and use it in your Python projects.

Ans-
One popular third-party package available in the Python Package Index (PyPI) is NumPy. NumPy is a fundamental package for scientific computing in Python. It provides support for large, multi-dimensional arrays and matrices, along with a collection of high-level mathematical functions to operate on these arrays1. NumPy is widely used in various fields, including data science, machine learning, and engineering.

To install NumPy, you can use the pip command in your command prompt or terminal: pip install numpy. Once installed, you can import the package into your Python script using the import statement: import numpy as np. You can then use the various functions and methods provided by NumPy to perform operations on arrays and matrices. For example, you can create a 2D array using the np.array() function and perform element-wise addition using the + operator:

import numpy as np

a = np.array([[1, 2], [3, 4]])
b = np.array([[5, 6], [7, 8]])

c = a + b
print(c)

This code creates two 2D arrays a and b, adds them together element-wise, and stores the result in a new array c. The output of this code would be:

[[ 6  8]
 [10 12]]

NumPy provides many other functions and methods for performing operations on arrays and matrices, including mathematical operations, statistical operations, and more.

