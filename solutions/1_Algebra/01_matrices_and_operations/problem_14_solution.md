# Exercise 14. Rotation Matrices

## Question

The matrix for a rotation through an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{pmatrix}.
$$

Compute $R(\alpha)R(\beta)$ and, using the angle-sum formulas for sine and cosine, show that

$$
R(\alpha)R(\beta)=R(\alpha+\beta).
$$

Explain the result geometrically.

## Solution

### The product

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha & -\sin\alpha \\
\sin\alpha & \cos\alpha \\
\end{pmatrix}
\begin{pmatrix}
\cos\beta & -\sin\beta \\
\sin\beta & \cos\beta \\
\end{pmatrix}
$$

Computing each entry as a row-column dot product:

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta & -\cos\alpha\sin\beta-\sin\alpha\cos\beta \\
\sin\alpha\cos\beta+\cos\alpha\sin\beta & -\sin\alpha\sin\beta+\cos\alpha\cos\beta \\
\end{pmatrix}
$$

### Angle-sum formulas

The trigonometric identities are

$$
\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta,\qquad
\sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta.
$$

The top-left and bottom-right entries are both $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.

The bottom-left entry is $\sin\alpha\cos\beta+\cos\alpha\sin\beta=\sin(\alpha+\beta)$.

The top-right entry is $-(\sin\alpha\cos\beta+\cos\alpha\sin\beta)=-\sin(\alpha+\beta)$.

Therefore

$$
R(\alpha)R(\beta)=
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta) \\
\end{pmatrix}=R(\alpha+\beta).
$$

### Geometric explanation

$R(\beta)$ rotates every vector in the plane counterclockwise by the angle $\beta$, and $R(\alpha)$ rotates by $\alpha$. The product $R(\alpha)R(\beta)$ applied to a vector $x$ means: first rotate $x$ by $\beta$, then rotate the result by $\alpha$. Two successive rotations about the same point are a single rotation by the total angle $\alpha+\beta$. The matrix identity is exactly this geometric fact written in coordinates.

A consequence is that rotation matrices commute with each other: $R(\alpha)R(\beta)=R(\alpha+\beta)=R(\beta+\alpha)=R(\beta)R(\alpha)$, unlike general matrices (compare Exercises 4 and 9).

### Verification

Take $\alpha=\beta=90^\circ$. Then 

$$
R(90^\circ)=\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
$$

 and

$$
R(90^\circ)R(90^\circ)=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
-1 & 0 \\
0 & -1 \\
\end{pmatrix}=R(180^\circ),
$$

since $\cos180^\circ=-1$ and $\sin180^\circ=0$. Two quarter turns make a half turn, as expected.
