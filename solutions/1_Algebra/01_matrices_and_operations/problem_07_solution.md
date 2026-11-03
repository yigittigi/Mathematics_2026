# Exercise 7. Identity Matrix, Zero Matrix, and Powers

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix},\qquad I=
\begin{pmatrix}
1 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad 0=
\begin{pmatrix}
0 & 0 \\
0 & 0 \\
\end{pmatrix}
$$

## Products with $I$

$$
AI=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=A,\qquad IA=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=A
$$

## Sum with $0$

$$
A+0=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=A
$$

## Powers

$$
A^2=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
$$

$$
A^3=A^2A=
\begin{pmatrix}
4 & 4 \\
0 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 12 \\
0 & 8 \\
\end{pmatrix}
$$

## Roles of $I$ and $0$

The identity matrix $I$ is the neutral element of matrix multiplication, because $AI=IA=A$. The zero matrix $0$ is the neutral element of matrix addition, because $A+0=A$.

## Pattern in the powers

Each power doubles the diagonal entries: $2, 4, 8$. The top-right entry is $1, 4, 12$, which equals $n\cdot2^{n-1}$. This suggests

$$
A^n=
\begin{pmatrix}
2^n & n\cdot2^{n-1} \\
0 & 2^n \\
\end{pmatrix}
$$

Check: for $n=1,2,3$ the formula gives $1$, $4$ and $12$ in the top-right position.
