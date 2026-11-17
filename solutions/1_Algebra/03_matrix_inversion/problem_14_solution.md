# Exercise 14. A Matrix That Is Its Own Inverse

## Question

Assume that a square matrix $A$ satisfies

$$
A^2=I.
$$

Show that

$$
A^{-1}=A.
$$

Then give an example of a $2\times2$ matrix different from $I$ and $-I$ that satisfies this condition, and verify it by multiplication.

## Solution

**Proof:**
We are given $A^2 = I$, which can be written directly as:
$$A \cdot A = I.$$
By definition, a matrix $B$ is the inverse of $A$ if $AB = BA = I$. Looking at $A \cdot A = I$, the matrix $A$ itself plays the role of $B$ on both the left and the right. Therefore, $A$ is invertible and $A^{-1} = A$.

**Example (other than $I$ and $-I$):**
Geometrically, any reflection across a line or a swap of axes does the trick, because reflecting twice gets you back to the start. Let's pick the matrix that swaps the $x$ and $y$ coordinates (or reflects across $y = x$):
$$A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}.$$
Clearly $A \neq I$ and $A \neq -I$. Let's check $A^2$ by multiplication:
$$A^2 = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0\cdot 0 + 1\cdot 1 & 0\cdot 1 + 1\cdot 0 \\ 1\cdot 0 + 0\cdot 1 & 1\cdot 1 + 0\cdot 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I \ \checkmark$$

Since $A^2 = I$, we have $A^{-1} = A$.
