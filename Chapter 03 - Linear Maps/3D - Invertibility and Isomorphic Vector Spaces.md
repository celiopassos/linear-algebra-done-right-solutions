Chapter 3: **Linear Maps**

**3.D**

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
- [x] Exercise 16
- [x] Exercise 17
- [x] Exercise 18
- [x] Exercise 19
- [x] Exercise 20

_Exercise 1_

We have that

$$
(T^{-1}S^{-1})(ST) = T^{-1}S^{-1}ST = T^{-1}T = I
$$

And

$$
(ST)(T^{-1}S^{-1}) = STT^{-1}S^{-1} = SS^{-1} = I
$$

Hence, $ST$ is invertible and $(ST)^{-1} = T^{-1}S^{-1}$.

_Exercise 2_

Let $N$ be the set of noninvertible operators on $V$.
Let $v_1, \dots, v_n$ be a basis of $V$. Define $S,T \in \mathcal{L}(V)$ such that

$$
\begin{aligned}
S(a_1 v_1 + \dots + a_n v_n) &= a_1 v_1\\\\
T(a_1 v_1 + \dots + a_n v_n) &= a_2 v_2 + \dots + a_n v_n
\end{aligned}
$$

Neither $S$ and $T$ are surjective, hence both are in $N$.
But $S + T = I$ and $I$ is clearly invertible.
Thus, $S + T \notin N$ and $N$ is not closed under addition.

_Exercise 3_

Suppose $T \in \mathcal{L}(V)$ is an invertible operator such that $Tu = Su$ for every $u \in U$.
Let $u_1, u_2 \in U$ such that $Su_1 = Su_2$.
Then

$$
Tu_1 = Su_1 = Su_2 = Tu_2
$$

Because $T$ is injective, it follows that $u_1 = u_2$.
Therefore, $S$ is also injective.

Conversely, suppose $S$ is injective.
Let $u_1, \dots, u_n$ be a basis of $U$ and extend it to a basis $u_1, \dots, u_n, v_1, \dots, v_m$ of $V$.
Because $\operatorname{dim} S = 0$, it follows that $Su_1, \dots, Su_n$ is linearly independent and we can extend it to a basis $Su_1, \dots, Su_n, \nu_1, \dots, \nu_m$ of $V$.
Define $T \in \mathcal{L}(V)$ by

$$
\begin{aligned}
Tu_j &= Su_j, \text{ for } j=1, \dots, n\\\\
Tv_j &= \nu_j, \text{ for } j=1, \dots, m
\end{aligned}
$$

Because $Su_1, \dots, Su_n, \nu_1, \dots, \nu_m$ is linearly independent, it follows that $\operatorname{null} T = \{0\}$.
Hence, $T$ is injective and, therefore, invertible.

_Exercise 4_

For the implication in the forward direction, by _Exercise 3_ we only need to prove the existence of an injective linear map $S \in \mathcal{L}(\operatorname{range} T_2, W)$ such that $T_1 = ST_2$.

Let $w_1, \dots, w_n$ be a basis of $\operatorname{range} T_2$ and $v_1, \dots, v_n \in V$ a reverse image of it when $T_2$ is applied.
Because $T_2 v_1, \dots, T_2 v_n$ is linearly independent, it follows that $\operatorname{null} T_2 \cap \operatorname{span}(v_1, \dots, v_n) = \\{0\\}$. Hence $\operatorname{null} T_2 + \operatorname{span}(v_1, \dots, v_n)$ is a direct sum.
We will show that $V = \operatorname{null} T_2 \oplus \operatorname{span}(v_1, \dots, v_n)$.
Let $v \in V$. There are $a_1, \dots, a_n \in \mathbb{F}$ such that

$$
\begin{aligned}
T_2 v &= a_1 w_1 + \dots + a_n w_n\\\\
&= a_1 T_2 v_1 + \dots + a_n T_2 v_n\\\\
&= T_2 (a_1 v_1 + \dots + a_n v_n)\\\\
\end{aligned}
$$

Then

