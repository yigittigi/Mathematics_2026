# Exercise 1. Definition of the Inverse

## Question

For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}
$$

check, without using a formula, whether $B=A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## Solution

I just multiplied them out entry by entry without touching the 2x2 formula.

First, for $AB$:
- $(1,1)$: $2 \cdot 1 + 1 \cdot (-1) = 2 - 1 = 1$
- $(1,2)$: $2 \cdot (-1) + 1 \cdot 2 = -2 + 2 = 0$
- $(2,1)$: $1 \cdot 1 + 1 \cdot (-1) = 1 - 1 = 0$
- $(2,2)$: $1 \cdot (-1) + 1 \cdot 2 = -1 + 2 = 1$

So $AB = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$.

Now $BA$ the exact same way:
- $(1,1)$: $1 \cdot 2 + (-1) \cdot 1 = 2 - 1 = 1$
- $(1,2)$: $1 \cdot 1 + (-1) \cdot 1 = 1 - 1 = 0$
- $(2,1)$: $(-1) \cdot 2 + 2 \cdot 1 = -2 + 2 = 0$
- $(2,2)$: $(-1) \cdot 1 + 2 \cdot 1 = -1 + 2 = 1$

So $BA = I$ as well. By definition, the inverse of $A$ is the unique matrix that satisfies $AB = BA = I$. Since both products give the identity matrix, yes, $B = A^{-1}$ ✓.
