## Welcome to Python from Scratch

This contains material to learning Python from scratch. The material in this class is suitable for students from 14 - 18 years of age!

### Table of contents

- [Lesson 0](#lesson-0) (Setting up, using your shell)

- [Lesson 1](#lesson-1) (Ints, Strings, Booleans, Lists, Dictionaries)

- [Lesson 2]() (Functions, If statements, Loops)

- [Lesson 3]() (Classes and Objects)

# Lesson 0

Welcome to Python from Scratch! In this lesson, we will be learning how to install and run Python on your machine as well as navigating your machine like a real programmer!

The instructions differ from Mac to Windows computers, so be sure to follow the instructions specific to your machine!

## Mac

[Download and install](https://www.python.org/ftp/python/3.6.3/python-3.6.3-macosx10.6.pkg) Python 3.6.3. Next, we will learn how to use your Terminal!

On your computer, open up the Terminal application and try to following commands:

1. `ls` - this lists the files/folders in the current directory you are in
2. `cd folder_name` - this changes the directory to `folder_name` from where you currently are; to move one folder back, try `cd ..`
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

With your virtual environment activated, everything you install via pip will now go into that `venv` folder instead of somewhere mysterious wherever Python is installed your computer (a 'global' installation). This makes it a lot neater to do this per project! Just make sure to activate the virtual environment by running `source venv/bin/activate` on the appropriate `venv` folder whenever you want to run code or install Python packages for the project.

## Windows

First, [download and install](https://www.python.org/ftp/python/3.6.3/python-3.6.3.exe) Python 3.6.3 - IMPORTANT: make sure when you install to check the 'Add python to path' option checkbox.

Now, we will learn how to navigate your computer using Powershell! On your computer, open up Powershell and try the following basic commands:

1. `ls` - this lists the files/folders in the current directory you are in
2. `cd folder_name` - this changes the directory to `folder_name` from where you currently are; to move one folder back, try `cd ..`
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

# Lesson 1

Now you know the basic commands to navigate around your computer via Terminal/Powershell. Cool! Let's begin learning some Python!

On your shell, type `python` and press enter. This launches the interactive Python interpreter - a Python playground of sorts. It is useful for playing with code! 

In programming, we have something called 'variables' which are names that we allocate to certain things. To allocate a variable, we use the `=` sign. For example, `x = 40` means we allocate the value of `40` to `x`. From now on, whenever we invoke `x`, we are invoking `40`! So something like `x + 5` will return us the value `45`.

In Python, you can use `print(x)` to show the value ('printing' it) on your shell. Try it! Type something like `print(40)` in your shell and check that the shell prints the value `40` after you press enter.

Let's first learn about the basic types:

### Integers
Integers are round numbers like `1` and `-999`. They have built-in functionality that are not limited to the following:

1. `int1 + int2` - Adds `int1` and `int2`
2. `int1 * int2` - Multiplies `int1` and `int2`
3. `int1 - int2` - Subtracts `int2` from `int1`
4. `int1 / int2` - Divides `int1` by `int2` and returns a float
5. `int1 // int2` - Divides `int1` by `int2` and returns an integer (rounded down result of `int1 / int2`)
6. `int1 % int2` - Gets integer remainder of `int1 / int2`

Try typing the above into your interpreter, substituting `int1` and `int2` out for actual numbers!

### Strings
Strings are a sequence of characters, such as `'hi'`, `'hello world'` or even `''` which is the empty string. Strings can be really long too, like a whole paragraph worth of words!

Let's try defining a string and assign it to a variable! Try something like `s1 = 'hello'`. Now, type `print(s1)` and see that Python prints `'hello'` to your shell. Coolio.

How do we join strings together? Python has a shortcut for doing so which is the `+` operator. Try typing `print(s1 + s1)` into your interpreter now! You should get `'hellohello'` as the output.

### Booleans
Booleans are values that can either be `True` or `False`. This is really useful for logic! Comparisons will give us booleans as results, for example `5 > 4` should be `True`!

Try the following on your terminal and see that they return what you'd expect:

1. `5 > 4` - returns `True` because 5 is bigger than 4
2. `4 < 5` - returns `True` because 4 is smaller than 5
3. `4 == 4` - returns `True` because 4 is equal to 4
4. `'hello' == 'hello'` returns `True` because the two strings are equivalent
5. `4 != 4` - returns `False` because 4 is not-not-equal to 4 (i.e. 4 is equal to 4).
6. `5 >= 4` returns `True` because 5 is bigger than or equal to 4
6. `5 <= 4` returns `False` because 5 is not smaller than or equal to 4

### Lists
Lists are objects that are an ordered collection of elements. By this, I really just mean that it contains 'things' in a certain order. To create a list, you do something like `[1,2,3]`. This is really useful because lists can store stuff in a certain order! For example, in a game you might want to store a list of items you have in your inventory, or a list of enemies you have to clear etc.

Something really interesting about lists is how we access them. Try the following (words after `#` are for commenting purposes and do not need to be entered into the shell):

```
l = [] # This creates an empty list
print(l) # Check that l is an empty list
l.append(1) # This puts the element 1 at the end l
print(l) # l is now a list [1]
l.append(2)
l.append(3) # l is now a list [1,2,3]
```

Now, to access the first element of `l`, we do `l[0]`. This `l[...]` syntax is called 'indexing'. Programmers refer to the first element of the list as the 0th element (this is called 0-based indexing), and hence to retrieve it we index at `0`! This is for good reason, because it makes taking 'slices' of the list much easier!

Aaaaand what exactly is a slice? Well, lets say you had a list `l = [1,2,3,4,5]`. You want to take a slice `[2,3,4]` (just like a pizza slice) out of this original list - the code for doing so is just `l[1:4]`! 0-based indexing makes it such that we can imagine the list as having 'buckets' of elements, and each divider in between the buckets is given a number. For e.g. `|1|2|3|4|5|`, and we number each divider incrementally from 0. To take a slice, we just define the slice to be between 2 dividers! Much easier than talking in terms of the buckets, isn't it?

### Dictionaries

Our last object for this lesson is the Dictionary. A dictionary allows us to have a 'mapping' from one set of values to another. For example, a dictionary representing a weapon in a game could look like:

```
weapon = {
  'damage': 50,
  'name': 'dagger of mischief',
  'ownder': 'Jay Chia'
}
```

You can see how this might be useful to store information! We can later retrieve information regarding the damage of the weapon by calling `weapon['damage']`.
