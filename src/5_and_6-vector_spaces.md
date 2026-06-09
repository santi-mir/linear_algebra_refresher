# Vector Spaces and Subspaces

A vector space is a set of vectors that:

- Can be **linearly combined**,
- **Contain the origin**: One vector in the space must be the zero vector / origin: $\mathbf{0}$,
- **Form a closed space**: The linear combinations must stay in the space.
  - For example, $N^N$ does not form a space if integers are allowed as coefficients $a$ (it can take us to negatives.)

We can think of the full space as all the possible combinations of values of the components of the vector; for a vector with 3 components is 3D space.

## Subspaces
Subspaces are _spaces within a larger space_; the 4 properties above are required.

The linear combination may not span the full space given by the vector's dimensions (say $R^N$).

Intersection and union of subspaces, the former forms a new subspace, the latter not.

## Subspaces

Note: to be a vector space (or subspace), is must follow the 4 rules.

### C(A)

This subspace is formed by the linear combination of the columns of $A$, and denoted $C(A)$, which we can write as $A\mathbf{x}$. We don't look at a particular system with a defined $\mathbf{b}$.

Where it relates to the linear system is in that _we can only solve_ $A\mathbf{x} = \mathbf{b}$ _if_ $\mathbf{b}$ _is in_ $C(A)$, but we are not caring about  _a specific_ $\mathbf{b}$.

Later we will consider whether all columns of $A$ are needed, or some can be thrown away.

### N(A)

This subspace is formed by the solutions $\mathbf{x}$, and written $N(A)$, rather than combining columns.

Rather than looking at $A\mathbf{x}$ we look at all the solutions for $A\mathbf{x}=\mathbf{0}$.

We can see $\mathbf{0}$ is a solution. (Look at some examples to see how it works.)

We could look whether the solutions $\mathbf{x}$ for other $\mathbf{b}$ form a subspace but they won't, because it needs to contain $\mathbf{0}$ which can only solve $A\mathbf{x} = \mathbf{0}$.

>[!IMPORTANT]
> Why doesn't $x$ in $A\mathbf{x}=\mathbf{b}$ form a subspace, but it does in $A\mathbf{x}=\mathbf{0}$?
>
> Because to contain the origin means $\mathbf{x}=\mathbf{0}$; however, $A\mathbf{0} = \mathbf{b}$ is only valid in the second case!
