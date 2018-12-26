## Welcome to Python from Scratch

This contains material to learning Python from scratch. The material in this class is suitable for students from 14 - 18 years of age!

### Table of contents

- [Lesson 0](#lesson-0) (Setting up, using your shell)

- [Lesson 1](https://github.com/jaychia/coding-class/l1.md) (Ints, Strings, Booleans, Lists, Dictionaries)

- [Lesson 2](https://github.com/jaychia/coding-class/l2.md) (Functions, If statements, Loops)

- [Lesson 3](https://github.com/jaychia/coding-class/l3.md) (Classes and Objects)

# Lesson 0

Welcome to Python from Scratch! In this lesson, we will be learning how to install and run Python on your machine as well as navigating your machine like a real programmer!

The instructions differ from Mac to Windows computers, so be sure to follow the instructions specific to your machine!

## Mac

[Download and install](https://www.python.org/ftp/python/3.6.3/python-3.6.3-macosx10.6.pkg) Python 3.6.3. Next, we will learn how to use your Terminal!

On your computer, open up the Terminal application and try to following commands:

1. `ls` - this lists the files/folders in the current directory you are in
2. `cd folder_name` - this changes the directory to `folder_name` from where you currently are
3. `mkdir folder_name` - this makes a new folder with name `folder_name`
4. `python` - this launches the python interpreter (the Python playground!)
5. `python filename.py` - this runs Python on the given file

As a start, let's `cd` into your Desktop using `cd Desktop`. Now, create a new folder called `coding-class` which will house all of your code/materials from this class. Great!

We need to install pip which is a Python package manager (it manages installations of Python packages which is code written by other people for your use). To do so, run `sudo easy_install pip`.

Lastly, we want to be working in a 'virtual environment' which will make working with Python a lot easier later on (trust me!).

To work in a virtual environment, follow the following workflow in your Terminal:

1. `pip install virtualenv` - this installs virtualenv, which is the package used to handle virtual environments
2. `virtualenv venv` - this creates a virtual environment in the folder `venv`, which is created in whichever directory your current shell is in; no need to run this if you have a pre-existing virtual environment!
3. `source venv/bin/activate` - this activates the virtual environment!

With your virtual environment activated, everything you install via pip will now go into that `venv` folder instead of somewhere mysterious wherever Python is installed your computer (a 'global' installation). This makes it a lot neater to do this per project! Just make sure to activate the virtual environment by running `.\venv\Scripts\activate` on the appropriate `venv` folder whenever you want to run code or install Python packages for the project.

## Windows

First, [download and install](https://www.python.org/ftp/python/3.6.3/python-3.6.3.exe) Python 3.6.3 - IMPORTANT: make sure when you install to check the 'Add python to path' option checkbox.

Now, we will learn how to navigate your computer using Powershell! On your computer, open up Powershell and try the following basic commands:

1. `ls` - this lists the files/folders in the current directory you are in
2. `cd folder_name` - this changes the directory to `folder_name` from where you currently are
3. `mkdir folder_name` - this makes a new folder with name `folder_name`
4. `python` - this launches the python interpreter (the Python playground!)
5. `python filename.py` - this runs Python on the given file

As a start, let's `cd` into your Desktop using `cd Desktop`. Now, create a new folder called `coding-class` which will house all of your code/materials from this class. Great!

To install Python packages, your installation of Python should come with `pip`, which is a Python package manager (it manages Python packages - code that other people have written that you can use - for you). You will also want to work in a 'virtual environment' which will make working with Python a lot easier later on (trust me!)

To work in a virtual environment, follow the following workflow in your Powershell:

1. `pip install virtualenv` - this installs virtualenv, which is the package used to handle virtual environments
2. `virtualenv venv` - this creates a virtual environment in the folder `venv`, which is created in whichever directory your current shell is in
3. `Set-ExecutionPolicy AllSigned` - this gives us permissions to activate the virtual environment
3. `.\venv\Scripts\activate` - this activates the virtual environment!

With your virtual environment activated, everything you install via pip will now go into that `venv` folder instead of somewhere mysterious wherever Python is installed your computer (a 'global' installation). This makes it a lot neater to do this per project! Just make sure to activate the virtual environment by running `.\venv\Scripts\activate` on the appropriate `venv` folder whenever you want to run code or install Python packages for the project.
