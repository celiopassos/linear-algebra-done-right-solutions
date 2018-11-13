Chapter 5: **Eigenvalues, Eigenvectors and Invariant Subspaces**

**5.A**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [x] Exercise 5
- [x] Exercise 6
- [x] Exercise 7
- [x] Exercise 8
- [ ] Exercise 9
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
- [ ] Exercise 24
- [x] Exercise 25
- [x] Exercise 26
- [x] Exercise 27
- [x] Exercise 28
- [x] Exercise 29
- [ ] Exercise 30
- [x] Exercise 31
- [x] Exercise 32
- [ ] Exercise 33
- [ ] Exercise 34
- [ ] Exercise 35
- [ ] Exercise 36

_Exercise 1_

_(a)_
Suppose $u \in U$.
Because $Tu = 0$ and $0 \in U$, it follows that $U$ is invariant under $T$.

_(b)_
Suppose $u \in U$.
By defitinion $Tu \in \operatorname{range} T$.
But $\operatorname{range} T \subset U$, hence $Tu \in U$.

_Exercise 2_

Suppose $v \in \operatorname{null} S$.
Since $STv = TSv = 0$, it follows that $Tv \in \operatorname{null} S$.

_Exercise 3_

Suppose $w \in \operatorname{range} S$.
There exists $v \in V$ such that $Sv = w$.
Then $Tw = TSv = STv \in \operatorname{range} S$.

_Exercise 4_

Suppose $u \in U_1 + \dots + U_m$.
There are $u_1 \in U_1, \dots, u_M \in U_m$ such that

$$
u = u_1 + \dots + u_m
$$

But

$$
Tu = Tu_1 + \dots + Tu_m.
$$

Because, for each $j = 1, \dots, m$, $U_j$ is invariant under $T$, it follows that $Tu_j \in U_j$.
Therefore $Tu \in U_1 + \dots + U_m$.

_Exercise 5_

Suppose $U_1, \dots, U_m$ are subspaces of $V$ invariant under $T$.
Let $u \in U_1 \cap \dots \cap U_m$.
For each $j = 1, \dots, m$, because $U_j$ is invariant under $T$ and $u \in U_j$, it follows that $Tu \in U_j$.
Therefore $Tu \in U_1 \cap \dots \cap U_m$.

_Exercise 6_

The statement is true.
We will give a prove of the contrapositive.

Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$ such that $U$ is neither $\\{0\\}$ or $V$.
Let $u \in U$ and $v \in V$ such that $u$ is non-zero and $v \notin U$.
Choose any operator $T \in \mathcal{L}(V)$ that maps $u$ to $v$.
Clearly $U$ is not invariant under $T$.

_Exercise 7_

Taking $\lambda (x, y) = (-3y, x)$ gives $\lambda x = -3y$ and $\lambda y = x$.
It follows that $y \neq 0$, because otherwise $x$ would be $0$ and we're not looking for the $0$ vector.
Substituting $x$ in first equation, we get $\lambda^2 y = -3y$.
Diving by $y$ on both sides we have that $\lambda = i\sqrt{3}$ or $\lambda = -i\sqrt{3}$.
Since we're working on $\mathbb{R}^2$, it follows that there are no eigenvalues.
Consider $\mathbb{C}^2$ instead.
To prove $i\sqrt{3}$ is indeed an eigenvalue, choose any vector of the form $(i\sqrt{3}x, x)$.
Then

$$
T(i\sqrt{3}x, x) = (-3x, i\sqrt{3}x) = i\sqrt{3}(i\sqrt{3}x, x).
$$

For $-i\sqrt{3}$, consider the vectors of the form $(x, -i\frac{\sqrt{3}}{3}x)$.
Then

$$
T(x, -i\frac{\sqrt{3}}{3}x) = (i\sqrt{3}x, x) = i\sqrt{3} (x, -i\frac{\sqrt{3}}{3}x).
$$

Since $\operatorname{dim} \mathbb{C}^2 = 2$, there are only two eigenvalues.

_Exercise 8_

With the usual procedure, we find that $\lambda = 1$ or $\lambda = -1$ and it is easy to verify that both are eigenvalues and corresponing eigenvectors are $(1, 1)$ and $(1, -1)$.

_Exercise 10_

_(a)_
The eigenvalues are $1, \dots, n$ and their corresponding eigenvectors are the vectors in the standard basis of $\mathbb{F}^n$.

