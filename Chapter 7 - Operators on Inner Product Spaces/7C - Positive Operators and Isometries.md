Chapter 7: **Positive Operators and Isometries**

**7.C**

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

_Exercise 1_

We give a counterexample.
Define $T \in \mathcal{L}(\mathcal{R}^2)$ by

$$
\begin{aligned}
Te_1 = e_1\\\\
Te_2 = -e_2
\end{aligned}
$$

where $e_1, e_2$ is the standard basis of $\mathbb{R}^2$.
The matrix of $T$ with respect to this same basis is

$$
\begin{pmatrix}1 & 0\\\\0 & -1\end{pmatrix},
$$

which equals its transpose, therefore $T$ is self-adjoint.
Moreover, the basis $\frac{1}{\sqrt{2}}(e_1 + e_2), \frac{1}{\sqrt{2}}(e_1 - e_2)$ is orthonormal and

$$
\begin{aligned}
\left\langle T\left(\frac{1}{\sqrt{2}}(e_1 + e_2)\right), \frac{1}{\sqrt{2}}\left(e_1 + e_2\right) \right\rangle &= 0\\\\
\left\langle T\left(\frac{1}{\sqrt{2}}(e_1 - e_2)\right), \frac{1}{\sqrt{2}}\left(e_1 - e_2\right) \right\rangle &= 0,
\end{aligned}
$$

but $T$ is not positive because

$$
\langle Te_2, e_2 \rangle = \langle -e_2, e_2 \rangle = -1.
$$

_Exercise 2_

$T$ is the positive square root of $T^2$.
Note that

$$
T^2v = TTv = Tw = v
$$

hence $v$ is an eigenvalue of $T^2$.
From the proof of 7.36, we see that $Tv = \sqrt{1}v$.
But $Tv = w$, therefore $v = w$.

_Exercise 3_

For all $u \in U$, we have

$$
\langle T|_U u, u \rangle = \langle Tu, u \rangle = \langle u, Tu \rangle = \langle u, T|_U u \rangle.
$$

Thus, $T|_U$ is self-adjoint.
Furthermore,

$$
\langle T|_U u, u \rangle = \langle Tu, u \rangle \ge 0,
$$

which shows that $T|_U$ is positive.

_Exercise 4_

We have $(T^\*T)^\* = T^\*(T^\*)^\* = T^\*T$, which implies that $T^\*T$ is self-adjoint and, for all $v \in V$,

$$
\langle T^\*Tv, v \rangle = \langle Tv, Tv \rangle \ge 0.
$$

Thereofer $T^\*T$ is positive.

It's basically the same thing for $TT^\*$.

_Exercise 5_

Suppose $S, T \in \mathcal{L}(V)$ are positive operators.
Then

$$
(S + T)^\* = S^\* + T^\* = S + T.
$$

Hence $S + T$ is self-adjoint.
Moreover, for all $v \in V$, we have

$$
\langle (S + T)v, v \rangle = \langle Sv, v \rangle + \langle Tv, v \rangle \ge 0,
$$

showing that $S + T$ is positive.

_Exercise 6_

From 7.6 (e), we have

$$
(T^k)^\* = (T^\*)^k = T^k.
$$

Therefore $T^k$ is self-adjoint.

To prove $T^k$ is positive, there are two cases.

* If $k$ is odd, we have $k = 2n + 1$ for some nonnegative integer $n$. Then, for all $v \in V$,

    $$
    \langle T^k v, v \rangle = \langle T^nTT^nv, v \rangle = \langle TT^nv, T^nv \rangle \ge 0
    $$

    where the the inequality follows because $T$ is positive.

* If $k$ is even, we have $k = 2n$ for some nonnegative integer $n$. Then, for all $v \in V$,

    $$
    \langle T^k v, v \rangle = \langle T^nT^nv, v \rangle = \langle T^nv, T^nv \rangle \ge 0.
    $$

Therefore $T^k$ is positive.

_Exercise 7_

Suppose $T$ is invertible.
Let $R$ be the positive square root of $T$.
Then

$$
\langle Tv, v \rangle = \langle R^\*Rv, v \rangle = \langle Rv, Rv \rangle > 0,
$$

where the inequality follows because $R$ and $T$ have the same eigenvalues (as we saw in the proof of 7.36), but $0$ is not an eigenvalue of $T$, thus $Rv \neq 0$ for all $v$.

