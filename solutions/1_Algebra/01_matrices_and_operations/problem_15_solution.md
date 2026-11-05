# Exercise 15. Associativity of Multiplication and Different Calculation Paths

## Question

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## Solution

First compute $AB$, then multiply by $C$:

$$
AB=\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix},\qquad (AB)C=\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

Alternatively, compute $BC$ first:

$$
BC=\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix},\qquad A(BC)=\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}
$$

Both paths give the same matrix, verifying $(AB)C=A(BC)$. Associativity allows changing the parentheses without changing the order of the factors.

Counting ordinary row-column operations without skipping zeros or ones, the first path needs $12+8=20$ multiplications and $8+4=12$ additions. The second needs $12+12=24$ multiplications and $6+8=14$ additions. Thus computing $AB$ first takes fewer operations; its intermediate matrix has four entries instead of six.