_(b)_
We claim that all subspaces invariant under $T$ are spans of vectors in the standard basis.

Suppose $U$ is an invariant subspace of $T$ and $v = \sum_{k=1}^m a_{i_k}e_{i_k} \in U$, where $i_1 < \cdots < i_m$ and all $a_{i_k}$'s are nonzero.
We will show that $e_{i_k} \in U$ for each $k$.
First, all is clear if $m = 1$, so suppose $m > 1$.
Note that
$$
Tv - i_1v = \sum_{k=2}^m a_{i_k}(i_k - i_1)e_{i_k} \in \operatorname{span}(e_{i_2}, \cdots, e_{i_m}).
$$
Also, $Tv - i_1v \in U$ because $v \in U$ and $U$ is a subspace.
Moreover, the coefficients in the sum above are all nonzero.
Repeating this $m-1$ times (subtracting $i_2(Tv-i_1v)$ from $Tv-i_1v$, ...), we're left with a nonzero vector in $\operatorname{span}(e_{i_m})$ which is also in $U$.
In particular, $e_{i_m} \in U$, so $v - a_{i_m}e_{i_m} \in U$.
Repeating again with this last vector, we find that $e_{i_{m-1}} \in U$.
Continuing like this, we see that $e_{i_k} \in U$ for all $k$.

Now, we have $\operatorname{span}(e_{i_1}, \dots, e_{i_m}) \subseteq U$.
If this inclusion is not an equality, we can find another vector $w \in U$ which is not in the span of the $e_{i_k}$'s.
Writing $w$ as a linear combination of vectors in the standard basis, we can find an integer $j$, distinct from all the $i_k$, such that the coefficient of $e_j$ is nonzero.
Thus, if we repeat the previous procedure with $w$ instead of $v$, we see that $e_j \in U$, so $\operatorname{span}(e_{i_1}, \dots, e_{i_m}, e_j) \subseteq U$.
If this inclusion is still not an equality, we can repeat this last procedure again and add another basis vector to the $\operatorname{span}$.
Each time the dimension increases by $1$.
Since $U$ is finite-dimensional, we must have equality at the some point.

_Exercise 11_

Since degree of a polynomial always decreases after applying $T$, the polynomials $p$ with $\deg p \ge 1$ can never be eigenvalues.
If $\deg p = 0$ (i.e. $p$ is a constant), then $Tp = 0$, so the only eigenvalue of $T$ is $0$.

_Exercise 12_

For each $j \in \\{0, 1, 2, 3, 4\\}$, we have that $j$ is an eigenvalue and all vectors in $\operatorname{span}(x^j)$ are corresponding eigenvectors.

_Exercise 13_

Choose $\alpha$ such that it is not an eigenvalue of $T$ and $\left| \alpha - \lambda \right| < \frac{1}{1000}$.
This $\alpha$ exists because there are infinite values of $\alpha$ satisfying such inequality, but only finitely many eigenvalues, because $V$ is finite-dimensional.
Then, suppose $v \in \operatorname{null}(T - \alpha I)$.
That means $Tv = \alpha Iv = \alpha v$. But $\alpha$ is not an eigenvalue of $T$. Therefore $v$ must be the $0$ vector, proving $T - \alpha I$ is injective.

_Exercise 14_

Suppose $\lambda$ is eigenvalue of $P$.
It follows that $u = \lambda(u + w)$ for some $u \in U$ and $w \in W$.
Thus $(1 - \lambda)u = \lambda w$.
Since $U + W$ is direct sum, that is $U \cap W = \\{0\\}$, if $u \neq 0$, then $w = 0$, implying $\lambda = 1$.
Similarly, if $w \neq 0$, then $u = 0$, implying $\lambda = 0$.
Hence $0$ and $1$ are only eigenvalues and $U$ and $W$, respectively, are the corresponding eigenvectors.

_Exercise 15_

_(a)_
Suppose $\lambda$ is an eigenvalue of $T$ and $v$ a corresponding eigenvector.
Then

$$
S^{-1}TS(S^{-1}v) = S^{-1}Tv = S^{-1}(\lambda v) = \lambda S^{-1}v.
$$

Hence $\lambda$ is an eigenvalue of $S^{-1}TS$ and $\operatorname{span}(S^{-1}v)$ a corresponding eigenvector.

