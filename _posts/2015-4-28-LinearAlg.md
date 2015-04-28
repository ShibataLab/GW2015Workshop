---
layout: post
title: Linear Algebra Tutorial
---

The [Machine Learning]({{ site.baseurl }}/ML) workshop requires some basic knowledge of Linear Algebra. Given below are some basics about Matrices, Vectors and their operations.

* Table of Contents:
{:toc}

## Matrices and Vectors
---

* Matrices are 2-dimensional arrays:

  $$
  \left [
  \begin{array}{ccc}
  a & b & c \\
  d & e & f \\
  g & h & i \\
  j & k & l
  \end{array}
  \right ]
  $$

  This matrix has 4 rows and 3 columns, so it is a $$4 \times 3$$ matrix.

* A vector is of two types:
  - **Column Vector**: Matrix with one column and many rows.
    
    $$
    \left [
    \begin{array}{c}
    w \\
    x \\
    y \\
    z \\
    \end{array}
    \right]
    $$

    This vector is of size $$4 \times 1$$.

  - **Row Vector**: Matrix with one row and many columns.

    $$
    \left [
    \begin{array}{cccc}
    w & x & y & z
    \end{array}
    \right]
    $$

    This vector is of size $$1 \times 4$$.

* Following are some of the notations used to refer to Matrices:

  - $$A_{ij}$$ refers to element in $$i^{th}$$ row and $$j^{th}$$ column in Matrix $$A$$.

  - $$v_i$$ refers to $$i^{th}$$ element of vector $$v$$.

  - Matrices $$A$$ are usually uppercase and vectors $$v$$ are lower case.

  - $$\mathbb{R}$$ refers to a set of scalars.

  - $$\mathbb{R}^n$$ refers to $$n$$-dimensional vectors.

  - $$\mathbb{R}^{m \times n}$$ refers tp $$m \times n$$-dimensional matrices.

## Addition and Scalar Multiplication
---

* Addition and subtraction are element-wise:

  $$
  \left [
  \begin{array}{cc}
    a & b \\
    c & d 
  \end{array}
  \right ]
  +
  \left [
  \begin{array}{cc}
    w & x \\
    y & z 
  \end{array}
  \right ]
  =
    \left [
  \begin{array}{cc}
    a+w & b+x \\
    c+y & d+z 
  \end{array}
  \right ]
  $$

* To add or subtract matrices, their dimensions must be the same.

* In scalar multiplication, we multiply every element by the scalar:

  $$
  \left [
  \begin{array}{cc}
    a & b \\
    c & d 
  \end{array}
  \right ]
  \times
  x
  =
  \left [
  \begin{array}{cc}
    a \times x & b \times x \\
    c \times x & d \times x 
  \end{array}
  \right ]
  $$

## Matrix-Vector Multiplication
---

* We map the column of a vector onto each row of a matrix, multiplying each element and summing the result.

  $$
  \left [
  \begin{array}{cc}
    a & b \\
    c & d \\
    e & f
  \end{array}
  \right ]
  \times
  \left [
  \begin{array}{c}
    x \\
    y	
  \end{array}
  \right ]
  =
  \left [
  \begin{array}{cc}
    a \times x + b \times y \\
    c \times x + d \times y \\
    e \times x + f \times y
  \end{array}
  \right ] 
  $$

* The number of rows of the vector must equal the number of columns of the matrix.

* An $$n \times m$$ matrix multiplied by an $$m \times 1$$ vector results in an $$n \times 1$$ vector.

## Matrix-Matrix Multiplication
---

* We multiply two matrices by breaking it into several vector multiplications and concatenating the result.

  $$
  \left [
  \begin{array}{cc}
    a & b \\
    c & d \\
    e & f
  \end{array}
  \right ]
  \times
  \left [
  \begin{array}{cc}
    w & x \\
    y & z	
  \end{array}
  \right ]
  =
  \left [
  \begin{array}{cc}
    a \times w + b \times y & a \times x + b \times z\\
    c \times w + d \times y & c \times x + d \times z\\
    e \times w + f \times y & e \times x + f \times z
  \end{array}
  \right ] 
  $$

* An $$m \times n$$ matrix multiplied by an $$n \times o$$ matrix results in an $$m \times o$$ matrix. In the above example, a $$3 \times 2$$ matrix times a $$2 \times 2$$ matrix resulted in a $$3 \times 2$$ matrix.

* To multiply two matrices, the number of columns of the first matrix must equal the number of rows of the second matrix.

## Matrix Multiplication Properties
---

* Matrix multiplication is not commutative. 

  $$
  A \times B \neq B \times A
  $$

* Matrix multiplication is associative. 

  $$
  (A \times B) \times C = A \times (B \times C)
  $$

* The **identity matrix**, when multiplied by any matrix of the same dimensions, results in the original matrix.

* When multiplying the identity matrix after some matrix, the square identity matrix should match the other matrix's columns. When multiplying the identity matrix before some other matrix, the square identity matrix should match the other matrix's rows.

## Inverse and Transpose
---
* The inverse of a matrix $$A$$ is denoted by $$A^{−1}$$. Multiplying a matrix by its inverse results in the identity matrix.

* A non square matrix does not have an inverse matrix.

* The transposition of a matrix is like rotating the matrix once clockwise and then reversing it:
  
  $$
  A = 
  \left [
  \begin{array}{cc}
    a & b \\
    c & d \\
    e & f
  \end{array}
  \right ]
  $$  

  $$
  A^T = 
  \left [
  \begin{array}{ccc}
    a & c & e\\
    b & d & f
  \end{array}
  \right ]
  $$  

* In other words:
  
  $$
  A_{ij} = A^T_{ji}
  $$

## Additional Resources
---

* Khan academy has excellent [Linear Algebra Tutorials](http://www.khanacademy.org/#linear-algebra).

* This [Linear Algebra text](http://en.wikipedia.org/wiki/Linear_least_squares_%28mathematics%29#Derivation_of_the_normal_equations) is a good resource for derivation of normal equation.