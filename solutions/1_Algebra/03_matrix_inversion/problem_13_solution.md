# Exercise 13. Undoing a Composite Transformation

## Question

The matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

## Solution

First let's note the individual inverses:
$S$ is diagonal, so $S^{-1} = \begin{pmatrix} 1/2 & 0 \\ 0 & 1 \end{pmatrix}$.
$H$ is a horizontal shear with $\det H = 1$, so $H^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}$.

**Way 1: Compute $T = HS$ first, then invert.**
$$T = HS = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}.$$
Here $\det T = 2 \cdot 1 - 0 = 2$. Using the 2×2 formula:
$$T^{-1} = \frac{1}{2}\begin{pmatrix} 1 & -1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 1/2 & -1/2 \\ 0 & 1 \end{pmatrix}.$$

**Way 2: Product rule $T^{-1} = (HS)^{-1} = S^{-1}H^{-1}$.**
$$S^{-1}H^{-1} = \begin{pmatrix} 1/2 & 0 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1/2 & -1/2 \\ 0 & 1 \end{pmatrix} \ \checkmark$$
Both ways give the exact same result.

**Why $H^{-1}S^{-1}$ is different and why we undo from the end:**
If we multiply in the non-reversed order:
$$H^{-1}S^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1/2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1/2 & -1 \\ 0 & 1 \end{pmatrix} \neq T^{-1}.$$
The top-right entry is $-1$ instead of $-1/2$. Indeed, $T(H^{-1}S^{-1}) = \begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1/2 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} \neq I$.

The reason is the order in which $T$ acts on a vector: $Tv = H(Sv)$, so $S$ (the scaling) is applied first and $H$ (the shear) second. To get $v$ back, we have to undo the operations from the end: first remove the shear with $H^{-1}$, which gives back $Sv$, and only then remove the scaling with $S^{-1}$, which gives back $v$. So $v = S^{-1}(H^{-1}(Tv))$, which means $T^{-1} = S^{-1}H^{-1}$.

Example with $v = (1, 1)$: $Sv = (2, 1)$ and $Tv = H(Sv) = (3, 1)$.
- Correct order: $H^{-1}(3, 1) = (2, 1)$, then $S^{-1}(2, 1) = (1, 1) = v$ ✓.
- Wrong order: $S^{-1}(3, 1) = (3/2, 1)$, then $H^{-1}(3/2, 1) = (1/2, 1) \neq v$. Here we tried to undo the scaling while the shear was still applied on top of it.

This is the rule "when undoing a composition of operations, we undo them from the end": the last operation applied is the first one to be undone, the same reversal as $(AB)^{-1} = B^{-1}A^{-1}$ in Exercise 7.
