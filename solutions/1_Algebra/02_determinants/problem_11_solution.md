# Exercise 11. Shortening the Calculation with Row Operations

## Question

Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## Solution

Denote the given matrix by $A$. All three rows begin with $1$, so subtracting the first row from the other rows creates two zeros in the first column at once. Only operations of the form $R_i\leftarrow R_i+cR_j$ with $i\neq j$ are used; adding a multiple of one row to another row does not change the determinant.

**Step 1.** $R_2\leftarrow R_2-R_1$ and $R_3\leftarrow R_3-R_1$:

$$
\det A=\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 2 & 3 \\
\end{pmatrix}
$$

**Step 2.** $R_3\leftarrow R_3-2R_2$ creates a third zero below the main diagonal:

$$
\det A=\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

The resulting matrix is upper triangular, so its determinant is the product of the diagonal entries:

$$
\det A=1\cdot1\cdot1=1
$$

Among the elementary row operations, the ones that do not change the determinant are the row additions $R_i\leftarrow R_i+cR_j$ with $i\neq j$; these are the only operations used here. Swapping two rows would change the sign of the determinant, and multiplying a row by $c\neq0$ would multiply the determinant by $c$.
