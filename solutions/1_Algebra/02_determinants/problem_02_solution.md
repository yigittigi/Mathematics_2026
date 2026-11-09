# Exercise 2. Determinant of a 3×3 Matrix

## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5 \\
\end{pmatrix}
$$

compute $\det A$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

## Solution

By Sarrus' rule:

$$
\begin{aligned}
\det A &= (1\cdot3\cdot5+2\cdot4\cdot2+(-1)\cdot0\cdot1) \\
&\quad -\left((-1)\cdot3\cdot2+2\cdot0\cdot5+1\cdot4\cdot1\right) \\
&= (15+16+0)-(-6+0+4) \\
&= 33
\end{aligned}
$$

Check: adding a multiple of one row to another row does not change the determinant. After $R_3\leftarrow R_3-2R_1$, expanding along the first column gives

$$
\det A=\det
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
0 & -3 & 7 \\
\end{pmatrix}=1\cdot\left(3\cdot7-4\cdot(-3)\right)=21+12=33
$$

The result agrees with the value obtained by Sarrus' rule.
