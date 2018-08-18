
# Introduction to Linux

<span style="color:#D3D3D3">Author: Xing Yu</span>

Linux is a very powerful and widely used type of operating system, which we will use to learn programming in I101. The i101appliance is basically a customized Ubuntu Linux operating system\(a flavor of Linux\). And we introduce the basics and command techniques in this introduction.

## 1. A non-graphic user interface

In i101appliance, we have a graphic user interface(GUI) called [xfce](https://xfce.org). It is light weight GUI and very intuitive to use. Since the point and click paradigm is very similar to Windows/MacOS.

But we will, for most of our time, use a non-graphic user interface for our programming tasks. It is called terminal.

### Terminal

If you go to `Menu` > `Terminal Emulator`, a window will pop up with a line of words that doesn't seem to make much sense as below

```bash
i101@i101:~$
```

And this window, which we will call `terminal` will be our main way to communicate with the computer this semster. So we will need to learn how to talk to it. And you will see a little invest of your time will help you go a long way in the future.

Now first, let's make one thing very clear. You will only be able to use your keyboard to interact with the terminal. Your mouse is useless. So don't try to click and select a word to delete. Instead, use your arrow keys on your keyboard to move your prompt and use backspace to delete.

Now let's try to understand how the terminal works. The terminal is pretty much like a dialog window that you can talk to the computer. However, you cannot use plain english. Instead, you will learn the commands that the computer could understand and execute. 

Let's take a look at the strange line `i101@i101:~$`. It has three parts. The first `i101` is you, or your username on this machine. It can be your name or anything you would like. But in i101appliance, we set it to be the same `i101`. The second `i101` is the name of the machine\(or the operating system, since we are running a virtual machine\). So together `i101@i101` means the user `i101` is on the machine `i101`. Your may see it in any other place like `Bob@office-desktop`, which means `Bos` is logged in on the computer `office-desktop`. 

The the semicolon following `i101@i101` is a seperator. And the information that following it shows what is going on in this machine. You see a wave line `~` first after the semicolon. It says that, currently, you are in your home folder \(strange, isn't it?\). We will explain it in the next section in more details. Right now, you just need to remember that `~` means your home folder. And for each user on a machine, they have their own home folders. For example, `Bob@office-desktop` and `Lily@office-desktop` will each have a home folder of their own so they can save the files in different places each through they share a computer. That is why Linux is a multiuser operating system.

The last part `$` is just a prompt, which is the computer's way of saying: "Hi, I'm ready for any instructions!"

So let's try to give some command to the computer.

```bash
i101@i101:~$whoami
i101
```

The command `whoami` is short for "who am I?", which asks the computer what is my username. The next line is the username `i101`, which is no surprise there.

Now let's try something that will give us more usefull information.

```bash
i101@i101:~$date
Mon Jul 16 17:27:35 EDT 2018
```

We use the command `date` to ask for the date and time information.

Now the last example is fun, but you will have to make sure that your computer is connected to the Internet before run it. 


```bash
i101@i101:~$telnet towel.blinkenlights.nl
```

Now you can layback and enjoy the show\(LOL\).

### Navigate using the terminal

Now that we had our movie time wrapped up, let's learn something basic as how to navigate your computer using terminal instead of your mouse.

#### 1. File structure of the Linux system

First, let's start calling folders directories, which is the term we are going to use. And there is a hierarchy of directories for Linux operating systems. You can think of it as a tree, and the root is the user directory for each username, which is represented as `~`.

If you open a new terminal window and type the command `pwd` (short for print working directory). You will see the following:

```bash
i101@i101:~$pwd
/home/i101
```

The result tells you where you are currtly. And `/home/i101` says that you are in the folder `i101`, which is in the folder `home` on this computer. And there is not a parent folder for the `home` folder. And the `home` folder is just on your hard disk. This is called a <span style=color:green>path</span> to your folder. And the path showed above is an absolute path, which gives you the full path from the hard disk.

Note that the `i101` folder is the home folder for the user `i101`. And the `home` folder that contains the `i101` folder is a folder for all users on this computer. The naming is a little bit confusing. But just remember that your home folder is `i101`, for now.

There is a `home` folder on your desktop, which is a link to the `i101` folder. So if you click to open it, your will see several folders already created for you. Now if you open a terminal window and type `ls`, which means list the content under the currently directory. You will see the same set of folders, only not in graphic.

So try to understand that the graphic user interface and the terminal are both a method to interact with the content on your computer. One is based on point and click and the other is based on typing commands.

#### 2. Navigate the computer

Okay, now we have a general idea of the directory, how do we navigate? 

We will use our tree metaphor here. Remember that you can use `pwd` to print out where you are. We will call the current directory the current node that you are at. And remember that you can use `ls` to list everything under the current directory. And we will call them the child nodes of current nodes. So we can go from current node to its child nodes. The command that we need is `cd`, short for "change directory". 

```shell
i101@i101:~$cd Documents
i101@i101:~/Documents$
```



Notice how the current directory `~` changed to `~/Documents`. That shows you are now in the `Documents` folder. If there are child folders in `Documents`, you can use `cd` again to move to the child node.

Let's take a look at the command `cd`. The example aforementioned is `cd Documents`. This is a typical way to give a command. First we call the name of the command, which is `cd`. Then we give the parameters that command needs, which is `Documents` or other folder names. We separate the command and the parameter with a space. So a general form of commands is `commandname parameters`. And we will see other examples later on.

Now you may wonder, how can I go to the parent node instead of the child nodes? There might be several child nodes for a node. But there is always one parent node. So there is a symbol to represent parent node, which is `..`. The double dots represent parent node. You can use it as `cd ..` to go back to the parent directory.

Sometimes, you will lost track of you path. Or you just want to go back to where it all begins. You can use ``cd ~`` to go back to your home folder\(notice that `~` represents home folder of the current user\).

#### 3. Create/Delete folders

As we now learned how to navigate, let's create new folders so we can organize our files.

```shell
i101@i101:~$cd Desktop
```

We first go to our `Desktop` folder.

```shell
i101@i101:~/Desktop$mkdir myFolder
i101@i101:~/Desktop$cd myFolder
i101@i101:~/Desktop/myFolder$
```

Then we use the command `mkdir` \(make directory\) to create a folder called `myFolder`. Notice the `commandname parameters` pattern here. Then you can use `ls` to list everything under `Desktop` and you will see your folder created. You can use `cd myFolder` to go to that folder, which will be empty at this point.

Let's learn how to delete the folder we just created. One thing to keep in mind is that <span style=color:red>you can only delete a node when you are at its parent node</span>. In other words, if you want to delete `myFolder`, you need to first navigate to `~/Desktop` where `myFolder` exists. But we already know how to do that, right?

```shell
i101@i101:~/Desktop/myFolder$cd ..



```

Now we are in the parent directory, and we can delete the folder as follows.

```sh
i101@i101:~/Desktop$rm -r myFolder
```

The command `rm` is short for remove. But we see something new in this line of command. We already know that `rm` is the commandname and `myFolder` is the parameter. What is the `-r` part? It is call an option for this command `rm`. Typically a option starts with a dash `-`. In this case `-r` means recursive. So in english, the command `rm -r myFolder` means recursively remove everything contained in the folder `myFolder` and then remove the folder.

#### 4. Other common commands

There are a lot of commands. But over time you will learn and get better with them. So don't worry. The belowing are some common commands that will be very helpful. And it would be great to play with them a little bit.

1. `man [commandname]` show the mannual of a command
2. `ls -l` list everything in a list form
3. `mv [file] [destination]` mv a file/folder to a new place
4. `python3 [.py file]` run a python 3 program

## Summary



As long as you have learned how to navigate, create, delete, and execute programs, you will be able to learn a lot more on your own. And there are a lot of good references online where you can pick up new stuff. And it would pay off since the terminal would let you do a lot of things easier. For example, `rm *.txt` will delete all text files in current directory so you don't have to select them one by one and click delete button.

Here is a link to a [cheatsheet](https://files.fosswire.com/2007/08/fwunixref.pdf). It is very helpful for beginners. So print it out and put it where you can see on your desk to help you save time while coding.
