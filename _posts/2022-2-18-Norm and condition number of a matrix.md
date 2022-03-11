---
layout: post
title: "Norm and condition number of a matrix"
categories: misc
tag: 
  - misc
---



In a numerical analysis with a vector involvement, norms are essential to predict the various errors involved in the numerical analysis. A norm is a function ||.|| in a vector space V. If A is a n*n matrix, then its norm is a real number and denoted by ||A||. A norm satisfies the following properties:

1. $||A|| \geq 0$ for any square matrix $A$
2. $||A||=0$; for null matrix
3. $||kA||=|k| ||A||$; $k$ is any scalar
4. $||A+B|| \leq||A||+||B||$
5. $||AB|| \leq||A|| \quad||B||$

1. ## Types of norm:

   1. **1- Norm or column norm:** This norm is a maximum absolute sum of column and is defined as:
      $$
      \|A\|_{1}=\max _{1 \leq j \leq n}\left(\sum_{i=1}^{n}\left|a_{i j}\right|\right)
      $$

   2. **Infinity norm:** This norm is a maximum absolute sum of row and is defined as:
      $$
      \|A\|_{\infty}=\max _{1 \leq i \leq n}\left(\sum_{j=1}^{n}\left|a_{i j}\right|\right)
      $$

   3. **2- Norm or Eucledian norm:** This norm is computed by taking square root of sum of squares of all the entities and it is defined as:
      $$
      \|A\|_{E}=\sqrt{\sum_{i=1}^{n} \sum_{j=1}^{n}\left(a_{i j}\right)^{2}}
      $$

   

   > Consider a matrix A and its various norms are computed as:
   > $$
   > A=\left[\begin{array}{rrr}
   > 5 & -4 & 2 \\
   > -1 & 3 & 2 \\
   > 1 & -2 & 0
   > \end{array}\right]
   > $$
   > $$
   > \begin{aligned}
   > \|A\|_{1} &=\max (5+1+1,4+3+2,2+2+0) \\
   > &=\max (7,9,4) \\
   > &=9
   > \end{aligned}
   > $$
   > $$
   > \begin{aligned}
   > \|A\|_{\infty} &=\max (5+4+2,1+3+2,1+2+0) \\
   > &=\max (11,6,3) \\
   > &=11
   > \end{aligned}
   > $$
   > $$
   > \begin{aligned}
   > \|A\|_{E} &=\sqrt{25+16+4+1+4+9+4+1+0} \\
   > &=\sqrt{64} \\
   > &=8
   > \end{aligned}
   > $$

   ## **Condition number:**

    In the numerical analysis, the condition number of a matrix is very important since it represents how much change reflects in the output with a minor change in the input. If a condition number of a matrix is small, it is **well conditioned** problem and that can be handled efficiently and accurately while if the condition number is large, the problem is **ill-conditioned** and cannot be handled accurately. In that case, some preconditioners can be used. For a singular matrix, condition number is infinite since its determinant is zero and inverse is not possible. The condition number of an invertible matrix A is defined as:
   $$
   \kappa(A)=||A|| \quad\left||A^{-1}\right||
   $$
   The value of the condition number of a matrix is always greater than or equal to one. Also, it is noted that when we calculate the condition number of a matrix, same type of norm is considered both for the matrix and its inverse.

   > $$
   > A=\left[\begin{array}{rr}
   > 2 & 3 \\
   > 1 & -1
   > \end{array}\right]
   > $$$$
   > \begin{gathered}
   > \|A\|_{1}=\max (2+1,3+1)=4 \\
   > A^{-1}=\frac{1}{-2-3}\left[\begin{array}{rr}
   > -1 & -3 \\
   > -1 & 2
   > \end{array}\right]=\left[\begin{array}{cc}
   > \frac{1}{5} & \frac{3}{5} \\
   > \frac{1}{5} & \frac{-2}{5}
   > \end{array}\right] \\
   > \left\|A^{-1}\right\|_{1}=\max \left(\frac{1}{5}+\frac{1}{5}, \frac{3}{5}+\frac{2}{5}\right)=1 
   > \end{gathered}
   > $$$$
   > \text { Therefore } \kappa_{1}(A)=\|A\|_{1}\left\|A^{-1}\right\|_{1}=4 \times 1=4
   > $$

   The convergence of an iterative process depends on the condition number of a matrix.  If the square matrix of the linear algebraic equation $A x=b$ is singular, then this system does not have a solution. On the other hand, when the matrix is non-singular, it is the condition number of a matrix that decides about the convergence of the approximate solution obtained in the iteration process.

> 
