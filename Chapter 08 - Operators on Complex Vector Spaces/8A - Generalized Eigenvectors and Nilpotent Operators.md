Chapter 8: **Operators on Complex Vector Spaces**

**8.A**

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
- [x] Exercise 19
- [x] Exercise 20
- [x] Exercise 21

_Exercise 1_

Since

$$
T^2(w, z) = T(z, 0) = (0, 0),
$$

it follows that $G(0, T) = V$.
Therefore every vector in $\mathbb{C}^2$ is a generalized eigenvector of $T$.

_Exercise 2_

The eigenvalues of $T$ are $i$ and $-i$.
Since $\mathbb{C}^2$ has dimension $2$, the generalized eigenspaces are the eigenspaces themselves.

_Exercise 3_

We will prove $\operatorname{null} (T - \lambda I)^n = \operatorname{null} \left(T^{-1} - \frac{1}{\lambda} I\right)^n$ for all nonnegative integers $n$ by induction on $n$.

It is easy to check that $\operatorname{null} (T - \lambda I) = \operatorname{null} \left(T^{-1} - \frac{1}{\lambda} I\right)$ (see Exercise 9 in section 5C).
Let $n > 1$ and assume the result holds for all nonnegative integers less than $n$.
Suppose $v \in \operatorname{null}(T - \lambda I)^n$.
Then

$$
(T - \lambda I)v \in \operatorname{null}\left(T - \lambda I\right)^{n-1}.
$$

By the induction hypothesis

$$
(T - \lambda I)v \in \operatorname{null}\left(T^{-1} - \frac{1}{\lambda} I\right)^{n-1}.
$$

Thus

$$
0 = \left(T^{-1} - \frac{1}{\lambda} I\right)^{n-1}(T - \lambda I)v = (T - \lambda I)\left(T^{-1} - \frac{1}{\lambda} I\right)^{n-1}v,
$$

where the second equality follows from Theorem 1 in Chapter 5 notes.

Therefore

$$
\left(T^{-1} - \frac{1}{\lambda}I\right)^{n-1}v \in \operatorname{null} (T - \lambda I).
$$

But

$$
\operatorname{null} (T - \lambda I) = \operatorname{null} \left(T^{-1} - \frac{1}{\lambda} I\right).
$$

Hence

$$
\left(T^{-1} - \frac{1}{\lambda}I\right)^{n-1}v \in \operatorname{null} \left(T^{-1} - \frac{1}{\lambda} I\right)
$$

and so

$$
0 = \left(T^{-1} - \frac{1}{\lambda} I\right) \left(T^{-1} - \frac{1}{\lambda}I\right)^{n-1}v = \left(T^{-1} - \frac{1}{\lambda}I\right)^n v,
$$

which shows that $v \in \operatorname{null} (T^{-1} - \frac{1}{\lambda}I)$.
Therefore $\operatorname{null} (T - \lambda I)^n \subset \operatorname{null} \left(T^{-1} - \frac{1}{\lambda} I\right)^n$.
To prove the inclusion in the other direction, it suffices to repeat the same thing replacing $\left(T - \lambda I\right)$ with $\left(T^{-1} - \frac{1}{\lambda}I\right)$ and vice versa.

Now, by 8.11, we have

$$
G(\lambda, T) = \operatorname{null}(T - \lambda I)^{\operatorname{dim} V} = \operatorname{null}\left(T^{-1} - \frac{1}{\lambda} I\right)^{\operatorname{dim} V} = G\left(\frac{1}{\lambda}, T^{-1}\right).
$$

_Exercise 4_

Suppose $v \in G(\alpha, T) \cap G(\beta, T)$ and suppose by contradiction that $v \neq 0$.
Then $v, v$ are generalized eigenvectors corresponding to distinct generalized eigenvalues of $T$.
Now 8.13 implies that $v, v$ is linearly independent, which is clearly a contradiction.
Therefore $v$ must be $0$.

_Exercise 5_

Let $a_0, a_1, \dots, a_{m-1} \in \mathbb{F}$ such that

$$
0 = a_0v + a_1Tv + \dots + a_{m-1}T^{m-1}v
$$

Applying $T^{m-1}$ to both sides of the equation above yields

$$
0 = a_0T^{m-1}v,
$$

which shows that $a_0 = 0$.
Therefore

$$
0 = a_1Tv + \dots + a_{m-1}T^{m-1}v
$$

Applying $T^{m-2}$ yields

$$
0 = a_1T^{m-1}v,
$$

which shows that $a_1 = 0$.
Continuing in this fashion, we see that $a_0 = a_1 = \dots = a_m = 0$.
Thus $v, Tv, T^2v, \dots, T^{m-1}v$ is linearly independent.

_Exercise 6_

