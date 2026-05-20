# Lesson 2: Elimination

Remember that $x$ is a point that solves all equations, say equation $A_i$ for its corresponding $b_i$.

Elimination works as if this solution existed, and operates with pivots: elements on $A$'s diagonal.

- These operations can themselves be encoded as matrices.
- They are row operations; we are modifying both sides of the equality for each equation.
- Each elimination matrix zeros elements of a certain column (below its diagonal element).

## Procedure (Elimination Game)

1. Divide the current pivot row by the pivot (making the pivot $1$),
2. Start with row $1$, and zero all entries below it in column $1$,
3. Move to the next row, row $2$, and zero column $2$ below its diagonal entry ($A_{22}$),
4. If a zero appears on the diagonal, and there is no row below we can swap it with (a permutation), we fail.
5. If we reach an upper triangular matrix $U$, we can back-substitute from the bottom row upward and solve all equations.

So row $N$ always zeros elements below the diagonal entry ($A_{NN}$), which is column $N$.

## Example

- Let
  $$A = \begin{bmatrix}1 & 2 \\ 3 & 4\end{bmatrix}$$
  and suppose we want to eliminate the $3$ below the pivot.
- We use
  $$E_1 = \begin{bmatrix}1 & 0 \\ -3 & 1\end{bmatrix}$$
  and apply it to both $A$ and $b$.
- Then
  $$E_1 A = \begin{bmatrix}1 & 2 \\ 0 & -2\end{bmatrix}$$

This allows us to solve the system easily by back-substitution, since now

$$-2x_2 = c_2'$$

We can also use the augmented matrix:

$$
A_+ =
\begin{bmatrix}
1 & 2 & b_1 \\
3 & 4 & b_2
\end{bmatrix}
$$

The result is an upper triangular matrix $U$, and a transformed vector $c$.

We end up with:

- $E_1$ zeroing entries below $A_{11}$,
- then $E_2$ below $A_{22}$,
- and finally:

$$
E_{N-1} \cdots E_2 E_1 A = E_p A = U
$$

Apparently, calculating $E_p$ directly is not ideal. Instead, we factor:

$$
A = LU
$$

where

$$
L = E_p^{-1}
$$

## Permutations

For example,

$$
\begin{bmatrix}
1 & 0 \\
0 & 1
\end{bmatrix}
$$

is the identity matrix, so

$$
IA = A
$$

while

$$
P =
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
$$

swaps rows:

$$
PA = B
$$

and multiplying on the right swaps columns:

$$
AP = B
$$

This is also pretty awesome.
