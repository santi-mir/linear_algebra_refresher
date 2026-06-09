# Null Space Solutions

_This is a critical lesson, which increases the complexity, and most concepts are needed going forward._

------------

## Review
We are now dealing with rectangular matrices $[A]=m\times{}n$.

The null space of a matrix is the linear combination of columns that solve $A\mathbf{x} = \mathbf{0}$. As a reminder:

- The _LC of columns_ $A\mathbf{x}$ forms a space, called the column space of $A$, denoted $C(A)$. This is not directly related to any equation,
- The _solutions_ for $A\mathbf{x} = \mathbf{b}$ don't form a space: they don't contain the $\mathbf{x}$ (unless $\mathbf{b}=\mathbf{0}$),
- The _solutions_ of $A\mathbf{x} = \mathbf{0}$ do form a space, called the null space of $A$. **This is what we explore here.**

## Uses of N(A)

- The general solution to $A\mathbf{x}=\mathbf{b}$ is $\mathbf{x} = \mathbf{x}_p + \sum_i c_i\,\mathbf{x}_i$ where the sum is over solutions to the null space, and $x_p$ is a particular solution to the system,
- If $A\mathbf{x} = \mathbf{0}$ has a solution, the column vectors of $A$ are linearly dependent, so it's is a linear dependence test,
 (e.g. $n\gt{}m$ has $r\leq{}m$, we have at most $r$ independent columns).

## Finding the Null Space of A
To find $N(A)$[^1] we solve $A\mathbf{x} = \mathbf{0}$ through Gaussian elimination. In the process, we find:

- **Pivot columns** are those columns with non-zeros in the pivot position. The values of the variables are found by solving the system.
- **Free columns** are those columns with non-zeros in the pivot position. The values of the variables can be freely chosen.
  - And it's best to choose values making an identity matrix.

Tip: There are as many pivot rows as there are pivot columns.

### Row Echelon Form of A

By elimination on $A$, we arrive to its _echelon_ form (not $U$) meaning staircase-shaped. But we _still_ call it $U$.

We solve $U\mathbf{x} = \mathbf{0}$ by back-substitution, and by giving _free variables_ &mdash;those multiplying the free columns&mdash; any values we want.

Finding a solution $\mathbf{x}_0$ implies $c\mathbf{x}_0$, so we get families of solutions. We better choose the simplest values for the free variables.

> [!NOTE]
> We can build one solution-family per free variable. But we must choose those to be independent directions.

- Rank $r$ of A: Number of pivots,
- $n-r$ free variables (for $n$ columns),
- We got to $U\mathbf{x} = \mathbf{0}$ (Remember: "$U$").

### Reduced Row Echelon Form of A

Continue performing elimination upwards (Gauss-Jordan), and dividing the pivot-rows by the pivot value (to make the pivot a $1$).

Usually, the resulting matrix ($R$) contains $I$ in the _pivot_ rows / columns (with _free_ columns / rows in between).

We get to $R\mathbf{x} = 0$. Think of the linear combination (sum), we can pass the free variables to the right, and get $I \mathbf{x}_{pivot} = -F \mathbf{x}_{free}$. If we choose the free variables as hot encoded vectors, we basically use $-F$ as a solution. This means the solution was already in $R$. In other words:

> [!NOTE]
> The solution is already included in the reduced matrix $R$, we just change the signs of the free variables.

We can then group these solutions so that $A N = 0$ where $X=N$ are independent null space vectors, and the space is a linear combination of the columns of $N$.

[^1]: Vectors that $A$ takes to the origin, or that take columns of $A$ to the origin vector.
