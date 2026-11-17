# Exercise 9. Matrix Equation

## Question

Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

Solve the equation $AX=B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be used. Then check the result by computing $AX$.

## Solution

In $AX = B$, the matrix $A$ is multiplying $X$ from the **left**. Because matrix multiplication isn't commutative, I have to multiply both sides by $A^{-1}$ from the **left** as well to cancel $A$:
$$A^{-1}(AX) = (A^{-1}A)X = IX = X \implies X = A^{-1}B.$$
(If I wrote $BA^{-1}$, $A$ and $A^{-1}$ wouldn't even be next to each other.)

Since $\det A = 1$, the inverse is just:
$$A^{-1} = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}.$$

Now compute $X = A^{-1}B$:
$$X = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix} = \begin{pmatrix} 1\cdot 3 + (-2)\cdot 2 & 1\cdot 1 + (-2)\cdot 4 \\ 0\cdot 3 + 1\cdot 2 & 0\cdot 1 + 1\cdot 4 \end{pmatrix} = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}.$$

Verification — multiply $AX$:
$$AX = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix} = \begin{pmatrix} -1 + 4 & -7 + 8 \\ 0 + 2 & 0 + 4 \end{pmatrix} = \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix} = B \ \checkmark$$
Matches $B$, so $X$ is correct.
