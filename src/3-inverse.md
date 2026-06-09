# The Inverse of A

Inverses are a special case of $A X = B$ where $B = I$, that is, $A X = I$. To solve it we use a modified elimination process: the Gauss-Jordan elimination:

1. We solve $A X = I$ by eliminating on $A$ until it becomes $I$ while operating in the RHS $\left(I\right)$.
2. We can depict this with augmented matrices: $\left[A \,|\, I\right] \rightarrow_E \left[I \,|\, ? \right]$.
    - The left hand side has $A \rightarrow_E I$
    - Then right hand side is $ I\rightarrow_E A^{-1}$.
3. Which is also equal to $X$ (showing inverse applies both sides).


A matrix is a linear transformation of a vector or matrix: $A \mathbf{b} = \mathbf{c}$ or $A B = C$.
An inverse is undoing this transformation, so we recover the initial vector or matrix:
$A^{-1} \mathbf{c} = \mathbf{b} $ or $A^{-1} C = B$.

Interestingly, some are unrecoverable; an easy example is $A \mathbf{b} = 0$ (assume $\mathbf{b}$ isn't $\mathbf{0}$).

### When there isn't an inverse?

- Case 1: If the system of equations (with multiple right hand sides) $A^{-1} A = I$ does not have a solution,
- Case 2: If $A\mathbf{x} = 0$ with $\mathbf{x} \neq \mathbf{0}$, then, assuming $A^{-1} A \mathbf{x} = \mathbf{x} = \mathbf{0}$ implies $\mathbf{x} = \mathbf{0}$ which contradicts the first result,
    - In other words, if $A\mathbf{x} = 0$ the inverse of $A$ does not exist.
- Case 3: If the determinant is 0.

## Example: Linear Dependency of Columns

We split a full system into system 1 and 2:

**System 1**:

$$
\begin{bmatrix}
2 & 3 \\
4 & 6
\end{bmatrix}
\begin{bmatrix}
a1\\
a3
\end{bmatrix} = \begin{bmatrix}
1\\
0
\end{bmatrix}
$$

**System 2**:

$$
\begin{bmatrix}
2 & 3 \\
4 & 6
\end{bmatrix}
\begin{bmatrix}
a2\\
a4
\end{bmatrix} = \begin{bmatrix}
0\\
1
\end{bmatrix}
$$

_Even if_ the linear combination of columns of system 1 takes us to $1,0$ it can only take use to points in the line that goes through $0,0$ and $1,0$ so it can not give us $0,1$.

Hence if the columns are linear combinations of each other, there isn't an inverse. It's like it removes one "direction". Performing elimination on $A$ would similarly fail.


## Useful Matrix Products

Both of these "distribute" while reversing the order of the product:

- **Product Inverse**: $(AB)^{-1} = B^{-1}A^{-1}$.
    - *Inverse both ways*: if we have $A A^{-1} = I$ then $A^{-1} A = I$.
- **Product Transpose**: $(AB)^T = B^T A^T$.
    - *Inverse of the transpose*: If we have $A^{-1} A = I$, using the above rule gives $A^T A^{-1^T} = I$. Knowing the inverse of $A$, we get the inverse of $A^T$ for free.
