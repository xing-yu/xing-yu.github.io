---
title: 'Introduction to python'
date: 2018-08-01
permalink: /posts/2018/08/Introduction/
tags:
  - category1
  - category2
---

# Introduction to Python

<span style="color:#D3D3D3">Author: Xing Yu</span>

Python (version 3 or later) is the main programming language that we will learn and use in I101. Python is a interpretive language that doesn't need to be compiled before running. Its grammar is relatively intuitive. And it is a very popular programming language used in informatics and computer science. This tutorial is a start point for you to get familar with programming in general.

## The "Hello World" example

Conventionally, we will start with a simple "Hello world" example, which is a simple program that prints out "Hello world!" on the computer screen. The reason for this is because it is the very [first program](https://blog.hackerrank.com/the-history-of-hello-world/) ever to test a system is working. And we will honor the tradition here:

### List of actions to write your first program

1. Choose a text editor
2. Use the text editor to write code
3. Save the code to a file
4. Run the file using the python interpreter

#### 1. Choose a text editor

A text editor is your main tool in programming. We have a built in text editor [gedit](https://wiki.gnome.org/Apps/Gedit) in the I101appliance. If you want to program on your local operating system, you can also try to install a text editor of your own choice. The popular ones are [Sublime text](https://www.sublimetext.com), [atom](https://atom.io), [notepad](https://notepad-plus-plus.org)\(only for windows OS\). Pick, download, and install whichever one you like and you can start programming.

#### 2. Use the text editor to write code

Now fire up the text editor and start typing, just like typing a report in a word document. However, you need to pay attention to "tabs" and "spaces" that you are using\(we will explaing more about this later\). Your first program should look like below.

```python
print("Hello world!")
```

Our first program just have one line\(simple, right?\). But you need to pay attention to not add any "spaces" or "tabs" at the beginning of the line.

#### 3. Save the code to a file
Now that we have finished the programming, we want to save the code and run it. Click the save button in the text editor. A dialog window should pop up and ask you to give the program a name. We will call it <span style="color:red"><b>hello.py</b></span>. Note that the extension <span style="color:red"><b>.py</b></span> tells everyone that it is a python program file. Just like <span style="color:red"><b>.doc</b></span> represents a word file.

In this tutorial, we will save the file on desktop.

#### 4. Run the file using tthe python interpreter

Now we have written and saved the program, we want the computer to run it. To do that, we need a python interpreter, which acts as a translator that will "translate" our program into binary code that a machine could read and understand. Luckily, there is a python interpreter that is already installed in the I101appliance\(we will introduce how to install a python interpreter on your local operating system later so you can program without the I101 appliance\).

Let's open the "terminal emulator"\(we introduced the terminal in more detail when we introduce the basics of linux systems\). And you will see the following

```bash
i101@i101:~$
```

Recall that the line `i101@i101` means that we have a user named `i101` that logged in `@` the system named as `i101`, and the prompt `~$` indicates that the system is ready to take your orders.

To run our program, we need to first locate it. Hence, we will navigate to the folder, which is `Desktop`, that we save the file. We can use `cd` to do that:

```bash
i101@i101:~$cd Desktop
```



Now the prompt will change to `i101@i101:~/Desktop$`, indicating that we are already in the `Desktop` directory. Use the `ls` command to list all files\/folders in current directory:

```bash
i101@i101:~/Desktop~$ls
hello.py
```

We can see the program <span style="color:red"><b>hello.py</b></span> that we saved here earlier. To run the program, we call the interpreter and pass our program to it as follows:

```bash
i101@i101:~/Desktop~$python3 hello.py
Hello World!
```

And the screen prints out `Hellow World!`! Congrats! Your just wrote and ran your very first program!

## Summary

This tutorial introduced how you can write and run a python program. There are several key concepts you need to understand:

1. A program is a file of codes that you write.
2. To run the program, you need a interpreter to interpret your code into binary codes so the machine could understand.
3. You will need to pass your code file to the python3 interpret(note the 3 at the end, represents that we are using python ver3 or later) to run. To do that we will use terminal emulator.
