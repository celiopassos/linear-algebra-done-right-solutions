Chapter 6: **Inner Product Spaces**

**Theorem 1.**
Suppose $V$ is a finite-dimensional inner product space and $u, v \in V$.
Then $u$ and $v$ are orthogonal if and only if their matrices with respect to some orthonormal basis of $V$ are orthogonal when thought as elements of $\mathbb{F}^n$ with the usual Euclidean inner product.

_Proof_

Let $e_1, \dots, e_n$ be an orthonormal basis of $V$.
We have

$$
u = a_1 e_1 + \cdots + a_n e_n \text{ and } v = c_1 e_1 + \cdots + c_n e_n
$$

where the $a$'s and the $c$'s are the entries of $\mathcal{M}(u, (e_1, \dots, e_n))$ and $\mathcal{M}(v, (e_1, \dots, e_n))$.
Therefore

$$
\langle u, v \rangle = a_1\overline{c_1} + \dots + a_n\overline{c_n} = \langle (a_1, \dots, a_n), (c_1, \dots, c_n) \rangle,
$$

where the first $\langle \cdot, \cdot \rangle$ is the inner product on $V$ and the second is the usual inner product on $\mathbb{F}^n$.
The equation above yields the desired result.

<p align="right"> $\blacksquare$ </p>
