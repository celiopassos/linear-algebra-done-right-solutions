Chapter 6: **Inner Product Spaces**


**6.A**

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
- [x] Exercise 22
- [x] Exercise 23
- [x] Exercise 24
- [x] Exercise 25
- [x] Exercise 26
- [ ] Exercise 27
- [ ] Exercise 28
- [ ] Exercise 29
- [ ] Exercise 30
- [ ] Exercise 31

_Exercise 1_

It does not satisfy homogeneity on the first slot when $\lambda$ is negative.

_Exercise 2_

It does not satisfy the definiteness property if we let the first and third slots equal zero but the second non-zero.

_Exercise 3_

Let $v \in V: \langle v,v\rangle > 0$. Suppose $\exists u \in V: \langle u, u \rangle < 0$. It is clear, that $u,v$ are linearly independent: suppose they are not. Then $u = \lambda v$ for some $\lambda \in \mathbb{F}$, which implies that $\langle u, u \rangle = \lambda^2\langle v, v \rangle \ge 0$, and this is a contradiction.

Consider vectors of the form $u + \lambda v$ for $\lambda \in \mathbb{F}$. Let us look for such $\lambda$ that $\langle (u + \lambda v), (u + \lambda v) \rangle = 0$. To find such $\lambda$, we need to solve 

$$
\langle u, u \rangle + 2 \lambda \langle u, v \rangle + \lambda^2\langle v, v \rangle = 0
$$

This is quadratic equation with respect to $\lambda$, so 

$$
\lambda_{1,2} = \frac{-2\langle u, v \rangle \plusmn \sqrt{(4\langle u, v \rangle^2 - 4\langle u, u \rangle\langle v, v \rangle)}}{2\langle v, v \rangle}
$$

The value in the denominator is known to be positive, and the value under the root is positive as well, hence $\lambda_{1,2}$ are well-defined. So, there is a vector $u + \lambda_1v$: it's squared norm is 0. However, this vector can't be 0 itself since we proved $u,v$ are linearly independent. So, we got a contradiction, hence $u$ doesn't exist.

_Exercise 4_

_(a)_
We have

$$
\begin{aligned}
\langle u + v, u - v \rangle &= \langle u, u \rangle - \langle u, v \rangle + \langle v, u \rangle - \langle v, v \rangle\\\\
&= \langle u, u \rangle - \langle v, v \rangle\\\\
&= ||u||^2 - ||v^2||\\\\
\end{aligned}
$$

_(b)_
This follows directly from the above.

_(c)_
Just look at the picture before 6.22.

_Exercise 5_

Suppose $v \in V$ such that $(T - \sqrt{2}I)v = 0$.
Then $Tv = \sqrt{2}v$.
This implies that $||v|| \ge ||Tv|| = ||\sqrt{2}v|| = \sqrt{2}||v||$.
Since $||v||$ cannot be negative, it follows that $||v|| = 0$.
Hence $v = 0$, showing that $T - \sqrt{2}I$ is injective and, therefore, invertible.

_Exercise 6_

Suppose $\langle u, v \rangle = 0$.
Note that $u$ is orthogonal to any multiple of $v$.
Then, by the Pythagorean Theorem (6.13), we have

$$
||u + av||^2 = ||u||^2 + |a| ||v||^2 \le ||u||^2.
$$

Taking the square root of both sides completes the forward direction.

For the converse, we will prove the contrapositive, that is, if $\langle u, v \rangle \neq 0$, then $||u|| > ||u + av||$ for some $a \in \mathbb{F}$.

Suppose $\langle u, v \rangle \neq 0$.
Note that neither $u$ nor $v$ can equal $0$.
We have

$$
\begin{aligned}
||u + av||^2 &= \langle u + av, u + av \rangle\\\\
&= \langle u, u \rangle + \langle u, av \rangle + \langle av, u \rangle + \langle av, av \rangle\\\\
&= ||u||^2 + \langle u, av \rangle + \langle av, u \rangle + |a|^2 ||v||^2\\\\
&< ||u||^2
\end{aligned}
$$

