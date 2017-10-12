Chapter 7: **Operators on Inner Product Spaces**

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
- [ ] Exercise 11
- [x] Exercise 12
- [x] Exercise 13
- [x] Exercise 14
- [x] Exercise 15
- [x] Exercise 16
- [x] Exercise 17
- [x] Exercise 18
- [ ] Exercise 19
- [ ] Exercise 20

_Exercise 1_

A quick calculation shows that $T^\*Tv = ||x||^2\langle v, u \rangle u$ for every $v \in V$.
The map $R \in \mathcal{L}(V)$ defined by

$$
Rv = \frac{||x||}{||u||}\langle v, u \rangle u
$$

is a square root of $T\^*T$.
Moreover, it is easy to check that $\langle Rv, v \rangle \ge 0$ for all $v \in V$.
We but need to prove that $R$ is self-adjoint.
Let $e_1, \dots, e_n$ be an orthonormal basis of $V$.
We can write

$$
u = a_1 e_1 + \dots + a_n e_n
$$

for some $a_1, \dots, a_n \in \mathbb{F}$.
Note that

$$
Re_j = \frac{||x||}{||u||}\langle e_j, u \rangle u = \frac{||x||}{||u||}(a_j \overline{a_1} e_1 + \dots + a_j \overline{a_n} e_n).
$$

Therefore, the matrix of $R$ with respect to the basis $e_1, \dots, e_n$ has entries defined by

$$
\mathcal{M}(R)_{j, k} = \frac{||x||}{||u||}a_j \overline{a_k}.
$$

Thus $\mathcal{M}(R)\_{j, k} = \overline{\mathcal{M}(R)\_{k, j}}$, that is, $\mathcal{M}(R) = \mathcal{M}(R^\*)$.
Hence $R$ is self-adjoint.

_Exercise 2_

Define $T \in \mathcal{L}(\mathbb{C}^2)$ by

$$
\begin{aligned}
Te_1 &= 0\\\\
Te_2 &= 5e_1
\end{aligned}
$$

where $e_1, e_2$ is the standard basis of $\mathbb{C}^2$.
Then the matrix of $T$ with respect to this is basis is

$$
\mathcal{M}(T) = \begin{pmatrix}0 & 5\\\\0 & 0\end{pmatrix},
$$

which is upper triangular.
Thus $0$ is the only eigenvalue of $T$.
We have

$$
\mathcal{M}(T^\*T) = \mathcal{M}(T^\*)\mathcal{M}(T) = \begin{pmatrix}0 & 0\\\\5 & 0\end{pmatrix}\begin{pmatrix}0 & 5\\\\0 & 0\end{pmatrix} = \begin{pmatrix}0 & 0\\\\0 & 25\end{pmatrix}.
$$

Hence the eigenvalues of $T^\*T$ are $0$ and $25$.
By 7.52, the singular values of $T$ are $0$ and $5$.

_Exercise 3_

By the Polar Decomposition (7.45), there exists an isometry $S \in \mathcal{L}(V)$ such that $T^\* = S\sqrt{TT^\*}$.
Taking the adjoint of each side, we get

$$
T = (S\sqrt{TT\^*})^\* = (\sqrt{TT^\*})\^*S^\* = \sqrt{TT^\*}S^\*,
$$

where the last equality follows because $\sqrt{TT^\*}$ is self-adjoint.
This yields the desired result, because $S^\*$ is also an isometry.

_Exercise 4_

Let $v \in V$ be an eigenvector of $\sqrt{T^\*T}$ with $||v|| = 1$ corresponding to $s$ and let $S \in \mathcal{L}(V)$ be an isometry such that $T = S\sqrt{T^\*T}$.
Then

$$
||Tv|| = ||S\sqrt{T^\*T}v|| = ||\sqrt{T^\*T}v|| = |s|\\:||v|| = |s| = s,
$$

where the last equality follows because $\sqrt{T^\*T}$ is positive.

_Exercise 5_

We have

