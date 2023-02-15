Chapter 8: **Operators on Complex Vector Spaces**

**8.C**

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
- [x] Exercise 19
- [x] Exercise 20

_Exercise 1_

Because

$$
4 = \operatorname{dim} \mathbb{C}^4 = \operatorname{dim} G(3, T) + \operatorname{dim} G(5, T) + \operatorname{dim} G(8, T),
$$

it follows that the multiplicities of the eigenvalues of $T$ are at most $2$.
Thus $p(z) = (z-3)^2(z-5)^2(z-8)^2$ is a polynomial multiple of the characteristic polynomial.
Therefore, we must have $p(T) = 0$.

_Exercise 2_

We have

$$
1 \le \dim G(5, T), \dim G(6, T) \le n - 1.
$$

Hence $p(z) = (z - 5I)^{n-1}(z - 6I)^{n-1}$ is a polynomial multiple of the characteristic polynomial.
Therefore, $p(T) = 0$.

_Exercise 3_

Define $T \in \mathcal{L}(\mathbb{C}^4)$ by

$$
T(z_1, z_2, z_3, z_4) = (7z_1, 7z_2, 8z_3, 8z_4).
$$

Since $E(7, T) \subset G(7, T), E(8, T) \subset G(8, T)$ and $\mathbb{C}^4 = E(7, T) \oplus E(8, T)$, it follows that $E(7, T) = G(7, T)$ and $E(8, T) = G(8, T)$.
We have $\dim E(7, T) = \dim E(8, T) = 2$.
Hence, the characteristic polynomial of $T$ is

$$
(z - 7)^2(z - 8)^2.
$$

_Exercise 4_

$$
A =
\begin{pmatrix}
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}
$$

Let

$$
A =
\begin{pmatrix}
1 & 1 & 0 & 0\\\\
0 & 5 & 1 & 0\\\\
0 & 0 & 5 & 0\\\\
0 & 0 & 0 & 5
\end{pmatrix}.
$$

Then

$$
\begin{aligned}
(A - 5I)^2(A - I) &=
\begin{pmatrix}
-4 & 1 & 0 & 0\\\\
0 & 0 & 1 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}^2
\begin{pmatrix}
0 & 1 & 0 & 0\\\\
0 & 4 & 1 & 0\\\\
0 & 0 & 4 & 0\\\\
0 & 0 & 0 & 4
\end{pmatrix}\\\\
&=
\begin{pmatrix}
-4 & 1 & 0 & 0\\\\
0 & 0 & 1 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}
\begin{pmatrix}
0 & 0 & 1 & 0\\\\
0 & 0 & 4 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}\\\\
&=
\begin{pmatrix}
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}.
\end{aligned}
$$

Define $T \in \mathcal{L}(\mathbb{C}^4)$ by

$$
T(z_1, z_2, z_3, z_4) = (z_1 + z_2, 5z_2 + z_3, 5z_3, 5z_4).
$$

Then $\mathcal{M}(T) = A$ and the eigenvalues of $T$ are thus $1$ and $5$ (the entries on the diagonal).
Now 8.36 implies that the minimal polynomial of $T$ is a polynomial multiple of $(z - 5)(z - 1)$.
The previous work shows that $(T - 5I)(T - I) \neq 0$ and $(T - 5I)^2(T - I) = 0$.
Hence $(z - 5)^2(z - 1)$ is the minimal polynomial of $T$.
By Exercise 11 in section 8B, the multiplicity of $1$ is $1$ and of $5$ is $3$.
Thereby the characteristic polynomial of $T$ is $(z - 1)(z - 5)^3$.

_Exercise 5_

Let

$$
A =
\begin{pmatrix}
0 & 0 & 0 & 0\\\\
0 & 1 & 1 & 0\\\\
0 & 0 & 1 & 0\\\\
0 & 0 & 0 & 3
\end{pmatrix}.
$$

Then

