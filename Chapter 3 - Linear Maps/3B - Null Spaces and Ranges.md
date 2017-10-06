Chapter 3: **Linear Maps**

**3.B**

- [ ] Exercise 1
- [ ] Exercise 2
- [ ] Exercise 3
- [ ] Exercise 4
- [ ] Exercise 5
- [ ] Exercise 6
- [ ] Exercise 7
- [ ] Exercise 8
- [ ] Exercise 9
- [ ] Exercise 10
- [x] Exercise 11
- [x] Exercise 12
- [ ] Exercise 13
- [ ] Exercise 14
- [ ] Exercise 15
- [x] Exercise 16
- [ ] Exercise 17
- [ ] Exercise 18
- [ ] Exercise 19
- [ ] Exercise 20
- [x] Exercise 21
- [x] Exercise 22
- [x] Exercise 23
- [x] Exercise 24
- [x] Exercise 25
- [x] Exercise 26
- [ ] Exercise 27
- [x] Exercise 28
- [x] Exercise 29
- [ ] Exercise 30
- [x] Exercise 31

_Exercise 11_

We will give a proof by induction.

Clearly, the hypothesis is true when $n = 1$.  Assume it is true for $n$.

Let $v$ and $v'$ be two vectors in the domain of $S_{n+1}$ such that $S_1 S_2 \dots S_{n+1} v = S_1 S_2 \dots S_{n+1} v$.
By induction, it follows that $S_1 S_2 \dots S_n$ is injective and, hence, $S_{n+1} v = S_{n+1} v'$.
Since $S_{n+1}$ is also injective, we have that $v = v'$, completing the proof.

_Exercise 12_

Use the notation from 3.22 and define $U = \operatorname{span}(v_1, \dots, v_n)$.

_Exercise 16_

We will prove the contrapositive.

Suppose $V$ is infinite-dimensional and $T$ is a linear map on $V$.
Assume that $\operatorname{null} T$ is finite-dimensional.
We need to show that $\operatorname{range} T$ is infinite-dimensional.

Let $v_1, \dots, v_n$ be a basis of $\operatorname{null} T$.
Because $V$ is infinite-dimensional, we can extend this list to a linearly independent list $v_1, \dots, v_n, \dots, v_m$ of any length $m$.
By the same reasoning used in 3.22, it follows that $Tv_{n+1}, \dots, Tv_m$ is a linearly independent list in $\operatorname{range} T$.
Since $m$ was arbitrary, by _Exercise 14_ in 2.A, we have that $\operatorname{range} T$ infinite-dimensional.

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

Conversely, suppose $TS$ is the identity map on $W$. Let $w \in W$, we have $TSw = w$. Since $Sw \in V$, it follows that there is a vector in $V$ that $T$ maps to $W$. Since $w$ was arbitrary, we have that $T$ is surjective.

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

Because $\operatorname{range} ST \subset \operatorname{range} S$, it follows that $\operatorname{dim} \operatorname{range} ST \le \operatorname{dim} \operatorname{range} S$.
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

_Exercise 26_

Let $T: P_m(R) \to P_{m-1}(R)$ such that $Tp = Dp$.
Suppose $p \in \operatorname{null} T$.
Since $T$ reduces the degree of every nonconstant polynomial by $1$ and $\deg 0 = -\infty$, it follows that $p$ can only be constant. Hence $\operatorname{dim} \operatorname{null} T = 1$. By the Fundamental Theorem of Linear Maps $T$ is surjective. Because $m$ was arbitrary, so is $D$.

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
Hence $v - \lambda u \in \operatorname{null} \varphi$ and $\lambda u \in \\{au: a \in \mathbb{F}\\}$.
But $v = (v - \lambda u) + \lambda u$, therefore $v \in \operatorname{null} \varphi + \\{au: a \in \mathbb{F}\\}$, proving the inclusion in one direction.
The inclusion in the opposite direction is clearly true.
Thus $V = \operatorname{null} \varphi + \\{au: a \in \mathbb{F}\\}$.
Since $\varphi(u) \neq 0$, it follows that $\varphi(\lambda  u) = 0$ if and only $\lambda = 0$. Therefore $\operatorname{null} \varphi \cap \\{au: a \in \mathbb{F}\\} = \\{0\\}$, proving that the sum is a direct one.

_Exercise 31_

Let $v_1,v_2,v_3,v_4,v_5$ be a basis of $\mathbb{R^5}$ and $w_1,w_2$ of $\mathbb{R^2}$. Define $T_1,T_2 \in \mathcal{L}(\mathbb{R^5},\mathbb{R^2})$ such that

$$
\begin{align*}
T_1(a_1 v_1 + \dots + a_5 v_5) &= a_1 w_1 + a_2 w_2\\\\
T_2(a_1 v_1 + \dots + a_5 v_5) &= a_2 w_1 + a_1 w_2
\end{align*}
$$

Clearly $\operatorname{null} T_1 = \operatorname{null} T_2 = \operatorname{span}(v_3,v_4,v_5)$, but $T_1 v_1 = w_1$ and $T_2 v_1 = w_2$. Because $w_1$ is not a scalar multiple of $w_2$ (they are linearly independent), we have that $T_1$ cannot be a scalar multiple $T_2$.
