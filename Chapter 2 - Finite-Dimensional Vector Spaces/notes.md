Chapter 2: **Finite-Dimensional Vector Spaces**

**Theorem 1.**
Suppose that $V$ is finite-dimensional and $U$ and $W$ are subspaces of $V$.
There is a basis $v_1, \dots, v_n, u_1, \dots, u_m, w_1, \dots, w_p$ of $U + W$ such that $v_1, \dots, v_n$ is a basis of $U \cap W$, $v_1, \dots, v_n, u_1, \dots, u_m$ is a basis of $U$ and $v_1, \dots, v_n, w_1, \dots, w_p$ is a basis of $W$.

_Proof_

Let $v_1, \dots, v_n$ be a basis of $U \cap W$.
Extend it a basis $v_1, \dots, v_n, u_1, \dots, u_m$ of $U$ and a basis $v_1, \dots, v_n, w_1, \dots, w_p$ of $W$.
Suppose there are $a_1, \dots, a_n, b_1, \dots, b_m, c_1, \dots, c_p \in \mathbb{F}$ such that

$$
a_1 v_1 + \dots + a_n v_n + b_1 u_1 + \dots + b_m u_m + c_1 w_1 + \dots + c_p w_p = 0
$$

We have

$$
a_1 v_1 + \dots + a_n v_n + b_1 u_1 + \dots + b_m u_m = - c_1 w_1 - \dots - c_p w_p
$$

Which implies that $- c_1 w_1 - \dots - c_p w_p$ is in $U$ and, therefore, in $U \cap W$ too.
Hence, there are scalars $d_1, \dots, d_n \in \mathbb{F}$ such that

$$
d_1 v_1 + \dots + d_n v_n = - c_1 w_1 - \dots - c_p w_p
$$

Because $v_1, \dots, v_n, w_1, \dots, w_p$ is a basis of $W$, all the $c$'s (and $d$'s) are 0 and the right hand side of the previous equation becomes 0.
It quickly follows that all $a$'s and $b$'s are 0.
Thus $v_1, \dots, v_n, u_1, \dots, u_m, w_1, \dots, w_p$ is linearly independent.
<p align="right"> $\blacksquare$ </p>

