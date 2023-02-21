Chapter 8: **Operators on Complex Vector Spaces**

**8.B**

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

_Exercise 1_

By 8.21 (a), $V = G(0, N)$.
Since $G(0, N) = \operatorname{null} N^{\operatorname{dim} V}$ (see 8.11), it follows that $N^{\operatorname{dim} V} = 0$ and so $N$ is nilpotent.

_Exercise 2_

Define $T \in \mathcal{L}(\mathbb{R}^3)$ by

$$
T(x, y, z) = (0, -z, x).
$$

That is, $T$ squashes vectors onto the $yz$ plane and rotates them counterclockwise by $\pi/2$ radians.
So all eigenvectors of $T$ are contained in the $x$-axis and correspond to the eigenvalue $0$.
$T$ obviously is not nilpotent.

_Exercise 3_

Suppose $\lambda$ is an eigenvalue of $T$ and $v \in V$ a corresponding eigenvalue.
$S$ is surject, so there exists $u \in V$ such that $Su = v$.
Then

$$
S^{-1}TSu = S^{-1}Tv = \lambda S^{-1}v = \lambda u,
$$

which shows that $\lambda$ is an eigenvalue of $S^{-1}TS$.
Hence every eigenvalue of $T$ is an eigenvalue of $S^{-1}TS$.
We will prove these eigenvalues have the same multiplicity and it will follow that $S^{-1}TS$ cannot have other eigenvalues (by 8.26).

Suppose $\lambda_1, \dots, \lambda_m$ are the distinct eigenvalues of $T$.
Fix $k \in {1, \dots, m}$.
Let $v_1, \dots, v_d$ be a basis of $G(\lambda_k, T)$.
There exist $u_1, \dots, u_d \in V$ such that $Su_j = v_j$ for each $j = 1, \dots, d$.
It easy to check that the $u$'s are linearly independent.
We have

$$
G(\lambda_k, S^{-1}TS) = \operatorname{null} (S^{-1}TS - \lambda_k I)^{\operatorname{dim} V} = \operatorname{null} S^{-1}(T - \lambda_k I)^{\operatorname{dim} V}S,
$$

where the first equality comes from 8.11 and the second from Exercise 5 in section 5B.
For each $j$, we have

$$
S^{-1}(T - \lambda_k I)^{\operatorname{dim} V}Su_j = S^{-1}(T - \lambda_k I)^{\operatorname{dim} V}v_j = 0,
$$

where the second equality follows because $v_j \in G(\lambda_k, T)$.
This shows that $u_1, \dots, u_d \in G(\lambda_k, S^{-1}TS)$.
Hence

$$
\operatorname{dim} G(\lambda_k, S^{-1}TS) \ge d = \operatorname{dim} G(\lambda_k, T). \tag{1}
$$

By 8.26, we must have

$$
\operatorname{dim} G(\lambda_1, T) + \dots + \operatorname{dim} G(\lambda_m, T) = \operatorname{dim} V \tag{2}
$$

and

$$
\operatorname{dim} G(\lambda_1, S^{-1}TS) + \dots + \operatorname{dim} G(\lambda_m, S^{-1}TS) \le \operatorname{dim} V. \tag{3}
$$

$(1)$ and $(2)$ imply that $(3)$ is only possible if $\operatorname{dim} G(\lambda_k, S^{-1}TS) = \operatorname{dim} G(\lambda_k, T)$.
Hence, their multiplicieties are the same and $S^{-1}TS$ cannot have other generalized eigenspaces (the ones shown here already eat up the dimension of $V$).

_Exercise 4_

By the same reasoning used in the proof of 8.4, it follows that $\operatorname{dim} \operatorname{null} T^{n-1} \ge n - 1$.
But $\operatorname{null} T^{n-1} \subset \operatorname{null} T^n = G(0, T)$ (see 8.2 and 8.11).
Thus $\operatorname{dim} G(0, T) \ge n - 1$ and $0$ is an eigenvalue of $T$.
If $\operatorname{dim} G(0, T) = n$, 8.26 shows that $0$ is the only eigenvalue of $T$.
If $\operatorname{dim} G(0, T) = n - 1$, there is only space for one more eigenvalue with multiplicty $1$.

_Exercise 5_

Every eigenvector is also a generalized eigenvector, so in the forward direction we can make a similar argument to that of Exercise 3, where the dimensions only fit if each eigenspace equals its corresponding generalized one (because the former is a subset of the latter).
The other direction is obvious from 8.23.

_Exercise 6_

The formula for $N$ doesn't really matter here.
We only care about the dimension of $\mathbb{F}^{5}$, which is $5$.
Using the same reasoning from the proof of 8.31, and because $N^j = 0$ for $j \ge 5$, we have

$$
\begin{aligned}
I + N &= (I + a_1N + a_2N^2 + a_3N^3 + a_4N^4)\\\\
&= I + 2a_1N + (2a_2 + a_1^2)N^2 + (2a_3 + 2a_1a_2)N^3 + (2a_4 + 2a_1a_3 + a_2^2)N^4
\end{aligned}
$$

