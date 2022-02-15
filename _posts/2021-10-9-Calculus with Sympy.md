---
layout: post
title: "Calculus with Sympy"
categories: misc
tag: 
  - misc
---

[Sympy](https://www.sympy.org/en/index.html) is a python package through which we can perform calculus operations in mathematics like differentiation, integration, limits, infinite series, and so on. It is a python library used mainly for symbolic mathematics. The installation of this library is simple by using the following command:

```
pip install sympy
```

In order to write any symbolic expressions, firstly, we have to declare the symbolic variables that are involved in the symbolic expression. This can be done by:

- **sympy.Symbol( ):** used to declare a single variable by passing a variable as a string

- **sympy.symbols( ):** used to declare multi variables.

  **1. Differentiation:**
  Differentiation of any function can be done through the command **diff(func, var,n)**. Here, the “**func**” represents the symbolic function that is to be differentiated, “**var**” denotes the variable with respect to which we have to differentiate the function, and “**n**” denotes the nth derivative that needs to be computed for the function. This can be illustrated as:

  ```
  # Importing essential library
  import sympy as sym
   
  # Declaration of the variables
  x, y, z = sym.symbols('x y z')
   
  # function whose derivative is to be find
  f = x**5 * y - y**2 + z
   
  # Differentiating f with respect to x
  derivative_x = sym.diff(f, x, 2)
  print('derivative w.r.t x: ',
        derivative_x)
   
  # Differentiating exp with respect to y
  derivative_y = sym.diff(f, y, 2)
  print('derivative w.r.t y: ',
        derivative_y)
  ```

  The output obtained is:

  ```
  derivative w.r.t x:  20*x**3*y
  derivative w.r.t y:  -2
  ```

  

**2. Integration :**

Through sympy, we can do both definite as well as indefinite integration by using `integerate()` function.

The general syntax used for the indefinite integration is given as:
`sympy.integrate(func, var)`

Here, “**func**” represents the function that is to be integrated and “**var**” represents the variable with respect to which it is integrated.

This can be illustrated as:

```
# Indefinite integration of sin(x) w.r.t. x
integration = sym.integrate(sym.sin(x), x)
print('indefinite integral of sin(x): ',
      integration)
```

The output obtained is:

```
indefinite integral of sin(x):  -cos(x)
```

The general syntax used for the definite integration is given as:

```
sympy.integrate(func, (var, lower_limit, upper_limit))
```

Here, **lower_limit** and **upper_limit** denote the lower and upper limit of the definite integration respectively.

This can be illustrated as:

```
# Definite integration of cos(x) w.r.t. x between -1 to 1
integration = sym.integrate(sym.cos(x), (x, -1, 1))
print('definite integral of cos(x) between -1 to 1: ',
      integration)
```

The output obtained is:

```
definite integral of cos(x) between -1 to 1:  2*sin(1)
```

**In sympy, infinity (∞) is written as oo**.

**3. Limits:**

The limit of a function can be computed using this library by using `limit(function, variable, point)`.

This can be illustrated as:

```
# Calculating limit of f(x) = 1/x as x tends to ∞
limit_a = sym.limit(1/x, x, sym.oo)
print(limit_a)
# Calculating limit of f(x) = tan(x)/x as x tends to 0
limit_b = sym.limit(sym.tan(x)/x, x, 0)
print(limit_b)
```

The output obtained is:

```
0
1
```

**4. Series expansion:**

The Taylor series expansions of functions around a point can be computed using sympy library. In order to compute the series expansion of f(x) around the point, x=x0 terms of order xn, the syntax used is:

```
sympy.series(f, x, x0, n)
```

The default value of x0=0 and n=6 is considered in case if they can be omitted from the syntax.

This can be illustrated as:

```
#  series expansion 
series = sym.series(sym.sin(x), x)
print(series)
```

The output obtained is:

```
x - x**3/6 + x**5/120 + O(x**6)
```

