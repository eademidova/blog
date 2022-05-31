---
title: Week 4
subtitle: Fourth week post.

# Summary for listings and search engines
summary: Fourth week post.

# Link this post with a project
projects: []

# Date published
date: '2020-12-13T00:00:00Z'

# Date updated
lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - Academic

categories:
  - Demo
---

## Introduction

Over the past week, laboratory work 11 and 12 was completed on the following topics:

1. Programming in the command processor OS UNIX. Branches and cycles.
2. Programming in the command processor OS UNIX. Advanced programming.

## Lab #11

As a result of the laboratory work, I learned the basics of programming in the UNIX OS shell. I learned how to write more complex batch files using logical control structures and loops..

Tasks were completed on the following topics:

1. Using the getopts grep commands, write a batch file that parses
command line with switches:
– -iinputfile — read data from the specified file;
– -ooutputfile — output data to the specified file;
– -ppattern — specify a search pattern;
– -C — to distinguish between large and small letters;
-n Print line numbers.
and then searches the specified file for the necessary lines, determined by the -p switch.
2. Write a C program that takes in a number and determines if it is
greater than zero, less than zero, or equal to zero. The program is then terminated with
exit(n) function, passing the exit code information to the shell. Team-
ny file should call this program and, after parsing with the command
$?, display a message telling you what number was entered.
3. Write a batch file that creates the specified number of files, numbered
sequentially from 1 to 𝑁 (for example, 1.tmp, 2.tmp, 3.tmp, 4.tmp, etc.). Number of files
to be created is passed as command line arguments. This same co-
The mand file must be able to delete all files created by it (if they exist).
4. Write a batch file that, using the tar command, packs into an archive
all files in the specified directory. Modify it so that it packs
only files that have been modified less than a week ago (use
find command)

## Lab #12

Studied the basics of programming in the UNIX OS shell. learned to write more
complex batch files using logical control constructs
and cycles.

The following tasks were solved:

1. Write a batch file that implements a simplified semaphore mechanism. Co-
mand file must wait for some time t1 to be released
resource, issuing a message about it, and after waiting for its release, use
it for some time t2<>t1, also giving out information that
the resource is used by the corresponding batch file (process). Run
batch file in one virtual terminal in the background by redirecting
its output to another (> /dev/tty#, where # is the terminal number where the
output) in which this file is also running, but not in the background, but in a privileged
mode. Refine the program so that there is the possibility of interaction between the three
or more processes.
2. Implement the man command using a batch file. Explore the contents of the
log /usr/share/man/man1. It contains archives of text files containing
help on most of the programs and commands installed in the system. Each archive
can be opened with the less command by immediately viewing the contents of the help. Command
the file must receive the name of the command as a command line argument and in the form
output a help about this command or a message about the lack of help,
if the corresponding file is not in the man1 directory.
3. Using the $RANDOM built-in variable, write a batch file that generates
generating a random sequence of letters of the Latin alphabet. Note that $RANDOM
produces pseudo-random numbers in the range from 0 to 32767

## Conclusions

Over the past week, I've learned the basics of UNIX shell programming. I also learned how to write more complex batch files using logical control structures.
and cycles. The tasks were interesting, but difficult, so I solved them for quite a long time and not without someone else's help. In general, I am satisfied with the results of the past week, I completed all the work in advance and I did not have any particular difficulties.


