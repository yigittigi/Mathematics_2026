# Exercise 14. A System of Equations and the Determinant

## Question

Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

## Solution

For a square matrix $A$, the system $Ax=b$ has exactly one solution for every $b$ if and only if $\det A\neq0$. Here

$$
\det A=1\cdot4-2\cdot k=4-2k
$$

and $4-2k=0$ only for $k=2$. Therefore the system has exactly one solution for every $b$ if and only if $k\neq2$.

For $k=2$ the matrix is

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4 \\
\end{pmatrix}
$$

and its second row is twice the first row. With $x=(x_1,x_2)^T$ and $b=(b_1,b_2)^T$ the system reads

$$
\begin{cases}
x_1+2x_2=b_1, \\
2x_1+4x_2=b_2.
\end{cases}
$$

The left-hand side of the second equation is twice the left-hand side of the first equation, so the system has a solution exactly when $b_2=2b_1$.

**Infinitely many solutions.** For $b=(1,2)^T$ the second equation is twice the first, so only one condition remains:

$$
x_1+2x_2=1
$$

Every vector $x=(1-2s,s)^T$, where $s$ is any real number, satisfies this condition, so the system has infinitely many solutions.

**No solution.** For $b=(1,0)^T$ the system is

$$
\begin{cases}
x_1+2x_2=1, \\
2x_1+4x_2=0.
\end{cases}
$$

Multiplying the first equation by $2$ gives $2x_1+4x_2=2$, which contradicts the second equation $2x_1+4x_2=0$. Hence the system has no solution.
