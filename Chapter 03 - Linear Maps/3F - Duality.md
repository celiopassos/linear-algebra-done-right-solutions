Chapter 3: **Linear Maps**

**3.F**

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
- [ ] Exercise 32
- [x] Exercise 33
- [ ] Exercise 34
- [x] Exercise 35
- [ ] Exercise 36
- [ ] Exercise 37

_Exercise 1_

Because for any linear functional $\varphi$, we have $\operatorname{dim}\operatorname{range}\varphi \leq \operatorname{dim}\mathbb{F} = 1$.

_Exercise 2_

Define $\varphi,\psi,\omega \in \mathcal{L}(\mathbb{R^{[0,1]}}, \mathbb{F})$ such that if $f \in \mathbb{R^{[0,1]}}$, then

$$
\begin{aligned}
\varphi(f) &= f(0)\\\
\psi(f) &= \pi f(0) + f(1)\\\
\omega(f) &= f(0) - if(1)
\end{aligned}
$$

_Exercise 3_

Since $v$ is non-zero, we can extend it to a basis $v, v_1, \dots, v_n$ of $V$.
Let $\varphi, \varphi_1, \dots, \varphi_n$ be the dual basis of $v, v_1, \dots, v_n$.
By definition of dual basis, we have $\varphi(v) = 1$, as desired.

_Exercise 4_

Let $u_1, \dots, u_n$ be a basis of $U$.
Extend it to a basis $u_1, \dots, u_n, v_1, \dots, v_m$ of $V$ and let $\omega_1, \dots, \omega_n, \varphi_1, \dots, \varphi_m$ be its dual basis.
By definition, we have that $\varphi_i(u) = 0$, for all $u \in U$ and all $i \in \{ 1, \dots, m \}$.

_Exercise 5_

This follows immediately from 3.76 and 3.95.

_Exercise 6_

_(a)_
Suppose $v_1, \dots, v_m$ spans $V$.
Let $\varphi, \psi \in V'$, such that $\Gamma(\varphi) = \Gamma(\psi)$.
We need to prove that $\varphi = \psi$.
By definition of $\Gamma$, we have

$$
\begin{aligned}
(\varphi(v_1), \dots, \varphi(v_m)) &= (\psi(v_1), \dots, \psi(v_m))\\\
\end{aligned}
$$

Hence $\varphi(v_j) = \psi(v_j)$ for $j = 1, \dots, m$.
By 2.31, it follows that $v_1, \dots, v_m$ contains a basis and then, by  the uniqueness part in 3.5, $\varphi$ and $\psi$ are equal.
Thus $\Gamma$ is injective.

Conversely, suppose $\Gamma$ is injective.
Let $U = \operatorname{span}(v_1, \dots, v_m)$ and suppose by contradiction that $U \neq V$.
By _Exercise 4_, there is a _non-zero_ linear functional $\varphi$ in $V'$ such that $\varphi(u) = 0$ for every $u \in U$.
We have $\Gamma(\varphi) = 0$, hence $\varphi \in \operatorname{null}\Gamma$.
But $\operatorname{null}\Gamma = \{0\}$ (since $\Gamma$ is injective), we get a contradiction.

_(b)_
Suppose $v_1, \dots, v_m$ is linearly independent.
We can extend it to a basis $v_1, \dots, v_m, u_1, \dots, u_n$ of $V$.
Let $x = (x_1, \dots, x_m)$ be any vector in $\mathbb{F^m}$.
Define $\varphi \in V'$ by

$$
\begin{aligned}
\varphi(v_j) &= x_j, \text{ for } j = 1, \dots, m\\\\
\varphi(u_j) &= 0, \text{ for } j = 1, \dots, n
\end{aligned}
$$

By 3.5 $\varphi$ is a well defined linear map.
And we have

$$
\begin{aligned}
\Gamma(\varphi) &= (\varphi(v_1), \dots, \varphi(v_m))\\\\
&= (x_1, \dots, x_m)\\\\
&= x
\end{aligned}
$$

Since $x$ was arbitrary, it follows that $\Gamma$ is surjective.

Conversely, suppose $\Gamma$ is surjective.
Let $U = \operatorname{span}(v_1, \dots, v_m)$.
We need to prove that $\operatorname{dim}U = m$.
We have

$$
\begin{aligned}
\operatorname{dim} U + \operatorname{dim} U^0 &= \operatorname{dim} V\\\\
&= \operatorname{dim} V'\\\\
&= \operatorname{dim} \operatorname{null} \Gamma + \operatorname{dim} \operatorname{range} \Gamma\\\\
&= \operatorname{dim} \operatorname{null} \Gamma + m
\end{aligned}
$$

Where the first equation follows from 3.106, the second from 3.95, the third from the Fundamental Theorem of Liner Maps and the fourth because $\Gamma$ is surjective.

Now it suffices to show that $\operatorname{dim} U^0 = \operatorname{dim} \operatorname{null} \Gamma$.

