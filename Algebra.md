[TOC]
# 第零章 杂题和小结论
## 其他
## 1.1 \(| GL_n(\mathbb{F}_p) |\)=  \(\prod_{k=0}^{n-1} (p^n - p^k)\) 
证明：一个 \( n \times n \) 可逆矩阵的 \( n \) 个列向量必须线性无关。      第 1 列：可以是 \( \mathbb{F}_p^n \) 中任意非零向量，共 \( p^n - 1 \) 种选择。      第 2 列：不能与第 1 列共线（即不在其张成的 1 维子空间中），共 \( p^n - p \) 种选择。      第 3 列：不能在前两列张成的 2 维子空间中，共 \( p^n - p^2 \) 种选择。        依此类推，直到第 \( n \) 列。    <div style="text-align: right;font-size: 20px;">▢</div> 
 
   
 ## 1.2 群 \( G \) 的类方程是 \( 1 + 4 + 5 + 5 + 5 \)  
 ### (1) \( G \) 有 5 阶子群吗？如果有，它是正规子群吗？ 
 证明：设共轭类依次为 $G(x_1), G(x_2), G(x_3), G(x_4), G(x_5)$，阶数依次为 $1, 4, 5, 5, 5$。由轨道稳定子定理知 $C_G(x_2)$ 阶数为 $|G|/|G(x_2)|$。于是 $C_G(x_2)$ 为 $G$ 的 一个 5 阶子群。断言 $G$ 只有这一个5阶子群。若不然：   设 $<r>$,$<s>$ 为 $G$ 的两个不同五阶子群，则 $<r>\cap <s> = {e}$(否则他们相同)。于是有 $r^is^j=r^ms^n \Leftrightarrow r^{i-m}=s^{n-j} \equiv e \Leftrightarrow m=n,i=j$(这里规定 $0\le i,j, m,n\le 5$ )于是有 $|G|\ge |\{r^is^j|0\le i,j\le 5\}|=25$ ,矛盾！ ### (2) \( G \) 有 4 阶子群吗？如果有，它是正规子群吗？ 同上 $C_{G}(x_i),i=3,4,5$ 即为所求。断言他们三都不是正规子群。若不然：   不妨设 $C_G(x_3) \triangleleft G,$ 则 $ \forall g\in G,gC_G(x_3) g^{-1} =C_G(x_3)$。$\forall a\in C_G(x_3) ,ax_3=x_3a, gag^{-1}x_3=x_3gag^{-1},ag^{-1}x_3g= g^{-1}x_3ga ,i.e.  a\in C_G(g^{-1}x_3g)$,于是 $C_G(x_3) \subseteq C_G(g^{-1}x_3g)$。同理 $C_G(g^{-1}x_3g) \subseteq C_G(x_3) $。于是 $C_G(g^{-1}x_3g) = C_G(x_3) $     由于 $\phi :G\rightarrow G, a \mapsto gag^{-1}$ 为双射，故 $\exists g_0\in G,s.t.x_i=a_i x_3a_i^{-1},i \ne 3$。 于是 $C_G(x_3)=C_G(x_i), i\ne 3 $, 这不可能！ 
 
 
 
 
 
 ## 1.2 The Class Equation of Group $ G $ is $ 1 + 4 + 5 + 5 + 5 $ 
 ### (1) Does $ G $ have a subgroup of order 5? If so, is it a normal subgroup? 
 Let the conjugacy classes be denoted as $ G(x_1), G(x_2), G(x_3), G(x_4), G(x_5) $, with orders $ 1, 4, 5, 5, 5 $, respectively. By the Orbit-Stabilizer Theorem, the order of the centralizer $ C_G(x_2) $ is $ |G| / |G(x_2)|=5$. Thus, $ C_G(x_2) $ is a subgroup of $ G $ of order 5. We claim that $ G $ has only one subgroup of order 5.   
 Suppose not:   Let $ \langle r \rangle $ and $ \langle s \rangle $ be two distinct subgroups of $ G $ of order 5. Then $ \langle r \rangle \cap \langle s \rangle = \{ e \} $ (otherwise, they would be the same). This implies that $ r^i s^j = r^m s^n \Leftrightarrow r^{i-m} = s^{n-j} \equiv e \Leftrightarrow m = n, i = j $ (where $ 0 \leq i, j, m, n \leq 5 $). Therefore, $ |G| \geq |\{ r^i s^j \mid 0 \leq i, j \leq 5 \}| = 25 $, which is a contradiction! 
 ### (2) Does $ G $ have a subgroup of order 4? If so, is it a normal subgroup? 
 Similarly, $ C_G(x_i) $ for $ i = 3, 4, 5 $ are the desired subgroups. We claim that none of them are normal subgroups.   
 Suppose not:   Without loss of generality, assume $ C_G(x_3) \triangleleft G $. Then, for all $ g \in G $, $ g C_G(x_3) g^{-1} = C_G(x_3) $. For all $ a \in C_G(x_3) $, $ a x_3 = x_3 a $, and $ g a g^{-1} x_3 = x_3 g a g^{-1} $. This implies $ a g^{-1} x_3 g = g^{-1} x_3 g a $, i.e., $ a \in C_G(g^{-1} x_3 g) $. Thus, $ C_G(x_3) \subseteq C_G(g^{-1} x_3 g) $. Similarly, $ C_G(g^{-1} x_3 g) \subseteq C_G(x_3) $. Therefore, $ C_G(g^{-1} x_3 g) = C_G(x_3) $.   
 Since the map $ \phi: G \rightarrow G $, $ a \mapsto g a g^{-1} $ is a bijection, there exists $ g_0 \in G $ such that $ x_i = a_i x_3 a_i^{-1} $ for $ i \neq 3 $. This implies $ C_G(x_3) = C_G(x_i) $ for $ i \neq 3 $, which is impossible! 

