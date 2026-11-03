# Exercise 5. Matrix Times Vector

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}
$$

## Product $Ax$

$$
Ax=
\begin{pmatrix}
2\cdot4+(-1)\cdot2 \\
1\cdot4+3\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

## Linear combination of columns

The columns of $A$ are

$$
c_1=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\qquad c_2=
\begin{pmatrix}
-1 \\
3 \\
\end{pmatrix}
$$

The coefficients are the entries of $x$:

$$
Ax=4c_1+2c_2=
\begin{pmatrix}
8 \\
4 \\
\end{pmatrix}+
\begin{pmatrix}
-2 \\
6 \\
\end{pmatrix}=
\begin{pmatrix}
6 \\
10 \\
\end{pmatrix}
$$

Both methods give the same result, which verifies the computation.
