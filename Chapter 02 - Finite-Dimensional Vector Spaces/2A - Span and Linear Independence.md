Chapter 2: **Finite-Dimensional Vector Spaces**

**2.A**

- [ ] Exercise 1
- [ ] Exercise 2
- [ ] Exercise 3
- [ ] Exercise 4
- [ ] Exercise 5
- [ ] Exercise 6
- [ ] Exercise 7
- [ ] Exercise 8
- [ ] Exercise 9
- [x] Exercise 10
- [ ] Exercise 11
- [ ] Exercise 12
- [ ] Exercise 13
- [x] Exercise 14
- [x] Exercise 15
- [x] Exercise 16
- [x] Exercise 17

_Exercise 10_

Suppose that $v_1 + w, \dots, v_m + w$ is linearly dependent. There are $a_1, \dots, a_m \in \mathbb{F}$ not all zero such that

$$
\begin{aligned}
a_1 (v_1 + w) + \dots + a_m (v_m + w) &= 0\\\\
a_1 v_1 + \dots + a_m v_m &= - (a_1 + \dots + a_m) w\\\\
-\frac{a_1}{a_1 + \dots + a_m} v_1 - \dots -\frac{a_m}{a_1 + \dots + a_m} v_m &= w\\\\
\end{aligned}
$$

Because $v_1, \dots, v_m$ is linearly independent, it follows by the second equation that $a_1 + \dots + a_m \neq 0$. Hence the third equation makes sense and $w \in \operatorname{span}(v_1, \dots, v_m)$.

_Exercise 14_

Suppose $V$ is infinite-dimensional.
Choose any positive integer $m$ and consider the following process

* Step 1

    Choose a non-zero vector $v_1$ in $V$.

* Step j

    Because $V$ is infinite-dimensional, it follows that $v_1, \dots, v_{j-1}$ doesn't span $V$. Hence, there is a vector $v_j \in V$ such that $v_j \notin \operatorname{span}(v_1, \dots, v_{j-1})$. Therefore $v_1, \dots, v_j$ is a linearly independent list in $V$. If $j = m$ stop the process.

After step $m$ the process stops and we have constructed a linearly independent list of length $m$.

For the converse, we will prove the contrapositive.
Suppose that $V$ is finite-dimensional and $v_1, \dots, v_n$ spans $V$.
By 2.23, we cannot have a linearly independent list of arbitrary length (specifically, it cannot be greater than $n$).

Therefore, by modus tollens, if we can have a linearly independent list in $V$ of arbitrary length, then $V$ is infinite-dimensional.

_Exercise 15_

Let $m$ be a positive integer.
Consider the list $v_1, \dots, v_m$, where $v_j$ has $0$ in all slots except for a $1$ at the $j$-th slot.
This list is obviously linearly independent.
Since $m$ was arbitrary, by the previous exercise $\mathbb{F}^\infty$ is infinite-dimensional.

_Exercise 16_

Let $C_{\mathbb{R}}[0, 1]$ denote the real vector space of all continuous real-valued functions on the interval $[0, 1]$.
Since every polynomial is continuous on $[0, 1]$, it follows that $\mathcal{P}(\mathbb{R})$ is a subspace of $C_{\mathbb{R}}[0, 1]$.
However, $\mathcal{P}(\mathbb{R})$ is infinite-dimensional (by 2.16).
Thus 2.26 now implies that $C_{\mathbb{R}}[0, 1]$ is infinite-dimensional.

_Exercise 17_

Suppose by contradiction that $p_0, p_1, \dots, p_m$ is linearly indepedent.
For every polynomial $p \in \operatorname{span}(p_0, p_1, \dots, p_m)$ we have $p(2) = 0$.
Therefore $1 \notin \operatorname{span}(p_0, p_1, \dots, p_m)$ and, by the Linear Dependence Lemma, the list $p_0, p_1, \dots, p_m, 1$ is linearly independent.
However, this list has length $m + 2$ and the list $1, x, \dots, x^m$, which spans $\mathcal{P}_m(R)$, has length $m + 1$.
This is a contradiction by 2.23.