where the last line follows provided that $\langle u, av \rangle + \langle av, u \rangle + |a|^2 ||v||^2 < 0$.
By 6.14, we can write $u = cv + w$ for some $c \in \mathbb{F}$ and $w \in V$ such that $\langle v, w \rangle = 0$.
Note that $c \neq 0$, because $\langle v, v \rangle \neq 0$ and

$$
0 \neq \langle u, v \rangle = \langle cv + w, v \rangle = \langle cv, v \rangle + \langle w, v \rangle = c \langle v, v \rangle
$$

Choose $a = -c$, then

$$
\begin{aligned}
\langle u, av \rangle + \langle av, u \rangle + |a|^2 ||v||^2 &= \langle cv + w, av \rangle + \langle av, cv + w \rangle + |a|^2 ||v||^2\\\\
&= \langle cv, av \rangle + \langle w, av \rangle + \langle av, cv \rangle + \langle av, w \rangle + |a|^2 ||v||^2\\\\
&= c\bar{a} \langle v, v \rangle + a\bar{c} \langle v, v \rangle + |a|^2 ||v||^2\\\\
&= (c\bar{a} + a\bar{c} + ||c||^2) ||v||^2\\\\
&= (-c\bar{c} - c\bar{c} + ||c||^2) ||v||^2\\\\
&= - |c|^2 ||v||^2\\\\
&< 0\\\\
\end{aligned}
$$

_Exercise 7_

The forward direction is obvious, just choose $a = 1$ and $b = 0$ to get the desired result.

Conversely, suppose $||u|| = ||v||$.
Then

$$
\begin{aligned}
||au + bv|| &= \langle au + bv, au + bv \rangle\\\\
&= \langle au, au \rangle + \langle au, bv \rangle + \langle bv, au \rangle + \langle bv, bv \rangle\\\\
&= |a|^2 ||u||^2 + ab \langle u, v \rangle + ab \langle v, u \rangle + |b|^2 ||v||^2\\\\
&= |a|^2 ||v||^2 + ab \langle u, v \rangle + ab \langle v, u \rangle + |b|^2 ||u||^2\\\\
&= \langle av, av \rangle + \langle bu, av \rangle + \langle av, bu \rangle + \langle bu, bu \rangle\\\\
&= \langle bu + av, bu + av \rangle\\\\
&= ||bu + av||^2\\\\
\end{aligned}
$$

_Exercise 8_

We have

$$
\langle u - v, u - v \rangle = \langle u, u \rangle - \langle u, v \rangle - \langle v, u \rangle + \langle v, v \rangle = 1 - 1 - 1 + 1 = 0
$$

Thus $u - v = 0$, which implies that $u = v$.

_Exercise 9_

Using Cauchy-Schwartz inequality, we have that $|\langle u, v \rangle| < ||u||||v|| \le 1$, so the right-hand side of the inequality we are interested in is at least positive. We can then apply square to both sides of the inequality, so it is equivalent to 

$$
(1 - ||u||^2)(1 - ||v||^2) \le (1 - |\langle u, v \rangle|)^2
$$

We can strengthen this inequality substituting $||u||||v||$ instead of $|\langle u, v \rangle|$. 

$$
(1 - ||u||^2)(1 - ||v||^2) \le (1 - ||u||||v||)^2
$$

Which is equivalent to 

$$
-||u||^2 -||v||^2 \le -2||u||||v||
$$

But this is obviously correct, since 

$$
0 \le -2||u||||v|| + ||u||^2 + ||v||^2 = (||v|| - ||u||)^2
$$

_Exercise 10_

$u = \lambda(1,3)$. Since $v$ should be orthogonal to (1,3), $v = \beta(-3, 1)$. Since $u + v = (1,2)$, we get the following system

$$
\begin{cases}
    \lambda - 3\beta = 1 \\
    3\lambda + \beta = 2 
\end{cases}
$$

So, $\lambda = 0.7$, $\beta = -0.1$.

_Exercise 11_

Let $u = \left(\sqrt{a}, \sqrt{b}, \sqrt{c}, \sqrt{d}\right)$ and $v = \left(\frac{1}{\sqrt{a}}, \frac{1}{\sqrt{b}}, \frac{1}{\sqrt{c}}, \frac{1}{\sqrt{d}}\right)$.
Then, by 6.15, we have

$$
4 = |\langle u, v \rangle| \le ||u||\\:||v|| = \sqrt{a + b + c + d} \sqrt{\frac{1}{a} + \frac{1}{b} + \frac{1}{c} + \frac{1}{d}}.
$$

Taking the square of each side now gives the desired result.

_Exercise 12_

Take $x = (x_1, \dots, x_n)$ and $y = (1, \dots, 1)$ ($n$ ones).
By 6.15, we have

$$
|x_1 + \dots + x_n| = |\langle x, y \rangle| \le ||x||\\:||y|| = \sqrt{n}\sqrt{x_1^2 + \dots + x_n^2}
$$

Squaring each side now gives the desired result.

_Exercise 13_

From the Law of Cosines, we have

$$
\begin{aligned}
||u - v||^2 &= ||u||^2 + ||v||^2 - 2 ||u||\\:||v|| \cos \theta\\\\
||u||^2 - 2 \langle u, v \rangle + ||v||^2 &= ||u||^2 + ||v||^2 - 2||u||\\:||v|| \cos \theta\\\\
-2 \langle u, v \rangle &= -2 ||u||\\:||v|| \cos \theta\\\\
\cos \theta &= \frac{\langle u, v \rangle}{||u||\\:||v||}\\\\
\end{aligned}
$$

_Exercise 14_

The Cauchy-Schwarz Inequality ensures $\frac{\langle x, y \rangle}{||x||\\:||y||}$ is always a number between $-1$ and $1$.
Moreover it only equals $1$ or $-1$ if one of $x, y$ is a scalar multiple of the other, that is, when the angle is $0$ or $\pi$.

_Exercise 15_

Let $a = (\sqrt{1} a_1, \dots, \sqrt{n} a_n)$ and $b = \left(\frac{b_1}{\sqrt{1}}, \dots, \frac{b_n}{\sqrt{n}}\right)$.
Then

$$
\begin{aligned}
\left(\sum\limits_{j=1}^n a_j b_j\right) &= \left(\langle a, b \rangle\right)^2\\\\
&\le \left(||a||\\:||b||\right)^2\\\\
&= ||a||^2 ||b||^2\\\\
&= \left(\sum\limits_{j=1}^n j a_j^2\right) \left(\sum\limits_{j=1}^n \frac{b_j^2}{j}\right)\\\\
\end{aligned}
$$

where the second line follows from the Cauchy-Schwarz Inequality.

_Exercise 16_

We can use the parallelogram equality:

$$
16 + 36 = 2(9 + ||v||^2)
$$

So, $||v|| = \sqrt{17}$, since $||v|| \ge 0$.

_Exercise 17_

This is clearly wrong. Suppose $v = (-1,-1)$, then $||v|| = -1 < 0$, which contradicts definition of norm as $||v|| = \sqrt(v,v) > 0$.

_Exercise 18_

First let us notice, that it should be true that $(-1)^p > 0$, because else we can easily construct a vector $(x,-x)$ such that it has zero norm, however it is not zero itself. This implies, that $\forall x \in \mathbb{F}\ x^p = |x|^p = (-x)^p$.

Now, consider two vectors $u = (x, x)$ and $v = (x, -x)$, with $x > 0$. Using the parallelogram equation, we obtain

$$
||(2x, 0)||^2 + ||(0,2x)||^2 = 2(||(x,x)||^2 + ||(x,-x)||^2)
$$

It is clear, that $||(0, 2x)|| = ||(2x, 0)|| = ((2x)^p)^{\frac{1}{p}} = 2x$. On the otehr hand, $||(x,x)|| = ||(x,-x)|| = (2x^p)^{\frac{1}{p}} = 2^{\frac{1}{p}}x$.

Hence, we end up with equation

$$
8x^2 = 4\cdot 2^{\frac{2}{p}}x^2
$$

After contracting $4x^2$, we get $2 = 2^{\frac{2}{p}}$, and $p = 2$ is the only solution to this equation with respect to $p$.

_Exercise 19_

We have

$$
\begin{aligned}
||u + v||^2 - ||u - v||^2 &= \langle u+v, u+v \rangle - \langle u-v, u-v \rangle\\\\
&= \langle u, u \rangle + 2\langle u, v \rangle + \langle v, v \rangle - \left(\langle u, u \rangle - 2\langle u, v \rangle + \langle v, v \rangle\right)\\\\
&= 4\langle u, v \rangle\\\\
\end{aligned}
$$

Dividing by $4$ yields the desired result.

_Exercise 20_

We have

$$
\begin{aligned}
||u+v||^2 - ||u-v||^2 + ||u+iv||^2 i - ||u-iv||^2i &= \langle u+v, u+v \rangle - \langle u-v,u-v \rangle + \left( \langle u+iv, u+iv \rangle - \langle u-iv, u-iv \rangle \right)i\\\\
&= 2\langle u, v \rangle + 2\langle v, u \rangle + \left( 2\langle u, vi \rangle + 2\langle iv, u \rangle \right) i\\\\
&= 2\langle u, v \rangle + 2\langle v, u \rangle + \left(-2i\langle u, v \rangle + 2i\langle v, u \rangle \right) i\\\\
&= 4\langle u, v \rangle\\\\
\end{aligned}
$$

Dividing by $4$ yields the desired result.

_Exercise 21_

Suppose $U$ is a complex vector space, then we can use inner product definition through the norm function defined in the previous exercise. All is left is to check that such defined function will in fact satisfy all the properties of inner product.

_Exercise 22_

Let $x = (1, \dots, 1)$ ($n$ ones) and $a = (a_1, \dots, a_n)$.
Then

$$
\begin{aligned}
\left( \frac{a_1 + \dots + a_n}{n} \right)^2 &= \frac{|\langle x, a \rangle|^2}{n^2}\\\\
&\le \frac{||x||^2||a||^2}{n^2}\\\\
&= \frac{||a||^2}{n}\\\\
&= \frac{a_1^2 + \dots + a_n^2}{n}\\\\
\end{aligned}
$$

where the second line follows from the Cauchy-Schwarz Inequality.

_Exercise 23_

We have $\langle (v_1, \dots, v_m), (v_1, \dots, v_m) \rangle = \langle v_1, v_1 \rangle + \dots + \langle v_m, v_m \rangle$.
Positivity and definiteness follow directly from the fact that $\langle v_j, v_j \rangle \ge 0$ for each $j$.
The remaining properties follow easily from the definitions.

_Exercise 24_

For positivity, we have $\langle v, v \rangle_1 = \langle Sv, Sv \rangle \ge 0$.

For definiteness, suppose $\langle v, v \rangle_1 = 0$.
Then $\langle Sv, Sv \rangle = 0$, which implies that $Sv = 0$.
However $S$ is injective, thus $v = 0$.
Conversely, if $v = 0$, then $\langle v, v \rangle_1 = \langle Sv, Sv \rangle = \langle 0, 0 \rangle = 0$.

For additivity in the first slot, we have $\langle u + v, w \rangle_1 = \langle Su + Sv, Sw \rangle = \langle Su, Sw \rangle + \langle Sv, Sw \rangle = \langle u, w \rangle_1 + \langle v, w \rangle_1$.

For homogeneity, $\langle \lambda u, v \rangle_1 = \langle \lambda Su, Sv \rangle = \lambda \langle Su, Sv \rangle = \lambda \langle u, v \rangle_1$.

For conjugate symmetry, we have $\langle u, v \rangle_1 = \langle Su, Sv \rangle = \overline{\langle Sv, Su \rangle} = \overline{\langle v, u \rangle_1}$.

_Exercise 25_

If $S$ is not injective, then there exists a non-zero $v \in V$, such that $Sv = 0$.
But $\langle v, v \rangle_1 = \langle Sv, Sv \rangle = \langle 0, 0 \rangle = 0$, therefore $\langle \cdot, \cdot \rangle_1$ cannot satisfy the definiteness property of inner products.

_Exercise 26_

_(a)_

$$
\begin{aligned}
\langle f(t), g(t) \rangle' &= \lim_{h \to 0} \frac{\langle f(t+h), g(t+h) \rangle - \langle f(t), g(t) \rangle}{h}\\\\
&= \lim_{h \to 0} \frac{\langle f(t+h), g(t+h) \rangle - \langle f(t), g(t+h) \rangle + \langle f(t), g(t+h) \rangle - \langle f(t), g(t) \rangle}{h}\\\\
&= \lim_{h \to 0} \frac{\langle f(t+h) - f(t), g(t+h) \rangle + \langle f(t), g(t+h) - g(t) \rangle}{h}\\\\
&= \lim_{h \to 0} \frac{\langle f(t+h) - f(t), g(t+h) \rangle}{h} + \lim_{h \to 0} \frac{\langle f(t), g(t+h) - g(t) \rangle}{h}\\\\
&= \lim_{h \to 0} \langle \frac{f(t+h) - f(t)}{h}, g(t+h) \rangle + \lim_{h \to 0} \langle f(t), \frac{g(t+h) - g(t)}{h} \rangle\\\\
&= \langle f'(t), g(t) \rangle + \langle f(t), g'(t) \rangle\\\\
\end{aligned}
$$

_(b)_

We have

$$
\langle f(t), f(t) \rangle' = \langle f'(t), f(t) \rangle + \langle f(t), f'(t) \rangle = 2\langle f'(t), f(t) \rangle.
$$

However, $\langle f(t), f(t) \rangle'$ is $0$, because $\langle f(t), f(t) \rangle$ is constant (it equals $c^2$ for all $t$).
Thus $\langle f'(t), f(t) \rangle = 0$.

_(c)_

If $f(t)$ describes a trajectory on the surface of a sphere centered at the origin, then $f'(t)$ is perpendicular to $f(t)$.

_Exercise 27_

Let us select $u' = w - \frac{1}{2}(u + v)$, $v' = \frac{1}{2}(v - u)$, then we need to prove that

$$
||u'||^2 = \frac{||u' + v'||^2 + ||u' - v'||^2}{2} - \frac{4||v'||^2}{4}
$$

which can be easily regrouped to form parallelogram equality.

_Exercise 28_

Suppose there exist two such points $u,v$. Suppose $||w - u|| = ||w - v|| = c$. Consider $x = \frac{1}{2}(v + u) \in C$. Then, from the previous exercise, we know, that

$$
||w - x||^2 = c^2 - \frac{1}{4}||u-v||^2 < c^2 
$$

Since $u\neq v$, we end up with $x$ being closer to $w$, then $v,u$, which is a contradiction.

_Exercise 29_

_(a)_
We need to check 4 properties:

1. The distance from point to itself should be zero: $d(x,x) = ||x - x|| = ||0|| = 0$.
2. Positivity: if $x \neq y$, $d(x,y) = ||x - y|| > 0$, which holds because of definitieness of inner product.
3. Symmetry is obvious: $d(x,y) = ||x - y|| = |-1|||y - x|| = ||y - x|| = d(y,x)$
4. Triangle inequality: $||x - z|| \le ||x - y|| + ||y - z||$, which follows from triangle inequality for norms with $u = y - z$, $v = x - y$.

_(b)_

Suppose $x_1,...,x_n,...$ is a Cauchy sequence, so $\forall \varepsilon >0 \exists N: m,n > N \implies d(x_m,x_n) < \varepsilon$. We will choose orthonormal basis $e_1,...,e_n$, and represent $x_i = \sum\limits_{r=1}^nc_{ir}e_r$. Writing down Cauchy sequence condition, we have that given arbitrary $\varepsilon >0$ we can find $N \in \mathbb{N}$ such, that if $i,j > \mathbb{N}$, we have $||\sum\limits_{r=1}^n(c_{ir} - c_{jr})e_r|| < \varepsilon$, which implies $\sum\limits_{r=1}^n|c_{ir} - c_{jr}| < \varepsilon$, and so $|c_{ir} - c_{jr}| < \varepsilon$ for any $r=1..n$.

This means, that $\{c_{1r}, c_{2r}, ....\}$ is a Cauchy sequence in $\mathbb{F}$, and if $\mathbb{F}$ is real or complex numbers, then it converges to an element of $\mathbb{F}$, denote it $c_r$. Then, it is easy to show that $d(x_i, c) \rightarrow 0$, with $i \to \infty$, where $c = \sum\limits_{i=1}^nc_ie_i \in V$.

_(c)_

By the same logic, we can operate orthonormal basis of $U$, and hence the limit $c$ will be also in $U$, so it will be closed subset of $V$.

