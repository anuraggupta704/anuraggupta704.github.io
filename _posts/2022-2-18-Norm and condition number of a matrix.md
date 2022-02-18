---
layout: post
title: "Norm and condition number of a matrix"
categories: misc
tag: 
  - misc
---

In a numerical analysis with a vector involvement, norms are essential to predict the various errors involved in the numerical analysis. A norm is a function ||.|| in a vector space V. If A is a n*n matrix, then its norm is a real number and denoted by ||A||. A norm satisfies the following properties:

1. ||A||≥0||A||≥0 for any square matrix AA
2. ||A||=0||A||=0; for null matrix
3. ||kA||=|k|||A||||kA||=|k|||A||; kk is any scalar
4. ||A+B||≤||A||+||B||||A+B||≤||A||+||B||
5. ||AB||≤||A||||B||||AB||≤||A||||B||

## Types of norm:

1. 1- Norm or column norm:

    

   This norm is a maximum absolute sum of column and is defined as:

   ∥A∥1=max1≤j≤n(∑i=1n|aij|)‖A‖1=max1≤j≤n(∑i=1n|aij|)

2. Infinity norm: 

   This norm is a maximum absolute sum of row and is defined as:

   ∥A∥∞=max1≤i≤n(∑j=1n|aij|)‖A‖∞=max1≤i≤n(∑j=1n|aij|)

3. 2- Norm or Eucledian norm: 

   This norm is computed by taking square root of sum of squares of all the entities and it is defined as:

   ∥A∥E=∑i=1n∑j=1n(aij)2−−−−−−−−−−⎷‖A‖E=∑i=1n∑j=1n(aij)2

   > Consider a matrix A and its various norms are computed as:
   >
   > A=⎡⎣⎢5−11−43−2220⎤⎦⎥A=[5−42−1321−20]
   >
   > ∥A∥1=max(5+1+1,4+3+2,2+2+0)=max(7,9,4)=9‖A‖1=max(5+1+1,4+3+2,2+2+0)=max(7,9,4)=9
   >
   > ∥A∥∞=max(5+4+2,1+3+2,1+2+0)=max(11,6,3)=11‖A‖∞=max(5+4+2,1+3+2,1+2+0)=max(11,6,3)=11
   >
   > ∥A∥E=25+16+4+1+4+9+4+1+0−−−−−−−−−−−−−−−−−−−−−−−−−−−√=64−−√=8‖A‖E=25+16+4+1+4+9+4+1+0=64=8

   ## **Condition number:**

 In the numerical analysis, the condition number of a matrix is very important since it represents how much change reflects in the output with a minor change in the input. If a condition number of a matrix is small, it is **well conditioned** problem and that can be handled efficiently and accurately while if the condition number is large, the problem is **ill-conditioned** and cannot be handled accurately. In that case, some preconditioners can be used. For a singular matrix, condition number is infinite since its determinant is zero and inverse is not possible. The condition number of an invertible matrix A is defined as:



κ(A)=||A||∣∣|A−1∣∣|κ(A)=||A||||A−1||



The value of the condition number of a matrix is always greater than or equal to one. Also, it is noted that when we calculate the condition number of a matrix, same type of norm is considered both for the matrix and its inverse.

> A=[213−1]A=[231−1]
>
> ∥A∥1=max(2+1,3+1)=4A−1=1−2−3[−1−1−32]=[151535−25]∥∥A−1∥∥1=max(15+15,35+25)=1‖A‖1=max(2+1,3+1)=4A−1=1−2−3[−1−3−12]=[153515−25]‖A−1‖1=max(15+15,35+25)=1
>
>  Therefore κ1(A)=∥A∥1∥∥A−1∥∥1=4×1=4 Therefore κ1(A)=‖A‖1‖A−1‖1=4×1=4

The convergence of an iterative process depends on the condition number of a matrix.  If the square matrix of the linear algebraic equation Ax=bAx=b is singular, then this system does not have a solution. On the other hand, when the matrix is non-singular, it is the condition number of a matrix that decides about the convergence of the approximate solution obtained in the iteration process.
