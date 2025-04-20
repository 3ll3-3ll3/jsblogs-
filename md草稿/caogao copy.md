

# 第一章 群

## §1 群的典型例子：循环群，二面体群，矩阵群，对称群

**习题 1.1**
### 7.设 $m$ 是正整数，在 $0, 1, 2, \dots, m-1$ 中，与 $m$ 互素的整数的个数记作 $\varphi(m)$，称它为 Euler (欧拉) 函数。证明：$Z_m$ 的单位群 $Z_m^*$ 的阶等于 $\varphi(m)$。  
设 3 阶实矩阵 A 为  
$$  
A = \begin{pmatrix}  
\frac{2}{3} & \frac{1}{3} & \frac{2}{3} \\  
\frac{2}{3} & \frac{2}{3} & \frac{1}{3} \\  
-\frac{1}{3} & \frac{2}{3} & -\frac{2}{3}  
\end{pmatrix}  
$$  
(1) 证明 $A \in SO_3$;  
(2) $A$ 可以表示空间中绕哪一条直线的旋转？  
在 $S_5$ 中，设  
$$  
\sigma_1 = \begin{pmatrix}  
1 & 2 & 3 & 4 & 5 \\  
3 & 1 & 5 & 2 & 4  
\end{pmatrix}, \quad  
\sigma_2 = \begin{pmatrix}  
1 & 2 & 3 & 4 & 5 \\  
4 & 5 & 1 & 3 & 2  
\end{pmatrix}  
$$  
(1) 求 $\sigma_1 \sigma_2, \sigma_2 \sigma_1$;  
(2) 分别写出 $\sigma_1, \sigma_2$ 的轮换分解式；  
(3) 求 $\sigma_1^{-1}, \sigma_1 \sigma_2 \sigma_1^{-1}$;  
(4) 分别写出 $\sigma_1, \sigma_2$ 的一种对换分解式；  
(5) 说出 $\sigma_1, \sigma_2$ 是偶置换，还是奇置换。  
$r$-轮换是偶置换还是奇置换，与 $r$ 的奇偶性有什么关系？  
分别写出 $A_3, A_4$ 的所有元素 (用轮换分解式表示)。  
设 $\sigma = (i_1, i_2, \dots, i_r)$，则对于任意 $\tau \in S_n$，有  
$$  
\tau \sigma \tau^{-1} = (\tau(i_1), \tau(i_2), \dots, \tau(i_r)).  
$$  

### §2 子群，陪集，Lagrange 定理，循环群的子群

**习题 1.2**

设 $k$ 是一个非负整数，令 $kZ \stackrel{\text{def}}{=} \{km \mid m \in Z\}$。  
(1) 说明 $kZ$ 是整数加群 $Z$ 的子群；  
(2) 说明 $kZ$ 是循环群。  
设 $H, K$ 都是群 $G$ 的子群，令 $HK \stackrel{\text{def}}{=} \{hk \mid h \in H, k \in K\}$。  
证明：$HK$ 为子群当且仅当 $HK = KH$。  
在复数加群 $C$ 中，由 $1, i$ 生成的子群 $(1, i)$ 称为 Gauss 整数群 (group of Gaussian integers)，它的元素是什么样子？  
如图 1-4 是一个正方形的棋盘，求它的对称 (性) 群。  

![棋盘](https://i.imgur.com/your_image_url.png) (请替换 `https://i.imgur.com/your_image_url.png` 为实际的图片链接)  
证明：  
(1) $S_n = \langle (12), (23), \dots, (n-1 \ n) \rangle$;  
(2) $S_n = \langle (12), (12 \dots n) \rangle$。  
证明：当 $n \geq 3$ 时，  
(1) $A_n$ 由 3-轮换生成；  
(2) $A_n = \langle (123), (124), \dots, (12n) \rangle$。  
在 $SL_2(Q)$ 中，设群不同构  
$$  
A = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}, \quad B = \begin{pmatrix} 0 & 1 \\ -1 & -1 \end{pmatrix}.  
$$  
证明：$A$ 的阶为 4, $B$ 的阶为 3, $AB$ 为无限阶元素。  
证明：如果群 $G$ 的每一个非单位元的阶都为 2，则 $G$ 必为 Abel 群。  
证明：如果群 $G$ 的阶为偶数，则 $G$ 必有 2 阶元素。  
证明 Euler 定理：设 $n$ 是正整数，如果整数 $a$ 与 $n$ 互素，则  
$$  
a^{\varphi(n)} \equiv 1 \pmod{n},  
$$  
其中 $\varphi(n)$ 是 Euler 函数。  
求循环群 $C = \langle a \rangle$ 的所有子群。  
求 $S_3$ 的所有子群。  
(1) 写出 $A_4$ 的所有子群；  
(2) 证明 $A_4$ 没有 6 阶子群。  
设 $H, K$ 是群 $G$ 的有限子群，证明：  
$$  
|HK| = \frac{|H| \cdot |K|}{|H \cap K|}  
$$  

