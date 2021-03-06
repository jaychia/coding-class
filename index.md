## Welcome to Python from Scratch

This contains material to learning Python from scratch. The material in this class is suitable for students from 14 - 18 years of age!

### Table of contents

- [Lesson 0](#lesson-0) (Setting up, using your shell)

- [Lesson 1](#lesson-1) (Ints, Strings, Booleans, Lists, Dictionaries)

- [Lesson 2](#lesson-2) (Functions, If statements, Loops)

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

Python also has a `not` keyword, which negates a boolean that follows it. Try this out:

1. `not True` - returns `False`
2. `not False` - returns `True`
3. `not 5 >= 4` - returns `False` because 5 is bigger than or equal to 4, and we negate that!

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
  'owner': 'Jay Chia',
  'upgraded': True,
  'previous_owners': ['James', 'Jamie'],
  'other_stats': {
    'age': 50,
    'durability': 0.4,
  }
}
```

You can see how this might be useful to store information! We can later retrieve information regarding the damage of the weapon by calling `weapon['damage']`. Notice also how we can put a dictionary within the dictionary! This is called a 'nested' dictionary.

To assign a new key and value in a dictionary, use `d[key] = value`. For example, if we did `weapon[3] = False`, the new weapon dictionary will look like (... added so I don't have to write the rest of the dictionary):

```
weapon = {
  'damage': 50,
  'name': 'dagger of mischief',
  3: False,
  ...
}
```

To delete a key-value pair from the dictionary, use `del d[key]`. For example, calling `del weapon[3]` on the previous dictionary will make the weapon dictionary revert to its original form.


# Lesson 2

In this lesson, we will touch on loops, if statements and functions! To do so, we need to understand the concept of 'code blocks'. Python does code blocks using indentation (the Tab key on your keyboard) - all code in the same block are on the same indent line. Code blocks determine the 'scope' in which code runs:

```
this is one
code block because
all the code has no indent
  but this is now
  a second code block
```

Python will throw an error if you try to run a file that is improperly formatted! The error will usually complain about code not being on the correct indentation line. Now, we are ready to jump into loops and functions - both of which have a code block!

### Loops
Loops make it easy to work with large amounts of data that you don't want to go through individually! For example,

```
l = [1, 2, 3]
for x in l:
  print(x) # This here is the for loop's code block!
```

Basically, a for loop loops (iterates) through an 'iterator', in this case a list, and assigns each element of the list to a variable name (in this case `x`). Then it runs the code block with the element as `x`! This is repeated for all elements in the list. Simple :)

This simple for-loop will print `1` and then `2` and then `3` in order.

Sometimes, you might require to iterate a certain number of times rather than iterate over the elements of a list. For example, if I wanted to draw an object 100 times, I can do the following:

```
for i in range(100):
  do_something()
  do_something_else()
  draw_object()
```

The `range(n)` function produces a list-like object that you can think of as being `[0, 1, 2, 3, ... n-1]` and it has `n` number of elements. This allows us to call the `draw_object()` function 100 times! This is also useful for iterating through a list using its indices, for example:

```
l = [1, 2, 3]
for i in range(len(l)):
  print(l[i])
```

This loop as the same effect as the first loop I showed you - it prints the elements of l out in order.

### Functions
Sometimes you have a piece of code that you want to pull out and make it reusable. Welcome to functions!

Functions have the syntax:
```
def <function_name>(argument1, argument2, ...):
  # Function body, notice it is on a new code indent
  return final_answer
``` 

Notice that the entire function body is on its on code block. This is how Python knows what code belongs to the function!

Functions will always return something. If your return statement is not specified, it returns a special value `None`. However, it is good practice to try and make it return something! In this case, this function returns whatever value is associated with the variable `final_answer`.

To demonstrate the power of functions, if I had the following code which gives me a new list `l2` with elements each 1 larger than the corresponding element in `l1`:

```
l1 = [1, 2, 3]
l2 = []
for x in l1:
  l2.append(x + 1)
```

I could make this functionality reusable for different l1 like so:
```
def increment_elements_by_1(l):
  new_list = []
  for x in l:
    new_list.append(x + 1)
  return new_list

l2 = increment_elements_by_1([1,2,3])
```
Now, I can pass the function **any** list and it would give me (return) a new list with all elements incremented by 1. Dandy :)

### If Statements

In code, it is oftentimes the case that you want to 'do this if something is true, otherwise do something else'. This is called an if-statement.

```
if check_1:
  do_something()
elif check_2:
  do_something_else()
else:
  default_to_something()
```

In the above example, `check_1` and `check_2` are both **booleans**, which if you can recall are either `True` or `False`. You can read the line of code in your head as follows: If `check_1` is `True`, then run the function `do_something()`, else if `check_2` is `True`, run the function `do_something_else()`, otherwise, run the function `default_to_something()`.

Notice how code blocks are used here - all code are indented the same under the if statement to indicate to Python that they should be run if the condition above it holds.
