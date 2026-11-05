# Exercise 13. A Recurrence Written in Matrix Form

## Question

Let

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

Compute $F^2$, $F^3$, $F^4$, and $F^5$. Compare the numbers obtained with the sequence

$$
0,1,1,2,3,5,8,\ldots
$$

and describe the relationship you observe. Then compute

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}
$$

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

## Solution

$$
F^2=\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad F^3=\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix},\qquad F^4=\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix},\qquad F^5=\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}
$$

The entries are consecutive Fibonacci numbers. Writing that sequence as $f_0=0$, $f_1=1$, $f_{n+1}=f_n+f_{n-1}$, the pattern is

$$
F^n=\begin{pmatrix}
f_{n+1} & f_n \\
f_n & f_{n-1} \\
\end{pmatrix}
$$

Also,

$$
F\begin{pmatrix}
a \\
b \\
\end{pmatrix}=\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}
$$

For $(a,b)=(f_n,f_{n-1})$, this produces $(f_{n+1},f_n)$: the sum is the next term and $a$ is retained for the following step. For example, $(1,0)$ becomes $(1,1)$ and then $(2,1)$.
