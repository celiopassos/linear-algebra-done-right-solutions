Chapter 8: **Operators on Complex Vector Spaces**

**8.D**

- [x] Exercise 1
- [x] Exercise 2
- [x] Exercise 3
- [x] Exercise 4
- [x] Exercise 5
- [x] Exercise 6
- [x] Exercise 7
- [x] Exercise 8

_Exercise 1_

By Exercise 11 in section 8B the characteristic polynomial is $z^4$ and by 8.46 this is a polynomial multiple of the minimal polynomial.
Since $N^3 \neq 0$, it follows that the minimal polynomial of $N$ is $z^4$.

_Exercise 2_

Similarly, the characteristic polynomial is $z^6$ and a quick computation shows that the matrix of $N$ equals $0$ when raised to the third power, hence the minimal polynomial of $N$ is $z^3$.

_Exercise 3_

Let $\mathcal{M}(N)$ denote the matrix of $N$ with respect to some Jordan basis for $N$.
Then $\mathcal{M}(N)$ is a block diagonal matrix of the form

$$
\mathcal{M}(N) =
\begin{pmatrix}
A_1 & & 0\\\\
& \ddots &\\\\
0 & & A_p
\end{pmatrix}.
$$

Because $N$ is nilpotent, $0$ is the only eigenvalue of $N$ (see Exercise 7 in section 8A).
Hence the diagonal entries of $\mathcal{M}(N)$ are all $0$ and each $A_j$ has the following form

$$
A_j =
\begin{pmatrix}
0 & 1 & & 0\\\\
& \ddots & \ddots &\\\\
& & \ddots & 1\\\\
0 & & & 0
\end{pmatrix}.
$$

Thus every string of consecutive $1$'s corresponds to one of these blocks and its length is the same as the length of the side of the block minus $1$.
It is easy to see that if $A_j$ is $n$-by-$n$, then $A_j^{n-1} \neq 0$ and $A_j^n = 0$ (think of it as the matrix of an operator on a $n$ dimensional vector space with respect some basis, each basis vector is mapped to the previous one, except the first one obviously, and to send the last one to $0$ we have to apply the operator $n$ times).
Exercise 9 in section 8B now implies that $\mathcal{M}(N)^{m} \neq 0$ and $\mathcal{M}(N)^{m+1} = 0$.
Hence the minimal polynomial of $N$ is $z^{m+1}$.

_Exercise 4_

The difference is that the order of the blocks in the diagonal is reversed and the $1$'s appear on the line below the diagonal.

_Exercise 5_

By Exercise 9 in section 8B we just need to square each block on the diagonal of the Jordan form of $T$.
In other words, the matrix of $T^2$ is a block diagonal matrix where each block has the following form

$$
\begin{pmatrix}
\lambda_j & 1 & & 0\\\\
& \ddots & \ddots &\\\\
& & \ddots & 1\\\\
0 & & & \lambda_j
\end{pmatrix}^2 =
\begin{pmatrix}
\lambda_j^2 & 2\lambda_j & 1 & & 0\\\\
& \ddots & \ddots & \ddots &\\\\
& & \ddots & \ddots & 2\lambda_j\\\\
0 & & & \ddots & \lambda_j^2
\end{pmatrix}.
$$

_Exercise 6_

No vector in the span of

$$
N^{m_1-1}v_1, \dots, Nv_1, v_1, \dots, N^{m_n-1}v_n, \dots, Nv_n, v_n
$$

is in $\operatorname{null} N$, because applying $N$ to any such vector we get a linear of combination of

$$
N^{m_1}v_1, \dots, Nv_1, \dots, N^{m_n}v_n, \dots, Nv_n,
$$

which is linearly independent.
The vectors above are all in $\operatorname{range} N$, therefore, by the Fundamental Theorem of Linear Maps (3.22), the dimension of $\operatorname{null} N$ is at most the dimension of $V$ minus the dimension of the span of the vectors above, that is, at most $n$.
Since $N^{m_1}v_1, \dots, N^{m_n} \in \operatorname{null} N$ is linearly independent and has length $n$, it must be a basis of $\operatorname{null} N$.

_Exercise 7_

Let $\lambda_1, \dots, \lambda_m$ denote the distinct zeros of $p$ and $q$.
Then

$$
p(z) = (z - \lambda_1)^{d_1} \cdots (z - \lambda_m)^{d_m}
$$

and

$$
q(z) = (z - \lambda_1)^{h_1} \cdots (z - \lambda_m)^{h_m}
$$

