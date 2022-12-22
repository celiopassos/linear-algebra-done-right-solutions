Chapter 5: **Eigenvalues, Eigenvectors and Invariant Subspaces**

**5.C**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [ ] Exercise 5
- [x] Exercise 6
- [x] Exercise 7
- [x] Exercise 8
- [x] Exercise 9
- [x] Exercise 10
- [x] Exercise 11
- [x] Exercise 12
- [ ] Exercise 13
- [ ] Exercise 14
- [ ] Exercise 15
- [x] Exercise 16

_Exercise 1_

If $\operatorname{null} T = \{0\}$ (because it implies surjectivity) or $\operatorname{range} T = \{0\}$ the result is obvious.
Assume both contain non-zero vectors.

Since $\operatorname{null} T \neq \{0\}$, we have that $0$ is an eigenvalue of $T$ and that $E(0, T) = \operatorname{null} T$.
Let $\lambda_1, \dots, \lambda_m$ denote the other distinct eigenvalues of $T$.
Now 5.41 implies that $V = \operatorname{null} T \oplus E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T)$.
We will prove that $\operatorname{range} T = E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T)$.

Suppose $v \in E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T)$.
Then $v = v_1 + \dots + v_m$ for some $v_1, \dots, v_m$, where each $v_j \in E(\lambda_j, T)$.
Moreover, $v = T(\frac{1}{\lambda_1}v_1) + \dots + T(\frac{1}{\lambda_m}v_m)$, which implies that $v \in \operatorname{range}(T)$.
Hence

$$E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T) \subset \operatorname{range} T.$$

For the inclusion in the other direction, suppose $v \in \operatorname{range} T$.
Note that $\operatorname{range} T$ stays the same when we restrict $T$ to $E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T)$.
Then $v = T(v_1 + \dots + v_m)$ for some $v_1, \dots, v_m$, where each $v_j \in E(\lambda_j, T)$.
Therefore $v = \lambda_1 v_1 + \dots + \lambda_m v_m$ and, because $\lambda_j v_j \in E(\lambda_j, T)$ for each $j$, this proves that $v \in E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T)$.
Thus $\operatorname{range} T \subset E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T)$, completing the proof.

_Exercise 2_

We give a counterexample.
Let $V = \mathbb{R}^2$ and $T(x, y) = (-y, x)$.
$T$ is invertible, thus $V = \operatorname{null} T \oplus \operatorname{range} T$.
But, as shown in Example 5.8, $T$ has no eigenvalues, therefore $T$ is not diagonalizable.

Note: If we let $V$ be infinite-dimensional, then any invertible operator $T \in \mathcal{L}(V)$ will prove it to be wrong, because we will have $V = \operatorname{null} T \oplus \operatorname{range} T$, but $T$ being diagonalizable requires $V$ to be finite-dimensional.

_Exercise 3_

Obviously (a) implies (b) and, by 1.45, it also implies (c).

Suppose (b) holds.
Combining 3.22 and 2.43, we have

$$
\begin{aligned}
\operatorname{dim} \operatorname{null} T + \operatorname{dim} \operatorname{range} T &= \operatorname{dim} V\\\\
&= \operatorname{dim} (\operatorname{null} T + \operatorname{range} T)\\\\
&= \operatorname{dim} \operatorname{null} T + \operatorname{dim} \operatorname{range} T - \operatorname{dim}(\operatorname{null} T \cap \operatorname{range} T)\\\\
\end{aligned}
$$

Therefore $\operatorname{dim}(\operatorname{null} T \cap \operatorname{range} T) = 0$, implying (c) is true.

Suppose (c) holds.
By 1.45, $\operatorname{null} T + \operatorname{range} T$ is a direct sum.
Then, by 2.43 and 3.22, we have

$$
\operatorname{dim} (\operatorname{null} T \oplus \operatorname{range} T) = \operatorname{dim} \operatorname{null} T + \operatorname{dim} \operatorname{range} T = \operatorname{dim} V
$$

Since $\operatorname{null} T \oplus \operatorname{range} T$ is a subspace of $V$, it follows that $\operatorname{null} T \oplus \operatorname{range} T = V$, implying (a) and completing the proof.

_Exercise 4_