_(b)_
If $v$ is an eigenvector of $T$, then $S^{-1}v$ is an eigenvector of $S^{-1}TS$ and if $v$ is an eigenvector of $S^{-1}TS$, then $Sv$ is an eigenvector of $T$.

_Exercise 16_

Suppose $\lambda$ is and eigenvalue of $T$ and $v$ a corresponding eigenvector.
Let $v_1, \dots, v_n$ be a basis of $V$ with respect to which $\mathcal(T)$ has only real entries.
We have that $\lambda = a + bi$ for some $a, b \in \mathbb{R}$.
Thus

$$
Tv = \lambda v = av + biv.
$$

_Exercise 17_

Let $v_1, \dots, v_4$ be a basis of $\mathbb{R}^4$.
Define $T$ by

$$
\begin{aligned}
Tv_1 &= iv_1\\\\
Tv_2 &= (1 + i)v_2\\\\
Tv_3 &= (\pi - i)v_3\\\\
Tv_4 &= (\sqrt{2} + i)v_4.
\end{aligned}
$$

Hence $T$ has $4$ non-real eigenvalues.
Since $\operatorname{dim} \mathbb{R}^4 = 4$, $T$ has no other eigenvalues.

_Exercise 18_

Suppose $(z_1, z_2, \dots) \in C^\infty$ and $\lambda \in \mathbb{F}$ are such that

$$
T(z_1, z_2, \dots) = \lambda(z_1, z_2, \dots).
$$

Therefore $\lambda z_{k+1} = z_k$ for each positive $k$.
Because $\lambda z_1 = 0$, if $\lambda = 0$, by the previous equation it follows that each $z_k = 0$ and, if $\lambda \neq 0$, then $z_1 = 0$ and by the previous equation $z_{k+1} = 0$.
Hence all $z$'s are $0$ and $T$ has no eigenvalues.

_Exercise 19_

Suppose $\lambda$ is an eigenvalue of $T$.
Then

$$
\lambda(x_1, \dots, x_n) = (x_1 + \dots + x_n, \dots, x_1 + \dots + x_n).
$$

That implies $x_k = \frac{1}{\lambda}(x^1 + \dots + x_n)$ for each $k = 1, \dots, n$.
Hence all the $x$'s are equal.
Therefore $\lambda = n$ and the corresponding eigenvectors are those which all entries equal to each other.
Since every eigenvector of $T$ must satisfy such property and eigenvectors corresponding to distinct eigenvalues are linearly independent, it follows that $T$ has no other eigenvalues.

_Exercise 20_

Suppose $\lambda$ is an eigenvalue of $T$.
Then

$$
\lambda(z_1, z_2, z_3, \dots) = (z_2, z_3, \dots),
$$

which means that $z_k = \frac{1}{\lambda} z_{k+1}$.
But $z_{k+1} = \frac{1}{\lambda} z_{k+2}$.
It easy to see (and easily proven by induction) that $z_k = (\frac{1}{\lambda})^{n-k} z_n$ or $z_n = \lambda^{n-k} z_k$.
Choose $k = 1$ and we have a formula for any geometric sequence.
Hence all real numbers are eigenvalues of $T$ and any of their respective geometric sequences are the corresponding eigenvectors.

_Exercise 21_

_(a)_
Suppose $\lambda$ is an eigenvalue of $T$ and $v$ a corresponding eigenvector.
Then, applying $T^{-1}$ to both sides of $Tv = \lambda v$, we get $v = \lambda T^{-1}v$. Dividing both sides by $\lambda$ shows that $\frac{1}{\lambda}$ is indeed an eigenvalue of $T^{-1}$.
The converse is basically the same.

_(b)_
The previous item also showed that if $v$ is an eigenvalue of $T$ it must be an eigenvalue of $T^{-1}$ too.

_Exercise 22_

If $w = -v$, then clearly $-3$ is an eigenvalue of $T$.
If $w \neq -v$, then $v + w \neq 0$ and

$$
T(v + w) = Tv + Tw = 3w + 3v = 3(v + w).
$$

Hence $3$ is an eigenvalue of $T$.


_Exercise 23_

Suppose $\lambda$ is an eigenvalue of $ST$ and $v$ a corresponding eigenvector.
Then $STv = \lambda v$.
Applying $T$ to both sides, we have

$$
TS(Tv) = T(\lambda v) = \lambda Tv.
$$

If $Tv \neq 0$, then $\lambda$ is indeed an eigenvalue of $TS$.

