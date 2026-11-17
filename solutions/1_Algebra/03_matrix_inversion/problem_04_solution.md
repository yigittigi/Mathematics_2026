# Exercise 4. Gauss–Jordan

## Question

Find $A^{-1}$ using the Gauss–Jordan method for

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

Show the augmented matrix $[A\mid I]$ after successive operations and explain why obtaining $I$ on the left gives the inverse on the right.

## Solution

Start with the augmented matrix $[A \mid I]$:
$$\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 3 & 5 & 0 & 1 \end{array}\right)$$

**Step 1:** Eliminate the $3$ below the first pivot using $R_2 \to R_2 - 3R_1$:
$$\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & -1 & -3 & 1 \end{array}\right)$$

**Step 2:** Flip the sign of row 2 to get a $+1$ pivot using $R_2 \to -R_2$:
$$\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & 1 & 3 & -1 \end{array}\right)$$

**Step 3:** Eliminate the $2$ above the second pivot using $R_1 \to R_1 - 2R_2$:
$$\left(\begin{array}{cc|cc} 1 & 0 & -5 & 2 \\ 0 & 1 & 3 & -1 \end{array}\right)$$

Now the left side is $I$, so the right side is our inverse:
$$A^{-1} = \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}.$$
(Quick sanity check: $\det A = 5 - 6 = -1$, and $(-5)(-1) - (2)(3) = 5 - 6 = -1$ ✓.)

**Why the right block becomes $A^{-1}$:**
Every row operation corresponds to multiplying from the left by an elementary matrix. Since we did three steps in order ($E_1$, then $E_2$, then $E_3$), the combined operation on the whole augmented matrix is multiplication on the left by $E = E_3 E_2 E_1$:
$$E[A \mid I] = [E_3 E_2 E_1 A \mid E_3 E_2 E_1 I].$$
Once the left block reaches $I$, we have $(E_3 E_2 E_1)A = I$. By definition of the inverse, that product of elementary matrices must be $E_3 E_2 E_1 = A^{-1}$. And since the right block started as $I$, it gets multiplied into $(E_3 E_2 E_1)I = A^{-1}$.
