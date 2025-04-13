# 作业5
梁彭博别学了，
梁彭博别学了，



梁彭博别学了，梁彭博别学了，
梁彭博别学了，
梁彭博别学了，
梁彭博别学了，
梁彭博别学了，
梁彭博别学了，

梁彭博别学了，梁彭博别学了，


梁彭博别学了，
梁彭博别学了，
梁彭博别学了，
梁彭博别学了，
梁彭博别学了，
梁彭博别学了，

<link rel="stylesheet" type="text/css" href="http://zlyd.iccnconn.com/markdowncss/stylelib/typora-purple-theme-1.5.7/purple.css">

# CH1 杂题&小结论
## 1.1 \(| GL_n(\mathbb{F}_p) |\)=  \(\prod_{k=0}^{n-1} (p^n - p^k)\)
证明：一个 \( n \times n \) 可逆矩阵的 \( n \) 个列向量必须线性无关。  
   第 1 列：可以是 \( \mathbb{F}_p^n \) 中任意非零向量，共 \( p^n - 1 \) 种选择。  
   第 2 列：不能与第 1 列共线（即不在其张成的 1 维子空间中），共 \( p^n - p \) 种选择。  
   第 3 列：不能在前两列张成的 2 维子空间中，共 \( p^n - p^2 \) 种选择。    
   依此类推，直到第 \( n \) 列。  
 <div style="text-align: right;font-size: 20px;">▢</div>


 

## 1.2 群 \( G \) 的类方程是 \( 1 + 4 + 5 + 5 + 5 \) 
### (1) \( G \) 有 5 阶子群吗？如果有，它是正规子群吗？
设共轭类依次为 $G(x_1), G(x_2), G(x_3), G(x_4), G(x_5)$，阶数依次为 $1, 4, 5, 5, 5$。由轨道稳定子定理知 $C_G(x_2)$ 阶数为 $|G|/|G(x_2)|$。于是 $C_G(x_2)$ 为 $G$ 的 一个 5 阶子群。断言 $G$ 只有这一个5阶子群。若不然：  
设 $<r>$,$<s>$ 为 $G$ 的两个不同五阶子群，则 $<r>\cap <s> = {e}$(否则他们相同)。于是有 $r^is^j=r^ms^n \Leftrightarrow r^{i-m}=s^{n-j} \equiv e \Leftrightarrow m=n,i=j$(这里规定 $0\le i,j, m,n\le 5$ )于是有 $|G|\ge |\{r^is^j|0\le i,j\le 5\}|=25$ ,矛盾！
### (2) \( G \) 有 4 阶子群吗？如果有，它是正规子群吗？
同上 $C_{G}(x_i),i=3,4,5$ 即为所求。断言他们三都不是正规子群。若不然：  
不妨设 $C_G(x_3) \triangleleft G,$ 则 $ \forall g\in G,gC_G(x_3) g^{-1} =C_G(x_3)$。$\forall a\in C_G(x_3) ,ax_3=x_3a, gag^{-1}x_3=x_3gag^{-1},ag^{-1}x_3g= g^{-1}x_3ga ,i.e.  a\in C_G(g^{-1}x_3g)$,于是 $C_G(x_3) \subseteq C_G(g^{-1}x_3g)$。同理 $C_G(g^{-1}x_3g) \subseteq C_G(x_3) $。于是 $C_G(g^{-1}x_3g) = C_G(x_3) $    
由于 $\phi :G\rightarrow G, a \mapsto gag^{-1}$ 为双射，故 $\exists g_0\in G,s.t.x_i=a_i x_3a_i^{-1},i \ne 3$。 于是 $C_G(x_3)=C_G(x_i), i\ne 3 $, 这不可能！






## 1.2 The Class Equation of Group $ G $ is $ 1 + 4 + 5 + 5 + 5 $

### (1) Does $ G $ have a subgroup of order 5? If so, is it a normal subgroup?

Let the conjugacy classes be denoted as $ G(x_1), G(x_2), G(x_3), G(x_4), G(x_5) $, with orders $ 1, 4, 5, 5, 5 $, respectively. By the Orbit-Stabilizer Theorem, the order of the centralizer $ C_G(x_2) $ is $ |G| / |G(x_2)|=5$. Thus, $ C_G(x_2) $ is a subgroup of $ G $ of order 5. We claim that $ G $ has only one subgroup of order 5.  

Suppose not:  
Let $ \langle r \rangle $ and $ \langle s \rangle $ be two distinct subgroups of $ G $ of order 5. Then $ \langle r \rangle \cap \langle s \rangle = \{ e \} $ (otherwise, they would be the same). This implies that $ r^i s^j = r^m s^n \Leftrightarrow r^{i-m} = s^{n-j} \equiv e \Leftrightarrow m = n, i = j $ (where $ 0 \leq i, j, m, n \leq 5 $). Therefore, $ |G| \geq |\{ r^i s^j \mid 0 \leq i, j \leq 5 \}| = 25 $, which is a contradiction!

### (2) Does $ G $ have a subgroup of order 4? If so, is it a normal subgroup?

Similarly, $ C_G(x_i) $ for $ i = 3, 4, 5 $ are the desired subgroups. We claim that none of them are normal subgroups.  

Suppose not:  
Without loss of generality, assume $ C_G(x_3) \triangleleft G $. Then, for all $ g \in G $, $ g C_G(x_3) g^{-1} = C_G(x_3) $. For all $ a \in C_G(x_3) $, $ a x_3 = x_3 a $, and $ g a g^{-1} x_3 = x_3 g a g^{-1} $. This implies $ a g^{-1} x_3 g = g^{-1} x_3 g a $, i.e., $ a \in C_G(g^{-1} x_3 g) $. Thus, $ C_G(x_3) \subseteq C_G(g^{-1} x_3 g) $. Similarly, $ C_G(g^{-1} x_3 g) \subseteq C_G(x_3) $. Therefore, $ C_G(g^{-1} x_3 g) = C_G(x_3) $.  

Since the map $ \phi: G \rightarrow G $, $ a \mapsto g a g^{-1} $ is a bijection, there exists $ g_0 \in G $ such that $ x_i = a_i x_3 a_i^{-1} $ for $ i \neq 3 $. This implies $ C_G(x_3) = C_G(x_i) $ for $ i \neq 3 $, which is impossible!

