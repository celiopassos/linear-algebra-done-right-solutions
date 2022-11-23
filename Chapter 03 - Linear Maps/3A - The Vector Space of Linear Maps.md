Chapter 3: **Linear Maps**

**3.A**

- [ ] Exercise 1
- [ ] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [ ] Exercise 5
- [ ] Exercise 6
- [ ] Exercise 7
- [x] Exercise 8
- [x] Exercise 9
- [x] Exercise 10
- [x] Exercise 11
- [x] Exercise 12
- [x] Exercise 13
- [x] Exercise 14

_Exercise 3_

Let us denote $u_1,...,u_n$ to be canonical basis of $\mathbb{F}^n$, i.e. $u_1 = (1,0,...,0)$, ..., $u_n = (0,0,...,1)$. We can define $T$ fully by defining its effect on this basis: 

$$
\begin{align}
T(u_1) &= (A_{11},A_{21}...,A_{m1})\\
T(u_2) &= (A_{12},A_{22}...,A_{m2})\\
\ldots & \\
T(u_n) &= (A_{1n},A_{2n}...,A_{mn})\\
\end{align}
$$

Then for arbitrary vector $v \in \mathbb{F}^n, v = (x_1,...,x_n)$ we have 

$$
\begin{align}
T(v) &= x_1T(u_1) + x_2 T(u_2) + \ldots + x_n T(u_n) \\
&= (A_{11}x_1 + A_{12}x_2 + \ldots + A_{1n}x_n,\\
& A_{21}x_1 + A_{22}x_2 + \ldots + A_{2n}x_n,\\ 
&\ldots \\
&A_{m1}x_1 + A_{m2}x_2 + \ldots + A_{mn}x_n)
\end{align}
$$

_Exercise 4_

Let us consider $a_1v_1 + a_2v_2 + \ldots + a_mv_m = 0$ and apply T to both parts of the equation. We have

$$
T(a_1v_1 + a_2v_2 + \ldots + a_mv_m) = T(0)
$$

$T(0)$ is 0, as we have proved, and we can use linearity on the left, after which we have

$$
a_1T(v_1) + a_2T(v_2) + \ldots + a_mT(v_m) = 0
$$

We know that $Tv_1,...,Tv_m$ are linearly independent, which imples that the equation above can hold only when $a_1 = a_2 = ... = a_m$ = 0. But this means, that the original equation holds only under the same conditions, which means that $v_1,...,v_m$ are linearly independent.

_Exercise 8_

I tried to come up with something simple, and I think that $\varphi(x, y) = \operatorname{sign}(x)\sqrt{|xy|}$ is a good choice. We can easiliy show, that $\varphi(ax,ay) = \operatorname{sign}(ax)\sqrt{|a^2xy|} = \operatorname{sign}(ax)|a|\sqrt{|xy|} = a\operatorname{sign}(x)\sqrt{|xy|} = a\varphi(x,y)$. However, it is obvious that $\varphi$ is not a linear map, since $\varphi(x + 0, y_1 + y_2) = \operatorname{sign}(x)\sqrt{|x(y_1 + y_2)|} \neq \operatorname{sign}(x)\sqrt{|xy_1|} + \operatorname{sign}(0)\sqrt{|0y_2|} = \operatorname{sign}(x)\sqrt{|xy_1|}$

_Exercise 9_

An example of a function which is additive, but non-homogeneous is $\varphi(x) = x^*$:

For instance, if we consider $\varphi(i * i) = \varphi(-1) = -1 \neq i\varphi(i) = i\cdot(-i) = 1$.

_Exercise 10_

Let us consider any element $u \in U$ and any element $w \in \{V \backslash U\}$: then $u + w \notin U$, because else we could subtract $u$ from it and get that $w \in U$. Having that, we can write

$$
\begin{align}
T(u + v) &= 0 \\
T(u + v) &= Tu + Tv = Su
\end{align}
$$

which means that $Tu = 0$ for any $u \in U$. But this is a contradiction, since S is not 0 map.

_Exercise 11_

Let us denote $u_1,...,u_m$ to be a basis of $U$. We can extend it to a basis of $V$ with some $v_1,...,v_k$. We now define our linear map to be 

$$
\begin{align}
Tu_i &= Su_i \ \forall i = 1...m \\
Tv_j &= 0 \ \forall j = 1...k
\end{align}
$$

_Exercise 12_

Suppose by contradiction that $\mathcal{L}(V, W)$ is finite-dimensional. Let $T_1,\dots,T_n$ be a basis of $\mathcal{L}(V, W)$ and $v_1,\dots,v_m$ of $V$. For every $w \in W$ there exists a linear map $T \in \mathcal{L}(V, W)$ such that

$$
Tv_1 = w, Tv_j = 0, \text{ for } j = 2,\dots,m.
$$

Because $T \in \mathcal{L}(V, W)$ we have

$$
T = a_1 T_1 + \dots + a_n T_n
$$

for some $a_1,\dots,a_n \in \mathbb{F}$. Thus

$$
a_1 T_1 v_1 + \dots + a_n T_n v_1 = w.
$$

Hence $w \in \operatorname{span}(T_1 v_1,\dots,T_n v_n)$. Because $w$ was arbitrary, we have that $W$ is a subspace of $\operatorname{span}(T_1 v_1,\dots,T_n v_1)$, which is finite-dimensional. By 2.26, $W$ is also finite-dimensional and we get a contradiction.

_Exercise 13_

If $v_k = 0$ for some $k$ when we can choose any nonzero vector as $w_k$.
So assume $v_k \neq 0$ for each $k$.
Let $n$ be the smallest integer such that $v_1, \dots, v_n$ is linearly indepedent.
Then we can write

$$
v_n = a_1 v_1 + \cdots + a_{n-1}v_{n-1}
$$

for some scalars $a_1, \dots, a_{n-1} \in \mathbb{F}$.
Then it suffices to choose any $w_1, \dots, w_n$ (the $w_k$ for $k > n$ won't make a difference) such that

$$
w_n \neq a_1 w_1 + \cdots + a_{n-1}w_{n-1}
$$

because if $T \in \mathcal{L}(V, W)$, with $Tv_k = w_k$ for each $k$, we must have

$$
\begin{align}
w_n
&= Tv_n\\\\
&= T(a_1 v_1 + \cdots + a_{n-1}v_{n-1})\\\\
&= a_1 Tv_1 + \cdots + a_{n-1}Tv_{n-1}\\\\
&= a_1 w_1 + \cdots + a_{n-1}w_{n-1}.
\end{align}
$$

_Exercise 14_

Let $v_1,\dots,v_n$ be a basis of $V$. Define $S,T \in \mathcal{L}(V, V)$ such that

$$
\begin{aligned}
S(a_1v_1 + \dots + a_nv_n) &= a_nv_1 + \dots + a_1v_n\\\\
T(a_1v_1 + \dots + a_nv_n) &= a_1v_1 + \dots + a_{n-1}v_{n-1}.
\end{aligned}
$$

By 3.5 $S$ and $T$ are well defined linear maps. But

$$
\begin{align*}
STv_n &= S0 = 0\\\\
TSv_n &= Tv_1 = v_1
\end{align*}.
$$

Hence $ST \neq TS$.
