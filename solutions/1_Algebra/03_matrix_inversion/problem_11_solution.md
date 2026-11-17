# Exercise 11. Parameter and Invertibility

## Question

For

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}
$$

find all $t$ for which the matrix is invertible, and then give a formula for $A(t)^{-1}$. Explain what happens to this formula at the excluded values.

## Solution

A matrix is invertible precisely when its determinant is nonzero. Let's compute $\det A(t)$:
$$\det A(t) = 1 \cdot 1 - t \cdot t = 1 - t^2 = (1 - t)(1 + t).$$

We need $1 - t^2 \neq 0$, which means $t^2 \neq 1$. So **$A(t)$ is invertible for all $t \neq 1$ and $t \neq -1$**.

For any $t \notin \{-1, 1\}$, the 2×2 inverse formula gives:
$$A(t)^{-1} = \frac{1}{1 - t^2}\begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}.$$

Quick check that $A(t)A(t)^{-1} = I$:
$$\frac{1}{1 - t^2}\begin{pmatrix} 1 & t \\ t & 1 \end{pmatrix}\begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix} = \frac{1}{1 - t^2}\begin{pmatrix} 1 - t^2 & -t + t \\ t - t & -t^2 + 1 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I \ \checkmark$$

**What happens at the excluded values ($t = \pm 1$):**
- **To the formula:** If we plug $t = 1$ or $t = -1$ into the formula for $A(t)^{-1}$, the denominator $1 - t^2$ becomes $1 - 1 = 0$. The scalar factor $\frac{1}{1-t^2}$ turns into division by zero ($\frac{1}{0}$), so the formula completely breaks down and is undefined.
- **To the matrix:** At $t = 1$, $A(1) = \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix}$ ($R_1 = R_2$), and at $t = -1$, $A(-1) = \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix}$ ($R_2 = -R_1$). In both cases the rows become linearly dependent, the rank drops to $1$, and the matrix squashes $\mathbb{R}^2$ onto a single line, so it cannot be inverted.