Suppose by contradiction that $S \in \mathcal{L}(\mathbb{C}^3)$ is a square root of $T$.
Note that $V = \operatorname{null} T^3$.
We have

$$
\begin{aligned}
V &= \operatorname{null} T^3\\\\
&= \operatorname{null} R^6\\\\
&= \operatorname{null} R^3\\\\
&= \operatorname{null} RT\\\\
&\subset \operatorname{null} R^2T\\\\
&= \operatorname{null} T^2,
\end{aligned}
$$

where the third line follows by 8.4.
But this a contradiction, since $T^2(z_1, z_2, z_3) = (z_3, 0, 0)$, we see that $\operatorname{null} T^2 = \\{(0, 0, z): z \in \mathbb{C}\\}$, then we can't have $V \subset \operatorname{null} T^2$.

_Exercise 7_

This follows directly from 8.19 and 5.32.

_Exercise 8_

False.
Let $V = \mathbb{C}^2$.
Define $S, T \in \mathcal{L}(\mathbb{C})$ by

$$
\begin{aligned}
S(z_1, z_2) &= (0, z_1)\\\\
T(z_1, z_2) &= (z_2, 0).
\end{aligned}
$$

Both $S$ and $T$ are nilpotent, however $S + T$ is not (its square equals the identity).

_Exercise 9_

We have

$$
\operatorname{null} (TS)^{\operatorname{dim} V} = \operatorname{null} TS(TS)^{\operatorname{dim} V} = \operatorname{null} T(ST)^{\operatorname{dim} V}S = V,
$$

where the first equality follows from 8.4 and the third because $(ST)^{\operatorname{dim} V} = 0$ (by 8.18).
Thus $(TS)^{\operatorname{dim} V} = 0$ and so $TS$ is nilpotent.

_Exercise 10_

If $T$ is not nilpotent, then $\operatorname{dim} \operatorname{null} T^n < n$ and , by the same reasoning used in 8.4, it follows that $\operatorname{null} T^{n-1} = \operatorname{null} T^n$.
Thus, by 8.5, we have

$$
V = \operatorname{null} T^{n-1} + \operatorname{range} T^n.
$$

Since $\operatorname{range} T^n \subset \operatorname{range} T^{n-1}$, we must also have

$$
V = \operatorname{null} T^{n-1} + \operatorname{range} T^{n-1}.
$$

Then, by the Fundamental Theorem of Linear Maps (3.22),

$$
\operatorname{dim} (\operatorname{null} T^{n-1} + \operatorname{range} T^{n-1}) = \operatorname{dim} V = \operatorname{dim} \operatorname{null} T^{n-1} + \operatorname{dim} \operatorname{range} T^{n-1}.
$$

3.78 now implies that $\operatorname{null} T^{n-1} + \operatorname{range} T^{n-1}$ is a direct sum.

_Exercise 12_

Suppose $v_1, \dots, v_n$ is such basis.
Then $Nv_1 = 0$, because the the first column of the matrix has $0$ in all its entries.
The definition of matrix of linear map shows that $Nv_2 \in \operatorname{span}(v_1)$.
But this implies that $N^2v_2 = 0$.
Similarly, $Nv_3 \in \operatorname{span}(v_1, v_2)$, so $N^3v_3 = 0$.
Continuing like this, we see that $N^j v_j = 0$, for each $j = 1, \dots, n$.
Therefore $N^n = 0$ and so $N$ is nilpotent.

_Exercise 13_

It is easy when $\mathbb{F} = \mathbb{C}$, because then $V$ has a basis consisting of eigenvectors of $N$ and for each vector $v$ in this basis we have $0 = N^{\operatorname{dim} V} v = \lambda^{\operatorname{dim} V} v$ for the corresponding eigenvalue $\lambda$, which implies that $\lambda = 0$.

More generally, without restricting $\mathbb{F}$ to $\mathbb{C}$, we will prove $N^{\operatorname{dim} V - 1} = 0$ and this fact can be used to show $N^{\operatorname{dim} V - 2} = 0$, which then can be used to show... and so on until $N^1$.

Let $\mathcal{N} = N^{\operatorname{dim} V - 1}$.
Note that $\mathcal{N}$ is also normal and that $\mathcal{N}^2 = 0$.
Then, for all $v \in V$,

$$
||\mathcal{N}^\*\mathcal{N}v||^2 = ||\mathcal{N}\mathcal{N}v|| = 0,
$$

where the first equality comes from 7.20.
Thus $\mathcal{N}\^*\mathcal{N} = 0$.
Therefore

$$
||\mathcal{N}v||^2 = \langle \mathcal{N}v, \mathcal{N}v \rangle = \langle v, \mathcal{N}^*\mathcal{N}v \rangle = 0,
$$

which shows that $\mathcal{N} = 0$.

_Exercise 14_

