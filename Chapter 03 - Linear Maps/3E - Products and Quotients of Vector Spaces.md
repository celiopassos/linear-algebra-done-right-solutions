Chapter 3: **Linear Maps**

**3.E**

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

Suppose $T$ is linear.
Let $(v_1, Tv_1), (v_2, Tv_2) \in \operatorname{graph of} T$.
We have

$$
\begin{aligned}
(v_1, Tv_1) + (v_2, Tv_2) &= (v_1 + v_2, Tv_1 + Tv_2)\\\\
&= (v_1 + v_2, T(v_1 + v_2))\\\\
&\in \operatorname{graph of} T,
\end{aligned}
$$

Where the second line follows because $T$ is linear and the third by definition of $\operatorname{graph of} T$.
Hence, $\operatorname{graph of} T$ is closed under addition.
Similarly, it also closed under scalar multiplication.
Therefore, $\operatorname{graph of} T$ is a subspace of $V \times W$.

Conversely, suppose $\operatorname{graph of} T$ is a subspace of $V \times W$.
Let $v_1, v_2 \in V$.
Then

$$
(v_1, Tv_1), (v_2, Tv_2), (v_1 + v_2, T(v_1 + v_2)) \in \operatorname{graph of} T. \tag{1}
$$

Since $\operatorname{graph of} T$ is a subspace of $V \times W$, adding the first two vectors above shows that

$$
(v_1 + v_2, Tv_1 + Tv_2) \in \operatorname{graph of} T. \tag{2}
$$

Because $T$ is function, if $(v, w), (v, \hat{w}) \in \operatorname{graph of} T$ then $w = \hat{w}$.
This, together with $(1)$ and $(2)$, implies that $T(v_1 + v_2) = Tv_1 + Tv_2$.
Hence, $T$ satisfies the additivity property of linear maps.
Similarly, $T$ satisfies the homogeneity property.
Therefore, $T$ is indeed a linear map.

_Exercise 2_

Define $T: V_1 \times \dots \times V_m \to V_j$ by

$$
T(v_1, \dots, v_m) = v_j.
$$

$T$ is clearly linear and surjective.
The Fundamental Theorem of Linear Maps (3.22) now implies that $V_j$ is finite-dimensional.

_Exercise 3_

Let $V = U_1 = U_2 = \mathbb{F}^\infty$.
Note that $U_1 + U_2 = \mathbb{F}^\infty$.
Define $T: \mathbb{F}^\infty \times \mathbb{F}^\infty \to \mathbb{F}^\infty$ by

$$
T\big((x_1, x_2, x_3, \dots), (y_1, y_2, y_3, \dots)\big) = (x_1, y_1, x_2, y_2, x_3, y_3, \dots).
$$

Thus, $T$ is obviously surjective.
To prove injectivity, let

$$
\big((x_1, x_2, x_3, \dots), (y_1, y_2, y_3, \dots)\big), \big((z_1, z_2, z_3, \dots), (w_1, w_2, w_3, \dots)\big) \in \mathbb{F}^\infty \times \mathbb{F}^\infty
$$

such that

$$
T\big((x_1, x_2, x_3, \dots), (y_1, y_2, y_3, \dots)\big) = T\big((z_1, z_2, z_3, \dots), (w_1, w_2, w_3, \dots)\big).
$$

This implies that

$$
(x_1, y_1, x_2, y_2, x_3, y_3, \dots) = (z_1, w_1, z_2, w_2, z_3, w_3).
$$

Therefore, $x_j = z_j$ and $y_j = w_j$ for each $j$.
Hence

$$
\big((x_1, x_2, x_3, \dots), (y_1, y_2, y_3, \dots)\big) = \big((z_1, z_2, z_3, \dots), (w_1, w_2, w_3, \dots)\big)
$$

and so $T$ is injective.
Thus, $T$ is an isomorphism, as desired.

_Exercise 4_