for some $a_1, a_2, a_3, a_4 \in \mathbb{F}$.
Choose

$$
\begin{aligned}
a_1 &= \frac{1}{2}\\\\
a_2 &= \frac{-1}{8}\\\\
a_3 &= \frac{1}{16}\\\\
a_4 &= \frac{-5}{128}
\end{aligned}
$$

and the terms on the second line will collapse to $N + I$.
Hence

$$
I + \frac{1}{2}N - \frac{1}{8}N^2 + \frac{1}{16}N^3 - \frac{5}{128}N^4
$$

is a square root of $N + I$.

_Exercise 7_

One can use the same strategy as in the proof of 8.31 to show that $I + N$ has a cube root for any nilpotent $N \in \mathcal{L}(V)$ and the rest of the proof will be same as the proof of 8.33.

_Exercise 8_

If $0$ is not an eigenvalue of $T$, then $T^j$ is injective and surjective for all integers $j$, which gives the desired result (take $j = n-2$).

Suppose $0$ is an eigenvalue of $T$.
Since $3$ and $8$ are also eigenvalues of $T$, by 8.26 the multiplicity of $0$, namely $\operatorname{dim} G(0, T)$ which equals $\operatorname{dim} \operatorname{null} T^n$, is at most $n - 2$.
By the same reasoning used in the proof of 8.4, we have $\operatorname{null} T^{n-2} = \operatorname{null} T^n$ (because the $\operatorname{null} T^{n-2} \subset \operatorname{null} T^n$).
Exercise 19 of section 8A implies that $\operatorname{range} T^{n-2} = \operatorname{range} T$.
Now 8.5 completes the proof.

_Exercise 9_

Keep in mind that when we mention the size of an $n$-by-$n$ matrix here we mean $n$ and not $n$ times $n$.

