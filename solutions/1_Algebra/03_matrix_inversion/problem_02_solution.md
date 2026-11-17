# Exercise 2. Formula for a 2×2 Matrix

## Question

Find the inverse of

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}
$$

using the formula for a $2\times2$ matrix. At the end, check the result by computing one product with $A$.

## Solution

For a 2×2 matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the inverse formla is
$$A^{-1} = \frac{1}{ad - bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.$$

Here $a = 3, b = 2, c = 5, d = 4$. First I check the determinant:
$$\det A = 3 \cdot 4 - 2 \cdot 5 = 12 - 10 = 2 \neq 0.$$
Nonzero, so the inverse exists (and dividing by 2 isn't too bad). Swapping the main diagonal and flipping the signs on the off-diagonal:
$$A^{-1} = \frac{1}{2}\begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix} = \begin{pmatrix} 2 & -1 \\ -5/2 & 3/2 \end{pmatrix}.$$

Check by multipying $A A^{-1}$:
- $(1,1)$: $3 \cdot 2 + 2 \cdot (-5/2) = 6 - 5 = 1$ ✓
- $(1,2)$: $3 \cdot (-1) + 2 \cdot (3/2) = -3 + 3 = 0$ ✓
- $(2,1)$: $5 \cdot 2 + 4 \cdot (-5/2) = 10 - 10 = 0$ ✓
- $(2,2)$: $5 \cdot (-1) + 4 \cdot (3/2) = -5 + 6 = 1$ ✓

We get $I$, so $A^{-1}$ is right.