$$
T_2(v - (a_1 v_1 + \dots + a_n v_n)) = T_2 v - T_2 (a_1 v_1 + \dots + a_n v_n) = T_2 v - T_2 v = 0
$$

Thus, $v - (a_1 v_1 + \dots + a_n v_n) \in \operatorname{null} T_2$.
We can write trivially correct statement $v = (v - (a_1 v_1 + \dots + a_n v_n)) + (a_1 v_1 + \dots + a_n v_n)$.
Hence, $v \in \operatorname{null} T_2 \oplus \operatorname{span}(v_1, \dots, v_n)$ and $V \subset \operatorname{null} T_2 \oplus \operatorname{span}(v_1, \dots, v_n)$.

Clearly, $\operatorname{null} T_2 \oplus \operatorname{span}(v_1, \dots, v_n) \subset V$, therefore $V = \operatorname{null} T_2 \oplus \operatorname{span}(v_1, \dots, v_n)$.

Define $S \in \mathcal{L}(\operatorname{range} T_2, W)$ by

$$
Sw_j = T_1 v_j, \text{ for } j = 1, \dots, n
$$

Because $\operatorname{null} T_1 \oplus \operatorname{span}(v_1, \dots, v_n)$ is also a direct sum, it follows that $T_1 v_1, \dots, T_1 v_n$ is linearly independent.
Thus, $S$ is injective.
Let $v \in V$.
There is $u \in \operatorname{null} T_1$ and $a_1, \dots, a_n \in F$ such that

$$
v = u + a_1 v_1 + \dots + a_n v_n
$$

Thus

$$
\begin{aligned}
T_1 v &= T_1 (u + a_1 v_1 + \dots + a_n v_n)\\\\
&= a_1 T_1 v_1 + \dots + a_n T_1 v_n\\\\
&= a_1 S w_1 + \dots + a_n S w_n\\\\
&= a_1 S T_2 v_1 + \dots + a_n S T_2 v_n\\\\
&= S T_2 (a_1 v_1 + \dots + a_n v_n)\\\\
&= S T_2 u + S T_2 (a_1 v_1 + \dots + a_n v_n)\\\\
&= S T_2 v\\\\
\end{aligned}
$$

Hence, $T_1 = S T_2$, as desired.

Conversely, suppose $S$ is an invertible operator on $W$ such that $T_1 = ST_2$.

Let $v \in \operatorname{null} T_1$.
Then

$$
0 = T_1 v = ST_2 v
$$

Because $S$ is invertible, it follows that $T_2 v = 0$.
Hence, $v \in \operatorname{null} T_2$.

For the inclusion in the other direction, let $v \in \operatorname{null} T_2$.
We have

$$
0 = ST_2 v = T_1 v
$$

Hence, $v \in \operatorname{null} T_1$ and, therefore $\operatorname{null} T_1 = \operatorname{null} T_2$.

_Exercise 5_

Suppose $\operatorname{range} T_1 = \operatorname{range} T_2$.
Let $u_1, \dots, u_n$ be a basis of $\operatorname{null} T_1$ and extend it to a basis $u_1, \dots, u_n, v_1, \dots, v_m$ of $V$.
By the same reasoning used in the proof of 3.22, it follows that $T_1 v_1, \dots, T_1 v_m$ is a basis of $\operatorname{range} T_1$.
Let $\nu_1, \dots, \nu_m \in V$ be an inverse image of this last basis when $T_2$ is applied and $\mu_1, \dots, \mu_n$ a basis of $\operatorname{null} T_2$.
Since $T_2 \nu_1, \dots, T_2 \nu_m$ is linearly independent, we have that $\operatorname{span}(\nu_1, \dots, \nu_m) \cap \operatorname{null} T_2 = \\{0\\}$.
Therefore, $\nu_1, \dots, \nu_m, \mu_1, \dots, \mu_n$ is a basis of $V$ and, because of this, the following linear map is invertible.

Define $S \in \mathcal{L}(V)$ by

