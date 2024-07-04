By Manik Sethi for *Neurotech@Davis*

Now that we've covered the basics of Python, we will dive into libraries which give us additional functionality. In this tutorial, we will cover [NumPy](https://numpy.org/doc/) and [Pandas](https://pandas.pydata.org/) . To follow this tutorial, make sure you have Python installed on your computer and a text-editor ready to work with.

## Table of Contents
- [Table of Contents](#table-of-contents)
- [1. Getting Started](#getting-started)
	- [1.1. Making Sure You Have PIP](#making-sure-you-have-pip)
	- [1.2. Importing Libraries](#importing-libraries)
- [2. NumPy](#numpy)
	- [2.1. Array Fundamentals](#array-fundamentals)
	- [2.2. Indexing and Slicing](#indexing-and-slicing)


## 1. Getting Started
### 1.1. Making Sure You Have PIP
Since libraries are add-ons to the basic version of Python, we need to install them onto our machines. We will be using the package installer for Python, which is called [pip](https://pip.pypa.io/en/stable/). First, we will ensure that the machine you're working on has pip. To do so, open up a terminal window and type the following command:

**MacOS**
`python  -m  ensurepip  --upgrade`
**Windows**
` py -m ensurepip --upgrade`

Typically, pip comes with the installation of Python in your system. But we will run these commands as a preventative measure for any errors down the line.

Now, we will install the packages onto our system. Enter the following terminal commands. [^1]

```
pip install numpy
pip install pandas
```
### 1.2. Importing Libraries
Now that we have our libraries installed, we can call upon them in. our `.py` files. To use the functionalities of our library in a given `.py` file, we type this at the very top.

```
import numpy as np
import pandas as pd
```
Let's break down these lines phrase by phrase
- `import` followed by the library name tells our code to load in the library, allowing us to access its functions and variables. 
- Using the `as` keyword let's us shorten our library name and give it a nickname [^2]. That way, instead of having to call functions using `numpy.function()`, we can just do `np.function()`
## 2. NumPy
Now that we have imported NumPy, let's access it and use it's functions and variables. For the sake of being concise we won't cover everything, but here is the [documentation.](https://numpy.org/doc/2.0/user/absolute_beginners.html)

### 2.1. Array Fundamentals
Let's start by creating an *array*, which is just a list of objects.
```
Input:
a = np.array([1, 2, 3, 4, 5, 6])
a
```
```
Output:
array([1, 2, 3, 4, 5, 6])
```
we used the `np.array()` function which takes in one argument: a list. However, this is just a one dimensional list, also known as a vector. In our use cases, it may be useful to have *list of lists*, also known as matrix. We can initialize one as shown below
```
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
```
As practice, can you guess what `matrix[0], matrix[2][1]` and `matrix[3]` will return? [^3] The correct answers would be `array([1, 2, 3]), 8, and IndexError`

NumPy also comes with functions that return attributes of our array

- `matrix.ndim` returns number of dimensions of the array. Since we made a 2D matrix, it'd be `2`
- `matrix.shape` returns the shape of our array, think of this as the length and width of our array, which is `(3,3)`
- `matrix.size` tells you how many *total* elements exist in our array, which in our case is `9`

Arrays will be incredibly useful for neurotech applications. All the brain data we will collect needs to be stored, and the `np.array()` datatype allows us to do so while also providing high functionality. If we used basic Python lists, we'd have to define these `shape`, `size`, and other functions on our own which becomes redundant quickly. NumPy takes care of this and lets us work on the important parts of the project.
### 2.2. Indexing and Slicing

The data we collect will also need to be manipulated. Thankfully, NumPy takes care of this. Sometimes we only want to work with specific parts of our data because of it's temporal importance (when it happened) or spatial importance (where it happened)


## Footnotes
[^1]: sometimes python decides to be funny and requires you type `pip3` instead of just `pip`. Please be mindful of what python version you have installed. If it's Python3, do the former.
[^2]: When choosing a nickname, make sure it's intuitive as to what library it's referring.
[^3]: The integers inside the `[]` such as `[0]` represent the index of the element to retrieve. Since Python is 0-based, `[0]` is the first element in the array. Here is a great resource for [Indexing in Python](https://www.hackerearth.com/practice/notes/samarthbhargav/a-quick-intro-to-indexing-in-python/)
