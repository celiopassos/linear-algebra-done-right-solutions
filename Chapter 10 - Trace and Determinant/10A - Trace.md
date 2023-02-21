Chapter 10: **Trace and Determinant**

**10.A**

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

_Exercise 1_

Suppose $\mathcal{M}(T, (v_1, \dots, v_n))$ is invertible.
Then there exists an $n$-by-$n$ matrix $A$ such that

$$
I = \mathcal{M}(T, (v_1, \dots, v_n))A.
$$

Define $S \in \mathcal{L}(V)$ such that

$$
\mathcal{M}(S, (v_1, \dots, v_n)) = A.
$$

Then

$$
\mathcal{M}(ST, (v_1, \dots, v_n)) = \mathcal{M}(S, (v_1, \dots, v_n)) \mathcal{M}(T, (v_1, \dots, v_n)) = \mathcal{M}(I, (v_1, \dots, v_n)).
$$

The equation above shows that $ST = I$.
Exercise 10 in section 3D now implies that $T$ is invertible and $S = T^{-1}$.

Conversely, suppose $T$ is invertible.
Then

$$
I = \mathcal{M}(T^{-1}T, (v_1, \dots, v_n)) = \mathcal{M}(T^{-1}, (v_1, \dots, v_n))\mathcal{M}(T, (v_1, \dots, v_n))
$$

and

$$
I = \mathcal{M}(TT^{-1}, (v_1, \dots, v_n)) = \mathcal{M}(T^{-1}, (v_1, \dots, v_n))\mathcal{M}(T^{-1}, (v_1, \dots, v_n)),
$$

which shows that $\mathcal{M}(T, (v_1, \dots, v_n))$ is invertible.

_Exercise 2_

Suppose $A$ and $B$ are $n$-by-$n$ matrices.
Let $V$ denote an $n$-dimensional vector space and choose a basis for $V$.
Define $S, T \in \mathcal{L}(\mathbb{F}^n)$ such that $\mathcal{M}(S) = A$ and $\mathcal{M}(T) = B$, where this matrices are with respect to the chosen basis.
We have

$$
I = AB = \mathcal{M}(S)\mathcal{M}(T) = \mathcal{M}(ST).
$$

Therefore $ST = I$.
Exercise 10 in section 3D shows that $TS = I$.
Thus

$$
I = \mathcal{M}(TS) = \mathcal{M}(T)\mathcal{M}(S) = BA.
$$

The equation above completes the proof.

_Exericse 3_

Let $A$ denote the matrix of $T$, which is the same with respect to every basis.
Let $v_1, \dots, v_n$ be basis of $V$.
Then

$$
Tv_k = A_{1,k}v_1 + \dots + A_{n, k}v_n. \tag{1}
$$

for $k = 1, \dots, n$.
We'll asumme $n \ge 2$ here (if $n = 1$ then every operator on $V$ already is a multiple of the identity).
The list $v_1 - v_2, v_2, \dots, v_n$ is also a basis of $V$.
The matrix of $T$ with respect to this basis is the same, therefore we have

$$
T(v_1 - v_2) = A_{1,1}(v_1 - v_2) + A_{2,1}v_2 + \dots + A_{n,1}v_n = A_{1,1}v_1 + (A_{2,1} - A_{1,1})v_2 + \dots + A_{n,1}v_n. \tag{2}
$$

Calculating $Tv_1 - Tv_2$ using $(1)$ we get

$$
T(v_1 - v_2) = Tv_1 - Tv_2 = (A_{1,1} - A_{1,2})v_1 + (A_{2,1} - A_{2,2})v_1 + \dots + (A_{n, 1} - A_{n, 2})v_n. \tag{3}
$$

Because $T(v_1 - v_2)$ can be uniquely written as combination of basis vectors, equating $(2)$ and $(3)$ shows that all entries in second column of $A$ equal $0$, except possibly $A_{2,2}$ which equals $A_{1,1}$.
This same argument can be repeated with every pair of the basis vectors.
Hence all nondiagonal entries of $A$ are $0$ and all diagonal entries are equal.
Thus $A$ is a scalar multiple of the identity, which implies that so is $T$.