$$
\begin{aligned}
Su_j &= \mu_j, \text{ for } j = 1, \dots, n\\\\
Sv_j &= \nu_j, \text{ for } j = 1, \dots, m\\\\
\end{aligned}
$$

Let $v \in V$.
There are $a_1, \dots, a_n, c_1, \dots, c_m \in \mathbb{F}$ such that

$$
v = a_1 u_1 + \dots + a_n u_n + c_1 v_1 + \dots + c_m v_m
$$

Then

$$
\begin{aligned}
T_1 v &= T_1 (a_1 u_1 + \dots + a_n u_n + c_1 v_1 + \dots + c_m v_m)\\\\
&= c_1 T_1 v_1 + \dots + c_m T_1 v_m\\\\
&= c_1 T_2 \nu_1 + \dots + c_m T_2 \nu_m\\\\
&= c_1 T_2 S v_1 + \dots + c_m T_2 S v_m\\\\
&= T_2 S (c_1 v_1 + \dots + c_m v_m)\\\\
&= T_2 (a_1 \mu_1 + \dots + a_n \mu_n) + T_2 S (c_1 v_1 + \dots + c_m v_m)\\\\
&= T_2 S (a_1 u_1 + \dots + a_m u_m) + T_2 S (c_1 v_1 + \dots + c_m v_m)\\\\
&= T_2 S v\\\\
\end{aligned}
$$

Hence, $T_1 = T_2 S$.

For the implication in the other direction, suppose $S \in \mathcal{L}(V)$ is an invertible operator such that $T_1 = T_2 S$.

Clearly $\operatorname{range} T_1 \subset \operatorname{range} T_2$.

Let $w \in \operatorname{range} T_2$ and $v \in V$ such that $T_2 v = w$.
Since $S$ is invertible, there is $\nu \in V$ such that $S\nu = v$.
Thus

$$
w = T_2 v = T_2 S \nu = T_1 \nu
$$

Hence $w \in \operatorname{range} T_1$ and therefore $\operatorname{range} T_2 \subset \operatorname{range} T_1$, implying $\operatorname{range} T_1 = \operatorname{range} T_2$, as desired.

_Exercise 6_

Suppose there are $R \in \mathcal{L}(V)$ and $S \in \mathcal{L}(W)$ such that $T_1 = S T_2 R$.
Then

$$
\begin{aligned}
\operatorname{dim} \operatorname{null} T_1 &= \operatorname{dim} \operatorname{null} T_2 R\\\\
&\le \operatorname{dim} \operatorname{null} T_2 + \operatorname{dim} \operatorname{null} R\\\\
&= \operatorname{dim} \operatorname{null} T_2\\\\
\end{aligned}
$$

Where the first equation follows from _Exercise 4_, the second from _Exercise 22_ in 3B and the third because $R$ is invertible.
Hence $\operatorname{dim} \operatorname{null} T_1 \le \operatorname{null} T_2$.
We also have

$$
\begin{aligned}
\operatorname{dim} \operatorname{range} T_1 &= \operatorname{dim} \operatorname{range} S T_2\\\\
&\ge \operatorname{dim} \operatorname{range} T_2\\\\
\end{aligned}
$$

Where the first equation follows from _Exercise 5_ and the second from _Exercise 23_ in 3B and because $\operatorname{dim} \operatorname{range} S = \operatorname{dim} W \ge \operatorname{dim} \operatorname{range} T_2$.
Thus

$$
\begin{aligned}
\operatorname{dim} \operatorname{null} T_1 &= \operatorname{dim} V - \operatorname{dim} \operatorname{range} T_1\\\\
&= \operatorname{dim} \operatorname{null} T_2 + \operatorname{dim} \operatorname{range} T_2 - \operatorname{dim} \operatorname{range} T_1\\\\
&\ge \operatorname{dim} \operatorname{null} T_2 + \operatorname{dim} \operatorname{range} T_1 - \operatorname{dim} \operatorname{range} T_1\\\\
&= \operatorname{dim} \operatorname{null} T_2\\\\
\end{aligned}
$$

