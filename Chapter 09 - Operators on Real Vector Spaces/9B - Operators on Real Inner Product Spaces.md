Chapter 9: **Operators on Real Vector Spaces**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [x] Exercise 5
- [x] Exercise 6
- [x] Exercise 7
- [x] Exercise 8

_Exercise 1_

Choose an orthonormal basis of $\mathbb{R}^3$ that puts the matrix of $S$ in the form given by 9.36.
Since $\mathcal{M}(S)$ is a $3$-by-$3$ matrix, one of the diagonal blocks is a $1$-by-$1$ matrix containing $1$ or $-1$.
Hence $Sx = x$ or $Sx = -x$ for some nonzero vector $x$ in the chosen basis.
Applying $S$ again in the two cases gives $S^2x = x$, as desired.

Geometrically speaking, an isometry on $\mathbb{R}^3$ is a rotation about an axis, perhaps with a reflexion through a plane orthogonal to the axis.
Hence an isometry on $\mathbb{R}^3$ either sends the vectors in the axis to themselves or to their reflexion.
If it's the first case, we already have what we wanted to prove, if it's the second, applying the isometry again sends the reflexions of the vectors back to the vectors themselves.

_Exercise 2_

This basically the same as the previous exercise.
Every operator on an odd-dimensional vector space has $n$-by-$n$ matrix for some odd integer $n$, hence one of the diagonal blocks is a $1$-by-$1$ matrix containing $1$ or $-1$.
The basis vector that corresponds to column where this vector appears is an eigenvector corresponding to $1$ or $-1$.

_Exercise 3_

For $u_1, u_2, v_1, v_2 \in V$ we have

$$
\begin{aligned}
\langle (u_1 + iv_1) + (u_1 + iv_2), x + iy \rangle &= \langle (u_1 + u_2) + i(v_1 + v_2), x + iy \rangle\\\\
&= \langle u_1 + u_2, x \rangle + \langle v_1 + v_2, y \rangle + \big(\langle v_1 + v_2, x \rangle - \langle u_1 + u_2, y \rangle\big)i\\\\
&= \langle u_1, x \rangle + \langle u_2, x \rangle +\langle v_1, y \rangle + \langle v_2, x \rangle + \big(\langle v_1, x \rangle - \langle u_1, y \rangle\big)i + \big(\langle v_2, x \rangle - \langle u_2, y \rangle\big)i\\\\
&= \langle u_1 + iv_1, x + iy \rangle + \langle u_2 + iv_2, x + iy \rangle.
\end{aligned}
$$

Therefore it satisfies additivity in the first slot.
For $a, b \in \mathbb{R}$, we have

$$
\begin{aligned}
\langle (a + bi)(u + iv), x + iy \rangle &= \langle (au - bv) + i(av + bu), x + iy \rangle\\\\
&= \langle au - bv, x \rangle + \langle av + bu, y \rangle + \big(\langle av + bu, x \rangle - \langle au - bv, y \rangle\big)i\\\\
&= \langle au, x \rangle - \langle bv, x \rangle + \langle av, y \rangle + \langle bu, y \rangle + \big(\langle av, x \rangle - \langle au, y \rangle\big)i + (\langle bu, x \rangle + \langle bv, y \rangle)i\\\\
&= \langle au, x \rangle + \langle av, y \rangle + \big(\langle av, x \rangle - \langle au, y \rangle\big)i - \langle bv, x \rangle + \langle bu, y \rangle + (\langle bu, x \rangle + \langle bv, y \rangle)i\\\\
&= a\langle u + iv, x + iy \rangle + bi\big(i\langle v, x \rangle - i\langle u, y \rangle + \langle u, x \rangle + \langle v, y \rangle\big)\\\\
&= a\langle u + iv, x + iy \rangle + bi\langle u + iv, x + iy \rangle\\\\
&= (a + bi)\langle u + iv, x + iy \rangle
\end{aligned}
$$

Hence homogeneity in the first slot is satisfied.
For positivity, we have

$$
\langle u + iv, u + iv \rangle = \langle u, u \rangle + \langle v, v \rangle + \big(\langle v, u \rangle - \langle u, v \rangle\big)i = \langle u, u \rangle + \langle v, v \rangle \ge 0,
$$

where the second equality follows because $V$ is a real inner product space.
The equation above also displays definiteness, because the left side equals $0$ if and only if $u = v = 0$, in other words, if $u + iv = 0$.
For conjugate symmetry, we have

$$
\begin{aligned}
\langle u + iv, x + iy \rangle &= \overline{\langle u, x \rangle + \langle v, y \rangle - (\langle v, x \rangle - \langle u, y \rangle)i}\\\\
&= \overline{\langle x, u \rangle + \langle y, v \rangle - (\langle x, v \rangle - \langle y, u \rangle)i}\\\\
&= \overline{\langle x + iy, u + iv \rangle}.
\end{aligned}
$$

