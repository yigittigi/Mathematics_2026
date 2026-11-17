# Exercise 5. A 3×3 Matrix

## Question

Use Gauss–Jordan elimination to find the inverse of

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

Check the result by multiplication.

## Solution

Set up $[A \mid I]$:
$$\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 1 & 0 & 1 & 0 & 0 & 1 \end{array}\right)$$

**Step 1:** Clear the $1$ in the bottom-left corner with $R_3 \to R_3 - R_1$:
$$\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & -1 & 1 & -1 & 0 & 1 \end{array}\right)$$

**Step 2:** Clear the $-1$ in row 3 using the second pivot, $R_3 \to R_3 + R_2$:
$$\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 2 & -1 & 1 & 1 \end{array}\right)$$

**Step 3:** Scale row 3 to make the third pivot $1$, $R_3 \to \frac{1}{2}R_3$ (here come the halves):
$$\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right)$$

**Step 4:** Eliminate the $1$ above the third pivot with $R_2 \to R_2 - R_3$:
$$\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & 1/2 & 1/2 & -1/2 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right)$$

**Step 5:** Finally eliminate the $1$ in row 1, column 2 with $R_1 \to R_1 - R_2$:
$$\left(\begin{array}{ccc|ccc} 1 & 0 & 0 & 1/2 & -1/2 & 1/2 \\ 0 & 1 & 0 & 1/2 & 1/2 & -1/2 \\ 0 & 0 & 1 & -1/2 & 1/2 & 1/2 \end{array}\right)$$

Factoring out $1/2$ makes it much cleaner to look at:
$$A^{-1} = \frac{1}{2}\begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix}.$$

Check by multiplying $A A^{-1}$:
$$A A^{-1} = \frac{1}{2}\begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1+1+0 & -1+1+0 & 1-1+0 \\ 0+1-1 & 0+1+1 & 0-1+1 \\ 1+0-1 & -1+0+1 & 1+0+1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{pmatrix} = I \ \checkmark$$