Let $T \in \mathcal{L}(\mathbb{F}^\infty)$ be the forward shift operator.

Then $\operatorname{null} T = \{0\}$, which implies (c).
However $T$ is not surjective, therefore (b) is false.

_Exercise 5_

Suppose $T$ is diagonalizable.
It is easy to see that, for every $\lambda \in \mathbb{C}$, $T - \lambda I$ is also diagonalizable, because $\mathcal{M}(T - \lambda I)$ equals $\mathcal{M}(T)$ with the entries on the diagonal subtracted by $\lambda$.
By _Exercise 1_, this implies that

$$
V = \operatorname{null} (T - \lambda I) \oplus \operatorname{range} (T - \lambda I). \tag{1}
$$

Conversely, suppose (1) holds.
Denote $\lambda_1,...,\lambda_m$ to be all distinct eigenvalues of $T$.

We first prove that $\operatorname{null}(T-\lambda_iI) \subset \operatorname{range}(T-\lambda_jI)$, if $i \neq j$. Suppose $v \in \operatorname{null}(T-\lambda_iI)$. We know, that $V = \operatorname{null}(T - \lambda_jI)\oplus \operatorname{range}(T - \lambda_jI)$, so 

$$
v = u + w\\
u \in \operatorname{null}(T-\lambda_jI)\\
w \in \operatorname{range}(T-\lambda_jI)
$$

Now, $Tv = \lambda_i v = \lambda_i(u + w) = \lambda_ju + Tw$, hence $(T - \lambda_iI)w = (\lambda_i - \lambda_j)u$, so $(T - \lambda_iI)w \in \operatorname{range}(T - \lambda_iI)$ and $w \in \operatorname{null}(T - \lambda_iI)$, which implies that $w = 0$, because from the definition of direct sum we know, that $\operatorname{null}(T - \lambda_iI) \cap \operatorname{range}(T - \lambda_iI) = \{0\}$.

We will now prove that $V = \bigcup\limits_{i}\operatorname{range}(T - \lambda_iI)$. Suppose this is not true, so there is $v \notin \operatorname{null}(T-\lambda_iI),\ i = 1...m$. This implies $v \neq 0$, and that $v \in \operatorname{range}(T - \lambda_iI),\ i=1...m$, and so $v \in \bigcap\limits_{i}\operatorname{range}(T - \lambda_iI)$. We can note, that for any $i$ $\operatorname{range}(T - \lambda_iI)$ is invariant under $T$, because if $v \in \operatorname{range}(T - \lambda_iI)$, $\exists w: v = Tw - \lambda_iw$, hence $Tv = T(-\lambda_i)Tw \in \operatorname{range}(T - \lambda_iI)$. So, $U = \bigcap\limits_i\operatorname{range}(T - \lambda_iI)$ is also invariant under $T$. This implies, $T_{|U}$ is an operator on $U$, and since $U \neq \{0\}$ and is finite-dimensional, $T_{|U}$ has an eigenvalue $\lambda$, and this is also an eigenvalue of $T$. But this implies that $\lambda = \lambda_i$, and so the corresponding eigenvector belongs both to $\operatorname{null}(T - \lambda_iI)$ and to $\operatorname{range}(T - \lambda_iI)$, which contradicts with the fact, that $V$ is a direct sum of these two subspaces.

So, $V = \bigcup\limits_{i}\operatorname{range}(T - \lambda_iI)$. It is clear, that $\bigcup\limits_{i}\operatorname{range}(T - \lambda_iI) \subset \operatorname{range}(T - \lambda_1I) + ... + \operatorname{range}(T - \lambda_mI)$, and the opposite inclusion is correct as well, since $\operatorname{range}(T - \lambda_1I) + ... + \operatorname{range}(T - \lambda_mI) \subset V$. Finally, we have proven, that $\operatorname{range}(T - \lambda_iI) \cap \operatorname{range}(T - \lambda_jI) = \{0\}$, which completes the proof.

_Exercise 6_

Let $\lambda_1, \dots, \lambda_m$ denote the distinct eigenvalues of $T$, $v_1, \dots, v_n$ corresponding eigenvectors and $\alpha_1, \dots, \alpha_n$ the corresponding eigenvalues of $S$.
Then

