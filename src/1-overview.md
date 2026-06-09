# Lesson 1: Overview

_Brief summary of most important aspects of linear algebra._

---------------------

## Equations: Lines, Planes, and Hyperplanes

- **Line** is a linear equation of two variables: $a_1 x_1 + a_2 x_2 = b$,
- **Plane** is a linear equation of three variables: $a_1 x_1 + a_2 x_2 + a_3 x_3 = b$,
- **Hyperplane** is a linear equation of more variables: $ a_1 x_1 + \ldots + a_n x_n = b$.

They can be written as $\mathbf{a}^T \mathbf{x} = b$. An interesting result is that:

$$
\begin{align}
\mathbf{a}^T \mathbf{x} &= b\\
\mathbf{a}^T \mathbf{x_0} &= b\\
\mathbf{a}^T (\mathbf{x}-\mathbf{x_0}) &= 0\\
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

_Solving_ the system of equations means finding the values of $x_i$ that solves _all_ equations at once.
A unique solution requires $N$ surfaces (for $N$ variables) that all intersect at a point. For example, two lines, three planes and so forth.

_Square systems_ are those with the same number of equations an unknowns. For a unique solution, we require $N$ surfaces (for $N$ variables) that all intersect at a point.


> [!IMPORTANT]
> We can't easily visualise linear equations for $N\gt{}3$.

### Ways to Look at Systems

- **Equation Picture** (elements): a linear combination of the row-elements of $A$ and the coefficients
    - Gilbert Strang calls this one the row picture,
    - This is less useful because in a sense we are thinking of surfaces (each equation).
- **Column Picture** (vectors): a linear combinations of the column-vectors of $A$ and the coefficients $x_i$ written as $\sum A_{col_i} \, x_i =  \mathbf{b}$,
- **Row Picture** (vectors): a linear combination of the row-vectors of $A$ and the coefficients $x_i$.

> [!IMPORTANT]
> The vector-pictures are easier to reason about: we extrapolate from 2D or 3D vectors rather than from surfaces (equation picture).
>
> The vector pictures also helps us thing of the _span_: For $A\mathbf{x} = \mathbf{b}$, the columns of $A$ _span_ all the N-D space, there are $x_i$ values solving for _any_ $\mathbf{b}$. A similar statement is valid for the row picture.
>
> The vector picture is the goat.

## Multiple Right Hand Sides

We have considered a system $A \mathbf{x} = \mathbf{b}$. And consider now many such systems:


$$\begin{align}
A &\mathbf{x_1} &= \mathbf{b_1} \\
  &\vdots       &  \vdots \\
A &\mathbf{x_n} &= \mathbf{b_n}
\end{align}$$

Where _each row above is a system of equations_, since $\mathbf{x_i}, \mathbf{b_i}$ are all vectors.

The multiple systems can be bundled together in: $A X = B$. Gaussian elimination allows us to solve one or multiple systems at once.
