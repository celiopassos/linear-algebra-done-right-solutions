Chapter 7: **Operators on Inner Product Spaces**

**Theorem 1.**
Suppose $V$ is a finite-dimensional inner product space and $S \in \mathcal{L}(V)$.
Then $S$ is an isometry if and only if the columns of the matrix of $S$ with respect to every orthonormal basis of $V$ are orthonormal when thought as elements of $\mathbb{F}^n$.

_Proof_

Let $e_1, \dots, e_n$ be an orthonormal basis of $V$ and let $A$ be the matrix of $S$ with respect to this basis.
We have

$$
Se_j = A_{1, j} e_1 + \dots + A_{n, j} e_n
$$

for each $j = 1, \dots, n$.
Therefore

$$
\langle Se_j, Se_k \rangle = A_{1, j}\overline{A_{1, k}} + \cdots + A_{n, j}\overline{A_{n, k}} = \langle (A_{1, j}, \dots, A_{n, j}), (A_{1, k}, \dots, A_{n, k}) \rangle.
$$

Then $S$ is an isometry if and only if the list $Se_1, \dots, Se_n$ is orthonormal (see 7.42), which happens if and only if the columns of $\mathcal{M}(S)$ are also orthonormal (by the equation above).
Note that the first $\langle \cdot, \cdot \rangle$ above is the inner product on $V$ and the second is the usual inner product on $\mathbb{F}^n$.
