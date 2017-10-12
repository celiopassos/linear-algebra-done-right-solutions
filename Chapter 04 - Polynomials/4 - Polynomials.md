Chapter 4: **Polynomials**

- [ ] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [x] Exercise 5
- [x] Exercise 6
- [ ] Exercise 7
- [x] Exercise 8
- [ ] Exercise 9
- [ ] Exercise 10
- [ ] Exercise 11

_Exercise 2_

No. Both $x^m$ and $-x^m + 1$ are in the set, but $x^m + (-x^m + 1) = 1$ has degree 0, therefore the set is not closed under addition.

_Exercise 3_

No, $x^2$ and $-x^2 + x$ are both in the set, but $x^2 + (-x^2 + x) = x$ is not.

_Exercise 4_

Define $p \in \mathcal{P}(\mathbb{F})$ by

$$
p(z) = (z - \lambda_1) \dots (z - \lambda_m) (z - \lambda_1)^{n - m}
$$

Clearly $p(\lambda_1) = \dots = p(\lambda_m) = 0$, $\deg p = n$ and $p$ has no other zeros, as desired.

_Exercise 5_

Define $\Upsilon: \mathcal{P}_m(\mathbb{F}) \to \mathbb{F}^{m+1}$ by

$$
\Upsilon(p) = (p(z_1), \dots, p(z_{m+1}))
$$

We have that $\operatorname{null} \Upsilon = \\{0\\}$, because no polynomial in $\mathcal{P}_m(\mathbb{F})$ has $m + 1$ zeros.
Hence $\Upsilon$ is injective, proving the uniqueness part.
By the Fundamental Theorem of Linear Maps, it follows that

$$
\operatorname{dim} \operatorname{range} \Upsilon = \operatorname{dim} \mathcal{P}_m(\mathbb{F}) = \operatorname{dim} \mathbb{F}^{m+1}
$$

Therefore $\Upsilon$ is surjective, proving the existence part.

_Exercise 6_

Suppose $p$ has $m$ distinct zeros.
Let $\lambda$ be a zero of $p$.
Then

$$
p(z) = (z - \lambda)q(z)
$$

For some polynomial $q$.
Using the product rule, we get

$$
p'(z) = q(z) + (z - \lambda)q'(z)
$$

Because the zeros of $p$ are distinct, it follows that $\lambda$ is not a zero of $q$.
Therefore

$$
p'(\lambda) = q(\lambda) + (\lambda - \lambda)q'(\lambda) = q(\lambda) \neq 0
$$

Thus $\lambda$ is not a zero of $p'$, as desired.

_Exercise 8_

We will show that $Tp = q$ where $q$ is the polynomial such that $p(x) - p(3) = (x - 3)q(x)$.

Clearly, if $x \neq 3$ then $Tp = q$.

Suppose $x = 3$.
We have that 3 is a root of $p(x) - p(3)$.
Thus, by the same reasoning used in _Exercise 6_, it follows that

$$
(p - p(3))'(3) = q(3)
$$

But $p' = (p - p(3))'$, hence $Tp(3) = q(3)$.
Therefore $Tp = q$ and $Tp$ is indeed a polynomial.

To prove $T$ is linear, let $r, s \in \mathbb{P}(R)$ and $\alpha \in \mathbb{F}$. If $x \neq 3$, then

$$
T(r + s) = \frac{r + s - r(3) - s(3)}{x - 3} = \frac{r - r(3)}{x - 3} + \frac{s - s(3)}{x - 3} = Tr + Ts
$$

And

$$
T(\alpha r) = \frac{\alpha r - \alpha r(3)}{x - 3} = \alpha\frac{r - r(3)}{x - 3} = \alpha Tr
$$

If $x = 3$, then $T$ is linear by the properties of derivatives.