Hence, $\operatorname{dim} \operatorname{null} T_1 \ge \operatorname{dim} \operatorname{null} T_2$.
Therefore, $\operatorname{dim} \operatorname{null} T_1 = \operatorname{dim} \operatorname{null} T_2$.

Conversely, suppose $\operatorname{dim} \operatorname{null} T_1 = \operatorname{dim} \operatorname{null} T_2$.
Let $u_1, \dots, u_n$ and $\mu_1, \dots, \mu_n$ be bases of $\operatorname{null} T_1$ and $\operatorname{null} T_2$, respectively.
Extend them to the bases $u_1, \dots, u_n, v_1, \dots, v_m$ and $\mu_1, \dots, \mu_n, \nu_1, \dots, \nu_m$ of $V$.
By the same reasoning used in the proof of 3.22, we have that $T_1 v_1, \dots, T_1 v_m$ and $T_2 \nu_1, \dots, T_2 \nu_m$ are bases of $\operatorname{range} T_1$ and $\operatorname{range} T_2$, respectively.

Define $R \in \mathcal{L}(V)$ by

$$
\begin{aligned}
Ru_j = \mu_j, \text{ for } j = 1, \dots, n\\\\
Rv_j = \nu_j, \text{ for } j = 1, \dots, m\\\\
\end{aligned}
$$

And $S \in \mathcal{L}(\operatorname{range} T_2 R, W)$ by

$$
\begin{aligned}
ST_2 \nu_j = T_1 v_j, \text{ for } j = 1, \dots, m
\end{aligned}
$$

It easy show that $T_1 = S T_2 R$ (it is almost the same as in the proof of _Exercise 4_ and _5_) and that $S$ injective.
By _Exercise 3_, there is an invertible operator on $W$ that satisfies the same property as $S$, which completes the proof.

_Exercise 7_

_(a)_
Let $S, T \in E$.
Then

$$
0 = Sv + Tv = (S + T)v
$$

Hence, $E$ is closed under addition.
Similarly, $E$ is closed under scalar multiplication.
Therefore, $E$ is indeed a subspace of $\mathcal{L}(V, W)$

_(b)_
Let $U$ be a subspace of $V$ such that $V = U \oplus \operatorname{span}(v)$ and let $u_1, \dots, u_n$ be a basis of $U$.
We will show that $E$ and $\mathcal{L}(U, W)$ are isomorphic.

Define $\Lambda \in \mathcal{L}(E, \mathcal{L}(U, W))$ by

$$
\Lambda(T) = T \lvert_U
$$

To prove $\Lambda$ is injective, let $S, T \in E$ such that $\Lambda(S) = \Lambda(T)$.
Let $u \in V$.
There are scalars $a_1, \dots, a_n, a \in \mathbb{F}$ such that

$$
u = a_1 u_1 + \dots + a_n u_n + a v
$$

Then

$$
\begin{aligned}
Tu &= T(a_1 u_1 + \dots + a_n u_n + a v)\\\\
&= a_1 T u_1 + \dots + a_n T u_n + a T v\\\\
&= a_1 T u_1 + \dots + a_n T u_n\\\\
&= a_1 T\lvert_U u_1 + \dots + a_n T\lvert_U u_n\\\\
&= a_1 S\lvert_U u_1 + \dots + a_n S\lvert_U u_n\\\\
&= a_1 S u_1 + \dots + a_n S u_n\\\\
&= S(a_1 u_1 + \dots + a_n u_n) + S(av)\\\\
&= S(u)\\\\
\end{aligned}
$$

Hence $S = T$.
Therefore $\Lambda$ is injective.

To prove surjectivity, let $T \in L(U, W)$.
Define $S \in L(V, W)$ by

$$
\begin{aligned}
Su_j &= Tu_j, \text{ for } j = 1, \dots, n\\\\
Sv &= 0\\\\
\end{aligned}
$$

We have that $S \in E$, and it is easy to see that $\Lambda(S) = T$.
Hence, $\Lambda$ is surjective, that is, an isomorphism between $E$ and $L(U, W)$.