$$
\mathcal{M}(T^\*T) = \mathcal{M}(T^\*)\mathcal{M}(T) = \begin{pmatrix}0 & 1\\\\-4 & 0\end{pmatrix}\begin{pmatrix}0 & -4\\\\1 & 0\end{pmatrix} = \begin{pmatrix}1 & 0\\\\0 & 16\end{pmatrix}.
$$

Therefore, the singular values of $T$ are $1$ and $4$.

_Exercise 6_

We will use the orthonormal basis $\sqrt{\frac{1}{2}}, \sqrt{\frac{3}{2}}x, \sqrt{\frac{45}{8}}\left(x^2 - \frac{1}{3}\right)$ of $\mathcal{P}_2(\mathbb{R})$, which was found in the example.

We have

$$
\begin{aligned}
D\sqrt{\frac{1}{2}} &= 0\\\\
D\sqrt{\frac{3}{2}}x &= \sqrt{3}\left(\sqrt{\frac{1}{2}}\right)\\\\
D\sqrt{\frac{45}{8}}\left(x^2 - \frac{1}{3}\right) &= \sqrt{15}\left(\sqrt{\frac{3}{2}}x\right).
\end{aligned}
$$

Therefore

$$
\mathcal{M}(D) =
\begin{pmatrix}
0 & \sqrt{3} & 0\\\\
0 & 0 & \sqrt{15}\\\\
0 & 0 & 0
\end{pmatrix}.
$$

Thus

$$
\mathcal{M}(D^\*D) =
\begin{pmatrix}
0 & 0 & 0\\\\
\sqrt{3} & 0 & 0\\\\
0 & \sqrt{15} & 0
\end{pmatrix}
\begin{pmatrix}
0 & \sqrt{3} & 0\\\\
0 & 0 & \sqrt{15}\\\\
0 & 0 & 0
\end{pmatrix} =
\begin{pmatrix}
0 & 0 & 0\\\\
0 & 3 & 0\\\\
0 & 0 & 15
\end{pmatrix}.
$$

Thus, the singular values of $D$ are $0, \sqrt{3}, \sqrt{15}$.

_Exercise 7_

A quick calculation, like the ones in the previous exercises, shows that

$$
T^\*T(z_1, z_2, z_3) = (4z_1, 9z_2, z_3).
$$

Thus

$$
\sqrt{T^\*T}(z_1, z_2, z_3) = (2z_1, 3z_2, z_3).
$$

Define $S \in \mathcal{L}(\mathbb{F}^3)$ by

$$
S(z_1, z_2, z_3) = (z_3, z_1, z_2).
$$

$S$ is clearly an isometry (it maps the standard basis, which is orthonormal, to a permutation of the standard basis) and we have $S\sqrt{T^\*T} = T$.

_Exercise 8_

Let $S' \in \mathcal{L}(V)$ be an isometry such that $T = S'\sqrt{T^\*T}$.
Then

$$
\begin{aligned}
0 &= ||Tv|| - ||Tv||\\\\
&= ||S^\*Tv|| - ||S'^\*Tv||\\\\
&= ||Rv|| - ||\sqrt{T^\*T}v||\\\\
&= \langle R^\*Rv, v \rangle - \langle T^\*Tv, v \rangle\\\\
&= \langle (R^\*R - T^\*T)v, v \rangle\\\\
&= \langle (R^2 - T^\*T)v, v \rangle
\end{aligned}
$$

where the last line follows because $R$ is self-adjoint.
7.16 now implies that $R^2 = T^\*T$.
Since $R$ is positive and the positive square root of $T^\*T$ is unique (by 7.36), it follows that $R = \sqrt{T^\*T}$.

_Exercise 9_

Consider the proof of 7.45.
$T$ being invertible implies $\operatorname{dim} (\operatorname{range} T)^\perp = 0$, thus $S_2 = 0$ and so $S = S_1$.
Clearly $S_1$ is unique, so $S$ must also be unique.
Conversely, if $S$ is unique then $S_2 = 0$, otherwise we could set $S = S_1 - S_2$ and it would still be an isometry satisfying $T = S\sqrt{T^\*T}$.
This implies that $m = 0$, because from the defintion we see that $S_2$ must be invertible for any positive integer $m$.
Thus $\operatorname{dim} (\operatorname{range} T)^\perp = 0$ and so $T$ is invertible.

