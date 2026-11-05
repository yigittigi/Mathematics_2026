# Exercise 2. Addition and Scalar Multiplication

## Question

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

## Solution

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

## Sum

$$
A+B=
\begin{pmatrix}
5 & 0 \\
-1 & 8 \\
\end{pmatrix}
$$

## Difference

$$
A-B=
\begin{pmatrix}
-3 & 4 \\
-1 & -2 \\
\end{pmatrix}
$$

## Linear combination

$$
3A=
\begin{pmatrix}
3 & 6 \\
-3 & 9 \\
\end{pmatrix},\qquad 2B=
\begin{pmatrix}
8 & -4 \\
0 & 10 \\
\end{pmatrix}
$$

$$
3A-2B=
\begin{pmatrix}
-5 & 10 \\
-3 & -1 \\
\end{pmatrix}
$$

## Explanation

Matrix addition is performed entry by entry:

$$
(A+B)_{ij}=a_{ij}+b_{ij}
$$

Every entry of $A$ needs a corresponding entry of $B$ in the same position. This is possible only when both matrices have the same number of rows and the same number of columns.
