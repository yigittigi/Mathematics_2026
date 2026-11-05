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

### Powers of $F$

$$
F^2=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
1+1 & 1+0 \\
1+0 & 1+0 \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
$$

$$
F^3=F^2F=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

$$
F^4=F^3F=
\begin{pmatrix}
3 & 2 \\
2 & 1 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
$$

$$
F^5=F^4F=
\begin{pmatrix}
5 & 3 \\
3 & 2 \\
\end{pmatrix}
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
8 & 5 \\
5 & 3 \\
\end{pmatrix}
$$

### Relationship with the sequence

The sequence $0,1,1,2,3,5,8,\ldots$ is the Fibonacci sequence, defined by $F_0=0$, $F_1=1$ and $F_{n+1}=F_n+F_{n-1}$.

All entries of the powers of $F$ are Fibonacci numbers. Reading $F^n$ as

$$
F^n=
\begin{pmatrix}
F_{n+1} & F_n \\
F_n & F_{n-1} \\
\end{pmatrix}
$$

we check: $F^1$ has entries $(1,1,1,0)=(F_2,F_1,F_1,F_0)$, $F^2$ has $(2,1,1,1)=(F_3,F_2,F_2,F_1)$, $F^3$ has $(3,2,2,1)$, $F^4$ has $(5,3,3,2)$ and $F^5$ has $(8,5,5,3)=(F_6,F_5,F_5,F_4)$.

So the top-left entry of $F^n$ is $F_{n+1}$, the off-diagonal entries are $F_n$, and the bottom-right entry is $F_{n-1}$. Each multiplication by $F$ moves one step forward in the sequence.

### One recurrence step

$$
F
\begin{pmatrix}
a \\
b \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot a+1\cdot b \\
1\cdot a+0\cdot b \\
\end{pmatrix}=
\begin{pmatrix}
a+b \\
a \\
\end{pmatrix}
$$

If we store two consecutive terms of the sequence in a vector as $(a,b)=(F_n,F_{n-1})$, then the first row of $F$ computes their sum $a+b=F_n+F_{n-1}=F_{n+1}$, which is the next term. The second row simply copies $a=F_n$ into the second position, so it is kept as the previous term for the following step. The output vector is therefore $(F_{n+1},F_n)$, which has exactly the same shape as the input, one step later.

### Verification

Starting from $(F_1,F_0)=(1,0)$:

$$
F
\begin{pmatrix}
1 \\
0 \\
\end{pmatrix}=
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix},\quad
F
\begin{pmatrix}
1 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix},\quad
F
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}=
\begin{pmatrix}
3 \\
2 \\
\end{pmatrix},\quad
F
\begin{pmatrix}
3 \\
2 \\
\end{pmatrix}=
\begin{pmatrix}
5 \\
3 \\
\end{pmatrix}
$$

The first coordinates $1,1,2,3,5$ are the Fibonacci numbers, confirming that repeated multiplication by $F$ runs the recurrence. This is why $F^n(1,0)^T=(F_{n+1},F_n)^T$, consistent with the first column of $F^n$ found above.
