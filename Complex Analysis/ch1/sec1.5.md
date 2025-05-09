
## §5 群在集合上的作用，群的自同构，轨道-稳定子定理

### 4. 设 $F$ 是一个域， $GL_n(F)$ 的中心为 $\{ kI_{n}|k\in \mathbb{Z} \}$ 。
### 5. $GL_2(C)$ 的每一个元素$$\begin{pmatrix} a & b \\ c & d \end{pmatrix}$$ 引起了扩充复平面 $C \cup \{\infty\}$ 上的一个变换：$$z \mapsto \frac{az + b}{cz + d},$$ 称它为 Möbius (默比乌斯) 变换。证明：(1) 所有 Möbius 变换组成的集合 $G$ 对于变换的乘法成一个群，称它为 Möbius 群；(2) $GL_2(C) / Z(GL_2(C)) \cong G$.

---

### 6. 设 $G$ 是一个群，证明：如果 $G/Z(G)$ 是循环群，则 $G$ 是 Abel 群。

Let $N = Z(G)$. Since $G/N$ is a cyclic group, therefore $G/N = \langle aN \rangle$. For any $x, y \in G$, let $xN = (aN)^r$, $yN = (aN)^s$, then there exist $n_1, n_2 \in N$ such that $x = a^r n_1$, $y = a^s n_2$. Thus

$x y x^{-1} y^{-1} = (a^r n_1)(a^s n_2)(a^r n_1)^{-1}(a^s n_2)^{-1} = a^r a^s a^{-r} a^{-s} n_1 n_1^{-1} n_2 n_2^{-1} = e.$

Therefore $xy = yx$. Hence $G$ is an Abelian group.

---


### 7. 分别求 $D_{2m-1}, D_{2m}$ 的中心，其中 $m \geq 2$。<a id=  1.5.7 ></a>   
$$
\begin{aligned}
\sigma^i \in Z(D_n) & \Leftrightarrow \tau \sigma^i = \sigma^i \tau \\
& \Leftrightarrow \tau \sigma^i \tau^{-1} = \sigma^i \\
& \Leftrightarrow (\tau \sigma \tau^{-1})^i = \sigma^i \\
& \Leftrightarrow \sigma^{-i} = \sigma^i \\
& \Leftrightarrow \sigma^{2i} = I \\
& \Leftrightarrow n \mid 2i.
\end{aligned}
$$

**Case 1: $ n = 2m - 1 $**  
$$ 
\sigma^i \in Z(D_{2m-1}) \Leftrightarrow 2m - 1 \mid i \Leftrightarrow i=0 \Leftrightarrow \sigma^i = I. 
$$

由于 $\tau \notin Z(D_{2m-1})$，故 
$$
Z(D_{2m-1}) = \{ I \}.
$$

**Case 2: $ n = 2m $**  
$$
\sigma^i \in Z(D_{2m}) \Leftrightarrow m \mid i \Leftrightarrow i=0 \text{ 或 } m \Leftrightarrow \sigma^i = I \text{ 或 } \sigma^m.
$$

由于 $\tau \notin Z(D_{2m})$，故
$$
Z(D_{2m}) = \{ I, \sigma^m \}.
$$

---


### 8. 求 $S_n$ 的中心，其中 $n \geq 3$。
Since $S_n = \langle (12), (13), \cdots, (1n) \rangle$, therefore

$$\begin{align*}
\tau \in Z(S_n) & \Leftrightarrow \tau(1i)\tau^{-1} = (1i), i=2, 3, \cdots, n\\
& \Leftrightarrow \tau(1)=1 ,  \tau(i)=i, i=2, 3, \cdots, n;  \text{or} \quad \tau(1)=i \tau(i)=1, i=2, 3, \cdots, n            \end{align*}
$$

Since $\tau$ is a mapping, thus when $n \geqslant 3$, the second case cannot occur. Therefore $\tau \in Z(S_n) \Leftrightarrow \tau=(1)$.

Hence $Z(S_n) = \{(1)\}$.


---

