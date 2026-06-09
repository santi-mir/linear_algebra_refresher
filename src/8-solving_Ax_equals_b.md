# Solving Ax=b

Note: I drop the vector notation in some cases, since by now it's obvious from the context when it is a vector or a number.

To maintain the equality, we apply elimination to the augmented matrix (i.e. to both sides) until we get to "$U$".

1. **Particular solution**: We find $\mathbf{x}_p$ by doing back substitution, while setting free variables to $0$.[^1]
2. **Null space**: We add solutions of $A\mathbf{x} = \mathbf{0}$, that is $\mathbf{x} = \mathbf{x_p} + \sum c_i \mathbf{x_i}$ where the sum contains independent vectors from the null space of $A$.

**This isn't a subspace**, it does not contain $\mathbf{0}$.
The solution $\mathbf{x_p}$ is shifting the null-space solution off the origin.

## Solvability

- $\mathbf{b}$ must be in $C(A)$ of $A$,
- If a combination of rows yields the zero-row, the same must be valid for the operations on $\mathbf{b}$ (must be 0).


## Rank (r) and Solutions of A x = b

We know that the number of pivots is always smaller or equal than both $m$ and $n$ &mdash;because at most, the smallest of those is all independent rows/columns, think of the identity formed within.

|Rank | N Solns | Comments |
|-----|---------|----------|
|$r=m=n$ | One   | The null space is the zero vector. Here $R=I$.|
|$r=n<m$ | 0 or 1 ($x_p$) | Only the zero-vector solves null-space of $A$. The matrix $R$ will have some zero rows.|
|$r=m<n$ | $\infty$| We also have $r$ independent columns, then any $b$ is achievable. There will be free variables ($F$) in the reduced row echelon form ($R$), mixed up with the identity, and giving rise to null space solutions. |
|$r<m$ and $r<n$ | 0 or $\infty$ | There will be free variables ($F$) in the reduced row echelon form ($R$), and $R$ will have some zero rows.|


It makes sense to always ask: _What is the maximum number of pivots ?_ This determines the identity and the free variables. If there are, there will be solutions to $Ax=0$ (besides zero-vector).

[^1]: We don't set them to 0 for A x = 0 because that would give the zero-vector only as a solution.
