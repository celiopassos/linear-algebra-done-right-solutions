Chapter 7: **Operators on Inner Product Spaces**

**7.B**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [x] Exercise 5
- [x] Exercise 6
- [x] Exercise 7
- [x] Exercise 8
- [x] Exercise 9
- [x] Exercise 10
- [x] Exercise 11
- [x] Exercise 12
- [x] Exercise 13
- [x] Exercise 14
- [x] Exercise 15

_Exercise 1_

False.
Define $T \in \mathcal{L}(\mathbb{R}^3)$ by

$$
\begin{aligned}
Te_1 &= e_1\\\\
Te_2 &= 2e_2\\\\
T(e_1 + e_2 + e_3) &= 3e_1 + 3e_2 + 3e_3,
\end{aligned}
$$

where $e_1, e_2, e_3$ is the standard basis of $\mathbb{R}^3$.
Clearly, $e_1, e_2, e_1 + e_2 + e_3$ is a basis of $\mathbb{R}^3$ consisting of eigenvectors of $T$.
However, the matrix of $T$ with respect to the standard basis (which is orthonormal) is

$$
\begin{pmatrix}
1 & 0 & 3\\\\
0 & 2 & 1\\\\
0 & 0 & 3
\end{pmatrix},
$$

which does not equal its transpose (the matrix of $T^*$, by 7.10).
Therefore $T$ is not self-adjoint.

_Exercise 2_

Since $T$ is self-adjoint, there exists a basis consisting of eigenvectors of $T$, by either 7.24 or 7.29 (depending on the choice of $\mathbb{F}$).
Because $x^2 - 5x + 6 = (x - 2)(x - 3)$, we have

$$
T^2 - 5T + 6I = (T - 2I)(T - 3I).
$$

Thus, applying it to any vector in the basis will give $0$ (for the eigenvectors corresponding to $2$ just switch the order to $(T - 3I)(T - 2I)$, which is valid by 5.20).

_Exercise 3_

Define $T \in \mathcal{L}(\mathbb{C}^3)$ by

$$
\begin{aligned}
Te_1 &= 2e_1\\\\
Te_2 &= 3e_2\\\\
Te_3 &= 3(e_1 + e_2 + e_3),
\end{aligned}
$$

where $e_1, e_2, e_3$ is the standard basis of $\mathbb{C}^3$.
The matrix of $T$ with respect to same basis is

$$
\mathcal{M}(T) = \begin{pmatrix}
2 & 0 & 3\\\\
0 & 3 & 3\\\\
0 & 0 & 3
\end{pmatrix}.
$$

Therefore, the only eigenvalues of $T$ are $2$ and $3$ (by 5.32).
Moreover

$$
\begin{aligned}
(T^2 - 5T + 6I)e_3 &= T^2e_3 - 5Te_3 + 6Ie_3\\\\
&= T(3e_1 + 3e_2 + 3e_3) - 15(e_1 + e_2 + e_3) + 6e_3\\\\
&= 6e_1 + 9e_2 + 9(e_1 + e_2 + e_3) - 15(e_1 + e_2 + e_3) + 6e_3\\\\
&= 3e_2\\\\
&\neq 0.
\end{aligned}
$$

Therefore, $T^2 - 5T + 6I \neq 0$.

_Exercise 4_

The forward direction is basically the same as 7.22 and 7.24.

Suppose all pairs of eigenvectors corresponding to distinct eigenvalues of $T$ are orthogonal and

$$
V = E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T),
$$

where $\lambda_1, \dots, \lambda_m$ are distinct eigenvalues of $T$.
Consider the constructed by concatenating orthonormal bases of $E(\lambda_1, T), \dots, E(\lambda_m, T)$.
By 5.41 (e) this list has length $\operatorname{dim} V$.
Moreover, because all pairs of eigenvectors corresponding to distinct eigenvalues of $T$ are orthogonal, by 6.26 this is list is also linearly indepedent.
Therefore $V$ has an orthonormal basis consisting of eigenvectors of $T$ and is normal by 7.24.

_Exercise 5_

Again, the forward direction is basically 7.22 (since $T$ is also normal) and 7.29 and the converse is the same as the previous exercise.

_Exercise 6_