## 群
## 环
## 域

# 第一章 群
## §1 群的典型例子：循环群，二面体群，矩阵群，对称群

### 7.设 $m$ 是正整数，在 $0, 1, 2, \dots, m-1$ 中，与 $m$ 互素的整数的个数记作 $\varphi(m)$，称它为 Euler (欧拉) 函数。证明：$Z_m$ 的单位群 $Z_m^*$ 的阶等于 $\varphi(m)$。

### 12.设 $\sigma = (i_1, i_2, \dots, i_r)$，则对于任意 $\tau \in S_n$，有$$\tau \sigma \tau^{-1} = (\tau(i_1), \tau(i_2), \dots, \tau(i_r))$$

## §2 子群，陪集，Lagrange 定理，循环群的子群

### 2. 设 $H, K$ 都是群 $G$ 的子群，令 $HK \stackrel{\text{def}}{=} \{hk \mid h \in H, k \in K\}$。证明：$HK$ 为子群当且仅当 $HK = KH$。


### 5. 证明：(1) $S_n = \langle (12), (23), \dots, (n-1 \ n) \rangle$; (2) $S_n = \langle (12), (12 \dots n) \rangle$.

### 6. 证明：当 $n \geq 3$ 时，(1) $A_n$ 由 3-轮换生成；(2) $A_n = \langle (123), (124), \dots, (12n) \rangle$.


### 9. 证明：如果群 $G$ 的阶为偶数，则 $G$ 必有 2 阶元素。
### 10.  证明 Euler 定理：设 $n$ 是正整数，如果整数 $a$ 与 $n$ 互素，则$$a^{\varphi(n)} \equiv 1 \pmod{n},$$ 其中 $\varphi(n)$ 是 Euler 函数。

### 13. (1) 写出 $A_4$ 的所有子群；(2) 证明 $A_4$ 没有 6 阶子群。
### 14. 设 $H, K$ 是群 $G$ 的有限子群，证明：$$|HK| = \frac{|H| \cdot |K|}{|H \cap K|}$$

## §3 群的同构，群的直积

### 1. 证明实数加群R与正实数乘法群R*同构.
### 2. 在Z₈的单位群Z₈*中,2的阶是多少? Z₈*与Z₆的加法群同构吗?
### 3. Z₆*与Klein群 Z₂×Z₂同构吗?
### 4. 习题1.2的第4题中,正方形棋盘的对称(性)群G与A₄的子群K={(1),(12)(34), (13)(24), (14)(23)}同构吗?
### 5. 证明:D₃≅S₃.
### 6. 设G是一个群,证明:映射 σ:x→x⁻¹是G到G的同构映射当且仅当G是Abel 群.
### 7. 正四面体的旋转对称(性)群G₁,正十二棱锥的旋转对称(性)群G₂,正六边形的对称(性)群D₆都是12阶群,这三个群彼此同构吗?
### 8. 证明:Z₃×V≅Z₂×Z₆,其中V是 Klein 群.