Therefore, $\operatorname{dim} E = \operatorname{dim} U \operatorname{dim} W = (\operatorname{dim} V - 1) \operatorname{dim} W$.

_Exercise 8_

Let $w_1, \dots, w_n$ be a basis of $W$ and $v_1, \dots, v_n$ an inverse image of this basis when $T$ is applied.
Because $w_1, \dots, w_n$ is linearly independent, it follows that $v_1, \dots, v_n$ is also linearly independent (you can check it).

Define $U$ by

$$
U = span(v_1, \dots, v_n)
$$

It is easy to see that $T\lvert_U$ is both injective and surjective.
Hence, $T\lvert_U$ is an isomorphism of $U$ onto $W$.

_Exercise 9_

Suppose $ST$ is invertible.
Since $ST$ is surjective, it follows that $S$ is also surjective and, thus, invertible.
Let $u,v \in V$ such that $Tv = Tu$. We have that $STv = STu$.
But $ST$ is injective, hence $v = u$, proving $T$ is injective, and thus, invertible.

The converse is the same as _Exercise 1_.

_Exercise 10_

This follows quickly from _Exercise 9_ and because $I$ is invertible.

_Exercise 11_

By _Exercise 9_ and _10_ it follows that $S$, $T$ and $U$ are all invertible.
Multiplying both sides of $STU = I$ from the left by $S^{-1}$ and then from the right by $U^{-1}$ we get $T = S^{-1}U^{-1} = (US)^{-1}$, which implies $T^{-1} = US$.

_Exercise 12_

Suppose $V = \mathcal{P}(\mathbb{R})$ and let $S$ be the integration map (with the constant of integration equal to zero), $T$ the differentiation map and $U$ the identity. $STU = I$ but $T$ is clearly not invertible.

_Exercise 13_

This is the same as _Exercise 11_.

_Exercise 14_

Suppose there are $u, v \in V$ such that $Tv = Tu$. We have that

$$
M(v) = M(u) = \begin{pmatrix}
c_1\\\\
\vdots\\\\
c_n\\\\
\end{pmatrix}
$$

For some $c_1, \dots, c_n \in \mathbb{F}$.
Thus

$$
v = c_1 v_1 + \dots + c_n v_n = u
$$

Hence $T$ is injective.
We have

$$
\begin{aligned}
\operatorname{dim} \mathbb{F}^{n,1} &= \operatorname{dim} V\\\\
&= \operatorname{dim} \operatorname{null} T + \operatorname{dim} \operatorname{range} T\\\\
&= \operatorname{dim} \operatorname{range} T\\\\
\end{aligned}
$$

Hence $T$ is surjective and, therefore, an isomorphism of $V$ onto $\mathcal{F}^{n,1}$

_Exercise 15_

Choose the standard bases to represent $\mathcal{M}(T)$, $\mathcal{M}(Tx)$ and $\mathcal{M}(x)$.
Let $A = \mathcal{M}(T)$.
The rest follows directly from 3.65.

_Exercise 16_

Suppose $T$ is a scalar multiple of the identity.
There exists $c \in \mathbb{F}$ such that $T = cI$.
Let $S \in \mathcal{L}(V)$.
Then, for any $v \in V$, we have

$$
STv = S(cI)v = cSIv = cSv = (cI)Sv = TSv
$$

Hence, $ST = TS$.

Conversely, suppose that $ST = TS$ for any $S \in \mathcal{L}(V)$.
Let $v$ be a non-zero vector in $V$ and $S$ an operator on $V$ such that $v$ is a basis of $\operatorname{null} S$ (it is easy to show a map like this exists).
We have

$$
0 = T(Sv) = S(Tv)
$$

Hence, $Tv \in \operatorname{null} S$. But $\operatorname{null} S = \operatorname{span}(v)$, therefore $Tv = cv$ for some $c \in \mathbb{F}$.
We but need to show that this scalar $c$ is the same for any $v$.