_Exercise 10_

Suppose $\lambda$ is an eigenvalue of $T$ and $v$ a corresponding eigenvector.
Then

$$
T^\*Tv = T^2v = \lambda^2 v = |\lambda|^2v,
$$

where the last equality follows because the eigenvalues of self-adjoint operators are real (see 7.13).
Therefore, the eigenvectors of $T$ are also eigenvectors of $T^\*T$ with corresponding eigenvalues squared.
Since $T$ has a basis consisting of eigenvectors, so does $T^\*T$ and thus all eigenvalues of $T^\*T$ are squares of the absolute values of eigenvalues of $T$.
7.52 now implies that the singular values of $T$ are the absolute values of the eigenvalues of $T$.

_Exercise 12_

As a counterexample, take the linear map $T$ from Exercise 5.
We have

$$
\mathcal{M}((T^2)^\*T^2) = \mathcal{M}(T^*)^2\mathcal{M}(T)^2 = \begin{pmatrix}-4 & 0\\\\0 & -4\end{pmatrix}\begin{pmatrix}-4 & 0\\\\0 & -4\end{pmatrix}
= \begin{pmatrix}16 & 0\\\\0 & 16\end{pmatrix}.
$$

Therefore, the singular values of $T^2$ are $4, 4$.
However, the singular values of $T$ are $1, 4$.

_Exercise 13_

Suppose $T$ is invertible.
Then

$$
\operatorname{null} T^\* = (\operatorname{range} T)^\perp = V^\perp = \\{0\\},
$$

where the first equality follows from 7.7 and the second because $T$ is surjective.
This shows that $T^\*$ is also invertible.
Therefore $0$ is not eigenvalue of $T^\*T$ and so, by 7.52, it cannot be a singular value of $T$.

Conversely, suppose $0$ is not a singular value of $T$.
Then $T^\*Tv \neq 0$ for all non-zero $v \in V$.
This implies that $Tv \neq 0$ for all non-zero $v \in V$.
Thus $T$ is invertible.

_Exercise 14_

First we will prove that $\operatorname{range} T = \operatorname{range} T^\*T$.
From Exercise 5 in section 7A we see that $\operatorname{range} T = \operatorname{range} T^\*$.

Suppose $w \in \operatorname{range} T$.
Then $w \in \operatorname{range} T^\*$.
Thus $w = T^\*v$ for some $v \in V$.
We can write $v = v' + v''$ for some $v' \in \operatorname{null} T^\*$ and $v'' \in (\operatorname{null} T^\*)^\perp$.
Thus $w = T^\*v''$.
But 7.7 shows that $(\operatorname{null} T^\*)^\perp = \operatorname{range} T$.
Therefore $v'' = Tu$ for some $u \in V$ and so $w = T^\*Tu \in \operatorname{range}{T^\*T}$.
Hence $\operatorname{range} T \subset \operatorname{range} T^\*T$.

The inclusion in the other direction is easy.
We have

$$
\operatorname{range} T^\*T \subset \operatorname{range} T^\* = \operatorname{range} T.
$$

Therefore $\operatorname{range} T = \operatorname{range} T^\*T$.

Since $\sqrt{T^\*T}$ is diagonalizable (because it is self-adjoint), it follows that the number of nonzero singular values of $T$ equals the dimension of $\operatorname{range} \sqrt{T^\*T}$.
Note that $\operatorname{range} T^\*T = \operatorname{range} \sqrt{T^\*T}$.
Therefore $\operatorname{dim} \operatorname{range} \sqrt{T^\*T} = \operatorname{dim} \operatorname{range} T$, completing the proof.

_Exercise 15_

The forward direction is obvious, because if $S$ is an isometry, then $\sqrt{S^\*S}$ equals the identity, whose eigenvalues equal $1$.

Suppose all singular values of $S$ equal $1$.
This implies that $\sqrt{S^\*S}$, and therefore so does $S^\*S$, equals the identity.
7.42 now implies that $S$ is an isometry.

_Exercise 16_