### 9.    Z₂₄, Z₁₂×Z₂, Z₆×Z₄, Z₂×Z₄×Z₃ 这四个24阶 Abel群中,哪些是彼此同构的?


### 10. D₁₂, D₄×Z₃, A₄×Z₂ 这三个24 阶非交换群中,有同构的吗?   

### 11.  证明:当 n是奇数时,D₂ₙ≅Dₙ×Z₂.

### 12. 设 n为奇数,证明:   (1) Oₙ≅SOₙ×{I,-I};   (2) Oₙ≅SOₙ×Z₂.




## §4 群的同态，正规子群，商群，可解群
### 8. 设群 $G$ 是子群 $H$ 与 $K$ 的内直积，证明：$H \triangleleft G, K \triangleleft G$, 并且$$ G/H \cong K, G/K \cong H.$$

### 10. 分别求 $D_{2m}, D_{2n}$ 的换位子群，其中 $m \geq 2$。

### 12. 求 $S_n$ 的换位子群，其中 $n \geq 3$。
### 13. 证明：当 $n \geq 5$ 时，$A_n' = A_n$。
### 14. 写出 $S_4$ 的导群列，由此看出，$S_4$ 是可解群。
### 15. 证明：如果置换群 $G$ 含有奇置换，则 $G$ 必有指数为 2 的子群。
### 16. 设 $\sigma$ 是群 $G$ 到群 $G'$ 的一个满同态，记 $K = \text{Ker } \sigma$。设 $H' \triangleleft G'$，令 $\sigma^{-1}(H') \stackrel{\text{def}}{=} \{g \in G \mid \sigma(g) \in H'\}$。证明：(1) $\sigma^{-1}(H') \triangleleft G$, 且 $\sigma^{-1}(H') \supseteq K$;    (2) $H' \mapsto \sigma^{-1}(H')$ 是 $G'$ 的子群集合到 $G$ 的包含 $K$ 的子群集合的一个双射。
### 17. 证明：当 $n \geq 5$ 时，$A_n$ 是单群。
### 18. 设 $G$ 是一个群，$N \triangleleft G, H \triangleleft G$。如果$$G = NH, 且 N \cap H = \{e\},$$ 则称 $G$ 可分解成它的正规子群 $N$ 与子群 $H$ 的半直积 (semidirect product)。证明：如果 $G$ 可分解成正规子群 $N$ 与子群 $H$ 的半直积，则$$G/N \cong H.$$

### 19. 证明：$S_n$ 可分解成 $A_n$ 与 $\langle (12) \rangle$ 的半直积，其中 $n \geq 3$。

## §5 群在集合上的作用，群的自同构，轨道-稳定子定理

### 4. 设 $F$ 是一个域，求 $GL_n(F)$ 的中心。
### 5. $GL_2(C)$ 的每一个元素$$\begin{pmatrix} a & b \\ c & d \end{pmatrix}$$ 引起了扩充复平面 $C \cup \{\infty\}$ 上的一个变换：$$z \mapsto \frac{az + b}{cz + d},$$ 称它为 Möbius (默比乌斯) 变换。证明：(1) 所有 Möbius 变换组成的集合 $G$ 对于变换的乘法成一个群，称它为 Möbius 群；(2) $GL_2(C) / Z(GL_2(C)) \cong G$.

### 6. 设 $G$ 是一个群，证明：如果 $G/Z(G)$ 是循环群，则 $G$ 是 Abel 群。
### 7. 分别求 $D_{2m-1}, D_{2m}$ 的中心，其中 $m \geq 2$。
### 8. 求 $S_n$ 的中心，其中 $n \geq 3$。
### 9. 分别求 $U_5, U_6$ 的自同构群。
### 10. 求 $Z_2 \times Z_2$ 的自同构群。
### 11. 求 $S_3$ 的自同构群。
### 12. 群 $G$ 的一个子群 $H$ 称为 $G$ 的特征子群 (characteristic subgroup)，如果 $G$ 的每一个自同构把 $H$ 映成 $H$ 自身，即对于所有的 $\tau \in \text{Aut}(G)$，有 $\tau(H) = H$。证明：$G$ 的中心 $Z(G)$ 和 $G$ 的换位子群 $G'$ 都是 $G$ 的特征子群。

