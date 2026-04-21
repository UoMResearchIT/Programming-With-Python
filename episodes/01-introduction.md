---
title: Python Basics Recap
teaching: 0
exercises: 0
---

::::::::::::::::::::::::::::::::::::::: objectives

- Understanding key concepts in Python

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- Python Refresher

::::::::::::::::::::::::::::::::::::::::::::::::::

This course follows on from the python introduction course. To ensure that we are starting from similar positions, there follows a short multiple choice quiz on key python concepts that we will be building on through this course.

## Variables and Lists

::::::::::::::::::::::::::::::::::::: challenge

### 1\. Assigning a value to a variable

We wish to store the string `Cat` as a value in the variable `animal`, which of these lines of code will do this for us?

1. `animal = 'Cat'`
2. `animal = Cat`
3. `Cat = animal`
4. `animal(Cat)`

:::::::::::::::  solution

Answer 1 is correct

:::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: challenge

### 2\. Assigning values to a list

We wish to create a list of values, which of these lines of code is valid to do this?

1. `varlist = [34, 57, '2d']`
2. `varlist = (12, 'vr', 95)`
3. `varlist = 'xcf', 12, 97`

:::::::::::::::  solution

Answer 1 is correct

:::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: challenge

### 3a. Indexing characters in a string

Lists and strings both contain multiple indexed values (in the case of strings these are specifically individual characters rather than other values). If we have a variable `animal` which contains the string `penguin`, which of these options will print the first character (`p`) for us?

1. `print(animal[0])`
2. `print(animal[1])`
3. `print(animal['p'])`

:::::::::::::::  solution

Answer 1 is correct

:::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: challenge

### 3b. Indexing characters in a string (slicing)

We can also select whole sections of lists and strings, not just single elements. Using the same variable `animal`, containing the string `penguin`, as above, which of these options will print the last 2 characters for us? (Note that there is more an one correct answer)

1. `print(animal[5:])`
2. `print(animal[6:])`
3. `print(animal[6:7])`
4. `print(animal[5:7])`
5. `print(animal[-2:])`
6. `print(animal[:-2])`

:::::::::::::::  solution

Answers 1, 4, and 5 are correct

:::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::

## Loops

::::::::::::::::::::::::::::::::::::: challenge

### 4\. Constructing a `for` loop

Please write a simple `for` loop which will print out each of the characters in the `animal` variable one at a time.

:::::::::::::::  solution

```python
for char in animal:
    print(char)
```

:::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::

## Software Modules

::::::::::::::::::::::::::::::::::::: challenge

### 5\. Loading new functions

We want to use the functions in the `numpy` library in our code. How do we open this library in our code?

1. `import numpy`
2. `load numpy`
3. `open numpy`

:::::::::::::::  solution

Answer 1 is correct

:::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::

## If statements and conditionals

::::::::::::::::::::::::::::::::::::: challenge

### 6\. Conditionals

Which of these conditional tests returns a `True` result?

1. `4 > 3`
2. `'a' != 'b'`
3. `6 >= 6.0`
4. `'3' == 3`
5. `3 > 'c'`

:::::::::::::::  solution

Answers 1, 2, and 3 return `True` results. 4 returns `False`. 5 raises an Error.

:::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: challenge

### 7\. If statements

What is printed when this `if` statement is used?

```python
if 4 > 5:
    print('A')
elif 4 <= 5:
    print('B')
elif 4 < 5:
    print('C')
else:
    print('D')
```

1. `A`
2. `B`
3. `C`
4. `B` and `C`
5. `D`
6. `A` and `D`

:::::::::::::::  solution

`B`. Both `4 <= 5` and `4 < 5` would return a `True` result, but the `if` statement is exited as soon as the `True` result is returned.

:::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::  callout

## Formatting Variables and Objects in Strings

Throughout this course, we will be printing the values of variables inside strings to demonstrate what the code does. There are a number of ways to this in Python; in this course we will be using `f-strings` which are the recommended string interpolation syntax from version 3.6 onwards.

To use `f-strings` simply start a string literal with `f` or `F`, then embed whatever you want interpolating into the string within curly braces `{}`:

```python
two_int = 2
two_str = "2"
f_string = f"{two_int} + {two_str} = {2 + 2}"
print(f_string)
```
```output
2 + 2 = 4
```

Numerical values can be formatted using `:` inside the curly braces. For example, an integer `i` can be made to have a width `n` using `{i:nd}`, or `{i:0nd}` to pad it out with zeros:

```python
print(f"One with four leading spaces {1:5d}")
print(f"One with four leading zeros {1:05d}")
```
```output
One with four leading spaces     1
One with four leading zeros 00001
```

Floating point variables can have their precision specified with a number after a decimal point and an `f`:
```python
pi = 3.141592653589793
print(pi)
print(f"pi to three decimal places is {pi:.3f}")
```
```output
3.141592653589793
pi to three decimal places is 3.142
```

Or made to use scientific notation with an `e`:

```python
print(1e9)
print(f"A billion in scientific notation is {1e9:.1e}")
```
```output
1000000000.0
A billion in scientific notation is 1.0e+09
```

This is only scratching the surface of what you can do with `f-strings`, they are often the most powerful and concise way to format variables inside strings. However, there are occasions when other methods are preferable, and you should be careful using them with Python [before version 3.12](https://realpython.com/python-f-strings/#upgrading-f-strings-python-312-and-beyond).

To learn more, see: [Python f-strings](https://realpython.com/python-f-strings/).

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::  callout

:::::::::::::::::::::::::::::::::::::::: keypoints

- variables
- lists
- indexing
- loops
- conditionals
- string formatting

::::::::::::::::::::::::::::::::::::::::::::::::::


