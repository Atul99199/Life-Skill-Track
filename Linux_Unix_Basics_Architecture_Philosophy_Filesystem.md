# Linux/Unix Basic Architecture, Philosophy, and Filesystem

## Introduction

* Linux and Unix are operating systems that manage your computer's
hardware and software.

* They act as a bridge between you and the
hardware, allowing programs to run safely and efficiently.

* It was developed in 1969 at Bell Labs.

<img width="1032" height="330" alt="image" src="https://github.com/user-attachments/assets/0f7a9599-f0b1-45a0-85ee-3066be270523" />


------------------------------------------------------------------------

# Linux/Unix Architecture

<img width="1830" height="558" alt="image" src="https://github.com/user-attachments/assets/74021f9b-e3bb-4420-8265-45dbb23e554d" />


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

<img width="1012" height="290" alt="image" src="https://github.com/user-attachments/assets/cd381c2d-d40a-45f1-a2ee-3b39ce9dd0f1" />


## Diffrent variants of Unix
<img width="852" height="558" alt="image" src="https://github.com/user-attachments/assets/a4fdbbc1-8536-4067-acba-d72783c02f41" />


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

<img width="870" height="282" alt="image" src="https://github.com/user-attachments/assets/0350084f-68b1-4a3f-9b82-4a306c400741" />


------------------------------------------------------------------------

## 2. Everything is a file

<img width="884" height="286" alt="image" src="https://github.com/user-attachments/assets/6edbdecd-d73b-4f02-8d70-862c1e76890e" />


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
<img width="878" height="256" alt="image" src="https://github.com/user-attachments/assets/1dc3478d-867e-4f44-bb66-4df04cfc52a3" />

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

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/3a21edd0-a0eb-48c1-b125-da2c763dc0fc" />


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

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/20ad25e6-3fc1-4fcb-982f-92e59b94e218" />


------------------------------------------------------------------------

### References 

* The Linux Foundation & Linux Kernel Documentation. https://docs.kernel.org/

* The Linux Documentation Project. https://tldp.org/

* GNU Core Utilities Manual. https://www.gnu.org/software/coreutils/manual/

* The Open Group. (2018). https://pubs.opengroup.org/onlinepubs/9699919799/



