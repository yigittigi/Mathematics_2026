# Exercise 12. Finding Inverses Without Starting from Scratch

## Question

It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

Without finding $A$, compute $(3A)^{-1}$, $(A^T)^{-1}$, and $(A^2)^{-1}$. Justify each result using the appropriate property.

## Solution

No need to invert $A^{-1}$ back to $A$ — we can just use the standard inverse rules directly on $A^{-1}$.

**1) $(3A)^{-1}$:**
Rule: For any nonzero scalar $c$, $(cA)^{-1} = \frac{1}{c}A^{-1}$ (if a matrix scales everything by $3$, its inverse has to divide by $3$).
$$(3A)^{-1} = \frac{1}{3}A^{-1} = \frac{1}{3}\begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} = \begin{pmatrix} 2/3 & -1/3 \\ -1 & 2/3 \end{pmatrix} \ \checkmark$$

**2) $(A^T)^{-1}$:**
Rule: Transposition and inversion commute, i.e., $(A^T)^{-1} = (A^{-1})^T$ (since $A^T(A^{-1})^T = (A^{-1}A)^T = I^T = I$). So I just transpose the given $A^{-1}$:
$$(A^T)^{-1} = (A^{-1})^T = \begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix} \ \checkmark$$

**3) $(A^2)^{-1}$:**
Rule: Using the product rule $(AB)^{-1} = B^{-1}A^{-1}$ with $B = A$, we get $(A^2)^{-1} = (AA)^{-1} = A^{-1}A^{-1} = (A^{-1})^2$. So we just square $A^{-1}$:
$$(A^2)^{-1} = \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}\begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} = \begin{pmatrix} 4 + 3 & -2 - 2 \\ -6 - 6 & 3 + 4 \end{pmatrix} = \begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix} \ \checkmark$$