If $Tv = 0$, then $\lambda = 0$.
Because $\operatorname{dim} \operatorname{null} T \ge 1$ (since $v$ is non-zero), it follows that $\operatorname{dim} \operatorname{null} TS \ge 1$, hence there is a vector $u \in \operatorname{null} TS$, with $u \neq 0$, such that $TSu = 0 = \lambda u$.

_Exercise 24_

_(a)_
It is easy to see that $\mathcal{M}(T, e_1, \dots, e_n) = A$.
Thus

$$
Te_k = \sum_{j=1}^n A_{j,k}e_j.
$$

and then

$$
\begin{aligned}
T(e_1 + \dots + e_n) &= \sum_{j=1}^n A_{j,1}e_j + \dots + \sum{j=1}^n A_{j, n}e_j\\\\
&= \left(\sum_{j=1}^n A_{1,j}\right)e_1 + \dots + \left(\sum_{j=1}^n A_{n,j}\right)e_n\\\\
&= e_1 + \dots + e_n.
\end{aligned}
$$

Hence $e_1 + \dots + e_n$ is an eigenvector of $T$ corresponding to the eigenvalue $1$.

_Exercise 25_

If $u$ and $w$ are linearly dependent, then they obviously correspond to the same eigenvalues.
Assume $u, w$ are linearly independent.
Let $\alpha, \beta, \lambda$ be eigenvalues of $T$ with corresponding vectors $u, v, u + w$, respectively.
Then

$$
\alpha u + \beta w = Tu + Tw = T(u + w) = \lambda (u + w) = \lambda u + \lambda w,
$$

which implies that $(\alpha - \lambda)u = (\lambda - \beta)w$.
Since $u, w$ are linearly independent, it follows that their coefficients are $0$.
Thus $\lambda = \alpha = \beta$.

_Exercise 26_

By _Exercise 25_, $T$ only has one eigenvalue.
Call it $\lambda$.
Let $v \in V$.
Then

$$
Tv = \lambda v = \lambda Iv.
$$

Therefore $T$ is a scalar multiple of the identity operator.

_Exercise 27_

We will prove the contrapositive.

Suppose $T$ is not a scalar multiple of the identity.
Note that the linear map $0$ is also a scalar multiple of the identity.
There are non-zero and linearly independent vectors $w, v \in V$, such that $Tv = w$.
Let $n = \operatorname{dim} V$.
Extend $w, v$ to a basis $w, v, v_1, \dots, v_{n-2}$ of $V$.
The dimension of $\operatorname{span}(v, v_1, \dots, v_{n-2})$ equals $\operatorname{dim} V - 1$, but this subspace is clearly not invariant under $T$, completing the proof.

_Exercise 28_

You can check that the sum of invariant subspaces is invariant.
Any subspace of $V$ with dimension $\operatorname{dim} V - 1$ can be written as a sum of 2-dimensional subspaces of $V$ and, therefore, is invariant.
By _Exercise 27_, $T$ is a scalar multiple of the identity.

_Exercise 29_

Let $n = k$ and use the same notation from 3.22.
If $\operatorname{dim} \operatorname{null} T \ge 1$, then $0$ is an eigenvalue of $T$ an the corresponding eigenvectors are the non-zero vectors in $\operatorname{null} T$.
Because maximum length of a linearly independent list outside $\operatorname{null} T$ is $k$, by 5.10 it follows that there exists at most other $k$ eigenvalues, as desired.

_Exercise 31_

Suppose $v_1, \dots, v_m$ is linearly independent.
Let $T \in \mathcal{L}(V)$ be any linear map such that

$$
Tv_1 = \lambda_1 v_1, \dots, Tv_m = \lambda_m v_m
$$

for some distinct $\lambda_1, \dots, \lambda_m \in \mathbb{F}$.
Therefore $v_1, \dots, v_m$ are eigenvectors of $T$ corresponding to distinct eigenvalues.

Converse is the same as 5.10.

_Exercise 32_

Let $D$ denote the differentiation operator on the vector space of real-valued functions on $\mathbb{R}$.
Note that

$$
De^{\lambda_j x} = \lambda_j e^{\lambda_j x}
$$

for each $j = 1, \dots, n$.
Then $e^{\lambda_1 x}, \dots, e^{\lambda_n x}$ are eigenvectors corresponding to distinct eigenvalues.
5.10 now implies that they are linearly independent.