Conversely, suppose $\langle Tv, v \rangle > 0$ for every $v \in V$ with $v \neq 0$.
This directly implies that $\operatorname{null} T = \\{0\\}$.
Thereofer $T$ is invertible.

_Exercise 8_

Suppose $\langle \cdot, \cdot \rangle_T$ is an inner product on $V$.
Let $v \in \operatorname{null} T$.
Then

$$
\langle v, v \rangle_T = \langle Tv, v \rangle = \langle 0, v \rangle = 0.
$$

Therefore, by the definiteness property of inner products, $v = 0$.
Thus $\operatorname{null} T = \\{0\\}$ and so $T$ is invertible.
Suppose now that $v$ is an eigenvector of $T$ with eigenvalue $\lambda$.
Then

$$
0 \le \langle v, v \rangle_T = \langle Tv, v \rangle = \lambda \langle v, v \rangle.
$$

Thus $\lambda \ge 0$.
Hence all eigenvalues of $T$ are nonnegative.
We but need to show that $T$ is self-adjoint and then $T$ will be positive by 7.35.
We have

$$
\begin{aligned}
\langle u, T^\*v \rangle &= \langle Tu, v \rangle\\\\
&= \langle u, v \rangle_T\\\\
&= \overline{\langle v, u \rangle_T}\\\\
&= \overline{\langle Tv, u \rangle}\\\\
&= \langle u, Tv \rangle.
\end{aligned}
$$

Hence $T$ is self-adjoint.

Conversely, suppose $T$ is an invertible positive operator.
The positive-definiteness property of $\langle \cdot, \cdot \rangle_T$ follows from the forward direction of the previous exercises.
For additivity in the first slot, we have

$$
\begin{aligned}
\langle u + v, w \rangle_T &= \langle T(u+v), w \rangle\\\\
&= \langle Tu, w \rangle + \langle Tv, w \rangle\\\\
&= \langle u, w \rangle_T + \langle v, w \rangle_T.
\end{aligned}
$$

Similarly, $\langle \cdot, \cdot \rangle_T$ satisfies homogeneity in the first slot.
For conjugate symmetry, we have

$$
\begin{aligned}
\langle u, v \rangle_T &= \langle Tu, v \rangle\\\\
&= \langle u, Tv \rangle\\\\
&= \overline{\langle Tv, u \rangle}\\\\
&= \overline{\langle v, u \rangle_T},
\end{aligned}
$$

where the second line follows because $T$ is self-adjoint.
Therefore $\langle \cdot, \cdot \rangle_T$ is indeed an inner product on $V$.

_Exercise 9_

It is true.
We shall consider $\mathbb{F} = \mathbb{R}$ for the sake of simplicity and it will be easy to see it generalizes to $\mathbb{C}$ as well.

Note that if $R$ is a self-adjoint square root of $I$ if and only if the matrix of $R$ is of the form

$$
\begin{pmatrix}a & b\\\\b & c\end{pmatrix}
$$

and

$$
\begin{aligned}
e_1 &= R^2e_1\\\\
&= R(ae_1 + be_2)\\\\
&= a(ae_1 + be_2) + b(be_1 + ce_2)\\\\
&= (a^2 + b^2)e_1 + b(a + c)e_2
\end{aligned}
$$

and

$$
\begin{aligned}
e_2 &= R^2e_2\\\\
&= R(be_1 + ce_2)\\\\
&= b(ae_1 + be_2) + c(be_1 + ce_2)\\\\
&= b(a+c)e_1 + (b^2 + c^2)e_2.
\end{aligned}
$$

Therefore, the problems falls down to finding $a, b, c \in \mathbb{F}$ such that

$$
\begin{aligned}
a^2 + b^2 &= 1\\\\
b^2 + c^2 &= 1\\\\
b(a + c) &= 0.
\end{aligned}
$$

As turns out, there are infinitely many solutions to this (just choose an $a \in [0, 1]$, take $c = -a$ and solve for $b$).
Each of this solutions define a different self-adjoint square root, hence the identity operator has infinitely-many self-adjoint square roots.

_Exercise 10_

Suppose (a) holds, so $S$ is an isometry.
Then 7.42 ("(a) $\Rightarrow$ (f)") implies that $SS^\* = I$.
Therefore, for all $u, v \in V$ we have