Consider any $\mathcal{f} \in \mathcal{L(V_1\times V_2 \times ... \times V_m, W)}$. We know that if $v_{11},...,v_{1,n_1}$ is a basis of $V_1$, ..., $v_{m1},...,v_{mn_m}$ is a basis of $V_m$, then $u_{11} = (v_{11}, 0, ... 0), u_{12} = (v_{12}, 0, ... 0), ...., u_{mn_m} = (0, 0, ... v_{mn_m})$ is a basis of $V_1\times V_2 \times ... \times V_m$. Let us also choose any basis $w_1,...,w_k$ in $W$ and denote matrix $A = \mathcal{M}(\mathcal{f})$. Then, $\mathcal{f}u_{ij} = \sum\limits_{k=1}^mA_{k,n_1+n_2+...+n_{i-1}+j}w_k$. We can then define $\varphi_{i} \in \mathcal{L}(V_i,W)$ through submatrix of $A$ corresponding to $V_i$ basis, so that $\mathcal{f}(v_1, v_2, ..., v_m) = \varphi_1(v_1) + ... + \varphi(v_m)$. The equation is clearly correct since we defined $\varphi_i$ through submatrix of $A$, so we have injectivity (obviously, different $A$ matrices will produce different sets of $\varphi_1,...,\varphi_m$, and $A$ matrices are trivially isomorphic to $\mathcal{L(V_1\times V_2 \times ... \times V_m, W)}$). Surjectivity is also obvious, since for every set of $\varphi_i$ we can build corresponding $\mathcal{M}(\mathcal{f})$ and hence find $\mathcal{f}$. So, we have got an isomorphism $\mathcal(f) \to (\varphi_1,...,\varphi_m)$, as desired.

_Exercise 5_

This is a bit simpler. Consider $T \in \mathcal{L}(V,W_1\times ...\times W_m)$ and suppose $Tv = (w_1,...,w_m)$. Define $T_i: T_iv = w_i$ - this will obviously be a linear map from $V$ to $W_i$. Then, we can build an isomorphism $\Psi$: $\Psi T = (T_1,...,T_m)$. It is clearly injective - since the only element in the $\operatorname{null}\Psi$ is $(0,...,0)$, and so it is in fact isomorphism.

_Exercise 6_

Let $u_1,...,u_n$ be a basis of $\mathbb{F}^n$. Let $(v_1,...,v_n) \in V^n$ and construct $T: \mathbb{F}^n \to V$ so, that $Tu_i = v_i$. It is clear that such definition uniquely maps any list of vectors from $V^n$ to a function from $\mathcal{\mathbb{F}^n,V}$. This mapping is also surjective, since we have taken arbitrary list of vectors, so it is isomorphism.

_Exercise 7_

Let $v + U = x + W$. For $u = 0$ there exists $w_0 \in W$: $v + 0 = x + w_0 \implies w_0 = v - x \implies v - x \in W$. We now can subtract $v$ from both parts and get $U = (x - v) + W = -w_0 + W = W$.

_Exercise 8_

$\Leftarrow$: Since $A \neq \emptyset$, there is at least one element. Denote it $v \in A$. We will now prove that $-v + A$ is a subspace.

1. Since $v \in A$, $v - v \in A - v$, so $0 \in A - v$.
2. Let $x \in A - v$. This means that $\exists u \in A: x = u - v$.
   By properties of $A$ we know that $\lambda u + (1 - \lambda)v \in A$, which means that $\lambda(u - v) + v \in A \implies \lambda x + v \in A \implies \lambda x \in A - v$.
3. Let $x_1, x_2 \in A - v$. This means $x_1 = u_1 - v$, $x_2 = u_2 - v$, $u_1,u_2 \in A$. By properties of $A$, $\frac{1}{2}u_1 + \frac{1}{2}u_2 \in A$, so $\frac{1}{2}u_1 + \frac{1}{2}u_2 - v \in A - v$, and using the previous statement we can conclude that $u_1 + u_2 - 2v \in A - v$, so $x_1 + x_2 \in A - v$.

We have shown that all three conditions of linear space are satisfied, so $A - v$ is in fact a linear space, which means that $A = v + (A - v)$ is an affine subset.

$\Rightarrow:$ Let $A$ be an affine subset. This means, that $\exists U \subset V$: $U$ is linear space, $v\in V$: $A = v + U$.

Consider any two elements from $A$: $v_1 = u_1 + v$, $v_2 = u_2 + v$, where $u_1,u_2 \in U$. 

$u_1, u_2 \in U \implies \lambda u_1 + (1 - \lambda)u_2 \in U \implies v + \lambda u_1 + (1 - \lambda)u_2 \in v + U \implies \lambda (v + u_1) + (1 - \lambda)(v + u_2) \in v + U \implies \lambda v_1 + (1-\lambda)v_2 \in v + U$.

_Exercise 9_

Let $A_1,A_2$ be two affine subsets of $V$, and suppose $A_1\cap A_2 \neq \emptyset$. If so, $\exists x \in A_1\cap A_2$. Consider any $y \in A_1 \cap A_2$, and denote $A_1 = v_1 + U_1$, $A_2 = v_2 + U_2$, where $U_1, U_2$ are subspaces of $V$, $v_1,v_2\in V$. After subtracting $y - x$, we get $y - x \in U_1$ and $y - x \in U_2$, and so $y - x \in U_1 \cap U_2$, from which it follows that $y = x + U_1 \cap U_2$. Since $y$ was arbitrary, we conclude, that $A_1 \cap A_2 = x + U_1 \cap U_2$, and since $U_1 \cap U_2$ is a linear subspace itself, $A_1 \cap A_2$ is an affine subset.

