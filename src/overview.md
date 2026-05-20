# Lesson 1: Overview

Focuses on $A x = b$, which is easy to forget, but it's a simple system of equations; the number of equations is the number of rows of $A$.

- **Row Picture**: look at each equation one at a time (lines, planes, and higher-dimensional flat surfaces.)
    - $A = \begin{bmatrix}1 & 2 \\ 3 & 4\end{bmatrix}$, $x = (x_1, x_2)$, $b = (b_1, b_2)$
    - Most obvious if we do $x^T A = b^T$; we linearly combine rows (just as in elimination)
    - For example:
      $$x_1 + 2x_2 = b_1$$
    - Gets hard or impossible to visualise for 4 or more dimensions
    - But simple cases help see what kinds of things can happen (intersections, parallels)
- **Column Picture**: look at linear combinations of the columns of $A$ with numbers (which are the rows of $x$).
    - For example:
      $$x_1 \begin{bmatrix}a_{11} \\ a_{21}\end{bmatrix} + x_2 \begin{bmatrix}a_{12} \\ a_{22}\end{bmatrix} = \begin{bmatrix}b_1 \\ b_2\end{bmatrix}$$
    - More powerful.

These views are left unchanged when multiplying matrices, and we can look at them as combining rows or columns of one or the other matrix. In

$$A B = C$$

row $i$ of matrix $A$ combines rows of $B$ and produces a new row $i$ (same index) in $C$. Matrix $B$ combines columns of $A$, producing columns of $C$.

### Does $x$ always exist, for any $b$?

We want methods to find $x$.

An essential question is:

> Can the $x$, combined with the columns of $A$, fill the whole $N$-dimensional space rather than just reaching a particular $b$?

- Yes for non-singular, invertible $A$
- Each parallel column (or non-independent column) makes it singular, removing one or more dimensions
- But we can still solve for vectors in that lower-dimensional space! (and for more advanced uses, we can also approximate it)

### Matrix-vector multiplication

- The common "dot product" method
- As a linear combination of columns or rows of $A$
    - $A x$ is a linear combination of columns of $A$
    - $x A$ is a linear combination of the rows of $A$

### Elimination

Method to find a solution ($x$) to

$$A x = b$$

if there is one; when there isn't one, the method will fail.