### §3 群的同构，群的直积

### §4 群的同态，正规子群，商群，可解群

**习题 1.4**

设 $f$ 是实数加法群 $R$ 到非零复数乘法群 $C^*$ 的一个映射：$f(x) = e^{2\pi i x}, \forall x \in R$。证明 $f$ 是一个同态；  
(1) 证明 $f$ 是一个同态；  
(2) 求 $\text{Ker } f$ 和 $\text{Im } f$。  
设 $\psi$ 是非零复数乘法群 $C^*$ 到自身的映射：$\psi(z) = \frac{z}{|z|}, \forall z \in C^*$。证明：  
(1) 证明 $\psi$ 是一个同态；  
(2) 求 $\text{Ker } \psi$ 和 $\text{Im } \psi$。  
设 $F$ 是一个域，$\sigma$ 是 $GL_n(F)$ 到 $F^*$ 的一个映射：$\sigma(A) = |A|, \forall A \in GL_n(F)$。  
(1) 证明 $\sigma$ 是一个同态；  
(2) 求 $\text{Ker } \sigma$ 和 $\text{Im } \sigma$；  
(3) 证明：$SL_n(F) \triangleleft GL_n(F)$;  
(4) 证明：$GL_n(F) / SL_n(F) \cong F^*$。  
设 $G$ 是数域 $R$ 上所有函数组成的集合，$H$ 是各项系数为 1 的所有函数组成的集合，证明：  
(1) $G$ 对于映射的乘法成一个群；  
(2) $G/H \cong R^*$, 其中 $R^*$ 是非零实数的乘法群；  
(3) $H$ 是 $G$ 的正规子群。  
设 $C$ 表示复平面上的单位圆，它对于复数乘法成一个群，证明：$R/Z \cong C$。  
设 $C^*$ 是复平面上的单位圆，证明：  
$$  
C^*/R \cong C.  
$$  
设 $G$ 和 $G'$ 是两个群，证明：$G \times \langle e' \rangle \cong \langle e \rangle \times G', |e| \times G' \triangleleft G \times G'$ 并且  
$$  
\frac{G \times G'}{G \times \langle e' \rangle} \cong G', \frac{G \times G'}{\langle e \rangle \times G'} \cong G.  
$$  
设群 $G$ 是子群 $H$ 与 $K$ 的内直积，证明：$H \triangleleft G, K \triangleleft G$, 并且  
$$  
G/H \cong K, G/K \cong H.  
$$  
分别求 $D_3, D_4$ 的换位子群。  
分别求 $D_{2m}, D_{2n}$ 的换位子群，其中 $m \geq 2$。  
求 $S_4$ 的换位子群。  
求 $S_n$ 的换位子群，其中 $n \geq 3$。  
证明：当 $n \geq 5$ 时，$A_n' = A_n$。  
写出 $S_4$ 的导群列，由此看出，$S_4$ 是可解群。  
证明：如果置换群 $G$ 含有奇置换，则 $G$ 必有指数为 2 的子群。  
设 $\sigma$ 是群 $G$ 到群 $G'$ 的一个满同态，记 $K = \text{Ker } \sigma$。设 $H' \triangleleft G'$，令 $\sigma^{-1}(H') \stackrel{\text{def}}{=} \{g \in G \mid \sigma(g) \in H'\}$。证明：  
(1) $\sigma^{-1}(H') \triangleleft G$, 且 $\sigma^{-1}(H') \supseteq K$;  
(2) $H' \mapsto \sigma^{-1}(H')$ 是 $G'$ 的子群集合到 $G$ 的包含 $K$ 的子群集合的一个双射。  
证明：当 $n \geq 5$ 时，$A_n$ 是单群。  
设 $G$ 是一个群，$N \triangleleft G, H \triangleleft G$。如果  
$$  
G = NH, 且 N \cap H = \{e\},  
$$  
则称 $G$ 可分解成它的正规子群 $N$ 与子群 $H$ 的半直积 (semidirect product)。证明：如果 $G$ 可分解成正规子群 $N$ 与子群 $H$ 的半直积，则  
$$  
G/N \cong H.  
$$  
证明：$S_n$ 可分解成 $A_n$ 与 $\langle (12) \rangle$ 的半直积，其中 $n \geq 3$。