for some positive integers $d_1, \dots, d_m, h_1, \dots, h_m$, where $h_j \ge d_j$ for each $j$ (because $q$ is a polynomial multiple of $p$).
Let $A$ equal the following block diagonal matrix

$$
A =
\begin{pmatrix}
A_1 & & 0\\\\
& \ddots &\\\\
0 & & A_m
\end{pmatrix}
$$

where each $A_j$ is the $h_j$-by-$h_j$ matrix defiend by

$$
A_j =
\begin{pmatrix}
\lambda_j & 1 & & & & &\\\\
 & \ddots & \ddots & & & &\\\\
& & \ddots & 1 & & &\\\\
& & & \lambda_j & 0 & &\\\\
& & & & \lambda_j & \ddots &\\\\
& & & & & \ddots & 0\\\\
& & & & & & \lambda_j
\end{pmatrix}
$$

where the $1$'s appear up to the $d_j$-th column and the $0$'s fill the rest.
Note that $A$ is a $\deg q$-by-$\deg q$ matrix.
Define $T \in \mathcal{L}(\mathbb{C}^{\deg q})$ such that the matrix of $T$ with respect to the standard basis is $A$.
Then each $\lambda_j$ is an eigenvalue of $T$, because $A$ is upper triangular and $\lambda_j$ appears on the diagonal of $A$.
Moreover, the multiplicity of $\lambda_j$ as an eigenvalue of $T$ is $h_j$, by Exercise 11 in section 8B.
Hence, the characteristic polynomial of $T$ is $q$.

It is easy to see that $(A_j - \lambda_j I)^{d_j - 1} \neq 0$ but $(A_j - \lambda_j I)^{d_j} = 0$ (we can use a reasoning similar to that of Exercise 3 to show this).
This, together with Exercise 9 from section 8B, shows that the $j$-th block is nonzero in $(A - \lambda_j I)^{d_j-1}$ and is zero in $(A - \lambda_j I)^{d_j}$ (pay attention to this fact).
It follows that

$$
(A - \lambda_1 I)^{d_1} \cdots (A - \lambda_m I)^{d_m} = 0.
$$

Hence $p(T) = 0$.
We claim now $p$ is the minimal polynomial of $T$.
To see this, suppose that it is not.
Then we can subtract $1$ from one of the exponents in the equation above and it will still hold.
Thus, we can write

$$
0 = p'(T)(T - \lambda_j)^{d_j - 1}
$$

for some $j \in \\{1, \dots, m\\}$ and some polynomial $p'$, with $p'(\lambda_j) \neq 0$.
Let $v \in G(\lambda_j, T)$ such that $(T - \lambda_j)^{d_j - 1}v \neq 0$ (this $v$ exists due to the fact we pinpointed before).
We have

$$
0 = p'(T)(T - \lambda_j)^{d_j - 1}v,
$$

but this is contradiction because $(T - \lambda_j)^{d_j - 1}v \in G(\lambda_j, T)$ and $\lambda_j$ is not an zero of $p'$.

_Exercise 8_

Suppose thre does not exist a direct sum decomposition of $V$ into two proper subspaces invariant under $T$.
Therefore, the block diagonal matrix of $T$ with respect to some Jordan basis for $T$ only has one block (the span of the basis vectors that correspond to each block is invariant under $T$).
Therefore $T$ only has one eigenvalue, call it $\lambda$.
Exercise 3 now implies that $(z - \lambda)^{\dim V}$ is minimal polynomial of $T$.

For the other direction, we will prove the contrapositive.
Suppose we can decompose $V$ into two proper subspaces invariant under $T$.
If $T$ has more than one eigenvalue the result is obvious.
Assume $T$ has only one eigenvalue, call it $\lambda$.
Then $V = G(\lambda, T)$ and there are proper subspaces $U_1, U_2$ of $G(\lambda, T)$ invariant under $T$ such that $G(\lambda, T) = U_1 \oplus U_2$ with $1 \le \dim U_1, \dim U_2 < \dim V$.
We have that $(z - \lambda)^{\dim U_1}$ and $(z - \lambda)^{\dim U_2}$ are the characteristic polynomials of $T|\_{U_1}$ and $T|\_{U_2}$.
Thus $(T - \lambda)^{\max\\{\dim U_1, \dim U_2\\}} = 0$ and so the minimal polynomial of $T$ cannot be $z^{\dim V}$.
