Chapter 6: **Inner Product Spaces**

**6.C**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [ ] Exercise 4
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

Suppose $w \in \\{v_1, \dots, v_m\\}^\perp$.
Let $v = \in \operatorname{span}(v_1, \dots, v_m)$.
We have that

$$
v = a_1 v_1 + \dots a_m v_m
$$

for some $a_1, \dots, a_m \in \mathbb{F}$.
Moreover

$$
\langle v, w \rangle = \langle a_1 v_1 + \dots a_m v_m, w \rangle = a_1 \langle v_1, w \rangle + \dots + a_m \langle v_m, w \rangle = 0.
$$

Thus $w \in (\operatorname{span}(v_1, \dots, v_m))^\perp$ and so $\\{v_1, \dots, v_m\\}^\perp \subset (\operatorname{span}(v_1, \dots, v_m))^\perp$.

Now suppose $w \in (\operatorname{span}(v_1, \dots, v_m))^\perp$.
Since each $v_j$ is in $\operatorname{span}(v_1, \dots, v_m)$, it follows that $w$ is orthogonal to each $v_j$.
Therefore $w \in \\{v_1, \dots, v_m\\}^\perp$ and thus $(\operatorname{span}(v_1, \dots, v_m))^\perp \subset \\{v_1, \dots, v_m\\}^\perp$.

_Exercise 2_

Suppose $U^\perp = \{0\}$.
Since $V = U \oplus U^\perp$ (by 6.47), it follows that $U = V$.

Conversely, suppose $U = V$.
Then $U^\perp = V^\perp = \{0\}$.

_Exercise 3_

