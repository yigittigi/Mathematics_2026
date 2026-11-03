# Exercise 6. Transpose

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

## Transposes

$$
A^T=
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix},\qquad B^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
$$

## Product $AB$

$$
AB=
\begin{pmatrix}
2 & 11 \\
8 & 23 \\
\end{pmatrix},\qquad (AB)^T=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

## Verification of $(AB)^T=B^TA^T$

$$
B^TA^T=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 1 & 3 \\
\end{pmatrix}
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 8 \\
11 & 23 \\
\end{pmatrix}
$$

Therefore

$$
(AB)^T=B^TA^T
$$

Transposing a product reverses the order of the factors.
