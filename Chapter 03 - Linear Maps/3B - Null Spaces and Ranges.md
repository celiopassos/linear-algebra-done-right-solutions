Chapter 3: **Linear Maps**

**3.B**

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
- [x] Exercise 21
- [x] Exercise 22
- [x] Exercise 23
- [x] Exercise 24
- [x] Exercise 25
- [x] Exercise 26
- [x] Exercise 27
- [x] Exercise 28
- [x] Exercise 29
- [x] Exercise 30
- [x] Exercise 31

_Exercise 1_

Consider $T = (x_1,..,x_5) \to (x_4, x_5)$. We have $\operatorname{null} T = \{(x_1,x_2,x_3,0,0) | x_1,x_2,x_3 \in \mathbb{F}\}$, and $\operatorname{range} T = \mathbb{F}^2$, so $\operatorname{dim} \operatorname{null} T = 3$ and $\operatorname{dim} \operatorname{range} T = 2$.

_Exercise 2_

Since $\operatorname{range} S \subset \operatorname{null} T$, we have that $\forall v \in V \ Sv \in \operatorname{null} T$. This means that $\forall v \in V \ TSv = 0$. $(ST)^2v = STSTv = S(TS(Tv)) = S0 = 0$, hence $(ST)^2$ maps any vector into 0, so $(ST)^2 = 0$.

_Exercise 3_

(a) $v_1,...,v_m$ span $V$ implies that $T$ is surjective, because then any vector $v \in V$ can be represented as $v = z_1v_1 + ... + z_mv_m$, and this means that $\operatorname{range}T = V$.

(b) $v_1,...,v_m$ being linearly indepenent implies that $T$ is injective: indeed, $z_1v_1 + ... + z_mv_m = 0$ implies $z_1 = ... = z_m = 0$, so $\operatorname{null} T = \{0\}$, and we have proved in 3.16 that injectivity is equivalent to having kernal space equal to $\{0\}$. 

_Exercise 4_

Denote $U = \{T \in \mathcal(\mathbb{R}^5,\mathbb{R}^4) | \operatorname{dim}\operatorname{null}T > 2\}$. Consider $T_1: (x_1,...,x_5) \to (x_1, x_2, 0, 0)$ and $T_2: (x_1,...,x_5) \to (0, 0, x_3, x_4)$. We can easiliy verify that $\operatorname{dim}\operatorname{null} T_1 = \operatorname{dim}\operatorname{null} T_2 = 3$, but $T_1 + T_2$ has $\operatorname{dim}\operatorname{null} T_1 + T_2 = 1$, so this means that $U$ is not closed under addition, so it is not a vector subspace.

_Exercise 5_

For example, $T: (x_1, x_2, x_3, x_4) \to (x_3, x_4, 0, 0)$. This map has $\operatorname{null} T = \operatorname{range} T = \{(x_1, x_2, 0, 0) | x_1, x_2 \in \mathbb{R}\}$.

_Exercise 6_

To show it we can use the fundamental theorem of linear maps, which states that $\operatorname{dim} V = \operatorname{dim} \operatorname{range}V + \operatorname{dim}\operatorname{null} V$. If $\operatorname{null} V = \operatorname{range} V$, then $5 = 2 \operatorname{dim}\operatorname{null} V$. But it is impossible, since 5 is odd and $\operatorname{dim}\operatorname{null} V$ is integer.

_Exercise 7_

Suppose $v_1,...,v_n$ is a basis of $V$ and $w_1,...,w_m$ is a basis of $W$, with $n \le m$. Let us consider $T_1$: 

$$
\begin{align}
T_1v_i &= w_i,\ i = 1..n-1\\
T_1v_i &= 0,\ i = n
\end{align}
$$

and $T_2$:

$$
\begin{align}
T_2v_i &= 0,\ i = 1..n-1\\
T_2v_i &= w_i,\ i = n
\end{align}
$$

