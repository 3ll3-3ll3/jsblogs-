[TOC]
# 拓扑基础知识
## 1.



### 1.1
>  

 **PROOF:**
 不妨设 $a_0 = 1$。下面，我们递归地定义 $b_n$ 如下：令 $b_0 = 1$，当 $b_0, \cdots, b_{n-1}$ 已定义好后，令
$$
b_n = -\sum_{i=0}^{n-1} a_{n-i} b_i, \quad n > 1.
$$

我们来说明幂级数 $\displaystyle\sum_{n=0}^{\infty} b_n x^n$ 具有正的收敛半径。事实上，因为 $\displaystyle\sum_{n=0}^{\infty} a_n x^n$ 在 $(-R, R)$ 中收敛，故存在 $M > 0$，使得
$$
\left| a_n \left( \frac{R}{2} \right)^n \right| \leq M, \quad \forall\, n \geq 0.
$$

因此有
$$
\left| b_n \left( \frac{R}{2} \right)^n \right| \leq \sum_{i=0}^{n-1} \left| a_{n-i} \left( \frac{R}{2} \right)^{n-i} \right| \cdot \left| b_i \left( \frac{R}{2} \right)^i \right| \leq M \sum_{i=0}^{n-1} \left| b_i \left( \frac{R}{2} \right)^i \right|.
$$

由此利用归纳法不难得到下面的估计
$$
\left| b_n \left( \frac{R}{2} \right)^n \right| \leq (1 + M)^n, \quad \forall\, n > 0.
$$

这说明，幂级数 $\displaystyle\sum_{n=0}^{\infty} b_n x^n$ 的收敛半径至少为 $r = \dfrac{R}{2(1+M)}$。根据 $\{b_n\}$ 的构造，显然（我们假设了 $a_0 = 1$）
$$
\left( \sum_{n=0}^{\infty} a_n x^n \right) \left( \sum_{n=0}^{\infty} b_n x^n \right) = \sum_{n=0}^{\infty} \left( \sum_{i+j=n} a_i b_j \right) x^n = 1.
$$ 
 

**NOTE: 前几项计算如下（未假设 $a_0=1$）：**
利用递推公式，前几项系数为：

1. $b_0$:
$$
b_0 = \frac{1}{a_0}
$$

2. $b_1$:
$$
b_1 = -\frac{1}{a_0} (a_1 b_0) = -\frac{a_1}{a_0^2}
$$

3. $b_2$:
$$
b_2 = -\frac{1}{a_0} (a_1 b_1 + a_2 b_0) = -\frac{1}{a_0} \left[ a_1 \left(-\frac{a_1}{a_0^2}\right) + a_2 \left(\frac{1}{a_0}\right) \right] = \frac{a_1^2 - a_0 a_2}{a_0^3}
$$

4. $b_3$:
$$
b_3 = -\frac{1}{a_0} (a_1 b_2 + a_2 b_1 + a_3 b_0) = -\frac{1}{a_0} \left[ a_1 \left(\frac{a_1^2 - a_0 a_2}{a_0^3}\right) + a_2 \left(-\frac{a_1}{a_0^2}\right) + a_3 \left(\frac{1}{a_0}\right) \right]
$$
化简后：
$$
b_3 = -\frac{a_1^3 - 2a_0 a_1 a_2 + a_0^2 a_3}{a_0^4}
$$

  


### 1.2
>   **Abel变换** 设 $\{a_k\}$, $\{b_k\}$ 为数列，则有$$\sum_{k=n}^m a_k (b_k - b_{k-1}) = a_m b_m - a_{n-1} b_{n-1} - \sum_{k=n}^{m-1} b_k (a_{k+1} - a_k)$$ 或者等价地写为$$\sum_{k=n}^m a_k b_k = a_m B_m - a_{n-1} B_{n-1} - \sum_{k=n}^{m-1} B_k (a_{k+1} - a_k)$$其中 $\displaystyle B_k = \sum_{j=n}^k b_j$。

