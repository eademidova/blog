---
title: Week 5
subtitle: Post for the fifth week.

# Summary for listings and search engines
summary: Post for the fifth week.

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
Over the past week, labs 13 and 14 were completed on the following topics:

1. Tools used in software development in OS such as UNIX/Linux
2. Named pipes

## Lab #13

As a result of the laboratory work, she acquired the simplest skills in developing, analyzing, testing and debugging applications in the UNIX/Linux operating system using the example of creating a calculator with simple functions in the C programming language.

The following tasks were completed:

1. Create a subdirectory ~/work/os/lab_prog in your home directory.
2. Create files in it: calculate.h, calculate.c, main.c.
It will be the most primitive calculator capable of adding, subtracting, multiplying
and divide, raise a number to a power, take the square root, calculate sin, cos, tan.
When run, it will ask for the first number, the operation, the second number. Thereafter
the program will print the result and stop.
3. Compile the program with gcc.
4. Correct syntax errors if necessary.
5. Create a Makefile.
6. Use gdb to debug the calcul program.
7. Using the splint utility, try to analyze the codes of the calculate.c files
and main.c.

## Lab #14

As a result of the laboratory work, she gained practical skills in working with named pipes.

The following tasks were solved:

Study the server.c and client.c programs given in the text. Taking these examples
for the sample, write similar programs with the following changes:

1. Not 1 client works, but several (for example, two).
2. Clients transmit the current time with some frequency (for example, once every five
seconds). Use the sleep() function to pause the client.
3. The server does not work indefinitely, but stops working after a while (for example,
measure, 30 sec). Use the clock() function to determine the server's uptime.
What happens if the server terminates without closing the channel?

## Conclusions

Over the past week, I've been learning about named pipes and getting hands-on with them. I also acquired the simplest skills in developing, analyzing, testing and debugging applications in UNIX/Linux operating systems using the example of creating a calculator with simple functions in a programming language. . In general, I am satisfied with the results of the past week, I completed all the work in advance and I did not have any particular difficulties.

