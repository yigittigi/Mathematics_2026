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

A product of matrices applied to a vector is read from right to left: in $RSx$ the vector is first scaled by $S$ and then rotated by $R$.

### First scale, then rotate: $RSx$

$$
Sx=
\begin{pmatrix}
2\cdot1+0\cdot2 \\
0\cdot1+1\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix},\qquad
RSx=R
\begin{pmatrix}
2 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
0\cdot2+(-1)\cdot2 \\
1\cdot2+0\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}
$$

### First rotate, then scale: $SRx$

$$
Rx=
\begin{pmatrix}
0\cdot1+(-1)\cdot2 \\
1\cdot1+0\cdot2 \\
\end{pmatrix}=
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix},\qquad
SRx=S
\begin{pmatrix}
-2 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
2\cdot(-2) \\
1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}
$$

### Comparison

$$
RSx=
\begin{pmatrix}
-2 \\
2 \\
\end{pmatrix}\neq \begin{pmatrix}
-4 \\
1 \\
\end{pmatrix}=SRx
$$

The results are different, so $RS\neq SR$. We can also verify this on the matrices themselves:

$$
RS=
\begin{pmatrix}
0 & -1 \\
2 & 0 \\
\end{pmatrix},\qquad SR=
\begin{pmatrix}
0 & -2 \\
1 & 0 \\
\end{pmatrix}
$$

### Geometric explanation

$S$ stretches only the horizontal direction by a factor of $2$ and leaves the vertical direction unchanged. $R$ rotates everything by $90^\circ$, which turns horizontal into vertical.

In $RSx$ the horizontal component of $x$ is doubled first ($1\to2$), and then the whole vector is rotated, so the doubled part ends up pointing vertically.

In $SRx$ the vector is rotated first, so its old vertical component ($2$) becomes horizontal, and only then is it doubled ($-2\to-4$).

Since the scaling acts on a fixed direction (the horizontal axis) while the rotation changes which component lies in that direction, the order of the two transformations changes which component gets stretched. This is why composition of transformations, like matrix multiplication, is not commutative.