$$
\begin{aligned}
(A - I)^2(A - 3)A &=
\begin{pmatrix}
-1 & 0 & 0 & 0\\\\
0 & 0 & 1 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 2
\end{pmatrix}^2
\begin{pmatrix}
-3 & 0 & 0 & 0\\\\
0 & -2 & 1 & 0\\\\
0 & 0 & -2 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}
\begin{pmatrix}
0 & 0 & 0 & 0\\\\
0 & 1 & 1 & 0\\\\
0 & 0 & 1 & 0\\\\
0 & 0 & 0 & 3
\end{pmatrix}\\\\
&=
\begin{pmatrix}
-1 & 0 & 0 & 0\\\\
0 & 0 & 1 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 2
\end{pmatrix}^2
\begin{pmatrix}
0 & 0 & 0 & 0\\\\
0 & -2 & -1 & 0\\\\
0 & 0 & -2 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}\\\\
&=
\begin{pmatrix}
-1 & 0 & 0 & 0\\\\
0 & 0 & 1 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 2
\end{pmatrix}
\begin{pmatrix}
0 & 0 & 0 & 0\\\\
0 & 0 & -2 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}\\\\
&=
\begin{pmatrix}
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0\\\\
0 & 0 & 0 & 0
\end{pmatrix}.
\end{aligned}
$$

Define $T \in \mathcal{L}(\mathbb{C}^4)$ by

$$
T(z_1, z_2, z_3, z_4) = (0, z_2 + z_3, z_3, 3z_4).
$$

Then $\mathcal{M}(T) = A$.
The rest of this exercise is almost the same as the previous one.

_Exercise 6_

Define $T \in \mathcal{L}(\mathbb{C}^4)$ by

$$
T(z_1, z_2, z_3, z_4) = (0, z_1, z_2, 3z_4).
$$

Then, the standard basis of $\mathbb{C}^4$ consists of eigenvectors of $T$ corresponding to the eigenvalues $0, 1, 1, 3$.
Applying $T(T - I)(T - 3)$ to each of these basis vectors shows that $T(T - I)(T - 3) = 0$.
Hence $z(z-1)(z-3)$ is the minimal polynomial of $T$.
We have

$$
\mathcal{M}(T) =
\begin{pmatrix}
0 & 0 & 0 & 0\\\\
0 & 1 & 0 & 0\\\\
0 & 0 & 1 & 0\\\\
0 & 0 & 0 & 3
\end{pmatrix}.
$$

Thus, by Exercise 11 in section 8B, the characteristic polynomial of $T$ is $z(z-1)^2(z-3)$.

_Exerise 7_

By Exercise 4 in section 5B, we have

$$
V = \operatorname{null} P \oplus \operatorname{range} P. \tag{1}
$$

It is easy to check that if $v \in \operatorname{range} P$ then $Pv = v$.
Thus

$$
\operatorname{null} P \subset G(0, T) \text{ and } \operatorname{range} P \subset G(1, T).
$$

$(1)$ and 8.26 then imply that these inclusions are actually equalities, which gives the desired result.

_Exercise 8_

Let $p$ denote the minimal polynomial of $T$.
We have

$$
\begin{aligned}
T \text{ is invertible } &\iff 0 \text{ is not an eigenvalue of } T\\\\
&\iff p(0) \neq 0\\\\
&\iff \text{the consant term of $p$ is nonzero},
\end{aligned}
$$

where the equivalence between the first and second lines follows from 8.49.

_Exercise 9_

Since

$$
4 + 5T - 6T^2 - 7T^3 + 2T^4 + T^5 = 0,
$$

multiplying both sides by $T^{-5}$ we get

$$
4T^{-5} + 5T^{-4} - 6T^{-3} - 7T^{-2} + 2T^{-1} + I = 0.
$$

Hence $4z^5 + 5z^4 - 6z^3 - 7z^2 + 2z + 1$ is a polynomial multiple of the minimal polynomial of $T^{-1}$ (by 8.46).
As it turns out, this is actually the minimal polynomial of $T^{-1}$ (with the coefficients multiplied by $4$).
To see this, suppose by contradiction that it is not.
Hence, the minimal polynomial of $T$ has degree at most $4$.
This means that

$$
a_0 I + a_1 T^{-1} + a_2 T^{-2} + a_3 T^{-3} + a_4 T^{-4} = 0
$$

for some $a_0, a_1, a_2, a_3, a_4 \in \mathbb{F}$, not all equal $0$.
Multiplying both sides of the equation above by $T^4$, we get