$$
\begin{aligned}
STv_j &= S(\lambda_j v_j)\\\\
&= \alpha_j \lambda_j v_j\\\\
&= \alpha_j Tv_j\\\\
&= T(\alpha_j Tv_j)\\\\
&= TSv_j\\\\
\end{aligned}
$$

for $j = 1, \dots, n$.
Thus, by 3.5, $ST = TS$.

_Exercise 7_

Suppose $\lambda$ appears $n$ times on the diagonal of $A$.
Let $v_1, \dots, v_n, u_1, \dots, u_m$ be a basis composed of the same basis vectors chosen to represent $A$ (possibly in different order) such that the $v$'s are eigenvectors of $\lambda$ and the remaining are corresponding eigenvectors to $\lambda_1, \dots, \lambda_m$.
Note that $\lambda_k \neq \lambda$ for each $k$, because we have $n$ $v$'s.

Let $v \in E(\lambda, T)$.
There are $a_1, \dots, a_n, c_1, \dots, c_m \in \mathbb{F}$ such that

$$
v = a_1 v_1 + \dots + a_n v_n + c_1 u_1 + \dots + c_m u_m
$$

Then

$$
\begin{aligned}
0 &= (T - \lambda I)v\\\\
&= \sum\limits_{k=1}^n (\lambda - \lambda) a_1 v + \sum\limits_{k=1}^m (\lambda_k - \lambda) c_k u_k\\\\
&= \sum\limits_{k=1}^m (\lambda_k - \lambda) c_k u_k\\\\
\end{aligned}
$$

Since $\lambda_k - \lambda \neq 0$, all the $c$'s are 0, implying that $v \in \operatorname{span}(v_1, \dots, v_n)$.
Hence $E(\lambda, T) \subset \operatorname{span}(v_1, \dots, v_n)$.
The inclusion in the other directions is obvious, thus it becomes an equality.
Moreover, $v_1, \dots, v_n$ is linearly independent and, hence, a basis of $E(\lambda, T)$.
Thus $\operatorname{dim} E(\lambda, T) = n$.

_Exercise 8_

Assume $T$ has other eigenvalues besides $8$ (otherwise there is nothing to prove).
Then, since $\operatorname{dim} E(8, T) + 1 = \operatorname{dim} F^5$ and by part (d) of 5.41, $T$ has only one eigenvalue besides $8$.
Therefore at least between $T - 2I$ and $T - 6I$ is invertible.

_Exercise 9_

$$
\begin{aligned}
v \in E(\lambda, T) &\iff Tv = \lambda v\\\\
&\iff T^{-1}(\lambda v) = v\\\\
&\iff T^{-1} v = \frac{1}{\lambda} v\\\\
&\iff v \in E(\frac{1}{\lambda}, T^{-1})\\\\
\end{aligned}
$$

_Exercise 10_

If $0$ is an eigenvalue of $T$, then

$$
\begin{aligned}
\operatorname{dim} \operatorname{range} T &= \operatorname{dim} V - \operatorname{dim} \operatorname{null} T\\\\
&= \operatorname{dim} V - \operatorname{dim} E(0, T)\\\\
&\ge \operatorname{dim}(E(0, T) \oplus E(\lambda_1, T) \oplus \dots \oplus E(\lambda_m, T)) - \operatorname{dim} E(0, T)\\\\
&= \operatorname{dim} E(0, T) + \operatorname{dim} E(\lambda_1, T) + \dots + \operatorname{dim} E(\lambda_m, T) - \operatorname{dim} E(0, T)\\\\
&= \operatorname{dim} E(\lambda_1, T) + \dots + \operatorname{dim} E(\lambda_m, T)\\\\
\end{aligned}
$$

Where the third line follows from 5.38.

If $0$ is not an eigenvalue of $T$, just disregard $E(0, T)$ and $\operatorname{dim} E(0, T)$ in each line.

_Exercise 11_

For the first column we have

$$
T(1, 4) = (41 + 28, -20 + 296) = (69, 276) = \mathbf{69}(1, 4) + \mathbf{0}(7,5)
$$

and the second

$$
T(7, 5) = (287 + 35, - 140 + 370) = (322, 230) = \mathbf{0}(1, 4) + \mathbf{46}(7, 5)
$$

