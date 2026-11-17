# Exercise 7. Inverse of a Product

## Question

For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

compute $(AB)^{-1}$ and $B^{-1}A^{-1}$. Check that the results are the same and explain the meaning of the reversed order.

## Solution

First let's get $A^{-1}$ and $B^{-1}$ separately.
For $A$, $\det A = 1$, so $A^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}$. Quick check on the whole product:
$$A A^{-1} = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1+0 & -1+1 \\ 0+0 & 0+1 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I \ \checkmark$$

$B$ is diagonal, so we just invert the diagonal entries:
$$B^{-1} = \begin{pmatrix} 1/2 & 0 \\ 0 & 1/3 \end{pmatrix}.$$

Now compute $AB$ first and invert it:
$$AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix} = \begin{pmatrix} 2 & 3 \\ 0 & 3 \end{pmatrix}.$$
Here $\det(AB) = 2 \cdot 3 - 0 = 6$, so:
$$(AB)^{-1} = \frac{1}{6}\begin{pmatrix} 3 & -3 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 1/2 & -1/2 \\ 0 & 1/3 \end{pmatrix}.$$

Now compute $B^{-1}A^{-1}$ in reverse order:
$$B^{-1}A^{-1} = \begin{pmatrix} 1/2 & 0 \\ 0 & 1/3 \end{pmatrix}\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1/2 & -1/2 \\ 0 & 1/3 \end{pmatrix} \ \checkmark$$
They match completely.

**Why the order reverses:**
When the product $AB$ acts on a vector $x$ (so $y = ABx = A(Bx)$), $B$ actually gets applied to $x$ **first**, and then $A$ is applied **second** to the result. To undo the whole process and get $x$ back from $y$, you have to undo the last step first (classic socks-and-shoes rule: you put socks on first then shoes, so you take shoes off first then socks). That means we apply $A^{-1}$ first and $B^{-1}$ second: $x = B^{-1}(A^{-1}y) = (B^{-1}A^{-1})y$. Algebraically too, $(AB)(B^{-1}A^{-1}) = A(BB^{-1})A^{-1} = AIA^{-1} = AA^{-1} = I$.