$$
a_0 T^4 + a_1 T^3 + a_2 T^2 + a_3 T + a_4 I = 0,
$$

which is a contradiction, because the minimal polynomial of $T$ has degree $5$.

_Exercise 10_

Let $\lambda_1, \dots, \lambda_m$ denote the distinct eigenvalues of $T$ and $d_1, \dots, d_m$ their corresponding multiplicities.
Then

$$
p(z) = (z - \lambda_1)^{d_1}\cdots(z - \lambda_m)^{d_m}.
$$

The eigenvalues of $T^{-1}$ are $\frac{1}{\lambda_1}, \dots, \frac{1}{\lambda_m}$ and by Exercise 3 in section 8A they have multiplicities $d_1, \dots, d_m$.
Thus

$$
\begin{aligned}
q(z) &= \left(z - \frac{1}{\lambda_1}\right)^{d_1}\cdots\left(z - \frac{1}{\lambda_m}\right)^{d_m}\\\\
&= z^{d_1}\left(1 - \frac{1}{\lambda_1 z}\right)^{d_1}\cdots z^{d_m}\left(1 - \frac{1}{\lambda_m z}\right)^{d_m}\\\\
&= z^{d_1 + \dots + d_m}\left(1 - \frac{1}{\lambda_1 z}\right)^{d_1}\cdots \left(1 - \frac{1}{\lambda_m z}\right)^{d_m}\\\\
&= z^{\dim V}\left(1 - \frac{1}{\lambda_1 z}\right)^{d_1}\cdots \left(1 - \frac{1}{\lambda_m z}\right)^{d_m}\\\\
&= z^{\dim V} \frac{1}{\lambda_1^{d_1}}\left(\lambda_1 - \frac{1}{z}\right)^{d_1}\cdots \frac{1}{\lambda_m^{d_m}}\left(\lambda_m - \frac{1}{z}\right)^{d_m}\\\\
&= z^{\dim V} \frac{1}{\lambda_1^{d_1}\cdots\lambda_m^{d_m}}\left(\lambda_1 - \frac{1}{z}\right)^{d_1}\cdots\left(\lambda_m - \frac{1}{z}\right)^{d_m}\\\\
&= z^{\dim V} \frac{(-1)^{d_1 + \cdots + d_m}}{\lambda_1^{d_1}\cdots\lambda_m^{d_m}}\left(\frac{1}{z} - \lambda_1\right)^{d_1}\cdots\left(\frac{1}{z} - \lambda_m\right)^{d_m}\\\\
&= z^{\dim V} \frac{(-1)^{d_1 + \cdots + d_m}}{\lambda_1^{d_1}\cdots\lambda_m^{d_m}}p\left(\frac{1}{z}\right)\\\\
&= z^{\dim V} \frac{1}{p(0)} p\left(\frac{1}{z}\right).
\end{aligned}
$$

_Exercise 11_

Let $z^m + \dots + a_1z + a_0$ be the minimal polynomial of $T$.
Then

$$
a_0I = -T^m - \dots - a_1T
$$

Multiplying both sides of the equation above by $\frac{1}{a_0}T^{-1}$ gives the desired result (note that $a_0$ is nonzero by Exercise 8).

_Exercise 12_

Suppose $V$ has a basis consisting of eigenvectors of $T$.
Let $\lambda_1, \dots, \lambda_m$ denote the distinct eigenvalues of $T$.
Then, it is easy to see that

$$
(T - \lambda_1 I) \cdots (T - \lambda_m I) = 0
$$

by applying the left side of the equation to each of the basis vectors, because the parentheses commute.
By 8.46, $(z - \lambda_1) \cdots (z - \lambda_m)$ is a polynomial multiple of the minimal polynomial of $T$.
This polynomial has no repeated zeros.
Hence the minimal polynomial has no repeated zeros.

Conversely, suppose the minimal polynomial of $T$, call it $p$, has no repeated zeros.
By 8.23, $T$ has a basis of generalized eigenvectors.
Let $v$ be one vector in this basis.
Then $v \in G(\lambda, T)$ for some eigenvalue $\lambda$ of $T$.
By 8.49, $\lambda$ is zero of $p$.
Thus, we can write $p(z) = (z - \lambda)q(z)$ for some polynomial $q$ with $q(\lambda) \neq 0$.
We have

