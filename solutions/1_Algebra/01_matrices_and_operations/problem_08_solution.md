# Exercise 8. Row Operations and Their Reversibility

## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order: (1) $R_2\leftarrow R_2-2R_1$, (2) $R_3\leftarrow R_3+R_1$, (3) interchange $R_2$ and $R_3$. Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

Applying the operations in order gives:

$$
A_1=\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix},\qquad A_2=\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix},\qquad A_3=\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

The reverse operations are $R_2\leftarrow R_2+2R_1$, $R_3\leftarrow R_3-R_1$, and swapping $R_2,R_3$ again. Applying these in reverse order returns the original matrix.
