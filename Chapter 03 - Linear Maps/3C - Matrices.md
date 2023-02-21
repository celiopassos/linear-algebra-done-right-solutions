Chapter 3: **Linear Maps**

**3.C**

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
- [ ] Exercise 15

_Exercise 1_

Let $v_1, \dots, v_m$ denote a basis of $V$.
The dimension of $\operatorname{range} T$ is the same as the dimension of $\operatorname{span}(Tv_1, \dots, Tv_m)$.
So if the matrix of $T$ has less than $\operatorname{dim} \operatorname{range} T$ nonzero entries, it follows from the definition of $\mathcal{M}(T)$ that the list $Tv_1, \dots, Tv_m$ has less than $\operatorname{dim} \operatorname{range} T$ non-zero vectors, which is not possible, because its span is $\operatorname{range} T$.

_Exercise 2_

Just differentiate any basis of $\mathcal{P}_3(\mathbb{R})$, take whatever is left as basis of $\mathcal{P}_2(\mathbb{\mathbb{R}})$ (except the $0$ vector) and adjust the order.
For example, differentiating the standard basis $1, x, x^2, x^3$ we get $0, 1, 2x, 3x^2$.
Therefore, the matrix of $D$ with respect to the basis $x^3, x^2, x, 1$ of $\mathcal{P}_3(\mathbb{R})$ and the basis $3x^2, 2x, 1$ of $\mathcal{P}_2(\mathbb{R})$ is

$$
\begin{pmatrix}
1 & 0 & 0 & 0\\\\
0 & 1 & 0 & 0\\\\
0 & 0 & 1 & 0
\end{pmatrix}.
$$

_Exercise 3_

Use the same notation from 3.22.
Extend $Tv_1, \dots, Tv_n$ to a basis $Tv_1, \dots, Tv_n, w_1, \dots, w_k$ of $W$.
It is easy to see now that the matrix of $T$ with respect to this basis and the basis $v_1, \dots, v_n, u_1, \dots, u_m$ of $V$ satisfies the desired property.

_Exercise 4_

If $Tv_1 = 0$, then all entries in the first column is zero for any basis of $W$.
If $Tv_1 \neq 0$, let $w_1 = Tv_1$ and extend it a basis $w_1, \dots, w_n$ of $W$.
Then

$$
Tv_1 = 1w_1 + 0w_2 + \dots + 0w_n,
$$

which shows that the entries in the first column are all $0$ except the first one, which is $1$.

_Exercise 5_

I will use facts from section 3F, although this was not what Axler intended.

