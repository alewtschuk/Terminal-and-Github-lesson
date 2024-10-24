# Introduction to Basic Terminal Commands in Bash

Welcome to this introductory lesson on using the terminal! By the end of this lesson, you will learn how to navigate the file system, manage files and directories, and use some fundamental commands.

## Table of Contents

1. [What is the Terminal?](#what-is-the-terminal)
2. [Opening the Terminal](#opening-the-terminal)
   - [For Windows Users (Using WSL)](#for-windows-users-using-wsl)
   - [For macOS Users](#for-macos-users)
3. [Understanding the Command Prompt](#understanding-the-command-prompt)
4. [Basic Commands](#basic-commands)
   1. [pwd - Print Working Directory](#1-pwd---print-working-directory)
   2. [ls - List Directory Contents](#2-ls---list-directory-contents)
   3. [cd - Change Directory](#3-cd---change-directory)
   4. [mkdir - Make Directory](#4-mkdir---make-directory)
   5. [touch - Create a New File](#5-touch---create-a-new-file)
   6. [cp - Copy Files and Directories](#6-cp---copy-files-and-directories)
   7. [mv - Move or Rename Files and Directories](#7-mv---move-or-rename-files-and-directories)
   8. [rm - Remove Files and Directories](#8-rm---remove-files-and-directories)
   9. [cat - Concatenate and Display Files](#9-cat---concatenate-and-display-files)
   10. [echo - Display a Line of Text](#10-echo---display-a-line-of-text)
5. [Understanding File Paths](#understanding-file-paths)
6. [Redirection and Pipes](#redirection-and-pipes)
7. [Getting Help](#getting-help)
8. [Practice Exercises](#practice-exercises)
9. [Conclusion](#conclusion)
10. [Additional Resources](#additional-resources)

## What is the Terminal?

The terminal is a text-based interface that allows you to interact with your computer by typing commands. It provides direct access to the operating system’s functions.

## Opening the Terminal

### For Windows Users (Using WSL)
- Press Win + R, type wsl, and press Enter.
- Alternatively, search for “Ubuntu” (or your chosen Linux distribution) in the Start menu.

### For macOS Users
- Open Terminal from Applications > Utilities.
- Or press Command + Space, type Terminal, and press Enter.

## Understanding the Command Prompt

When you open the terminal, you’ll see a prompt that looks something like this:

```
username@computername:~$
```
- `username` is your user name.
- `computername` is the name of your computer.
- `~` represents your home directory.
- `$` indicates that you’re a regular user (not an administrator).

## Basic Commands

### 1. pwd - Print Working Directory
Displays the full path of the current directory you’re in.
```bash
$ pwd
/home/username
```

### 2. ls - List Directory Contents
Lists files and directories within the current directory.
```bash
$ ls
Documents  Downloads  Music  Pictures  Videos
```
- **Options:**
  - `ls -l`: Detailed list with permissions, sizes, and modification dates.
  - `ls -a`: Includes hidden files (those starting with `.`).

### 3. cd - Change Directory
Navigates between directories.
```bash
$ cd Documents
```
- **Special Shortcuts:**
  - `cd ~`: Go to your home directory.
  - `cd ..`: Move up one directory level.
  - `cd -`: Go to the previous directory.

### 4. mkdir - Make Directory
Creates a new directory.
```bash
$ mkdir new_folder
```

### 5. touch - Create a New File
Creates an empty file or updates the timestamp of an existing file.
```bash
$ touch new_file.txt
```

### 6. cp - Copy Files and Directories
Copies files or directories.
```bash
$ cp source.txt destination.txt
```
- **Copy a directory:**
```bash
$ cp -r source_folder/ destination_folder/
```

### 7. mv - Move or Rename Files and Directories
Moves or renames files and directories.
- **Rename a file:**
```bash
$ mv oldname.txt newname.txt
```
- **Move a file to a directory:**
```bash
$ mv file.txt /path/to/destination/
```

### 8. rm - Remove Files and Directories
Deletes files or directories.
- **Remove a file:**
```bash
$ rm file.txt
```
- **Remove a directory and its contents:**
```bash
$ rm -r folder_name/
```
**Warning:** Use `rm` carefully. Deleted files are not sent to the Recycle Bin and cannot be easily recovered.

### 9. cat - Concatenate and Display Files
Displays the contents of a file.
```bash
$ cat file.txt
```

### 10. echo - Display a Line of Text
Prints text to the terminal or writes text to a file.
- **Display text:**
```bash
$ echo "Hello, World!"
```
- **Write text to a file:**
```bash
$ echo "This is a line of text." > file.txt
```

## Understanding File Paths
- **Absolute Path:** The full path from the root directory.
```
/home/username/Documents/file.txt
```
- **Relative Path:** The path relative to the current directory.
```
./file.txt       # Current directory
../file.txt      # Parent directory
subfolder/file.txt
```

## Redirection and Pipes

### Redirection
- **Redirect Output (>):** Sends the output of a command to a file, overwriting the file if it exists.
```bash
$ echo "First line" > file.txt
```
- **Append Output (>>):** Adds the output to the end of a file.
```bash
$ echo "Second line" >> file.txt
```

### Pipes (|)

Used to pass the output of one command as input to another.
```bash
$ ls -l | less
```
In this instance you're getting the files in the current directory and piping that into the `less` command which allows you to view the output of the command in the less pager.

## Getting Help
- **Manual Pages (man):** Displays the manual page for a command.
```bash
$ man ls
```
- **Inline Help (--help):** Provides a brief overview of how to use a command.
```bash
$ ls --help
```

## Practice Exercises
1. Navigate to your home directory.
```bash
$ cd ~
```
2. Create a directory called practice.
```bash
$ mkdir practice
```
3. Change into the practice directory.
```bash
$ cd practice
```
4. Create an empty file named test.txt.
```bash
$ touch test.txt
```
5. Write “Hello, Terminal!” into test.txt.
```bash
$ echo "Hello, Terminal!" > test.txt
```
6. Display the contents of test.txt.
```bash
$ cat test.txt
```
7. Make a copy of test.txt named copy.txt.
```bash
$ cp test.txt copy.txt
```
8. List all files in the directory with detailed information.
```bash
$ ls -l
```
9. Rename copy.txt to renamed.txt.
```bash
$ mv copy.txt renamed.txt
```
10. Delete renamed.txt.
```bash
$ rm renamed.txt
```

## Additional Resources
- [Bash Reference Manual](https://www.gnu.org/s/bash/manual/bash.html)
- [Explainshell - Explains shell commands and their options.](https://explainshell.com/)
