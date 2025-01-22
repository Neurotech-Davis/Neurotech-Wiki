By Priyal Patel for _Neurotech@Davis_

# What is Jupyter Notebook?

Jupyter Notebook is a web application that allows you to easily write, run, and visualize smaller chunks of code. It is commonly used for data preprocessing and analysis.

# Installing Jupyter Notebook

First, install [python](https://www.python.org/downloads/) by downloading newest release and check that you downloading version where the operating system matches the device you are using (ex. macOS for a MAC).

After, install [pip](https://pip.pypa.io/en/stable/installation/) using either ensurepip or get-pip.py.

Finally, open the Terminal (Mac/Linux) or Command Prompt (Windows) and run this command:

```
$ pip install notebook
```

See Additional Resources for an alternative installation method using Anaconda Navigator.

# How to Use

**Opening Jupyter Notebook**

<img width="600" alt="Screenshot 2025-01-21 at 11 06 01 PM" src="https://github.com/user-attachments/assets/a756bfca-e835-4d29-a534-a1669638607b" />

To open Jupyter Notebook, run this command:

```
$ jupyter notebook
```
Make sure the terminal window that you used to run this command stays open the whole time you are using Jupyter Notebook.

**Files and Folders Structure**

<img width="600" alt="Screenshot 2025-01-21 at 11 14 39 PM" src="https://github.com/user-attachments/assets/3cae42c4-b6e4-4aa0-a58c-8ef38e57a0f9" />

The Files section will look very similar to Finder (Mac) or File Explorer (Windows). If you select the box next to a folder/file, then click on an option this change will also automatically apply to your Finder/File Explorer. For example, if you delete a file, then you will need to go to your trash to recover it.

**Creating a Notebook**

<img width="600" alt="Screenshot 2025-01-21 at 11 16 33 PM" src="https://github.com/user-attachments/assets/ad3ce7aa-3f84-4c34-80a5-4a88ef19b86c" />

Navigate to the folder where you want the notebook to be stored. Click "New" and select "Python 3". The new notebook will open in a new tab. If you navigate back to the folder, then a .ipynb file will have been added.

**Press Save**

<img width="600" alt="Screenshot 2025-01-21 at 11 19 50 PM" src="https://github.com/user-attachments/assets/85478aa2-2726-4d10-8113-453cc2ea7710" />

The most important thing to remember is to periodically press the "save" button especially before closing the notebook or your laptop. After pressing the button, make sure a checkpoint created message appears.

**Cells**

<img width="600" alt="Screenshot 2025-01-21 at 11 19 29 PM" src="https://github.com/user-attachments/assets/a9f1b60c-8e5c-4853-a7f6-3c5349b49416" />

Each box is called a cell. Using cells allows you to split up your code into multiple cells and add markdown cells to provide written explanations. Cells can be run in any order; however, if certain code requires an imported package, then the cell importing the package needs to be run first.

To add a cell, either click on "+" or select an option under "Insert". Use the dropdown to specify what type of cell (ex. code). 

More operations with cells can be found under "Edit". 

To run a cell, either click on "> Run" or select an option under "Cell". 

See the Beginner Tutorial in Additional Resources for more features and how to use them.

**Closing Jupyter Notebook**

<img width="400" alt="Screenshot 2025-01-21 at 11 40 40 PM" src="https://github.com/user-attachments/assets/eb9c3c7f-5aa8-492b-99f9-d6ebe480b5ff" />

Close all tabs in your browser that are running Jupyter Notebooks. Then, type (ctrl+c) and after 'y' in the terminal used to open Jupyter Notebook:
```
^c
y
```

# Additional Resources

- [Beginner Tutorial](https://www.dataquest.io/blog/jupyter-notebook-tutorial/)
- [Anaconda Navigator](https://sparkbyexamples.com/python/install-anaconda-jupyter-notebook/)
