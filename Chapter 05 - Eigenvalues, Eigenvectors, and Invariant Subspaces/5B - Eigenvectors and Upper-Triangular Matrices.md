Chapter 5: **Eigenvalues, Eigenvectors and Invariant Subspaces**

**5.B**

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

_Exercise 1_

_(a)_
We will prove the contrapositive.

Suppose $I - T$ is not invertible.
There exists non-zero $v \in V$ such that $Iv - Tv = 0$, which implies $Tv = v$.
Applying $T$ to both sides of this last equation, yields $TTv = Tv = v$.
Continuing this, we see that for any positive integer $n$, $T^n v = v$.
Therefore $T^n$ can never be $0$.

Now suppose $T^n = 0$.
We have

$$
\begin{aligned}
(I - T)(I + T + \dots + T^{n-1}) &= (I - T) \sum\limits_{k=0}^{n-1} T^k\\\\
&= \sum\limits_{k=0}^{n-1} T^k - \sum\limits_{k=0}^{n-1} T^{k + 1}\\\\
&= I + \sum\limits_{k=1}^{n-1} T^k - \sum\limits_{k=1}^n T^k\\\\
&= I + \sum\limits_{k=1}^{n-1} T^k - T^n - \sum\limits_{k=1}^{n-1} T^k\\\\
&= I - T^n\\\\
&= I\\\\
\end{aligned}
$$

Therefore $I - T$ is an inverse of $I + T + \dots + T^{n-1}$, which implies the desired result.

_(b)_
I wouldn't.

We know, that $(1 - x^n) = (1 - x)(1 + x + ... + x^{n-1})$. If we consider this as polynomial over $\mathcal{L}(V)$, and substitute $T$, we get $I = (I - T)(I + T + ... + T^{n-1})$.

_Exercise 2_

Suppose $\lambda$ is an eigenvalue of $T$ and $v$ a corresponding eigenvector.
Then

$$
\begin{aligned}
0 &= (T - 2I)(T - 3I)(T - 4I)v\\\\
&= (T^3 - 9T^2 + 26T - 24I)v\\\\
&= T^3 v - 9T^2 v + 26T - 24v\\\\
&= \lambda^3 v - 9\lambda^2 v + 26\lambda v - 24v\\\\
&= (\lambda^3 - 9\lambda^2 + 26\lambda - 24)v\\\\
\end{aligned}
$$

Therefore, because $v \neq 0$, $\lambda^3 - 9\lambda^2 + 26\lambda + 24 = 0$.
But we can factor this to $(\lambda - 2)(\lambda - 3)(\lambda - 4) = 0$.
Thus $\lambda$ is either $2$, $3$ or $4$.

_Exercise 3_

Let $v \in V$.
Then

$$
0 = (T^2 - I^2)v = (T + I)(T - I)v
$$

which implies $(T - I)v \in \operatorname{null} (T + I)$.
We but need to prove that $T + I$ is injective and we will have $Tv = v$.
Let $u, w \in V$ such that $(T + I)u = (T + I)w$.
Then $Tu + u = Tw + w$ which implies $T(u - w) = w - u = -1(u - w)$.
But $-1$ is not an eigenvalue of $T$, thus $u - w = 0$, implying $u = w$, as desired.

_Exercise 4_

Suppose $v \in V$.
We have $v = (I - P)v + Pv$.
Because $P - P^2 = 0$, it follows that $P(I - P)v = 0$.
Therefore $(I - P)v \in \operatorname{null} P$.
Obviously $Pv \in \operatorname{range} P$, thus $v \in \operatorname{null} P + \operatorname{range} P$ and we have $V \subset \operatorname{null} P + \operatorname{range} P$.
The inclusion in the opposite direction is clearly true, therefore $V = \operatorname{null} P + \operatorname{range} P$.

To see why this is a direct sum, suppose $u \in \operatorname{null} P \cap \operatorname{range} P$.
Because $u \in \operatorname{range} P$, there exists $w$ such that $Pw = u$.
But $u \in \operatorname{null} P$, so we must have

$$
0 = Pu = P^2 w = Pw = u
$$

Therefore $\operatorname{null} P \cap \operatorname{range} P = \{0\}$ and by 1.45 it is direct sum.

_Exercise 5_

