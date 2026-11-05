# Exercise 8. Row Operations and Their Reversibility

## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order: (1) $R_2\leftarrow R_2-2R_1$, (2) $R_3\leftarrow R_3+R_1$, (3) interchange $R_2$ and $R_3$. Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

### Step 1: $R_2\leftarrow R_2-2R_1$

New second row: $(2-2\cdot1,\ 4-2\cdot2,\ 1-2\cdot(-1))=(0,0,3)$.

$$
A_1=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

### Step 2: $R_3\leftarrow R_3+R_1$

New third row: $(-1+1,\ 1+2,\ 3+(-1))=(0,3,2)$.

$$
A_2=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 0 & 3 \\
0 & 3 & 2 \\
\end{pmatrix}
$$

### Step 3: interchange $R_2$ and $R_3$

$$
A_3=
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 2 \\
0 & 0 & 3 \\
\end{pmatrix}
$$

The result is an upper triangular matrix.

### Reversing operations

Each elementary row operation is reversible by another elementary row operation of the same type.

Step 1 is reversed by $R_2\leftarrow R_2+2R_1$: adding back what was subtracted.

Step 2 is reversed by $R_3\leftarrow R_3-R_1$: subtracting what was added.

Step 3 is reversed by interchanging $R_2$ and $R_3$ again: a swap is its own inverse.

### Verification

Applying the reverse operations to $A_3$ in reverse order (swap, then $R_3\leftarrow R_3-R_1$, then $R_2\leftarrow R_2+2R_1$) gives back $A_2$, then $A_1$, then the original $A$. For example, the swap gives $A_2$, and $R_3\leftarrow R_3-R_1$ gives third row $(0-1,\ 3-2,\ 2-(-1))=(-1,1,3)$, which is the original third row.