$$
0 = p(T)v = q(T)(T - \lambda)v.
$$

Note that $(T - \alpha)\hat{v} \neq 0$ for all nonzero $\hat{v} \in G(\lambda, T)$ and all $\alpha \in \mathbb{F}$ with $\alpha \neq \lambda$.
This implies that $(T - \lambda)v = 0$, since $G(\lambda, T)$ is invariant under every polynomial of $T$ and so $(T-\lambda I)v \neq 0$ implies $q(T)(T-\lambda I) \neq 0$ (because we can factor $q(T)$ and $\lambda$ is not a zero of $q$).
Therefore $v$ is an eigenvector of $T$ and the basis of $V$ consisting of generalized eigenvectors of $T$ actually consists of eigenvectors of $T$.

_Exercise 13_

If $\mathbb{F} = \mathbb{C}$, this follows directly from the previous exercise from the Complex Spectral Theorem (7.24).

Suppose $\mathbb{F} = \mathbb{R}$. Using 8.40, we know, that there is a unique monic polynomial of smallest degree, such that $p(T) = 0$.

Suppose $m$ is the degree of this polynomial, then we can state that there exist $a_0,...,a_m \in \mathbb{R}$ such that

$$
T^m = a_0 + a_1T + ... + a_{m-1} T^{m-1}
$$

Now, let us consider $T$ as an operator over $\mathbb{C}$. There is also a minimal monic polynomial $q \in \mathcal{P}(\mathbb{C})$ such that $q(T) = 0$. Suppose it has degree $k$ and so

$$
T^k = (b_0 + c_0i) + (b_1 + c_1i)T + ... + (b_{k-1} + c_{k-1}i)T^{k-1}
$$

It is clear, that $k \le m$, because $p \in \mathcal{F}(\mathbb{R}) \subset \mathcal{F}(\mathbb{C})$, $p$ is monic and $p(T) = 0$, so it must be $k = \operatorname{deg}q \le \operatorname{deg}p = m$.

$$
T^k - b_0 - b_1 T - ... - b_{k-1}T^{k-1} = i(c_0 + c_1T + ... + c_{k-1}T^{k-1})
$$

Fix any basis of $V$ when $V$ is considered a real vector space. It can be easily shown, that this set of vectors also form a basis of $V$ when it is considered as a complex vector space. On the left-hand side, we have an operator, which has real-valued coefficients when applied to any vector in $V$'s basis, while on the right-hand side, all the coefficients have 0 real part. This implies, that left part, as well as right part, are just 0 operators, and this, in turn, means that $k \ge m$, because any zero polynomial of $T$ over $\mathbb{R}$ should be a multiple of minimal polynomial, so it has degree no less, than $m$. It is also clear, that $c_0, ..., c_{k - 1}$ are all equal to zero, since else $c_0 + c_1T + ... + c_{k-1}T^{k-1}$ will be a polynomial of less than $m$ degree which is 0, which contradicts the fact that $p$ is minimal polynomial of $T$ over $\mathbb{R}$.

We already proved, that over $\mathbb{C}$ $T$ has a minimal polynomial with no repeated zeros. Since this minimal polynomial is the same over $\mathbb{R}$, we can conclude that it has no repeated real roots.

_Exercise 14_

As you can see in the solution to Exercise 10, the constant term in the characteristic polynomial, which equals $p(0)$, is is $1$ or $-1$ times the product of the eigenvalues of $S$ raised to the their respective multiplicities.
The eigenvalues of $S$ all have absolute value $1$ (see 7.43 (b)), hence $|p(0)| = 1$.

_Exercise 15_

_(a)_
Just repeat the proof of 8.40 replacing $I$ with $v$, $T^j$ with $T^jv$ and $n^2$ with $n$.

_(b)_
This is essentially the same as the proof of 8.46.

Let $q$ denote the minimal polynomial of $T$.
Then we also have $q(T)v = 0$.
Furthermore, $\deg q \ge \deg p$.
By the Division Algorithm for Polynomials (4.8), there exist $s, r \in \mathbb{P}(\mathbb{F})$ such that

$$
q = sp + r
$$

and $\deg r < \deg p$.
This implies that