By 6.31, we have $\operatorname{span}(u_1, \dots, u_m) = \operatorname{span}(e_1, \dots, e_m)$.
Therefore $e_1, \dots, e_m$ is indeed an orthonormal basis of $U$.
Clearly $\operatorname{span}(f_1, \dots, f_n) \subset U^\perp$ (because each of the $f$'s are orthogonal to the basis of $U$).
Moreover,

$$
\operatorname{dim} U^\perp = \operatorname{dim} V - \operatorname{dim} U = m + n - m = n.
$$

Hence $f_1, \dots, f_n$ is linearly independent list of length $\operatorname{dim} U^\perp$, that is, a basis of $U^\perp$.

_Exercise 5_

Suppose $v \in V$.
By 6.47, we can write $v = u + w$, where $u \in U$ and $w \in U^\perp$.
Note that, by 6.51, $(U^\perp)^\perp = U$.
Thus $P_{U^\perp}v = w$, because $u \in (U^\perp)^\perp$.
Therefore

$$
P_{U^\perp}v = w = v - u = Iv - P_Uv = (I - P_U)v.
$$

Hence $P_{U^\perp} = I - P_U$.

_Exercise 6_

Suppose $P_U P_W = 0$.
Then $\operatorname{range} P_W \subset \operatorname{null} P_U$.
However, 6.55 shows that $\operatorname{range} P_W = W$ and $\operatorname{null} P_U = U^\perp$.
Thus $W \subset U^\perp$, which implies that $\langle u, w \rangle = 0$ for all $u \in U$ and all $w \in W$.

Conversely, suppose $\langle u, w \rangle = 0$ for all $u \in U$ and all $w \in W$.
It follows that $W \subset U^\perp$.
Let $v \in V$.
By 6.47, we can write $v = w + u$, where $w \in W$ and $u \in W^\perp$.
Then

$$
P_U P_W v = P_Uw = 0.
$$

Where the last equality, follows from the fact that $W \subset U^\perp$.

_Exercise 7_

Define $U = \operatorname{range} P$.
Suppose $u \in U$.
There exists $v \in V$ such that $Pv = u$.
Then

$$
u = Pv = P^2 v = P(Pv) = Pu.
$$

We've shown that $Pu = u$ for any $u \in U$.
Let $v \in V$.
By Exercise 4 in section 5B, we can write $v = u + w$ for some $u \in U$ and $w \in \operatorname{null} P$.
Note that $\operatorname{null} P \subset U^\perp$.
Thus

$$
Pv = P(u + w) = Pu = u = P_U(u + w) = P_Uv.
$$

Therefore $P = P_U$.

_Exercise 8_

We will try to prove that $U = \operatorname{range}P$ is the desired subspace, such that $P = P_U$.

Consider any basis $u_1,...,u_k$ of $U$, and extend it to a basis of $V$. Perform Gramm-Schmidt orthogonalization, getting orthonormal basis $e_1,...,e_n$, with $e_1,...,e_k$ still forming basis of $U$. We can notice, that $Pe_i = e_i$ for any $i =1...k$, because since $e_i \in U$, there exists $w: Pv = e_i$, and so $Pe_i = P^2w = Pw = e_i$. 

Consider $j>k$ with $Pe_j = b_1e_1 + ... + b_kc_k$ (since $Pe_j \in U$, it can be represented through its basis), and let us consider vector $v = x_1e_1 + ... x_ke_k + e_{k+1}$. We can easily write its squared norm as 

$$
||v||^2 = x_1^2 + ... + x_k^2 + 1
$$

Now, applying $P$ to this vector and computing its squared norm, we get

$$
||Pv||^2 = ||P(x_1e_1 + ... x_ke_k + e_{k+1})|| = (x_1 + b_1)^2 + ... + (x_k + b_k)^2
$$

We know, that $||Pv|| \le ||v||$, hence $||Pv||^2 \le ||v||^2$, so

$$
(x_1 + b_1)^2 + ... + (x_k + b_k)^2 \le x_1^2 + ... + x_k^2 + 1
$$

Let us select all $x_i$ to be proportional to $b_i$ with some fixed coefficient $x$: $x_i = xb_i$. Then, inequality simplifies

$$
\begin{align}
(1 + x)^2b_1^2 + ... + (x + 1)^2b_k^2 &\le x^2(b_1^2 + ... + b_k^2) + 1 \implies \\
(2x + 1)\sum\limits_{i=1}^kb_i^2 &\le 1
\end{align}
$$

We can now see, that if $\sum\limits_{i=1}^kb_i^2 \neq 0$, we have a condition which can be violated by selecting appropriate $x > \frac{1}{2\sum\limits_{i=1}^kb_i^2} - \frac{1}{2}$. Hence, $\sum\limits_{i=1}^kb_i^2 = 0$, which implies $b_i = 0$ for all $i=1...k$, so $Pe_j = 0$ for any $j > k$, and so since for any $v \in V$ $v = \sum\limits_{i=1}^kx_ie_i +  \sum\limits_{i=k+1}^nx_ie_i = u + w$, where $u \in U$ and $w \in U^\perp$, and $Pv = u$, we conclude, that $P = P_U$.

_Exercise 9_

Suppose $U$ is invariant under $T$.
Let $v \in V$.
Then, by part (b) in 6.55, $P_U v \in U$, which implies that $T P_U v \in U$ (since $U$ is invariant under $T$), which implies that $P_U T P_U v = T P_U v$.
Thus $P_U T P_U = T P_U$.

Conversely, suppose $P_U T P_U = T P_U$.
Let $u \in U$.
Then

$$
Tu = T P_U u = P_U T P_U u \in U.
$$
Therefore $U$ is invariant under $T$.

_Exercise 10_

Suppose $U$ and $U^\perp$ are both invariant under $T$.
Let $v \in V$.
Then $v = u + w$ for some $u \in U$ and $w \in U^\perp$.
Therefore, by parts (b) and (c) from 6.55, we have

$$
\begin{aligned}
P_U Tv &= P_U Tu + P_U Tw\\\\
&= P_U Tu\\\\
&= Tu\\\\
&= TP_U u\\\\
&= TP_U u + TP_U w\\\\
&= TP_U v.
\end{aligned}
$$

Hence $P_U T = TP_U$.

Conversely, suppose $P_U T = TP_U$.
Let $u \in U$.
Then

$$
Tu = TP_U u = P_U Tu \in U,
$$

Hence $U$ is invariant under $T$.
Let $w \in U^\perp$.
Then

$$
\begin{aligned}
Tw &= Tw - TP_U w = Tw - P_U Tw = (I - P_U)Tw = P_{U^\perp} Tw \in U^{\perp}
\end{aligned}
$$

where the last equality follows from Exercise 5.
Therefore $U^\perp$ is invariant under $T$.

_Exercise 11_

Applying the Gram-Schmidt procedure to the basis $(1, 1, 0, 0), (1, 1, 1, 2)$ we get $\frac{1}{\sqrt{2}}(1, 1, 0, 0), \frac{1}{\sqrt{5}}(0, 0, 1, 2)$.
Using the formula from part (i) in 6.55 to calculate $P_U (1, 2, 3, 4)$, we get

$$
P_U (1, 2, 3, 4) = \frac{3}{2}(1, 1, 0, 0) + \frac{11}{5}(0, 0, 1, 2).
$$

_Exercise 12_

Define $U$ by

$$
U = \{p \in P_3(\mathbb{R}): p(0) = 0 \text{ and } p'(0)\}.
$$

Note that $U$ is a subspace of $\mathcal{P}_3(\mathbb{R})$.
Let $u \in U$.
Since $p \in \mathcal{P}_3(\mathbb{R})$, we have

$$
p(x) = ax^3 + bx^2 + cx + d
$$

for some $a, b, c, d \in \mathbb{R}$.
$p(0) = 0$ and $p'(0) = 0$ now imply that $c = d = 0$ and so $U \subset \operatorname{span}(x^2, x^3)$.
Because $x^2, x^3 \in U$, it follows that $x^2, x^3$ is a basis of $U$.
Applying the Gram_Schmidt Procedure to this basis, we get

$$
\sqrt{5}x^2, 6\sqrt{7}x^3 - 5\sqrt{7}x^2.
$$

Now, using the formula from part(i) in 6.55 to get $P_U(2 + 3x)$, we get

$$
P_U(2 + 3x) = -\frac{203}{10}x^3 + 24x^2.
$$

_Exercise 13_

In this Exercise, I used the SymPy Python package to calculate the integrals necessary for the Gram-Schmidt Procedure on the basis $1, x, x^2, x^3, x^4, x^5$ of $\mathcal{P}_5(\mathbb{R})$ and to compute the polynomial $p$ with the formula in 6.55 (i).
I found the following

$$
p(x) = x^{5} \left(- \frac{72765}{8 \pi^{8}} + \frac{693}{8 \pi^{6}} + \frac{654885}{8 \pi^{10}}\right) + x^{3} \left(- \frac{363825}{4 \pi^{8}} - \frac{315}{4 \pi^{4}} + \frac{39375}{4 \pi^{6}}\right) + x \left(- \frac{16065}{8 \pi^{4}} + \frac{105}{8 \pi^{2}} + \frac{155925}{8 \pi^{6}}\right),
$$

which, if you assume $\pi = 3.14159265359$, is exactly what appers in 6.60.
Here is the code used:

```python
from sympy import *

x = Symbol('x')

def inner_product(f, g):
    return integrate(f*g, (x, -pi, pi))

def gs_procedure(basis):
    orthonormal_basis = []

    for j, v_j in enumerate(basis):
        e_j = v_j - sum(map(lambda e_k: inner_product(v_j, e_k) * e_k, orthonormal_basis[:j - 1]))
        e_j = e_j / sqrt(inner_product(e_j, e_j))
        orthonormal_basis.append(e_j)

    return orthonormal_basis

def project(func, orthonormal_basis):
    return sum(map(lambda e_j: inner_product(func, e_j) * e_j, orthonormal_basis))

orthonormal_basis = gs_procedure([1, x, x**2, x**3, x**4, x**5])

approx_sin = project(sin(x), orthonormal_basis)

p = collect(expand(approx_sin), x)
print(latex(p))
```

_Exercise 14_

_(a)_

Suppose there exists $v \neq 0: v \in U^\perp$. We can represent it as $v(x) = u(x) + v(0)$, where $u(x) = v(x) - v(0) \in U$, since $u(0) = 0$. 

Since $u \in U$, it follows that $\langle v, u \rangle = 0$:
$$
\langle v, u \rangle = ||u||^2 + v(0)\langle u, 1 \rangle = 0
$$

We have two options here: 

1. Suppose $\langle u, 1 \rangle = 0$. This implies $||u||^2 = 0$, and this is possible only if $u(x) = 0$, so $v(x) = v(0) = const$, and it is easy to show that this restricts $v(0) = 0$, because $\langle v, x^2 \rangle = v(0)\frac{1}{3}x^3 \Big |_{-1}^1 = \frac{2}{3}v(0)$ should be equal 0 since $x^2 \in U$, which implies $v(x) = v(0) = 0$, and this contradicts our hypothesis that $v(x) \neq 0$.
2. $\langle u, 1 \rangle \neq 0$. Then, we can express $v(0)$:

$$
v(0) = -\frac{||u||^2}{\langle u, 1 \rangle}
$$

Consider 

$$
f_n(x) = 
\begin{cases}
1, |x| > \frac{1}{n}\\
n|x|, |x| \le \frac{1}{n}
\end{cases}
$$

It is clear that $f_n \in C_\mathbb{R}([-1,1])$, and 

$$
\langle v, f_n \rangle = \langle v, 1 \rangle - \int\limits_{-\frac{1}{n}}^\frac{1}{n}v(x)n|x|dx
$$

Since $v$ is continuous, $\forall \varepsilon > 0 \ \exists \delta: |x| < \delta \implies |v(x) - v(0)| < \varepsilon$. 

So, for arbitrary $\varepsilon > 0$ we can find $N_\varepsilon = [\frac{1}{\delta}] + 1$, such that if $n > N_\varepsilon$, we get $|v(x) - v(0)| < \varepsilon$ when $x \in [-\frac{1}{n}, \frac{1}{n}]$.

This means that when $n > N_\varepsilon$, we have

$$
\int\limits_{-\frac{1}{n}}^\frac{1}{n}v(x)n|x|dx \le \int\limits_{-\frac{1}{n}}^\frac{1}{n}(v(0) + \varepsilon)n|x|dx = \frac{(v(0) + \varepsilon)}{n}
$$

In the same fashion, 

$$
\int\limits_{-\frac{1}{n}}^\frac{1}{n}v(x)n|x|dx \ge \int\limits_{-\frac{1}{n}}^\frac{1}{n}(v(0) - \varepsilon)n|x|dx = \frac{(v(0) - \varepsilon)}{n}
$$

This means, that $\operatorname{lim}\limits_{n \to \infty}\int\limits_{-\frac{1}{n}}^\frac{1}{n}v(x)n|x|dx = 0$

So, taking limit of $\langle f_n, v \rangle$, we get 

$$
0 = \langle v, 1 \rangle
$$

This implies, that $0 = \langle u + v(0), 1 \rangle = \langle u, 1 \rangle + 2v(0)$, so 

$$
\langle u, 1 \rangle = - 2v(0)
$$

and so, 

$$
v(0) = -\frac{||u||^2}{\langle u, 1 \rangle} = \frac{||u||^2}{2v(0)}
$$

Hence 

$$
v(0)^2 = \frac{1}{2}||u||^2
$$

Now, consider $||v||^2$:

$$
||v||^2 = ||u||^2 + 2v(0)\langle u, 1 \rangle + 2v(0)^2
$$


Substituting $v(0)$ and $v(0)^2$ we get

$$
||v||^2 = ||u||^2 -2\frac{||u||^2}{\langle u, 1 \rangle}\langle u, 1 \rangle + 2 \frac{1}{2}||u||^2 = 0
$$

Which implies that $v = 0$, and this is a contradiction with $v \neq 0$.

So, in both cases we ended up with a contradiction, so $U^\perp = \{0\}$.

_(b)_

We can easily see, that $C_\mathbb{R}([-1, 1]) = U \oplus \{f(x) = c| c \in \mathbb{R}\}$, and so $C_\mathbb{R}([-1, 1]) \neq U \oplus U^\perp$.

As for the second statement, it is clear that $(U^\perp)^\perp = \{0\}^\perp = C_\mathbb{R}([-1, 1]) \neq U$. 
