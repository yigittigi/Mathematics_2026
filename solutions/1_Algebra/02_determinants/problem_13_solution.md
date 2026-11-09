# Exercise 13. Determinant by Elimination

## Question

Compute the determinant of

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.

## Solution

The matrix is reduced to upper triangular form. Every operation below adds a multiple of one row to another row, and an operation of this type does not change the determinant.

**Step 1.** $R_2\leftarrow R_2-2R_1$; the determinant does not change:

$$
\det A=\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

**Step 2.** $R_3\leftarrow R_3-R_1$; the determinant does not change:

$$
\det A=\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & -2 & -1 \\
\end{pmatrix}
$$

**Step 3.** $R_3\leftarrow R_3+2R_2$; the determinant does not change:

$$
\det A=\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 1 \\
0 & 0 & 1 \\
\end{pmatrix}
$$

No row swaps or row scalings were used, so no sign change or extra factor appears. The final matrix is upper triangular, and its determinant is the product of the diagonal entries:

$$
\det A=1\cdot1\cdot1=1
$$
