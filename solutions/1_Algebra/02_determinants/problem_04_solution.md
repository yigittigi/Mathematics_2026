# Exercise 4. Triangular Matrix

## Question

Without expanding the determinant, compute

$$
\det
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7 \\
\end{pmatrix}.
$$

State the rule for an arbitrary triangular matrix and explain it using this example.

## Solution

Denote the given matrix by $A$. The determinant of a triangular matrix is the product of the entries on its main diagonal:

$$
\det A=2\cdot(-3)\cdot7=-42
$$

In general, for an upper or lower triangular $n\times n$ matrix,

$$
\det A=a_{11}a_{22}\cdots a_{nn}
$$

In this example the entries below the main diagonal are zero, so in the expansion of the determinant only the product of the main diagonal entries remains.