_Exercise 4_

Let $A = \mathcal{M}(T, (v_1, \dots, v_n))$.
Then

$$
Iu_k = Tv_k = A_{1,k}v_1 + \dots + A_{n,k}v_n.
$$

The equation above shows that $\mathcal{M}(I, (u_1, \dots, u_n), (v_1, \dots, v_n)) = A$, because each $Iu_k$ can be uniquely written as linear combination of the $v$'s and this combination forces the desired equality.

_Exercise 5_

Suppose $B$ is an $n$-by-$n$ matrix.
Let $V$ denote an $n$-by-$n$ dimensional vector space and let $v_1, \dots, v_n$ be a basis of $V$.
Define $T \in \mathcal{L}(V)$ such that $\mathcal{M}(T, (v_1, \dots, v_n)) = B$.
By 5.27, there is a basis $u_1, \dots, u_n$ of $V$ such that $\mathcal{M}(T, (u_1, \dots, u_n))$ is upper triangular.
The equation written in 10.7 completes the proof.

_Exercise 6_

Choose $V = \mathbb{R}^2$ and define $T \in \mathcal{L}(V)$ by

$$
T(x, y) = (-y, x).
$$

Then

$$
T^2(x, y) = (-x, -y),
$$

which shows that $-1$ is the only eigenvalue of $T^2$, with multiplicity $2$.
Thus $\operatorname{trace}(T^2) = -2$.

_Exercise 7_

It is easy to see that every eigenvalue of $T^2$ is nonnegative, by applying $T$ twice to each of basis vectors which are eigenvectors of $T$.

_Exercise 8_

If $w = 0$, then $T = 0$ and $\operatorname{trace} T = 0$.
If $w \neq 0$, then extend $w$ to a basis of $V$.
All entries of the matrix of $T$ with respect to this basis are $0$, except possibly the first row, because $\operatorname{range} T \subset \operatorname{span}(w)$.
Therefore, the trace of this matrix, which equals the trace of $T$, is $\langle w, v \rangle w$.

_Exercise 9_

It is easy to check that $Pw = w$ for every $w \in \operatorname{range} P$.
Let $u_1, \dots, u_n$ be a basis of $\operatorname{null} P$ and let $w_1, \dots, w_m$ be a basis of $\operatorname{range} P$.
Exercise 4 in section 5B implies that joining these two basis we get a basis of $V$.
Moreover this is a basis consisting of eigenvectors of $P$.
Therefore the eigenvalues of $T$ are $0$, with multiplicity $n$, and $1$, with multiplicity $m$.
Thus $\operatorname{trace} T = m$.

_Exercise 10_

This follows directly from Exercise 2 in section 7A.

_Exercise 11_

Because $T$ is self-adjoint, $V$ has a basis consisting of eigenvectors of $T$, by the Spectral Theorems (see 7.24 and 7.29).
By 7.35 (b), all eigenvalues of $T$ are nonnegative.
If their sum equals $0$, then they all equal $0$.
Applying $T$ to each of the basis vectors (which are eigenvectors of $T$), we see that $T = 0$.

_Exercise 12_

Every orthogonal projection is positive (see 7.32) and equal to its square (see 6.55).
We have

$$
(PQP)^* = P^*Q^*P\^* = PQP
$$

and

$$
\langle PQPv, v \rangle = \langle QPv, Pv \rangle \ge 0,
$$

where the inequality above follows because $Q$ is positive.
Hence $PQP$ is positive.
Thus

$$
\operatorname{trace}(PQ) = \operatorname{trace}(P^2 Q) = \operatorname{trace}(PQP) \ge 0.
$$

_Exercise 13_

The trace of $T$ is

$$
\operatorname{trace} T = 51 - 40 + 1 = 12.
$$

If $\lambda$ is the third eigenvalue of $T$, then

$$
-48 + 24 + \lambda = 12.
$$

Thus $\lambda = 36$.

_Exercise 14_

We have

$$
\operatorname{trace} (cT) = \operatorname{trace}(\mathcal{M}(cT)) = \operatorname{trace}(c\mathcal{M}(T)) = c \operatorname{trace}(\mathcal{M}(T)) = c \operatorname{trace} (T).
$$