### 14. 分别求 $D_{2m-1}, D_{2m}$ 的所有共轭类，其中 $m \geq 2$。
### 15. 设 $\sigma$ 的不相交的轮换分解式 (包含所有的 1-轮换) 为$$\sigma = (a_1 a_2 \dots a_{l_1})(b_1 b_2 \dots b_{l_2}) \dots (q_1 q_2 \dots q_{l_r})$$ 其中 $l_1 \geq l_2 \geq \dots \geq l_r$, 且 $l_1 + l_2 + \dots + l_r = n$。则我们把有序数组 $(l_1, l_2, \dots, l_r)$ 称为置换 $\sigma$ 的型 (type)，也称为 $n$ 的一个分拆 (partition)。证明：(1) $\sigma_1$ 与 $\sigma_2$ 在 $S_n$ 中共轭当且仅当 $\sigma_1$ 与 $\sigma_2$ 同型；(2) $S_n$ 中共轭类的个数等于 $n$ 的分拆的个数。  

### 16. 求 $S_4$ 的共轭类的个数，以及每个共轭类的代表和元素数目。
### 17. 求 $A_4$ 的共轭类的个数，以及每个共轭类的代表和元素数目。
### 18. 设 $\sigma$ 是一个 $n$-轮换。求 $\sigma$ 的共轭类的元素数目，以及 $C_{S_n}(\sigma)$ 的阶。
### 19. 求 $O_2$ 的所有共轭类。
### 20. 证明：群 $G$ 的子群 $H$ 为正规子群当且仅当 $H$ 是 $G$ 的一些共轭类的并集。
### 21. (1) 求 $S_5$ 的共轭类的个数，以及每个共轭类的代表和元素数目；(2) 证明：$S_5$ 只有三个正规子群，即 $\{1\}, A_5, S_5$。
### 22. 设 $G$ 为 $p$-群，$N \triangleleft G$, 且 $|N| = p$。证明：$N \subseteq Z(G)$。
### 23. 设 $G$ 是一个群，$G$ 的所有子群组成的集合记作 $\Omega$。令 $G \times \Omega \to \Omega: (a, H) \mapsto aHa^{-1}$。容易看出这给出了群 $G$ 在 $\Omega$ 上的一个作用。$H$ 的轨道 $G(H)$ 是由 $H$ 的所有共轭子群组成的。$H$ 的稳定子群 $G_H = \{g \in G \mid gHg^{-1} = H\}$ 称为 $H$ 在 $G$ 中的正规化子 (normalizer)，记作 $N_G(H)$。显然，$H \triangleleft N_G(H)$。证明：如果 $G$ 为有限群，$H < G$，则 $H$ 的共轭子群的个数等于 $[G: N_G(H)]$。
### 24. 设 $H$ 是有限群 $G$ 的一个非平凡子群，证明：$$\bigcap_{g \in G} gHg^{-1}.$$
### 25. 设 $G$ 为一个 $2k$ 阶群，$k$ 为奇数，证明：$G$ 必有指数为 2 的子群。
### 26. 设 $G$ 为一个有限群，$H < G$, 且 $[G:H] = n > 1$。证明：$G$ 或者有一个指数整除 $n!$ 的非平凡正规子群，或者 $G$ 同构于 $S_n$ 的一个子群。
### 27. 设 $G$ 为一个有限群，$p$ 为 $|G|$ 的最小素因子。证明：指数为 $p$ 的子群 (如果存在) 必为正规子群。
### 28. 正方体的 6 个面用红、绿两种颜色染色，求真正不同的染色方案的个数。
### 29. 设群 $G$ 在集合 $\Omega$ 和 $\Omega'$ 上分别作用 “” 和 “\*”。如果在 $\Omega$ 与 $\Omega'$ 之间有一个双射 $\psi$，使得$$\psi(a \cdot x) = a * \psi(x), \quad \forall a \in G, x \in \Omega,$$
### 也就是，使得下图的图 1-7 可交换：

(图 1-7 描述了等价作用，由于无法直接绘制，这里省略)

