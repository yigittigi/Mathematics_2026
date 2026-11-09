# Exercise 5. Row Operations

## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

find $\det A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Solution

The matrix is reduced to upper triangular form. Two rules describe the effect of the operations used:

- adding a multiple of one row to another row does not change the determinant;
- multiplying a row by a number $c\neq0$ multiplies the determinant by $c$.

**Step 1.** $R_2\leftarrow R_2-2R_1$. A multiple of $R_1$ is added to $R_2$, so the determinant does not change:

$$
\det A=\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
-1 & 4 & 2 \\
\end{pmatrix}
$$

**Step 2.** $R_3\leftarrow R_3+R_1$. A multiple of $R_1$ is added to $R_3$, so the determinant does not change:

$$
\det A=\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

**Step 3.** $R_2\leftarrow -\frac{1}{3}R_2$. Multiplying a row by $-\frac{1}{3}$ multiplies the determinant by $-\frac{1}{3}$, so the factor $-3$ is written in front to keep the equality:

$$
\det A=-3\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 6 & 5 \\
\end{pmatrix}
$$

**Step 4.** $R_3\leftarrow R_3-6R_2$. A multiple of $R_2$ is added to $R_3$, so the determinant does not change:

$$
\det A=-3\det
\begin{pmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 0 & -7 \\
\end{pmatrix}
$$

The last matrix is upper triangular, so its determinant is the product of its diagonal entries:

$$
\det A=-3\cdot\left(1\cdot1\cdot(-7)\right)=21
$$
