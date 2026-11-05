# Exercise 10. Columns of a Matrix Product

## Question

Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1,b_2$. Tasks: (1) compute $Ab_1$ and $Ab_2$; (2) compute the matrix $AB$; (3) compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Solution

### Columns of $B$

$$
b_1=
\begin{pmatrix}
1 \\
-1 \\
3 \\
\end{pmatrix},\qquad b_2=
\begin{pmatrix}
2 \\
0 \\
1 \\
\end{pmatrix}
$$

### Products $Ab_1$ and $Ab_2$

$$
Ab_1=
\begin{pmatrix}
1\cdot1+2\cdot(-1)+0\cdot3 \\
0\cdot1+1\cdot(-1)+1\cdot3 \\
\end{pmatrix}=
\begin{pmatrix}
-1 \\
2 \\
\end{pmatrix}
$$

$$
Ab_2=
\begin{pmatrix}
1\cdot2+2\cdot0+0\cdot1 \\
0\cdot2+1\cdot0+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
2 \\
1 \\
\end{pmatrix}
$$

### Product $AB$

$A$ is $2\times3$ and $B$ is $3\times2$, so $AB$ is defined and has size $2\times2$.

$$
AB=
\begin{pmatrix}
1\cdot1+2\cdot(-1)+0\cdot3 & 1\cdot2+2\cdot0+0\cdot1 \\
0\cdot1+1\cdot(-1)+1\cdot3 & 0\cdot2+1\cdot0+1\cdot1 \\
\end{pmatrix}=
\begin{pmatrix}
-1 & 2 \\
2 & 1 \\
\end{pmatrix}
$$

### Comparison

The first column of $AB$ is $(-1,2)^T=Ab_1$ and the second column is $(2,1)^T=Ab_2$. So

$$
AB=
\begin{pmatrix}
Ab_1 & Ab_2 \\
\end{pmatrix}
$$

### Explanation

By definition, the entry in row $i$ and column $j$ of $AB$ is the dot product of row $i$ of $A$ with column $j$ of $B$. If we fix the column $j$ and let $i$ run over all rows, we get exactly the entries of the matrix-vector product $Ab_j$, because $Ab_j$ is computed by taking the dot product of each row of $A$ with the single vector $b_j$. Therefore column $j$ of $AB$ equals $Ab_j$ for every $j$.

In other words, multiplying $A$ by $B$ means applying $A$ to each column of $B$ separately and collecting the results as columns. This is why the matrix product is a natural extension of the matrix-vector product.
