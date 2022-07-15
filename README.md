# Tate-Shafarevich-groups-of-multinorm-one-torus

We represent an implementation of the algorithm described in Ting-Yu Lee's paper "The Tate-Shafarevich groups of multinorm-one tori." To be more specific, we use the results in Theorem 6.5 to compute the Tate-Shafarevich groups of multinorm one tori over number fields. All of the following files are written in SageMath 9.6.

1. Example 7.4 in [L].ipynb.
It computes Example 7.4 in Lee's paper using the algorithm inside. In this case $k = \mathbb{Q}(i)$, $K_0 = k(\sqrt[4]{17})$, $K_1 = k(\sqrt[4]{17 \times 13})$ and $K_2 = k(\sqrt[4]{13})$.

2. Example 7.5 in [L].ipynb.
It computes Example 7.5 in Lee's paper using the algorithm inside. In this case $k = \mathbb{Q}(i)$, $K_0 = k(\sqrt[4]{17})$, $K_1 = k(\sqrt[4]{17 \times 409})$ and $K_2 = k(\sqrt[4]{409})$.

3. Example 7.7 in [L].ipynb.
It computes Example 7.5 in Lee's paper using the algorithm inside. In this case $k = \mathbb{Q}(i)$, $K_0 = k(\sqrt[4]{13})$, $K_1 = k(\sqrt[4]{17})$ and $K_2 = k(\sqrt[4]{13 \times 17^2})$.

4. Final Presentation Example 1.ipynb.
It computes the case $k = \mathbb{Q}(\zeta_{27})$, $K_0 = k(\sqrt[27]{5})$, $K_1 = k(\sqrt[27]{5 \times 19})$, $K_2 = k(\sqrt[27]{5^2 \times 19^3})$, $K_3 = k(\sqrt[27]{5^3 \times 19^5})$, $K_4 = k(\sqrt[27]{5^5 \times 19^{11}})$.

5. Final Presentation Example 2.ipynb.
It computes the case $k = \mathbb{Q}(\zeta_{27})$, $K_0 = k(\sqrt[27]{5})$, $K_1 = k(\sqrt[27]{5 \times 19})$, $K_2 = k(\sqrt[27]{5^2 \times 19^3})$, $K_3 = k(\sqrt[27]{5^4 \times 19^9})$, $K_4 = k(\sqrt[27]{5^{10} \times 19^{19}})$.

File 1, 2, and 3 depend on the implementation of number fields in Sage and involves complex computations such as checking inclusions of number fields and computing Galois groups relatve to $k$. To make computation easier and less time-consuming, in File 4 and 5 we make the following assumptions on $k$ and $K_i$'s:
1. $k = \mathbb{Q}(\zeta_{p^n})$, where $\zeta_{p^n} = e^{2 \pi i/p^n}$ and $p$ is a prime integer.
2. $\ell_1$ and $\ell_2$ are distinct prime numbers not equal to $p$.
3. $K_i$ are of the form $K_i = k\left(\sqrt[p^n]{\ell_1^{a_i} \ell_2^{b_i}}\right)$, where $0 \leq a_i, b_i < p^n$ and $(a_i, b_i) \neq (0, 0)$.
File 4 and 5 does not depend on the implementatin of number fields in Sage. We hope that the files are self-explanatory as `.ipynb` files.
