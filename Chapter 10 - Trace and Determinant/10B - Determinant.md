Chapter 10: **Trace and Determinant**

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

_Exercise 1_

Because $T_\mathbb{C}$ has no real eigenvalues, if $\lambda$ is an eigenvalue of $T_\mathbb{C}$, then $\overline{\lambda}$ is also an eigenvalue of $T_\mathbb{C}$ with equal multiplicity.
The determinant of $T_\mathbb{C}$, which equals the determinant of $T$, is thus a product of terms of the form $\lambda\overline{\lambda} = |\lambda|^2$, which are all greater than $0$, because $0$ is not eigenvalue of $T$.
Hence $\det T > 0$.

_Exercise 2_

By the previous exercise, $T$ has at least one eigenvalue $\alpha$, which is negative because $\det T < 0$.
Suppose by contradiction that $\alpha$ is the only eigenvalue of $T$.
Then this can't be the only eigenvalue of $T_\mathbb{C}$, otherwise the $\det T$ would equal $\lambda^{\dim V}$ which is positive (because $\dim V$ is even).
The other eigenvalues of $T_\mathbb{C}$ are nonreal, so they come in pairs and won't change sign of $\det T$.
It follows that $\det T$ is a product of absolute values times $\lambda$ raised to its multiplicity.
Thus the multiplicity of $\lambda$ must be odd.
This is a contradiction, because the sum of the multiplicities of the other eigenvalues of $T_\mathbb{C}$ is even (because they come in pairs) and the sum of all multiplicies must equal $\dim V$, which is even.
Hence, our assumption that $\lambda$ was the only eigenvalue of $T$ is false.

_Exercise 3_

_(a)_
The characteristic polynomial of $T$ is

$$
(z - \lambda_1) (z - \lambda_2) \cdots (z - \lambda_n).
$$

Expanding this product we see that the coefficient of $z^{n-2}$ is the sum of the products of all pairs of distinct eigenvalues.
In other words, it equals

$$
\lambda_1 \sum_{j=2}^n \lambda_j + \lambda_2 \sum_{j=3}^n \lambda_j + \dots + \lambda_{n-1} \sum_{j=n}^n \lambda_j.
$$

_(b)_
It equals the sum of the products of the eigenvalues of $T$ with one term missing:

$$
\sum_{j=1}^n \prod_{k \neq j} (-1)^{n-1}\lambda_k.
$$

More succinctly, assuming $0$ is not an eigenvalue of $T$:

$$
\sum_{j=1}^n (-1)^{n-1}\frac{\det T}{\lambda_j}.
$$

_Exercise 4_

This is follows easily from the definitions.
If $\lambda$ is an eigenvalue of $T$, or $T_\mathbb{C}$, then $c\lambda$ is an eigenvalue of $cT$, or $(cT)_\mathbb{C}$, with equal multiplicity.
Let $\lambda_1, \dots, \lambda_n$ denote the eigenvalues of $T_\mathbb{C}$, repeated according to its multiplicity.
Then $c\lambda_1, \dots, c\lambda_n$ are the eigenvalues of $(cT)_\mathbb{C}$ and we have

$$
\det (cT) = (c \lambda_1) \cdots (c \lambda_n) = c^{\dim V}\lambda_1 \cdots \lambda_n = c^{\dim V} \det T.
$$

_Exercise 5_

We give a counterexample.
Let $I$ be the identity operator on $\mathbb{R}^2$.
Then

$$
\det(I - I) = 0 \neq 2 = \det(I) + \det(-I).
$$

_Exercise 6_

As we know, 

$$
\operatorname{det}A = \sum\limits_{(m_1,..,m_n)\in \operatorname{perm}(n)}\operatorname{sign}(m_1,..,m_n)A_{m_1,1}...A_{m_n,n}
$$

Denote $n_i$ to be number of rows/columns in $A_i$. Since $A$ is block-diagonal, we can notice, that for every permutation, having $m_i > n_1$ for any $i = 1..n_1$ we have $A_{m_i,i} = 0$. This means, that the sum above has non-zero terms only for permutations which map range $1..n_1$ to range $1..n_1$. We can note, that for such permutations, all the inversions happen with $(i,j)$ which are either both $\le n_1$ or $\ge n_1$, which means that $\operatorname{sign}(m_1,...,m_n) = \operatorname{sign}(m_1,...,m_{n_1})\cdot \operatorname{sign}(m_{n_1+1},...,m_n)$ This means, that we can rewrite equation above as

$$
\begin{align}
\begin{split}
  \operatorname{det}A &= \sum\limits_{(m_1,..,m_{n_1})\in \operatorname{perm}(n_1)}\sum\limits_{(m_{n_1+1},..,m_{n})\in \operatorname{perm}([n_1+1,...,n])}\operatorname{sign}(m_{1},..,m_{n_1})\operatorname{sign}(m_{n_1 +1},..,m_n)A_{m_1,1}...A_{m_{n_1},n_1} A_{m_{n_1+1},n_1+1}...A_{m_n,n} \\
