# 第零章 杂题和小结论

## 0.0 其他

### 0.0.1 定义-命题 (半直积)
设 $H$ 和 $N$ 为群，$\varphi : H \rightarrow \text{Aut}(N)$ 为群同态；记 $h \in H$ 对 $\varphi$ 的像为 $\varphi_h : N \rightarrow N$。在积集 $N \times H$ 上定义二元运算

$$
(n, h)(n', h') := (n \varphi_h(n'), hh').
$$

这给出群结构，称为 $H$ 和 $N$ 相对于 $\varphi$ 的半直积，记为 $N \rtimes_{\varphi} H$。它满足

$$
1_{N \rtimes H} = (1_N, 1_H), \quad (n, h)^{-1} = (\varphi_{h^{-1}}(n^{-1}), h^{-1}).$$

群 $N$ 和 $H$ 分别通过 $n \mapsto (n, 1_H)$ 和 $h \mapsto (1_N, h)$ 嵌入为 $N \rtimes H$ 的子群。进一步，$N \triangleleft N \rtimes_{\varphi} H$；事实上，

$$
(1_N, h)(n, 1_H)(1_N, h)^{-1} = (\varphi_h(n), 1_H).
$$

**先说明定义的动机：** 我们的思路是将 $H$ 和 $N$ 嵌入一个更大的群 $G$，使得 $N \triangleleft G$ 而且 $G$ 的所有元素都能唯一地表为 $nh$，其中 $n \in N$ 而 $h \in H$。熟悉的写法

$$
nh \cdot n'h' = n \underbrace{hn'h^{-1}}_{\in N} hh'
$$

表明只要能对所有 $h$ 和 $n'$ 描述 $Ad_h(n') = hn'h^{-1}$，则 $G$ 的乘法便唯一从 $N$ 和 $H$ 的乘法确定。定义中的 $\varphi_h$ 正是此处的 $Ad_h \in \text{Aut}(N)$。关于公元和逆元的描述也都可以按此理解。

严格论证将反其道而行，从 $N, H$ 和 $\varphi$ 构造这般的群 $G$，而自然的思路是在积集 $N \times H$ 上建群。

---

**严格证明**
首先是乘法结合律：

$((n,h)(n',h'))(n'',h'') = (n\varphi_h(n'),hh')(n''',h'') = (n\varphi_h(n')\varphi_{hh'}(n'')),hh'h''),$

$(n,h)((n',h')(n''',h'')) = (n,h)(n'\varphi_{h'}(n'')),h'h'') = (n\varphi_h(n'\varphi_{h'}(n'')),hh'h'').$

问题化为证 $\varphi_h(n')\varphi_{hh'}(n'') = \varphi_h(n'\varphi_{h'}(n''))$；因为 $\varphi_h$ 是同态，目标进一步化为 $\varphi_{hh'} = \varphi_h\varphi_{h'}$，然而 $\varphi: H \rightarrow \text{Aut}(N)$ 也是同态，故结合律得证。

公元 $(1_N,1_H)$ 的性质容易归结为 $\varphi_{1_H} = \text{id}_N$ 和 $\varphi_h(1_N) = 1_N$。至于逆元的性质，我们有

$$\begin{align*}
(n,h)(\varphi_{h^{-1}}(n^{-1}),h^{-1}) &= (n\varphi_h(\varphi_{h^{-1}}(n^{-1})),hh^{-1}) \\
&= (nn^{-1},hh^{-1}) = (1_N,1_H),\\
(\varphi_{h^{-1}}(n^{-1}),h^{-1})(n,h) &= (\varphi_{h^{-1}}(n^{-1})\varphi_{h^{-1}}(n),h^{-1}h) \\
&= (\varphi_{h^{-1}}(n^{-1}n),h^{-1}h) = (1_N,1_H).            
\end{align*}$$

最后，嵌入 $H \hookrightarrow   N \rtimes_\varphi H$ 和 $N \hookrightarrow   N \rtimes_\varphi H$ 的同态性质是毫无困难的。按此计算

$(1_N,h)(n,1_H)(1_N,h)^{-1} = (\varphi_h(n),h)(1_N,h^{-1}) = (\varphi_h(n),1_H);$
此处用到了 $\varphi_h(1_N) = 1_N$。

---

**注：**
如果取 $\varphi : H \rightarrow \text{Aut}(N)$ 为平凡同态，亦即 $\forall h, \varphi_h = \text{id}_N$，则 $N \rtimes H$ 便化为直积 $N \times H$。

留意到若将 $N$ 和 $H$ 等同于 $N \rtimes_\varphi H$ 的子群，则它们的交为平凡子群，而且 $N \rtimes_\varphi H = NH$；这蕴涵 $ N \rtimes_\varphi H$ 都能唯一地写成 $nh$ 的形式。

