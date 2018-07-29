Chapter 7: **Operators on Inner Product Spaces**

**7.A**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [x] Exercise 5
- [x] Exercise 6
- [x] Exercise 7
- [x] Exercise 8
- [x] Exercise 9
- [ ] Exercise 10
- [x] Exercise 11
- [x] Exercise 12
- [x] Exercise 13
- [x] Exercise 14
- [x] Exercise 15
- [x] Exercise 16
- [x] Exercise 17
- [x] Exercise 18
- [x] Exercise 19
- [x] Exercise 20
- [x] Exercise 21

_Exercise 1_

We have

$$
\begin{align}
\langle (z_1, \dots, z_n), T^*(x_1, \dots, x_n) \rangle &= \langle T(z_1, \dots, z_n), (x_1, \dots, x_n) \rangle\\\\
&= \langle (0, z_1, \dots, z_{n-1}), (x_1, \dots, x_n) \rangle\\\\
&= z_1\overline{x_2} + \dots + z_{n-1}\overline{x_n}\\\\
&= \langle (z_1, \dots, z_n), (x_2, \dots, x_n, 0) \rangle.
\end{align}
$$

Thus $T^*(x_1, \dots, x_n) = (x_2, \dots, x_n, 0)$.

_Exercise 2_

Clearly, it suffices to prove one direction.
Suppose $\lambda$ is an eigenvalue of $T$.
Then

$$
\operatorname{null} (T^* - \overline{\lambda}I) = \operatorname{null} (T - \lambda I)^* = (\operatorname{range} (T - \lambda I))^\perp,
$$

where the last equality comes from 7.7.
Now, since $\dim \operatorname{null} (T - \lambda I) > 0$, the subspace on the right has non zero dimension and the result follows.

_Exercise 3_

Suppose $U$ is invariant under $T$.
Let $u \in U$ and $w \in U^\perp$.
Then

$$
\langle u, T^*w \rangle = \langle Tu, w \rangle = 0,
$$

where the second equality follows because $Tu \in U$.
Thus $T^*w \in U^\perp$.

The converse is the same, because $(T^*)^\* = T$ and $(U^\perp)^\perp = U$.

_Exercise 4_

Since $(T^\*)^\* = T$, the statements in (a) and (b) are equivalent, so we give a single proof.

This follows directly from 7.7 (b) and 6.46 (b).
We have

$$
\begin{aligned}
T \text{ is injective } &\iff \operatorname{null} T = 0\\\\
&\iff (\operatorname{range} T^\*)^\perp = \\{0\\}\\\\
&\iff \operatorname{range} T^\* = V\\\\
&\iff T^* \text{ is surjective. }
\end{aligned}
$$

_Exercise 5_

We have

$$
\begin{aligned}
\operatorname{dim} \operatorname{null} T^* &= \operatorname{dim} (\operatorname{range} T)^\perp\\\\
&= \operatorname{dim} W - \operatorname{dim} \operatorname{range} T\\\\
&= \operatorname{dim} W + \operatorname{dim} \operatorname{null} T - \operatorname{dim} V
\end{aligned}
$$

where the first line follows from 7.7 (a), the second from 6.50 and the third from 3.22.
We alse have

$$
\begin{aligned}
\operatorname{dim} \operatorname{range} T^* &= \operatorname{dim} (\operatorname{null} T)^\perp\\\\
&= \operatorname{dim} V - \operatorname{dim} \operatorname{null} T\\\\
&= \operatorname{dim} \operatorname{range} T
\end{aligned}
$$

where the first line follows from 7.7 (b), the second from 6.50 and the third from 3.22.

_Exercise 6_

_(a)_
If $T$ were self-adjoint, we would have

$$
\langle Tp, q \rangle = \langle p, T^*q \rangle = \langle p, Tq \rangle.
$$

However, let $p(x) = a_0 + a_1 x + a_2 x^2$ and $q(x) = b_0 + b_1 x + b_2 x^2$.
We have

$$
\begin{aligned}
\langle Tp, q \rangle &= \langle a_1 x, q \rangle\\\\
&= a_1 \int_0^1 b_0x + b_1x^2 + b_2x^3\\:dx\\\\
&= a_1 \left(\frac{b_0}{2}x^2 + \frac{b_1}{3}x^3 + \frac{b_2}{4}x^4\right)\biggr\rvert_0^1\\\\
&= a_1 \left(\frac{b_0}{2} + \frac{b_1}{3} + \frac{b_2}{4}\right).
\end{aligned}
$$

Similarly

$$
\langle p, Tq \rangle = \langle p, b_1x \rangle = b_1 \left(\frac{a_0}{2} + \frac{a_1}{3} + \frac{a_2}{4}\right).
$$

Thus, taking $a_1 = 0$ and $b_1, a_0, a_2 > 0$ clearly shows $\langle Tp, q \rangle \neq \langle p, Tq \rangle$.

