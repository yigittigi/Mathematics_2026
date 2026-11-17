# Exercise 3. When Does the Inverse Not Exist?

## Question

For

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}
$$

explain in two ways why $A^{-1}$ does not exist: using the determinant and using dependence between the rows.

## Solution

**1) Via the determinant:**
$$\det A = 2 \cdot 2 - 4 \cdot 1 = 4 - 4 = 0.$$
Since the 2×2 inverse formula divides by $\det A$, we would be dividing by zero. A matrix with determinant $0$ collapses area to zero and cannot be inverted.

**2) Via row dependence:**
Looking at the rows, row 1 is $[2, 4]$ and row 2 is $[1, 2]$, so $R_1 = 2R_2$. The rows are linearly dependent (if we did elimination, $R_1 - 2R_2$ would give a row of all zeros, so we can never reach $I$). Because of this redundancy, $Ax = 0$ has nontrivial solutions — for example $x = (2, -1)$ gives
$$\begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix}\begin{pmatrix} 2 \\ -1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \end{pmatrix}.$$
Since both $(2, -1)$ and $(0, 0)$ get sent to the exact same output $(0, 0)$, there is no way to reverse the transformation uniquely, so $A^{-1}$ cannot exist.