Let $V$ be vector space whose dimension equals the size $A$ (or $B$, since they're the same).
Choose a basis of $V$ and define $S, T \in \mathcal{L}(V)$ such that $\mathcal{M}(S) = A$ and $\mathcal{M}(T) = B$.
Then $\mathcal{M}(ST) = AB$.

Let $d_j$ equal the size of $A_j$ (or $B_j$, because they're the same).
Consider the list consisting of the first $d_1$ vectors in the chosen basis.
$A$ and $B$ show that the span of these vectors are invariant under $S$ and $T$.
Similarly, the span of the next $d_2$ vectors after this list is also invariant under $T$.
Continuing in this fashion, we see that there are $m$ distinct lists of consecutive vectors, with no intersections, in the chosen basis whose spans are invariant under $S$ and $T$.

Let $U_1, \dots, U_m$ denote such spans.
Clearly $\mathcal{M}(S|_{U_j}) = A_j$ and $\mathcal{M}(T|_{U_j}) = B_j$ for each $j$.
Hence $\mathcal{M}(S|_{U_j}T|_{U_j}) = A_jB_j$ and so it easy to see that $\mathcal{M}(ST)$ (which equals $AB$) has the desired form.

_Exercise 10_

Let $v_1, \dots, v_n$ denote a basis of $V$ consisting of generalized eigenvectors of $T$ (which exists by 8.23).
Define $\langle \cdot, \cdot \rangle: V \times V \to \mathbb{C}$ by

$$
\langle a_1 v_1 + \dots + a_n v_n, b_1 v_1 + \dots + b_n v_n \rangle = a_1\overline{b_1} + \dots + a_n\overline{b_n},
$$

where the $a$'s and $b$'s are complex numbers.
You can check that $\langle \cdot, \cdot \rangle$ is a well defined inner product on $V$.
Thus $v_1, \dots, v_n$ is an orthonormal basis of $V$.
Moreover, the generalized eigenspaces of $T$ are orthogonal to each other.
This implies that, if $v \in G(\beta, T)$, then

$$
P_{G(\alpha, T)} v =
\begin{cases}
v, \text{ if } \alpha = \beta\\\\
0, \text{ if } \alpha \neq \beta
\end{cases}
\tag{$\*$}
$$

where $P_{G(\alpha, T)}$ is the orthogonal projection of $V$ onto $G(\alpha, T)$.

Let $\lambda_1, \dots, \lambda_m$ denote the distinct eigenvalues of $T$.
We have

$$
T = T|_{G(\lambda_1, T)}P_{G(\lambda_1, T)} + \dots + T|_{G(\lambda_m, T)}P_{G(\lambda_m, T)}.
$$

For each $j = 1, \dots, m$, we can write $T|_{G(\lambda_j, T)} = \lambda_j I + N_j$ where $N_j$ is a nilpotent operator under which $G(\lambda_j, T)$ is invariant (see 8.21 (c)).
Therefore

$$
\begin{aligned}
T &= (\lambda_1 I + N_1)P_{G(\lambda_1, T)} + \dots + (\lambda_m I + N_m)P_{G(\lambda_m, T)}\\\\
&= \underbrace{\lambda_1 P_{G(\lambda_1, T)} + \dots + \lambda_m P_{G(\lambda_m, T)}}_\text{(4)} + \underbrace{N_1P_{G(\lambda_1, T)} + \dots + N_mP_{G(\lambda_m, T)}}_\text{(5)}.
\end{aligned}
$$

Fix $k \in \{1, \dots, n\}$.
Then $v_k \in G(\lambda_j, T)$ for some $j \in \{1, \dots m\}$.
$(*)$ shows that $(4)$ maps $v_k$ to $\lambda_j v_k$.
Hence $v_1, \dots, v_n$ is a basis of eigenvectors of $(4)$ and so $(4)$ is diagonalizable.
$(*)$ also shows that $(5)$ maps $v_k$ to $N_j v_k$.
But $G(\lambda_j, T)$ is invariant under $N_j$, so $(*)$ actually implies that $(5)$ raised to the power of $\operatorname{dim} V$ maps $v_k$ to $N_j^{\dim V}v_k$ which equals $0$.
Therefore $(5)$ is nilpotent.
It is easy to see that $(4)$ and $(5)$ commute (they map $v_k$ to $\lambda_j N_j v_k$, no matter the order), which completes the proof.

_Exercise 11_

Suppose $T$ has an upper-triangular matrix with respect to the basis $v_1, \dots, v_n$.
Suppose also that $\lambda$ appears on the $j$-th diagonal entry of $\mathcal{M}(T)$.
Then

$$
Tv_j = a_1 v_1 + \dots + a_{j-1} v_{j-1} + \lambda v_j
$$

for some $a_1, \dots, a_{j-1} \in \mathbb{F}$,
and so

$$
(T - \lambda I)v_j = a_1 v_1 + \dots + a_{j-1} v_{j-1} \in \operatorname{span}(v_1, \dots, v_{j-1})
$$

We have

$$
(T - \lambda I)v_{j-1} = c_1 v_1 + \dots + (c_{j-1} - \lambda) v_{j-1}
$$

for some $c_1, \dots, c_{j-1} \in \mathbb{F}$.
If $c_{j-1} - \lambda = 0$, then $(T - \lambda I)^2v_j \in \operatorname{span}(v_1, \dots, v_{j-2})$.
If $c_{j-1} - \lambda \neq 0$, then

$$
(T - \lambda I)\left(v_j - \frac{a_{j-1}}{c_{j-1} - \lambda}v_{j-1}\right) \in \operatorname{span}(v_1, \dots, v_{j-2}).
$$

We go on, either squaring by squaring $(T - \lambda I)$ or subtracting a vector $u \in \operatorname{span}(v_1, \dots, v_{j-1})$ from $v_j$ in the argument of $(T - \lambda I)$, and we will have $(T - \lambda I)^2(v_j - u)$  in the span of the first $j - 3$ vectors of the basis, then in span of the first $n - 4$, an so on until it will be in the span of an empty list, that is, $\\{0\\}$.
This means that $v_j - u \in G(\lambda, T)$ for some $u \in \operatorname{span}(v_1, \dots, v_{j-1})$.

Let $\nu_1, \dots, \nu_d$ denote the vectors of the chosen basis of $V$ that correspond to the columns of $\mathcal{M}(T)$ in which $\lambda$ appears and in the order that they appear on the basis.
We can repeat the previous process and find $u_1, \dots, u_d$ such

$$
\nu_1 - u_1, \dots, \nu_d - u_d \in G(\lambda, T), \tag{6}
$$

where each $u_k$ is in the span of the basis vectors that come before $\nu_k$.
We claim this list is linearly independent.
To see this, fix $k \in \\{1, \dots, d\\}$.
Suppose $\nu_k$ is the $j$-th basis vector, i.e. $\nu_k = v_j$.
This means that

$$
\operatorname{span}(\nu_1 - u_1, \dots, \nu_{k-1} - u_{k-1}) \subset \operatorname{span}(v_1, \dots, v_{j-1}).
$$

Therefore, we can't have $\nu_k - u_k \in \operatorname{span}(\nu_1 - u_1, \dots, \nu_{k-1} - u_{k-1})$, because that would imply that

$$
v_j \in \operatorname{span}(v_1, \dots, v_{j-1}),
$$

since $u_k \in \operatorname{span}(v_1, \dots, v_{j-1})$.
This argument can be repeated for each $k$.
Therefore no vector in $(6)$ is in the span of the previous ones.
It follows that the list in $(6)$ is linearly independent.

Hence $\operatorname{dim} G(\lambda, T) \ge d$.
By 8.26, the dimension of $G(\lambda, T)$ cannot be greater $d$, because we have $\operatorname{dim} V$ diagonal entries and each one adds at least $1$ to the dimension of some generalized eigenspace.
Thus $\operatorname{dim} G(\lambda, T) = d$, completing the proof.
