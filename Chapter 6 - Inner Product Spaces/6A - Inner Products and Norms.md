Chapter 6: **Inner Product Spaces**


**6.A**

- [x] Exercise 1
- [x] Exercise 2
- [ ] Exercise 3
- [x] Exercise 4
- [x] Exercise 5
- [x] Exercise 6
- [x] Exercise 7
- [x] Exercise 8
- [ ] Exercise 9
- [ ] Exercise 10
- [x] Exercise 11
- [x] Exercise 12
- [x] Exercise 13
- [x] Exercise 14
- [x] Exercise 15
- [ ] Exercise 16
- [ ] Exercise 17
- [ ] Exercise 18
- [x] Exercise 19
- [x] Exercise 20
- [ ] Exercise 21
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