_Exercise 15_

$$
\begin{aligned}
\operatorname{trace} (ST) &= \operatorname{trace} (\mathcal{M}(ST))\\\\
&= \operatorname{trace} (\mathcal{M}(S)\mathcal{M}(T))\\\\
&= \operatorname{trace}(\mathcal{M}(T)\mathcal{M}(S))\\\\
&= \operatorname{trace}(\mathcal{M}(TS))\\\\
&= \operatorname{trace}(TS)
\end{aligned}
$$

_Exercise 16_

We give a counterexample.
Define $T \in \mathcal{L}(\mathbb{R}^2)$ by

$$
T(x, y) = (-y, x).
$$

The matrix of $T$ with respect to standard basis of $\mathbb{R}^2$ is

$$
\begin{pmatrix}
0 & -1\\\\
-1 & 0
\end{pmatrix}.
$$

Hence $\operatorname{trace} T = 0$.
However, $T^2 = -I$, which implies that $\operatorname{trace} T^2 = -2$.

_Exercise 17_

Let $u_1, \dots, u_m$ be a basis of $\operatorname{null} T$.
Extend it to a basis $u_1, \dots, u_m, v_1, \dots, v_n$ of $V$.
Then $Tv_1, \dots, Tv_n$ is a basis of $\operatorname{range} T$ (see the proof of 3.22).
Define a linear map $S': \operatorname{range} T \to V$ by

$$
S'(Tv_j) = v_j
$$

for $j = 1, \dots, n$.
We can extend $S'$ to an operator $S$ on $V$.
Regardless of how we extend $S'$, it is clear that the matrix of $ST$ will be of the following form

$$
\mathcal{M}(ST, (u_1, \dots, u_m, v_1, \dots, v_n)) =
\begin{pmatrix}
0 &   &   &   &\\\\
  & \ddots &   &   &\\\\
  &   & 0 &   &   &\\\\
  &   &   & 1 &   &\\\\
  &   &   &   & \ddots &\\\\
  &   &   &   &   & 1
\end{pmatrix},
$$

where the $1$'s appear on the last $n$ diagonal entries.
However, the trace of this matrix should equal $0$ (since $\operatorname{trace} (ST) = 0$).
Hence $n = 0$, because the $1$'s should not appear in any of the columns.
Therefore $T = 0$.

_Exercise 18_

Note that $||Te_j||^2$ is the sum of the the squares of the absolute values of the entries in the $j$-th column of the matrix of $T$ with respect to the basis $e_1, \dots, e_n$.
Thus, we're essentially being asked to prove that $\operatorname{trace}(T^*T)$ equals the sum of the squares of the absolute values of the entries in the matrix of $T$ with respect to any orthonormal basis.
We have

$$
\operatorname{trace}(T^*T) = \operatorname{trace}(\mathcal{M}(T^*T)) = \operatorname{trace}(\mathcal{M}(T^*)\mathcal{M}(T)),
$$

where these matrices are taken with respect to $e_1, \dots, e_n$.
The equation above gives the desired result, because $\mathcal{M}(T^*)$ is the conjugate transpose of $\mathcal{M}(T)$ and so the $j$-th diagonal entry of $\mathcal{M}(T^*)\mathcal{M}(T)$ equals the sum of the squares of the absolute values of the entries in the $j$-th column of $\mathcal{M}(T)$.

_Exercise 19_

The function $\langle \cdot, \cdot \rangle$ satisfies additivity and homogeneity in the first slot by 10.18 and Exercise 14.
For conjugate symmetry we have

$$
\langle S, T \rangle = \operatorname{trace}(ST^*) = \operatorname{trace}((TS^*)^*) = \overline{\operatorname{trace}(TS^*)} = \overline{\langle T, S \rangle},
$$

where the third equality follows from Exercise 10.
By Exercise 18, it satisfies positive-definiteness.

_Exercise 20_