Let $u \in V$ such that $u = av$, where $a \in \mathbb{F}$.
Because $T$ is linear, we have that

$$
Tu = T(av) = aTv = acv = cav = cu
$$

Hence, $c$ is the same for any multiple of $v$.
Let $w \in V$ such that $w$ is not a scalar multiple of $v$, i.e, $v$ and $w$ are linearly independent.
There is a scalar $b$ such that $Tw = bw$ and a scalar $d$ such that

$$
T(v + w) = d(v + w)
$$

But, because $T$ is linear, also

$$
T(v + w) = Tv + Tw = cv + bw
$$

Therefore

$$
0 = T(v + w) - T(v + w) = dv + dw - cv - bw = (d - c)v + (d - b)w
$$

Because $v$ and $w$ are linearly independent, it follows that $c = d = b$.

Hence the scalar is the same for all vectors and $T$ is a scalar multiple of the identity.

_Exercise 17_

Note that if $I \in \mathcal{E}$, then $\mathcal{E} = \mathcal{L}(V)$.
We will prove $I \in \mathcal{E}$ if $\mathcal{E}$ is not $\\{0\\}$.

Suppose $\mathcal{E} \neq \\{0\\}$.
Then there exists non-zero $T \in \mathcal{E}$.
Let $v_1 \in V$ such that $Tv_1 \neq 0$.
Then $v_1$ is also non-zero and we can extend it to a basis $v_1, \dots, v_n$ of $V$.
Define $S_1, \dots, S_n \in \mathcal{L}(V)$ by

$$
S_j v_j = v_1, S_j v_k = 0 \text{ for } k \neq j
$$

and let $R_1, \dots, R_n$ be any operators on $V$ such that

$$
R_j Tv_1 = v_j
$$

for each $j = 1, \dots, n$.
Note that $R_jTS_j \in \mathcal{E}$.
We have

$$
R_jTS_j v_j = R_jTv_1 = v_j
$$

and, for $k \neq j$,

$$
R_jTS_j v_k = R_jT0 = 0.
$$

Thus, $R_1TS_1 + \dots + R_nTS_n$ equals the identity and is in $\mathcal{E}$, since $\mathcal{E}$ is closed under addition.

_Exercise 18_

This follows directly from 3.61.

_Exercise 19_

_(a)_
Let $P = \mathcal{P}_m(\mathbb{R})$ for some positive integer $m$.
Suppose $p \in P$.
We have $m \ge \deg p \ge \deg Tp$.
Therefore, $Tp \in P$.
$T$ restricted to $P$ is an operator on $P$ and, since $T$ is injective, $T$ restricted to $P$ is also injective and, thus, surjective.
This means that $T$ maps to every polynomial with degree less or equal than $m$.
Because $m$ was arbitrary, it follows that $T$ is surjective.

_(b)_
Suppose there exists $p \in \mathcal{P}_m(\mathbb{R})$ such that $\deg p = m$ and $\deg Tp < \deg p$.
Let $n = \deg Tp$.
$T$ restricted to $\mathcal{P}_n(\mathbb{R})$ is surjective, hence there exists $q \in \mathcal{P}_n(\mathbb{R})$ such that $Tq = Tp$.
Since $m > n$, it follows that $p - q \neq 0$, but

$$
T(p - q) = Tp - Tq = Tp - Tp = 0
$$

Which is a contradiction to the fact that $T$ is injective, therefore we cannot have $\deg Tp < \deg p$.

_Exercise 20_

Let $v_k = \left(A_{1,k}, \dots, A_{n, k}\right)$, for $k = 1, \dots, n$.

Suppose (a) holds.
Then (a) implies that $v_1, \dots, v_n$ is linearly independent.
Since this list has length $\operatorname{dim} \mathbb{F}^n$, it must also span $\mathbb{F}^n$, proving (b).

Suppose (b) holds.
Then (b) implies that $v_1, \dots, v_n$ spans $\mathbb{F}^n$.
Moreover, this list has length $\operatorname{dim} \mathbb{F}^n$, therefore it is linearly independent, proving (a).

