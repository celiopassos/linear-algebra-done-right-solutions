Chapter 2: **Finite-Dimensional Vector Spaces**

**2.C**

- [ ] Exercise 1
- [ ] Exercise 2
- [ ] Exercise 3
- [ ] Exercise 4
- [ ] Exercise 5
- [ ] Exercise 6
- [ ] Exercise 7
- [ ] Exercise 8
- [x] Exercise 9
- [ ] Exercise 10
- [ ] Exercise 11
- [ ] Exercise 12
- [ ] Exercise 13
- [x] Exercise 14
- [x] Exercise 15
- [x] Exercise 16
- [x] Exercise 17

_Exercise 9_

The result clearly holds if $v_1 + w, \dots, v_m + w$ is linearly independent, so assume it is not.
By Exercise 10 in section 2A, $w \in \operatorname{span}(v_1, \dots, v_m)$ we can write
$$
w = a_1 v_1 + \cdots + a_m v_m,
$$
for some unique scalars $a_1, \dots, a_m \in \mathbb{R}$.
Since $w$ is nonzero, we have $a_j \neq 0$ for at least one $j$.
Removing $v_j + w$, we get a list of length $m-1$ which is linearly indepdent by previously cited exercise and the uniqueness of the scalars $a_i$.

_Exercise 13_

Let $U \in \mathbb{C}^6$, $W \in \mathbb{C}^6$, and $\operatorname{dim} U = \operatorname{dim} W = 4$.

We have that $\operatorname{dim} (U + W) = \operatorname{dim} U + \operatorname{dim} V - \operatorname{dim} U \cap V$, which implies that $\operatorname{dim} U \cap V = \operatorname{dim} U + \operatorname{dim} W - \operatorname{dim} (U + W) = 8 - \operatorname{dim} (U + W)$.

We know, that $\operatorname{dim} (U + W) \le \operatorname{dim} \mathbb{C}^6 = 6$, which in turn means that $\operatorname{dim} (U \cap V) \ge 8 - 6 = 2$, so basis of $U \cap V$ consists of 2 or more vectors, and since basis is linearly list of vectors independent, we can conclude that we have proved the statement.

_Exercise 14_

We will prove by induction on $m$.
For the base case we have $\operatorname{dim} U_1 \le \operatorname{dim} U_1$.
Suppose $m > 1$ and

$$
\operatorname{dim} (U_1 + \dots + U_k) \le \operatorname{dim} U_1 + \dots + \operatorname{dim} U_k
$$

for all positive integers $k < m$.
Then

$$
\begin{aligned}
\operatorname{dim} (U_1 + \dots + U_m) &= \operatorname{dim}(U_1 + \dots + U_{m-1}) + \operatorname{dim}(U_m) - \operatorname{dim}((U_1 + \dots + U_{m-1}) \cap U_m)\\\\
&\le \operatorname{dim}(U_1 + \dots + U_{m-1}) + \operatorname{dim} U_m\\\\
&\le \operatorname{dim} U_1 + \dots + \operatorname{dim} U_{m-1} + \operatorname{dim} U_m,
\end{aligned}
$$

where first equality follows from 2.43 and third from the induction hypothesis.

_Exercise 15_

Let $u_1, \dots, u_n$ be a basis of $V$.
Define $U_j$ by

$$
U_j = \operatorname{span}(u_j)
$$

for $j = 1, \dots, n$.
Each $U_j$ is clearly $1$-dimensional.
Moreover, $V = U_1 + \dots + U_n$, because this sum contains all the basis vectors.
Thus, for every $v \in V$, we can write it uniquely in the form

$$
v = a_1 u_1 + \dots + a_n u_n
$$

for some scalars $a_1, \dots, a_n \in \mathbb{F}$ (by 2.29).
Since each $u_j$ is in $U_j$, by the definition of direct sum, $U_1 + \dots + U_m$ is a direct sum.

_Exercise 16_

Let $V = U_1 \oplus \dots \oplus U_m$.
Because every vector in $V$ can be written as sum $v_1 + \dots + v_m$ where each $v_j \in U_j$ and since each $v_j$ can be written as sum of $u_1 + \dots + u_{\operatorname{dimU_j}}$ for some basis $u_1, \dots, u_{\operatorname{dimU_j}}$ of $U_j$, it follows that the list composed of all such bases spans $V$.
Hence $V$ is finite-dimensional.

Moreover, if a linear combination of this list equals $0$, then a linear combination of $v_1, \dots, v_m$ also equals $0$.
But, $U_1 + \dots + U_m$ being a direct sum forces each $u_j$ to equal $0$ and, thus, the coefficients of the basis vectors of $U_j$ must also equal $0$, proving that the list is linear independent.

Therefore, this list is a basis of $V$ and its length is $\operatorname{dim} U_1 + \dots + \operatorname{dim} U_m$, as desired.

_Exercise 17_

The statement is not true. 

Suppose it was: let us conisder 
$$
\begin{aligned}
U_1 &= \{(x, 2x) | x \in \mathbb{R}\}\\
U_2 &= \{(x,x) | x \in \mathbb{R}\}\\
U_3 &= \{(x, 0.5x) | x \in \mathbb{R}\}
\end{aligned}
$$

We have that  $\operatorname{dim} U_1 =  \operatorname{dim} U_2 = \operatorname{dim} U_3 = 1$,  $\operatorname{dim} (U_1 \cap U_2) = \operatorname{dim} (U_1 \cap U_3) = \operatorname{dim} (U_2 \cap U_3) = 0$, $\operatorname{dim} (U_1 \cap U_2 \cap U_3) = 0$. So, if we apply formula, we get that $\operatorname{dim} (U_1 + U_2 + U_3) = 1 + 1 + 1 - 0 - 0 - 0 + 0 = 3$, but this is wrong, since $\operatorname{dim} (U_1 + U_2 + U_3) = \operatorname{dim} \mathbb{R}^2 = 2$.