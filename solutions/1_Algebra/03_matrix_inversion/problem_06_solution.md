# Exercise 6. Solving a System Using the Inverse

## Question

Solve

$$
Ax=b,
$$

where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix},
$$

using $x=A^{-1}b$. Then substitute the resulting vector back into the equation and check the result.

## Solution

First find $A^{-1}$ with the 2×2 formula. The determinant is $\det A = 2 \cdot 3 - 1 \cdot 1 = 6 - 1 = 5$. So:
$$A^{-1} = \frac{1}{5}\begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}.$$

Now multiply $x = A^{-1}b$:
$$x = \frac{1}{5}\begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}\begin{pmatrix} 5 \\ 7 \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 3 \cdot 5 + (-1) \cdot 7 \\ (-1) \cdot 5 + 2 \cdot 7 \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 15 - 7 \\ -5 + 14 \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 8 \\ 9 \end{pmatrix} = \begin{pmatrix} 8/5 \\ 9/5 \end{pmatrix}.$$

Substitute $x = (8/5, 9/5)$ back into $Ax$ to check:
- Row 1: $2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) = \frac{16 + 9}{5} = \frac{25}{5} = 5$ ✓
- Row 2: $1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) = \frac{8 + 27}{5} = \frac{35}{5} = 7$ ✓

Both equations give $b = (5, 7)$, so the solution is right.
