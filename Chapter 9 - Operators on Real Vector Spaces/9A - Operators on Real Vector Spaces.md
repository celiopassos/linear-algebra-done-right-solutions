Chapter 9: **Operators on Complex Vector Spaces**

**9.A**

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
- [ ] Exercise 18
- [ ] Exercise 19

_Exercise 1_

$V_\mathbb{C}$ is clearly closed under addition.
We can write each complex number in the form $a + bi$ for some $a, b \in \mathbb{R}$ and we have

$$
(a + bi)(u + iv) = (au - bv) + i(av + bu) = (au - bv, av + bu) \in V \times V = V_{\mathbb{C}},
$$

where the first equality follows from the definition and the second because the vectors inside both parentheses are in $V$.
Thus $V_{\mathbb{C}}$ is closed under complex scalar multiplication.
If $0$ is the additive identity on $V$, then $0 + i0$ is the additive identity on $V_\mathbb{C}$ because

$$
(u + iv) + (0 + i0) = (u + 0) + i(v + 0) = u + iv.
$$

One easily checks that the rest of the properties listed in 1.19 are satisfied by $V_\mathbb{C}$.

Therefore $V_\mathbb{C}$ is a complex vector space.

_Exercise 2_

Let $u_1, u_2, v_1, v_2 \in V$.
Then

$$
\begin{aligned}
T_\mathbb{C} \big((u_1 + iv_1) + (u_2 + iv_2)\big) &= T_\mathbb{C} \big((u_1 + u_2) + i(v_1 + v_2)\big)\\\\
&= T(u_1 + u_2) + iT(v_1 + v_2)\\\\
&= (Tu_1 + iTv_1) + (Tu_2 + iTv_2)\\\\
&= T_\mathbb{C}(u_1 + iv_1) + T_\mathbb{C}(u_2 + iv_2).
\end{aligned}
$$

Hence $T_\mathbb{C}$ satisfies the additivity property of linear maps.
Now let $u, v \in V$ and $a, b \in \mathbb{R}$.
Then

$$
\begin{aligned}
T_\mathbb{C}\big((a + bi)(u + iv)\big) &= T_\mathbb{C}\big((au - bv) + i(av + bu)\big)\\\\
&= T(au - bv) + iT(av + bu)\\\\
&= (aTu - bTv) + i(aTv + bTu)\\\\
&= (a + bi)(Tu + iTv)\\\\
&= (a + bi)T_\mathbb{C}(u + iv)
\end{aligned}
$$

where the fourth line follows from the definition of complex scalar multiplication on $V_\mathbb{C}$.
Hence $T_\mathbb{C}$ satisfies the homogeneity property of linear maps.
Therefore $T_\mathbb{C}$ is a linear map.

_Exercise 3_

The forward direction is obvious, because $\mathbb{R} \subset \mathbb{C}$.
For the other direction we can just repeat the same argument used in the proof of 9.4 to show the linear independence of $v_1, \dots, v_n$.

_Exercise 4_

Suppose $v_1, \dots, v_m$ spans $V_\mathbb{C}$.
Let $v \in V$.
Then $v + i0 \in V_\mathbb{C}$ and we can write

$$
v + i0 = \lambda_1 v_1 + \dots + \lambda_m v_m = (\operatorname{Re} \lambda_1 v_1 + \dots + \operatorname{Re} \lambda_m v_m) + i(\operatorname{Im} \lambda_1 v_1 + \dots + \operatorname{Im} \lambda_m v_m)
$$

for some $\lambda_1, \dots, \lambda_m \in \mathbb{C}$.
The equation above implies that

$$
\operatorname{Re} \lambda_1 v_1 + \dots + \operatorname{Re} \lambda_m v_m = v
$$

Therefore $v \in \operatorname{span}(v_1, \dots, v_m)$.
Hence $v_1, \dots, v_m$ spans $V$.

Conversely, suppose $v_1, \dots, v_m$ spans $V$.
Then we can reduce this list to a basis of $V$.
But a basis of $V$ is also a basis $V_\mathbb{C}$.
Therefore we can reduce $v_1, \dots, v_m$ to a basis of $V_\mathbb{C}$ and this implies that it spans $V_\mathbb{C}$.

_Exercise 5_

Suppose $u, v \in V$.
Then

$$
\begin{aligned}
(S + T)\_\mathbb{C}(u + iv) &= (S + T)u + i(S + T)v\\\\
&= (Su + iSv) + (Tu + iTv)\\\\
&= S_\mathbb{C}(u + iv) + T_\mathbb{C}(u + iv).
\end{aligned}
$$

