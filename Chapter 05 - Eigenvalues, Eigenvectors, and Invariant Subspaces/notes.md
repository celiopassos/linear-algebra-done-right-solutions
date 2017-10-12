Chapter 5: **Eigenvalues, Eigenvector, and Invariant Subspaces**

**Theorem 1.**
Suppose $T \in \mathcal{L}(V)$ is invertible and $p, q \in \mathcal{P}(\mathbb{F})$.
Then $p(T^{-1}) q(T) = q(T) p(T^{-1})$.

_Proof_

The key idea used here is that $T$ commutes with $T^{-1}$, even when raised to different powers.

Suppose $p(z) = \sum_{j=0}^m a_j z^j$ and $q(z) = \sum_{k=0}^n b_k z^k$ for $z \in \mathbb{F}$.
Then

$$
\begin{aligned}
p\left(T\right)q\left(T^{-1}\right) &= \left(\sum_{j=0}^m a_j T^j\right)\left(\sum_{k=0}^n b_k \left(T^{-1}\right)^k\right)\\\\
&= \sum_{j=0}^m \sum_{k=0}^n a_j b_k T^j \left(T^{-1}\right)^k\\\\
&= \sum_{j=0}^m \sum_{k=0}^n b_k a_j \left(T^{-1}\right)^k T^j\\\\
&= \sum_{k=0}^n \sum_{j=0}^m b_k a_j \left(T^{-1}\right)^k T^j\\\\
&= \left(\sum_{k=0}^n b_k \left(T^{-1}\right)^k\right)\left(\sum_{j=0}^m a_j T^j\right)\\\\
&= q\left(T^{-1}\right)p\left(T\right)
\end{aligned}
$$

<p align="right"> $\blacksquare$ </p>