_Exercise 12_

Let $v_1, v_2, v_3$ and $w_1, w_2, w_3$ be eigenvectors of $R$ and $T$, respectively, corresponding to $2, 6, 7$.
Note that the $v$'s and $w$'s are both bases of $\mathbb{F}^3$.
Define $S \in \mathcal{L}(\mathbb{F}^3)$ by

$$
\begin{aligned}
Sv_1 &= w_1\\\\
Sv_2 &= w_2\\\\
Sv_3 &= w_3\\\\
\end{aligned}
$$

It is easy to see that $S$ is invertible.
Thus

$$
\begin{aligned}
S^{-1}TS(a_1 v_1 + a_2 v_2 + a_3 v_3) &= S^{-1}T(a_1 w_1 + a_2 w_2 + a_3 w_3)\\\\
&= S^{-1}(2 a_1 w_1 + 6 a_2 w_2 + 7 a_3 w_3)\\\\
&= 2 a_1 v_1 + 6 a_2 v_2 + 7 a_3 v_3\\\\
&= R(a_1 v_1 + a_2 v_2 + a_3 v_3)\\\\
\end{aligned}
$$

Therefore $R = S^{-1}TS$.

_Exercise 13_

Suppose $R$ and $T$ are diagonalizable, and $R = \operatorname{diag}(2,6,7,7)$, $T = \operatorname{diag}(2,2,6,7)$ for natural basises. This means that $\operatorname{dim}E(7, T) = 1$ and $\operatorname{dim}E(7, R) = 2$. Denote $e_1,...,e_4$ as basis vectors. Suppose desired invertible $S$ exists, then

$Re_3 = 7e_3 = S^{-1}TSe_3$, and so $7Se_3 = TSe_3$, which means that $Se_3 \in E(7, T)$. By the same reasoning, $Se_4 \in E(7, T)$. Since $e_3,e_4$ are linearly independent and $S$ is injective, $Se_3, Se_4$ are also linearly independent, which implies that $\operatorname{dim}(E(7, T)) \ge 2$, which is a contradiction.

_Exercise 14_

Consider operator with the following matrix in standard basis

$$
A = \begin{pmatrix}
    6 & 0 & 0 \\
    0 & 7 & 1 \\
    0 & 0 & 7
\end{pmatrix}
$$

Since this is an upper triangular matrix, it is clear that 6 and 7 are the only eigenvalues of $T$. We see that $\operatorname{dim}\operatorname{null}(T - 6I) = 1$, because $u = (T - 6I)e_2 = e_2, v = (T - 6I)e_3 = e_2 + e_3$, and $v,u\in \operatorname{range}(T-6I)$ and $v,u$ are linearly independent, so $\operatorname{dim}\operatorname{range}(T-6I) \ge 2$, so by the fundamental theorem of linear maps $\operatorname{dim}\operatorname{null}(T-6I) \le 1$. 

By the same reasoning, $\operatorname{dim}\operatorname{null}(T-6I) \le 1$. If there were 3 linearly independent eigenvectors of $T$, at least two of them would correspond to the same eigenvalue, but we see that for both eigenspaces this leads to a contradiction.

_Exercise 15_

We are looking for a vector $v: Tv = 8v + w$, where $w = (17, \sqrt 5, w\pi)$. This implies $(T - 8I)v = w$. We know, that 8 is not an eigenvalue of $T$, therefore $T - 8I$ is injective and hence surjective, so, $\forall w \in V \exists v: (T - 8I)v = w$, which completes the proof. 

_Exercise 16_

_(a)_

We will prove by induction on $n$. When $n = 1$, the result is clearly true.

Assume it is true for $n$.
Then

$$
\begin{aligned}
T^{n+1} (0, 1) &= TT^n (0, 1)\\\\
&= T(F_n, F_{n+1})\\\\
&= (F_{n+1}, F_n + F_{n+1})\\\\
&= (F_{n+1}, F_{n+2})\\\\
\end{aligned}
$$

_(b)_

We need to find $(x, y)$ and $\lambda \in \mathbb{R}$ that satisfy $T(x, y) = \lambda(x, y)$.
Thus need to solve the following set of equations