Thus $(S + T)\_\mathbb{C} = S_\mathbb{C} + T_\mathbb{C}$.
Now suppose $\lambda \in \mathbb{R}$.
Then

$$
(\lambda T)\_\mathbb{C}(u + iv) = \lambda Tu + \lambda iTv = \lambda(Tu + iTv) = \lambda T_\mathbb{C}(u + iv).
$$

Therefore $(\lambda T)\_\mathbb{C} = \lambda T_\mathbb{C}$.

_Exercise 6_

Suppose $T_\mathbb{C}$ is invertible.
Then, because $T_\mathbb{C}$ is surjective, for every $w \in V$ there exist $u, v \in V$ such that $T_\mathbb{C}(u + iv) = w + i0$.
This means that

$$
Tu + iTv = w + i0.
$$

Thus $Tu = w$.
Hence $T$ is surjective and therefore invertible.

Conversely, suppose $T$ is invertible.
Let $u, v \in V$.
By surjectivity of $T$, there exist $\hat{u}, \hat{v} \in V$ such that $T\hat{u} = u$ and $T\hat{v} = v$.
Thus

$$
T_\mathbb{C}(\hat{u} + i\hat{v}) = T\hat{u} + iT\hat{v} = u + iv.
$$

Since $u$ and $v$ were arbitrary, it follows that $T_\mathbb{C}$ is surjective and therefore invertible.

_Exercise 7_

Suppose $\mathbb{N}_C$ is nilpotent.
By 8.18, for any $v \in V$, we have

$$
0 + i0 = (N_\mathbb{C})^{\dim V}(v + i0) = N^{\dim V}v + i0
$$

where the second equality follows from 9.9.
This implies that $N^{\dim V}v = 0$.
Thus $N$ is nilpotent.

The other direction is obvious from 9.9 and the definitions.

_Exercise 8_

If $T_\mathbb{C}$ had a nonreal eigenvalue $\lambda$, then by 9.11 and 9.16 it would have $4$ eigenvalues, namely $5, 7, \lambda, \overline{\lambda}$, which is a contradiction because the dimension of $(\mathbb{R}^3)\_\mathbb{C}$ equals $3$ (see 9.4 (b)) and $\mathbb{T}_C$ has at most $3$ eigenvalues (see 5.13).

_Exercise 9_

Suppose by contradiction that $T \in \mathcal{L}(\mathbb{R}^7)$ is such that $T^2 + T + I$ is nilpotent.
Then by Exercise 7 $(T^2 + T + I)\_\mathbb{C}$ is also nilpotent and its minimal polynomial is of the form $z^j$ for some positive integer $j$ (because $0$ is its only eigenvalue, see Exercise 7 in section 8A and 8.49).
We have

$$
z^2 + z + 1 = \left(z - \frac{-1 + i\sqrt{3}}{2}\right)\left(z - \frac{-1 - i\sqrt{3}}{2}\right).
$$

Define $p \in \mathcal{P}(\mathbb{R})$ by

$$
p(z) = (z^2 + z + 1)^j.
$$

Then $p$ has no real roots and $p(T_\mathbb{C}) = 0$.
This is a contradiction, because $p$ must be a polynomial multiple of the minimal polynomial of $T_\mathbb{C}$ (by 8.46) and the minimal polynomial of $T_\mathbb{C}$ has at least one real root (see 9.19, 9.11 and 8.49).

_Exercise 10_

Choose $\lambda \in \mathbb{C}$ such that $\lambda^2 + \lambda + 1 = 0$ and define $T \in \mathcal{L}(\mathbb{C}^7)$ by

$$
Tv = \lambda v
$$

for all $v \in \mathbb{C}^7$.
Then

$$
(T^2 + T + I)v = T^2v + Tv + Iv = (\lambda^2 + \lambda + 1)v = 0.
$$

Therefore $T^2 + T + I$ is nilpotent.

_Exercise 11_

From the definitions, it is easy to see that

$$
(T_\mathbb{C}^2 + bT_\mathbb{C} + cI) = 0.
$$

Therefore $z^2 + bz + c$ is polynomial multiple of the minimal polynomial of $T_\mathbb{C}$ (see 8.46).
Note that, because this polynomial has real coefficients, it either has two real roots or two nonreal roots.
Thus $T$ has an eigenvalue if and only if $T_\mathbb{C}$ has a real root (see 9.10), which happens if and only if $z^2 + bz + c$ has a real root (by the previous reasoning and 8.49), which happens if and only if $b^2 \ge 4c$.

_Exercise 12_

By Exercise 3 in section 8D, the minimal polynomial of $T^2 + bT + cI$ is of the form $z^m$ for some positive integer $m$.
Let the $p$ be the polynomial defined by

