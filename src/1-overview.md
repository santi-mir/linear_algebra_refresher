# Lesson 1: Overview

_Brief summary of most important aspects of linear algebra._

---------------------

## Equations: Lines, Planes, and Hyperplanes

- **Line** is a linear equation of two variables: $a_1 x_1 + a_2 x_2 = b$,
- **Plane** is a linear equation of three variables: $a_1 x_1 + a_2 x_2 + a_3 x_3 = b$,
- **Hyperplane** is a linear equation of more variables: $ a_1 x_1 + \ldots + a_n x_n = b$.

They can be written as $\mathbf{a} \cdot \mathbf{x} = b$. An interesting result is that:

$$
\begin{align}
\mathbf{a} \cdot \mathbf{x} &= b\\
\mathbf{a}\cdot  \mathbf{x_0} &= b\\
\mathbf{a}\cdot(\mathbf{x}-\mathbf{x_0}) &= 0\\
\end{align}
$$

This is showing that $\mathbf{a}$ is orthogonal to the surface.

## System of Equations: Many Equations

_A system_ of linear equations is a bunch of those combined:

$$
\begin{align}
a_1 x_1 + a_2 x_2 &= b_1\\
a_3 x_1 + a_4 x_2 &= b_2
\end{align}
$$

They can be written as $A \mathbf{x} = \mathbf{b}$.

_Solving_ the system means finding the values of $x_i$ that solves _all_ the equations at once.

_Square systems_ are those with the same number of equations an unknowns. For a unique solution, we require $N$ surfaces (for $N$ variables) that all intersect at a point.


We can't easily visualise linear equations for $N\gt{}3$, so we need to develop other ways to look at the system.

### Ways to Look at Systems

- **Row Picture**: dot product of rows of $A$ and coefficients
    - We are thinking of surfaces (each equation).
- **Column Picture**: linear combination of the column-vectors of $A$ and the coefficients $x_i$ written as $\sum A_{col_i} \, x_i =  \mathbf{b}$,

> [!NOTE]
> Columns is easier to reason about: we imagine some (hyper)vector rather than some hypersurface.

## Generalisation

We have considered a system $A \mathbf{x} = \mathbf{b}$. And consider now many such systems (multiple right-hand sides):


$$\begin{align}
A &\mathbf{x_1} &= \mathbf{b_1} \\
  &\vdots       &  \vdots \\
A &\mathbf{x_n} &= \mathbf{b_n}
\end{align}$$

Each row above is a system of equations but can be bundled together in: $A X = B$: here the rows of $B$ are given by $A$, and the columns of $B$ by $X$.

Gaussian elimination allows us to solve one or multiple systems at once.
