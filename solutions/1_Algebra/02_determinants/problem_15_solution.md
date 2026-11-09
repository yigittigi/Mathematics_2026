# Exercise 15. Combining Determinant Properties

## Question

Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.

## Solution

The following properties are used, in this order:

1. Product rule: $\det(XY)=\det X\cdot\det Y$ for square matrices of the same size. Applied twice, it splits the determinant of a product of three matrices into a product of three determinants.
2. Determinant of the inverse: $\det(B^{-1})=\frac{1}{\det B}$. This follows from $BB^{-1}=I$, because $\det B\cdot\det(B^{-1})=\det I=1$.
3. Determinant of the transpose: $\det(A^T)=\det A$.

Applying these properties gives

$$
\begin{aligned}
\det\left(B^{-1}A^TB\right) &= \det(B^{-1})\cdot\det(A^T)\cdot\det B \\
&= \frac{1}{\det B}\cdot\det A\cdot\det B \\
&= \frac{1}{3}\cdot(-2)\cdot3 \\
&= -2
\end{aligned}
$$

After the product rule is applied, every factor is a real number, and multiplication of real numbers is commutative. The factors $\frac{1}{\det B}$ and $\det B$ can therefore be multiplied together first, and their product is $1$. This is why the factors involving $B$ cancel and

$$
\det\left(B^{-1}A^TB\right)=\det A=-2
$$

This holds even though the matrix $B^{-1}A^TB$ is in general different from $A^T$, because matrix multiplication is not commutative.