This follows directly from 8.19 and 6.37.

_Exercise 15_

By the same reasoning used in the proof of 8.4, it follows that $\operatorname{dim} \operatorname{null} N^{\operatorname{dim} V} \ge \operatorname{dim} V$.
Thus $\operatorname{dim} \operatorname{null} N^{\operatorname{dim} V} = \operatorname{dim} V$ and so $N$ is nilpotent.
We have $\operatorname{dim} V + 1$ null spaces each of different dimension.
Since the sequence

$$
\operatorname{dim} \operatorname{null} N^0, \operatorname{dim} \operatorname{null} N^1, \dots, \operatorname{dim} \operatorname{null} N^{\operatorname{dim} V}
$$

must be sorted in strictly increasing order, the only way this can fit is if $\operatorname{dim} \operatorname{null} N^j = j$ for each $j$.

_Exercise 16_

Obviously $V = \operatorname{range} T^0 = \operatorname{range} I$.
Let $k$ be a nonnegative integer.
Suppose $v \in \operatorname{range} T^{k+1}$.
Then $v = T^{k+1}u$ for some $u \in V$.
But then $v = T^k(Tu)$.
This implies that $v \in \operatorname{range} T^k$.

_Exercise 17_

By the Fundamental Theorem of Linear Maps (3.22), we have

$$
\operatorname{dim} \operatorname{null} T^m + \operatorname{dim} \operatorname{range} T^m = \operatorname{dim} \operatorname{null} T^{m+1} + \operatorname{dim} \operatorname{range} T^{m+1},
$$

which implies that $\operatorname{dim} \operatorname{null} T^m = \operatorname{dim} \operatorname{null} T^{m+1}$ (because $\operatorname{dim} \operatorname{range} T^m = \operatorname{dim} \operatorname{range} T^{m+1}$).
Thus, by 8.3, for all $k > m$, we have

$$
\operatorname{dim} \operatorname{null} T^m = \operatorname{dim} \operatorname{null} T^{m+k}.
$$

Applying the Fundamental Theorem of Linear Maps again to $T^m$ and $T^{m+k}$ we see that

$$
\operatorname{dim} \operatorname{range} T^m = \operatorname{dim} \operatorname{range} T^{m+k}.
$$

Since $\operatorname{range} T^{m+k} \subset \operatorname{range} T^m$, it follows that $\operatorname{range} T^{m+k} = \operatorname{range} T^m$.

_Exercise 18_

This follows directly from the previous exercise and 8.4.

_Exercise 19_

This is just a matter of realizing that $\operatorname{null} T^m \subset \operatorname{null} T^{m+1}$ and $\operatorname{range} T^{m+1} \subset \operatorname{range} T^m$ and applying the Fundamental Theorem of Linear Maps.

_Exercise 20_

By Exercise 19, $\operatorname{null} T^4 \neq \operatorname{null} T^5$.
By Exercise 15, this implies that $T$ is nilpotent.

_Exercise 21_

Let $W = \mathbb{F}^\infty \times \mathbb{F}^\infty$ and define $T \in \mathcal{L}(W)$ by

$$
T\bigr((x_1, x_2, x_3, \dots), (y_1, y_2, y_3, \dots)\bigl) = \bigr((x_2, x_3, \dots), (0, y_1, y_2, y_3, \dots)\bigl),
$$

that is, $T$ applies the backward shift operator (call it $B$) on the first slot and forward shift operator (call it $F$) on the second slot.
Thus, for each positive integer $k$, we have

$$
\operatorname{null} B^k = \\{(x_1, x_2, x_3, \dots) \in \mathbb{F}^\infty: x_j = 0 \text{ for all } j > k\\}
$$

and

$$
\operatorname{range} F^k = \\{(x_1, x_2, x_3, \dots) \in \mathbb{F}^\infty: x_1 = x_2 = \dots = x_k = 0\\}.
$$

Moreover $\operatorname{range} B^k = \mathbb{F}^\infty$ and $\operatorname{null} F^k = \\{0\\}$.
Note that $\operatorname{null} B^k \subsetneq \operatorname{null} B^{k+1}$ and $\operatorname{range} F^k \supsetneq \operatorname{range} F^{k+1}$.
Thus

$$
\operatorname{null} T^k = \\{(x, 0) \in \mathbb{F}^\infty \times \mathbb{F}^\infty: x \in \operatorname{null} B^k\\}
$$

and

$$
\operatorname{range} T^k = \\{(x, y) \in \mathbb{F}^\infty \times \mathbb{F}^\infty: y \in \operatorname{range} T^k\\}.
$$

Hence $\operatorname{null} T^k \subsetneq \operatorname{null} T^{k+1}$ and $\operatorname{range} T^k \supsetneq \operatorname{range} T^{k+1}$.
