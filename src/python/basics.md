# Python Basics

By Dhruv Sangamwar for _Neurotech@Davis_

Python is a versatile and popular programming language known for its simplicity and readability. In this tutorial, we will cover the basics of Python, including variables, data types, control structures, functions, and more.

## Table of Contents

- [Table of Contents](#table-of-contents)
- [1. Getting Started](#1-getting-started)
  - [1.1. Installing Python](#11-installing-python)
    - [MacOS](#macos)
    - [Windows](#windows)
  - [1.2. Running Python](#12-running-python)
- [2.Variables and Data Types](#2variables-and-data-types)
- [3. Control Structures](#3-control-structures)
  - [3.1. Conditional Statements](#31-conditional-statements)
  - [3.2. Loops](#32-loops)
    - [3.2.1. `for` Loop](#321-for-loop)
    - [3.2.2. `while` Loop](#322-while-loop)
- [4. Functions](#4-functions)
- [5.Modules and Packages](#5modules-and-packages)
- [6. File Handling](#6-file-handling)
- [7. Error Handling](#7-error-handling)
- [8. Object Oriented Programming](#8-object-oriented-programming)
- [9. Conclusion](#9-conclusion)

<a name="getting-started"></a>
## 1. Getting Started

### 1.1. Installing Python

Before you can start programming in Python, you need to make sure you have a text-editor and the right environment.
#### MacOS
* We personally recommend using [Homebrew](https://brew.sh/#install), a package manager that handles package download and installations
* Follow the following commands to install , python and some libraries.
> `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"` : Installs Homebrew.\
> `export PATH="/usr/local/opt/python/libexec/bin:$PATH"` : This sets up the Path variable so that your command line can find python.
The following commands will install python along with some libraries: 
```
brew install python
python --version
pip install numpy
pip install seaborn
pip install matplotlib
```
We strongly reccomend that you use [Visual Studio code](https://code.visualstudio.com) as it has plenty of free plugins that make development in python easier.

If you want to use any additional packages, visit [PyPi](https://pypi.org). This is the python package index where you can find installation instructions and documentation for packages. (Make sure to check which version you want before installation) 

#### Windows
* Environment setup has a couple more steps on Windows
* **Open command prompt as an administrator**
* Run `wsl --install` to install WSL2.
  * _Restart your computer after the step._
* At this point you should be able to run `wsl` in your command prompt which should start a linux vm.
  * _If this is not the case please reach out to anyone on the projects division to debug platform related issues._
* You can now use the same commands as above for MacOS to install python and all the related dependencies
* Install [Visual Studio code](https://code.visualstudio.com) and run `code .` in your command prompt; `code .` should open up VScode where you can write all your python code.
  * WSL should detect that you are trying to open VScode, it will install the virtualized version of it automatically and open the desktop VScode client. 

### 1.2. Running Python

You can run Python code in two ways: using the Python interactive interpreter or by creating Python scripts.

To start the Python interactive interpreter, open your terminal or command prompt and type:

```
python
```
You can also run Python scripts by creating a .py file and executing it with the python command.
```
# hello.py
print("Hello, Python!")
```
To run the script:
```
python hello.py
```

<a name="variables-and-data-types"></a>
## 2.Variables and Data Types

In Python, you don't need to declare the data type of a variable explicitly. Python infers it based on the value assigned.
```
# Integer
x = 10

# Float
y = 3.14

# String
name = "Alice"

# Boolean
is_python_fun = True

# List
fruits = ["apple", "banana", "cherry"]

# Tuple
coordinates = (3, 4)

# Dictionary
person = {"name": "Bob", "age": 30}
```

<a name="control-structures"></a>
## 3. Control Structures

Python provides various control structures like if, for, and while for managing program flow.

### 3.1. Conditional Statements

```
if condition:
    # Code to execute if the condition is True
elif another_condition:
    # Code to execute if the second condition is True
else:
    # Code to execute if none of the conditions are True

```

### 3.2. Loops

#### 3.2.1. `for` Loop

```
for item in iterable:
    # Code to execute for each item in the iterable
```

#### 3.2.2. `while` Loop

```
while condition:
    # Code to execute as long as the condition is True
```

<a name="functions"></a>
## 4. Functions
Functions allow you to encapsulate code into reusable blocks.
```
def greet(name):
    """A simple greeting function."""
    print(f"Hello, {name}!")

# Calling the function
greet("Alice")\
```

<a name="modules-and-packages"></a>
## 5.Modules and Packages
Python has a rich ecosystem of modules and packages to extend its functionality. We installed some earlier if you followed the getting started section.

```
# Importing a module
import math
import numpy as np

# Using a module function
print(math.sqrt(16))

# using numpy
arr = np.array([[1, 2],
                [3, 4]])
print("Matrix: \n", arr)
```

<a name="file-handling"></a>
## 6. File Handling
Python provides functions for reading from and writing to files.

```
# Opening a file for reading
with open("file.txt", "r") as file:
    content = file.read()

# Opening a file for writing
with open("new_file.txt", "w") as file:
    file.write("Hello, World!")
```

<a name="error-handling"></a>
## 7. Error Handling
Use `try` and `except` blocks to handle errors gracefully.

```
try:
    # Code that might raise an exception
except ExceptionType:
    # Code to handle the exception
else:
    # Code to execute if no exception is raised
finally:
    # Code that always runs, regardless of exceptions
```

<a name="object-oriented-programming"></a>
## 8. Object Oriented Programming
Python supports object-oriented programming (OOP) principles like classes and inheritance.

```
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

# Creating objects
dog = Dog("Buddy")
print(dog.speak())
```

<a name="conclusion"></a>
## 9. Conclusion 
This Python tutorial covered the fundamental concepts of the Python programming language, including variables, data types, control structures, functions, modules, file handling, error handling, and object-oriented programming. Python is a versatile language with a vast ecosystem of libraries and frameworks, making it suitable for your Neurotech projects. 


