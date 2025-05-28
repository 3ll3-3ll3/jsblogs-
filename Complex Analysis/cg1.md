
### 3.24
>  证明：若 $f \in H(B(0,1)) \cap C(\overline{B(0,1)})$, $f(\overline{B(0,1)} ) \subset B(0,1)$，则 $f(z)$ 在 $B(0,1)$ 中有唯一的不动点。
**PROOF:**
连续映射将紧致集映为紧致集，于是存在 $r\in (0,1)$, s.t. $f(\overline{B(0,1)}) \subset \overline{B(0,r)} $。在单位圆周上，$|f-z-(-z)|=|f|\le r<1=|z|,$ 于是由幅角原理即可

 


### 3.25
>  设 $f$ 是域 $D$ 上非常数的全纯函数。证明：存在在 $D$ 中无极限点的点列 $\{z_n\}$，使得对每个 $z \in D \setminus \{z_n\}$，有 $f'(z) \neq 0$。

**PROOF:**
因为 $f$ 非常数且全纯，$f'$ 不恒为零。全纯函数 $f'$ 的零点集 $S = \{ z \in D \mid f'(z) = 0 \}$ 是离散的（每个零点孤立）且闭（由连续性，零点的极限点一定也是零点）。孤立点集合 $S$ 至多可数 **(每个点去不交小球，有理半径)** ，可表示为点列 $\{z_n\}$。假设 $S$ 在 $D$ 内有极限点 $z^*$，则 $f'$ 在 $z^*$ 的某邻域内全纯且无限多零点趋近于 $z^*$。根据唯一性定理，在 $D$ 上 $f' \equiv 0$，矛盾于 $f$ 非常数。因此，$S$ 无极限点，即为所求。

 



### 3.26
>  设 $D$ 是域，$f_n \in H(D) \cap C(\overline{D}), \forall n \in \mathbb{N}$。证明：若 $\sum\limits_{n=1}^{\infty} f_n(z)$ 在 $\partial D$ 上一致收敛，则必在 $\overline{D}$ 上一致收敛。
> 
**HINT:** 定义+最大模原理。

  

### 3.27
>  设 $z_1, z_2, \cdots, z_n \in B(\infty,1)$。证明：存在 $z_0 \in \partial B(0,1)$, 使得 $\displaystyle \prod\limits_{k=1}^n |z_0 - z_k| > 1$。
> 
**PROOF:**
否则由最大模原理得
$$ 
1<\prod_{k=1}^{n} |z_k|\le 1
$$ 
 
 **NOTE:$B(\infty,1)$  的含义解释**

在复分析中，$B(\infty,1)$  表示**以无穷远点为中心、半径为1的圆**，这是使用黎曼球面概念进行的表示。

具体解释：

1. 普通的圆盘 $\displaystyle B(z_0,r)$ 表示以z₀为中心、半径为r的圆盘

2. 当中心是无穷远点时：$\displaystyle B(\infty,r)=\{ z\in \mathbb{C}:|z|>\frac{1}{r} \}$  

因此 **$B(\infty,1)=\{ z\in \mathbb{C}:|z|>1 \}$ **，即**单位圆外部区域**。



 



### 3.28
>  （1）设 $f \in H(B(0,R))$。则 $M(r) = \max\limits_{|z|=r} |f(z)|$ 是 $[0, R)$ 上的增函数。
>  （2）设 $f \in H(B(\infty, R)) \cap C(\overline{B(\infty, R)} )$，并且 $\lim\limits_{z \to \infty} f(z)$ 存在。证明：若 $f$ 非常数，则 $M(r) = \max\limits_{|z|=r} |f(z)|$ 是 $[R, \infty)$ 上的严格减函数。
> 
**(2) PROOF:**
设 $\displaystyle g(z) = f\left(\frac{1}{z}\right)$。则 $g$ 在 $\displaystyle B\left(0,\frac{1}{R}\right) \backslash \{0\}$ 上全纯，在 $\displaystyle \overline{B\left(0,\frac{1}{R}\right)} \backslash \{0\}$ 上连续，且 $\displaystyle \lim\limits_{z\rightarrow 0} g(z) = A$ 存在。补充定义 $\displaystyle g(0) = A$ 后，$g$ 在 $\displaystyle B\left(0,\frac{1}{R}\right)$ 上连续。由 **Morera Theorem** 知 $g$ 在 $\displaystyle B\left(0,\frac{1}{R}\right)$ 上全纯，在 $\displaystyle \overline{B\left(0,\frac{1}{R}\right)}$ 上连续。 $\displaystyle \forall R \leq r_1 < r_2 < \infty$，$0 < \frac{1}{r_2} < \frac{1}{r_1} \leq \frac{1}{R}$，由最大模原理知
$$
|z| = \frac{1}{r_2} \Rightarrow |z| < \frac{1}{r_1} \Rightarrow |g(z)| < \max_{|z|=\frac{1}{r_1}} |g(z)|
$$

故

$$
\max_{|z|=\frac{1}{r_2}} |g(z)| < \max_{|z|=\frac{1}{r_1}} |g(z)| \Leftrightarrow M(r_2) = \max_{|z|=r_2} |f(z)| < \max_{|z|=r_1} |f(z)| = M(r_1)
$$
 
 

### 3.29
>  设 $f \in H(B(0,1)), f(0) = 0$。证明：$\sum\limits_{n=1}^{\infty} f(z^n)$ 在 $B(0,1)$ 上绝对且内闭一致收敛。

[见qs](https://mp.weixin.qq.com/s/X0V7MwHdUrRIpqSToPsdaQ)


### 3.30
> **全纯函数的 Hadamard 三圆定理:** 设 $0 < r_1 < r_2 < \infty, D = \{z \in \mathbb{C} : r_1 < |z| < r_2\}, f \in H(D) \cap C(\overline{D}), M(r) = \max\limits_{|z|=r} |f(z)| (r_1 < r < r_2)$。证明：$\log M(r)$ 在 $[r_1, r_2]$ 上是 $\log r$ 的凸函数，即
$$
\log M(r) \leq \frac{\log r_2 - \log r}{\log r_2 - \log r_1} \log M(r_1) + \frac{\log r - \log r_1}{\log r_2 - \log r_1} \log M(r_2).
$$

**PROOF1:**
在[三线引理](分析题.md/#11)中考虑
$$
h(z) = f(e^z),\ \ln R_1 < \ln r_1 < \Re z < \ln r_2 < \ln R_2,
$$

则
$$
\sup_{y \in \mathbb{R}} \left| f\left(e^{\ln r + iy}\right) \right| \leq \sup_{y \in \mathbb{R}} \left| f\left(e^{\ln r_1 + iy}\right) \right|^{\frac{\ln r_2 - \ln r}{\ln r_2 - \ln r_1}} \cdot \sup_{y \in \mathbb{R}} \left| f\left(e^{\ln r_2 + iy}\right) \right|^{\frac{\ln r - \ln r_1}{\ln r_2 - \ln r_1}},\quad \ln r \in [\ln r_1, \ln r_2],
$$

即
$$
\log M(r) \leq \frac{\log r_2 - \log r}{\log r_2 - \log r_1} \log M(r_1) + \frac{\log r - \log r_1}{\log r_2 - \log r_1} \log M(r_2).
$$
 
 
 
**PROOF2:** 
利用最大模原理有 $M(r)\le \max \{ M(r_1),M(r_2) \}$, 于是应该有 $M(r)\le \alpha M(r_1) +(1-\alpha)M(r_2),\alpha\in (0,1)$, 或者变换一下得到 $\log M(r)\le \alpha' \log M(r_1) +(1-\alpha')\log M(r_2),\alpha'\in (0,1)$ 
 
于是待定 $q(r)=A\log M(r_1)+B   $ 满足边界条件 $q(r_1)=\log M(r_1),q(r_2)=\log M(r_2)$ .解得
$$ 
q(r)= \frac{\log r_2 - \log r}{\log r_2 - \log r_1} \log M(r_1) + \frac{\log r - \log r_1}{\log r_2 - \log r_1} \log M(r_2)
$$

故有
$$ 
\log M(r)\le q(r)= \frac{\log r_2 - \log r}{\log r_2 - \log r_1} \log M(r_1) + \frac{\log r - \log r_1}{\log r_2 - \log r_1} \log M(r_2) 
$$


 


### 3.31
>（1）设 $f \in H(B(0,1)), f(0) = 0$，并且存在 $A > 0$，使得 $\operatorname{Re} f(z) \leq A, \forall z \in B(0,1)$。证明：$$|f(z)| \leq \frac{2A|z|}{1 - |z|}, \quad \forall z \in B(0,1).$$

**PROOF:**
对
$$ 
g(z):=\frac{f(z)}{f(z)-2A}
$$ 
用 Schwarz 引理即可。注意 
$$  
\left| g \right| \le 1 \Longleftrightarrow |f|^{2}\le |f|^{2}+4A^{2}-2A(f+\overline {f} )\Longleftrightarrow 4A \Re  f\le 4A^{2} \Longleftrightarrow \Re  f\le A 
$$

> （2）**Carathéodory 不等式:** 设 $f \in H(B(0,R)) \cap C(\overline{B(0,R)})$，$M(r) = \max\limits_{|z|=r} |f(z)|$，$A(r) = \max\limits_{|z|=r} \operatorname{Re} f(z) \ (0 \leq r \leq R)$。证明：
$$
M(r) \leq \frac{2r}{R - r} A(R) + \frac{R + r}{R - r} |f(0)|, \quad \forall r \in [0, R).
$$

**HINT:对 $g(z)=f(z)-f(0)$用（1）** [详见知乎](https://zhuanlan.zhihu.com/p/640805927)
 **NOTE:其实感觉[Schwarz 积分公式](ch2.md#28)也能算**

### 3.32
> 设 $f \in H(B(0,1))$。证明：存在 $z_0 \in \partial B(0,1)$ 和收敛于 $z_0$ 的点列 $\{z_n\}$，使得 $\lim\limits_{n \to \infty} f(z_n)$ 存在。

[见qs](https://mp.weixin.qq.com/s/X0V7MwHdUrRIpqSToPsdaQ)

### 3.33
>  求出所有满足条件“$|f(z)| = 1, \forall z \in \partial B(0,1)$”的整函数。



### 3.34
>  设 $P_n(z)$ 是 $n$ 次多项式, $P_n^*(z) = z^n P_n\left(\frac{1}{z}\right)$。证明：若 $P_n(z)$ 的所有零点都在 $B(\infty, 1)$ 内, 则 $P_n(z) + e^{i\theta} P_n^*(z) (\theta \in \mathbb{R})$ 的零点都在 $\partial B(0,1)$ 上。













1.  设 $f \in H(B(0,1)), f(B(0,1)) \subset B(0,1)$。证明：若 $z_1, z_2, \cdots, z_n$ 是 $f$ 在 $B(0,1)$ 中的所有彼此不同的零点，其阶数分别为 $k_1, k_2, \cdots, k_n$，则
$$
|f(z)| \leq \prod_{j=1}^n \left| \frac{z_j - z}{1 - \overline{z_j}z} \right|^{k_j}, \quad \forall z \in B(0,1).
$$
特别地，有
$$
|f(0)| \leq \prod_{j=1}^n |z_j|^{k_j}.
$$

1.  设 $f \in H(B(0,1)), f(B(0,1)) \subset B(0,1)$。证明：
$$
\frac{|f(0)| - |z|}{1 - |f(0)||z|} \leq |f(z)| \leq \frac{|f(0)| + |z|}{1 + |f(0)||z|}.
$$

1.  设 $f \in H(B(0,1)), f(B(0,1)) \subset B(0,M)$。证明：
$$
M|f'(0)| \leq M^2 - |f(0)|^2.
$$

1.  设 $f \in H(B(0,1)), f(0) = 0, f(B(0,1)) \subset B(0,1)$。证明：若存在 $z_1, z_2 \in B(0,1)$，使得 $z_1 \neq z_2, |z_1| = |z_2|, f(z_1) = f(z_2)$，则
$$
|f(z_1)| = |f(z_2)| \leq |z_1|^2 = |z_2|^2.
$$
（提示：考虑
$$
\frac{f(z_1) - f(z)}{1 - \overline{f(z_1)} f(z)} \left( \frac{1 - \overline{z_1}z}{z_1 - z} \right) \left( \frac{1 - \overline{z_2}z}{z_2 - z} \right)
$$
）。