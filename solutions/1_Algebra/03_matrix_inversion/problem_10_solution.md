# Exercise 10. Inverse of a Diagonal Matrix

## Question

Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

## Solution

A diagonal matrix scales each coordinate axis independently, and its determinant is just the product of the diagonal entries. So it's invertible if and only if none of the diagonal entries are zero.

- **$D$ is invertible** because all three diagonal entries ($2, -3, 5$) are nonzero ($\det D = -30 \neq 0$).
- **$E$ is not invertible** because the middle diagonal entry is $0$ ($\det E = 0$). It crushes the second component of any vector to $0$, so there is no way to recover it.

To invert $D$, we just take the reciprocal of each diagonal entry:
$$D^{-1} = \begin{pmatrix} 1/2 & 0 & 0 \\ 0 & -1/3 & 0 \\ 0 & 0 & 1/5 \end{pmatrix}.$$

Check by multiplying $D D^{-1}$:
$$D D^{-1} = \begin{pmatrix} 2 & 0 & 0 \\ 0 & -3 & 0 \\ 0 & 0 & 5 \end{pmatrix}\begin{pmatrix} 1/2 & 0 & 0 \\ 0 & -1/3 & 0 \\ 0 & 0 & 1/5 \end{pmatrix} = \begin{pmatrix} 2(1/2) & 0 & 0 \\ 0 & (-3)(-1/3) & 0 \\ 0 & 0 & 5(1/5) \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = I \ \checkmark$$
