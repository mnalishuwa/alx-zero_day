# Foundations 1 
## Upcoming Projects/Concepts
### 0x00-Shell Basics 8 February 2023
**1. The Shell**
The shell is an environment or special program that provides an interface
for a user to use *operating system* services. It sits on top of the *kernel*
and takes commands from the keyboard, the kernel is the heart of the OS,
it sits on top of the hardware and effectively controls all tasks of the system. The kernel translates commands it receives into machine language,
the hardware the executes commands received.

**2. Navigation**
OS has a hierarchical directory structure (tree structure with first directory as root which contains files and subdirectories).
Useful navigation commands:
`code`pwd`code` - print working director (current directory) name
`code`ls`code` - list contents (files and folders) of directory
`code`cd`code` - change working directory
`code`less`code` - view contents of a text file
`code`file`code` - classify a file contents (display type of the type of the file)

Refer to [linux folders](http://linuxcommand.org/lc3_lts0040.php) for a description of common directories.

**3. Commands**
Commands are effectively keywords that are recognised by the shell, that
when called execute an executable program or function. They can be an
executable program, built into the shell, a shell function, or an alias
(a custom command built from other commands).

The commands below are typically used other commands to get more details
about the commands.

`code`type`code` - Display information about command type
`code`which`code` - Locate a command, only works for executable programs
`code`help`code` - Display reference page for builtin
`code`man`code` - Display an on-line command reference

**4. Shebang #!**
A character sequence consisting of `code`#!`code` at the beginning of
the character sequence, when a text file with shebang is used as if it is an executable in a Unix-like operating system, the program loader mechanism parses the rest of the file's initial line as an *interpreter directive*.

For example, if file `code`/bin/A`code` is an executable in *ELF* format, and
file `code`/bin/B`code` contains the shebang `code`#!/bin/A operator_parameter`code` and file `code`/bin/C`code` contains the shebang `code`#!/bin/B`code`, then
executing file `code`/bin/C`code` resolves to `code`/bin/B /bin/C`code` which
then resolves to `code`/bin/A operator_parameter /bin/B /bin/C`code`.

Some typical shebang lines:
     -`code`#!/bin/sh`code` - Execute using the *[Bourne Shell](https://en.wikipedia.org/wiki/Bourne_shell)* or compatible shell assumed to be in */bin* directory.
     -`code`#!/bin/bash`code` - Execute using the *Bash shell*
     -`code`#!/usr/bin/pwsh`code` - Execute the file using *PowerShell*
     -`code`#!/usr/bin/env python3`code` - Execute with a Python interprester, using the env program search path to find it.

Refer the the [Shebang Wiki](https://en.wikipedia.org/wiki/Shebang_%28Unix%29) for more details.

Interpreter directives allow scripts and data files to be used as commands, hiding the details of their implementation from users and other programs, by removing the need to prefix scripts with their interpreter on the command line.