_(b)_
7.10 requires the chosen basis to be orthonormal.

_Exercise 7_

Keep in mind that, by 7.6 (c), $(ST)^\* = T^\*S^\*$.

Suppose $ST$ is self adjoint.
Then

$$
ST = (ST)^\* = T^\*S^\* = TS.
$$

Conversely, suppose $ST = TS$.
Then

$$
ST = TS = T^\*S^\* = (ST)^\*.
$$

_Exercise 8_

Suppose $S, T \in \mathcal{L}(V)$ are self-adjoint.
Then

$$
(S + T) = S + T = S^\* + T^\* = (S + T)^\*,
$$

proving that $S + T$ is self-adjoint.
Let $\lambda \in \mathbb{R}$.
Then

$$
(\lambda T) = \lambda T = \lambda T^\* = (\overline{\lambda}T)^\* = (\lambda T)^\*,
$$

proving that $\lambda T$ is self adjoint.

_Exercise 9_

From the previous exercise, we see that $(\lambda T) = (\overline{\lambda}T)^\*$. Therefore, if $\lambda$ is not real, we cannot have $(\lambda T) = (\lambda T)^\*$

_Exercise 11_

Note that $P^2 = P$ implies that $Pu = u$ for $u \in \operatorname{range} P$.

Suppose $P = P_U$ for some subspace $U$ of $V$.
Let $v_1, v_2 \in V$.
We have $v_1 = u_1 + w_1$ and $v_2 = u_2 + w_2$ for some $u_1, u_2 \in U$ and $w_1, w_2 \in U^\perp$.
Then

$$
\begin{aligned}
\langle v_1, P^*v_2 \rangle &= \langle Pv_1, v_2 \rangle\\\\
&= \langle u_1, u_2 + w_2 \rangle\\\\
&= \langle u_1, u_2 \rangle\\\\
&= \langle u_1 + w_1, u_2 \rangle\\\\
&= \langle v_1, u_2 \rangle\\\\
&= \langle v_1, Pv_2 \rangle.
\end{aligned}
$$

Therefore $P = P^*$.

Conversely, suppose $P$ is self-adjoint.
Then, by 7.7 (a), $(\operatorname{range} P)^\perp = \operatorname{null} P^* = \operatorname{null} P$, and so, by 6.47, we have $V = \operatorname{range} P \oplus \operatorname{null} P$.
Let $U = \operatorname{range} P$ and $v \in V$.
We can write $v = u + w$ for some $u \in \operatorname{range} P$ (which equals $U$) and $w \in \operatorname{null} P$ (which equals $U^\perp$).
Therefore

$$
Pv = Pu + Pw = Pu = u = P_U u = P_U u + P_U w = P_U v.
$$

Hence $P = P_U$.

_Exercise 12_

Let $u$ and $w$ denote normalized eigenvectors corresponding to $3$ and $4$.
By 7.22, $u$ and $w$ are orthogonal.
From the Pythagorean Theorem, we have

$$
||u + w||^2 = ||u||^2 + ||w||^2 = 2
$$

and

$$
||T(u+w)||^2 = ||3u + 4w||^2 = ||3u||^2 + ||4w||^2 = 9 + 16 = 25.
$$

Letting $v = u + w$ and taking the square root of each equation gives the desired result.

_Exercise 13_

Define $T \in L(\mathbb{C}^4)$ by

$$
T(z_1, z_2, z_3, z_4) = (z_4, z_1, z_2, z_3).
$$

We have

$$
\begin{aligned}
\langle (z_1, z_2, z_3, z_4), T^\*(x_1, x_2, x_3, x_4) \rangle
&= \langle T(z_1, z_2, z_3, z_4), (x_1, x_2, x_3, x_4) \rangle\\\\
&= \langle (z_4, z_1, z_2, z_3), (x_1, x_2, x_3, x_4) \rangle\\\\
&= z_4\overline{x_1} + z_1\overline{x_2} + z_2\overline{x_3} + z_3\overline{x_4}\\\\
&= \langle (z_1, z_2, z_3, z_4), (x_2, x_3, x_4, x_1) \rangle.
\end{aligned}
$$

Thus $T^*(z_1, z_2, z_3, z_4) = (z_2, z_3, z_4, z_1)$.
Note that $T$ is normal ($T^\*T$ and $TT^\*$ equal the identity), however $T \neq T^\*$.

_Exercise 14_

Since $v$ and $w$ are eigenvectors corresponding to distinct eigenvalues, by 7.22 they are orthogonal.
Thus

$$
\begin{aligned}
||T(v + w)||^2 &= ||Tv + Tw||^2\\\\
&= ||3v + 4w||^2\\\\
&= ||3v||^2 + ||4w||^2\\\\
&= 9||v||^2 + 16||w||^2\\\\
&= 100,
\end{aligned}
$$

