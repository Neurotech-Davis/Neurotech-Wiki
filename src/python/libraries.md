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
	- [2.3. Reshaping and Flattening](#reshaping-and-flattening)
- [3. Pandas](#pandas)
	- [3.1. Dataframe](#dataframes)
	- [3.2. Reading and Writing](#reading-and-writing)
- [4. Conclusion](#conclusion)


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
Now that we have imported NumPy, let's access and use it's functions and variables. For the sake of being concise we won't cover everything, but here is the [documentation.](https://numpy.org/doc/2.0/user/absolute_beginners.html)

### 2.1. Array Fundamentals
Arrays will be incredibly useful for neurotech applications. All the brain data we will collect needs to be stored, and the `np.array()` datatype allows us to do so while also providing high functionality. Let's start by creating an *array*, which is just a list of objects.
```
Input:
a = np.array([1, 2, 3, 4, 5, 6])
a
```
```
Output:
array([1, 2, 3, 4, 5, 6])
```
We used the `np.array()` function which takes in one argument: a list. However, this is just a one dimensional list, also known as a vector. In our use cases, it may be useful to have *list of lists*, also known as matrix. We can initialize one as shown below
```
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
```
NumPy also comes with functions that return attributes of our array

- `matrix.ndim` returns number of dimensions of the array. Since we made a 2D matrix, it'd be `2`
- `matrix.shape` returns the shape of our array, think of this as the length and width of our array, which is `(3,3)`
- `matrix.size` tells you how many *total* elements exist in our array, which in our case is `9`

If we used basic Python lists, we'd have to define these `shape`, `size`, and other functions on our own which becomes redundant quickly. NumPy takes care of this and lets us work on the important parts of the project.
### 2.2. Indexing and Slicing

The data we collect will also need to be manipulated. Thankfully, NumPy takes care of this. Sometimes we only want to work with specific parts of our data because of it's temporal importance (when it happened) or spatial importance (where it happened)
```
data = np.array([[1, 7, 3, 9], 
				[2, 5, 0, 4], 
				[7, 3, 4, 1], 
				[8, 6, 0, 2]])
data[0]
data[2][1]
data[3]
data[5][0]
```
The integers inside the `[]` such as `[0]` represent the index of the element to retrieve. Since Python is 0-based, `[0]` is the first element in the array. Therefore, `[2][1]` is the first element of the second element! Here is a great resource for [Indexing in Python](https://www.hackerearth.com/practice/notes/samarthbhargav/a-quick-intro-to-indexing-in-python/). As practice, guess what the previous code snippet will return. The answer will be in the footnotes [^3]

Slicing lets us manipulate our matrix by cutting out specific parts. We will continue using the `data` variable from the previous example. If we want to access the first two objects inside `data`, we can write out the following line of code:
```
data[0:2]
```
the `[0:2]` lets our computer know we only want objects from the 0th index, up to the 2nd index (exclusive[^4]). Here are the rules for slicing:
- `data[x:y]` returns an object with elements from the xth index to yth index 
- `data[x:]` returns an object with all elements starting from the xth index
- `data[:y]` returns an object with all elements up till the xth index

### 2.3. Reshaping and Flattening
Sometimes we need to reshape our data to execute certain operations on it. NumPy comes with a `.reshape()` function which takes in two arguments, the number of rows and columns
```
Input:
a = np.array([1, 2, 3, 4, 6])
b = a.reshape(3, 2)
```
```
Output:
array([1, 2, 3, 4, 5, 6])
array([0, 1], 
	  [2, 3], 
	  [4, 5] )
```
We reshaped our flat array `a` to have 3 rows and 2 columns. NumPy also has a function to go from an arbritary shape array back to a flat array.

Flattening our data gets rid of the dimensionality, and turns our higher dimensional data into a 1-D vector. 
```
Input
c = b.flatten()
```
```
Output:
array([1, 2, 3, 4, 5, 6])
```
No parameters are needed, since it will *always* turn the array back into a one dimensional list.

Reshaping and flattening are crucial operations for making sure our data is compatible with certain operations, such as matrix multiplication. If the dimensions don't match, we can reshape our data to fix it.



## 3. Pandas
Moving on, we will cover the basics of pandas. Once again, here is the link for the comprehensive [documentation](https://pandas.pydata.org/docs/getting_started/index.html#getting-started)

### 3. 1. Dataframes
Pandas is used for two-dimensional *tabular data*, such as data stored in spreadsheets. The most common datatype we work with in pandas is called a *DataFrame*. Let's make one right now.
```
df = pd.DataFrame(
     {
         "Name": ["Avni", "Aryaman", "Sofia", "Manik", "Grace", "Priyal"],
         "Sex": ["female", "male", "female", "male", "female", "female"],
     }
 )
```
Here is a table we've made of the current projects division board members. If we print it out, we would get the following
|index|Name|Sex|
|---|---|---|
|0|Avni|female|
|1|Aryaman|male|
|2|Sofia|female|
|3|Manik|male|
|4|Grace|female|
|5|Priyal|female|
Here is a list of the two most basic return functions
- `df["{column_name}"]` returns the column corresponding to the column name
- `df.iloc[x:y]` returns the rows ranging from index `x` to index `y` (exclusive)

### 3.2. Reading and Writing 
Most likely, you will be creating dataframes with pre-existing csv files from data collection. Luckily, Pandas supports the ability to read from these files

```
data = pd.read_csv("directory/data.csv")
```
The variable `data` has a type `DataFrame`, which means all the previous functions we used can be applied here as well. 
- `data.head(x)` will display the first `x` rows of the dataframe
- `data.tail(x)` does the opposite and displays the last `x` rows of the dataframe
- `data.shape` returns the shape of our dataframe

To write out the tabular data we have manipulated, we can use the function
`df.to_csv("board_members.csv", sheet_name="board")`

Here is a link for a more comprehensive guide towards [dataframe indexing](https://pandas.pydata.org/docs/getting_started/intro_tutorials/03_subset_data.html)

## 4. Conclusion
This Python tutorial covered important libraries that will be relevant to your work in signal pre-processing and manipulation. Libraries such as NumPy and Pandas come with a vast amount of functionality, allowing users to focus on meaningful work, and generate results quickly.


[^1]: sometimes python decides to be funny and requires you type `pip3` instead of just `pip`. Please be mindful of what python version you have installed. If it's Python3, do the former.
[^2]: When choosing a nickname, make sure it's intuitive as to what library it's referring.
[^3]: `[1 7 3 9], 3, [8 6 0 2], IndexError`. An IndexError occurs because there is no value at the `[5]` index of our variable.
[^4]: By exclusive, we mean that `data[0:2]` will not include the element at the 2nd index

