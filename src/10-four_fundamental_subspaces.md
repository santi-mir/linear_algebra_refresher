# Four Fundamental Subspaces

For $[A] = m\times{}n$:

| rank $\rightarrow$ <br/> dimension $\downarrow$ | $r$ | $n-r$ | $m-r$ |
|--------------------------------------------|-----|-------|-------|
|$R^m$ | $C(A)$            |-|$N(A^T)$|
|$R^n$ | $C(A^T)$,<br/> $R(A)$|$N(A)$|-|

The spaces in the same row (same dimensions) add their ranks up to the dimensionality.

$C(A)$ and $C(A^T)$ have the same _rank_: _we have as many independent rows as we have columns_.

The reduced matrix $R$ has same row space than $A$ but different column space: $C(R^T)=C(A^T)$ and $C(R) \neq C(A)$.


For $N(A)$ we solve $A\mathbf{x} = \mathbf{0}$ (LC of columns giving zero-column). For $N(A^T)$ we solve $A^T\mathbf{x} = \mathbf{0}$ which we can transpose to $\mathbf{x}^TA=\mathbf{0}^T$.

Sadly, the solutions don't have an obvious connection.

> [!IMPORTANT]
> $N(A)$ comes straight from $R$, but $N(A^T)$ from the elimination matrix $E$, in the same row that made that row all zeros!

When reducing $A$ we did $EA = R$ or $EA = I$ for invertible-square matrices (in which case $E=A^{-1}$). Any remaining zeros-row of $R$ must be the free row.

_Why does the row space not change?_ Because by adding and subtracting vectors we never leave the initial space: we are linearly combining vectors in the space and remain in the space!

## Basis and Dimension

The dimension of the column space of $A$ is the rank: $dim(C(A)) = r$. The basis columns are the pivot columns. Rank is the number of them.

The rank of $A^T$ (rank of the row space) is the same as the rank of the column space. The basis rows are the pivot rows. Rank is the number of them.

If we have $r$ independent columns, then we have $r$ independent rows (and the converse). Similarly, we have $n-r$ for the dimension of $N(A)$ and of $N(A^T)$.