$$
\langle u, v \rangle = \langle SS^\*u, v \rangle = \langle S^\*u, S^\*v \rangle.
$$

Thus (b) holds.
Clearly (b) implies (c) and (c) implies (d).
Now suppose (d) holds.
Then 7.42 ("(d) $\Rightarrow$ (g)" with $S$ replaced with $S^\*$) implies that $S$ is an isometry.
Thus (a) holds.

_Exercise 11_

Let $e_1, e_2, e_3$ and $f_1, f_2, f_3$ be orthonormal bases of $\mathbb{F}^3$ consisting of eigenvectors of $T_1$ and $T_2$, respectively, corresponding to the eigenvalues $2, 5, 7$.
Define $S$ by

$$
Se_j = f_j
$$

for $j = 1, 2, 3$.
One easily checks that $S$ is an isometry (using the Pythagorean Theorem).
Then, because $S^{-1} = S^\*$ (by 7.42), we have $S^\*f_j = e_j$.
Thus

$$
T_1e_1 = 2e_1 = S^\*(2f_1) = S^\*(T_2f_1) = S^\*T_2Se_1.
$$

Similarly $T_1e_2 = S^\*T_2Se_2$ and $T_1e_3 = S^\*T_2Se_3$.
Therefore $T_1 = S^\*T_2S$.

_Exercise 12_

Let $e_1, e_2, e_3, e_4$ denote an orthonormal basis of $\mathbb{F}^4$.
Define $T_1, T_2 \in \mathcal{L}(\mathbb{F}^4)$ by

$$
\begin{aligned}
T_1e_1 &= 2e_1\\\\
T_1e_2 &= 2e_2\\\\
T_1e_3 &= 5e_3\\\\
T_1e_4 &= 7e_4\\\\
\\\\
T_2e_1 &= 2e_1\\\\
T_2e_2 &= 5e_2\\\\
T_2e_3 &= 5e_3\\\\
T_2e_4 &= 7e_4.
\end{aligned}
$$

Then both $T_1$ and $T_2$ are self-adjoint (the matrices equal their transposes) and $2, 5, 7$ are their eigenvalues.
Suppose by contradiction that $S$ is an isometry on $V$ such that $T_1 = S^\*T_2S$.
Let $v \in V$ be the vector that $S$ maps to $e_2$.
Then

$$
T_1v = S^\*T_2Sv = S\^*T_2e_2 = 5S\^*e_2 = 5v
$$

Therefore $v \in E(T_1, 5) = \operatorname{span}(e_3)$.
Let also $w \in V$ be the vector that $S$ maps to $e_3$.
Note that $v, w$ is linearly independent, because $e_2, e_3$ is linearly independent.
Then

$$
T_1w = S^\*T_2Sw = S\^*T_2e_3 = 5S\^*e_3 = 5w.
$$

Therefore $w \in E(T_1, 5) = \operatorname{span}(e_3)$.
But this is a contradiction, because we can't have a linearly independent list of length $2$, $v, w$, in a $1$-dimensional vector space, $\operatorname{span}(e_3)$.
Hence, there does not exist such $S$.

Notice that it wasn't necessary to require $S$ to be an isometry, we just needed to suppose, by contradiction, the existence of an invertible $S$ such that $T_1 = S^{-1}T_2S$.
This $S$ does not exist.
Since the desired isometry must satisfy the same property (because the adjoint of an isometry equals its inverse), it follows that there cannot exist such isometry.
The key idea here is that the eigenspaces of $T_1$ and $T_2$ don't fit.

_Exercise 13_

It is false.
Let $e_1, \dots, e_n$ be an orthonormal basis of $V$ and define $Se_j = e_1$ for $j = 1, \dots, n$.
Then $||Se_j|| = 1$ for each $e_j$, but obviously $S$ is not invertible, therefore $S$ is not an isometry (7.42 requires isometries to be invertible).

_Exercise 14_

In the exercise, $T$ was already shown to be self-adjoint.
So $-T$ is also self-adjoint.
Note that $1, \cos x, \cos 2x, \dots, \cos nx, \sin x, \sin 2x, \dots, \sin nx$ is a basis of $V$ consisting of eigenvectors of $-T$ whose corresponding eigenvalues are all nonnegative.
Thus by 7.35 $-T$ is positive.
