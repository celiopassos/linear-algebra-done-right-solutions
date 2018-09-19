Chapter 3: **Linear Maps**

**3.A**

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
- [ ] Exercise 11
- [x] Exercise 12
- [x] Exercise 13
- [x] Exercise 14

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

\begin{align}
w_n
&= Tv_n\\\\
&= T(a_1 v_1 + \cdots + a_{n-1}v_{n-1})\\\\
&= a_1 Tv_1 + \cdots + a_{n-1}Tv_{n-1}\\\\
&= a_1 w_1 + \cdots + a_{n-1}w_{n-1}.
\end{align}

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
