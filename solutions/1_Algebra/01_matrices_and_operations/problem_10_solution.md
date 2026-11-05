# Exercise 10. Columns of a Matrix Product

## Question

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$. Tasks: (1) compute $Ab_1$ and $Ab_2$; (2) compute the matrix $AB$; (3) compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Solution

$$
b_1=\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},\qquad b_2=\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
$$



$$
Ab_1=\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}=\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix},\qquad Ab_2=\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}=\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$



$$
AB=\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

Each column of $AB$ is found by multiplying every row of $A$ by that column of $B$. Therefore the columns are exactly $Ab_1$ and $Ab_2$, as the result confirms.