_Exercise 10_

This can be easiliy done through induction. We have already proven that for two subsets it is true. Now, suppose the statement is true for any number of subsets less, than n. Then, we can rewrite $A_1\cap A_2 \cap ... \cap A_n$ as $B \cap A_n$, where $B = A_1\cap A_2 \cap...\cap A_{n-1}$. By induction, $B$ is either empty or is an affine subset. In the first case, the overall intersection is also empty. In the latter case, we can use the base of our induction and conclude, that $B \cap A_n$ is either an affine subset itself, or is empty.

_Exercise 11_

a) We can use the result of the problem #8. To prove that $A$ is an affine subset we need to prove that if $u_1, u_2 \in A$, then $\lambda u_1 + (1 - \lambda)u_2 \in A$.

Let $u_1 = \lambda_1 v_1 + ... + \lambda_m v_m$ and $u_2 = \mu_1v_1 + ... + \mu_m v_m$, where $\sum\limits_{i=1}^m\lambda_i = \sum\limits_{i=1}^m\mu_i = 1$. 

$$
\lambda u_1 + (1 - \lambda)u_2 = \lambda\sum\limits_{i=1}^m\lambda_iv_i + (1 - \lambda)\sum\limits_{i=1}^m\mu_iv_i = \sum\limits_{i=1}^m(\lambda\lambda_i + (1 - \lambda)\mu_i)v_i
$$

Consider sum of coefficients in front of $v_1$ in the expression above:

$$
\sum\limits_{i=1}^m(\lambda\lambda_i + (1 - \lambda)\mu_i) = \lambda\sum\limits_{i=1}^m(\lambda_i) + (1 - \lambda)\sum\limits_{i=1}^m(\\mu_i) = \lambda \cdot 1 + (1 - \lambda) \cdot 1 = 1
$$

This implies that by definition of $A$ $\lambda u_1 + (1 - \lambda)u_2 \in A$, so $A$ is indeed an affine subset.

b) Let $B$ be an affine subset containing all of $v_1,...,v_m$. Suppose $B = v + U$, where $v \in V$ and $U$ is a subspace of $V$. Since $v_1,...,v_m$ are in $B$, we can write

$$
v_1 = v + u_1\\
v_2 = v + u_2\\
...\\
v_m = v + u_m
$$

We then have for any $\lambda_1,...,\lambda_m$: $\sum\limits_{i=1}^m\lambda_i = 1$: $\lambda_1 v_1 + ... + \lambda_m v_m = \sum\limits_{i=1}^m\lambda_iv + \sum\limits_{i=1}^m(\lambda_i)u_i = v + \sum\limits_{i=1}^m(\lambda_i)u_i = v + u'$, where $u' \in U$, so $\lambda_1 v_1 + ... + \lambda_m v_m \in B$, and since $\{\lambda_i\}$ were arbitrary, $A \subset B$.

c) Note that $v_m \in A$, which means that we can write $A = v_m + U$. This implies that $U = A - v_m$, and so any element in $U$ can be written as $u = \sum\limits_{i=1}^m \lambda_iv_i - v_m = \sum\limits_{i=1}^{m-1} \lambda_iv_i + (1 - \sum\limits_{i=1}^{m-1} \lambda_i)v_m - v_m = \sum\limits_{i=1}^{m-1} \lambda_i(v_i - v_m)$, where $\lambda_1...\lambda_{m-1} \in \mathbb{F}$, so $U = \operatorname{span}(v_1 - v_m,..., v_{m-1} - v_m)$, which implies $\operatorname{dim}U = \operatorname{dim}\operatorname{span}(v_1 - v_m,..., v_{m-1} - v_m) \le m - 1$.

_Exercise 12_

Let $v_1 + U, ..., v_k + U$ be a basis of $V/U$. Consider x = $\sum\limits_{i=1}^kc_iv_i$. Suppose $x \in U$, then $x + U = U = 0_{V/U}$, but it is possible only if all $c_i = 0$, since $x + U = \sum\limits_{i=1}^kc_i(v_i + U)$, and this is a linear combination of the $V/U$ bases vectors. So, any linear combination of $v_1,...,v_k$ with not all $c_i=0$ is not in $U$.