Note that, for non-negative $k$, $(STS^{-1})^k = ST^kS^{-1}$, because the $S$'s and $S^{-1}$'s cancel out (this can easily me proven by induction on $k$).
Let $n = \deg p$ and $a_0, a_1, \dots, a_n \in \mathbb{F}$ be the coefficients of $p$.
Then

$$
\begin{aligned}
p(STS^{-1}) &= \sum\limits_{k=0}^n a_k(STS^{-1})^k\\\\
&= \sum\limits_{k=0}^n a_k S T^k S^{-1}\\\\
&= S(\sum\limits_{k=0}^n a_k T^k)S^{-1}\\\\
&= Sp(T)S^{-1}\\\\
\end{aligned}
$$

_Exercise 6_

It is easy to see that $T^k u \in U$ for $u \in U$ and non-negative $k$ (this can easily be proven by induction on $k$).
Since $p(T)u$ is a sum of terms like this, multiplied by the coefficients of $p$, and $U$ is closed under addition and scalar multiplication, then $p(T)u \in U$.

_Exercise 7_

Suppose $9$ is an eigenvalue of $T^2$.
Let $v$ be a corresponding eigenvector.
Then $(T^2 - 9I)v = 0$, which implies $(T - 3I)(T + 3I)v = 0$.
If $(T + 3I)v = 0$ then $-3$ is an eigenvalue of $T$.
Otherwise, $(T + 3I)v$ is an eigenvector of $T$ and $3$ is a corresponding eigenvalue.

Conversely, suppose $\pm 3$ is an eigenvalue of $T$.
Let $v$ be a corresponding eigenvector.
Then $T^2 v = T(\pm 3v) = (\pm 3)^2 v = 9v$, showing that $9$ is an eigenvalue of $T^2$.

_Exercise 8_

Define $T \in \mathcal{L}(\mathbb{R}^2)$ by

$$
T(x, y) = \frac{1}{\sqrt{2}}(x - y, x + y)
$$

Then, for $(a, b) \in \mathbb{R}^2$, we have

$$
\begin{aligned}
T^4 (a, b) &= \frac{1}{\sqrt{2}} T^3 (a - b, a + b)\\\\
&= \frac{1}{2} T^2 (-2b, 2a)\\\\
&= \frac{1}{2\sqrt{2}} T (-2a - 2b, 2a - 2b)\\\\
&= \frac{1}{4}(-4a, -4b)\\\\
&= -(a, b)\\\\
\end{aligned}
$$

_Exercise 9_

Let $c(z - \lambda_n) \dotsm (z - \lambda_1)$ be a factorization of $p$.
Then $c(T - \lambda_n I) \dotsm (T - \lambda_1 I)$ is a factorization of $p(T)$.
Since $p$ is the polynomial of smallest degree such that $p(T)v = 0$, it follows that $(T - \lambda_j I) \dotsm (T - \lambda_1 I)v \neq 0$, for $j < n$.
Therefore, we have that $(T - \lambda_{n - 1} I) \dotsm (T - \lambda_1 I)v \neq 0$ is an eigenvector of $T$ and $\lambda_n$ the corresponding eigenvalue.
Note that, by 5.20, the order of factorization can be changed, placing any other factor $(T - \lambda_j)$ in the beginning. This implies that all $\lambda$'s are indeed eigenvalues of $T$.

_Exercise 10_

Note that $T^k v = \lambda^k v$.
Let $n = \deg p$ and $a_0, a_1, \dots, a_n \in \mathbb{F}$ be the coefficients of $p$.
Then

$$
\begin{aligned}
p(T)v &= (\sum\limits_{k=0}^n a_k T^k)v\\\\
&= \sum\limits_{k=0}^n a_k T^k v\\\\
&= \sum\limits_{k=0}^n a_k \lambda^k v\\\\
&= (\sum\limits_{k=0}^n a_k \lambda^k) v\\\\
&= p(\lambda) v\\\\
\end{aligned}
$$

_Exercise 11_

Suppose $\alpha$ is an eigenvalue of $p(T)$.
Let $c(z - \lambda_1) \dotsm (z - \lambda_n)$ be a factorization of $p(z) - \alpha$.
We have

$$
p(T) - \alpha I = c(T - \lambda_1 I) \dotsm (T - \lambda_n I)
$$