Both $T_1$ and $T_2$ are not injective, since $\operatorname{dim}\operatorname{null}T_1 = 1 > 0$ and $\operatorname{dim}\operatorname{null}T_1 = n - 1 > 0$ since $n \ge 2$. However, $T_1 + T_2$ is injective, because $\forall v = a_1v_1 + ... + a_nv_n \in V \implies \ (T_1 + T_2)v = a_1w_1 + ... + a_nw_n \neq 0$ if any of $a_1...a_n$ is non-zero, because $w_1...w_n$ is a basis of $W$. 

_Exercise 8_

Suppose $v_1,...,v_n$ is a basis of $V$ and $w_1,...,w_m$ is a basis of $W$, with $n \ge m$. Let us consider $T_1$: 

$$
\begin{align}
T_1v_i &= w_i,\ i = 1..m-1\\
T_1v_i &= 0,\ i = m...n
\end{align}
$$

and $T_2$: 

$$
\begin{align}
T_2v_i &= 0,\ i \neq m\\
T_2v_i &= w_i,\ i = m
\end{align}
$$

It is clear, that $T_1$ and $T_2$ are not surjective, but $T_1 + T_2$ is surjective, since every element of $W$ basis has prototype in the $V$ domain. 

_Exercise 9_

Let us consider linear combination $c_1(Tv_1) + ... + c_n(Tv_n) = T(c_1v_1 + ... + c_nv_n)$. Since $T$ is injective, $\operatorname{null}T = \{0\}$, so this linear combination is zero if and only if $c_1v_1 + ... + c_nv_n = 0$. This sum, in turn, is zero if and only if $c_1 = ... = c_n = 0$, since $v_1,...,v_n$ are linearly independent.

_Exercise 10_

By the definition of a span, any vector $v \in V$ can be represented as $v = c_1v_1 + ... + c_nv_n$. This means, that any vector $u = Tv \in \operatorname{range} T$ can be represented as $T(c_1v_1 + ... + c_nv_n) = c_1(Tv_1) + ... + c_n(Tv_n)$, from which it follows, that $Tv_1,...,Tv_n$ spans $\operatorname{range}T$.

_Exercise 11_

We will give a proof by induction.

Clearly, the hypothesis is true when $n = 1$.  Assume it is true for $n$.

Let $v$ and $v'$ be two vectors in the domain of $S_{n+1}$ such that $S_1 S_2 \dots S_{n+1} v = S_1 S_2 \dots S_{n+1} v$.
By induction, it follows that $S_1 S_2 \dots S_n$ is injective and, hence, $S_{n+1} v = S_{n+1} v'$.
Since $S_{n+1}$ is also injective, we have that $v = v'$, completing the proof.

_Exercise 12_

Use the notation from 3.22 and define $U = \operatorname{span}(v_1, \dots, v_n)$.

_Exercise 13_

We can see that $(5, 1, 0, 0), (0,0,7,1)$ is a basis of $\operatorname{null}T$, so $\operatorname{dim}\operatorname{null}T = 2$. From the fundamental theorem of linear maps, $\operatorname{dim}\operatorname{range}T = 4 - 2 = 2$, so $\operatorname{dim}\operatorname{range} = \mathbb{R}^2$, which means that $T$ is surjective.

_Exercise 14_

From the fundamental theorem of linear maps $8 = \operatorname{dim}\operatorname{null}T + \operatorname{dim}\operatorname{range}T = 3 + \operatorname{dim}\operatorname{range}T$, so $\operatorname{dim}\operatorname{range}T = 5$, so $\operatorname{dim}\operatorname{range}T = \mathbb{R}^5$, which means that $T$ is surjective. 

_Exercise 15_

Null space of such hypothetical map is $\operatorname{null}T = \{3x_2, x_2, x_3,x_3,x_3\}$. It has 2 dimensions, so $\operatorname{dim}\operatorname{range}T = 3$, but it is impossible, since $\operatorname{dim}\operatorname{range}T \le \operatorname{dim}\operatorname{range} \mathbb{F}^2 = 2$.

