---
layout: post
title: "Gradient vector, Hessian matrix and Quadratic forms"
categories: misc
tag: 
  - misc
---

1. Gradient vector: 

   If the partial derivative of a function f(x) (function having $n$ variables) with respect to the $n$ variables $x_1$, $x_2$.....$x_n$ at a point $x^{\star}$ is taken, then that partial derivative vector of f(x) represents the 

   "gradient vector" 

   which is represented by symbols like $c$ or $\triangledown {f}$, as:

   $\mathbf{c}=\nabla f\left(\mathrm{x}^{*}\right)=\left[\begin{array}{c}\frac{\partial f\left(\mathrm{x}^{*}\right)}{\partial x_{1}} \\ \frac{\partial f\left(\mathrm{x}^{*}\right)}{\partial x_{2}} \\ \vdots \\ \frac{\partial f\left(\mathrm{x}^{*}\right)}{\partial x_{n}}\end{array}\right]=\left[\frac{\partial f\left(\mathrm{x}^{*}\right)}{\partial x_{1}} \frac{\partial f\left(\mathrm{x}^{*}\right)}{\partial x_{2}} \cdots \frac{\partial f\left(\mathrm{x}^{*}\right)}{\partial x_{n}}\right]^{T}$

   **The geometrical intrepretation of the gradient vector is that it is normal to the tangent plane at the point $x^{\star}$ .
   **

   [caption id="attachment_5296" align="aligncenter" width="300"]![img](https://computationalmechanics.in/wp-content/uploads/2022/06/Screenshot-2022-06-08-183706-300x226.png) Gradient vector of a function f(x) at the point $x^{\star}$ [/caption]

2. Hessian matrix: 

   When we differentiate the gradient vector, then we will get the matrix of the second partial derivatives of a function f(x) called the 

   "Hessian matrix"

   .

   $$\frac{\partial^{2} f}{\partial \mathrm{x} \partial \mathrm{x}}=\left[\begin{array}{cccc}\frac{\partial^{2} f}{\partial x_{1}^{2}} & \frac{\partial^{2} f}{\partial x_{1} \partial x_{2}} & \cdots & \frac{\partial^{2} f}{\partial x_{1} \partial x_{n}} \\ \frac{\partial^{2} f}{\partial x_{2} \partial x_{1}} & \frac{\partial^{2} f}{\partial x_{2}^{2}} & \cdots & \frac{\partial^{2} f}{\partial x_{2} \partial x_{n}} \\ \vdots & \vdots & & \vdots \\ \frac{\partial^{2} f}{\partial x_{n} \partial x_{1}} & \frac{\partial^{2} f}{\partial x_{n} \partial x_{2}} & \cdots & \frac{\partial^{2} f}{\partial x_{n}^{2}}\end{array}\right]$$

   Each element in a Hessian matrix is a function in itself that is evaluated at a point $x^{\star}$. The Hessian is always a symmetric matrix.

3. Quadratic Forms: 

   A quadratic form is a non-linear function that consists of only second-order terms (either the square of a variable or the product of the two variables). This form is very important in the context of optimization.

   **It is also used to predict the convexity of the functions of the optimization problem; that means we can check whether a given function is convex or not by checking its definite form.** We first compute the Hessian matrix of that particular function and if the Hessian matrix is positive definite or positive semidefinite, then that function is convex in nature. If the Hessian matrix is positive definite, then the function is strictly convex and if the Hessian matrix is positive semidefinite, then the function is convex. Also, it is to be noted that a linear function is always convex in nature. Consider the function F(x) as:
   $$
   F(x)=x_{1}^{2}+7 x_{2}^{2}+9 x_{3}^{2}+5 x_{1} x_{2}-4 x_{2} x_{3}+9 x_{3} x_{1}
   $$
   The quadratic form of this function is written as:
   $$
   F(\mathbf{x})=\mathbf{x}^{T} \mathbf{P} \mathbf{x}
   $$
   where $P$ represents the matrix of the quadratic form F(x) whose elements are obtained from the coefficients of the terms in the function F(x).It is to be noted that there are infinite matrices that are associated with the given quadratic form. Out of all such matrices, there is only one symmetric matrix (i.e $A$) while the rest are all asymmetric matrix.

   The symmetric matrix in terms of the asymmetric matrix is written as:
   $$ 
   A = \frac{1}{2} (P+P^{T})
   $$

   The quadratic form of a function F(x) when a matrix $A$ is written instead of matrix $P$ as:
   $$F(\mathbf{x})=\mathbf{x}^{T} \mathbf{A} \mathbf{x} $$

   The symmetric matrix $A$ is used to predict the nature of the quadratic form. Following are the possible forms for the function F(x).

- **Positive definite:** $F(\mathbf{x})>0$ for all $\mathbf{x} \neq 0$; the matrix $\mathbf{A}$ is called positive definite.

- **Positive semidefinite:** $F(\mathbf{x}) \geq 0$ for all $\mathbf{x} \neq \mathbf{0}$; the matrix $\mathbf{A}$ is called positive semidefinite.

- **Negative definite:** $F(\mathbf{x})<0$ for all $\mathbf{x} \neq 0$; the matrix $\mathbf{A}$ is called negative definite.

- **Negative semidefinite:** $F(\mathbf{x}) \leq 0$ for all $\mathbf{x} \neq 0$; the matrix $\mathbf{A}$ is called negative semidefinite.

- **Indefinite:** The quadratic form is called indefinite if it is positive for some values of $\mathbf{x}$ and negative for some others. In that case, the matrix $\mathbf{A}$ is also called indefinite.

  In order to check the form of a matrix, the **eigenvalue check** is used which is explained as under-
  \1. F(x) is said to be **positive definite** if and only if all the eigenvalues of symmetric matrix $A$ (matrix $A$ having order $n \times n$) are strictly positive i.e $\lambda_{i} > 0$; i= 1 to $n$.
  \2. F(x) is said to be **positive semidefinite** if and only if all the eigenvalues of symmetric matrix $A$ are non-negative i.e  $\lambda_{i} \geq 0$; i= 1 to $n$. **It is to be noted here that at least one of the eigenvalue must be zero for the matrix to be called a** **positive semidefinite**. 
  \3. F(x) is said to be **negative definite** if and only if all the eigenvalues of symmetric matrix $A$ are strictly negative  i.e $\lambda_{i} < 0$; i= 1 to $n$.
  \4. F(x) is said to be **negative semidefinite** if and only if all the eigenvalues of symmetric matrix $A$ are nonpositive i.e  $\lambda_{i} \leq 0$; i= 1 to $n$. **It is to be noted here that at least one of the eigenvalue must be zero for the matrix to be called a** **negative semidefinite**. 
  \5.  F(x) is said to be **indefinite** if some of the eigenvalues are less than zero and some of them are greater than zero. i.e some $\lambda_{i} \leq 0$ and some other $\lambda_{j} \geq 0$.

  **Differentiation of a Quadratic form:**
  The first derivative (called gradient) and second derivative (called Hessian) of a quadratic form is given as:
  $$ \triangledown F(x) = 2 A x $$ 
  $$ H= 2 A $$