**example:** 验证 $(n,h) \mapsto h$ 给出满同态 $N \rtimes_\varphi H  \rightarrow H$，而且它诱导同构 $( N \rtimes_\varphi H )/N \cong H$。



---

### 0.0.2 定义-命题 11.10.3 (半直积的内在版本)
设 $H$ 和 $N$ 为群 $G$ 的子群，满足下述条件

$$
N \triangleleft G, \quad G = NH, \quad N \cap H = \{1\}.
$$

考虑由 $\operatorname{Ad}_h(n) = hnh^{-1}$ 给出的同态 $\operatorname{Ad}: H \rightarrow \text{Aut}(N)$，则有群同构

$$
\Phi : N \rtimes_{\operatorname{Ad}} H \xrightarrow{\sim} G\\
(n,h) \longmapsto nh.
$$

此时也称 $G$ 是子群 $H$ 和正规子群 $N$ 的半直积，合理地记为 $G = N \rtimes H$。

**证明** 验证 $\Phi$ 是群同态：$(n,h)(n',h') = (n \operatorname{Ad}_h(n'),hh')$ 被映为 $n \operatorname{Ad}_h(n')hh'$，然而后者即 $nhn'h^{-1}hh' = (nh)(n'h')$。

条件 $G = NH$ 相当于说 $\Phi$ 满。最后证明 $\Phi$ 单：若 $\Phi(n,h) = 1$，则 $n = h^{-1} \in N \cap H = \{1\}$。因此 $\Phi$ 是同构。

**example:** $ S_n $ 是 $A_n$ 与 $\langle (12)   \rangle     $  的半直积

---

## 0.1 群
### 0.1.1 令 $S$ 是整数加群 $\mathbb{Z}^+$ 的子群，则 $S$ 或为平凡子群 $\{0\}$，或是有形式 $Z_a$，其中 $a$ 为 $S$ 中最小正整数。

证明：令 $S$ 是 $\mathbb{Z}$ 的一个子群，则 $0 \in S$。如果 $0$ 是 $S$ 中唯一的元素，则 $S$ 为平凡子群。因而对这一情形结论成立。否则，$S$ 包含异于 $0$ 的整数 $n$，且要么 $n$ 是正数，要么 $-n$ 是正数。由子群的第三个性质知：$-n \in S$。故 $S$ 含有正整数。我们必须证明 $S = Za$，其中 $a$ 为 $S$ 中最小正整数。

首先证明 $Z_a$ 是 $S$ 的子集，换句话说，$ka \in S$ 对于任意整数 $k$ 成立。如果 $k$ 是正整数，则 $ka = a + a + \dots + a$ ($k$ 项)。由于 $a \in S$，由子群的封闭性和归纳法知 $ka \in S$。子群中元素的逆元仍属于 $S$，因此 $-ka \in S$。最后，$0a = 0 \in S$。

其次，证明 $S$ 是 $Za$ 的子集，即 $S$ 中任意元素 $n$ 是 $a$ 的整数倍。用带余除法，记 $n = qa + r$，其中 $q, r$ 都是整数且余数 $r$ 的取值范围为 $0 \le r < a$。由于 $Za \subseteq S$，故 $qa \in S$，当然 $n \in S$。因为 $S$ 是子群，故也有 $r = n - qa \in S$。现在，根据我们的选取，$a$ 为 $S$ 中最小正整数，而余数 $r$ 满足 $0 \le r < a$。因此，属于 $S$ 的唯一余数是 $0$。所以，$r = 0$ 且 $n$ 是 $a$ 的整数倍数 $qa$。

---

### 0.1.2 Any group can be expressed as a union of cyclic subgroups.  <a id=  0.2 ></a>   

This follows directly from set inclusion: every element $ g \in G $ belongs to the cyclic subgroup $ \langle g \rangle $, so $ G = \bigcup_{g \in G} \langle g \rangle $.  

---

### 0.1.3 A group $G$ has only finitely many subgroups $\Leftrightarrow$ $G$ is finite.

Assume $G$ has finitely many subgroups。We only need to prove: an infinite group $G$ must have infinitely many subgroups。  

First, suppose $G$ is not cyclic。By [the previous problem](#0.2), $G = \bigcup_{g \in G}\langle g\rangle$, and there must exist some $\langle g_0\rangle$ that is an infinite cyclic group。Thus, without loss of generality, we may assume $G$ is the cyclic group $\langle g_0\rangle$, which has infinitely many subgroups: $\langle g_0\rangle, \langle g_0^{2}\rangle, \langle g_0^{3}\rangle, \ldots$  

Next, if $G$ is finite, the conclusion is obvious by [the previous problem](#0.2)。   <div style="text-align: right;font-size: 20px;">▢</div>

---

### 0.1.4 There does not exist a group with exactly two elements of order 2

Suppose, for contradiction, that $G$ is a group with exactly two distinct elements of order 2, say $a$ and $b$.

**Case 1:** $ab = ba$。
Then $ab$ is distinct from $a$, $b$, and $e$, and $(ab)^2 = a^2b^2 = e$, so $ab$ has order 2。This contradicts the assumption that $G$ has only two elements of order 2。

**Case 2:** $ab \ne ba$。
Consider $aba$。Since $a \ne b$, $aba$ is distinct from $a$, $b$, and $e$。Moreover, $(aba)^2 = ab(a^2)ba = abba = e$, so $aba$ has order 2, again yielding a contradiction。

Thus, no such group $G$ can exist。         <div style="text-align: right;font-size: 20px;">▢</div>


---


### 0.1.5 Abel单群一定为素数阶循环群
**熟知Abel群的子群一定为正规子群**。又因 $G$ 是单群，其正规子群仅有 $\{e\}$ 和 $G$ 本身。于是任取非单位元 $g \in G,\ g \neq e$，构造子群 $\langle g \rangle$，由于 $\langle g \rangle \neq \{e\}$，故 $\langle g \rangle = G$。  
**断言 $|G|=n$ 为素数**  若不然，存在 $a, b > 1$ 使得 $n = ab$，循环群 $G$ 必存在一个 $a$ 阶子群（例如由 $g^b$ 生成的子群 $\langle g^b \rangle$），这与 $G$ 无非平凡子群矛盾。   <div style="text-align: right;font-size: 20px;">▢</div>

---

### 0.1.6 

---







### 0.1.7 (1) $| GL_n(F_{p})| = \prod_{k=0}^{n-1} (p^n - p^k) , | SL_n(\mathbb{F}_p) |=\frac{| GL_n(\mathbb{F}_p) |}{p-1} $ ; (2) 求 $GL_n(F_{p})$ 的 sylow-p子群，并确定sylow—p子群的个数 
(1) 对于前者：一个 $ n \times n $ 可逆矩阵的 $ n $ 个列向量必须线性无关。      第 1 列：可以是 $ \mathbb{F}_p^n $ 中任意非零向量，共 $ p^n - 1 $ 种选择。      第 2 列：不能与第 1 列共线（即不在其张成的 1 维子空间中），共 $ p^n - p $ 种选择。      第 3 列：不能在前两列张成的 2 维子空间中，共 $ p^n - p^2 $ 种选择。        依此类推，直到第 $ n $ 列。   
后者可由[习题1.4.3](#1.4.3)   
(2) 
 <div style="text-align: right;font-size: 20px;">▢</div> 
 
---

 ### 0.1.8 群 $ G $ 的类方程是 $ 1 + 4 + 5 + 5 + 5 $  
 #### (1) $ G $ 有 5 阶子群吗？如果有，它是正规子群吗？ 
 证明：设共轭类依次为 $G(x_1), G(x_2), G(x_3), G(x_4), G(x_5)$，阶数依次为 $1, 4, 5, 5, 5$。由轨道稳定子定理知 $C_G(x_2)$ 阶数为 $|G|/|G(x_2)|$。于是 $C_G(x_2)$ 为 $G$ 的 一个 5 阶子群。断言 $G$ 只有这一个5阶子群。若不然：   设 $<r>$,$<s>$ 为 $G$ 的两个不同五阶子群，则 $<r>\cap <s> = {e}$(否则他们相同)。于是有 $r^is^j=r^ms^n \Leftrightarrow r^{i-m}=s^{n-j} \equiv e \Leftrightarrow m=n,i=j$(这里规定 $0\le i,j, m,n\le 5$ )于是有 $|G|\ge |\{r^is^j|0\le i,j\le 5\}|=25$ ,矛盾！   
### (2) $ G $ 有 4 阶子群吗？如果有，它是正规子群吗？ 
不用Sylow很目前觉得困难

---
 
### 0.1.9 Showing that a p-group has a normal subgroup for each divisor of its order
proof: We will use induction on $n$, where $|P|=p^n$.  Clearly the result is true if $|P|=p^1$.  Now assume the statement is true for all groups of order $p^k$ where $k<n$.

Since $P$ is a $p$-group it has nontrivial center, and $Z(P)$ is also a $p$-group.  It follows that $P$ has a normal subgroup of order $p$, say $N$.  Form the quotient group $P/N$, which has order $p^{n-1}$, and therefore has a normal subgroup of order $q$ for each divisor $q$ of $p^{n-1}$ by the induction hypothesis.

We can show that $P$ has a normal subgroup of index $p^{i} ,1\le i\le n$ .  Clearly this is true for $i=1,n$, and $|P:N|=p^{n-1}$.  Consider the canonical homomorphism $\pi:P \to P/N$, which is surjective.  Then by the **Correspondence Theorem**, $\pi$ and $\pi^{-1}$ are inverse bijections between subgroups of $P/N$ and subgroups of $P$ containing $N$, that respect normality and index。  Then since $P/N$ (by the induction hypothesis) has a normal subgroup of index $p \le i \le p^{n-2}$, so does $P$, and the result follows.

---

### 0.1.10 $n$ 为素数时，$S_n$ 中n阶元一定是n-轮换。当n为一般整数时不一定成立
**hint:** 任意置换 $ \sigma \in S_n $ 可以唯一分解为不相交轮换的乘积：$\sigma = \gamma_1 \gamma_2 \dots \gamma_k,$ 其中 $\gamma_i $  是长度为 $ \ell_i $ 的轮换，且 $ \ell_1 + \ell_2 + \dots + \ell_k \leq n $。置换的阶为：$\text{ord}(\sigma) = \text{lcm}(\ell_1, \ell_2, \dots, \ell_k).$



 ---


## 0.2 环
### 0.2.1 $n$ 阶实方阵全体对于通常的矩阵加法和乘法形成含幺环, 叫做 $n$ 阶实方阵环, 表示成 $M_n(R)$. 零元素为 $n$ 阶零方阵, 幺元素为 $n$ 阶单位方阵 $I_n$. 类似可定义有理矩阵环 $M_n(Q)$, 复矩阵环 $M_n(C)$ 等. 当 $n \ge 2$ 时, 易知它们均不是交换环. <br> 更一般地, 对于任意环 $R$, 我们仍旧像通常那样定义元素属于 $R$ 的两个 $n$ 阶方阵的加法和乘法, 可以直接验证全体这种 $n$ 阶方阵形成环, 叫做环 $R$ 上的 $n$ 阶方阵环, 表示成 $M_n(R)$. 如果环 $R$ 有幺元素 $1_R$, 则环 $M_n(R)$ 也有幺元素 $I_n = \begin{pmatrix} 1_R & & \\ & \ddots & \\ & & 1_R \end{pmatrix}$. 进而, 如果 $R$ 是交换环, 我们可以定义方阵 $A = (a_{ij}) \in M_n(R)$ 的行列式 $\det A = \sum_{\sigma \in S_n} \text{sgn}(\sigma) a_{1\sigma(1)} \cdots a_{n\sigma(n)}$. 基于环 $R$ 的乘法交换性, 我们可以看出 $\det A$ 仍具有行列式通常那些性质, 例如:$$\begin{align*}(1)& (\det A)(\det B) = \det(AB);          \\(2)& A(\text{adj} A) = (\text{adj} A)A = (\det A) \cdot I_n.          \end{align*} $$ 其中 $\text{adj} A$ 表示 $A$ 的伴随方阵, 即 $\text{adj} A = (A_{ji})$, 而 $A_{ij}$ 是 $A$ 中元素 $a_{ij}$ 的代数余子式. 上面 (1) 式表明, 当 $R$ 为含幺交换环时, 行列式映射 $$\det: M_n(R) \to R, \quad A \mapsto \det A$$ 是乘法半群的同态 (并且易知这是满同态). 因此若 $A$ 是环 $M_n(R)$ 中的单位, 则 $\det A$ 也是环 $R$ 中的单位 . 反之, 如果 $\det A \in U(R)$, 则由上面的 (2) 式可知 $(\det A)^{-1} \text{adj} A$ 是 $A$ 的逆元素, 即 $A \in U(M_n(R))$. 这就完全决定了矩阵环 $M_n(R)$ 的单位群 (其中 $R$ 为含幺交换环): $$U(M_n(R)) = \{A \in M_n(R) \mid \det A \in U(R)\}$$. 乘法群 $U(M_n(R))$ 叫做含幺交换环 $R$ 上的 $n$ 次一般线性群, 表示成 $GL(n, R)$. 例如 $GL(n, \mathbb{Z}) = \{A \in M_n(\mathbb{Z}) \mid \det A = \pm 1\}$, 而对任意域 $F$, $GL(n, F) = \{A \in M_n(F) \mid \det A \neq 0\}$. <br> 注：这里 $U(R)$ 表示环 $R$ 的乘法逆元的集合（单位群） 

---


## 域

