Chapter 10: **Trace and Determinant**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [x] Exercise 5
- [ ] Exercise 6
- [x] Exercise 7
- [x] Exercise 8
- [ ] Exercise 9
- [ ] Exercise 10
- [ ] Exercise 11
- [ ] Exercise 12

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
\sum_{j=1}^n \prod_{k \neq j} \lambda_k.
$$

More succinctly, assuming $0$ is not an eigenvalue of $T$:

$$
\sum_{j=1}^n \frac{\det T}{\lambda_j}.
$$

_Exercise 4_

This is follows easily from the definitions.
If $\lambda$ is an eigenvalue of $T$, or $T_\mathbb{C}$, then $c\lambda$ is an eigenvalue of $cT$, or $(cT)\_\mathbb{C}$, with equal multiplicity.
Let $\lambda_1, \dots, \lambda_n$ denote the eigenvalues of $T_\mathbb{C}$, repeated according to its multiplicity.
Then $c\lambda_1, \dots, c\lambda_n$ are the eigenvalues of $(cT)\_\mathbb{C}$ and we have

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
By the same reasoning used in 10.35, the determinant of $\mathcal{M}(T^\*)$ is also the product of the entries on diagonal.
The diagonal entries of $\mathcal{M}(T^\*)$ are the conjugates of the diagonal entries of $\mathcal{M}(T)$.
Hence $\det \mathcal{M}(T^\*) = \overline{\det \mathcal{M}(T)}$.
Now 10.42 implies that $\det T^\* = \overline{\det T}$.

Form 10.44, we have

$$
(\det \sqrt{T^\*T})^2 = \det (\sqrt{T^\*T}\sqrt{T^\*T}) = \det (T^\*T) = \det T^\* \det T = \overline{\det T} \det T = \left|\det T\right|^2.
$$

Taking the square root of each side we get $\det \sqrt{T^\*T} = \left|\det T\right|$.