_Exercise 16_

We will prove the contrapositive.

Suppose $V$ is infinite-dimensional and $T$ is a linear map on $V$.
Assume that $\operatorname{null} T$ is finite-dimensional.
We need to show that $\operatorname{range} T$ is infinite-dimensional.

Let $v_1, \dots, v_n$ be a basis of $\operatorname{null} T$.
Because $V$ is infinite-dimensional, we can extend this list to a linearly independent list $v_1, \dots, v_n, \dots, v_m$ of any length $m$.
By the same reasoning used in 3.22, it follows that $Tv_{n+1}, \dots, Tv_m$ is a linearly independent list in $\operatorname{range} T$.
Since $m$ was arbitrary, by _Exercise 14_ in 2.A, we have that $\operatorname{range} T$ infinite-dimensional.

_Exercise 17_

$\implies$: Let $\operatorname{dim}V \le \operatorname{dim} W$. Denote $v_1,...,v_n$ as basis of $V$, $w_1,...,w_m$ as basis of $W$, and $n \le m$. Consider linear map $T: Tv_i = w_i \ \forall i=1...n$. Then, if we consider two distinct vectors $v \neq v'$, $v = \sum c_iv_i,\ v' = \sum c'_iv_i$, we have that $Tv \neq Tv'$, because else $0 = T(v - v') = T\sum(c_i - c'_i)v_i = \sum(c_i - c'_i)Tv_i = \sum(c_i - c'_i)w_i$ implies that $c_i - c'_i = 0$, since $w_1,..,w_n$ are linear independent, but this is a contradiction, because $v \neq v'$. This implies that $Tv \neq Tv'$, so $T$ is injective.

$\Leftarrow$: Let $T$ be injective map $V \to W$, we need to prove, that $\operatorname{dim} V \le \operatorname{dim}W$. From the fundamental theorem of linear maps, we know, that $\operatorname{dim} V = \operatorname{dim}\operatorname{null} T + \operatorname{dim}\operatorname{range}T$. Since $T$ is injective, we know, that $\operatorname{null}T = \{0\}$, and so $\operatorname{dim}\operatorname{range}T = \operatorname{dim} V$. But $\operatorname{range}T$ is subspace of $W$, so $\operatorname{dim} W \ge \operatorname{dim}\operatorname{range}T = \operatorname{dim} V$.

_Exercise 18_

$\Rightarrow$: suppose $\operatorname{dim} V \ge \operatorname{dim} W$. Let us denote a basis of V as $v_1,..,v_n$, a basis of $W$ as $w_1,...,w_m$, with $n \le m$. We can build the surjective map setting $Tv_i = w_i ,\ i = 1..m$, and $Tv_i = 0, \ i > m$. We obviously get $\operatorname{range}T = W$, so $T$ is surjective.

$\Leftarrow$: suppose $T$ is surjective, we need to show, that $\operatorname{dim} V \ge \operatorname{dim} W$. Since $T$ is surjective, $\operatorname{range}T = W$, so $\operatorname{dim}\operatorname{range}T = \operatorname{dim}W$. Using the fundamental theorem of linear maps, we have $\operatorname{dim}V = \operatorname{dim}\operatorname{null}T + \operatorname{dim}W$, which implies that $\operatorname{dim}\operatorname{null}T = \operatorname{dim}V - \operatorname{dim}W$. $\operatorname{dim}\operatorname{null}T \ge 0$ by difenition of dimensionality, so $\operatorname{dim}V \ge \operatorname{dim}W$.

_Exercise 19_

By the fundamental theorem of linear maps, $\operatorname{dim}\operatorname{null}T = \operatorname{dim} V - \operatorname{dim} \operatorname{range} T \ge \operatorname{dim} V - \operatorname{dim} W$, because $\operatorname{range} T$ is a subspace of $W$ so its dimensionalty is not greater than that of containing finite-dimensional space.

