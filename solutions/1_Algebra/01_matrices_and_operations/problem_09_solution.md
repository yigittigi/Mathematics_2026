# Exercise 9. Composing Transformations

## Question

Let

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation. For

$$
x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}
$$

compute $RSx$ and $SRx$. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

$$
Sx=\begin{pmatrix}
2 \\
2 \\
\end{pmatrix},\qquad RSx=\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$



$$
Rx=\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix},\qquad SRx=\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

The results differ. Scaling first doubles the original horizontal component, which rotation then turns vertical. Rotating first moves the original vertical component onto the horizontal axis, where it is doubled. Thus the order matters.
