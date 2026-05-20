# Lecture 3: MMul and Inverse

## Four ways of MMul
There are four ways to multiply matrices `AB=C`, summarised with respect to what part of `C` they calculate, as follows:

1. Elements of C: `Cij` as the dot product of `Row i of A` and `Column j of B`,
2. Rows of C: `Row i of C` as the result of `Row i of A` linearly combining `rows of B`
3. Columns of C: `Column i of B` linearly combines `Columns of A` and yields `Column i of C`.
4. Matrix-sums: `Column i of A` and `Row i of B` produce a matrix, and we sum `n` matrices.

Always the constrain in shape is `[A]=mxn` and `[B]=nxk`, that is, `Cols of A` must match `rows of B`.

Block Multiplication is another method, non-obvious one; each matrix is split and "rows x columns" gives each result. In this case, they are all matrices though.


## Inverses

- Invertible == Non-Singular
- Non-Invertible == Singular.
    - Determinant is 0
    - `A-1 A = I` does not have a solution.
    - If we can find `Ax = 0` (and `x != 0`): then, _if_ there were an inverse `A-1 A x = x = 0` then `x = 0` which contradicts the first result.

Look at this is using the column picture: a column of A initially and a column of `I`.

$$
\begin{matrix}
2 & 3\\
4 & 6
\end{matrix}

\begin{matrix}
a1 & a2\\
a3 & a4
\end{matrix}

 =
\begin{matrix}
1 & 0\\
0 & 1
\end{matrix}
$$

We can think of two systems of equations, looking at columns in the RHS. For example:

$$
\begin{matrix}
2 & 3\\
4 & 6
\end{matrix}

\begin{matrix}
a1\\
a3
\end{matrix}

 =
\begin{matrix}
1 \\
0
\end{matrix}
$$

With the columns being multiples of each other, there isn't a solution. Only a case where one column is `k*[1,0]` and another is `[0,0]` would work. But this case won't solve the second one!

> [!TIP]
> So `AX=B` is a set of `Ax = b` problems, but they can be solved together.