Consider the dual basis $\psi_1, \dots, \psi_n$ of $w_1, \dots, w_n$ and the dual map $T'$ of $T$ (note that $T'$ is map from $W'$ to $V'$).
By the previous exercise, there exists a basis of $\varphi_1, \dots, \varphi_m$ of $V'$ such that all entries in the first column of $\mathcal{M}(T')$ (with respect to the bases we have here of $W'$ and $V'$) are $0$ except for possibly a $1$ in the first row, first column.
By Exercise 31 in section 3F, there exists a basis $v_1, \dots, v_m$ of $V$ such that its dual basis is $\varphi_1, \dots, \varphi_m$.
Moreover, by 3.114, we have $\mathcal{M}(T)$ (with respect to the bases shown here of $V$ and $W$) is equal to $(\mathcal{M}(T'))^t$, which shows that $\mathcal{M}(T)$ satisfies the desired property.

Alternative proof:

Consider any basis $v_1,...,v_m$ of $V$, and a set of vectors $Tv_1,...,Tv_m$, and denote $Tv_i = \sum\limits_{j=1}^nA_{ji}w_j$. 

Suppose first that all $A_{1i} = 0$ - then we have found the desired basis. 

Suppose now that not all $A_{1i} = 0$. Without loss of generality, let us assume $A_{11} \neq 0$. Then, let us consider set of vectors 

$$
\begin{align}
v_1' &= \frac{1}{A_{11}}v_1\\
v_2' &= v_2 - \frac{A_{12}}{A_{11}}v_1\\
v_3' &= v_3 - \frac{A_{13}}{A_{11}}v_1\\
\ldots\\
v_m' &= v_m - \frac{A_{1m}}{A_{11}}v_1
\end{align}
$$

It's obvious that $Tv_1' = 1w_1 + \sum\limits_{j=2}^nA_{j1}w_j$, and $Tv_i' = 0w_1 + \sum\limits_{j=2}^nA_{ji}w_j$, so we have the first line of corresponding matrix equal to $(1, 0, 0,..., 0)$. We now need to prove that $v_1',...,v_m'$ is a basis of $V$, which will complete the task.

Let us consider $\sum\limits_{i=1}^mc_iv_i' = 0$. We can rewrite the left part of this equation

$$
\begin{align}
&\frac{c_1}{A_{11}}v_1 + \sum\limits_{i=2}^mc_iv_i - \sum\limits_{i=2}^m\frac{c_i}{A_{11}}v_1 \\
& = v_1(\frac{c_1}{A_{11}} - \sum\limits_{i=2}^m\frac{c_i}{A_{11}}) + \sum\limits_{i=2}^mc_iv_i
\end{align}
$$

Since $v_1,...,v_m$ are linearly independent, if this expression is 0, it must be that all the coefficients in front of $v_1...v_m$ are 0 as well, so $c_2=c_3=...=c_m = 0$, and $\frac{c_1}{A_{11}} - \sum\limits_{i=2}^m\frac{c_i}{A_{11}}$, which implies that $c_1 = 0$. So, this completes the proof that $v_1',...,v_m'$ are linearly independent and hence form a basis of $V$.

_Exercise 6_

$\Rightarrow$: Since $\operatorname{dim}\operatorname{range}T = 1$, its basis consists of a single vector. Denote this vector $w \neq 0$. Next, we can extend this basis to a basis of $W$ with some vectors $w_2,...,w_m$. Now, let $w_1 = w - \sum\limits_{i=2}^mw_i$. It is clear, that $w_1,...,w_m$ are linearly independent: $\sum\limits_{i=1}^mc_iw_i = \sum\limits_{i=2}^mc_iw_i + c_1w - c_1\sum\limits_{i=2}^mw_i = c_1w + \sum\limits_{i=2}^m(c_i - c_1)w_i$. Since $w, w_2,...,w_m$ are linearly independent as a basis, this expression is 0 only if $c_1 = 0$ and $c_i - c_1 = 0$ for all $i=2...m$, which means that all $c_i=0$, so $w_1,...,w_m$ are also linearly independent and hence they form another basis of $W$. 

Let us select $v_1,...,v_{n-1}$ as a basis of $\operatorname{null}T$, and extend it to a basis of $V$ with $v_n$. Since $Tv_n \in \operatorname{range}T$, we have $Tv_n = \lambda w$, $\lambda \neq 0$. We now select a set of vectors 

$$
\begin{align}
v_1' &= v_1 + \frac{1}{\lambda}v_n \\
v_2' &= v_2 + \frac{1}{\lambda}v_n \\
... \\
v_{n-1}' &= v_{n-1} + \frac{1}{\lambda}v_n \\
v_n' &= \frac{1}{\lambda}v_n
\end{align}
$$

It is clear that $\forall i Tv_i' = \frac{1}{\lambda}Tv_n = w = w_1 + ... +w_m$. It is also easy to show, that $v_1',...,v_n'$ form a basis of V. 

$\Leftarrow$: suppose there are bases $v_1,...,v_n$ and $w_1,...,w_m$ of $V$ and $W$ such, that $Tv_i = w_1 + ... + w_m$. We know that $\operatorname{range}T = \operatorname{span}(Tv_1, Tv_2, ..., Tv_n)$, but since all $Tv_i$ are equal, $\operatorname{span}(Tv_1, Tv_2, ..., Tv_n) = \operatorname{span}(Tv_1)$, and so $\operatorname{dim}\operatorname{range}T = 1$.


_Exercise 7_

Use the same choice of basis for $\mathcal{M}(S)$, $\mathcal{M}(T)$ and $\mathcal{M}(S + T)$ and same notation as in 3.32.

Let $A = \mathcal{M}(S)$, $B = \mathcal{M}(T)$ and $C = \mathcal{M}(S + T)$.
Then

$$
\begin{aligned}
\sum\limits_{j=1}^m C_{j,k} w_j &= (S + T)v_k\\\\
&= Sv_k + Tv_k\\\\
&= \sum\limits_{j=1}^m A_{j,k} w_j + \sum\limits_{j=1}^m B_{j, k} w_j\\\\
&= \sum\limits_{j=1}^m (A_{j,k} + B_{j, k}) w_j.
\end{aligned}
$$

Since $w_1, \dots, w_m$ is a basis, by 2.29 their coefficients are unique for each vector they determine, therefore it follows that $C_{j, k} = A_{j, k} + B_{j, k}$, as desired.

_Exercise 8_

This is almost the same as _Exercise 7_.

_Exercise 9_

Clearly, $Ac$ is a $m$-by-$1$ matrix.
Then

$$
\begin{aligned}
(Ac)_{j, 1} &= \sum\limits_{r=1}^n A_{j, r} c_{r,1}\\\\
&= \sum\limits_{r=1}^n A_{j, r} c_r\\\\
&= c_1 A_{j, 1} + \dots + c_n A_{j, n}\\\\
&= c_1 (A_{.,1})_{j, 1} + \dots + c_n (A_{.,n})_{j, 1}\\\\
&= (c_1 A_{.,1})_{j, 1} + \dots + (c_n A_{.,n})_{j, 1}\\\\
&= (c_1 A_{.,1} + \dots + c_n A_{.,n})_{j, 1}.
\end{aligned}
$$

_Exercise 10_

Use the same notation as in the motivation prior to 3.41.

Let $Z$ be a $1$-dimensional vector space and $z$ a basis for it.
Define $S_j: V \to Z$ by

$$
S_j v_r = A_{j, r} z
$$

for $1 \le r \le n$.
Obviously, $\mathcal{M}(S_j) = A_{j,.}$.
Therefore, $A_{j,.}C = \mathcal{M}(S_j) \mathcal{M}(T) = \mathcal{M}(S_j T)$.
Thus

$$
\begin{aligned}
S_j Tu_k &= S_j (\sum\limits_{r=1}^n C_{r, k} v_r)\\\\
&= \sum\limits_{r=1}^n C_{r, k} S_j v_r\\\\
&= \sum\limits_{r=1}^n C_{r, k} A_{j, r} z\\\\
&= (AC)_{j, k} z
\end{aligned}
$$

for $1 \le k \le p$.
Hence, $(AC)_{j,.} = A_{j,.}C$.

_Exercise 11_

We have

$$
\begin{aligned}
(aC)_{1, k} &= \sum\limits_{r=1}^n a_{1, r} C_{r, k}\\\\
&= \sum\limits_{r=1}^n a_r C_{r, k}\\\\
&= a_1 C_{1, k} + \dots + a_n C_{n, k}\\\\
&= a_1 (C_{1,.})_{1, k} + \dots + a_n (C_{n,.})_{1, k}\\\\
&= (a_1 C_{1,.} + \dots + a_n C_{n,.})_{1, k}\\\\
\end{aligned}
$$

_Exercise 12_

We have

$$
\begin{pmatrix} 1 & -1\\\\ 1 & -1 \end{pmatrix} \begin{pmatrix} 1 & 1\\\\ -1 & -1 \end{pmatrix} =
\begin{pmatrix} 2 & 2\\\\ 2 & 2 \end{pmatrix},
$$

but

$$
\begin{pmatrix} 1 & 1\\\\ -1 & -1 \end{pmatrix} \begin{pmatrix} 1 & -1\\\\ 1 & -1 \end{pmatrix} =
\begin{pmatrix} 2 & -2\\\\ -2 & 2 \end{pmatrix}.
$$

_Exercise 13_

Since $A(B+C)$ and $(D+E)F$ make sense, $B$ has the same size, as C (denote it $m,n$), and $D$ has the same size as $E$ (denote it also $m,n$). Also, $A$ has the same number of columns, as $B+C$ (as well as $B$ and $C$) has rows, so $A$ has a shape $p,m$ and $F$ has the same number of rows as $D+E$ has columns (which is the same as number of columns in $D$ and $E$), so we can denote the shape of $F$ as $n,p$. So, $AB$ and $AC$ are well-defined and have the same shape $p,n$, so their sum is also well-defined. The same goes for $DF$, $EF$ and their sum, which all have shape $m,p$.

Consider arbitrary $i,j$: $1 \le i \le p$, $1 \le j \le n$ $A(B+C)_{ij} = \sum\limits_{r=1}^mA_{ir}(B+C)_{rj} = \sum\limits_{r=1}^mA_{ir}(B_{rj}+C_{rj}) = \sum\limits_{r=1}^mA_{ir}B_{rj} + \sum\limits_{r=1}^mA_{ir}C_{rj} = (AB)_{ij} + (AC)_{ij}$. So, all elements of $AB + AC$ and $A(B+C)$ are equal, which means that these matrices are equal.

The proof for $(D+E)F$ is similar.

_Exercise 14_

If $(AB)C$ makes sense, then if $A$ has shape $m,n$, and $C$ has a shape $p,q$, $C$ should have shape $m,p$, and it means that $A(BC)$ also is well-defined. 

$$
\begin{align}
((AB)C)_{ij} &= \sum\limits_{k}(AB)_{ik}C_{kj}\\
 &= \sum\limits_{k}\sum\limits_{r}A_{ir}B_{rk}C_{kj}\\
 &= \sum\limits_{r}\sum\limits_{k}A_{ir}B_{rk}C_{kj}\\
 &= \sum\limits_{r}A_{ir}\sum\limits_{k}B_{rk}C_{kj}\\
 &= \sum\limits_{r}A_{ir}(BC)_{rj} \\
 &= (A(BC))_{ij}
\end{align}
$$