Now, consider any $v \in V$. Let us prove that there $\exists u: v = \sum\limits_{i=1}^kc_iv_i + u$. Indeed, consider $v + u_0: u_0 \in U$. $v + u_0 \in v + U$, so $v + u_0 = \sum\limits_{i=1}^kc_iv_i + u_1$, where $v + U = \sum\limits_{i=1}^kc_i(v_i + U)$ is representation of $v + U$ as linear combination of basis vectors of $V/U$. So, we have that $v + u_0 = \sum\limits_{i=1}^kc_iv_i + u_1$, and so $v = \sum\limits_{i=1}^kc_iv_i + u_1 - u_0 = \sum\limits_{i=1}^kc_iv_i + u$, where $u = u_1 - u_0 \in U$. We have proven, that any vector $v$ can be represented as $\sum\limits_{i=1}^kc_iv_i + u$, where $u \in U$.

Now, let us show that this representation is unique. Indeed, consider $v \in V$, and let $v = \sum\limits_{i=1}^kc_iv_i + u = \sum\limits_{i=1}^kd_iv_i + u'$. Then, $0 = v - v = \sum\limits_{i=1}^kc_iv_i + u - (\sum\limits_{i=1}^kd_iv_i + u') = \sum\limits_{i=1}^k(c_i - d_i)v_i + u - u'$, hence we get $u' - u = \sum\limits_{i=1}^k(c_i - d_i)v_i$. But the left part of the equation belongs to $U$, and this means that the right part of the equation must be 0, as we have proven earlier. So, $c_i = d_i$, and hence $u = u'$, so the representation is indeed unique.

We next want to prove that such a mapping $T$: $v = (\sum\limits_{i=1}^kc_iv_i + u) \to (u, \sum\limits_{i=1}^kc_i(v_i + U))$ is isomorphism, and to do this, we need to show that $T$ is linear.

1. $T0 = 0$. Indeed, if $v = 0$, then $0 = \sum\limits_{i=1}^kc_iv_i + u \implies u = -\sum\limits_{i=1}^kc_iv_i$. But we already have proven that if linear combination of $v_i$ is in $U$, it implies that $c_i = 0$. So, $c_i = 0$ and $u = 0$, so $T0 = (0, 0 + U)$. By the way, we also have proven that $\operatorname{null}T = \{0\}$, so $T$ is injective. 

2. $T\lambda v = T\lambda(\sum\limits_{i=1}^kc_iv_i + u) = T(\sum\limits_{i=1}^k\lambda c_iv_i + \lambda u) = (\lambda u, \sum\limits_{i=1}^k\lambda c_iv_i + U) = \lambda (u, \sum\limits_{i=1}^k c_iv_i + U) = \lambda Tv$

3. $T(v + w) = T(\sum\limits_{i=1}^kc_iv_i + u + \sum\limits_{i=1}^kd_iv_i + u') = T(\sum\limits_{i=1}^k(c_i + d_i)v_i + u + u') = (u + u', \sum\limits_{i=1}^k(c_i + d_i)v_i + U) = Tv + Tw$.

So, $T$ is indeed linear. Since it is also surjective and injective, we can conclude, that it is isomorphism.

_Exercise 13_

We have already proven in the previous task that $v_1,...,v_m$ are linearly independent and $\forall v \in V$ we can represent uniquely $v = \sum\limits_{i=1}^mc_iv_i + u$, where $u \in U$. So, $v = \sum\limits_{i=1}^mc_iv_i + \sum\limits_{i=1}^nd_iu_i$. This representation is unique, so $c_i, d_i$ are unique, which means that $v_1,...v_m,u_1,...,u_n$ indeed form a basis of V.

_Exercise 14_

a) It is clear that if $(0, 0,...) \in U$, $v \in U \implies \lambda v \in U$ and $v_1,v_2 \in U \implies v_1 + v_2 \in U$ since $v_1 + v_2$ will still have a finite number of non-zero coefficients.

b) Denote $v_i \in \mathbb{F}^\infty$: $v_i[j] = 1$ if $j = p_i^n$, where $p_i$ is the i'th prime number, and $n \in \mathbb{N}$. It is clear, that every $v_i$ has non-zero coefficients on different positions than any other $v_j$, so $\sum\limits_{i=1}^nc_iv_i = 0 \implies c_1=...=c_n0$ for any $n$. It is also clear, that $v_i \notin U$ since there are infinitely many non-zero coefficients in $v_i$. Now, consider $v_1 + U,...,v_n+U$ for some $n \in \mathbb{N}$. If they were linearly independent in $\mathbb{F}^\infty/U$, then there should exist non-zero coefficients $c_1...c_n$: $\sum\limits_{i=1}^nc_iv_i \in U$. But this linear combination will have infinitely many non-zero coefficients, and hence it cannot be in $U$. This means that $v_1 + U,...,v_n+U$ are linearly independent for any $n$, and so $\mathbb{F}^\infty/U$ is infinite-dimensional. 

