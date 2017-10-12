Chapter 3: **Linear Maps**

**Theorem 1.**
Suppose $V$ is a finite-dimensional vector space and $\varphi \in V'$. Then $\operatorname{span}(\varphi) = (\operatorname{null}\varphi)^0$.

_Proof_

Clearly, $\operatorname{span}(\varphi) \subset (\operatorname{null}\varphi)^0$.

For the inclusion in the other direction, suppose $\psi \notin \operatorname{span}(\varphi)$.

If $\varphi = 0$, then $(\operatorname{null} \varphi)^0 = V^0 = \\{0\\}$ and then, because $\psi \neq 0$, it follows that $\psi \notin \operatorname{span}(\varphi)$.

Assume $\varphi$ is non-zero.
Let $v_1, \dots, v_n$ be a basis of $\operatorname{null} \varphi$.
By _Exercise 1_ in section 3F, it follows that $\varphi$ is surjective.
Choose a vector $v$ in $V$ such that $\varphi(v) = 1$.
By the Fundamental Theorem of Linear Maps (3.22), $v, v_1, \dots, v_n$ is a basis of $V$.
Note that $\varphi(v_i) = 0$ for $i = 1, \dots, n$.
Let $\varphi, \psi_1, \dots, \psi_n$ be its dual basis.

We have $\psi = a \varphi + a_1 \psi_1 + \dots + a_n \psi_n$, for some scalars $a, a_1, \dots, a_n \in \mathbb{F}$, where $a_j \neq 0$ for some $j \in \\{1, \dots, n\\}$ because $\psi \notin \operatorname{span}(\varphi)$.
Then

$$
\begin{aligned}
\psi(v_j) &= (a \varphi + a_1 \psi_1 + \dots + a_n \psi_n)(v_j)\\\\
&= a \varphi(v_j) + a_1 \psi_1(v_j) + \dots + a_n \psi_n(v_j)\\\\
&= a_j\\\\
&\neq 0
\end{aligned}
$$

Because $v_j \in \operatorname{null} \varphi$ it follows that $\psi \notin (\operatorname{null} \varphi)^0$.

By modus tollens, $\psi \in (\operatorname{null} \varphi)^0$ implies $\psi \in \operatorname{span}(\varphi)$.
Hence $(\operatorname{null} \varphi)^0 \subset \operatorname{span}(\varphi)$ and $\operatorname{span}(\varphi) = (\operatorname{null}\varphi)^0$, as desired.
<p align="right"> $\blacksquare$ </p>

**Theorem 2.**
Suppose $V$ is finite-dimensional and $\varphi, \varphi_1, \dots, \varphi_n \in V'$.
If $(\operatorname{null} \varphi_1) \cap \dots \cap (\operatorname{null} \varphi_n) \subset \operatorname{null} \varphi$, then $\varphi \in \operatorname{span}(\varphi_1, \dots, \varphi_n)$.

_Proof_

We have that

$$
\begin{aligned}
\varphi \in \operatorname{span}(\varphi) &= (\operatorname{null} \varphi)^0\\\\
&\subset ((\operatorname{null} \varphi_1) \cap \dots \cap (\operatorname{null} \varphi_n))^0\\\\
&= (\operatorname{null} \varphi_1)^0 + \dots + (\operatorname{null} \varphi_n)^0\\\\
&= \operatorname{span}(\varphi_1) + \dots + \operatorname{span}(\varphi_n)\\\\
&= \operatorname{span}(\varphi_1, \dots, \varphi_n)\\\\
\end{aligned}
$$

Where the first and fourth lines follow from _Theorem 1_, the second and third from _Exercise 20_ and _Exercise 23_ in section 3F, respectively, and the fifth from the definition of sum of subspaces.
<p align="right"> $\blacksquare$ </p>