Suppose $T$ is self-adjoint.
Let $\lambda$ be an eigenvalue of $T$ and $v$ a corresponding eigenvector.
Then

$$
\lambda \langle v, v \rangle = \langle Tv, v \rangle = \langle v, Tv \rangle = \overline{\lambda} \langle v, v \rangle.
$$

Therefore $\lambda  = \overline{\lambda}$, that is, $\lambda$ is real.

Conversely, suppose all eigenvalues of $T$ are real.
Let $e_1, \dots, e_n$ denote an orthonormal basis consisting of eigenvalues of $T$ (which exists by 7.24) and let $\lambda_1, \dots, \lambda_n$ denote their corresponding eigenvalues (which are real).
For any $v \in V$, we can write

$$
v = a_1 e_1 + \dots + a_n e_n
$$

for some $a_1, \dots, a_n \in \mathbb{C}$.
Then

$$
\langle Tv, v \rangle = \langle \lambda_1 a_1 e_1 + \dots + \lambda_n a_n e_n, a_1 e_1 + \dots + a_n e_n \rangle = \lambda_1 |a_1|^2 + \dots + \lambda_n |a_n|^2 \in \mathbb{R}.
$$

Thus, by 7.15, $T$ is self-adjoint.

_Exercise 7_

Let $e_1, \dots, e_n$ be an orthonormal basis of $V$ consisting of eigenvalues of $T$ and let $\lambda_1, \dots, \lambda_n$ denote their corresponding eigenvalues.
We have

$$
\lambda_j^9 e_j = T^9e_j = T^8e_j = \lambda_j^8 e_j,
$$

for each $j = 1, \dots, n$.
This implies that $\lambda_j = 0$ or $\lambda_j = 1$.
Hence, every eigenvalue of $T$ is a real number and by the previous exercise $T$ is self-adjoint.
Moreover, $\lambda_j^2 = \lambda_j$, regardless if $\lambda_j$ is $0$ or $1$.
Therefore $T^2 = T$.

_Exercise 8_

Let $V$ be a $3$-dimensional complex vector space and $v_1, v_2, v_3$ a basis for it.
Define $T \in \mathcal{L}(V)$ by

$$
\begin{aligned}
Tv_1 &= v_2\\\\
Tv_2 &= v_3\\\\
Tv_3 &= 0.
\end{aligned}
$$

Obviously $T^9 = T^8 = 0$, however $T^2e_1 = e_3$ and $Te_1 = e_2$, therefore $T^2 \neq T$.

_Exercise 9_

Suppose that $T$ is a normal operator on $V$.
Let $e_1, \dots, e_n$ be an orthonormal basis of $V$ consisting of eigenvalues of $T$ and let $\lambda_1, \dots, \lambda_n$ denote their corresponding eigenvalues.
Define $S$ by

$$
Se_j = \sqrt{\lambda_j}e_j,
$$

for each $j = 1, \dots, n$.
Obviously, $S^2e_j = \lambda_j e_j = Te_j$.
Therefore $S^2 = T$.

_Exercise 10_

Define $T \in \mathcal{L}(\mathbb{R}^2)$ by

$$
\begin{aligned}
Te_1 &= e_2\\\\
Te_2 &= -e_1,
\end{aligned}
$$

where $e_1, e_2$ is the standard basis of $\mathbb{R}^2$.
Then

$$
(T^2 + I)e_1 = T^2e_1 + Ie_1 = Te_2 + e_1 = -e_1 + e_1 = 0.
$$

Therefore $T^2 + bT + cI$ is not injective for $b = 0$ and $c = 1$.

_Exercise 11_

This is about the same as Exercise 9.
Just note that is one is valid when $\mathbb{F} = \mathbb{R}$, not only because it just applies to self-adjoint operators, but also because every real number has a cube root, although the same cannot be same about square roots.

_Exercise 12_

Let $e_1, \dots, e_n$ be an orthonormal basis of $V$ consisting of eigenvectors of $T$ and let $\lambda_1, \dots, \lambda_n$ denote their corresponding eigenvalues.
Choose an eigenvalue $\lambda'$ of $T$ such that $|\lambda' - \lambda|^2$ is minimized.
There are $a_1, \dots, a_n \in \mathbb{F}$ such that