### 1.3
>  泰勒公式余项对比
| 余项类型       | 形式                                                                 | 适用场景                                                                 | 优点                                                                 | 缺点                                                                 | 经典应用示例                                                                 |
|     -|                       -|                        --|                       -|                       -|                          |
| **佩亚诺余项** | $ \displaystyle R_n(x) = o\left((x-a)^n\right) \quad (x \to a) $                 | - 局部极限/极值分析<br>- 简化定性分析                                    | - 形式简单<br>- 无需计算具体余项值                                   | - 仅限$x \to a$<br>- 无法定量误差                                  | 求极限：<br>$ \displaystyle \lim_{x \to 0} \frac{\sin x - x}{x^3} = -\frac{1}{6} $       |
| **拉格朗日余项** | $ \displaystyle R_n(x) = \frac{f^{(n+1)}(\xi)}{(n+1)!}(x-a)^{n+1} $<br>$ \displaystyle \xi \in (a,x) $ | - 全局误差估计<br>- 收敛性证明<br>- 数值计算                          | - 定量表达误差<br>- 适用于区间内任意$x$                            | - 需计算高阶导数<br>- $\xi$未知（只能估计上界）                    | 证明级数收敛：<br>$ \displaystyle e^x = \sum_{k=0}^\infty \frac{x^k}{k!} $               |
| **积分型余项** | $ \displaystyle R_n(x) = \frac{1}{n!} \int_a^x (x-t)^n f^{(n+1)}(t) \, dt $      | - 高阶光滑函数分析<br>- 严格理论证明<br>- 精确误差计算                  | - 表达式精确<br>- 可结合积分技巧推导                                 | - 计算复杂<br>- 需$f^{(n+1)}$可积                                  | 数学推导：<br>泰勒公式的积分法证明                                           |                                     |

**积分余项的记忆：重复NL公式，直到出现 $ (x-t)^n $ 项：**  

$$ \begin{align*}   
\displaystyle f(x) &= f(a) + \int_a^x f'(t) \, dt\\
\displaystyle \int_a^x f'(t) dt &= f'(a)(x-a) + \int_a^x f''(t)(x-t) dt\\
\int_a^x f''(t)(x-t)dt &= f''(a)\frac{(x-a)^2}{2} + \int_a^x f'''(t)\frac{(x-t)^2}{2}dt \\
\int_a^x f'''(t)\frac{(x-t)^2}{2}dt &= f'''(a)\frac{(x-a)^3}{3!} + \int_a^x f^{(4)}(t)\frac{(x-t)^3}{3!}dt\\
&\vdots \\
\int_a^x f^{(n)}(t)\frac{(x-t)^{n-1}}{(n-1)!}dt &= f^{(n)}(a)\frac{(x-a)^n}{n!} + \int_a^x f^{(n+1)}(t)\frac{(x-t)^n}{n!}dt\\
f(x) &= f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \cdots + \frac{f^{(n)}(a)}{n!}(x-a)^n + R_n(x) 
\end{align*}$$


### 1.4
>  泰勒级数及其收敛域


| 函数                     | 泰勒级数展开                                                                 | 实数收敛域               | 复数收敛域                     |
|        --|                         --|        --|          --|
| $e^z$      | $\displaystyle \sum_{n=0}^{\infty} \frac{z^n}{n!}$                       | $(-\infty, +\infty)$   | **全平面**（$\mathbb{C}$）   |
| $\sin z$   | $\displaystyle \sum_{n=0}^{\infty} (-1)^n \frac{z^{2n+1}}{(2n+1)!}$      | $(-\infty, +\infty)$   | **全平面**（$\mathbb{C}$）   |
| $\cos z$   | $\displaystyle \sum_{n=0}^{\infty} (-1)^n \frac{z^{2n}}{(2n)!}$          | $(-\infty, +\infty)$   | **全平面**（$\mathbb{C}$）   |
| \(\ln(1+z)\)  | $\displaystyle \sum_{n=1}^{\infty} (-1)^{n+1} \frac{z^n}{n}$         | $(-1, 1]$              | **单位圆盘**（$\|z\| < 1$）<br>（$z=-1$ 发散） |
| $\frac{1}{1-z}$ / $\frac{1}{1-x}$ | $\displaystyle \sum_{n=0}^{\infty} z^n$                     | $(-1, 1)$              | **单位圆盘**（$\|z\| < 1$）  |
| $(1+z)^k$ | $\displaystyle \sum_{n=0}^{\infty} \binom{k}{n} z^n$                  | $(-1, 1)$              | **单位圆盘**（$\|z\| < 1$）<br>（$k \in \mathbb{C}$） |
| $\arctan z$ | $\displaystyle \sum_{n=0}^{\infty} (-1)^n \frac{z^{2n+1}}{2n+1}$    | $[-1, 1]$              | **单位圆盘**（$\|z\| < 1$） |
| $\sinh z$ | $\displaystyle \sum_{n=0}^{\infty} \frac{z^{2n+1}}{(2n+1)!}$          | $(-\infty, +\infty)$   | **全平面**（$\mathbb{C}$）   |
| $\cosh z$  | $\displaystyle \sum_{n=0}^{\infty} \frac{z^{2n}}{(2n)!}$              | $(-\infty, +\infty)$   | **全平面**（$\mathbb{C}$）   |