---
layout: post
title: "Calculus with Sympy"
categories: misc
tag: 
  - misc
---

[Sympy](https://www.sympy.org/en/index.html) is a python package through which we can perform calculus operations in mathematics like differentiation, integration, limits, infinite series, and so on. It is a python library used mainly for symbolic mathematics. The installation of this library is simple by using the following command:

``

pip install sympy

In order to write any symbolic expressions, firstly, we have to declare the symbolic variables that are involved in the symbolic expression. This can be done by:

- **sympy.Symbol( ):** used to declare a single variable by passing a variable as a string

- **sympy.symbols( ):** used to declare multi variables.

  **1. Differentiation:**
  Differentiation of any function can be done through the command **diff(func, var,n)**. Here, the “**func**” represents the symbolic function that is to be differentiated, “**var**” denotes the variable with respect to which we have to differentiate the function, and “**n**” denotes the nth derivative that needs to be computed for the function. This can be illustrated as:



