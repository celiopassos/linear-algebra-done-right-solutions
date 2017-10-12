Chapter 3: **Linear Maps**

**3.E**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [ ] Exercise 4
- [ ] Exercise 5
- [ ] Exercise 6
- [ ] Exercise 7
- [ ] Exercise 8
- [ ] Exercise 9
- [ ] Exercise 10
- [ ] Exercise 11
- [ ] Exercise 12
- [ ] Exercise 13
- [ ] Exercise 14
- [ ] Exercise 15
- [ ] Exercise 16
- [ ] Exercise 17
- [ ] Exercise 18
- [ ] Exercise 19
- [ ] Exercise 20

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

where the second line follows because $T$ is linear and the third by definition of $\operatorname{graph of} T$.
Hence $\operatorname{graph of} T$ is closed under addition.
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
Hence $T$ satiesfies the additivity property of linear maps.
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

Thus $T$ is obviously surjective.
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

Therefore $x_j = z_j$ and $y_j = w_j$ for each $j$.
Hence

$$
\big((x_1, x_2, x_3, \dots), (y_1, y_2, y_3, \dots)\big) = \big((z_1, z_2, z_3, \dots), (w_1, w_2, w_3, \dots)\big)
$$

and so $T$ is injective.
Thus $T$ is an isomorphism, as desired.
