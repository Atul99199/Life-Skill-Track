# Linux/Unix Basic Architecture, Philosophy, and Filesystem

## Introduction

* Linux and Unix are operating systems that manage your computer's
hardware and software.

* They act as a bridge between you and the
hardware, allowing programs to run safely and efficiently.

* It was developed in 1969 at Bell Labs.

![alt text](<Screenshot 2026-07-26 at 1.21.05 PM.png>)

------------------------------------------------------------------------

# Linux/Unix Architecture

 ![alt text](<Screenshot 2026-07-26 at 1.29.14 PM.png>)

## 1. User Level

The user interacts with the system by typing commands or using graphical
applications.

Examples: - Opening a browser - Creating a file - Making Directories.

## 2. Shell

The shell is a command interpreter.

* Common shells: - bash - zsh (macOS) - sh - fish
* The shell reads your command, passes it to the kernel, and displays the
result.

## 3. Kernel

The kernel is the core of the operating system or heart of the OS.

### Responsibilities:
* Process management 
* Memory management 
* File system management 
* Device management 
* Networking 
* Security

Example: When you run:

``` bash
cat file.txt
```

the shell asks the kernel to read the file. The kernel retrieves the
data from storage and returns it.

## 4. Hardware

Examples:  CPU, RAM, SSD/HDD, Keyboard, Mouse, Monitor, Network
card

![alt text](<Screenshot 2026-07-26 at 1.41.57 PM-1.png>)

## Diffrent variants of Unix
![alt text](<Screenshot 2026-07-26 at 1.26.35 PM-1.png>)

## Unix Family Tree 

                    Original UNIX
                         │
      ┌──────────────────┼───────────────────┐
      │                  │                   │
    BSD               System V           Unix-like
      │                  │                   │
      │                  ├── Solaris         ├── Linux
      │                  ├── AIX             │   ├── Ubuntu
      │                  ├── HP-UX           │   ├── Debian
      │                  └── SCO Unix        │   ├── Fedora
      │                                      │   ├── Red Hat
      └── FreeBSD                            │   └── CentOS
------------------------------------------------------------------------

# Linux/Unix Philosophy

## 1. Do one thing well

![alt text](<Screenshot 2026-07-26 at 1.57.04 PM-1.png>)

------------------------------------------------------------------------

## 2. Everything is a file

![alt text](<Screenshot 2026-07-26 at 2.00.47 PM-1.png>)

------------------------------------------------------------------------

## 3. Build powerful commands using pipes

Example:

``` bash
cat book | tr ' ' '\n' | sort | uniq | wc -l
```

Flow:

    book
     |
     v
    cat
     |
     v
    tr
     |
     v
    sort
     |
     v
    uniq
     |
     v
    wc -l

------------------------------------------------------------------------

## 4. Small tools working together

Example:

``` bash
ps -ef | grep python
```
![alt text](<Screenshot 2026-07-26 at 2.02.57 PM-1.png>)
------------------------------------------------------------------------
## 5. Choose portability over efficiency:
It's usually better to write software that works on many systems than software that only works on one system but is slightly faster.

----------------------------------------------------------------------
## 6. Keep it Simple, Stupid (KISS)
It is one of the most important principles in Unix/Linux philosophy.
Don't make your program, design, or command more complicated than it needs to be.

```
                 KISS Principle

          Problem to Solve
                 │
        ┌────────┴────────┐
        │                 │
        ▼                 ▼
 Simple Solution      Complex Solution
        │                 │
        │                 │
   Easy to Read      Hard to Read
   Easy to Debug     Hard to Debug
   Easy to Maintain  Hard to Maintain
        │                 │
        └────────┬────────┘
                 ▼
       Choose the Simple One
```

# Linux Filesystem
* The Linux File System is the way Linux organizes, stores, and manages all files and directories.
* Unlike Windows, Linux does not have multiple drive letters such as C:\, D:\, or E: .
* Instead, Linux stores everything under a single root directory "/".

![alt text](file-System-1.png)

------------------------------------------------------------------------


------------------------------------------------------------------------

# Absolute vs Relative Paths

**Absolute path:-** An Absolute Path is the complete path to a file or directory. It always starts with the root directory (`/`).

``` text
/Users/atul/Documents/file.txt
```

**Relative path:-** A Relative Path starts from your current working directory.

``` text
Documents/file.txt
```



------------------------------------------------------------------------

# File Permissions
Linux uses **file permissions** to control who can read, modify, or execute a file or directory. Every file has three types of users and three types of permissions.

![alt text](file-permission-1.png)

------------------------------------------------------------------------