$$
p(z) = (z^2 + bz + c)^m.
$$

Then $p$ has no real roots (because $z^2 + bz + c$ does not) and $p(T_\mathbb{C}) = 0$.
Thus 8.46 and 8.49 imply that $T_\mathbb{C}$ has no real eigenvalues.
Now 9.10 implies that $T$ has no eigenvalues.

_Exercise 13_

We have

$$
z^2 + bz + c = (z - \lambda)(z - \overline{\lambda})
$$

for some nonreal $\lambda \in \mathbb{C}$.
Suppose $v \in \operatorname{null}(T_\mathbb{C}^2 + bT_\mathbb{C} + cI)^j$.
Then

$$
0 = (T_\mathbb{C}^2 + bT_\mathbb{C} + cI)^j v = (T_\mathbb{C} - \lambda I)^j(T_\mathbb{C} - \overline{\lambda}I)^jv.
$$

It is easy to check that $v$ is of the form $v = u + w$ where $u \in G(\lambda, T_\mathbb{C})$ and $w \in G(\overline{\lambda}, T_\mathbb{C})$.
We have

$$
0 = (T_\mathbb{C} - \lambda I)^j(T_\mathbb{C} - \overline{\lambda}I)^jv = (T_\mathbb{C} - \lambda I)^j(T_\mathbb{C} - \overline{\lambda}I)u + (T_\mathbb{C} - \lambda I)^j(T_\mathbb{C} - \overline{\lambda}I)^jw.
$$

Since each generalized eigenspace is invariant under $T_\mathbb{C}$ and every vector in $V$ (the left side of the equation) can be written uniquely as linear combination of generalized eigenvectors that correspond to distinct eigenvalues, the equation above implies that

$$
(T_\mathbb{C} - \lambda I)^j(T_\mathbb{C} - \overline{\lambda}I)^ju = 0 \text{ and } (T_\mathbb{C} - \lambda I)^j(T_\mathbb{C} - \overline{\lambda}I)^jw = 0.
$$

Hence $u \in \operatorname{null} (T_\mathbb{C} - \lambda I)^j$ and $w \in \operatorname{null} (T_\mathbb{C} - \overline{\lambda} I)^j$.
Therefore

$$
\operatorname{null}(T_\mathbb{C}^2 + bT_\mathbb{C} + cI)^j \subset \operatorname{null} (T_\mathbb{C} - \lambda I)^j \oplus \operatorname{null} (T_\mathbb{C} - \overline{\lambda} I)^j.
$$

The inclusion in the other direction is obvious.
Thus

$$
\operatorname{null}(T_\mathbb{C}^2 + bT_\mathbb{C} + cI)^j = \operatorname{null} (T_\mathbb{C} - \lambda I)^j \oplus \operatorname{null} (T_\mathbb{C} - \overline{\lambda} I)^j,
$$

which gives us that

$$
\dim \operatorname{null}(T_\mathbb{C}^2 + bT_\mathbb{C} + cI)^j = \dim \operatorname{null} (T_\mathbb{C} - \lambda I)^j + \dim \operatorname{null} (T_\mathbb{C} - \overline{\lambda} I)^j.
$$

By 9.12, the two dimensions on the right side of the equation above are equal.
Therefore the left side is even.
One easily checks that

$$
(\operatorname{null} (T^2 + bT + cI))\_\mathbb{C} = \operatorname{null} (T_\mathbb{C}^2 + bT_\mathbb{C} + Ic).
$$

Now 9.4 (b) yields the desired result.

_Exercise 14_

Because it is nilpotent, the minimal polynomial of $T_\mathbb{C}^2 + T_\mathbb{C} + I$ is of the form $z^m$ for some positive integer $m$.
We have

$$
z^2 + z + 1 = (z - \lambda)(z - \overline{\lambda})
$$

for some nonreal $\lambda \in \mathbb{C}$.
Thus

$$
0 = (T_\mathbb{C}^2 + T_\mathbb{C} + I)^m = (T_\mathbb{C} - \lambda)^m(T_\mathbb{C} - \overline{\lambda})^m.
$$

This, together with 9.16, implies that the eigenvalues of $T_\mathbb{C}$ are $\lambda$ and $\overline{\lambda}$, with equal multiplicities, namely $4$.
The characteristic polynomial of $T_\mathbb{C}$, and of $T$ as well by definition, is therefore

$$
(z - \lambda)^4(z - \overline{\lambda})^4.
$$

which equals $(z^2 + z + 1)^4$.
By the Cayley-Hamilton Theorem (9.24), it follows that

$$
(T^2 + T + I)^4 = 0.
$$