So, if $U = \operatorname{null} T$, we get that $\operatorname{dim} U \ge \operatorname{dim} V -\operatorname{dim} W$.

Now, suppose $\operatorname{dim} U \ge \operatorname{dim} V -\operatorname{dim} W$. Let us denote $u_1,...,u_k$ to be a basis of $U$, and let us denote $w_1,...,w_m$ to be a basis of $W$. We know, that $k \ge \operatorname{dim} V - m$. Let us extend basis of $U$ to a basis of $V$ by adding vectors $v_{1},...,v_r$. The previous statement implies $k \ge k + r - m$, and so $r \le m$. We can build the map $T$ in the following way: $Tu_i = 0\ \forall i = 1..k$, and $Tv_i = w_i\ \forall i = 1..r$. This map obviously has $U \subset \operatorname{null}T$, and for every $v \in V \backslash U$ $Tv = \sum c_iTv_i = \sum\limits_{i=1}^r c_i w_i \neq 0$ if not all $c_i=0$, because $\{w_1,...,w_r\}$ are linear independent as basis vectors, so $\operatorname{null}T \subset U$, and hence $\operatorname{null}T = U$.

_Exercise 20_

$\Rightarrow$: Suppose $T$ is injective. Consider $\operatorname{range}T \subset W$: we have that $\forall w \in \operatorname{range}T \ \exist! v \in V:\ Tv = w$. Denote a basis of $\operatorname{range}T$ as $w_1,...,w_k$, and extend it to the basis of $W$ with $w_{k+1},...,w_m$. We will define linear map $S: W \to V$ in the following way:

$$
\begin{align}
Sw_i &= v_i \text{ if } i \le k \text{ and }\ v:  Tv_i = w_i\\
Sw_i &= 0 \text{ if } i > k
\end{align}
$$

For arbitrary vector $w = \sum\limits_{i=1}^m c_iw_i \in W$ we define $Sw = \sum\limits_{i=1}^m c_iSw_i = \sum\limits_{i=1}^k c_iv_i$. It is obvious that $S0 = 0$, so $S$ is in fact a linear map.

Let us prove, that $ST$ is an identity map: consider arbitrary vector $v \in V$, and suppose $Tv = w = \sum\limits_{i=1}^k c_iw_i$.

Denote $u = STv = S\sum\limits_{i=1}^k c_iw_i = \sum\limits_{i=1}^k c_iSw_i = \sum\limits_{i=1}^k c_iv_i$.

Let us now apply $T$ to $u$: $Tu = T\sum\limits_{i=1}^k c_iv_i = \sum\limits_{i=1}^k c_iTv_i = \sum\limits_{i=1}^k c_iw_i = Tv$. Since $T$ is injective, this implies, that $u = v$, so $ST$ in fact maps $v \to v$, so it is identity map on $V$.

