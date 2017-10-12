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
- [ ] Exercise 13
- [x] Exercise 14

_Exercise 12_

Suppose by contradiction that $\mathcal{L}(V, W)$ is finite-dimensional. Let $T_1,\dots,T_n$ be a basis of $\mathcal{L}(V, W)$ and $v_1,\dots,v_m$ of $V$. For every $w \in W$ there exists a linear map $T \in \mathcal{L}(V, W)$ such that

$$
Tv_1 = w, Tv_j = 0, \text{ for } j = 2,\dots,m
$$

Because $T \in \mathcal{L}(V, W)$ we have

$$
T = a_1 T_1 + \dots + a_n T_n
$$

For some $a_1,\dots,a_n \in \mathbb{F}$. Thus

$$
a_1 T_1 v_1 + \dots + a_n T_n v_1 = w
$$

Hence $w \in \operatorname{span}(T_1 v_1,\dots,T_n v_n)$. Because $w$ was arbitrary, we have that $W$ is a subspace of $\operatorname{span}(T_1 v_1,\dots,T_n v_1)$, which is finite-dimensional. By 2.26, $W$ is also finite-dimensional and we get a contradiction.

_Exercise 14_

Let $v_1,\dots,v_n$ be a basis of $V$. Define $S,T \in \mathcal{L}(V, V)$ such that

$$
\begin{aligned}
S(a_1v_1 + \dots + a_nv_n) &= a_nv_1 + \dots + a_1v_n\\\\
T(a_1v_1 + \dots + a_nv_n) &= a_1v_1 + \dots + a_{n-1}v_{n-1}
\end{aligned}
$$

By 3.5 $S$ and $T$ are well defined linear maps. But

$$
\begin{align*}
STv_n &= S0 = 0\\\\
TSv_n &= Tv_1 = v_1
\end{align*}
$$

Hence $ST \neq TS$.