### 则称 $G$ 的这两个作用是等价的 (equivalent)。
### 证明：群 $G$ 在任一集合 $\Omega$ 上的传递作用等价于群 $G$ 在左商集 $(G/G_x)$ 上的左平移，其中 $x \in \Omega$。

### 30. 设 $N$ 和 $H$ 是两个群，并且 $H$ 到 $\text{Aut}(N)$ 有一个同态 $\psi$。在集合 $N \times H$ 上定义一个二元运算如下：$$(n_1, h_1)(n_2, h_2) \stackrel{\text{def}}{=} (n_1 \cdot \psi(h_1)(n_2), h_1 \cdot h_2),$$ 证明 $N \times H$ 成为一个群，称它为 $N$ 与 $H$ 的半直积 (semidirect product)，记作 $N \rtimes H$。

### 31. 令 $N = (n, e) \mid n \in N$, 证明：$N \triangleleft N \rtimes H$, 且 $N \cap H = N$。
### 32. 设群 $G$ 与群 $H$ 分别作用在集合 $\Omega$ 和 $W$ 上。令$$(g, h) \cdot (x, y) \stackrel{\text{def}}{=} (g \cdot x, h \cdot y),$$ 证明这给出了群 $G \times H$ 在集合 $\Omega \times W$ 上的一个作用，称它是乘积作用 (product action)。求 $\Omega \times W$ 里的元素 $(x, y)$ 的轨道 $(G \times H)_{(x, y)}$，以及 $(x, y)$ 的稳定子群 $(G \times H)_{(x, y)}$。

## §6 Sylow定理

### 1. 证明不存在阶为 148 的单群。
### 2. 证明不存在阶为 36 的单群。
### 3. 证明不存在阶为 56 的单群。
### 4. 证明不存在阶为 30 的单群。
### 5. 证明 6 阶群或者是循环群，或者同构于 $S_3$。
### 6. 决定 10 阶群的类型。
### 7. 决定 15 阶群的类型。
### 8. 决定 35 阶群的类型。
### 9. 决定 21 阶群的类型。
### 10. 设 $p, q$ 都是素数，且 $p < q$。决定 $pq$ 阶群的类型。
### 11. 设 $p, q$ 是不同的素数。证明 $p^2q$ 阶群必包含一个正规的 Sylow 子群。
### 12. 设群 $G$ 的阶为 $p^3$，其中 $p$ 是素数。证明：如果 $G$ 是非交换群，则 $|Z(G)| = p$, 且 $Z(G) = G'$.
### 13. 设 $p$ 是素数。计算 $S_p$ 中 Sylow $p$-子群的个数。由此证明 Wilson 定理：$$(p-1)! \equiv -1 \pmod{p}.$$
### 14. 设 $G$ 为一个有限群，$N \triangleleft G$, $P$ 是 $N$ 的一个 Sylow $p$-子群。证明：$G = N \cdot N_G(P)$.
### 15. 证明：如果有限群 $G$ 有一个循环的 Sylow 2-子群，则 $G$ 有一个指数为 2 的子群。

## §7 有限Abel群的结构

### 1. 决定 12 阶 Abel 群的互不同构的类型。
### 2. 决定 108 阶 Abel 群的互不同构的类型。
### 3. 决定 360 阶 Abel 群的互不同构的类型。
### 4. 决定 144 阶 Abel 群的互不同构的类型。
### 5. 决定 216 阶 Abel 群的互不同构的类型。
### 6. 求下列群的初等因子：(1) $Z_{16} \times Z_{15} \times Z_{20}$; (2) $Z_9 \times Z_{45}$; (3) $Z_4 \times Z_{14} \times Z_{16}$.
### 7. 设 $G$ 是 100 阶 Abel 群。(1) 证明 $G$ 必含有 10 阶元；(2) $G$ 的初等因子应当怎样才能使 $G$ 不含大于 10 的元素？

### 8. 证明：如果有限 Abel 群的阶没有平方因子，则它必为循环群。
### 9. 证明：一个 Abel $p$-群如果恰好有 $p-1$ 个 $p$ 阶元，则它一定是循环群。
### 10. 设 $V$ 是域 $Z_2$ 上的 $n$ 维线性空间，决定 $V$ 的加法群的结构，写出它的初等因子，它是不是初等 Abel 2-群？
### 11. 设 $V$ 是域 $Z_p$ 上的 $n$ 维线性空间，$p$ 是素数。$V$ 的加法群是不是初等 Abel $p$-群？