$$
0 = q(T)v = s(T)p(T)v = r(T)v = r(T)v.
$$

By the same reasoning used in the proof, it follows that $r = 0$.

_Exercise 16_

We have

$$
a_0I + a_1T + a_2T^2 + \dots + a_{m-1}T^{m-1} + T^m = 0.
$$

Taking the adjoint of it side yields

$$
\overline{a_0}I + \overline{a_1} T^* + \overline{a_2} (T^*)^2 + \dots + \overline{a_{m-1}}(T^*)^{m-1} + (T^*)^m = 0
$$

and we see that the minimal polynomial of $T^*$ is

$$
\overline{a_0} + \overline{a_1} z + \overline{a_2} z^2 + \dots + \overline{a_{m-1}}z^{m-1} + z^m.
$$

To see this, suppose by contradiction this is not the minimal polynomial of $T^*$.
Let $p$ denote the minimal polynomial of $T^*$.
Then $\deg p < m$. Because $p(T^*) = 0$, taking the adjoing of each side as we did above shows that $\overline{p}(T) = 0$, where $\overline{p}$ equals $p$ with conjugated coefficients.
But $\deg \overline{p} < m$, which is a contradiction because the minimal polynomial of $T$ has degree $m$.

_Exercise 17_

The characteristic polynomial of $T$, call it $q$, has degree $\dim V$ (see 8.36) and is a polynomial multiple of the minimal polynomial of $T$ (see 8.48), call it $p$.
Because $q$ is a multiple of $q$, it follows that $q = ps$ for some polynomial $s$ and, because $\deg q = \deg p$, it follows that $\deg s = 0$.
Hence $s$ is a constant.
Since they're both monic, $s = 1$ and they should be equal.

_Exercise 18_

First, let us consider equations on eigenvalues. Suppose $(x_1, x_2, ..., x_n)$ is an eigenvector corresponding to eigenvalue $\lambda$. Then we can write:

$$
\begin{cases}
\lambda x_0 = -a_0x_{n-1}\\
\lambda x_1 = x_0 - a_1x_{n-1}\\
...\\
\lambda x_{n-1} = x_{n-2} - a_{n-1}x_{n-1}
\end{cases}
$$

Let us multiply $i$'th equation in this system by $\lambda^{i-1}$:

$$
\begin{cases}
\lambda x_0 = -a_0x_{n-1}\\
\lambda^2 x_1 = \lambda x_0 - a_1\lambda x_{n-1}\\
\lambda^3 x_2 = \lambda^2 x_1 - a_2\lambda^2 x_{n-1}\\
...\\
\lambda^{n} x_{n-1} = \lambda^{n-1}x_{n-2} - a_{n-1}\lambda^{n-1}x_{n-1}
\end{cases}
$$

We can now sequentially substitute left part from $k$'th equation into right part of $k+1$st equation, getting

$$
\lambda^{k + 1} x_{k} = -a_0x_{n-1} -a_1\lambda x_{n-1} - .... - a_{k}\lambda^{k} x_{n-1}
$$

So, for the last one, we obtain

$$
\lambda^{n} x_{n-1} = -a_0x_{n-1} -a_1\lambda x_{n-1} - .... - a_{n-1}\lambda^{n-1} x_{n-1}
$$

Hence 

$$
(\lambda^{n} + a_{n-1}\lambda^{n-1} + ... + a_1\lambda +a_0)x_{n-1} = 0
$$

Left part turns zero if either first or second factor is 0. Suppose at first that $x_{n-1} = 0$. Then, from the last equation from the initial system we conclude that $x_{n-2} = 0$, this implies that $x_{n-3} = 0$ and so on. Therefore, if $x_{n-1} = 0$, then all the coefficients of vector must be zero, so it won't be eigenvector, and this means that $x_{n-1}\neq 0$. 

Now, this means that 

$$
\lambda^{n} + a_{n-1}\lambda^{n-1} + ... + a_1\lambda +a_0 = 0
$$

It is easy to show, that if $\lambda$ is a zero of the above polynomial, we can consequitively find unique solution for $x_i$, supposing that $x_{n-1}=1$: 