Let $S_1, S_2 \in \mathcal{L}(V)$ be isometries such that $T_1 = S_1\sqrt{T_1^\*T_1}$ and $T_2 = S_2\sqrt{T_2^\*T_2}$ and let $e_1, \dots, e_n$ and $f_1, \dots, f_n$ be orthonormal basis of $V$ consisting of eigenvectors of $T_1$ and $T_2$, respectively, corresponding to the singular values $s_1, \dots, s_n$.
Defin $S \in \mathcal{L}(V)$ by

$$
Se_j = f_j
$$

for each $j = 1, \dots, n$.
Then $S$ is also an isometry and we have

$$
\begin{aligned}
\sqrt{T_1^\*T_1}e_j &= s_je_j\\\\
&= S^\*(s_jf_j)\\\\
&= S^\*\sqrt{T_2^\*T_2}f_j\\\\
&= S^\*\sqrt{T_2^\*T_2}Se_j.
\end{aligned}
$$

So $\sqrt{T_1^\*T_1} =  S^\*\sqrt{T_2^\*T_2}S$.
Therefore

$$
T_1 = S_1\sqrt{T_1^\*T_1} = S_1S^\*\sqrt{T_2^\*T_2}S = S_1S^\*S_2^\*T_2S,
$$

where the last equality follows by multiplying both sides of the equation $T_2 = S_2\sqrt{T_2^\*T_2}$ by $S_2^\*$.
This gives the desired result, because the product of isometries is also an isometry.

_Exercise 17_

_(a)_
We have $Te_j = s_jf_j$.
This implies that the matrix of $T$ if respect to the bases $e_1, \dots, e_n$ and $f_1, \dots, f_n$ is the diagonal matrix whose diagonal entries are the singular values of $T$.
By 7.10, we have $T^\*f_j = s_je_j$ for each $j$.
If we replace $v$ with $f_j$ in the right hand side of the desired result we get the same thing, therefore

$$
T^\*v = s_1\langle v, f_1 \rangle e_1 + \dots + s_n \langle v, f_n \rangle e_n
$$

by uniqueness of linear maps (see 3.5).

_(b)_
Just apply the previous item to the formula given of the singular value decomposition of $T$.

_(c)_
Note that the $e_j$'s are eigenvectors of $T^\*T$ with corresponding eigenvalue $s_j^2$.
Thus $\sqrt{T^\*T}e_j = s_je_j$.
Plugging $e_j$ in the place of $v$ in the right hand side yields the same thing, so the result holds by uniqueness of linear maps again.

_(d)_
The given formula satisfies $TT^{-1} = I$ and $T^{-1}T = I$ and it is well defined, because from Exercise 13 we see that none of $s_j$'s are $0$.

_Exercise 18_

_(a)_
Use the same notation from the Singular Value Decompositon theorem (7.52).
We have

$$
\begin{aligned}
||Tv||^2
&= |s_1\langle v, e_1 \rangle|^2 + \dots + |s_n\langle v, e_n \rangle|^2\\\\
&= |s_1|^2|\langle v, e_1 \rangle|^2 + \dots + |s_n|^2|\langle v, e_n \rangle|^2\\\\
&\le |s|^2|\langle v, e_1 \rangle|^2 + \dots + |s|^2|\langle v, e_n \rangle|^2\\\\
&= |s|^2{|\langle v, e_1 \rangle|^2 + \dots + |\langle v, e_n \rangle|^2}\\\\
&= s^2||v||^2
\end{aligned}
$$

for all $v \in V$, where the first line follows from the Pythagorean Theorem (6.13) and last because $s$ is a positive real value.
Taking the square root of both sides shows that $||Tv|| \le s||v||$ for all $v \in V$.
The proof that $\hat{s}||v|| \le ||Tv||$ is almost the same.

_(b)_
Let $v$ be an eigenvector of $T$ corresponding to $\lambda$ with $||v|| = 1$.
Then

$$
|\lambda| = |\lambda|\\:||v|| = ||Tv|| \le s||v|| = s.
$$

Similarly, we have $\hat{s} \le |\lambda|$.