_Exercise 15_

Suppose $U$ is a subspace of $V$ invariant under $T$.
Because $T|_U$ doesn't have an eigenvalue, 9.19 implies that $U$ has even dimension.


_Exercise 16_

Suppose $T$ is such that $T^2 = -I$.
Then clearly $T$ does not have an eigenvalue.
Then 9.19 implies that $\dim V$ is even.

Conversely, suppose $V$ has even dimension.
Let $v_1, \dots, v_n, u_1, \dots, u_n$ be a basis of $V$.
Define $T \in \mathcal{L}(V)$ by

$$
Tv_j = -u_j, Tu_j = v_j
$$

for each $j = 1, \dots, n$.
We have

$$
T^2v_j = -Tu_j = -v_j \text{ and } T^2u_j = Tv_j = -u_j.
$$

Thus $T^2 = -I$.

_Exercise 17_

_(a)_
Obviously $V$ closed under addition and complex scalar multiplication.
One can easily check that the other properties in 1.19 are satisfied.

_(b)_
Let $n$ be the integer such that $\dim V = 2n$ and consider the following process.

* Step $1$

    Choose a nonzero $v_1 \in V$.
    Then $v_1, Tv_1$ is linearly independent in $V$ as real vector space because $v_1$ is not an eigenvector of $T$ (because $T$ has no eigenvectors).
    Set $U_1 = \operatorname{span}(v_1, Tv_1)$.
    Then $\dim U_1 = 2$ and $U_1$ is invariant under $T$.

* Step $j$

    If $j = n + 1$, stop the process.
    We have that

    $$
    \dim U_{j-1} = 2(j-1) \le 2n - 2 < \dim V,
    $$

    $U_{j-1}$ is invariant under $T$ and

    $$
    v_1, Tv_1, \dots, v_{j-1}, Tv_{j-1}
    $$

    is a basis of $U_{j-1}$.
    Hence there exists a nonzero $w \in V$ such that $w \notin U_{j-1}$.
    Since $T$ is surjective, there exists $v_j \in V$ such that $Tv_j = w$.
    Thus $v_j \notin U_{j-1}$, because $U_{j-1}$ being invariant under $T$ would imply $w \in U_{j-1}$.
    Moreover, the list

    $$
    v_1, Tv_1, \dots, v_j, Tv_j \tag{1}
    $$

    is linearly independent.
    To see this, let $a_1, \dots, a_j, c_1, \dots, c_j \in \mathbb{R}$ such that

    $$
    a_1v_1 + c_1Tv_1 + \dots + a_jv_j + c_jTv_j = 0
    $$

    We already know that $v_j$ is not in the span of the previous vectors, so $c_j = 0$ implies $a_j = 0$ which implies that the rest of the $a$'s and $c$'s is $0$.
    Assume by contradiction $c_j \neq 0$.
    We can write the equation above as

    $$
    a_1v_1 + c_1Tv_1 + \dots + a_{j-1}v_{j-1} + c_{j-1}Tv_{j-1} = - a_jv_j - c_jTv_j. \tag{2}
    $$

    Applying $T$ to both sides we get

    $$
    a_1Tv_1 - c_1v_1 + \dots + a_{j-1}Tv_{j-1} - c_{j-1}v_{j-1} = - a_jTv_j + c_jv_j. \tag{3}
    $$

    Multiplying $(3)$ by $\frac{a_j}{c_j}$ and summing with $(2)$ shows us that


    $$
    \left(\frac{-a_j^2}{c_j} - c_j\right)Tv_j \in U_{j-1}.
    $$

    Hence the parentheses above equals $0$.
    This means that $-a_j^2 = c_j^2$, which is only possible if $a_j = c_j = 0$ and contradicts our assumption that $c_j \neq 0$.
    Therefore the list in $(1)$ is linearly independent.
    Set

    $$
    U_j = \operatorname{span}(v_1, Tv_1, \dots, v_j, Tv_j).
    $$

    Then $\dim U_j = 2j$ and $U_j$ is invariant under $T$.

At the end of the process, we will have constructed a subspace $U_n$ of $V$ which has a basis

$$
v_1, Tv_1, \dots, v_n, Tv_n
$$

and dimension $2n$.
Thus $U_n = V$ and the above list is a basis of $V$.
Clearly $v_1, \dots, v_n$ spans $V$ as a complex vector space.
Futhermore, it is linearly independent in $V$ as a complex vector space, because if a (complex) linear combination of it equals $0$, then a linear combination of the list above equals $0$, which implies that the coefficients are $0$.
Therefore $V$ as a complex vector space has dimension $n$, completing the proof.
