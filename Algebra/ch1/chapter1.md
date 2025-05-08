# 第一章 群 

## §1 群的典型例子：循环群，二面体群，矩阵群，对称群

### 7.设 $m$ 是正整数，在 $0, 1, 2, \dots, m-1$ 中，与 $m$ 互素的整数的个数记作 $\varphi(m)$，称它为 Euler (欧拉) 函数。证明：$Z_m$ 的单位群 $Z_m^*$ 的阶等于 $\varphi(m)$。

---

### 12.设 $\sigma = (i_1, i_2, \dots, i_r)$，则对于任意 $\tau \in S_n$，有$$\tau \sigma \tau^{-1} = (\tau(i_1), \tau(i_2), \dots, \tau(i_r))$$   <a id="1.1.12"></a> 


## §2 子群，陪集，Lagrange 定理，循环群的子群

### 2. 设 $H, K$ 都是群 $G$ 的子群，令 $HK \stackrel{\text{def}}{=} \{hk \mid h \in H, k \in K\}$。则 $HK$ 为子群当且仅当 $HK = KH$。

---

### 5. (1) $S_n = \langle (12), (23), \dots, (n-1 \ n) \rangle$; (2) $S_n = \langle (12), (12 \dots n) \rangle$.
(1)  $(ij)=(1i)(1j)(1i),S_n = \langle (12), (13), \dots, (1n) \rangle , $因此只要对于 $k \in \{3, 4, \dots, n\}$，去证 $(1k)$ 可以表示成 $(12), (23), \dots, (n-1, n)$ 这些对换的乘积 (它们可以重复出现)。由习题[1.1.12](#1.1.12) 得

$(13) = (23)(12)(23)$,

$(14) = (34)(13)(34) = (34)(23)(12)(23)(34)$,

$\dots$

$(1k) = (k-1, k)(1, k-1)(k-1, k)$

$= (k-1, k)(k-2, k-1) \dots (34)(23)(12)(23)(34) \dots (k-2, k-1)(k-1, k)$.

因此 $S_n = \langle (12), (23), (34), \dots, (n-1, n) \rangle$.

(2) 根据 (1) ，只要去证对于 $k \in \{2, 3, \dots, n-1\}$，有 $(k, k+1)$ 可以表示成 $(12), (123 \dots n)$ 的整数次幂的乘积。

$(23) = (123 \dots n)(12)(123 \dots n)^{-1}$,

$(34) = (123 \dots n)(23)(123 \dots n)^{-1} = (123 \dots n)^2 (12) (123 \dots n)^{-2}$,

$\dots$

$(k, k+1) = (123 \dots n)(k-1, k)(123 \dots n)^{-1}$

$= (123 \dots n)^{k-1} (12) (123 \dots n)^{-(k-1)}$.

因此 $S_n = \langle (12), (123 \dots n) \rangle$.

---

### 6. 当 $n \geq 3$ 时，(1) $A_n$ 由 3-轮换生成；(2) $A_n = \langle (123), (124), \dots, (12n) \rangle$.
(1) n元偶置换可以写为 3-轮换之积 $(1i)(1j)=(1ji)$    
(2) 只要证任一 3-轮换 $(ijk) \in \langle (123), (124), \dots, (1n) \rangle$.

$(ijk) = [(1i)(2j)](12k)[(1i)(2j)]^{-1}$

$= [(1i)(12)(2i)(2j)](12k)[(1i)(12)(2i)(2j)]^{-1}$

$= [(12i)(12j)](12k)[(12i)(12j)]^{-1}$.

因此 $A_n = \langle (123), (124), \dots, (1n) \rangle$.

---

### 9. 如果群 $G$ 的阶为偶数，则 $G$ 必有 2 阶元素。 <a id=  1.2.9 ></a>   
反证秒了

---

### 10.  证明 Euler 定理：设 $n$ 是正整数，如果整数 $a$ 与 $n$ 互素，则$$a^{\varphi(n)} \equiv 1 \pmod{n},$$ 其中 $\varphi(n)$ 是 Euler 函数。
$a\in Z_{n}^{*},$ 由Lagrange定理 $  |a| {\big | |Z_{n}^{*}|},i.e.,|a| {\big |} \varphi(n)$ 


---

### 13. 写出 $A_4$ 的所有子群，并证明 $A_4$ 没有 6 阶子群。<a id=  1.2.13 ></a>   
$A_4$ 的阶为 $\frac{4!}{2} = 12$，因此 $A_4$ 的子群的阶只可能是 1, 2, 3, 4, 6, 12.  $A_4$ 有：

* 1 个 1 阶子群：{ (1) }
* 3 个 2 阶子群：{ (1), (12)(34) }, { (1), (13)(24) }, { (1), (14)(23) }
* 4 个 3 阶子群：{ (1), (123), (132) }, { (1), (124), (142) }, { (1), (134), (143) }, { (1), (234), (243) }
* 1 个 4 阶子群：{ (1), (12)(34), (13)(24), (14)(23) }
* 1 个 12 阶子群：$A_4$    


**$A_4$ 没有 6 阶子群：** 假设 $H$ 是 $A_4$ 的 6 阶子群。 由于 $A_4$ 中不是 3-轮换的元素只有 4 个，因此 $H$ 中必有 3-轮换。 如果 $H$ 中有一个 3-轮换，那么它的逆也属于 $H$。 又由于 3-轮换的逆不等于自身，因此 $H$ 中 3-轮换的数目 $r$ 为偶数。 由于 $H$ 中有单位元 $(1)$，因此 $r = 4$ 或 $r = 2$。

**情形 1:** $r = 4$. 设 $\sigma, \sigma^{-1}, \tau, \tau^{-1}$ 是 $H$ 中的 3-轮换，则 $(1), \sigma, \sigma^{-1}, \tau, \tau^{-1}, \sigma \tau, \sigma \tau^{-1}$ 是 $H$ 中 7 个不同的元素，这与 $|H| = 6$ 矛盾。

**情形 2:** $r = 2$. 由于 $A_4$ 中含有 8 个 3-轮换，3 个 2 阶元，1 个单位元，因此 6 阶子群 $H$ 一定包含 $A_4$ 的 4 阶子群：$\{\{ (1), (12)(34), (13)(24), (14)(23) \}\}$。 从而 $A_4$ 的这个 4 阶子群也是 $H$ 的一个子群，但是 4 不是 6 的因数，这与 Lagrange 定理矛盾。

综上所述，$A_4$ 没有 6 阶子群。

---


### 14. 设 $H, K$ 是群 $G$ 的有限子群，则 $|HK| = \frac{|H| \cdot |K|}{|H \cap K|}$
记 $H \cap K = M$, 则 $M$ 是 $G$ 的子群. 又由于 $M \subseteq H$, 因此 $M$ 也是 $H$ 的子群. 设 $M$ 在 $H$ 中的左陪集分解式为 $H = \bigcup_{i=0}^{r-1} h_i M$, 其中 $h_0 = e$. 显见
$$
H K = \left( \bigcup_{i=0}^{r-1} h_i M \right) K = \bigcup_{i=0}^{r-1} (h_i M) K = \bigcup_{i=0}^{r-1} h_i (M K) = \bigcup_{i=0}^{r-1} h_i K,
$$
其中最后一步是由于 $M \subseteq K$ 且 $K$ 是子群, 因此 $M K = K$.

对于 $i, j \in \{0, 1, \dots, r-1\}$, 当 $i \neq j$ 时, 有 $h_i M \cap h_j M = \emptyset$. 假如 $h_i K \cap h_j K \neq \emptyset$, 则存在 $k_1, k_2 \in K$, 使得 $h_i k_1 = h_j k_2$. 从而 $h_j^{-1} h_i = k_2 k_1^{-1} \in H \cap K = M$. 于是 $h_i M = h_j M$, 矛盾. 因此 $h_i K \cap h_j K = \emptyset$. 从而
$$
|H K| = \sum_{i=0}^{r-1} |h_i K| = \sum_{i=0}^{r-1} |K| = r |K| = [H: M] |K|
$$ $$
|H K| = \frac{|H|}{|M|} |K| = \frac{|H| \cdot |K|}{|H \cap K|}. $$


---




## §3 群的同构，群的直积

### 1.实数加群R与正实数乘法群R*同构.
映射 $\phi: x \mapsto e^{x}$ 

---

### 8. 证明:Z₃×V≅Z₂×Z₆,其中V是 Klein 群.
由于 $V=Z_2 \times Z_2$，因此 $Z_3 \times V = Z_3 \times (Z_2 \times Z_2)$ ，说明映射 $(a, (b, c)) \mapsto ((a, b), c)$ 是 $Z_3 \times (Z_2 \times Z_2)$ 到 $(Z_3 \times Z_2) \times Z_2$ 的一个同构映射，从而 $Z_3 \times (Z_2 \times Z_2) \cong (Z_3 \times Z_2) \times Z_2$。又由于 $Z_3 \times Z_2 \cong Z_6$，从可说明 $ (Z_3 \times Z_2) \times Z_2 \cong Z_6 \times Z_2 $。最后说明 $Z_6 \times Z_2 \cong Z_2 \times Z_6$。
利用同构关系的传递性即可得所要证的结论。

---


### 10. D₁₂, D₄×Z₃, A₄×Z₂ 这三个24 阶非交换群中,有同构的吗?   
$D_{12}$ 有12阶元 $\sigma_{12}$， 有12个（反射）二阶元  

$D_{4} \times \mathbb{Z}_3 :$ 考虑同构映射 $f:D_4\rightarrow D_4\times \mathbb{Z}_3,x \mapsto (x,\bar{0})$
    
$\sigma_4$ 为 $D_4$ 的4阶元，故 $f(\sigma_4)=(\sigma_4, \bar{0})$ 是 $D_4\times \mathbb{Z}_3$ 的4阶元，同理 $(e,\bar{1})$ 为 $D_4\times \mathbb{Z}_3$ 的3阶元。又 $(3,4)=1$ 且 $(\sigma_4,\bar{0})+(e,\bar{1})=(\sigma_4,\bar{1})=(e,\bar{1})+(\sigma_4,\bar{0})$, 故 $(\sigma_4,\bar{1})$ 为 $D_4\times \mathbb{Z}_3$ 中的12阶元。但是 $D_4\times \mathbb{Z}_3$ 中2阶元 $(a,b)$ 的阶为 $\operatorname{lcm}(|a|,|b|)$, 而 $\mathbb{Z}_3$ 没有2阶元，于是这里 $D_4\times \mathbb{Z}_3$ 中2阶元 $(a,b)$ 只能为 $(a,\bar{0})$ 与 $D_4$ 中二阶元一一对应，共计4个（反射）  

$A_4\times \mathbb{Z}_2:$  由习题[1.2.13](#1.2.13), $A_6$ 没有6阶元，若 $A_4\times \mathbb{Z}_2$ 有12阶元 $(a,b)$, 则根据 $|(a,b)|=\operatorname{lcm}(|a|,|b|),|a|=12$, 于是 $a^{2}$ 为 $A_4$ 中6阶元，矛盾！于是 $A_4\times \mathbb{Z}_2$ 没有12阶元

综上，他们三个两两不同构 


---


### 11. $D_{2n} \cong D_n \times \mathbb{Z}_2 \quad \text{when } n \text{ is odd.}$ 

The dihedral group $D_n$ is presented as:
$$ D_n = \langle \sigma, \tau \mid \sigma^n = \tau^2 = I, \tau \sigma \tau = \sigma^{-1} \rangle = \{ \sigma^j, \sigma^j \tau \mid 0 \leq j \leq n-1 \} $$

Similarly, $D_{2n}$ is presented as:
$$ D_{2n} = \langle \gamma, \delta \mid \gamma^{2n} = \delta^2 = I, \delta \gamma \delta = \gamma^{-1} \rangle $$

Consider the elements $(\sigma, \bar{1})$ and $(\tau, \bar{1})$ in $D_n \times \mathbb{Z}_2$:

1. **Order**:
   - $|(\sigma, \bar{1})| = \operatorname{lcm}(|\sigma|, |\bar{1}|) = \operatorname{lcm}(n, 2) = 2n$ (since $n$ is odd).
   - $|(\tau, \bar{1})| = \operatorname{lcm}(2, 2) = 2$.

2. **Conjugation**:
   - $(\tau, \bar{1})(\sigma, \bar{1})(\tau, \bar{1}) = (\tau \sigma \tau, \bar{1}) = (\sigma^{-1}, \bar{1})$.
   - Moreover, $(\sigma^{-1}, \bar{1})(\sigma, \bar{1}) = (e, \bar{0})$ and $(\sigma, \bar{1})(\sigma^{-1}, \bar{1}) = (e, \bar{0})$.
   - Thus, $(\tau, \bar{1})(\sigma, \bar{1})(\tau, \bar{1}) = (\sigma, \bar{1})^{-1}$, and by induction:
     $$
     (\tau, \bar{1})(\sigma, \bar{1})^i (\tau, \bar{1}) = (\sigma, \bar{1})^{-i}, \quad i \in \mathbb{Z}.
     $$

3. **Generating All Elements**:
   Any element $c = (\sigma^i \tau^j, \bar{k}) \in D_n \times \mathbb{Z}_2$ (where \$0 \leq i \leq n-1$, \$0 \leq j, k \leq 1$) can be expressed as:
   - If $\overline{i + j - k} = \bar{0}$, then $c = (\sigma, \bar{1})^i (\tau, \bar{1})^j$.
   - Otherwise, $c = (\sigma, \bar{1})^i (\tau, \bar{1})^j (I, \bar{1}) = (\sigma, \bar{1})^i (\tau, \bar{1})^j (\sigma, \bar{1})^n$  (since $n$ is odd).

   This shows that $D_n \times \mathbb{Z}_2$ is generated by $(\sigma, \bar{1})$ and $(\tau, \bar{1})$, with the relations:
   $$
   D_n \times \mathbb{Z}_2 = \langle (\sigma, \bar{1}), (\tau, \bar{1}) \mid (\sigma, \bar{1})^{2n} = (\tau, \bar{1})^2 = I, (\tau, \bar{1})(\sigma, \bar{1})(\tau, \bar{1}) = (\sigma, \bar{1})^{-1} \rangle.
   $$

Then it's easy to see that $D_{2n} \cong D_n \times \mathbb{Z}_2$ 

---


### 12. $O_n \cong SO_{n} \times \{ I,-I \}\quad$ when $ n $ is odd
$SO_{n}\cap \{ I,-I \}=I$, since $n$ is odd.

It's easy to see that the elements of $ SO_n $ commute with the elements of $ \{ I, -I \} $ and $O_n = SO_{n} \times \{ I,-I \}$ .

Then we can obtain that $O_n \cong SO_{n} \times \{ I,-I \}$

---
## §4 群的同态，正规子群，商群，可解群
### 3.  设 $F$ 是一个域, $\sigma$ 是 $GL_n(F)$ 到 $F^{*} $ 的一个映射: $\sigma(A) = |A|, \forall A \in GL_n(F)$. 则 $GL_n(F) / SL_n(F) \cong F^{*}$. <a id=  1.4.3 ></a>   
群同态基本定理

---

### 10. $D_n'=\langle \sigma^{2}   \rangle   $ (where $ D_n = \langle \sigma, \tau \mid \sigma^n = \tau^2 = I, \tau \sigma \tau = \sigma^{-1} \rangle $)

 Since $\sigma^{i} \sigma \sigma^{-i} = \sigma^2$, $\tau \sigma \tau^{-1} = (\tau \sigma \tau^{-1})^2 = (\sigma^{-1})^2 \in \langle \sigma^2 \rangle$, thus $\langle \sigma^2 \rangle \triangleleft D_n$.

$|\sigma^2| = \frac{|\sigma|}{(|\sigma|, 2)} = \frac{n}{(n, 2)}$.  Therefore, $|D_n / \langle \sigma^2 \rangle| = \frac{2n}{(n, 2)} / \frac{n}{(n, 2)} = 2(n, 2)\in \{ 2,4 \}$. It is well known that second-order and fourth-order groups are both Abelian. Hence, $D_n / \langle \sigma^2 \rangle$ is an Abelian group.  Thus, $D_n' \subseteq \langle \sigma^2 \rangle$.  Since $\sigma^2 = \sigma \tau \sigma^{-1} \tau^{-1} \in D_n'$, thus $\langle \sigma^2 \rangle \subseteq D_n'$.  Therefore, $D_n' = \langle \sigma^2 \rangle$.    (When $n$ is odd, $|\sigma^2| = n = |\sigma|$, thus $D_n' = \langle \sigma^2 \rangle = \langle \sigma \rangle$.)

---

### 12.  $S_n'=A_n$, $n \geq 3$。
Since $[S_n : A_n] = 2$, thus $A_n \triangleleft S_n$, and $S_n / A_n$ is an Abelian group.  Therefore, $S_n' \subseteq A_n$.

$A_n$ can be generated by 3-cycles, and for every 3-cycle $(ijk)$, and we have

$(ijk) = (ijk)^{-2} = (ikj)^2 = [(ij)(ik)]^2 = (ij)(ik)(ij)^{-1}(ik)^{-1} \in S_n'$, Therefore, $A_n \subseteq S_n'$. 

Hence, $S_n' = A_n$.

---

### 13.  $A_n' = A_n$, $n \geq 5$ 
When $ n \geq 5 $, for any 3-cycle swap $(a_1, a_2, a_3)$ in $A_n$, define $\sigma = (a_1 a_3 a_4 a_2 a_5) \in A_n$, $\tau = (a_1 a_5 a_2) \in A_n$, then

$$ \sigma \tau \sigma^{-1} \tau^{-1} = (a_3 a_1 a_5)(a_1 a_2 a_3) = (a_1 a_2 a_3). $$

Thus, $(a_1 a_2 a_3) \in A_{n}'$. Since $A_n$ can be generated by 3-cycles, $A_n \subseteq A_n'$. Therefore, $A_n' = A_n$.
**Notes:** When $ n \geq 5 $, $S_n' = A_n$, $A_n' = A_n$. Then $S_n$ is non-solvable, $n\ge 5$ .


---

### 14. 写出 $S_4$ 的导群列，由此看出，$S_4$ 是可解群。
Because $ S_4' = A_4 $, $ A_4' = V $, and $ V' = \{ (1) \} $, it follows that $ S_4^{(3)} = \{ (1) \} $. Hence, $ S_4 $ is solvable.

---

### 17. $A_n $ is simple group, $n\ge 5$
$A_n$ can be generated by 3-cycles. That is, for any $a, b \in \{1, 2, ..., n\}$ where $a \neq b$, take a 3-cycle $(ijk)$. Then $(ijk) = (ik)(jk)$.

$(ij)(ka) = (ai)(aj)(bj)(ka)(ai)(aj)(bj)^{-1}$
$= (ai)(aj)(ab)(bj)(ka)(bj)^{-1}(ab)^{-1}(aj)^{-1}(ai)^{-1}$
$= (abi)(bja)(abk)(bja)^{-1} = (abi)(abj)(abk)(abi)(abj)^{-1}$;
$(ajk) = (jka) = (ajb)(akb)(ajb)^{-1} = (abj)^{-1}(abk)^{-1}(abj)$;
$(bjk) = (kbj) = (abk)(abj)(abk)^{-1}$.

Therefore, for any $a, b \in \{1, 2, ..., n\}$, $a \neq b$, $A_n$ is generated by the set $M = \{(abl) | 1 \le l \le n, l \neq a, l \neq b\}$, i.e., $A_n = \langle M \rangle$.

Take any normal subgroup $N \neq \{ (1) \}$ of $A_n$, we want to prove $N = A_n$.

**Case 1:** Suppose $N$ contains a 3-cycle $(abc)$, then for any $k \in \{1, 2, ..., n\}$ and $k \neq a, b, c$, we have
$(abk) = (cbk)(acb)(cbk)^{-1} \in N$.

Since $M \subseteq N$, then $\langle M \rangle \subseteq N$. But $A_n \subseteq N$. Therefore, $N = A_n$.

**Case 2:** Suppose $N$ contains a permutation $\sigma$, and the decomposition of $\sigma$ into transpositions has at least one $r$-cycle, where $r \ge 4$, i.e., $\sigma = (a_1 a_2 \dots a_r) \dots$. Take $\tau = (a_1 a_2 a_3) \in A_n$, then $\sigma_1 = \tau \sigma \tau^{-1} \in N$. And $\sigma^{-1} (\tau \sigma \tau^{-1}) = \sigma^{-1} \sigma_1 = \sigma^{-1} [(a_1 a_2 \dots a_r) \dots] (a_1 a_2 a_3) [(a_1 a_2 \dots a_r) \dots]^{-1} (a_1 a_2 a_3)^{-1}$
$= \sigma_1^{-1} (a_1 a_2 a_3) \sigma_1 (a_1 a_2 a_3)^{-1} = \sigma_1^{-1} \sigma_1 (a_1 a_2 a_3) (a_1 a_2 a_3)^{-1} = (a_1 a_3 a_r) \in N$. By Case 1, $N = A_n$.

**Case 3:** Suppose $N$ contains a permutation $\sigma$, and the decomposition of $\sigma$ into transpositions has at least two 3-cycles, i.e., $\sigma = (a_1 a_2 a_3)(a_4 a_5 a_6) \dots$. Take $\tau = (a_2 a_3 a_4) \in A_n$, then $\sigma_1 = \tau \sigma \tau^{-1} \in N$.
$\sigma^{-1} (\tau \sigma \tau^{-1}) = \sigma^{-1} \sigma_1 = \sigma^{-1} [(a_1 a_2 a_3)(a_4 a_5 a_6) \dots] (a_2 a_3 a_4) [(a_1 a_2 a_3)(a_4 a_5 a_6) \dots]^{-1} (a_2 a_3 a_4)^{-1}$
$= \sigma_1^{-1} \sigma_1 [(a_1 a_2 a_3)^{-1} (a_1 a_3 a_4) (a_4 a_5 a_6) ] (a_1 a_2 a_4)^{-1}$
$= (a_3 a_1 a_4)(a_1 a_2 a_4 a_6)$,

$(a_1 a_4 a_4 a_2 a_3) \in N$. By Case 2, $N = A_n$.

**Case 4:** Suppose $N$ contains a permutation $\sigma$, and the decomposition of $\sigma$ into transpositions is $\sigma = (a_1 a_2)(a_3 a_1) \sigma_1$, where $\sigma_1$ is a product of some disjoint transpositions. From $\sigma^2 = (a_1 a_3 a_2)$. From $(a_1 a_3 a_2) \in N$. By Case 1, $N = A_n$.

**Case 5:** Suppose $N$ contains a permutation $\sigma$ which is an even number of disjoint transpositions, i.e., $\sigma = (a_1 a_2)(a_3 a_4) \sigma_1$, where $\sigma_1$ is an even number of disjoint transpositions. Take $\tau = (a_1 a_2 a_3) \in A_n$, then $\sigma^{-1} (\tau \sigma \tau^{-1}) \in N$.

$\sigma^{-1} (\tau \sigma \tau^{-1}) = \sigma_1^{-1} \sigma_1 [(a_1 a_2)(a_3 a_4)] (a_1 a_2 a_3) [(a_1 a_2)(a_3 a_4)] \sigma_1 (a_1 a_2 a_3)^{-1}$
$= \sigma_1^{-1} \sigma_1 (a_3 a_4)(a_1 a_2 a_3)(a_1 a_2)(a_3 a_4)^{-1}$
$= (a_1 a_3 a_4 a_2) = (a_2 a_4)$,

Because $\gamma = (a_1 a_3)(a_2 a_4) \in N$. For $n \ge 5$, there exists $b \in \{1, 2, ..., n\}$, and $b \neq a_1, a_2, a_3$, take $\delta = (a_3 a_1 b)$, then $\gamma^{-1} (\delta \gamma \delta^{-1}) \in N$.

$\gamma^{-1} (\delta \gamma \delta^{-1}) = (\gamma^{-1} \delta \gamma) \delta^{-1} = (a_3 a_1 b)(a_1 ba_3) = (a_1 a_3 b)$.

Therefore, $(a_1 a_3 b) \in N$. By Case 1, $N = A_n$.

In summary, $N = A_n$. Therefore, $A_n$ is simple.

---

### 15. 如果置换群 $G$ 含有奇置换，则 $G$ 必有指数为 2 的子群。<a id=  1.4.15 ></a>   
Let $\psi$ be a mapping from $G$ to the group of 2nd roots of unity $U_2$. $\psi$ maps even permutations to $1$ and odd permutations to $-1$, then $\psi$ is surjective. Since the product of two even permutations is an even permutation, the product of two odd permutations is an even permutation, the product of an even permutation and an odd permutation is an odd permutation, and the product of an odd permutation and an even permutation is an odd permutation, therefore $\psi$ preserves the operation. Thus $\psi$ is a surjective homomorphism from $G$ to $U_2$. Therefore $G/\text{Ker}\psi \cong U_2$. Hence $G$ has a subgroup of index 2, namely $\text{Ker}\psi$. From the definition of $\psi$, we know that $\text{Ker}\psi$ is the subgroup of $G$ consisting of all even permutations.


---





### 16. 设 $\sigma$ 是群 $G$ 到群 $G'$ 的一个满同态，记 $K = \text{Ker } \sigma$。设 $H' \triangleleft G'$，令 $\sigma^{-1}(H') \stackrel{\text{def}}{=} \{g \in G \mid \sigma(g) \in H'\}$。证明：(1) $\sigma^{-1}(H') \triangleleft G$, 且 $\sigma^{-1}(H') \supseteq K$;    (2) $H' \mapsto \sigma^{-1}(H')$ 是 $G'$ 的子群集合到 $G$ 的包含 $K$ 的子群集合的一个双射。

---


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
