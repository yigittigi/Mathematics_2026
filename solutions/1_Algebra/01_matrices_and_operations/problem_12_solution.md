# Exercise 12. Formula for a Matrix Power

## Question

Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$. Then do not stop after checking one more case: assume the formula is true for $n$, multiply by $A$, and explain why you obtain exactly the formula for $n+1$.

## Solution

### Powers

$$
A^2=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot1+1\cdot0 & 1\cdot1+1\cdot1 \\
0\cdot1+1\cdot0 & 0\cdot1+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
$$

$$
A^3=A^2A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}
$$

$$
A^4=A^3A=
\begin{pmatrix}
1 & 3 \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & 4 \\
0 & 1 \\
\end{pmatrix}
$$

### Conjecture

The diagonal entries stay equal to $1$ and the top-right entry increases by $1$ with each multiplication: $1,2,3,4$. This suggests

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}\qquad\text{for every integer } n\geq1.
$$

### Inductive step

Base case: for $n=1$ the formula gives $A^1=A$, which is true.

Assume the formula holds for some $n$, that is

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}.
$$

Multiply both sides by $A$ on the right:

$$
A^{n+1}=A^nA=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot1+n\cdot0 & 1\cdot1+n\cdot1 \\
0\cdot1+1\cdot0 & 0\cdot1+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
1 & n+1 \\
0 & 1 \\
\end{pmatrix}.
$$

This is exactly the conjectured formula with $n$ replaced by $n+1$. The key point is the top-right entry: multiplying by $A$ adds the row-one entry $1$ of $A^n$ to the top-right entry $n$, so it becomes $n+1$, while the zeros in the second row keep the diagonal fixed at $1$.

### Conclusion

Since the formula holds for $n=1$ and holds for $n+1$ whenever it holds for $n$, by induction it holds for all $n\geq1$:

$$
A^n=
\begin{pmatrix}
1 & n \\
0 & 1 \\
\end{pmatrix}.
$$

Geometrically, $A$ is a shear along the horizontal axis by $1$ unit, and applying it $n$ times gives a shear by $n$ units.
