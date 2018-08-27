---
title: 'Python Controls'
date: 2018-08-26
permalink: /posts/2018/08/pythoncontrols/
tags:
- category1
- category2
---

<span style="color:#D3D3D3">Author: Xing Yu</span>

In the last tutorial, we talked about basic data types and operators in python. However, a programming language won't be helpful without controls, which alows programmers to create programs that could theoretically carry out any computations. In this tutorial, we will introduce `loop` and `condition`, which are basical controls that make a programming language [Turing complete](https://en.wikipedia.org/wiki/Turing_completeness).

## Turing Completeness

Before the computers that we see everywhere nowadays were invented, defferent machines were created for different kind of computations. For example, in order to do `addition` and `division`, two different machines must be made. However, it is expensive to create a machine to just carry out one type of computation. Ideally, it would be great to have one machine that could do any kind of computation. This idea was first introduced by [Alan Turing](https://en.wikipedia.org/wiki/Alan_Turing). And the idea is called a Universal Turing Mahince.

Python is a programming language that is Turing complete, which means it can do all kind of computation. And the controls `loop` and `condition` are the building blocks. So we will take a good look at them in this post.

## Loop

Think of `Loop` as our way to as computers to do repeating tasks, which is quite common in computing. Let's see a toy example of loop to get a general idea.

```python
# assuming you are playing hide and seek
# and you need to count from 1 to 100 before you set off

count = 0

while count <= 100:    # while statement with termination condition
    count += 1         # part of the while loop
    print(count)       # part of the while loop
```

This simple example initiates a variable `count` as integer with the value 0. The variable got updated for 100 times with an increment of 1 at each time. And the result of each update is printed to the screen.

As simple as the example may seem, there are several caveats that we need to stress on:

1. Indentations: Notice that we used indentations for the two lines of code after the `while` statement. This is the python way of creating 'blocks' of code. In this case, we created a `while` loop block. Notice that there is a colon after the first line. It is us tell the computer that we are starting a block. And all the lines of code within the block, which we specified by adding an indentation, will be executed at each iteration of the loop. Now think about it, what would be the output if we didn't add an indentation in front of the second line `print(count)`?

2. Termination condition: Pay attention to the line that immediately follows the `while` statement. We will refer to it as the termination condition. It tells the computer when the `loop` should end. If this condition is not satisfied or missing, the loop will go on for ever, which is called in infinit loop. So think about it, what would happen if we remove the line `count += 1`? What would happen? And why?

What we just saw is call a `while loop`. There is another 'flavor' of loops in python, which is called a `for loop`. Let's take a look at how it works.

```python
for each in range(1, 101):    # the function range(a, b) generates ints from a to b - 1
    print(each)
```

This much shorter code will do exactly the same as out first example. Once you understand how it works, you will realize how powerful and intuitive it is. 

First, we see a new built-in function [`range(a, b)`](https://www.pythoncentral.io/pythons-range-function-explained/). It is very commonly, if not the mostly, used function in python. It generates a list of integers between two give values that specify the range of the integers. Notice that the first value is inclusive and the second is not. 

Second, we created a local variable (we will talk more about this when we introduce functions) called `each` that will be assigned with each of the integers in the generated list (an intuitive name, right?). And we print `each` at each iteration.

## Condition

Besides `loop`, another type of control is `condition`. Let's see an example first:

```python
# print all even numbers that are less than 10

for i in range(1, 10):
    if i % 2 == 0:
        print(i)
    else:
        continue
```

This piece of code is very straitforwad. For each number less than 10, we check if the number can be divided by 2. If that is the case, we print the number, else, we continue our loop.

Let's think of `loop` and `condition` from a high level to understand how they work. Let's assume a computer is a black box that could process an input. However, we can have different states during the process. So the `loop` statement is used to make the black box iterate over all inputs. And `condition` statements decide what state of the black box it should be (to print or to pass).

## Summary

This posting gives a basic introduction of `loop` and `condition` statements. Read chapter 3, 5 in the [book](https://www.pythonlearn.com/html-270/) for more details.