As explained in the solution to Exercise 18, the right side of the inequality is equal to $\operatorname{trace} (T^*T)$.
Let $f_1, \dots, f_n$ be an orthonormal basis of $V$ with respect to which the matrix of $T$ is upper triangular (6.37 assures the existence of this basis).
Then the eigenvalues of $T$ appear on the diagonal of this matrix.
Because $\mathcal{M}(T^*)$ is the conjugate transpose of $\mathcal{M}(T)$, where this matrices are with respect to the basis $f_1, \dots, f_n$, a moment's thought shows that

$$
|\lambda_1|^2 + \dots + |\lambda_n|^2 \le \operatorname{trace}(\mathcal{M}(T^*)\mathcal{M}(T)).
$$

The right side of the inequality above equals $\operatorname{trace}(T^*T)$, which yields the desired result.

_Exercise 21_

We already have proven, that if $e_1,..,e_n$ is an othonormal basis, then $\operatorname{trace}(T^*T) = ||Te_1||^2 + ... + ||Te_n||^2$.

Since $Te_i = A_{1i}e_1 + ... + A_{ni}e_n$, we have that $||Te_i||^2 = |A_{1i}|^2 + ... + |A_{ni}|^2$, and hence 

$$
\operatorname{trace}(T^*T) = \sum\limits_{k=1}^n\sum\limits_{j=1}^n|A_{jk}|^2
$$

On the other hand, consider a basis $v_1,..,v_n$ of $T$ where it has upper-triangular matrix, which exists for any operator over $\mathbb{C}$.

$$
\mathcal{M}(T, (v_1, \dots, v_n)) =
\begin{pmatrix}
a_{11} &  a_{12} &   &   &\\\\
 0 &  a_{22} & \ddots &   &\\\\
  &   & ... &   &  \\\\
  &   &   &  &   a_{nn}\\\\
\end{pmatrix}
$$


 It is easy to see, that in this basis $T^*T$ has matrix such that $\mathcal{M}(T^*T, (v_1,..,v_n))_{i,i} = |a_{1i}|^2 + ... + |a_{i,i}|^2 \ge |a_{ii}|^2$, with $a_{11}...a_{nn}$ being the list of eigenvalues of $T$. 

 Since the trace of an operator is the trace of its matrix in any basis, we conclude that 

$$
\operatorname{trace}(T^*T) = \sum\limits_{k=1}^n\sum\limits_{j=1}^n|A_{jk}|^2 = |\lambda_1|^2 + ... + |\lambda_n|^2 + c
$$

where $c = \sum\limits_{i=1}^n\sum\limits_{j=1}^i|a_{ij}|^2 \ge 0$, so it is clear that 

$$
|\lambda_1|^2 + ... |\lambda_n|^2 \le \sum\limits_{k=1}^n\sum\limits_{j=1}^n|A_{jk}|^2
$$

_Exercise 21_

Let $e_1, \dots, e_n$ be an orthonormal basis of $V$.
By Exercise 18, we have

$$
\begin{aligned}
\operatorname{trace}(T^*T) &= ||Te_1||^2 + \dots + ||Te_n||^2\\\\
&\ge ||T^*e_1||^2 + \dots + ||T^*e_n||^2\\\\
&= \operatorname{trace}(TT^*)\\\\
&= \operatorname{trace}(T^*T).
\end{aligned}
$$

Because the first and last lines are equal, we must have equality throughout.
Thus

$$
||Te_1||^2 + \dots + ||Te_n||^2 = ||T^*e_1||^2 + \dots + ||T^*e_n||^2.
$$

Since $||Te_j|| \ge ||T^*e_j||$, the equation above actually implies that $||Te_j|| = ||T^*e_j||$.
Note that the basis $e_1, \dots, e_n$ was arbitrary and for any nonzero vector $v \in V$, we can extend $\frac{v}{||v||}$ to an orthonormal basis of $V$.
Thus

$$
\left|\left|T\left(\frac{v}{||v||}\right)\right|\right| = \left|\left|T^*\left(\frac{v}{||v||}\right)\right|\right|
$$

for all nonzero $v \in V$.
Multiplying the equation above by $||v||$ we get that $||Tv|| = ||T^*v||$.
Then $T$ is normal by 7.20.
