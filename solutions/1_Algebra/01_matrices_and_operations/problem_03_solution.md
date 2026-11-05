# Exercise 3. When Can Matrices Be Multiplied?

## Question

The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Solution

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}
$$

## Rule

A product $XY$ of an $m\times n$ matrix $X$ and a $p\times q$ matrix $Y$ is defined only when $n=p$ (the inner numbers are equal). The result then has size $m\times q$ (the outer numbers).

## Results

| Product | Inner sizes | Defined? | Result size |
|---|---|---|---|
| $AB$ | $3=3$ | Yes | $2\times4$ |
| $BA$ | $4\neq2$ | No | - |
| $BC$ | $4=4$ | Yes | $3\times2$ |
| $CB$ | $2\neq3$ | No | - |
| $AC$ | $3\neq4$ | No | - |
| $CA$ | $2=2$ | Yes | $4\times3$ |
| $AD$ | $3\neq2$ | No | - |
| $DA$ | $2=2$ | Yes | $2\times3$ |

For example, $C$ is $4\times2$ and $A$ is $2\times3$. The inner numbers are $2$ and $2$, so $CA$ is defined and has size $4\times3$.