## §8 自由群，群的表现

### 1. 把下列由字母表 $X = \{x, y, z\}$ 形成的字化简成既约字：    (1) $w_1 = x^{-1} y^4 y^{-1} y^{-3} z z^{-2} y^{-1} z^{-1}$;    (2) $w_2 = z^{-2} y^3 x^{-2} x^{-2} y x^2 z^{-3} z^3$;    (3) $w_3 = z_3^2 y x x^{-1} x z^{-1} y^2 z^{-1} y^{-1}$.


### 2. $w_1, w_2, w_3$ 同第 1 题，求 $w_1 w_2 w_3$。
### 3. 在 3-辫群 $B_3$ 中，求 $b_1^2, b_2^2, b_1 b_2$，其中 $b_1, b_2$ 是初等辫子 (见 §8 的图 1-10)。
### 4. 在 3-辫群 $B_3$ 中，分别写出 $b_1^2, b_2^2, b_1 b_2$ 产生的 $S_3$ 中的置换。
### 5. 找出 $B_3$ 中的两个不同的辫子，它们都产生置换 (132)。
### 6. 在 4-辫群 $B_4$ 中，求 $b_1 b_3, b_3 b_1$ 和 $b_3 b_1 b_3^{-1}$，其中 $b_1, b_3$ 都是初等辫子 (见 §8 的图 1-14)。从所画的图看，$b_1 b_3$ 与 $b_3 b_1$ 相等吗？
### 7. 设 $G$ 和 $G'$ 是两个群，$x_1, x_2, \dots, x_n$ 称为一个字，其中每个 $x_i$ 属于无交并 $G \cup G'$ (即，把 $G$ 的元素与 $G'$ 的元素看成不同的元素形成的并集，注意即使 $G = G'$，在求无交并 $G \cup G'$ 时，也需要把前一个集合 $G$ 与后一个集合 $G$ 的元素看成不同的元素)。称一个字是既约的，如果 $x_i$ 与 $x_{i+1}$ 不在同一个群里 (1 ≤ i < n)，并且 $x_i$ 不是 $G$ 或 $G'$ 的单位元 (1 ≤ i ≤ n)。可证明每一个字能化简成唯一的既约字 (类似于本节定理 1 的证法)。两个既约字 $w_1$ 与 $w_2$ 相乘就是在 $w_1$ 后面接着写 $w_2$，然后把它化简成既约字。所有既约字连同字空间的集合对于上述乘法成一个群，称它为 $G$ 与 $G'$ 的自由积 (free product)，记作 $G * G'$。证明：$Z * Z \cong F_2$，其中 $F_2$ 代表由 2 个元素生成的自由群。



# 第二章 环

## §1 环的类型和性质，理想

### 1. 设 $F$ 是一个域，令$$S = \{aE_{11} \mid a \in F\},$$ 证明 $S$ 是 $M_n(F)$ 的一个子环，并且求 $S$ 的单位元。

### 2. 证明有限整环是域。
### 3. 令$$H = \left\{ \begin{pmatrix} \alpha & \beta \\ -\overline{\beta} & \overline{\alpha} \end{pmatrix} \mid \alpha, \beta \in C \right\},$$ 证明 $H$ 是一个除环。

### 4. 设 $R$ 是有单位元的环，证明 $R$ 的每一个非平凡的理想都不能含有单位元。
### 5. 证明域 $F$ 没有非平凡的理想。
### 6. 设 $R$ 是一个有单位元的交换环，证明：如果 $R$ 没有非平凡的理想，则 $R$ 是一个域。
### 7. 设 $I$ 是交换环 $R$ 的一个理想。令$$\text{rad } I = \{r \in R \mid r^n \in I \text{ 对某一正整数 } n \}.$$ 证明 $\text{rad } I$ 也是 $R$ 的一个理想。称 $\text{rad } I$ 是 $I$ 的根 (radical)。