_Exercise 4_

Choose an orthonormal basis of $V$.
Then this is also a basis of $V_\mathbb{C}$, see (9.4).
We have

$$
\mathcal{M}(T_\mathbb{C}) = \mathcal{M}(T) = \mathcal{M}(T^\*) = \mathcal{M}((T^\*)\_\mathbb{C}) = \mathcal{M}((T_\mathbb{C})^\*),
$$

where the first and third equalities follow from 9.7, the second from 7.10 and the fourth from 9.30 (c) (take $U = V$).
This implies that $T_\mathbb{C} = (T_\mathbb{C})^\*$.

_Exercise 5_

Suppose $V$ is a real inner product space and $T \in \mathcal{L}(V)$ is self-adjoint.
Then $T_\mathbb{C}$ is a self-adjoint operator on the complex inner product space $V_\mathbb{C}$ defined in Exercise 3.
By the Complex Spectral Theorem, there is an orthonormal basis $e_1 + if_1, \dots, e_n + if_n$ of $V_\mathbb{C}$ consisting of eigenvectors of $T_\mathbb{C}$.
By 7.13, the eigenvalues of $T_\mathbb{C}$ are all real.
Thus, there are $\lambda_1, \dots, \lambda_n \in \mathbb{R}$ such that

$$
Te_j + iTf_j = T_\mathbb{C}(e_j + if_j) = \lambda_j e_j + i \lambda_j Tf_j
$$

for each $j$.
The equation above shows that the $e$'s and $f$'s are eigenvectors of $T$.
Fix $j \in \\{1, \dots, n\\}$.
Let $e_1' + if_1', \dots, e_{d(\lambda_j)}' + if_{d(\lambda_j)}'$ denote the basis vectors that correspond to $\lambda_j$, where $d(\lambda_j) = \dim E(\lambda_j, T_\mathbb{C})$.
Then the list

$$
e_1', f_1', \dots, e_{d(\lambda_j)}', f_{d(\lambda_j)}' \in E(\lambda_j, T)
$$

is in $E(\lambda_j, T)$.
Since $E(\lambda, T_\mathbb{C})$ is contained in the complex span of the list above, it follows that the dimension of the compelx span of the list above is at least $d(\lambda_j)$.
Thus, by 9.4, the dimension of the real span of the list above is at least $d(\lambda_j)$.
Hence $\dim E(\lambda_j, T) \ge d(\lambda_j)$.
Because

$$
\dim E(\lambda_1, T) + \dots + \dim E(\lambda_n, T) \le \dim V
$$

and

$$
d(\lambda_1) + \dots + d(\lambda_n) = \dim V
$$

we must have $\dim E(\lambda_j, T) = d(\lambda_j)$ for each $j$.
The sum of eigenspaces corresponding to different eigenvalues is a direct sum.
The equation above thus shows that the sum of the eigenspaces of $T$ has the same dimension as $V$.
This means that

$$
E(\lambda_1, T) \oplus \dots \oplus E(\lambda_n, T) = V.
$$

For each eigenspace of $T$, we can select an orthonormal basis.
Putting these bases together, we get a basis of $V$ (by the equation above) consisting of eigenvectors of $T$.
By 7.22, this basis is orthonormal.

_Exercise 6_

Define $T \in \mathcal{L}(\mathbb{R}^2)$ by

$$
T(x, y) = (x + y, y).
$$

Then $\operatorname{span}((1, 0))$ is invariant under $T$, however, its orthogonal complement, namely $\operatorname{span}((0, 1))$, is not, because

$$
T(0, 1) = (1, 1) \not \in \operatorname{span}((0, 1)).
$$

_Exercise 7_

We have

$$
\mathcal{M}(T_1 \cdots T_m) = \mathcal{M}(T_1) \cdots \mathcal{M}(T_m) = \mathcal{M}(T),
$$

where the second equality follows from Exercise 9 in section 8B.
The left and right side of the equation above imply that $T_1 \cdots T_m = T$.

_Exercise 8_

Define

$$
e_j = \frac{\cos jx}{\sqrt{\pi}} \text{ and } f_j = \frac{\sin jx}{\sqrt{\pi}}
$$

for each $j = 1, \dots, n$.
By Exercise 4 in section 6B, the list $\frac{1}{\sqrt{2\pi}}, f_1, e_1, \dots, f_n, e_n$ is an orthonormal basis of $V$.
Note that $D\frac{1}{\sqrt{2\pi}} = 0$, $Df_j = je_j$ and $De_j = -jf_j$.
Hence, the matrix of $D$ with respect to this basis has the desired form, where the first block is the $1$-by-$1$ matrix $\begin{pmatrix}0\end{pmatrix}$ and others are of the form

$$
\begin{pmatrix}
0 & -j\\\\
j & 0
\end{pmatrix}
$$

for some $j \in \\{1, \dots, n\\}$.
