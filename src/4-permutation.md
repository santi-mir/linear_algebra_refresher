# Permutations and Transposes

There isn't much to say about _transposes_. We are exchanging rows and columns, and it may be worth remembering the rules on products:

- **Product Inverse**: $(AB)^{-1} = B^{-1}A^{-1}$,
- **Product Transpose**: $(AB)^T = B^T A^T$.

If a matrix is symmetric, this returns itself. What about the product $A A^T$ ? If we transpose it, we see that it's symmtric: $(A A^T)^T = A^{TT} A^T = A A^T$ so the transpose returns the original "untransposed".

## Permutations
Permutation matrices are binary matrices, including the identity.

They are derived from the identity by exchanging rows or columns.

For example, $P_{12}$ below is built permuting row 1 and 2 of the identity. What it does on a matrix $A$ depends on which side it is applied from.

$$P_{12} A = \begin{bmatrix}
0  &  1 \\
1 & 0 \\
\end{bmatrix}
\begin{bmatrix}
a  &  b \\
c & d \\
\end{bmatrix}
= \begin{bmatrix}
c & d \\
a  &  b \\
\end{bmatrix}
$$

And on the right to exchange columns:

$$
A P_{12} =
\begin{bmatrix}
b & a \\
d  &  c \\
\end{bmatrix}
$$

## Some Properties
- These are binary matrices, and they form a group. Applying two or more, yields another one in the group (since we are applying multiple permutations)
- They are all invertible,
- Fact about inverses: $P^{-1} = P^T$. This is because the exchange $P_{ij} = 1, P_{ji} = 0$ inverts what $P_{ij} = 0, P_{ji} = 1$ does,
- The number of them is a factorial. For $3 \times 3$ matrices it's $6$ for $4 \times 4$ it's $24$.

>[!TIP]
> As we considered, the inverses are undoing operations, so the inverse of a permutation matrix does the opposite permutation.
