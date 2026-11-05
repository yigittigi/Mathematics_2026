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

$$
R(\alpha)R(\beta)=\begin{pmatrix}
\cos\alpha\cos\beta-\sin\alpha\sin\beta & -\cos\alpha\sin\beta-\sin\alpha\cos\beta \\
\sin\alpha\cos\beta+\cos\alpha\sin\beta & \cos\alpha\cos\beta-\sin\alpha\sin\beta \\
\end{pmatrix}
$$

Using the sine and cosine angle-sum formulas, this becomes

$$
\begin{pmatrix}
\cos(\alpha+\beta) & -\sin(\alpha+\beta) \\
\sin(\alpha+\beta) & \cos(\alpha+\beta) \\
\end{pmatrix}=R(\alpha+\beta).
$$

Geometrically, a rotation by $\beta$ followed by a rotation by $\alpha$, about the same point, is one rotation by $\alpha+\beta$.
