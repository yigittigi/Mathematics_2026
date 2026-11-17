# Exercise 8. Inverse of a Transformation

## Question

The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac12 \\
\end{pmatrix}
$$

describes a scaling of the plane. Find $S^{-1}$ and explain geometrically what the inverse transformation does. Check the action of the pair $S,S^{-1}$ on one simple vector.

## Solution

Geometrically, $S$ takes a vector $(x, y)$ to $(2x, \frac{1}{2}y)$ — so it stretches the plane horizontally by a factor of $2$ and squishes it vertically by half.

To undo that transformation, $S^{-1}$ has to do the exact opposite: shrink horizontally by $1/2$ and stretch vertically by $2$. Since $S$ is diagonal, we just invert the diagonal entries:
$$S^{-1} = \begin{pmatrix} 1/2 & 0 \\ 0 & 2 \end{pmatrix}.$$

Let's test it on the vector $v = \begin{pmatrix} 4 \\ 6 \end{pmatrix}$ (picked even numbers to avoid fractions):
- Applying $S$:
  $$Sv = \begin{pmatrix} 2 & 0 \\ 0 & 1/2 \end{pmatrix}\begin{pmatrix} 4 \\ 6 \end{pmatrix} = \begin{pmatrix} 8 \\ 3 \end{pmatrix}.$$
- Now applying $S^{-1}$ to that result:
  $$S^{-1}(Sv) = \begin{pmatrix} 1/2 & 0 \\ 0 & 2 \end{pmatrix}\begin{pmatrix} 8 \\ 3 \end{pmatrix} = \begin{pmatrix} 4 \\ 6 \end{pmatrix} = v \ \checkmark$$

The vector lands right back where it started.
