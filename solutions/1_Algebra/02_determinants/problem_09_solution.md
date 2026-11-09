# Exercise 9. Area and the Determinant

## Question

The vectors

$$
u=
\begin{pmatrix}
3 \\
1 \\
\end{pmatrix},\qquad v=
\begin{pmatrix}
1 \\
4 \\
\end{pmatrix}
$$

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

## Solution

Placing the vectors $u$ and $v$ as columns:

$$
\det
\begin{pmatrix}
3 & 1 \\
1 & 4 \\
\end{pmatrix}=3\cdot4-1\cdot1=11
$$

The area of the parallelogram is the absolute value of this determinant, so the area equals $11$ square units.

When the order of the vectors is reversed, the determinant becomes $-11$. The sign changes, but the absolute value does not, so the area remains $11$ square units.