$$
\begin{aligned}
\lambda x &= y\\\\
\lambda y &= x + y\\\\
\end{aligned}
$$

Substituting $y$ in the second equation and dividing both sides by $\lambda$, we get $y = \frac{1 + \lambda}{\lambda} x$.
Therefore, an eigenvector of $T$ has the form $\left(x, \frac{1 + \lambda}{\lambda} x\right)$ and we have

$$
T \left(x, \frac{1 + \lambda}{\lambda} x\right) = \left(\frac{1 + \lambda}{\lambda} x, \frac{1 + 2\lambda}{\lambda} x\right)
$$

We need then, to solve for $\lambda$ in the following equations

$$
\frac{1 + \lambda}{\lambda} = \lambda, \frac{1 + 2\lambda}{\lambda} = 1 + \lambda
$$

You can check that both are equivalent and have the solutions $\frac{1 + \sqrt{5}}{2}$ and $\frac{1 - \sqrt{5}}{2}$, which we will denote $\varphi$ and $\hat{\varphi}$.

_(c)_

Substituting the eigenvalues found in (b) on the eigenvector form $\left(x, \frac{1 + \lambda}{\lambda} x\right)$, we get

$$
(1, \varphi) \text{ and } (1, \hat{\varphi}).
$$

Both are linearly independent, since they are eigenvectors corresponding to distinct eigenvalues.
Thus, they are indeed a basis of $\mathbb{R}^2$.

_(d)_

Here we use the fact that if $\lambda$ is an eigenvalue of $T$ and $v$ a corresponding eigenvector then $T^k v = \lambda^k v$.
Since $(0, 1) = \frac{1}{\sqrt{5}} (0, \varphi - \hat{\varphi})$, we have

$$
\begin{aligned}
T^n (0, 1) &= \frac{1}{\sqrt{5}} T^n (0, \varphi - \hat{\varphi})\\\\
&= \frac{1}{\sqrt{5}} T^n ((1, \varphi) - (1, \hat{\varphi}))\\\\
&= \frac{1}{\sqrt{5}} \left[T^n (1, \varphi) - T^n (1, \hat{\varphi})\right]\\\\
&= \frac{1}{\sqrt{5}} \left[\varphi^n (1, \varphi) - \hat{\varphi}^n (1, \hat{\varphi})\right]\\\\
&= \frac{1}{\sqrt{5}} (\varphi^n - \hat{\varphi}^n, \varphi^{n+1} - \hat{\varphi}^{n+1})\\\\
\end{aligned}
$$

Therefore

$$
F^n = \frac{1}{\sqrt{5}} (\varphi^n - \hat{\varphi}^n) = \frac{1}{\sqrt{5}} \left[ \left(\frac{1 + \sqrt{5}}{2}\right)^n - \left(\frac{1 - \sqrt{5}}{2}\right)^n \right]
$$

_(e)_

This follows directly from the fact that $\frac{1}{\sqrt{5}} \left|\frac{1 - \sqrt{5}}{2}\right|^n < \frac{1}{2}$, for all positive integers $n$, which we will prove by induction.

When $n = 1$, we have

$$
\begin{aligned}
\frac{1}{\sqrt{5}} \left| \frac{1 - \sqrt{5}}{2} \right| &= \frac{1}{\sqrt{5}} \frac{\sqrt{5} - 1}{2}\\\\
&= \frac{5 - \sqrt{5}}{10}\\\\
&< \frac{5}{10}\\\\
&= \frac{1}{2}\\\\
\end{aligned}
$$

Assume the result holds true for $n$.
Then

$$
\begin{aligned}
\frac{1}{\sqrt{5}} \left| \frac{1 - \sqrt{5}}{2} \right|^{n + 1} &=
\left| \frac{1 - \sqrt{5}}{2} \right|
\frac{1}{\sqrt{5}}
\left| \frac{1 - \sqrt{5}}{2} \right|^n
\\\\
&< \left| \frac{1 - \sqrt{5}}{2} \right| \frac{1}{2}\\\\
&= \frac{\sqrt{5} - 1}{2} \cdot \frac{1}{2}\\\\
&< \frac{\sqrt{9} - 1}{2} \cdot \frac{1}{2}\\\\
&= \frac{1}{2}\\\\
\end{aligned}
$$