_Exercise 15_

Using fundamental theorem of linear maps, we can write $\operatorname{dim}V = \operatorname{dim}\operatorname{null}\varphi + \operatorname{dim}\operatorname{range}\varphi$. Since $\varphi \neq 0$, we have that $\operatorname{dim}\operatorname{range}\varphi > 0$, and $\operatorname{range}\varphi \subset \mathbb{F}$, so $\operatorname{dim}\operatorname{range}\varphi = 1$. Hence, $\operatorname{dim}\operatorname{null}\varphi = \operatorname{dim}V - 1$. So, the dimension of the quotient space is $\operatorname{dim}V/\operatorname{null}\varphi = \operatorname{dim}V - \operatorname{dim}\operatorname{null}\varphi = 1$.

_Exercise 16_

Since $\operatorname{dim}V/U = 1$, its basis consists of single element $v_0 + U$. This implies, that any vector $v \in V$ can be represented as $\lambda v_0 + u$, where $u \in U$. Define $\varphi$ so that $\varphi v_0 = 1$, and $\forall u \in U \ \varphi u = 0$. It is easy to show that $\varphi$ is linear, and $\operatorname{null}\varphi = U$.

_Exercise 17_

We have proven everything required in exercise 12

_Exercise 18_

$\Rightarrow$: suppose $\exists S: T = S \circ \pi$. Consider $u \in U$. We have $Tu = S \circ \pi u = S(u + U) = S0 = 0$, so indeed $U \subset \operatorname{null}T$.

$\Leftarrow$: suppose $U \subset \operatorname{null}T$. Let us define $S(v + U) = Tv$ and show that it is linear map $V/U \to W$. 

1. $S(0 + U) = Tu = 0$ since $U \subset \operatorname{null}T$
2. $S((v + w + U)) = T(v + w) = Tv + Tw = S(v + U) + S(w + U)$
3. $S(\lambda(v + U)) = S(\lambda v + U) = T\lambda v = \lambda Tv = \lambda S(v + U)$

_Exercise 19_

The equivalent statement is $U_1$,...,$U_n$: $U_i \in V$ are disjoint if and only if $|U_1 \cup U_2 \cup ... \cup U_n| = |U_1| + ... + |U_n|$. 

_Exercise 20_

a) Let's prove $\Gamma$ is linear. 
1. $\Gamma(0) = 0 \circ \pi = 0$
2. $\Gamma(S_1 + S_2) = (S_1 + S_2)\circ \pi$. $\forall v \in V \ \implies ((S_1 + S_2)\circ \pi)(v) = (S_1 + S_2)(v + U) = S_1(v + U) + S_2(v + U) = (S_1 \circ \pi) (v) + (S_2 \circ \pi) (v) = \Gamma(S_1)(v) + \Gamma(S_2)(v)$, hence $\Gamma(S_1 + S_2) = \Gamma(S_1) + \Gamma(S_2)$ since these function are equal in every point.
3. $\Gamma(\lambda S) = (\lambda S) \circ \pi$. $\forall v \in V \ \implies ((\lambda S) \circ \pi)(v) = (\lambda S) (v + U) = \lambda S(v + U) = \lambda \Gamma(S)(v)$, and so $\Gamma(\lambda S) = \lambda \Gamma(S)$

b) consider $S_1,S_2 \in \mathcal{L}(V/U,W)$. 

$\Gamma(S_1) - \Gamma(S_2) = (S_1 - S_2) \circ \pi$. If $\Gamma(S_1) = \Gamma(S_2)$, we have that $\forall v \in V$ (S_1 - S_2)(v + U) = 0. But this means, that $S_1 - S_2 = 0$, and hence $S_1 = S_2$, so $\Gamma$ is indeed injective.

c) We want to prove that $\operatorname{range}\Gamma = \{T \in \mathcal{L}(V, W): Tu = 0 \forall u \in U\}$. 

Consider first $u \in U$. $\forall S \ \Gamma(S)(u) = S(u + U) = S(0 + U) = 0$, which means that $\operatorname{range}\Gamma \subset \{T \in \mathcal{L}(V, W): Tu = 0 \forall u \in U\}$

On the other hand, consider any $T: \forall u \in U \ Tu = 0$. Define $S \in \mathcal(L)(V/U, W): S(v + U) = Tv$. It is easy to show, that such defined S will be linear map on $V/U$ and by construction $\Gamma(S) = T$.