$$
v = a_1 e_1 + \dots + a_n e_n.
$$

Thus, we have

$$
\begin{aligned}
\epsilon^2 &> ||Tv - \lambda v||^2\\\\
&= |\langle Tv - \lambda v, e_1 \rangle|^2 + \dots + |\langle Tv - \lambda v, e_n \rangle|^2\\\\
&= |\lambda_1a_1 - \lambda a_1|^2 + \dots + |\lambda_n a_n - \lambda a_n|^2\\\\
&= |a_1|^2|\lambda_1 - \lambda|^2 + \dots + |a_n|^2|\lambda_n - \lambda|^2\\\\
&\ge |a_1|^2|\lambda' - \lambda|^2 + \dots + |a_n|^2|\lambda' - \lambda|^2\\\\
&= |\lambda' - \lambda|^2,
\end{aligned}
$$

where the second and fifth lines follow from 6.30 (the fifth because $||v|| = 1$).
Taking the square root now yields the desired result.

_Exercise 13_

We will just prove (a) implies (b), since that's the part which uses Schur's Theorem, and we will do so by induction on $\operatorname{dim} V$.

Suppose (a) holds. Note that if $\operatorname{dim} V = 1$, then (a) trivially implies (b), just take any non-zero vector in $V$ and divide it by its norm.
Now suppose that $\operatorname{dim} V > 1$ and that (a) implies (b) for all complex inner product spaces of smaller dimension.

Choose an eigenvector $u$ of $T$ with $||u|| = 1$ (the existence of an eigenvalue is guaranteed by 5.21).
Let $U = \operatorname{span}(u)$.
Since $U$ is invariant under $T$, it follows by Exercise 3 in section 7A that $U^\perp$ is invariant under $T^\*$.
By 6.50 $\operatorname{dim} U^\perp = \operatorname{dim} V - 1$.
Thus, by the induction hypothesis there exists an orthonormal basis of $U^\perp$ consisting of eigenvectors of $T^\*|_{U^\perp}$, which are also eigenvectors of $T$, by 7.21.
Moreover, adjoining $u$ to this basis produces an orthornomal basis of $V$ consisting of eigenvectors of $T$.
Therefore (b) holds.

_Exercise 14_

Suppose $U$ has a basis $e_1, \dots, e_n$ consisting of eigenvectors of $T$.
We can assume without loss of generality that this list is normalized (we can divide each vector by its norm if it isn't).
Define $\langle \cdot, \cdot \rangle: U \times U \to \mathbb{R}$ by

$$
\langle a_1 e_1 + \dots + a_n e_n, b_1 e_1 + \dots + b_n e_n \rangle = a_1b_1 + \dots + a_nb_n.
$$

Since every vector in $U$ can be uniquely written as linear combination of $e_1, \dots, e_n$, this function is well defined.
Moreover, one easily checks that this function is an inner product.
Note that

$$
\langle e_j, e_k \rangle = \langle 0e_1 + \dots + 1e_j + \dots + 0e_n, 0e_1 + \dots + 1e_k + \dots + 0e_n \rangle =
\begin{cases}
1, \text{ if } j = k\\\\
0, \text{ if } j \neq k
\end{cases}.
$$

Therefore $e_1, \dots, e_n$ is also orthonormal.
The Real Spectral Theorem (7.29) now implies that $T$ is self-adjoint.

The converse follows directly from 7.29.

_Exercise 15_

We have

$$
\begin{pmatrix} 1 & 1 & 0\\\\ 0 & 1 & 1\\\\ 1 & 0 & x \end{pmatrix} \begin{pmatrix} 1 & 0 & 1\\\\ 1 & 1 & 0\\\\ 0 & 1 & x \end{pmatrix} = \begin{pmatrix} 1 & 0 & 1\\\\ 1 & 1 & 0\\\\ 0 & 1 & x \end{pmatrix} \begin{pmatrix} 1 & 1 & 0\\\\ 0 & 1 & 1\\\\ 1 & 0 & x \end{pmatrix}.
$$

Multiplying the third row with the second column on both sides we get

$$
1\cdot0 + 0\cdot1 + x\cdot1 = 0\cdot1 + 1\cdot1 + x\cdot0,
$$

therefore $x = 1$.