### 14. Determine all conjugacy classes of $D_{2m-1}$ and $D_{2m}$, where $m \geq 2$.

From Exercise [1.5.7](#1.5.7), we know that 
$$
Z(D_{2m-1}) = \{ I \}, \quad Z(D_{2m}) = \{ I, \sigma^m \}.
$$ 

For $D_{2m-1}:$ It is obvious that 
$$\begin{align*}
C_{D_{2m-1}}(\sigma^i) &= \langle \sigma \rangle, & 1 \le i \le 2m-2; \\
C_{D_{2m-1}}(\sigma^i \tau) &= \{ I, \sigma^i \tau \}, & 0 \le i \le 2m-2; \\
C_{D_{2m-1}}(I) &= D_{2m-1}.
\end{align*}$$

Then by the **Orbit-Stabilizer Theorem**,
$$ |D_{2m-1}(\sigma^j)| = 2, \quad 1 \le j \le 2m-2, \quad |D_{2m-1}(I)| = 1, \quad |D_{2m-1}(\sigma^i \tau)| = 2m-1, \quad 1 \le i \le 2m-1.
$$

And since 
$$\begin{align*}
\sigma \sigma \sigma^{-1} &= \sigma, \\
\sigma^2 \tau \sigma \tau \sigma^{-2} &= \sigma^{2m-2} \in D_{2m-1}(\sigma); \\
\sigma \sigma^2 \sigma^{-1} &= \sigma^2, \\
\sigma^2 \tau \sigma^2 \tau \sigma^{-2} &= \sigma^{2m-3} \in D_{2m-1}(\sigma^2); \\
&\vdots \\
\sigma \sigma^k \sigma^{-1} &= \sigma^k, \\
\sigma^2 \tau \sigma^k \tau \sigma^{-2} &= \sigma^{2m-1-k} \in D_{2m-1}(\sigma^k),
\end{align*}$$

we have 
$$ 
D_{2m-1}(\sigma^k) = \{ \sigma^k, \sigma^{2m-1-k} \}, \quad 1 \le k \le m-1; \quad D_{2m-1}(I) = \{ I \}.
$$

For the remaining $2m-1$ elements $\sigma^j \tau$, find $x$ such that $\sigma^x (\sigma^j \tau) \sigma^{-x} = \sigma^{j+2x} \tau \equiv \sigma^i \tau$
$$
\Leftrightarrow j + 2x \equiv i \pmod{2m-1} \Leftrightarrow 2x \equiv i - j \pmod{2m-1}.
$$

By number theory, $(2, 2m-1) = 1$, so this congruence equation has a solution for $x$.

Thus, $\{ \sigma^j \tau \mid 1 \le j \le 2m-1 \}$ is contained in one conjugacy class.

By the **Orbit Decomposition Theorem**, this conjugacy class is $D(\tau)$.

For $D_{2m}:$ Similarly, we can obtain that 
$$\begin{align*}
C_{D_{2m}}(\sigma^i) &= \langle \sigma \rangle,  1 \le i \le 2m-1 \backslash \{ m \}; \\
C_{D_{2m}}(I) &=C_{D_{2m}}(\sigma^{m})= D_{2m};\\
D_{2m}(\sigma ^{k})&=\{ \sigma^{k},\sigma^{2m-k} \},1\le k\le m-1;D_{2m}(\sigma^{m})=\{ \sigma^{m} \};D_{2m}(I)=\{ I \}
\end{align*}$$

For the remaining $2m$ elements $\sigma^j \tau$, find $x$ such that $\sigma^x (\sigma^j \tau) \sigma^{-x} = \sigma^{j+2x} \tau \equiv \sigma^i \tau$
$$
\Leftrightarrow j + 2x \equiv i \pmod{2m} \Leftrightarrow 2x \equiv i - j \pmod{2m} \Leftrightarrow i \equiv j \pmod{2} .
$$

So $\{ \sigma^{2i}\tau|1\le i\le m \},\{ \sigma^{2j-1}\tau|1\le j\le m \}$  each is contained in one conjugacy class.

By the **Orbit Decomposition Theorem**, the two conjugacy classes are $D(\tau),D(\sigma\tau)$.

In conclusion, the $m+1$  conjugacy classes of $D_{2m-1}$ are 
$$ 
D_{2m-1}(I)=\{ I \} \quad D_{2m-1}(\sigma^{k})=\{ \sigma^{k},\sigma^{2m-1-k} \} ,1\le k\le m-1 \quad D_{2m-1}(\tau)=\{ \sigma^{j}\tau|1\le j\le 2m-1 \} ;
$$  

the $m+3$  conjugacy classes of $D_{2m-1}$ are 
$$ D_{2m}(I)=\{ I \}\quad D_{2m}(\sigma^{k})=\{ \sigma^{k},\sigma^{2m-k} \},1\le k\le m-1 \quad D_{2m}(\sigma^{m})=\{ \sigma^{m} \} \quad D_{2m}(\tau) \quad D_{2m}(\sigma\tau)
$$

---


### 15. 设 $\sigma$ 的不相交的轮换分解式 (包含所有的 1-轮换) 为$$\sigma = (a_1 a_2 \dots a_{l_1})(b_1 b_2 \dots b_{l_2}) \dots (q_1 q_2 \dots q_{l_r})$$ 其中 $l_1 \geq l_2 \geq \dots \geq l_r$, 且 $l_1 + l_2 + \dots + l_r = n$。则我们把有序数组 $(l_1, l_2, \dots, l_r)$ 称为置换 $\sigma$ 的型 (type)，也称为 $n$ 的一个分拆 (partition)。证明：(1) $\sigma_1$ 与 $\sigma_2$ 在 $S_n$ 中共轭当且仅当 $\sigma_1$ 与 $\sigma_2$ 同型；(2) $S_n$ 中共轭类的个数等于 $n$ 的分拆的个数。<a id=  1.5.15 ></a>   
From exercise[1.1.12](#1.1.12), this is quite easy to prove.

---

### 16. 求 $S_4$ 的共轭类的个数，以及每个共轭类的代表和元素数目。

$4=4$, $4=3+1$, $4=2+2$, $4=2+1+1$, $4=1+1+1+1$. Therefore, the partitions of $4$ have $5$ types. Thus, $S_4$ has $5$ conjugacy classes, and their representatives are: $(1234)$, $(123)$, $(12)(34)$, $(12)$, $(1)$. The number of elements in the corresponding conjugacy classes are respectively: $\frac{1}{4}4! = 6$, $\frac{1}{3}(4 \cdot 3 \cdot 2) = 8$, $\frac{1}{2}\left[\frac{1}{2}(4 \cdot 3)\right] = 3$, $\frac{1}{2}(4 \cdot 3) = 6$, $1$.


---


### 17. 求 $A_4$ 的共轭类的个数，以及每个共轭类的代表和元素数目。

In $A_4$, the necessary condition for permutations $\sigma_1$ and $\sigma_2$ to be conjugate is that $\sigma_1$ and $\sigma_2$ are of the same type, but this is not a sufficient condition.

For example, $(123)$ and $(132)$ are of the same type, but they are not conjugate in $A_4$. This is because the only $\tau$ that satisfies $\tau(123)\tau^{-1} = (132)$ are $(23)$, $(13)$, $(12)$, which are all odd permutations and do not belong to $A_4$. Using the necessary condition for conjugacy and checking, we find that $A_4$ has $4$ conjugacy classes, with representatives: $(1)$, $(12)(34)$, $(123)$, $(132)$. The number of elements in the corresponding conjugacy classes are: $1$, $3$, $4$, $4$.

---

### 18. 设 $\sigma$ 是一个 $n$-轮换。求 $\sigma$ 的共轭类的元素数目，以及 $C_{S_n}(\sigma)$ 的阶。
Based on the conclusion of  problem [1.5.15](#1.5.15), the conjugacy class of an $n$-cycle $\sigma$ consists exactly of all $n$-cycles. Thus, the number of elements in the conjugacy class of $\sigma$ is $\frac{n!}{n} = (n-1)!$(**Circular arrangement**). Therefore, $|C_{S_n}(\sigma)| = \frac{n!}{(n-1)!} = n$. Since $\sigma \in C_{S_n}(\sigma)$ and the order of $\sigma$ is $n$, it follows that $C_{S_n}(\sigma) = \langle \sigma \rangle$.

---

### 19. 求 $O_2$ 的所有共轭类。
$O_2$ consists of all $2 \times 2$ orthogonal matrices. According to Advanced Algebra, there are only two types of $2 \times 2$ orthogonal matrices:

$ A_\theta = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}, \quad B_\varphi = \begin{pmatrix} \cos\varphi & \sin\varphi \\ \sin\varphi & -\cos\varphi \end{pmatrix}, $

where $0 \leq \theta < 2\pi$, $0 \leq \varphi < 2\pi$. Two elements in $O_2$ are conjugate if and only if these two matrices are orthogonally similar. Since similar matrices have the same determinant, and $|A_\theta| = 1$, $|B_\varphi| = -1$, for any $\theta$ and $\varphi$, $A_\theta$ and $B_\varphi$ are not conjugate. Since $B_\varphi$ is a real symmetric matrix, $B_\varphi$ must be orthogonally similar to a diagonal matrix with its main diagonal elements being the eigenvalues of $B_\varphi$. 

Since

$ |\lambda I - B_\varphi| = (\lambda - \cos\varphi)(\lambda + \cos\varphi) - \sin^2\varphi = \lambda^2 - 1, $

the eigenvalues of $B_\varphi$ are $1$ and $-1$. Therefore, $B_\varphi$ is conjugate to $\text{diag}\{1, -1\}$, $0 \leq \varphi < 2\pi$. Thus, $\{B_\varphi \mid 0 \leq \varphi < 2\pi\}$ is a conjugacy class of $O_2$.

Given $\theta$ ($0 \leq \theta < 2\pi$), for any $\psi$ ($0 \leq \psi < 2\pi$),

$ A_\psi A_\theta A_\psi^{-1} = A_\theta, $
$ B_\psi A_\theta B_\psi^{-1} = \begin{pmatrix} \cos(\psi-\theta) & \sin(\psi-\theta) \\ \sin(\psi-\theta) & -\cos(\psi-\theta) \end{pmatrix} \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix} = \begin{pmatrix} \cos(-\theta) & -\sin(-\theta) \\ \sin(-\theta) & \cos(-\theta) \end{pmatrix} = A_{-\theta} = A_{2\pi-\theta}. $

Therefore, when $0 < \theta < \pi$, the conjugacy class of $A_\theta$ is $\{A_\theta, A_{2\pi-\theta}\}$. The conjugacy class of $A_0 = I$ is $\{I\}$, and the conjugacy class of $A_\pi = -I$ is $\{-I\}$. In summary, the complete conjugacy classes of $O_2$ are:

$ \{I\}, \quad \{-I\}, \quad \{B_\varphi \mid 0 \leq \varphi < 2\pi\}, \quad \{A_\theta, A_{2\pi-\theta}\}, \quad 0 < \theta < \pi. $



---

### 20. 群 $G$ 的子群 $H$ 为正规子群当且仅当 $H$ 是 $G$ 的一些共轭类的并集。<a id=  1.5.20 ></a>   

---

### 21. (1) 求 $S_5$ 的共轭类的个数，以及每个共轭类的代表和元素数目；(2) 证明：$S_5$ 只有三个正规子群，即 $\{1\}, A_5, S_5$。

(1): The partitions of $5$ have $7$ types, so $S_5$ has $7$ conjugacy classes. Their representatives are:

$(1)$, $(12)$, $(12)(34)$, $(123)$, $(123)(45)$, $(1234)$, $(12345)$.

The number of elements in the corresponding conjugacy classes are:

$1$, $10$, $15$, $20$, $20$, $30$, $24$.

(2):The normal subgroups of $S_5$ should be unions of some conjugacy classes. The order of a subgroup must be a divisor of $|S_5| = 120$, and the subgroup must contain the identity element. Therefore, the non-trivial normal subgroups of $S_5$ cannot be the union of two conjugacy classes. The union of three conjugacy classes only has $1 + 15 + 24 = 40$ as a divisor of $120$, but $(12)(34)(12345) = (1)(245)(3)$ does not belong to this union. The union of four conjugacy classes only has $1 + 15 + 20 + 24 = 60$ as a divisor of $120$, one of which is exactly $A_5$, and another union is not closed under the operation. The union of five or six conjugacy classes does not have an element count that is a divisor of $120$. Therefore, the normal subgroups of $S_5$ are only three: $\{(1)\}$, $A_5$, $S_5$.

---

### 22. 设 $G$ 为 $p$-群，$N \triangleleft G$, 且 $|N| = p$。证明：$N \subseteq Z(G)$。

Since $N \triangleleft G$, there is a conjugation action of group $G$ on set $N$
Let $\Omega_0$ denote the set of fixed points of the conjugation action of group $G$ on $N$. Since the set of fixed points of the conjugation action of $G$ on $G$ is $Z(G)$, we have $\Omega_0 = Z(G) \cap N$. Since $G$ is a $p$-group, according to Proposition 4 of this section, $|Z(G) \cap N| \equiv |N| \ (\text{mod } p)$. Since $|N| = p$ and $Z(G) \cap N < N$, we have $|Z(G) \cap N| = p$. Thus, $N = Z(G) \cap  N \subseteq Z(G) $. 

---

### 23. 设 $G$ 是一个群，$G$ 的所有子群组成的集合记作 $\Omega$。令 $G \times \Omega \to \Omega: (a, H) \mapsto aHa^{-1}$。容易看出这给出了群 $G$ 在 $\Omega$ 上的一个作用。$H$ 的轨道 $G(H)$ 是由 $H$ 的所有共轭子群组成的。$H$ 的稳定子群 $G_H = \{g \in G \mid gHg^{-1} = H\}$ 称为 $H$ 在 $G$ 中的正规化子 (normalizer)，记作 $N_G(H)$。显然，$H \triangleleft N_G(H)$。证明：如果 $G$ 为有限群，$H < G$，则 $H$ 的共轭子群的个数等于 $[G: N_G(H)]$。

This follows immediately from the Orbit-Stabilizer Theorem.

---

### 24. 设 $H$ 是有限群 $G$ 的一个非平凡子群，则 $G \ne \bigcup_{g \in G} gHg^{-1}.${1.5.24}
 
The number of conjugacy classes of $H$ equals $[G : N_G(H)]$, and $|gHg^{-1}| = |H|$. Since $H$ is non-trivial and the identity element $e$ of $G$ belongs to each conjugacy class, we have $|\bigcup_{g \in G} gHg^{-1}| < [G : N_G(H)]|H|$. If $G = \bigcup_{g \in G} gHg^{-1}$, then

$ |G| = |\bigcup_{g \in G} gHg^{-1}| < [G : N_G(H)]|H| = \frac{|G|}{|N_G(H)|}|H|. $

This implies that $|N_G(H)| < |H|$. This contradicts with $H \subseteq N_G(H)$. Therefore, $G \neq \bigcup_{g \in G} gHg^{-1}$.

---

### 25. 设 $G$ 为一个 $2k$ 阶群，$k$ 为奇数，证明：$G$ 必有指数为 2 的子群。

Consider the left multiplication of group $G$ on set $G$. Since $|G| = 2k$, there is an isomorphism 
$$ 
\psi:G \to S_{2k}, a \mapsto \psi_{(a)}, \psi_{(a)} x:=a\circ x=ax.\\
a\in \ker  \psi \Leftrightarrow \psi_{(a)}=I \Leftrightarrow ax=x,\forall x\in G \Leftrightarrow a=e
$$

Then by the **Fundamental Theorem of Homomorphisms**
$$ 
G \cong \text{Im}  \psi,|G|=|\text{Im} \psi|=2k
$$

By the exercise[1.2.9](#1.2.9), there exists 2-order element $\psi_{(a)}$ in $\text{Im} \psi$. According to the **cycle decomposition** of a permutation, $\psi_{(a)}$ must be the product of some 2-cycles. Suppose $\psi_{(a)}$ has a fixed point $x$, then $ax = x$. Thus, $\varphi(a) = \varphi(e) = (1)$, which is a contradiction. 
And since there are a total of 2k elements, k disjoint 2-cycles are needed to cover all the elements. Therefore, the cycle decomposition of $\varphi(a)$ is

$$ \varphi(a) = (i_1 i_2)(i_3 i_4)\cdots(i_{2k-1} i_{2k}), $$

which contains $k$ transpositions. Since $k$ is odd, $\varphi(a)$ is an odd permutation. According to exercise[1.4.15](#1.4.15), the permutation group $\text{Im}\varphi$ must have a subgroup $\widetilde{H}$ of index $2$. Thus, $G$ has a subgroup $\varphi^{-1}(\widetilde{H})$ of index $2$.




---

### 26. Let $H$ be a subgroup of the group $G$, then the kernel of the left multiplication action of $G$ on the left coset set $(G/H)_l$ is equal to $\bigcap_{x \in G} xHx^{-1}$。{1.5.26}

$a$ belongs to the kernel of the left multiplication action of group $G$ on the left coset set $(G/H)_l$

$\Leftrightarrow a \circ xH = xH, \forall xH \in (G/H)_l \Leftrightarrow axH = xH, \forall xH \in (G/H)_l$

$\Leftrightarrow x^{-1}ax \in H, \forall x \in G \Leftrightarrow a \in xHx^{-1}, \forall x \in G。$

Therefore, the kernel of the left multiplication action of group $G$ on the left coset set $(G/H)_l$ is equal to $\bigcap_{x \in G} xHx^{-1}$.

---

### 27. 设 $G$ 为一个有限群，$H < G$, 且 $[G:H] = n > 1$。证明：$G$ 或者有一个指数整除 $n!$ 的非平凡正规子群，或者 $G$ 同构于 $S_n$ 的一个子群。
Consider the group $G$ acting on the left coset set $(G/H)_l$ by left multiplication. Since $[G:H]=n>1$, there is a homomorphism $\phi$ from $G$ to $S_n$.

Case 1: $\text{Ker}\phi=\{e\}$. Then $G \cong \text{Im}\phi$. Thus, $G$ is isomorphic to a subgroup of $S_n$.

Case 2: $\text{Ker}\phi \neq \{e\}$. Then $G/\text{Ker}\phi \cong \text{Im}\phi$. Therefore, $[G:\text{Ker}\phi]=|\text{Im}\phi|$, and $\text{Im}\phi \leq S_n$, so $|\text{Im}\phi|$ is a factor of $n!$. Hence, the normal subgroup $\text{Ker}\phi$ of $G$ has an index that divides $n!$. According to problem[1.5.26](1.5.26), $\text{Ker}\phi = \bigcap_{x \in G} xHx^{-1}$. Thus, $\text{Ker}\phi \subseteq H$. Since $H \neq G$, $\text{Ker}\phi \neq G$. Therefore, $\text{Ker}\phi$ is a non-trivial normal subgroup of $G$.


---

### 32. 设群 $G$ 与群 $H$ 分别作用在集合 $\Omega$ 和 $W$ 上。令$$(g, h) \circ  (x, y) \stackrel{\text{def}}{=} (g \circ  x, h \circ  y),$$ 易证明这给出了群 $G \times H$ 在集合 $\Omega \times W$ 上的一个作用，称它是乘积作用 (product action)。 $\Omega \times W$ 里的元素 $(x, y)$ 的轨道 $(G \times H){(x, y)}=G(x)\times H(y)$， $(x, y)$ 的稳定子群 $(G \times H)_{(x, y)}=G_{(x)}\times H_{(y)}$。 -->

---

