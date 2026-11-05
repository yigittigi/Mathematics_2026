# Exercise 11. When Do Matrices Commute?

## Question

Given

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

Find the conditions on $a,b,c,d$ under which $AB=BA$. Describe the general form of all such matrices $B$.

## Solution

### Compute both products

$$
AB=
\begin{pmatrix}
1\cdot a+1\cdot c & 1\cdot b+1\cdot d \\
0\cdot a+1\cdot c & 0\cdot b+1\cdot d \\
\end{pmatrix}=
\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix}
$$

$$
BA=
\begin{pmatrix}
a\cdot1+b\cdot0 & a\cdot1+b\cdot1 \\
c\cdot1+d\cdot0 & c\cdot1+d\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}
$$

### Compare entry by entry

Two matrices are equal when all corresponding entries are equal. Setting $AB=BA$ gives four equations:

$$
a+c=a,\qquad b+d=a+b,\qquad c=c,\qquad d=c+d.
$$

The first equation gives $c=0$. The second gives $d=a$. The third is always true. The fourth gives $c=0$ again, consistent with the first.

### Conditions and general form

The conditions are

$$
c=0,\qquad d=a,
$$

while $a$ and $b$ can be any numbers. So every matrix commuting with $A$ has the form

$$
B=
\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}=aI+bN,\qquad\text{where } N=
\begin{pmatrix}
0 & 1 \\
0 & 0 \\
\end{pmatrix}.
$$

These are the upper triangular matrices with equal diagonal entries. Note that $A=I+N$ itself has this form, as do $I$ and all powers of $A$.

### Verification

Take $a=2$, $b=5$: $B=\begin{pmatrix}2 & 5 \\ 0 & 2\end{pmatrix}$.

$$
AB=
\begin{pmatrix}
2 & 7 \\
0 & 2 \\
\end{pmatrix},\qquad BA=
\begin{pmatrix}
2 & 7 \\
0 & 2 \\
\end{pmatrix}
$$

The products agree. For a matrix outside this family, such as $B=\begin{pmatrix}1 & 0 \\ 1 & 1\end{pmatrix}$ (here $c=1\neq0$), we get $AB=\begin{pmatrix}2 & 1 \\ 1 & 1\end{pmatrix}$ but $BA=\begin{pmatrix}1 & 1 \\ 1 & 2\end{pmatrix}$, so they do not commute.