&= \sum\limits_{(m_1,..,m_{n_1})\in \operatorname{perm}(n_1)}\operatorname{sign}(m_{1},..,m_{n_1})A_{m_1,1}...A_{m_{n_1},n_1} \sum\limits_{(m_{n_1+1},..,m_{n})\in \operatorname{perm}([n_1+1,...,n])}\operatorname{sign}(m_{n_1 +1},..,m_n) A_{m_{n_1+1},n_1+1}...A_{m_n,n}\\
&= \operatorname{det}A_1 \sum\limits_{(m_{n_1+1},..,m_{n})\in \operatorname{perm}([n_1+1,...,n])}\operatorname{sign}(m_{n_1 +1},..,m_n) A_{m_{n_1+1},n_1+1}...A_{m_n,n}
\end{split}
\end{align}
$$

Continuing in this fashion, we can see that the same argument can be applied to ${m_{n_1+1},...,m_{n_1+n_2}}$: it should be permutation of ${n_1+1,..,n_1+n_2}$, and it goes further until eventually we get 

$$
\operatorname{det}A = \operatorname{det}A_1...\operatorname{det}A_m
$$

_Exercise 7_

From 10.16, we have

$$
\operatorname{trace} S = \operatorname{trace} A = \operatorname{trace} T
$$

and, from 10.42, we have

$$
\det S = \det A = \det T.
$$

_Exercise 8_

Suppose $\mathbb{F} = \mathbb{C}$.
Choose an orthonormal basis of $V$ with respect to which the matrix of $T$ is upper triangular.
Then, by 10.35, the determinant of $\mathcal{M}(T)$ equals the product of the entries on the diagonal.
By the same reasoning used in 10.35, the determinant of $\mathcal{M}(T^*)$ is also the product of the entries on diagonal.
The diagonal entries of $\mathcal{M}(T^*)$ are the conjugates of the diagonal entries of $\mathcal{M}(T)$.
Hence $\det \mathcal{M}(T^*) = \overline{\det \mathcal{M}(T)}$.
Now 10.42 implies that $\det T^* = \overline{\det T}$.

Form 10.44, we have

$$
(\det \sqrt{T^*T})^2 = \det (\sqrt{T^*T}\sqrt{T^*T}) = \det (T^*T) = \det T^* \det T = \overline{\det T} \det T = \left|\det T\right|^2.
$$

Taking the square root of each side we get $\det \sqrt{T^*T} = \left|\det T\right|$.

_Exercise 9_

Consider $y = (0,..,\delta x_i, 0, .., 0)$. We can write 

$$
\begin{align}
\sigma(x + y) - \sigma(x) &= \sigma(x_1, ..., x_i + \delta x_i, ... x_n) - \sigma(x_1,..,x_n) \\
&= (\sigma'_{x_i}(x_1,..,x_n) + \mathcal{o}(\delta x_i))\delta x_i
\end{align}
$$

In the equations above, $T$ is applied to a vector with 1 on $i$th position:
$$
\begin{align}
\operatorname{lim}_{y\to 0}\frac{||\sigma(x + y) - \sigma(x) - T(y)||}{||y||} &=_{y = (0,...\delta x_i, ...0)}
\operatorname{lim}_{\delta x_i \to 0}\frac{||(\sigma'_{x_i}(x_1,..,x_n) + \mathcal{o}(\delta x_i))\delta x_i - \delta x_iT(0,..,1,..0)||}{|\delta x_i|} \\
&= ||\sigma'_{x_i}(x_1,..,x_n) - T(0,...,1,...0)||
\end{align}
$$

We know that from inner product definition the only vector that has a zero norm is a zero vector, so $T(0,..1,..0) = \sigma'_{x_i}(x_1,..,x_n)$. This means, that on a standard basis $T$ is defined uniquely, and this means that it is defined uniquely on $\mathbb{R}^n$, so there exists only one such linear operator which satisfies the equation 10.56. 

_Exercise 10_

We need to substitute $\sigma(x) = Tx$ into 10.56:

Suppose $T' = S$, we will prove that $S = T$:

$$
\begin{align}
\operatorname{lim}_{y\to 0}\frac{||T(x + y) - T(x) - S(y)||}{||y||} &= \operatorname{lim}_{y\to 0}\frac{||T(x) + T(y) - T(x) - S(y)||}{||y||} \\
&= \operatorname{lim}_{y\to 0}\frac{||(T-S)(y)||}{||y||} \\
&= \operatorname{lim}_{y\to 0}\frac{||(T-S)(e_y)|| ||y||}{||y||}\\
&= \operatorname{lim}_{y\to 0}||(T-S)(e_y)|| = 0
\end{align}
$$

Where $y = ||y||e_y$. We see, that $(S-T)e_y = 0$ for arbitrary union vector $e_y$, so taking arbitrary orthonormal basis we conclude that $(S-T)$ is 0 on all vectors of this basis, hence $S-T = 0$, and so $S = T$. 

_Exercise 11_

The proof can be derived the same way we proved the uniqueness of $T$ in exercise 9.

_Exercise 12_

We know the volume of a unit ball, which is $\frac{4}{3}\pi$. It is easy to see that described ellipsoid is linearly shrinked unit ball with linear map $T(x,y,z) = (ax, by, cz)$. This linear map has $\operatorname{det}T = abc$, and so ellipsoid volume is $\frac{4}{3}\pi abc$