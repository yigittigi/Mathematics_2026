# Exercise 7. Using Properties Instead of Recomputing

## Question

Suppose that for a $3\times3$ matrix, $\det A=-4$. Compute

$$
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
$$

Justify each answer using the appropriate property.

## Solution

Since $A$ is a $3\times3$ matrix with $\det A=-4$:

For $\det(2A)$, use $\det(cA)=c^n\det A$ with $n=3$:

$$
\det(2A)=2^3\cdot(-4)=-32
$$

For $\det(A^T)$, transposition does not change the determinant:

$$
\det(A^T)=\det A=-4
$$

For $\det(A^2)$, use $\det(AB)=\det A\cdot\det B$ with $B=A$:

$$
\det(A^2)=(\det A)^2=(-4)^2=16
$$

For $\det(-A)$, use $\det(cA)=c^n\det A$ with $c=-1$ and $n=3$:

$$
\det(-A)=(-1)^3\cdot(-4)=4
$$
