# Elimination, Factorisation

Let's first refresh matrix multiplication.

## Background: Matrix-Matrix operations

When multiplying matrices we can apply the same conceptual model as with Matrix-Vector operations. We can look at them as **combining rows or columns** of one or the other matrix.

Ways to look at the matrix multiplication $C = A B$:

| Cell of C | Col$_i$ of C| Row$_i$ of C | Sum of Matrices | Blocks |
|-----------|-----------|------------|-------|-------|
|$C_{ik} = \sum_j A_{ij} B_{jk}$| LC of elements in col $i$ of $B$ with column vectors of $A$| LC of elements in row $i$ of $A$ with rows vectors of $B$| Sum of columns of $\mathbf{a}^{[m,1]}$ times rows of $\mathbf{b}^{[1,n]}$ and yields a full matrix ($[m,n]$), so this is a sum of matrices| Splits the matrices and multiply the splits using an analogous of the "element-wise" algorithm, and finally join the results


Many special matrices such as &mdash;elimination, permutation, scaling and rotation matrices&mdash; can be looked at from the conceptual view of the second and third columns.


## Elimination: Solving for x

Elimination is one method to solve for point $\mathbf{x}$ (which solves all equations in the system) when it exists, and it fails otherwise.

- We _record_ the elimination process in _elimination matrices_ ($E$), which zeros elements of a certain column below its diagonal element.
- The total elimination process is a product $E_p = \prod_{ij} E_{ij}$, we can also write it as:

$$ A \mathbf{x} = \mathbf{b} \\
E_p A \mathbf{x} =  E_p \mathbf{b} \\
U \mathbf{x} = c
$$

We can now back-substitute and find $\mathbf{x}$, unless the method fails.

## Factorisation: One Extra Step

_Factorisation involves an extra step from elimination. That is their connection_. Let's see this in steps:

1. Elimination is: $E_p A \mathbf{x} = U\mathbf{x} = E\mathbf{b}$,
2. Get its inverse changing a sign on each step: $E_p^{-1} = E_{21}^{-1}\ldots{}E_{ij}^{-1}$,
     - Rename it to $L = E_p^{-1}$,
3. We have $E_p A = U$, then $I A = LU$.

In other words, $L$ is the inverse of the elimination matrix (either each factor or the total).

We can also get $A = LDU$ where $D$ is diagonal, and another much more useful (because it's very common in practise) is the $PA = LU$ allowing for permutations of rows.



