# Learn the Basics
>> Introduction

What is Bash ?
Bash is the shell, or a command language interpreter, For the GNU operating system.[You can think of GNU has an extensive collection of free software(383 packages)which can be used as an operating system or can be used in parts with other os's].

It is acronym for the 'Boune-again-shell' . Stephen Bourne is the author of these command language.

Bash is largely compatible with sh and incorporates useful features from Korn shell "ksh" and the c shell "csh" .

It offers functional improvements over "sh" for both interactive and programming use.

While the GNU os provides other shells, including a version of "csh" , bash is the default shell.

Like other GNU software, Bash is quite portable. It currently runs on nearly every version of Unix and a few other operating systems-independently supported ports exists for MS-Dos, OS/2 and windows platforms.


well, from quite sometime you are speaking about shell, what exactly is shell ?
what is shell ?
At its base, a shell is simply a macro processor that executes commands. The term macro processor means functionality where text and symbols are expanded to create larger expressions.

A unix shell is both a command interpreter and programming language. As a command interpreter, the shell provides the user interface to the rich set of GNU utilitites.the programming language feature allows these utilities to be combined. Files containing commands can be created and become command themselves. These new commands have the same status as system commands in directories such as /bin. allowing users or groups to establish custom environments to automate their common tasks.

shells may be used interactively or non-interactively. In interactive mode, they accept input typed from keyboard. when executing noninteractively , shells execute commands read from a file.

A shell allows execution of GNU commands, both synchronously and asynchronously. The shell waits for synchronous commands to complete before accepting more input. Asynchronous commands continue to execute in parallel with the shell while it read and executes additional commands.

The redirection constructs permit fine-grained control of the input and output of those commands. Moreover, the shell allows control over the contents of commands environments

shells also provide a small set of built in commands(builtins) implementing functionality impossible or inconvenient to obtain via separate utilities. for ex: cd, break, continue, and exec cannot be implemented outside of the shell because they directly manipulate the shell itself.

While executing commands is essential, most of the power (and complexity) of shells id due to their

embedded programming languages. Like any high-level language, the shell provides variables, flow control constructs, quoting and functions.

shells offer features geared specifically for interactive use rather than to augment the programming language. These interactive features include job control, command line editing, command history, and aliases

**Hello, World!**

Shell programming can be accomplished by directly executing shell commands at the shell prompt or by storing them in the order of execution, in a text file, called a shell script, and then executing the shell script. To execute, simply write the shell script file name, once the file has execute permission (chmod +x filename).

The first line of the shell script file begins with a "sha-bang" (#!) which is not read as a comment, followed by the full path where the shell interpreter is located. This path, tells the operating system that this file is a set of commands to be fed into the interpreter indicated. Note that if the path given at the "sha-bang" is incorrect, then an error message e.g. "Command not found.", may be the result of the script execution. It is common to name the shell script with the ".sh" extension. The first line may look like this:

#!/bin/bash

Adding comments: any text following the "#" is considered a comment

To find out what is currently active shell, and what is its path, type the highlighted command at the shell prompt (sample responses follow):

ps | grep $$

987 tty1 00:00:00 bash

This response shows that the shell you are using is of type 'bash'. next find out the full path of the shell interpreter

which bash

/bin/bash

This response shows the full execution path of the shell interpreter. Make sure that the "sha-bang" line at the beginning of your script, matches this same execution path.

Exercise
Use the "echo" command to print the line "Hello, World!".



Variables

Passing Arguments to the Script

Arrays

Basic Operators

Basic String Operations

Decision Making

Loops

Array-Comparison

Shell Functions

# Advanced Tutorials

Special Variables

Bash trap command

File Testing

Input Parameter Parsing

Pipelines

Process Substitution

Regular Expressions

Special Commands sed,awk,grep,sort

![image](https://user-images.githubusercontent.com/89054489/233785186-5a2ce6da-80be-4d3e-89b0-63020be828ca.png)

## Learning Resources for free
[Linux Shell Scripting Tutorial web](https://bash.cyberciti.biz/guide/Main_Page)

[Interactive shell script learning](https://www.learnshell.org/)
