# Exercise 3. Swapping Two Rows

## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

compute $\det A$. Then form a matrix $B$ by swapping the first and second rows of $A$.

First predict $\det B$ using a determinant property, and then verify your prediction by calculation.

## Solution

By Sarrus' rule:

$$
\begin{aligned}
\det A &= (1\cdot3\cdot1+2\cdot1\cdot2+0\cdot0\cdot1) \\
&\quad -(0\cdot3\cdot2+2\cdot0\cdot1+1\cdot1\cdot1) \\
&= (3+4+0)-(0+0+1) \\
&= 6
\end{aligned}
$$

Swapping the first and second rows of $A$ gives

$$
B=
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1 \\
\end{pmatrix}
$$

**Prediction.** Interchanging two rows of a square matrix changes the sign of its determinant and leaves its absolute value unchanged. Therefore

$$
\det B=-\det A=-6
$$

**Verification.** By Sarrus' rule:

$$
\begin{aligned}
\det B &= (0\cdot2\cdot1+3\cdot0\cdot2+1\cdot1\cdot1) \\
&\quad -(1\cdot2\cdot2+3\cdot1\cdot1+0\cdot0\cdot1) \\
&= (0+0+1)-(4+3+0) \\
&= -6
\end{aligned}
$$

The calculated value agrees with the prediction: the row swap changed only the sign of the determinant.
