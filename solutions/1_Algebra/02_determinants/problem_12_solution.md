# Exercise 12. A Parameter Revealed by a Row Operation

## Question

For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

## Solution

The operation $R_2\leftarrow R_2-2R_1$ adds a multiple of the first row to the second row, so it does not change the determinant. The new second row is

$$
(2,4,t)-2\cdot(1,2,3)=(0,0,t-6)
$$

Therefore

$$
\det A(t)=\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t-6 \\
0 & 1 & 1 \\
\end{pmatrix}
$$

The first column now has only one nonzero entry, so expansion along the first column reduces the calculation to one $2\times2$ determinant:

$$
\det A(t)=1\cdot\det
\begin{pmatrix}
0 & t-6 \\
1 & 1 \\
\end{pmatrix}=0\cdot1-(t-6)\cdot1=6-t
$$

A square matrix is not invertible exactly when its determinant is zero:

$$
6-t=0\quad\Longrightarrow\quad t=6
$$

Hence $A(t)$ is not invertible only for $t=6$; for every other value of $t$ it is invertible.

For $t=6$ the second row of $A(6)$ is $(2,4,6)=2\cdot(1,2,3)$, so $R_2=2R_1$. The rows are linearly dependent, and the operation $R_2\leftarrow R_2-2R_1$ turns the second row into a zero row, which makes the determinant equal to zero.
