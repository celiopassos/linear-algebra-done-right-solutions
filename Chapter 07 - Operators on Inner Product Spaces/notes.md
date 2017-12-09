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
<p align="right"> $\blacksquare$ </p>

**Theorem 2.** (Rayleigh's principle)
Suppose $V$ is a finite-dimensional real inner product space and $T \in \mathcal{L}(V)$ is self-adjoint with eigenvalues $\lambda_1 \ge \dots \ge \lambda_n$ (with each eigenvalue $\lambda$ repeated $\dim E(\lambda, T)$ times).
Let $e_1, \dots, e_n$ be a corresponding orthonormal basis of $V$ consisting of eigenvectors of $T$, that is, $Te_j = \lambda_j e_j$.
Then

$$
\frac{1}{||u||^2} \langle Tu, u \rangle \ge \lambda_i \text{ if } u \in \operatorname{span}(e_1, \dots, e_i)
$$

and

$$
\frac{1}{||u||^2} \langle Tu, u \rangle \le \lambda_i \text{ if } u \in \operatorname{span}(e_1, \dots, e_{i-1})^\perp.
$$

_Proof_

Suppose $u \in \operatorname{span}(e_1, \dots, e_i)$.
We can write $u = a_1 e_1 + \dots + a_i e_i$ for some $a_1, \dots, a_i \in \mathbb{R}$.
Then

$$
\begin{aligned}
\frac{1}{||u||^2} \langle Tu, u \rangle &= \frac{1}{||u||^2} (\lambda_1 |a_1|^2 + \dots + \lambda_i |a_i|^2)\\\\
&\ge \frac{1}{||u||^2} (\lambda_i |a_1|^2 + \dots + \lambda_i |a_i|^2)\\\\
&= \frac{1}{||u||^2} \lambda_i ||u||^2\\\\
&= \lambda_i.
\end{aligned}
$$

Now suppose $u \in \operatorname{span}(e_1, \dots, e_{i-1})^\perp$.
Then $u \in \operatorname{span}(e_i, \dots, e_n)$ and we can write $u = a_i e_i + \dots + a_n e_n$ for some $a_i, \dots a_n \in \mathbb{R}$.
Thus

$$
\begin{aligned}
\frac{1}{||u||^2} \langle Tu, u \rangle &= \frac{1}{||u||^2} (\lambda_i |a_i|^2 + \dots + \lambda_n |a_n|^2)\\\\
&\le \frac{1}{||u||^2} (\lambda_i |a_i|^2 + \dots + \lambda_i |a_n|^2)\\\\
&= \frac{1}{||u||^2} \lambda_i ||u||^2\\\\
&= \lambda_i.
\end{aligned}
$$
<p align="right"> $\blacksquare$ </p>

As a corollary of this we have the following result:

**Corollary 1.**

$$
\min_{u \in V, u \neq 0} \frac{1}{||u||^2} \langle Tu, u \rangle = \lambda_n.
$$

Or, equivalently,

$$
\min_{u \in V, ||u|| = 1} \langle Tu, u \rangle = \lambda_n.
$$