where the third line follows from the Pythagorean Theorem.

_Exercise 15_

Let $w_1, w_2 \in V$.
We have

$$
\begin{aligned}
\langle w_1, T^\*w_2 \rangle &= \langle Tw_1, w_2 \rangle\\\\
&= \langle \langle w_1, u \rangle x, w_2 \rangle\\\\
&= \langle w_1, u \rangle \langle x, w_2 \rangle\\\\
&= \langle w_1, \overline{\langle x, w_2 \rangle} u \rangle\\\\
&= \langle w_1, \langle w_2, x \rangle u \rangle\\\\
\end{aligned}
$$

Hence $T^\*v = \langle v, x \rangle u$.

_(a)_
Suppose $T$ is selft-adjoint.
Then

$$
\langle v, u \rangle x - \langle v, x \rangle u = Tv - T^\*v = 0,
$$

for all $v \in V$.
We can assume $u$ and $x$ are non-zero (otherwise there is nothing to prove).
Taking $v = u$ forces $\langle v, u \rangle \neq 0$, showing that $x$ and $u$ are linearly dependent.

Conversely, suppose $x$ and $u$ are linearly dependent.
We can assume $x$ and $u$ are non-zero, otherwise $T$ would equal $0$, which already is self-adjoint.
Then $u = cx$, for some non-zero $c \in \mathbb{R}$.
Thus

$$
\begin{aligned}
Tv &= \langle v, u \rangle x\\\\
&= \langle v, cx \rangle \frac{1}{c}u\\\\
&= \langle v, x \rangle u\\\\
&= T^\* v.
\end{aligned}
$$

Therefore $T = T^\*$.

_(b)_
Again, we can assume $u$ and $x$ are both non-zero in both directions of the proof.

We have

$$
\begin{aligned}
\langle \langle v, u \rangle x, x \rangle u &= T^\*(\langle v, u \rangle x)\\\\
&= T^\*Tv\\\\
&= TT^\*v\\\\
&= T(\langle v, x \rangle u)\\\\
&= \langle \langle v, x \rangle u, u \rangle x.
\end{aligned}
$$

Taking $v = u$ ensures $\langle \langle v, u \rangle x, x \rangle \neq 0$, showing that $u$ and $x$ are linearly dependent.

Conversely, suppose $x$ and $u$ are linearly dependent.
Then $u = cx$ for some non-zero $c \in \mathbb{F}$.
Then

$$
\begin{aligned}
&= TT^\*v\\\\
&= T(\langle v, x \rangle u)\\\\
&= \langle \langle v, x \rangle u, u \rangle x\\\\
&= \langle \langle v, x \rangle x, cx \rangle cx\\\\
&= \langle \langle v, cx \rangle x, x \rangle cx\\\\
&= \langle \langle v, u \rangle x, x \rangle u\\\\
&= T^\*(\langle v, u \rangle x)\\\\
&= T^\*Tv.
\end{aligned}
$$

Hence $TT^\* = T^\*T$.

_Exercise 16_

Suppose $u \in \operatorname{null} T$.
Then, by 7.20,

$$
0 = ||Tu|| = ||T^\*u||,
$$

which implies that $u \in \operatorname{null} T^\*$.
Hence $\operatorname{null} T = \operatorname{null} T^*$ (because $(T^\*)^\* = T$ and the same argument can be repeated).
Now we have

$$
\begin{aligned}
\operatorname{range} T &= (\operatorname{null} T^\*)^\perp\\\\
&= (\operatorname{null} T)^\perp\\\\
&= \operatorname{range} T^*,
\end{aligned}
$$

where the first and last equality follow from items (d) and (b) of 7.7.

_Exercise 17_

Suppose $w \in \operatorname{range} T$ and $w \neq  0$.
By 7.7 (d), we see that $w \in (\operatorname{null} T^\*)^\perp$.
In the previous exercise, we saw that $\operatorname{null} T = \operatorname{null} T^\*$,
thus $w \in (\operatorname{null} T)^\perp$.
Since $\operatorname{null} T \cap (\operatorname{null} T)^\perp = \\{0\\}$, it follows that $w \notin \operatorname{null} T$.

With this reasoning in mind, one can easily see (or show by induction on $k$) that if $v \notin \operatorname{null} T$ then $v \notin \operatorname{null} T^{k}$ for any positive integer $k$.
Therefore, taking the contrapositive of this statement, we see that $\operatorname{null} T^k \subset \operatorname{null} T$.
The inclusion in the other direction is obvious, hence $\operatorname{null} T^k = \operatorname{null} T$.

Therefore

$$
\begin{aligned}
\operatorname{range} T^k &= (\operatorname{null} (T^k)^*)^\perp\\\\
&= (\operatorname{null} T^k)^\perp\\\\
&= (\operatorname{null} T)^\perp\\\\
&= \operatorname{range} T^\*\\\\
&= \operatorname{range} T,
\end{aligned}
$$

