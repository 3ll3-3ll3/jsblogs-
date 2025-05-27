
### 3.24
#### 证明：若 $f \in H(B(0,1)) \cap C(\overline{B(0,1)})$, $f(\overline{B(0,1)} ) \subset B(0,1)$，则 $f(z)$ 在 $B(0,1)$ 中有唯一的不动点。
**PROOF:**
连续映射将紧致集映为紧致集，于是存在 $r\in (0,1)$, s.t. $f(\overline{B(0,1)}) \subset \overline{B(0,r)} $。在单位圆周上，$|f-z-(-z)|=|f|\le r<1=|z|,$ 于是由幅角原理即可

---


### 3.25
#### 设 $f$ 是域 $D$ 上非常数的全纯函数。证明：存在在 $D$ 中无极限点的点列 $\{z_n\}$，使得对每个 $z \in D \setminus \{z_n\}$，有 $f'(z) \neq 0$。

**PROOF:**
因为 $f$ 非常数且全纯，$f'$ 不恒为零。全纯函数 $f'$ 的零点集 $S = \{ z \in D \mid f'(z) = 0 \}$ 是离散的（每个零点孤立）且闭（由连续性，零点的极限点一定也是零点）。孤立点集合 $S$ 至多可数 **(每个点去不交小球，有理半径)** ，可表示为点列 $\{z_n\}$。假设 $S$ 在 $D$ 内有极限点 $z^*$，则 $f'$ 在 $z^*$ 的某邻域内全纯且无限多零点趋近于 $z^*$。根据唯一性定理，在 $D$ 上 $f' \equiv 0$，矛盾于 $f$ 非常数。因此，$S$ 无极限点，即为所求。

---



### 3.26
#### 设 $D$ 是域，$f_n \in H(D) \cap C(\overline{D}), \forall n \in \mathbb{N}$。证明：若 $\sum\limits_{n=1}^{\infty} f_n(z)$ 在 $\partial D$ 上一致收敛，则必在 $\overline{D}$ 上一致收敛。
**HINT:** 定义+最大模原理。

 ---

### 3.27
#### 设 $z_1, z_2, \cdots, z_n \in B(0,1)$。证明：存在 $z_0 \in \partial B(0,1)$, 使得 $\prod\limits_{k=1}^n |z_0 - z_k| > 1$。



### 3.28
#### （1）设 $f \in H(B(0,R))$。则 $M(r) = \max\limits_{|z|=r} |f(z)|$ 是 $[0, R)$ 上的增函数。
#### （2）设 $f \in H(B(\infty, R)) \cap C(B(\infty, R))$，并且 $\lim\limits_{z \to \infty} f(z)$ 存在。证明：若 $f$ 非常数，则 $M(r) = \max\limits_{|z|=r} |f(z)|$ 是 $[R, \infty)$ 上的严格减函数。


### 3.29
#### 设 $f \in H(B(0,1)), f(0) = 0$。证明：$\sum\limits_{n=1}^{\infty} f(z^n)$ 在 $B(0,1)$ 上绝对且内闭一致收敛。



### 3.30
#### $\boxed{\text{（全纯函数的 Hadamard 三圆定理）}}$ 设 $0 < r_1 < r_2 < \infty, D = \{z \in \mathbb{C} : r_1 < |z| < r_2\}, f \in H(D) \cap C(\overline{D}), M(r) = \max\limits_{|z|=r} |f(z)| (r_1 < r < r_2)$。证明：$\log M(r)$ 在 $[r_1, r_2]$ 上是 $\log r$ 的凸函数，即
$$
\log M(r) \leq \frac{\log r_2 - \log r}{\log r_2 - \log r_1} \log M(r_1) + \frac{\log r - \log r_1}{\log r_2 - \log r_1} \log M(r_2).
$$


### 3.31
#### （1）设 $f \in H(B(0,1)), f(0) = 0$，并且存在 $A > 0$，使得 $\operatorname{Re} f(z) \leq A, \forall z \in B(0,1)$。证明：$$|f(z)| \leq \frac{2A|z|}{1 - |z|}, \quad \forall z \in B(0,1).$$

#### （2）$\boxed{\text{（Carathéodory 不等式）}}$ 设 $f \in H(B(0,R)) \cap C(\overline{B(0,R)})$，$M(r) = \max\limits_{|z|=r} |f(z)|$，$A(r) = \max\limits_{|z|=r} \operatorname{Re} f(z) \ (0 \leq r \leq R)$。证明：
$$
M(r) \leq \frac{2r}{R - r} A(R) + \frac{R + r}{R - r} |f(0)|, \quad \forall r \in [0, R).
$$




### 3.32
#### 设 $f \in H(B(0,1))$。证明：存在 $z_0 \in \partial B(0,1)$ 和收敛于 $z_0$ 的点列 $\{z_n\}$，使得 $\lim\limits_{n \to \infty} f(z_n)$ 存在。
[见qs](https://mp.weixin.qq.com/s/X0V7MwHdUrRIpqSToPsdaQ)

### 3.33
#### 求出所有满足条件“$|f(z)| = 1, \forall z \in \partial B(0,1)$”的整函数。



### 3.34
#### 设 $P_n(z)$ 是 $n$ 次多项式, $P_n^*(z) = z^n P_n\left(\frac{1}{z}\right)$。证明：若 $P_n(z)$ 的所有零点都在 $B(\infty, 1)$ 内, 则 $P_n(z) + e^{i\theta} P_n^*(z) (\theta \in \mathbb{R})$ 的零点都在 $\partial B(0,1)$ 上。













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