$$
\begin{align}
x_{n-1} &= 1\\
x_{n-2} &= a_{n-1} + \lambda \\
x_{n-3} &= a_{n-2} + a_{n-1}\lambda + \lambda^2\\
... & \\
x_0 &= a_1 + a_2\lambda + ... + \lambda^{n-1}
\end{align}
$$

and so all the eigenvalues of the operator are zeros of the above polynomial. However, it is not yet clear whether this polynomial is minimal or characteristic polynomial of given operator, since the multiplicities of roots may differ in those two polynomials, even though all the mentioned polynomials have the same set of roots. We will now try to prove, that this polynomial is in fact minimal (and hence, characteristic, because it is monic and its degree is n).

First let us prove that minimal polynomial has in fact degree $n$. To do it, we will prove lemma: $A^j$ has a form 

$$
A^j = \begin{pmatrix}
  0 & 0 & ... & 0 & -a_0 & ... \\
  0 & 0 & ... & 0 & -a_1 & ... \\
  ... & ... & ... & ... & ... & ... \\
  1 & 0 & ... & 0 & -a_{j} & ... \\
  0 & 1 & ... & 0 & -a_{j + 1} & ... \\
  ... & ... & ... & ... & ... & ... \\
  0 & 0 & ... & 1 & -a_{n - 1} & ... \\
\end{pmatrix}
$$

In short, $A_{j+1, 1} = A_{j+2, 2} = ... = A_{n, n - j} = 1$, $A_{i,n - j + 1} = -a_{i - 1}$ for all $i = 1..n$, and $A_{ij} = 0$ for all other $i = 1..n$, $j = 1..n - j$.

This is obviously true for $j = 1$, and it is also true for $j = 0$ if we agree to ignore all the values which do not fit into matrix size (since for $j = 0$ it doesn't make sense to talk about $A_{i,n - j + 1}$ for any $i$).

To prove this statement, we can use induction. Suppose this is true for $A^j$, consider now $A^{j+1} = A\cdot A^j$. 
....

Consider now minimal polynomial $p(z)$, and suppose its least power term having non-zero coefficient is $c_jz^j$ (such monomial exists since $p(z) \neq 0$). This means, that $p(A)$ matrix gets $c_j \neq 0$ as a coefficient in position $(j + 1,1)$. By the above lemma, no powers of $A$ in range $0..n$ except $A^j$ and $A^{n}$ can have non-zero coefficient in this position, so to make it $p(A)_{j+1,1}$ zero, we must add properly scaled $A^{n}$. This implies, that $p(z)$ has a degree of at least $n$. On the other hand, we know that characteristic polynomial has a degree of $n$ by Cayley–Hamilton theorem, and that minimal polynomial has a degree not greater than that of characteristic polynomial. This implies, that $\operatorname{deg}p(z) = n$.

Now that we proved minimal polynomial has a degree of $n$, it must be that minimal polynomial and characteristic polynomial are the same, since they have the same degree, minimal polynomial divides characteristic polynomial and they both are monic.

Finally, we have already understood, that minimal polynomial contains term $z^n$ (since it has a degree $n$ and is monic, so the coefficient is 1). Suppose $p(z) = z^n + c_{n-1}z^{n-1} + ... + c_1z + c_0$ We know that $p(A) = 0$, which implies, that $0 = p(A)_{i,1} = A^n_{i,1} + c_{i - 1}A^{i-1} = -a_{i-1} + c_{i - 1}$, where the last two equations follow from the above lemma. 

This means, that $c_{i-1} = a_{i-1}$, and so in fact minimal and characteristic polynomials are both 

$$
p(z) = z^{n} + a_{n-1}z^{n-1} + ... + a_1z +a_0 
$$

_Exercise 19_

This follows directly from Exercise 11 in section 8B.

_Exercise 20_

This is a bit obvious if you realize that

$$
\dim G(\lambda, T) = \dim G(\lambda, T|_{V_1}) + \dots + G(\lambda, T|_{V_m}) \tag{2}
$$

for every $\lambda \in \mathbb{F}$.
This is true because the subspaces on the right side of the equation are contained in $G(\lambda, T)$ and because when we write each $V_j$ as a direct sum of generalized eigenspaces of $T|_{V_j}$ in the equation

$$
V = V_1 \oplus \dots \oplus V_m
$$

the only way the dimensions will fit is if $(2)$ is true.