Suppose $\varphi \in U^0$.
Clearly $\varphi \in \operatorname{null} \Gamma$, thus $U^0 \subset \operatorname{null} \Gamma$.
To show the inclusion in the other direction, suppose $\varphi \in \operatorname{null} \Gamma$.
Let $u \in U$.
There are scalars $a_1, \dots, a_m$ such that $u = a_1 v_1 + \dots + a_m v_m$.
Thus

$$
\begin{aligned}
\varphi(u) &= \varphi(u = a_1 v_1 + \dots + a_m v_m)\\\\
&= a_1 \varphi(v_1) + \dots + a_m \varphi(v_m)\\\\
&= 0
\end{aligned}
$$

Since $u$ was arbitrary, we have $\varphi \in U^0$.
Hence $\operatorname{null} \Gamma \subset U^0$.
Therefore $U^0 = \operatorname{null} \Gamma$ and $\operatorname{dim} U^0 = \operatorname{dim} \operatorname{null} \Gamma$ as desired.

_Exercise 7_

We have that $\frac{d^j}{dx^j} x^k = \frac{k!}{(k-j)!} x^{k-j}$ for $k \ge j$ (this can easily be proven by induction on $j$, but I don't think that's really the point here).

Thus, if $k = j$, we have

$$
\begin{aligned}
\varphi_j(x^k) &= \varphi_j(x^j)\\\\
&= \frac{\frac{d^j}{dx^j} x^j \rvert_{x=0}}{j!}\\\\
&= \frac{\frac{j!}{(j-j)!} x^{j-j} \rvert_{x=0}}{j!}\\\\
&= \frac{j!}{j!}\\\\
&= 1
\end{aligned}
$$

And if $k > j$, we have

$$
\begin{aligned}
\varphi_j(x^k) &= \frac{\frac{d^j}{dx^j} x^k \rvert_{x=0}}{j!}\\\\
&= \frac{\frac{k!}{(k-j)!} x^{k-j} \rvert_{x=0}}{j!}\\\\
&= 0\\\\
\end{aligned}
$$

Clearly, if $k < j$ then $\frac{d^j}{dx^j} x^k = 0$.
Therefore

$$
\varphi_j(x^k) =
\begin{cases}
1, &\text{ if } j = k\\\\
0, &\text{ if } j \neq k
\end{cases}
$$

Which is the definition of dual basis.

_Exercise 8_

_(a)_
Suppose there are $a_1, \dots, a_m \in \mathbb{F}$ such that

$$
a_1 + a_2 (x - 5) + \dots + a_m (x - 5)^m = 0
$$

It is easy to see that, after expanding all terms, the only one containing $x^m$ is $a_m x^m$, therefore $a_m = 0$, since there is no other term containing $x^m$ to cancel it.
Thus

$$
0 = a_1 + a_2 (x - 5) + \dots + a_m (x - 5)^m = a_1 + a_2 (x - 5) + \dots + a_{m - 1} (x - 5)^{m - 1}
$$

The same argument can be used to show that all $a$'s are zero.
Hence $1, x - 5, \dots, (x - 5)^m$ is a linearly independent list of length $m + 1$.
But $\operatorname{dim} \mathcal{P_m}(\mathbb{R}) = m + 1$, therefore it also a basis of $\mathcal{P_m}(\mathbb{R})$.

_(b)_
Define $\varphi_0, \dots, \varphi_m$, where $\varphi_j(p) = \frac{p^{(j)}(5)}{j!}$.
By _Exercise 7_, this is the dual basis (just swap $x$ for $x-5$).

_Exercise 9_

Let $c_1, \dots, c_n \in \mathbb{F}$ such that

$$
\psi = c_1 \varphi_1 + \dots + c_n \varphi_n
$$

Therefore

$$
\psi(v_j) = c_1 \varphi_1(v_j) + \dots + c_n \varphi_n(v_j) = c_j
$$

Substituting this in the previous equation for each $j$ we get

$$
\psi = \psi(v_1) \varphi_1 + \dots + \psi(v_n) \varphi_n
$$

_Exercise 10_

Suppose $\psi \in W'$.
For the additive property, we have

$$
\begin{aligned}
(S + T)'(\psi) &= \psi \circ (S + T)\\\\
&= \psi \circ S + \psi \circ T\\\\
&= S'(\psi) + T'(\psi)
\end{aligned}
$$

Where the second equation follows from the distribuitve property of linear maps.
Hence $(S + T)' = S' + T'$.

For the scalar multiplication, let $v \in V$.
We have

