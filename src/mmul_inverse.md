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
    - Determinant is 0,
    - $A^{-1} A = I$ does not have a solution,
    - If we can find $Ax = 0$ (and $x \neq 0$): then, _if_ there were an inverse $A^{-1} A x = x = 0$ then $x = 0$ which contradicts the first result.

Look at this is using the column picture: a column of A initially and a column of $I$.

$$
\begin{bmatrix}
2 & 3\\
4 & 6
\end{bmatrix}

\begin{bmatrix}
a_1 & a_2\\
a_3 & a_4
\end{bmatrix}

 =
\begin{bmatrix}
1 & 0\\
0 & 1
\end{bmatrix}
$$

We can think of two systems of equations, looking at columns in the RHS. For example:

$$
\begin{bmatrix}
2 & 3\\
4 & 6
\end{bmatrix}

\begin{bmatrix}
a1\\
a3
\end{bmatrix}

 =
\begin{bmatrix}
1 \\
0
\end{bmatrix}
$$

With the columns being multiples of each other, there isn't a solution. Only a case where one column is $k\times [1,0]$ and another is $[0,0]$ would work. But this case won't solve the second one!

> [!TIP]
> So $AX=B$ is a set of $Ax = b$ problems, but instead of solving them separately, they can be solved together / at once, thanks to Gauss-Jordan.

One way to solve all at once is augmenting it with the identity:

$$
\begin{matrix}
1 & 3 & 1 & 0\\
2 & 7 & 0 & 1
\end{matrix}
$$

And perform elimination, until we get:

$$
\begin{matrix}
1 & 0 & 7 & -3\\
0 & 1 & -2 & 1
\end{matrix}
$$

Now

$$
\begin{bmatrix}
1 & 3\\
2 & 7 \\
\end{bmatrix}
\begin{bmatrix}
7 & -3\\
-2 & 1
\end{bmatrix}
$$

Is the identity.

### Why does it work?

We solved $A X = I$, doing $E A X = E$ Since we got to $EA = $, then $E=A-1$.
