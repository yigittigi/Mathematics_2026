# Exercise 15. Two Methods for Solving the Same System

## Question

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

solve $Ax=b$ in two ways:

1. using $A^{-1}b$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Solution

**Method 1: Using the inverse ($x = A^{-1}b$).**
1. Compute $\det A = 2 \cdot 3 - 1 \cdot 1 = 5$ and form $A^{-1} = \frac{1}{5}\begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}$ (which we also already had from Exercise 6).
2. Multiply $A^{-1}$ by $b = (7, 8)$:
$$x = A^{-1}b = \frac{1}{5}\begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}\begin{pmatrix} 7 \\ 8 \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 21 - 8 \\ -7 + 16 \end{pmatrix} = \frac{1}{5}\begin{pmatrix} 13 \\ 9 \end{pmatrix} = \begin{pmatrix} 13/5 \\ 9/5 \end{pmatrix}.$$

**Method 2: Gaussian elimination.**
Set up $[A \mid b]$, swap rows to get a pivot of $1$, and eliminate below:
$$\left(\begin{array}{cc|c} 2 & 1 & 7 \\ 1 & 3 & 8 \end{array}\right) \xrightarrow{R_1 \leftrightarrow R_2} \left(\begin{array}{cc|c} 1 & 3 & 8 \\ 2 & 1 & 7 \end{array}\right) \xrightarrow{R_2 \to R_2 - 2R_1} \left(\begin{array}{cc|c} 1 & 3 & 8 \\ 0 & -5 & -9 \end{array}\right).$$
Back-substitution:
- From row 2: $-5x_2 = -9 \implies x_2 = \frac{9}{5}$.
- From row 1: $x_1 + 3\left(\frac{9}{5}\right) = 8 \implies x_1 = \frac{40}{5} - \frac{27}{5} = \frac{13}{5}$.

Both methods give $x = (13/5, 9/5)$ ✓. (Check in row 1: $2(13/5) + 9/5 = 35/5 = 7$ ✓.)

**Comparison of steps and which is simpler here:**
- **Step count:** Starting from scratch, both take roughly 2–3 short steps for a 2×2 system: Method 1 takes 2 steps (1: determinant + 2×2 swap/sign-flip formula, 2: one matrix-vector product), while Method 2 takes 3 steps (1: row swap, 2: one row elimination $R_2 - 2R_1$, 3: back-substitution with fractions).
- **Which is simpler in this example:** **Method 1 ($x = A^{-1}b$) is definitely simpler here**, first because we already computed $A^{-1}$ back in Exercise 6 (so it took just a single multiplication!), and second because even from scratch on a 2×2 matrix, keeping the $\frac{1}{5}$ outside until the very end avoids doing fraction arithmetic during back-substitution like $8 - 3(9/5)$. (For larger 3×3 or $n \times n$ matrices with a single $b$, Gaussian elimination wins easily.)