### 8. 环 $R$ 中元素 $a$ 称为零幂元 (nilpotent element)，如果有一个正整数 $n$，使得 $a^n = 0$。证明：如果 $a$ 是有单位元的环 $R$ 中的零幂元，则 $1-a$ 可逆。
### 9. 证明：在交换环 $R$ 中，所有零幂元组成的集合是 $R$ 的一个理想，称为 (0) 的根，称为 $R$ 的零幂根 (nilradical)。
### 10. 设 $D$ 是一个除环，证明 $M_n(D)$ 是单环。











## §2 商环，环的同态，环的直和

### 1. 设$$R = \left\{ \begin{pmatrix} \alpha & \beta \\ -\overline{\beta} & \overline{\alpha} \end{pmatrix} \mid \alpha, \beta \in C \right\},$$证明环 $R$ 与四元数体 $H$ 同构。

### 2. 设 $\sigma$ 是环 $R$ 到环 $R'$ 的一个满同态。证明：    (1) 如果 $I$ 是 $R$ 的一个理想，则 $\sigma(I)$ 是 $R'$ 的理想；    (2) 如果 $I'$ 是 $R'$ 的一个理想，则 $\sigma^{-1}(I')$ 是 $R$ 的理想，且 $\text{Ker } \sigma \subseteq \sigma^{-1}(I')$.


### 3. 求出“物不知其数”问题的解。
### 4. 在 $Z/(35)$ 中，分别求 $\overline{1}$ 的平方根和 $\overline{4}$ 的平方根。
### 5. 在 $Z/(35)$ 中，$\overline{2}$ 的平方根存在吗？$\overline{3}$ 的平方根存在吗？
### 6. 设正整数 $n = p_1^{r_1} p_2^{r_2} \dots p_s^{r_s}$，其中 $p_1, p_2, \dots, p_s$ 是两两不同的素数，$r_i > 0, i = 1, 2, \dots, s$。证明：$$    Z/(n) \cong Z/(p_1^{r_1}) \oplus Z/(p_2^{r_2}) \oplus \dots \oplus Z/(p_s^{r_s}).    $$

## §3素理想和极大理想，有限域的构造

### 1. 证明本节命题 2：域 $F$ 上一元多项式环 $F[x]$ 的每一个理想都是主理想，其中非 (0) 的主理想可以由首项系数为 1 的多项式生成。
### 2. 设 $R$ 是有单位元 ($\neq 0$) 的交换环，$R$ 是 $R$ 的一个子环，并且 $R$ 与 $R$ 有相同的单位元。设 $P$ 是 $R$ 的一个素理想，证明 $P \cap R$ 是 $R$ 的一个素理想。
### 3. 求 $\text{Spec } Z/(30)$.
### 4. 设 $F$ 是一个域，证明：如果 $p(x)$ 是 $F[x]$ 的不可约多项式，则 $F[x]/(p(x))$ 是一个域。
### 5. 设 $F$ 是一个域，证明：如果 $f(x)$ 是 $F[x]$ 的可约多项式，则 $F[x]/(f(x))$ 有非平凡的零因子。
### 6. 构造含 4 个元素的有限域，写出它的加法运算表和乘法运算表。
### 7. 构造含 9 个元素的有限域。
### 8. 构造含 8 个元素的有限域。
### 9. 设 $R = 2Z$，证明 \$4Z$ 是 $R$ 的一个极大理想，但是 $R/4Z$ 不是域。
### 10. 设 $R$ 是有单位元 $e (\neq 0)$ 的环，令 $Z_R = \{ne \mid n \in Z\}$.    (1) 证明 $Z_R$ 是 $R$ 的一个子环，且 $Z/m \cong Z_R$，其中 $m$ 某一个非负整数；我们把 $m$ 叫做环 $R$ 的特征。  (2) 如果 $R$ 是整环，则 $R$ 的特征为 0 或者是一个素数。
### 11. 设 $R$ 是一个有单位元 ($\neq 0$) 的交换环，证明：如果 $R$ 的每一个理想都是素理想，则 $R$ 是一个域。
### 12. 设 $R$ 是一个交换环



## § 4代数数域和Galois环的构造



## §5 分式域




## §6 唯一因子分解整环，主理想整环，Euclid(欧几里得)整环


# 第三章 域扩张及其自同构

### §1 域扩张，分裂域，正规扩张，可分扩张  
### §2 域扩张的自同构群，Galois 扩张，Galois 基本定理  
### §3 本原元素，迹与范数  
