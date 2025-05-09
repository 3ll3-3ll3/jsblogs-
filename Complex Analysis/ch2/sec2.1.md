## §1 环的类型和性质，理想

### 2. 有限整环是域。
只要证有限整环 R 的每个非零元可逆. 设 $R = \{a_1, a_2, \dots, a_n\}$. 任取 R 的一个非零元 $a$, 则 $aa_1, aa_2, \dots, aa_n$ 两两不等 (假如 $aa_j = aa_l$, 由于整环 R 没有非平凡的零因子, 因此从 $a(a_j - a_l) = 0$ 得出 $a_j - a_l = 0$, 即 $a_j = a_l$). 于是
$\{aa_1, aa_2, \dots, aa_n\} = R$.

从而必有某个 $j \in \{1, 2, \dots, n\}$, 使得 $aa_j = 1$. 因此 $a$ 可逆, 从而 R 是一个域.

### 4. 设 $R$ 是有单位元的环，则 $R$ 的每一个非平凡的理想都不能含有单位元。
$r=1\cdot r\in I \Rightarrow R \subset I$ 

### 5. 域 $F$ 没有非平凡的理想。
$1=aa^{-1}\in I,$ 由上题即可 

### 6. 设 $R$ 是一个有单位元的交换环，如果 $R$ 没有非平凡的理想，则 $R$ 是一个域。
任取 $R$ 的一个非零元 $a$, 考虑 $Ra := \{ra \mid r \in R\}$. 由于$r_1a - r_2a = (r_1 - r_2)a \in Ra$, $r(r_1a) = (rr_1)a \in Ra$, $(r_1a)r = (r_1r)a \in Ra$,
因此 $Ra$ 是 $R$ 的一个理想. 由已知条件得, $Ra = R$. 于是 $1 \in Ra$. 故 $\exists  b \in R$, 使得 $1 = ba$. 从而 $a$ 可逆, 于是, $R$ 是一个域.

### 10. 设 $D$ 是一个除环，证明 $M_n(D)$ 是单环。
任取 $M_n(D)$ 的一个理想 $J$, 且 $J \neq \{0\}$. 于是有 $A \in J$, 且 $A \neq 0$. 从而有 一个元素 $a_{kl} \neq 0$. 由于 $E_{ik}AE_{lj} = a_{kl}E_{ij}$, 因此 $a_{kl}E_{ij} \in J$. 从而 $E_{ij} = a_{kl}^{-1}(a_{kl}E_{ij}) \in J$. 于是 $E_{ij} = E_{ik}E_{kl}E_{lj} \in J, 1 \leq i, j \leq n$. 因此对于任意 $B = (b_{ij}) \in M_n(D)$, 有 $$B = \sum_{i=1}^{n} \sum_{j=1}^{n} b_{ij}E_{ij} \in J$$.  从而 $M_n(D) \subseteq J$. 又有 $J \subseteq M_n(D)$, 因此 $J = M_n(D)$. 这证明了 $M_n(D)$ 没有非平凡的理想. 于是 $M_n(D)$ 是单环.