$$
((\lambda T)'(\psi))(v) = (\psi \circ (\lambda T))(v) = \psi \circ T(\lambda v) = (T'(\psi))(\lambda v) = \lambda (T'(\psi))(v)
$$

Thus $(\lambda T)'(\psi) = \lambda T'(\psi)$ which implies $(\lambda T)' = \lambda T'$, as desired.

_Exercise 11_

Suppose that the rank of $A$ is 1.
We have that all the columns are multiples of each other.
Then $A$ can be written in the following form

$$
A = \begin{bmatrix}
c_1\\\\
\vdots\\\\
c_m
\end{bmatrix}
\begin{bmatrix}
d_1 & \dots & d_n
\end{bmatrix}
= \begin{bmatrix}
c_1 d_1 & \dots & c_1 d_n\\\\
\vdots & \ddots & \vdots\\\\
c_m d_1 & \dots & c_m d_n
\end{bmatrix}
$$

Where the first vector is a non-zero scalar multiple of a column in $A$ and the $d$'s are the corresponding scalars of each column such that $d_j$ times the first vector equals the $j$-th column of $A$.

Conversely, suppose there are $(c_1, \dots, c_m) \in F^m$ and $(d_1, \dots, d_n) \in F^n$ such that $A_{j,k} = c_j d_k$.
It is easy to see that $A$ takes the same previous form and thus each column is a scalar multiple of each other which implies that the rank of A is 1.

_Exercise 12_

Suppose that $I$ is the identity map on $V$ and $\varphi$ is any linear functional in $V'$.
We have

$$
I'(\varphi) = \varphi \circ I = \varphi
$$

As desired.

_Exercise 13_

_(a)_

$$
\begin{aligned}
T'(\varphi_1)(x, y, z) &= \varphi_1 \circ T(x, y, z)\\\\
&= \varphi_1(4x + 5y + 6z, 7x + 8y + 9z)\\\\
&= 4x + 5y + 6z
\end{aligned}
$$

$$
\begin{aligned}
T'(\varphi_2)(x, y, z) &= \varphi_2 \circ T(x, y, z)\\\\
&= \varphi_2(4x + 5y + 6z, 7x + 8y + 9z)\\\\
&= 7x + 8y + 9z
\end{aligned}
$$

_(b)_
Since $\psi_1(x, y, z) = x$, $\psi_2(x, y, z) = y$ and $\psi_3(x, y, z) = z$, substituting these in the results from item _(a)_, we get

$$
T'(\varphi_1)(x, y, z) = 4 \psi_1(x, y z) + 5 \psi_2(x, y, z) + 6 \psi_3(x, y, z)
$$

Thus $T'(\varphi_1) = 4 \psi_1 + 5 \psi_2 + 6 \psi_3$.
Similarly, we get $T'(\varphi_2) = 7 \psi_1 + 8 \psi_2 + 9 \psi_3$.

_Exercise 14_

_(a)_
Let $p \in \mathcal{P}(\mathbb{R})$.
Then

$$
\begin{aligned}
T'(\varphi)(p) &= \varphi \circ Tp\\\\
&= \varphi(x^2 p + p'')\\\\
&= (2xp + x^2p' + p'') \rvert_{x=4}\\\\
&= 8p(4) + 16p'(4) + p'''(4)
\end{aligned}
$$

_(b)_
$$
\begin{aligned}
(T'(\varphi))(x^3) &= \varphi \circ T(x^3)\\\\
&= \varphi(x^5 + 6x)\\\\
&= \int_0^1 x^5 + 6x \ dx\\\\
&= (\frac{x^6}{6} + 3x^2) \biggr\rvert_{0}^{1}
\end{aligned}
$$

_Exercise 15_

Suppose $T' = 0$.
Let $w \in \operatorname{range} T$.
Suppose by contradiction that $w \neq 0$.
By _Exercise 3_, there is a linear functional $\psi \in W'$ such that $\psi(w) = 1$.
Let $v$ be a vector in $V$ such that $Tv = w$.
We have

$$
T'(\psi)(v) = \psi \circ Tv = \psi(w) = 1
$$

But $T' = 0$, we have a contradiction.
Therefore $w = 0$.

Conversely, suppose $T = 0$.
Let $v \in V$ and $\psi \in W'$.
We have

$$
T'(\psi)(v) = \psi \circ Tv = \psi(0) = 0
$$

Since both $v$ and $\psi$ were arbitrary, we get that $T'$ must be zero.

_Exercise 16_

Let $T_1, \dots, T_n$ be a basis of $\mathcal{L}(V, W)$.
Define $R: \mathcal{L}(V, W) \to \mathcal{L}(W', V')$ by

$$
RT_j = T_j', \text{ for } j = 1, \dots, n
$$

Let $T \in \mathcal{L}(V, W)$ and $\psi \in W'$.
There are scalars $a_1, \dots, a_n$ such that $T = a_1 T_1 + \dots + a_n T_n$.
We have

$$
\begin{aligned}
(RT)\psi &= (R(a_1 T_1 + \dots + a_n T_n)) \psi\\\\
&= (a_1 R T_1 + \dots + a_n R T_n) \psi\\\\
&= (a_1 T_1' + \dots + a_n T_n') \psi\\\\
&= a_1 T_1' \psi + \dots + a_n T_n' \psi\\\\
&= \psi \circ (a_1 T_1) + \dots + \psi \circ (a_n T_n)\\\\
&= \psi \circ (a_1 T_1 + \dots + a_n T_n)\\\\
&= \psi \circ T\\\\
&= T'(\psi)
\end{aligned}
$$

Hence $R$ satisfies the desired property of taking $T$ to $T'$.
(I think showing the existence of $R$ like this wasn't necessary, since the question already presumes the existence of such map, but I kept it anyway)

We but need to prove that $\operatorname{dim} \operatorname{null} R = 0$, since $\mathcal{L}(V, W)$ and $\mathcal{L}(W', V')$ have the same dimension.
Suppose that $T \in \operatorname{null} R$.
We have that $0 = RT = T'$.
By _Exercise 15_, $T = 0$, therefore $\operatorname{null} R =  \{ 0 \}$ as desired.

_Exercise 17_

Because $\varphi(u) = 0$ for all $u \in U$ implies that $U \subset \operatorname{null} \varphi$.

_Exercise 18_

Suppose $U = \{0\}$.
By 3.106, we have that $\operatorname{dim} U^0 = \operatorname{dim} V = \operatorname{dim} V'$.
Since $U^0$ is a subspace of $V'$, it follows that $U^0 = V$.

Conversely, suppose $U^0 = V'$.
Using 3.016 again, it follows that $\operatorname{dim} U = 0$, hence $U = \{0\}$.

_Exercise 19_

$\Leftarrow$: Let $U^0 = \{0\}$. Let us prove that $U = V$. Suppose it is not true, so $U \neq V$, $U \subset V$. There exists basis of $U$ $u_1,...,u_n$, and it can be extended to the basis of $V$ with $v_1,...,v_m$, and $m > 0$ since $U \neq V$. Consider $\varphi \in V': \forall i \varphi(u_i) = 0$, and $\forall i \varphi(v_i) = 1$. Then, it is clear that $\varphi \in U^0$, but $\varphi \neq 0$ since for instance $\varphi(v_1) = 1 \neq 0$. But this contradicts to the condition $U^0 = \{0\}$, so the hypothesis was wrong and $U = V$.

$\Rightarrow$: let $U = V$. $U^0 = \{\varphi \in V': \varphi(u) = 0 \forall u \in U\}$. If $\varphi \in U^0$, it maps to 0 every vector in $U$, and hence any vector in $V$. By definition, $\varphi = 0$, and so in fact $U^0 = \{0\}$.

_Exercise 20_

Let $\varphi \in W^0$.
From _Exercise 17_, it follows that $W \subset \operatorname{null} \varphi$ and, since $U \subset W$, $U  \subset \operatorname{null} \varphi$.
Therefore $\varphi \in U^0$ and thus $W^0 \subset U^0$.

_Exercise 21_

We will prove the contrapositive.

Suppose that $U \not\subset W$.
Use the notation from _Theorem 1_ in Chapter 2 notes.
We have that $\psi_1 \in W^0$, but $\psi_1 \notin U^0$ (because of linear independence with the basis of $U^0$), hence $W^0 \not\subset U^0$.

_Exercise 22_

Suppose $\varphi \in (U + W)^0$.
Let $u \in U$ and $w \in W$.
By definition of sum of subspaces, we have that $u + w \in U + W$.
Thus

$$
\varphi(u + w) = 0
$$

Taking $u = 0$ implies that $\varphi \in W^0$.
Similarly, taking $w = 0$ implies that $\varphi \in U^0$.
Hence $\varphi \in U^0 \cap W^0$ and $(U + W)^0 \subset U^0 \cap W^0$.

To prove the inclusion in the other direction, suppose $\varphi \in U^0 \cap W^0$.
Let $v \in U + W$.
There are $u \in U$ and $w \in W$ such that $v = u + w$.
We have

$$
0 = 0 + 0 = \varphi(u) + \varphi(w) = \varphi(u + w) = \varphi(v)
$$

Since $v$ was arbitrary, $\varphi \in (U + W)^0$.
Hence $U^0 \cap W^0 \subset (U + W)^0$, as desired.

_Exercise 23_

Use the notation from _Theorem 1_ in Chapter 2 notes.

Extend $v_1, \dots, v_n, u_1, \dots, u_m, w_1, \dots, w_p$ to a basis $v_1, \dots, v_n, u_1, \dots, u_m, w_1, \dots, w_p, s_1, \dots, s_q$ of $V$.
Let $\varphi_1, \dots, \varphi_n, \psi_1, \dots, \psi_m, \omega_1, \dots, \omega_p, \sigma_1, \dots, \sigma_q$ be its dual basis.

We will prove $U^0 = \operatorname{span}(\omega_1, \dots, \omega_p, \sigma_1, \dots, \sigma_q)$.

We have

$$
\begin{aligned}
\operatorname{dim} U^0 &= \operatorname{dim} V - \operatorname{dim} U\\\\
&= n + m + p + q - (n + m)\\\\
&= p + q\\\\
\end{aligned}
$$

Where the first equation follows from 3.106. Therefore $\omega_1, \dots, \omega_p, \sigma_1, \dots, \sigma_q$ is a linearly independent list of length $\operatorname{dim}U^0$, in other words, a basis of $U^0$.
Similarly we can prove $W^0 = \operatorname{span}(\psi_1, \dots, \psi_m, \sigma_1, \dots, \sigma_q)$ and $(U \cap W)^0 = \operatorname{span}(\psi_1, \dots, \psi_m, \omega_1, \dots, \omega_p, \sigma_1, \dots, \sigma_q)$ and now we can see that $(U \cap W)^0 = U^0 + W^0$ by the definition of sum of subspaces.

_Exercise 24_

Let $u_1, \dots, u_m$ be a basis of $U$.
It can be extended to a basis $u_1, \dots, u_m, v_1, \dots, v_n$ of V.
Let $\psi_1, \dots, \psi_m, \varphi_1, \dots, \varphi_n$ be the dual basis.

Suppose $\varphi \in \operatorname{span}(\varphi_1, \dots, \varphi_n)$.
There are $a_1, \dots, a_n \in \mathbb{F}$ such that

$$
\varphi = a_1 \varphi_1 + \dots + a_n \varphi_n
$$

Let $u \in U$.
We have

$$
\varphi(u) = (a_1 \varphi_1 + \dots + a_n \varphi_n)(u) = 0
$$

Therefore $\varphi \in U^0$.
Hence $\operatorname{span}(\varphi_1, \dots, \varphi_n) \subset U^0$.

Now suppose $\varphi \in U^0$.
Because $\varphi \in V'$ there are $c_1, \dots, c_m, a_1, \dots, a_n \in \mathbb{F}$ such that

$$
\varphi = c_1 \psi_1 + \dots + c_m \psi_m + a_1 \varphi_1 + \dots + a_n \varphi_n
$$

For every $j \in \{ 1, \dots, m \}$, we have $\psi_j(u_j) = c_j$.
But $\varphi \in U^0$, that implies $c_j = 0$ and, hence, $\varphi \in \operatorname{span}(\varphi_1, \dots, \varphi_m)$.
Thus $U^0 \subset \operatorname{span}(\varphi_1, \dots, \varphi_m)$.

Since $\varphi_1, \dots, \varphi_m$ is linearly independent, $\operatorname{dim}(U^0) = m$.
We get

$$
\begin{aligned}
\operatorname{dim} V &= m + n\\\\
&= \operatorname{dim} U^0 + \operatorname{dim} U
\end{aligned}
$$

_Exercise 25_

Let $B = \{v \in V: \varphi(v) = 0 \text{ for every } \varphi \in U^0\}$.

Suppose that $u \in U$.
By definition, $\varphi(u) = 0$ for all $\varphi \in U^0$.
Thus $u \in B$ and, therefore, $U \subset B$.

For the inclusion in the other direction, we will prove the contrapositive.
Suppose that $v \notin U$.
Since $0 \in U$, it follows that $v \neq 0$.
Let $u_1, \dots, u_n$ be a basis of $U$.
We have that $v, u_1, \dots, u_n$ is a linearly indepedent list in $V$.
Extend it to a basis $v, u_1, \dots, u_n, v_1, \dots, v_m$ of $V$ and let $\varphi, \psi_1, \dots, \psi_n, \varphi_1, \dots, \varphi_m$ be its dual basis.
It is easy to see that $\varphi, \varphi_1, \dots, \varphi_m$ is a basis of $U^0$.
But $\varphi(v) = 1$, thus $v \notin B$.

By modus tollens, $v \in B$ implies $v \in U$.
Therefore $B \subset U$.

_Exercise 26_

Let $U$ be the subspace of $V$ such that

$$
U = \bigcap\limits_{\varphi \in \Gamma} \operatorname{null} \varphi
$$

We have that

$$
\begin{aligned}
U &= \{v \in V: v \in U\}\\
&= \{v \in V: v \in \bigcap\limits_{\varphi \in \Gamma} \operatorname{null} \varphi\}\\
&= \{v \in V: v \in \operatorname{null} \varphi \text{ for every } \varphi \in \Gamma\}\\
&= \{v \in V: \varphi(v) = 0 \text{ for every } \varphi \in \Gamma\}\\
\end{aligned}
$$

By _Exercise 25_, $\Gamma = U^0$.
Therefore

$$
\Gamma = U^0 = \{v \in V: \varphi(v) = 0 \text{ for every } \varphi \in \Gamma\}^0\\
$$

_Exercise 27_

We have

$$
\begin{aligned}
\operatorname{range} T &= \{p \in \mathcal{P_5}(\mathbb{R}): \psi(p) = 0 \text{ for every } \psi \in (\operatorname{range} T)^0\}\\
&= \{p \in \mathcal{P_5}(\mathbb{R}): \psi(p) = 0 \text{ for every } \psi \in \operatorname{null} T'\}\\
&= \{p \in \mathcal{P_5}(\mathbb{R}): \psi(p) = 0 \text{ for every } \psi \in \operatorname{span}(\varphi)\}\\
&= \{p \in \mathcal{P_5}(\mathbb{R}): \varphi(p) = 0\}\\
&= \{p \in \mathcal{P_5}(\mathbb{R}): p(8) = 0\}\\
\end{aligned}
$$

Where the first equation follows from _Exercise 25_ and the second from 3.107.

_Exercise 28_

Similarly to _Exercise 27_, we have

$$
\begin{aligned}
\operatorname{range} T &= \\{v \in V: \psi(v) = 0 \text{ for every } \psi \in (\operatorname{range} T)^0\\}\\\\
&= \\{v \in V: \psi(v) = 0 \text{ for every } \psi \in \operatorname{null} T'\\}\\\\
&= \\{v \in V: \psi(v) = 0 \text{ for every } \psi \in \operatorname{span}(\varphi)\\}\\\\
&= \\{v \in V: \varphi(v) = 0\\}\\\\
&= \\{v \in V: v \in \operatorname{null} \varphi\\}\\\\
&= \operatorname{null} \varphi
\end{aligned}
$$

_Exercise 29_

This is almost the same as _Exercise 28_.
Just use 3.109 instead.

_Exercise 30_

We have

$$
\begin{aligned}
\operatorname{dim}(\operatorname{null} \varphi_1 \cap \dots \cap \operatorname{null} \varphi_m) &= \operatorname{dim} V - \operatorname{dim}((\operatorname{null} \varphi_1 \cap \dots \cap \operatorname{null} \varphi_m)^0)\\\\
&= \operatorname{dim} V - \operatorname{dim}((\operatorname{null} \varphi_1)^0 + \dots + (\operatorname{null} \varphi_m)^0)\\\\
&= \operatorname{dim} V - \operatorname{dim}(\operatorname{span}(\varphi_1) + \dots + \operatorname{span}(\varphi_m))\\\\
&= \operatorname{dim} V - \operatorname{dim}(\operatorname{span}(\varphi_1, \dots, \varphi_m))\\\\
&= \operatorname{dim} V - m\\\\
\end{aligned}
$$

Where the first equation follows from 3.106, the second from _Exercise 23_, the third from _Theorem 1_ in Chapter 3 notes, the fourth from definition of sum of subspaces and the fifth because $\varphi_1, \dots, \varphi_m$ is linearly independent.

_Exercise 31_

By _Exercise 1_, all the $\varphi$'s are surjective. Consider the following process


* Step 1.

    Choose $v_1 \in V$ such that $\varphi_1(v_1) = 1$.

* Step j.

    If $j = n + 1$, stop the process.
    By the contrapositive of the statement in _Theorem 2_ of Chapter 3 notes, it follows that there is a vector $v_j \in V$ such that $v_j \in \bigcap_{1 \le k \le n, k \neq j}$ and $v_j \notin \operatorname{null} \varphi_j$.
    Because both these subspaces are closed under scalar multiplication and because $\varphi_j$ is surjective, we can assume without loss of generality that $\varphi_j(v_j) = 1$.

After step $n$ the process stops and we will have a list $v_1, \dots, v_n$ such that $\varphi_j(v_k) = 1$ if $j = k$ and $\varphi_j(v_k) = 0$ if $j \neq k$.
We but need to prove that $v_1, \dots, v_n$ is linearly independent, since it already has length $\operatorname{dim} V$.

Suppose there are $a_1, \dots, a_n \in \mathbb{F}$ such that

$$
a_1 v_1 + \dots + a_n v_n = 0
$$

Applying $\varphi_j$ to both sides of the equation above gives $a_j = 0$, for each $j = 1, \dots, n$. Hence $v_1, \dots, v_n$ is linearly independent and, therefore, a basis of $V$.

_Exercise 32_

$1 \Rightarrow 2, 3$: Suppose $T$ is invertible, then since $V$ is finite-dimensional, $T$ is injective and surjective. This implies, that $\operatorname{range}T = V$. On the other hand, $\operatorname{range}T = \operatorname{span}(Tv_1,...,Tv_n)$, and hence $V = \operatorname{span}(Tv_1,...,Tv_n)$. Since $\operatorname{dim}V = n$, all the vectors forming span should be independent, so indeed columns of $\mathcal{M}(T)$ are independent. 

$1 \implies 4$: since $\mathcal{M}(T)^T$ is the matrix of the dual map $T'$, and its range is equal to the range of $T$ and hence equal $n$, we conduct that columns of $\mathcal{M}(T)^T$ are linearly independent and span $\mathbb{F}^{n,1}$, which implies that rows of $\mathcal{M}(T)$ are linearly independent and span $\mathbb{F}^{1,n}$.

$5 \Rightarrow 1$: Finally, suppose that rows of $\mathcal{M}(T)$ span $F^{1,n}$. This means they are linearly independent, and this implies $T'\psi_1,...,T'\psi_n$ is linearly independent list in $V'$, where $\psi_1,...,\psi_n$ is dual basis to u_1,...,u_n. This means, that $\operatorname{range}T' = V'$, which implies $\operatorname{range}T = V$, and this means that $T$ is surjective hence invertible.

_Exercise 33_

Let $t \in \mathcal{L}(\mathbb{F}^{m,n}, \mathbb{F}^{n,m})$ denote the linear map that takes a matrix to its transpose.
For this exercise, assume $1 \le k \le m$ and $1 \le j \le n$.

Suppose $A, C \in \mathbb{F}^{m, n}$. Then

$$
\begin{aligned}
(t(A + C))\_{k, j} &= ((A + C)^T)\_{k, j}\\\\
&= (A + C)\_{j, k}\\\\
&= A\_{j, k} + C\_{j, k}\\\\
&= (A^T)\_{k, j} + (C^T)\_{k, j}\\\\
&= (t(A))\_{k, j} + (t(C))\_{k, j}\\\\
\end{aligned}
$$

Let $\lambda \in \mathbb{F}$. We have

$$
\begin{aligned}
(t(\lambda A))\_{k, j} &= ((\lambda A)^T)\_{k, j}\\\\
&= (\lambda A)\_{j, k}\\\\
&= \lambda (A\_{j, k})\\\\
&= \lambda (A^T)\_{k, j}\\\\
&= \lambda (t(A))\_{k, j}\\\\
\end{aligned}
$$

Therefore $t$ is indeed a linear map.

Since $\operatorname{dim}(\mathbb{F}^{m, n}) = \operatorname{dim}(\mathbb{F}^{n, m})$, to prove that $t$ is invertible we only need to show that it is injective.

Suppose $t(A) = 0$ for some $A \in F^{m,n}$ (here 0 denotes a matrix in $\mathbb{F}^{n, m})$ with 0 in all entries). We have that

$$
0 = (t(A))\_{k, j} = (A^T)\_{k, j} = A\_{j,k}
$$

Because $A$ has zero in all its entries, it follows that $A = 0$ and, therefore, $\operatorname{null} t = \\{ 0 \\}$, which implies that $t$ is injective.

_Exercise 34_

(a) 

1. It is clear, that $\Lambda 0 = 0$, because $ \forall \varphi \in \mathcal{L}(V, \mathbb{F}) (\Lambda 0)(\varphi) = \varphi(0) = 0$
2. $\forall \varphi \ \Lambda(v + u)(\varphi) = \varphi(v + u) = \varphi(v) + \varphi(u) = \Lambda v (\varphi) + \Lambda u(\varphi)$, so $\Lambda(v + u) = \Lambda v + \Lambda u$
3. $\forall \varphi \ \Lambda(\lambda v)(\varphi) = \varphi(\lambda v) = \lambda \varphi(v) = \lambda\Lambda v(\varphi)$, hence $\Lambda(\lambda v) = \lambda \Lambda v$

So, $\Lambda$ is indeed a linear map

(b) Let us prove that $T'' \circ \Lambda = \Lambda \circ T$.

This is rather simple, but for me personally it is a bit hard to imagine this entities without explicitely stating their types, so I will do it now.

$V': V \to \mathbb{F}$

$T': V' \to V' = (V \to \mathbb{F}) \to (V \to \mathbb{F})$

$V'': V' \to \mathbb{F} = (V \to \mathbb{F}) \to \mathbb{F}$

$T'': V'' \to V'' = (V' \to \mathbb{F}) \to (V' \to \mathbb{F}) = ((V \to \mathbb{F}) \to \mathbb{F}) \to ((V \to \mathbb{F}) \to \mathbb{F})$

Now, let us jump to the proof itself. $\forall v \in V$ we have

$$(T'' \circ \Lambda)(v) = T''(\Lambda v) = (\Lambda v)\circ T'$$
where the second equality comes from the definition of $T''$. This implies that $\forall v \in V, \forall \varphi \in V'$

$$
\begin{align}
((T'' \circ \Lambda)(v))(\varphi) &= ((\Lambda v)\circ T')(\varphi) \\
&= (\Lambda v)(T'(\varphi)) \\
&= (\Lambda v)(\varphi \circ T) \\
&= (\varphi \circ T)(v) \\
&= \varphi(Tv)
\end{align}
$$

On the other hand,

$$
\begin{align}
((\Lambda \circ T)(v))(\varphi) &= (\Lambda(Tv))(\varphi) = \varphi(Tv)
\end{align}
$$

So, since for every $\varphi, v$ the values are equal, we conclude, that the functions are equal.

(c) let $v, u \in V$ and $\Lambda u = \Lambda v$. Then $\forall \varphi \in V' \ (\Lambda v)(\varphi) = (\Lambda u)(\varphi) = \varphi(v) = \varphi(u)$. Suppose $v_1,...,v_n$ is a basis of $V$ and $\varphi_1,...,\varphi_n$ is the corresponding dual basis of $V'$. Then $v = \sum\limits_{i=1}^nc_iv_i$, $u = \sum\limits_{i=1}^nd_iv_i$. We have that $\varphi_i(v) = \varphi_i(u)$, hence $c_i = d_i$, and so $v = u$. Therefore, $\Lambda$ is injective.

We also have, that $\operatorname{dim}V'' = \operatorname{dim}(\mathcal{L}(V', \mathbb{F})) = 1\cdot\operatorname{dim}(V') = 1\cdot1\cdot \operatorname{dim}(V) = \operatorname{dim}V$. 

So, since $\operatorname{dim}V = \operatorname{dim}V''$ and $\Lambda$ is injective, it means that $\Lambda$ is isomorphism.

_Exercise 35_

Define $\tau \in \mathcal{L}((\mathcal{P}(\mathbb{R}))', \mathbb{R}^\infty)$ by

$$
\tau(\sigma) = (\sigma(1), \sigma(x), \sigma(x^2), \dots)
$$

You can check that $\tau$ is indeed linear.
To prove $\tau$ is injective, suppose there are $\sigma, \eta \in (\mathcal{P}(\mathbb{R}))'$ such that $\tau(\sigma) = \tau(\eta)$.
By definition of $\tau$ we have that $\sigma(x^j) = \eta(x^j)$.
Let $p \in \mathcal{P}(\mathbb{R})$.
Clearly $p$ takes the form

$$
p(x) = a_0 + a_1 x + \dots + a_m x^m
$$

For some $a_0, \dots, a_m \in \mathbb{F}$ where $\deg p = m$. Then

$$
\begin{aligned}
\sigma(p) &= \sigma(a_0 + a_1 x + \dots + a_m x^m)\\\\
&= \sigma(a_0) + \sigma(a_1 x) + \dots + \sigma(a_m x^m)\\\\
&= a_0 \sigma(1) + a_1 \sigma(x) + \dots + a_m \sigma(x^m)\\\\
&= a_0 \eta(1) + a_1 \eta(x) + \dots + a_m \eta(x^m)\\\\
&= \eta(a_0) + \eta(a_1 x) + \dots + \eta(a_m x^m)\\\\
&= \eta(a_0 + a_1 x + \dots + a_m x^m)\\\\
&= \eta(p)\\\\
\end{aligned}
$$

Because $p$ was arbitrary, it follows that $\sigma = \eta$ and thus $\tau$ is injective.

To prove surjectivity, let $a = (a_0, a_1, a_2, \dots)\in \mathbb{R}^\infty$.
Define $\sigma \in (\mathcal{P}(\mathbb{R}))'$ by

$$
\sigma(x^n) = a_n
$$

You can check that $\sigma$ is also linear.
By definition of $\tau$ we have that $\tau(\sigma) = a$ and, because $a$ was arbitrary, it follows that $\tau$ is surjective.

Hence $\tau$ is an isomorphism between $(\mathcal{P}(\mathbb{R}))'$ and $\mathbb{R}^\infty$.

_Exercise 36_

_(a)_
We have

$$
\begin{aligned}
\operatorname{null} i' &= \{\varphi \in V': i'(\varphi) = 0\}\\\\
&= \{\varphi \in V': i'(\varphi)(u) = 0 \text{ for every } u \in U\}\\\\
&= \{\varphi \in V': \varphi \circ i(u) = 0 \text{ for every } u \in U\}\\\\
&= \{\varphi \in V': \varphi(u) = 0 \text{ for every } u \in U\}\\\\
&= \{\varphi \in V': \varphi \in U^0\}\\\\
&= U^0\\\\
\end{aligned}
$$

_(b)_

$\forall u \in U, \varphi \in U' i'(\varphi)(u) = \varphi(i(u)) = \varphi(u)$, hence $i'(\varphi) = \varphi$. So, $U' = \operatorname{range}i'$.

_(c)_

Suppose $\varphi, \psi \in V'$, and $\tilde{i'}(\varphi + U^0) = \tilde{i'}(\psi + U^0)$. This means, that $i'(\varphi) - i'(\psi) \in U^0$, which implies $\forall u \in U\ i'(\varphi)(u) - i'(\psi)(u) = 0$, which means that $\forall u \in U\ \varphi(i(u)) - \psi(i(u)) = 0$, which means that $\forall u \in U \ \varphi(u) - \psi(u) = 0$, and so $\varphi - \psi \in U^0$, which means that $\varphi + U^0 = \psi + U^0$ holds in $V/U^0$. So, $\tilde{i'}$ is injective. 

We also can verify that $\operatorname{dim}V'/U^0 = \operatorname{dim}V' - \operatorname{dim}U^0 = \operatorname{dim}V' - (\operatorname{dim}V - \operatorname{dim}U^0) = \operatorname{dim}U^0$.

So, $\tilde{i'}$ is isomorphism.

_Exercise 37_

_(a)_

By definition, $\pi$ is injective, so $\pi'$ is surjective.

_(b)_

We know that $\operatorname{range}\pi' = (\operatorname{null} \pi)^0$, hence we need to prove, that $U = (\operatorname{null}\pi)$, and this is obviously true.

_(с)_

$\operatorname{dim}\operatorname{range}\pi' = \operatorname{dim}U^0 = \operatorname{dim}V - \operatorname{dim}U$, and $\operatorname{dim}(V/U)' = \operatorname{dim}(V/U) = \operatorname{dim}V - \operatorname{U}$, and hence $\pi'$ is injective, we can conclude, that it is isomirphism.