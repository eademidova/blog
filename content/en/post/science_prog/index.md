---
title: Scientific programming languages.
subtitle: Post about scientific programming languages.

# Summary for listings and search engines
summary: Post about scientific programming languages.

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

In this article, we will cover the following topics:

1. LaTeX markup language
2. Octave programming language
3. Julia Programming Language

## LaTeX markup language

 LaTeX (pronounced /ˈlɑːtɛx/ or /ˈleɪtɛx/ [1]) is the most popular set of macro extensions (or macro package) for the TeX computer-aided layout system, which facilitates the typesetting of complex documents.

 This tool is used ubiquitously to create scientific papers, write books, and many other forms of publication. It allows not only to create beautifully designed documents, but also allows users to implement complex typesetting elements such as mathematical expressions, tables, references and bibliographies very quickly, getting consistent markup across all sections.

 Thanks to the availability of a large number of open libraries (more on that later), the possibilities of LaTeX are almost limitless. These libraries extend the user experience even further, allowing you to add footnotes, draw diagrams, and more.

 One of the most compelling reasons many people use LaTeX is to separate the content of a document from its style. This means that after writing the content, you can easily change its appearance. Similarly, you can create one document style and use it to standardize the look of others.

 This allows scientific journals to create templates for submissions. These templates have pre-defined markup, leaving only the content to be added. In fact, there are hundreds of such templates, ranging from various resumes to slide presentations.

## Octave programming language

 MGNU Octave is a free system for mathematical calculations[1] using a high-level language compatible with MATLAB.

 Octave provides an interactive command interface for solving linear and non-linear mathematical problems and other numerical experiments. In addition, Octave can be used for batch processing. The Octave language operates with arithmetic of real and complex scalars, vectors and matrices, has extensions for solving linear algebraic problems, finding the roots of systems of nonlinear algebraic equations, working with polynomials, solving various differential equations, integrating systems of differential and differential-algebraic equations of the first order, integrating functions on finite and infinite intervals. This list can be easily expanded using the Octave language (or using dynamically loaded modules created in C, C++, Fortran, etc.).

 Researchers at the University of Maryland in the US compared math calculations using MATLAB, Octave, SciLab, and FreeMat in a simple and complex scenario. In the first case, a system of linear equations was solved, and in the second, a finite-difference discretization of the Poisson equation in two-dimensional space. The main conclusion is that GNU Octave copes with tasks better than other open mathematical packages, demonstrating results (pages 23 and 25) comparable to those of Matlab.

 Scientific calculations performed using open source software have an additional "layer of protection", because if desired, anyone can repeat the same calculations and check the validity of the results. The same calculations performed on expensive software partially cut off the possibility of verifying the results. The problem is actually much broader (English text) and it's not just open source or proprietary math programs. It is no secret that scientific journals usually do not require authors to provide data and methods sufficient to guarantee the repetition of the results of the experiment, the verification of the model. Especially often economists and financiers sin with this, simply classifying their data. Checking the calculations and conclusions among a sample of an array of articles with "classified" data gave unexpected results (English text). Science, like software, should be open, which is why open math packages are of value to the whole society.

 

## Programming language Julia.

 The Julia language is a dynamically typed, cross-platform, freely distributed (MIT license) compiled free programming language that has a number of advantages and disadvantages.
Julia implements the ability to JIT - compilation based on LLVM. Just-in-Time (JIT) compilation provides both the expressiveness of modern interpreted languages ​​and the performance of languages ​​such as C and Fortran. The JIT compiler compiles the first time a program is run, extracting information from the text that is not explicitly specified by the programmer, and using this information to optimize the generated machine code.

 The advantages of the Julia language include the following:
 - Simplicity intuitive language whose syntax resembles the syntax of Python and MATLAB;
 - the speed of calculations of programs written in Julia is comparable to the speed of programs written in C or Fortran;
 - efficient vectorization and parallelization of calculations, a large number of data types, including rational and complex numbers;
 - carrying out calculations in the absence of some data (there is a missing data type);
 - setting the accuracy of calculations (data type BigFloat, function setprecision);
 - implementation of symbolic calculations using macro commands;
 - use of libraries written in C and Fortran, and exchange of libraries with Python and R;
 - integration with DBMS (PostgreSQL, MySQL, JSON);
 - support for Unicode characters;
 - use of the multiple dispatching paradigm - the function call weakly depends on the type of function parameters (parametric polymorphism);
 - the presence of a good built-in mathematical library with linear algebra functions.
 
 Julia is a full-fledged programming language that has integer arithmetic, floating point operations, loops, working with C-like structures, and even an analogue of the goto operator. At the same time, the language has a very convenient ability to vectorize calculations, which is typical for high-level languages.
 - If we talk about the shortcomings of the Julia language, then it should be noted that the compilation time of large programs can be quite noticeable (minutes);
 - the language is relatively new, so the number of libraries in this language is relatively small (compared to Python);
 - it is impossible to create a stand-alone program - Julia programs work only in the Julia environment.
 

## Conclusions

Scientific programming uses many programming languages ​​and mathematical systems, but those listed in this article, in my opinion, are the most convenient and effective.


