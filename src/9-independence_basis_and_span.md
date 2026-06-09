# Linear Combinations

## (In)Dependence
A set of vectors is _linearly dependent_ if some linear combination (LC) gives the zero-vector, and _linearly independent_ if none does (besides $\forall_{c_i=0}$).

$$\begin{align}
\sum_i c_i \mathbf{x}_i &= \mathbf{0} \hspace{1em} \text{linear dependence}\\
\sum_i c_i \mathbf{x}_i &\neq \mathbf{0}\hspace{1em} \text{linear independence}
\end{align}
$$

These definitions do not mention matrices, but there is an important connection between linear combinations and matrices.

### Connection to Matrices

- $A\mathbf{c}$ is a linear combination, where the $\{\mathbf{x}_i\}$ vectors are the columns of $A$.

- A $\mathbf{c} = \mathbf{0}$ (null space) solutions beyond $\mathbf{c} = \mathbf{0}$ imply linear dependence.

> [!NOTE]
> _How do we find whether vectors are dependent?_ Put them in the columns of a matrix ($A$) and perform RREF. If there are free variables, the column vectors are dependent.

### The Possible Scenarios

1. If the rank is $r\lt{n}$, the echelon form will have _free variables_.
    - For example, having more rows than columns (more vectors than dimensions), will give linear dependency (e.g. 3 vectors in 2D).
    - Here by eliminating on the extended $A I$, we get $R E$, with $EA=R$; the elimination here is not the inverse of $A$
2. If the rank is $r=n$ the vectors are linearly independent and $N(A)$ is only the zero vector, and the reduced echelon form only contains the identity ($I$) matrix ($F$ is not there). The elimination $E$ here is the identity (if the matrix is square, otherwise it's $E$).

### Other Useful Cases
- **Zero vector in the set** (a column): there is linear dependence. Imagine just one $c_0\times \mathbf{0}$ the rest $c_j$ all zero then the LC is the zero vector.

- **Matrix is square**, independence means we must arrive at $I$ when performing RREF (row reduced echelon form). So we would have performed $EA=I$. Hence $A$ was invertible, and $E$ is its inverse. In other words, for square matrices, independence implies invertible.

- **Two independent vectors in 3D?** Then they will span a plane and be a basis for that subspace. If we add another vector such as the sum of them to the matrix, they won't be a basis any more (they span the same space but aren't independent any more).


## Span, Basis, Dimension

The _span_ of vectors is the linear combination of them. They may be dependent or independent.

The _basis_ is the _smallest set_ of vectors that is:

1. They're _independent_,
2. They _span_ the space.


Some important issues:

- Are basis unique? No.
- How many basis-vectors does an $N$-dimensional space need? Always $N$.
- Conversely, the number basis vectors is the _dimension_ of the space (but they needn't be unique). The basis of $C(A)$ is the number of independent columns: $dim(C(A))=$rank.

>[!NOTE]
> RREF is helping us find independent columns and dependent columns. So it finds basis vectors for space. The pivot columns are for the column space $C(A)$, and the free columns leaves us one step away of the basis for the null space $N(A)$ (changing $F$ signs).
