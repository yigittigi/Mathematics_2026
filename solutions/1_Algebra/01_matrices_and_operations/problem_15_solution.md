# Exercise 15. Associativity of Multiplication and Different Calculation Paths

## Question

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

Compute $(AB)C$ and $A(BC)$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

## Solution

### First path: $(AB)C$

The product $AB$ has size $2\times2$:

$$
AB=
\begin{pmatrix}
1\cdot1+2\cdot2+0\cdot(-1) & 1\cdot0+2\cdot1+0\cdot3 \\
0\cdot1+1\cdot2+1\cdot(-1) & 0\cdot0+1\cdot1+1\cdot3 \\
\end{pmatrix}=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}.
$$

Multiplying this intermediate result by $C$ gives

$$
(AB)C=
\begin{pmatrix}
5 & 2 \\
1 & 4 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}=
\begin{pmatrix}
5\cdot2+2\cdot0 & 5\cdot1+2\cdot(-1) \\
1\cdot2+4\cdot0 & 1\cdot1+4\cdot(-1) \\
\end{pmatrix}=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

### Second path: $A(BC)$

The intermediate product $BC$ has size $3\times2$:

$$
BC=
\begin{pmatrix}
1\cdot2+0\cdot0 & 1\cdot1+0\cdot(-1) \\
2\cdot2+1\cdot0 & 2\cdot1+1\cdot(-1) \\
(-1)\cdot2+3\cdot0 & (-1)\cdot1+3\cdot(-1) \\
\end{pmatrix}=
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}.
$$

Therefore

$$
A(BC)=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
4 & 1 \\
-2 & -4 \\
\end{pmatrix}=
\begin{pmatrix}
1\cdot2+2\cdot4+0\cdot(-2) & 1\cdot1+2\cdot1+0\cdot(-4) \\
0\cdot2+1\cdot4+1\cdot(-2) & 0\cdot1+1\cdot1+1\cdot(-4) \\
\end{pmatrix}=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

### Comparison of calculation costs

Using ordinary row-column multiplication without skipping operations involving zeros or ones, an $m\times n$ matrix times an $n\times p$ matrix needs $mnp$ scalar multiplications and $mp(n-1)$ scalar additions.

| Path and stage | Intermediate/result size | Multiplications | Additions |
|---|---|---|---|
| $AB$ | $2\times2$ | 12 | 8 |
| $(AB)C$ after computing $AB$ | $2\times2$ | 8 | 4 |
| **First-path total** | | **20** | **12** |
| $BC$ | $3\times2$ | 12 | 6 |
| $A(BC)$ after computing $BC$ | $2\times2$ | 12 | 8 |
| **Second-path total** | | **24** | **14** |

Thus the first path uses four fewer scalar multiplications and two fewer additions under this counting convention. Its intermediate matrix has four entries rather than six. Hand calculations that simplify zeros and ones may have different counts; the table specifies the uniform standard algorithm.

### Associativity and verification

Both independently computed paths give the same matrix:

$$
(AB)C=A(BC)=
\begin{pmatrix}
10 & 3 \\
2 & -3 \\
\end{pmatrix}.
$$

Associativity means that changing the placement of parentheses, while preserving the order $A,B,C$, does not change the product. It allows a more efficient calculation path, but does not permit exchanging the factors. The equality of all four entries computed by the two paths verifies this example.