Because $p(T) - \alpha I$ is not injective, it follows that, for some $j$, $T - \lambda_j I$ is not injective.
Therefore $\lambda_j$ is an eigenvalue of $T$.
Since $\lambda_j$ is a root of $p(z) - \alpha$, we have that $p(\lambda_j) = \alpha$.

The converse is the same as _Exercise 10_.

_Exercise 12_

Define $T \in \mathcal{L}(\mathbb{R}^4)$ by

$$
T(x_1, x_2, x_3, x_4) = (x_2, x_3, x_4, -x_1)
$$

Let $p \in \mathcal{P}(R)$ such that $p(x) = x^4$.
Then $-1$ is an eigenvalue of $p(T)$, but $p$ is always positive, therefore no eigenvalue $\lambda$ of $T$ satisfies $p(\lambda) = -1$.

_Exercise 13_

By 5.21, $W$ is either $\{0\}$ or infinite-dimensional.
Let $U$ be a subspace of $W$ invariant under $T$.
Then $T\rvert_U$ also has no eigenvalues.
But $T\rvert_U$ is also an operator on a complex vector space, therefore $U$ is either $\{0\}$ or infinite-dimensional.

_Exercise 14_

Suppose $V$ is finite-dimensional vector space.
Let $v_1, \dots, v_n$ be a basis of $V$.
Define $T \in \mathcal{L}(V)$ by

$$
\begin{aligned}
Tv_j &= v_{j+1}, \text{ for } j = 1, \dots, n - 1\\\\
Tv_n &= v_1\\\\
\end{aligned}
$$

$T$ is clearly invertible, but $\mathcal{M}(T)$ with respect to same basis only has zeros in the diagonal.

_Exercise 15_

Suppose $V$ is finite-dimensional vector space.
Let $v_1, \dots, v_n$ be a basis of $V$.
Define $T \in \mathcal{L}(V)$ by

$$
Tv_j = v_1 + \dots + v_n
$$

$\mathcal{M}(T)$ contains $1$'s in all its entries, but $T$ is clearly not inveritible.

_Exercise 16_

Let $n = \operatorname{dim} V$.
Define $\Psi \in \mathcal{L}(\mathcal{P}_n(\mathbb{C}), V)$ by

$$
\Psi(p) = (p(T))v
$$

for $p \in \mathcal{P}_n(\mathbb{C})$.
One can easily verify that $\Psi$ is linear.
Since $\operatorname{dim} \mathcal{P}_n(\mathbb{C}) > \operatorname{dim} V$, by 3.23, there exists $p \in \mathcal{P}_n(\mathbb{C})$ such that $0 = \Psi(p) = (p(T))v$.
The rest follows exactly as 5.21.

_Exercise 17_

This is almost the same as _Exercise 16_.

_Exercise 18_

Note that $f$ can only output integer values.
Thus, if $f$ is not constant, there will be a jump discontinuity at some point.
We will prove $f$ is not constant.

If $T$ is invertible, then the existence of an eigenvalue of $T$ (guaranteed by 5.21) implies that $T - \lambda I$ is not surjective for some $\lambda \in \mathbb{F}$.
Hence $f(0) = \operatorname{dim} \operatorname{range} T > \operatorname{dim} \operatorname{range} (T - \lambda I) = f(\lambda)$.

If $T$ is not invertible, choose $\lambda$ such that it is not an eigenvalue of $T$.
Then, for any non-zero $v \in V$, $(T - \lambda I)v \neq 0$, showing that $T - \lambda I$ is injective and, therefore, surjective.
Hence $f(0) = \operatorname{dim} \operatorname{range} T < \operatorname{dim} \operatorname{range} (T - \lambda I) = f(\lambda)$.

_Exercise 19_

5.20 implies that any two operators in $\{p(T): p \in \mathcal{P}(\mathbb{F})\}$ commute.
But this is obviously not true for $\mathcal{L}(V)$, because $\operatorname{dim} V > 1$.
For example, let $v_1, \dots, v_n$ be a basis of $V$.
Define $S, R \in L(V)$ by

$$
\begin{aligned}
Sv_1 &= v_2, Sv_j = 0 \text{ for } j = 2, \dots, n\\\\
Rv_1 &= 0, Rv_j = v_j \text{ for } j = 2, \dots, n.
\end{aligned}
$$

Then $SRv_1 = 0$ but $RSv_1 = v_2$.
Thus $SR \neq RS$.

_Exercise 20_

This follows directly from 5.27 and 5.26.
