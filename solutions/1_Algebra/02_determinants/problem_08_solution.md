# Exercise 8. Determinant of a Product

## Question

Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.

## Solution

$$
\det(AB)=\det A\cdot\det B=3\cdot(-5)=-15
$$

$$
\det(BA)=\det B\cdot\det A=(-5)\cdot3=-15
$$

Since $\det A=3\neq0$, the inverse $A^{-1}$ exists, and

$$
\det(A^{-1}B)=\det(A^{-1})\cdot\det B=\frac{\det B}{\det A}=-\frac{5}{3}
$$

Although in general $AB\neq BA$, the two determinants are equal, because each of them is the product of the real numbers $\det A$ and $\det B$, and multiplication of real numbers does not depend on the order.
