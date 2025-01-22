By Priyal Patel for _Neurotech@Davis_

# What is Jupyter Notebook?

Jupyter Notebook is a web application that allows you to easily write, run, and visualized smaller chunks of code. It is commonly used for data preprocessing and analysis.

# Installing Jupyter Notebook

First you need to install [python](https://www.python.org/downloads/) by downloading newest release and check that you downloading version where the operating system matches the device you are using (ex. macOS for a MAC).

After install [pip](https://pip.pypa.io/en/stable/installation/) using either ensurepip or get-pip.py.

Finally open the Terminal (Mac/Linux) or Command Prompt (Windows) and run this command:

```
$ pip install notebook
```

See Additional Resources for an alternative installation method using Anaconda Navigator.

# How to Use

**Opening Jupyter Notebook**

To open Jupyter Notebook, run this command:

```
$ jupyter notebook
```
Make sure the terminal window that you used to run this command stays open the whole time you are using Jupyter Notebook.

**Files and Folders Structure**

The Files section will look very similar to Finder (Mac) or File Explorer (Windows). If you select the box next to a folder/file, then click on an option this change will also automatically apply to your Finder/File Explorer. For example, if you delete a file, then you will need to go to your trash to recover it.

**Creating a Notebook**

Navigate to the folder where you want the notebook to be stored. Click "New" and select "Python 3". The new notebook will open in a new tab. If you navigate back to the folder, then a .ipynb file will have been added.

**Press Save**

The most important thing to remember is to periodically press the "save" button especially before closing the notebook or your laptop. After pressing the button, make sure a checkpoint created message appears.

**Cells**

Each box is called a cell. Using cells allows you to split up your code into multiple cells and add markdown cells to provide written explanations. Cells can be run in any order; however, if certain code requires an imported package, then the cell importing the package needs to be run first.

To add a cell, either click on "+" or select an option under "Insert". Use the dropdown to specify what type of cell (ex. code). 

More operations with cells can be found under "Edit". 

To run a cell, either click on "> Run" or select an option under "Cell". 

See the Beginner Tutorial in Additional Resources for more features and how to use them.

**Closing Jupyter Notebook**
Close all tabs in your browser that are running Jupyter Notebooks. Then, type (ctrl+c) in the terminal used to open Jupyter Notebook:
```
^c
y
```


# Additional Resources

- [Beginner Tutorial](https://www.dataquest.io/blog/jupyter-notebook-tutorial/)
- [Anaconda Navigator](https://sparkbyexamples.com/python/install-anaconda-jupyter-notebook/)
