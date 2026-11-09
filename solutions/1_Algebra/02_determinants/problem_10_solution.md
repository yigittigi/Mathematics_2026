# Exercise 10. Detecting Dependence

## Question

Without carrying out a full determinant calculation, explain why

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & 6 \\
0 & 1 & 5 \\
\end{pmatrix}=0.
$$

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

## Solution

Denote the given matrix by $A$. The second row is twice the first row:

$$
R_2=2R_1
$$

Therefore the rows are linearly dependent and $\det A=0$. Consequently, the matrix is not invertible.
