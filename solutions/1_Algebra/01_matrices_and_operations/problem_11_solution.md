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

$$
AB=\begin{pmatrix}
a+c & b+d \\
c & d \\
\end{pmatrix},\qquad BA=\begin{pmatrix}
a & a+b \\
c & c+d \\
\end{pmatrix}
$$

Comparing corresponding entries gives $c=0$ and $d=a$, with no restriction on $b$. Hence all such matrices have the form

$$
B=\begin{pmatrix}
a & b \\
0 & a \\
\end{pmatrix}
$$

Substitution gives the same product in either order, so these conditions are sufficient as well as necessary.
