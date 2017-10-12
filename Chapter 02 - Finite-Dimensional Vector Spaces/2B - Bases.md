Chapter 2: **Finite-Dimensional Vector Spaces**

**2.B**

- [ ] Exercise 1
- [ ] Exercise 2
- [ ] Exercise 3
- [ ] Exercise 4
- [ ] Exercise 5
- [ ] Exercise 6
- [ ] Exercise 7
- [x] Exercise 8

_Exercise 8_

Let $v \in V$.
Then $v = u + w$ for some $u \in U$ and $w \in W$.
Since $u$ is a linear combination of the $u$'s and $w$ a linear combination of the $w$'s, it follows that

$$
u_1, \dots, u_m, w_1, \dots, w_n
$$

spans $V$.

Now let $a_1, \dots, a_m, b_1, \dots, b_n \in \mathbb{F}$ such that

$$
a_1 u_1 + \dots + a_m u_m + b_1 w_1 + \dots + b_n w_n = 0.
$$

This is a sum of a vector in $U$ and a vector in $W$ (just group the $u$'s and $w$'s in separate parentheses).
Then, 1.44 implies that

$$
a_1 u_1 + \dots + a_m u_m = 0 \text{ and } b_1 w_1 + \dots + b_n w_n = 0.
$$

Since $u_1, \dots, u_m$ is linearly independent, the first equation above shows that $a_1 = \dots = a_m = 0$.
Similarly, the $b$'s are also $0$.
Therefore, the list

$$
u_1, \dots, u_m, w_1, \dots, w_n
$$

is linearly independent, that is, a basis of $V$.