$\Leftarrow$: suppose now that $ST$ is identity map. Consider any two vectors $v,v' \in V$, and suppose further that $Tv = Tv'$. Then, $STv = v$ and $STv = S(Tv') = STv' = v'$, which implies $v = v'$, and this means that $T$ is injective.

_Exercise 21_

Suppose $T$ is surjective. Let $w_1,\dots,w_m$ be a basis of $W$. There are $v_1,\dots,v_m \in V$ such that

$$
Tv_j = w_j, \text{ for } j = 1,\dots,m
$$

Define $S \in \mathcal{L}(W, V)$ by

$$
Sw_j = v_j, \text{ for } j = 1,\dots,m
$$

Now suppose $w \in W$. We have

$$
w = a_1 w_1 + \dots + a_m w_m
$$

For some scalars $a_1,\dots,a_m$. Therefore

$$
\begin{aligned}
TSw &= TS(a_1 w_1 + \dots + a_m w_m)\\\\
&= a_1 TSw_1 + \dots + a_m TSw_m\\\\
&= a_1 Tv_1 + \dots + a_m Tv_m\\\\
&= a_1 w_1 + \dots + a_m w_m\\\\
&= w
\end{aligned}
$$

Thus $TS$ is the identity map on $W$.

Conversely, suppose $TS$ is the identity map on $W$. Let $w \in W$, we have $TSw = w$. Since $Sw \in V$, it follows that there is a vector in $V$ that $T$ maps to $w$. Since $w$ was arbitrary, we have that $T$ is surjective.

_Exercise 22_

By the Fundamental Theorem of Linear Maps, we have

$$
\begin{aligned}
\operatorname{dim}\operatorname{null}ST &= \operatorname{dim}U - \operatorname{dim}\operatorname{range}ST\\\\
&= \operatorname{dim}\operatorname{null}T + \operatorname{dim} \operatorname{range}T - \operatorname{dim}\operatorname{range}ST\\\\
&\le \operatorname{dim}\operatorname{null}T + \operatorname{dim}V - \operatorname{dim}\operatorname{range}ST\\\\
&= \operatorname{dim}\operatorname{null}T + \operatorname{dim}V - \operatorname{dim}\operatorname{range}S + \operatorname{dim}\operatorname{range}S - \operatorname{dim}\operatorname{range}ST\\\\
&= \operatorname{dim}\operatorname{null}T + \operatorname{dim}\operatorname{null}S + \operatorname{dim}\operatorname{range}S - \operatorname{dim}\operatorname{range}ST
\end{aligned}
$$

Where the third line follows because $\operatorname{range}T \subseteq V$. We need only to prove that $\operatorname{dim}\operatorname{range}S \ge \operatorname{dim}\operatorname{range}ST$. Suppose that $w \in \operatorname{range}ST$. Then there exists $u \in U$ such that $STu = w$. Since $Tu \in V$, it follows that for every vector $w \in \operatorname{range}ST$ there is another vector in $V$ that $S$ maps to $w$. Therefore $\operatorname{range}ST \subseteq \operatorname{range}S$, which implies $\operatorname{dim}\operatorname{range}S \ge \operatorname{dim}\operatorname{range}ST$.

_Exercise 23_

Consider $w \in \operatorname{range}ST$. This means, that $\exist u \in U, v \in V$ such that $Sv = w$ and $Tu = v$. The first equation implies that $w \in \operatorname{range}S$, so $\operatorname{range}ST \subset \operatorname{range}S$. Because $\operatorname{range} ST \subset \operatorname{range} S$, it follows that $\operatorname{dim} \operatorname{range} ST \le \operatorname{dim} \operatorname{range} S$.

Let $v_1, \dots, v_n$ be a basis of $\operatorname{range} T$.
It is easy to see that $\operatorname{range} ST = \operatorname{span}(Sv_1, \dots, Sv_n)$.
Hence

$$
\operatorname{dim} \operatorname{range} ST = \operatorname{dim} \operatorname{span}(Sv_1, \dots, Sv_n) \le n = \operatorname{dim} \operatorname{range} T
$$

_Exercise 24_

Suppose $\operatorname{null} T_1 \subset \operatorname{null} T_2$.
Let $w_1, \dots, w_n$ be a basis of $\operatorname{range} T_1$ and $v_1, \dots, v_n \in V$ an inverse image of this basis when $T_1$ is applied.
We will prove that $V = \operatorname{null} T_1 + \operatorname{span}(v_1, \dots, v_n)$.

Suppose $v \in V$.
There are $a_1, \dots, a_n \in \mathbb{F}$ such that

$$
\begin{aligned}
T_1 v &= a_1 w_1 + \dots + a_n w_n\\\\
&= a_1 T_1 v_1 + \dots + a_n T_1 v_n\\\\
&= T_1 (a_1 v_1 + \dots + a_n v_n)\\\\
\end{aligned}
$$

Let $\nu = a_1 v_1 + \dots + a_n v_n$.
We have that $0 = T_1 v - T_1 \nu = T_1(v - \nu)$.
Hence $v - \nu \in \operatorname{null} T_1$.
But $v = (v - \nu) + \nu$, therefore $v \in \operatorname{null} T_1 + \operatorname{span}(v_1, \dots, v_n)$, implying $V \subset \operatorname{null} T_1 + \operatorname{span}(v_1, \dots, v_n)$.
The inclusion in the other direction is clearly true, hence $V = \operatorname{null} T_1 + \operatorname{span}(v_1, \dots, v_n)$.

Let $S \in \mathcal{L}(W, W)$ be any linear map such that

$$
Sw_j = T_2 v_j, \text{ for } j = 1, \dots, n
$$

Let $v \in V$.
There are $u \in \operatorname{null} T_1$ and $c_1, \dots, c_n \in F$ such that

$$
v = c_1 v_1 + \dots + c_n v_n + u
$$

Thus

$$
\begin{aligned}
T_2 v &= T_2 (c_1 v_1 + \dots + c_n v_n + u)\\\\
&= c_1 T_2 v_1 + \dots + c_n T_2 v_n + T_2 u\\\\
&= c_1 T_2 v_1 + \dots + c_n T_2 v_n\\\\
&= c_1 S w_1 + \dots + c_n S w_n\\\\
&= c_1 S T_1 v_1 + \dots + c_n S T_1 v_n\\\\
&= S T_1 (c_1 v_1 + \dots + c_n v_n)\\\\
&= S T_1 (c_1 v_1 + \dots + c_n v_n) + S T_1 u\\\\
&= S T_1 v\\\\
\end{aligned}
$$

Hence $T_2 = S T_1$, as desired.

Conversely, suppose $T_2 = ST_1$.
Let $u \in \operatorname{null} T_1$.
Then

$$
0 = S(0) = ST_1 u = T_2 u
$$

Hence $u \in \operatorname{null} T_2$, as desired.

_Exercise 25_

Let $T = T_1$ and consider the same notatition from 3.22.

Suppose $\operatorname{range} T_1 \subset \operatorname{range} T_2$.
Let $\nu_1, \dots, \nu_n \in V$ be an inverse image of $T_1 v_1, \dots, T_1 v_n$ when $T_2$ is applied (this inverse image exists because of the initial assumption).
Define $S \in \mathcal{L}(V, V)$ by

$$
\begin{aligned}
Su_j &= 0, \text{ for } j = 1, \dots, m\\\\
Sv_j &= \nu_j, \text{ for } j = 1, \dots, n\\\\
\end{aligned}
$$

Then

$$
\begin{aligned}
T_1 v &= T_1(a_1 u_1 + \dots + a_m u_m + b_1 v_1 + \dots b_n v_n)\\\\
&= b_1 T_1 v_1 + \dots + b_n T_1 v_n\\\\
&= b_1 T_2 \nu_1 + \dots + b_n T_2 \nu_n\\\\
&= b_1 T_2 Sv_1 + \dots + b_n T_2 Sv_n\\\\
&= T_2S(b_1 v_1 + \dots + b_n v_n)\\\\
&= T_2S(a_1 u_1 + \dots + a_m u_m) + T_2S(b_1 v_1 + \dots + b_n v_n)\\\\
&= T_2Sv\\\\
\end{aligned}
$$

Hence $T_1 = T_2S$.

Conversely, suppose $T_1 = T_2S$.
Let $w \in \operatorname{range} T_1$.
There exists $v \in V$ such that $T_1v = w$.
But $T_2Sv = T_1v = w$ and, because $Sv \in V$, it follows that $w \in \operatorname{range} T_2$, completing the proof.

Alternative proof for $\Rightarrow$:

Suppose $\operatorname{range}T_1 \subset \operatorname{range}T_2$. Denote $w_1,...,w_k$ to be a basis of $\operatorname{range}T_1$, and $v_1,...,v_k$ to be inverse $T_1$ image of the basis, and $\nu_1,...,\nu_k$ to be inverse $T_2$ image of the same basis. 

It is easy to show, that $v_1,...,v_n$ are linearly independent in V. Indeed, let us consider $\sum\limits_{i=1}^kc_iv_i = 0$. After applying $T_1$ to both parts, we get $\sum\limits_{i=1}^kc_iT_1v_i = \sum\limits_{i=1}^kc_iw_i = 0$, and it is possible only if $c_i = 0 \ \forall i$, which finishes the proof.

Since $v_1,...,v_k$ are independent, we can extend them to basis of $V$ with $v_{k+1},...,v_m$.

We also know, that since $w_1...w_k$ is a basis of $\operatorname{range}T_1$, we can represent $T_1v_j = \sum\limits_{i=1}^kc_{ji}w_i$ $\forall j = k+1...m$.

We define $S$ as follows:

$$
\begin{align}
Sv_j := \begin{cases}
\nu_j & \text{ if } j \le k\\
\sum\limits_{i=1}^kc_{ji}\nu_i & \text{ if } j > k\\
\end{cases}
\end{align}
$$

Now, consider arbitrary $v \in V$: $v = \sum\limits_{j=1}^ma_jv_j$, and let us apply $T_2S$ to it:

$$
\begin{align}
T_2Sv &= T_2S(\sum\limits_{j=1}^ka_jv_j + \sum\limits_{j=k+1}^ma_jv_j) \\
&= \sum\limits_{j=1}^ka_jT_2Sv_j + \sum\limits_{j=k+1}^ma_jT_2Sv_j \\
&= \sum\limits_{j=1}^ka_jT_2\nu_j + \sum\limits_{j=k+1}^ma_jT_2\sum\limits_{i=1}^kc_{ji}\nu_i \\
&= \sum\limits_{j=1}^ka_jw_j + \sum\limits_{j=k+1}^ma_j\sum\limits_{i=1}^kc_{ji}w_i \\
&= \sum\limits_{j=1}^ka_jT_1v_j + \sum\limits_{j=k+1}^ma_jT_1v_j \\
&= T_1\sum\limits_{j=1}^ma_jv_j \\
&= T_1 v
\end{align}
$$

_Exercise 26_

Let $T: P_m(R) \to P_{m-1}(R)$ such that $Tp = Dp$.
Suppose $p \in \operatorname{null} T$.
Since $T$ reduces the degree of every nonconstant polynomial by $1$ and $\deg 0 = -\infty$, it follows that $p$ can only be constant. Hence $\operatorname{dim} \operatorname{null} T = 1$. By the Fundamental Theorem of Linear Maps $T$ is surjective. Because $m$ was arbitrary, so is $D$.

_Exercise 27_

Consider linear map $D: P(\mathbb R) \mapsto P(\mathbb R): Dq = 5q'' + 3q'$. It is clear, that for every $d \in \mathbb{R}$ there is $p \in \operatorname{range}D:\ \operatorname{deg}p = d$. But we know, that any set of polynoms with degrees from 0 to $d$ spans $P_d(\mathbb{R})$, so $P_d(\mathbb{R}) \subset \operatorname{range}D$
. Since $d$ is arbitrary, we conclude that $P(\mathbb{R}) \subset \operatorname{range}D$, but at the same time $\operatorname{range}D \subset P(\mathbb{R})$, which means that $\operatorname{range}D = P(\mathbb{R})$, so $D$ is surjective.

_Exercise 28_

Define $S_j \in \mathcal{L}(\operatorname{range}T, \mathbb{F})$ such that $S_j(w_j) = 1$ and $S_j(w_k) = 0$ for $k \neq j$. $S_j$ is well defined by 3.5 and we have that

$$
S_j(c_1 w_1 + \dots + c_m w_m) = c_j
$$

Now define $\varphi_j = S_j T$, for $j = 1,\dots,m$. Note that $\varphi_j$ is also linear, since it is the product of linear maps. Thus

$$
\begin{align*}
Tv &= a_1 w_1 + \dots + a_m w_m\\\\
&= (S_1 Tv) w_1 + \dots + (S_m Tv) w_m\\\\
&= \varphi_1(v) w_1 + \dots + \varphi_m(v) w_m
\end{align*}
$$

_Exercise 29_

Suppose $v \in V$.
Since $\operatorname{dim} \operatorname{range} \varphi = 1$, it follows that $\varphi(u)$ is a basis of $\operatorname{range} \varphi$.
There exists $\lambda \in \mathbb{F}$ such that $\varphi(v) = \lambda \varphi(u)$, which implies $\varphi(v - \lambda u) = 0$.
Hence $v - \lambda u \in \operatorname{null} \varphi$ and $\lambda u \in \{au: a \in \mathbb{F}\}$.
But $v = (v - \lambda u) + \lambda u$, therefore $v \in \operatorname{null} \varphi + \{au: a \in \mathbb{F}\}$, proving the inclusion in one direction.
The inclusion in the opposite direction is clearly true.
Thus $V = \operatorname{null} \varphi + \{au: a \in \mathbb{F}\}$.
Since $\varphi(u) \neq 0$, it follows that $\varphi(\lambda  u) = 0$ if and only $\lambda = 0$. Therefore $\operatorname{null} \varphi \cap \{au: a \in \mathbb{F}\} = \{0\}$, proving that the sum is a direct one.

_Exercise 30_

Since $\operatorname{range}\varphi_1 \subset F$, we know that $\operatorname{dim}\operatorname{range}\varphi_1 \le \operatorname{dim}\mathbb{F} = 1$, and $\operatorname{dim}\operatorname{range}\varphi_1 = \operatorname{dim}\operatorname{range}\varphi_2$. If $\operatorname{dim}\operatorname{range}\varphi_1 = 0$, then $\varphi_1 = \varphi_2 = \mathbb{0}$, so $\varphi_1 = 1 \cdot \varphi_2$.

If $\operatorname{dim}\operatorname{range}\varphi_1 = 1$, then $\operatorname{range}\varphi_1 = \mathbb{F}$, so there exists $v \in V: \ \varphi_1 v = 1$. Denote $\varphi_2 v = \lambda$. 

We now can represent $V = \{v\} \bigoplus \operatorname{null}\varphi_1$, and so for any $u \in V \implies u = \alpha v + \beta w$, where $w \in \operatorname{null}\varphi_1$, and $\varphi_1 u = \alpha$, $\varphi_2 u = \alpha \lambda$, so $\varphi_2 u = \lambda \varphi_1u \implies \varphi_2 = \lambda \varphi_1$ because $u$ was arbitrary. 

_Exercise 31_

Let $v_1,v_2,v_3,v_4,v_5$ be a basis of $\mathbb{R^5}$ and $w_1,w_2$ of $\mathbb{R^2}$. Define $T_1,T_2 \in \mathcal{L}(\mathbb{R^5},\mathbb{R^2})$ such that

$$
\begin{align*}
T_1(a_1 v_1 + \dots + a_5 v_5) &= a_1 w_1 + a_2 w_2\\\\
T_2(a_1 v_1 + \dots + a_5 v_5) &= a_2 w_1 + a_1 w_2
\end{align*}
$$

Clearly $\operatorname{null} T_1 = \operatorname{null} T_2 = \operatorname{span}(v_3,v_4,v_5)$, but $T_1 v_1 = w_1$ and $T_2 v_1 = w_2$. Because $w_1$ is not a scalar multiple of $w_2$ (they are linearly independent), we have that $T_1$ cannot be a scalar multiple $T_2$.