where the first line follows from 7.7 (d), the second and the last were proved in the previous exercise and the fourth follows from 7.7 (b).

_Exercise 18_

We give a counterexample.
Let $V = \mathbb{R}^2$ and $T$ defined by

$$
Te_1 = e_1 + e_2,
Te_2 = - e_1 - e_2
$$

where $e_1, e_2$ is the standard basis of $\mathbb{R}^2$.
Its matrix with respect to the same basis is

$$
\begin{pmatrix}
1 & -1\\\\
1 & -1
\end{pmatrix}.
$$

Taking the transpose, we see that $T^*$ is defined by

$$
T^\*e_1 = e_1 - e_2,
T^\*e_2 = e_1 - e_2.
$$

Note that $||Te_1|| = ||T^\*e_1||$ and $||Te_2|| = ||T^\*e_2||$.
However $\mathcal{M}(T^\*)\mathcal{M}(T) \neq \mathcal{M}(T)\mathcal{M}(T^\*)$, thus $T$ is not normal.

_Exercise 19_

We saw in Exercise 16 that $\operatorname{null} T = \operatorname{null} T^*$ (for $T$ normal).
Thus $(z_1, z_2, z_3) \in \operatorname{null} T$ and we have

$$
\begin{aligned}
0 &= \langle T^\*(z_1, z_2, z_3), (1, 1, 1) \rangle\\\\
&= \langle (z_1, z_2, z_3), T(1, 1, 1) \rangle\\\\
&= \langle (z_1, z_2, z_3), (2, 2, 2) \rangle\\\\
&= 2z_1 + 2z_2 + 3z_3.
\end{aligned}
$$

Dividing by $2$ yields the desired result.

_Exercise 20_

Let $v \in V$ and $w \in W$.
Then

$$
\begin{aligned}
((\Phi_V \circ T^*)(w))(v) &= (\Phi_V(T^\*w))(v)\\\\
&= \langle v, T^\*v \rangle\\\\
&= \langle Tv, w \rangle.
\end{aligned}
$$

On the other hand, we have

$$
\begin{aligned}
((T' \circ \Phi_W)(w))(v) &= (T' \circ \Phi_W(w))(v)\\\\
&= (\Phi_W(w) \circ T)(v)\\\\
&= (\Phi_W(w))(Tv)\\\\
&= \langle Tv, w \rangle.
\end{aligned}
$$

Therefore $\Phi_V \circ T^* = T' \circ \Phi_W$.

_Exercise 21_

_(a)_
Let $e_j = \frac{\cos jx}{\sqrt{\pi}}$ and $f_j = \frac{\sin jx}{\sqrt{\pi}}$.
By Exercise 4 in section 6B, $\frac{1}{\sqrt{2\pi}}, e_1, \dots, e_n, f_1, \dots, f_n$ is an orthonormal basis of $V$.
Note that $De_j = -jf_j$ and $Df_j = je_j$.
Then, for any $v, w \in V$, we have

$$
\begin{aligned}
\langle v, D^\*w \rangle &= \langle Dv, w \rangle\\\\
&= \left\langle D\left(\left\langle v, \frac{1}{\sqrt{2\pi}} \right\rangle \frac{1}{\sqrt{2\pi}} + \sum_{j=1}^n (\langle v, e_j \rangle e_j + \langle v, f_j \rangle f_j)\right), w \right\rangle\\\\
&= \left\langle \sum_{j=1}^n (-j\langle v, e_j \rangle f_j + j\langle v, f_j \rangle e_j), \left\langle w, \frac{1}{\sqrt{2\pi}} \right\rangle \frac{1}{\sqrt{2\pi}} + \sum_{j=1}^n (\langle w, e_j \rangle e_j + \langle w, f_j \rangle f_j) \right\rangle\\\\
&= \sum_{j=1} (-j\langle v, e_j \rangle \langle w, f_j \rangle + j\langle v, f_j \rangle \langle w, e_j \rangle)\\\\
&= \left\langle \left\langle v, \frac{1}{\sqrt{2\pi}} \right\rangle \frac{1}{\sqrt{2\pi}} + \sum_{j=1}^n (\langle v, e_j \rangle e_j + \langle v, f_j \rangle f_j), \sum_{j=1}^n (-j\langle w, f_j \rangle e_j + j\langle w, e_j \rangle f_j)\right\rangle\\\\
&= \langle v, -Dw \rangle.
\end{aligned}
$$

Hence $D^\* = -D$.
Obviously $D$ is normal but not self-adjoint.

_(b)_
Note that $T = D^2$.
Thus $T^\* = (DD)^\* = D^\*D\^* = (-D)(-D) = D^2 = T$.