### §5 群在集合上的作用，群的自同构，轨道-稳定子定理

**习题 1.5**

令  
$$  
Z \times R \to R \\  
(n, x) \mapsto n + x,  
$$  
说明这个映射给出了整数加群 $Z$ 在实数集 $R$ 上的一个作用。  
令  
$$  
Z \times R \to R \\  
(n, x) \mapsto (-1)^n x,  
$$  
说明这个映射给出了整数加群 $Z$ 在实数集 $R$ 上的一个作用。  
证明：映射 $\sigma: x \mapsto x^{-1}$ 是任一 Abel 群 $G$ 的一个自同构。  
设 $F$ 是一个域，求 $GL_n(F)$ 的中心。  
$GL_2(C)$ 的每一个元素  
$$  
\begin{pmatrix} a & b \\ c & d \end{pmatrix}  
$$  
引起了扩充复平面 $C \cup \{\infty\}$ 上的一个变换：  
$$  
z \mapsto \frac{az + b}{cz + d},  
$$  
称它为 Möbius (默比乌斯) 变换。证明：  
(1) 所有 Möbius 变换组成的集合 $G$ 对于变换的乘法成一个群，称它为 Möbius 群；  
(2) $GL_2(C) / Z(GL_2(C)) \cong G$。  
设 $G$ 是一个群，证明：如果 $G/Z(G)$ 是循环群，则 $G$ 是 Abel 群。  
分别求 $D_{2m-1}, D_{2m}$ 的中心，其中 $m \geq 2$。  
求 $S_n$ 的中心，其中 $n \geq 3$。  
分别求 $U_5, U_6$ 的自同构群。  
求 $Z_2 \times Z_2$ 的自同构群。  
求 $S_3$ 的自同构群。  
群 $G$ 的一个子群 $H$ 称为 $G$ 的特征子群 (characteristic subgroup)，如果 $G$ 的每一个自同构把 $H$ 映成 $H$ 自身，即对于所有的 $\tau \in \text{Aut}(G)$，有 $\tau(H) = H$。证明：$G$ 的中心 $Z(G)$ 和 $G$ 的换位子群 $G'$ 都是 $G$ 的特征子群。  
分别求 $D_5, D_6$ 的所有共轭类。  
分别求 $D_{2m-1}, D_{2m}$ 的所有共轭类，其中 $m \geq 2$。  
设 $\sigma$ 的不相交的轮换分解式 (包含所有的 1-轮换) 为  
$$  
\sigma = (a_1 a_2 \dots a_{l_1})(b_1 b_2 \dots b_{l_2}) \dots (q_1 q_2 \dots q_{l_r})  
$$  
其中 $l_1 \geq l_2 \geq \dots \geq l_r$, 且 $l_1 + l_2 + \dots + l_r = n$。则我们把有序数组 $(l_1, l_2, \dots, l_r)$ 称为置换 $\sigma$ 的型 (type)，也称为 $n$ 的一个分拆 (partition)。证明：  
(1) $\sigma_1$ 与 $\sigma_2$ 在 $S_n$ 中共轭当且仅当 $\sigma_1$ 与 $\sigma_2$ 同型；  
(2) $S_n$ 中共轭类的个数等于 $n$ 的分拆的个数。  
求 $S_4$ 的共轭类的个数，以及每个共轭类的代表和元素数目。  
求 $A_4$ 的共轭类的个数，以及每个共轭类的代表和元素数目。  
设 $\sigma$ 是一个 $n$-轮换。求 $\sigma$ 的共轭类的元素数目，以及 $C_{S_n}(\sigma)$ 的阶。  
求 $O_2$ 的所有共轭类。  
证明：群 $G$ 的子群 $H$ 为正规子群当且仅当 $H$ 是 $G$ 的一些共轭类的并集。  
(1) 求 $S_5$ 的共轭类的个数，以及每个共轭类的代表和元素数目；  
(2) 证明：$S_5$ 只有三个正规子群，即 $\{1\}, A_5, S_5$。  
设 $G$ 为 $p$-群，$N \triangleleft G