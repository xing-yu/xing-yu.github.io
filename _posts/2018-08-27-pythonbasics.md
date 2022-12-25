---
title: 'Python basics'
date: 2018-08-27
permalink: /posts/2018/10/pythonbasics/
tags:
- category1
- category2
---

<span style="color:#D3D3D3">Author: Xing Yu</span>

After seeing the `Hello World!` example, it is time to do some coding yourselves. In this tutorial, we will go through the basics of python systemetically. 

We will cover:

1. Basic data types
2. Operators for computation
3. Coding style

## Basic data types

Where programming, we typically follow a pattern like below:

Get a value >> do some computation >> output the new value

The pattern is simple, however, most complex programs can be broken down into a combination of the patterns. So we need a way to store values. In programming, we need to create a variable to store values first. It is called a variable because the value it contains can change\(that may not be true for all the time, but let's think of it that way now\).

There are different types of values. The basic types are integers, characters, strings, and float numbers. Each of them takes different amount of storage space on your computer's memory. Hence, a variable usually has a type so it can only store values that has the same type. This is how a static programming language would do. For example, if you program in `C`, the creation\(declaration\) of variables would look like something below:

```C
int x = 11
float y = 0.5
char z = "h"
```

And you cannot assign a value of different type to a variable. For example, the following is not allow in `C`.

```C
int x = 0.5
char z = 11
```

These examples show you how a variable is created conventionally. But the good news is we are learning Python, which is a dynamic programming language. Which means that you don't have to worry about the types of variables as the language will infer it by itself. So in python you can do the following:

```Python
x = 11
y = 0.5
z = "h"
```

See, all you have to do is to give the variable a name and a value to store. And you can also change the values how ever you like \(The symbol `#` is used to denote comments in python\).

```python
x = 11    # create a variable x of integers
x = 0.99  # give a float number to x
z = "h"   # create a variable z of characters
Z = 66    # assign an interger to z
```

Now let's see where common data types we have in python. The mostly used types in programming are integers, float numbers, characters, strings, and boolean. A boolean var\(short for variables\) can only has two values: True of False. Let's see some examples:

```python
storeIsOpen = True
downloadIsFinished = False
```

As you can see, the naming of a variable is up to you. But it is a programmer's responsibility to make a variable's meaning clear. A usually way to do is using camel case like what we did with `storeIsOpen`. It adds to the readability of the code.

## Operators for computations

Now let's see some examples of computations that you can do after creating variables. 

```python
a = 5
b = 3

add = a + b # result will be 8
diff = a - b # result will be 2
multi = a * b # result will be 15
quo = b / a # result will be 0.6
```

The arithmetcs computations shows a pattern: you will create a new var to store the result of each computation. 

Besides the basic arithmatics, python has other operators that are commonly seen in other programming lanuages.

```python
x += 1 # increament x by 1
x -= 1 # decreament x by 1
x *= 2 # multiply x by 2
x /= 4 # divide x by 4

x ** 2 # x to the power of 2
x // 2 # x divided by 2 and only return the integer part
```

It would be a good idea to open the python interpretor in the interactive mode to test all these operations by yourself.

## Coding Style

Each person writes code differently. But a good coding style is important for you so we briefly introduce some helpful tips right now.

First, indentations are important in writing python code. We will cover more of it when we introduce `loop` and `if elfs` statements. But for right now, you need to keep in mind that indentations are used to write a block of lines that relates to each other. So you shouldn't use indentation while you are writing a line of code that can be executed independently.

Second, an indentation is 4 spaces. If you are using a text editor such as [Atom](https://atom.io), you can use the `tab` key, which is set to be 4 spaces in common. But don't mix using the `tab` key and the `space` key together, which would lead the program to fail.

Third, write comments as often as you could. You may already noticed that the symbol `#` is used to specify a comment, which will be ignored by the python interpretor.

Fourth, try to make your code clear and easy to read by giving intuitive names to the variables.

```python

# example NO.1

qty = 10 # quantity

rate = 30 # price

total = qty * rate

```

```python

# example NO.2

a = 10
b = 30
c = a * b
```

Take a look at the two examples above. Example 1 is more intuitive than example 2 with that proper naming of variables and comments. Also, it is easier to maintain and debug in the long run. We will talk more about good programming practice later on.

## Summary

This tutorial introduced us to the very basics of python. We now have a basic understanding of basic data types and operators. And we also talked about good coding style. 
