
## <p style="color:green">CH1 Holomorphic Function</p>
### 1.1 
####  A function $u(x, y)$ is harmonic on the complex plane $\mathbb{C}$, and $u(x, y) \geq a$, where $a$ is a constant. Prove that $u(x, y)$ is constant.
**Proof:**  
Since $u(x, y)$ is harmonic on $\mathbb{C}$, there exists a holomorphic function $f(z)$ such that  
$$
u(x, y) = \Re f(z).
$$  

Define  
$$
g(z) = e^{-f(z)}.
$$  

Then,  
$$
|g(z)| = e^{-\Re f(z)} = e^{-u(x, y)} \leq e^{-a},
$$  
since $u(x, y) \geq a$.  

Thus, $g(z)$ is an entire and bounded function. By **Liouville's Theorem**, $g(z)$ must be constant.  

This implies that $f(z)$ is constant, and therefore $u(x, y) = \Re f(z)$ is also constant.  


---


### 1.2 
####  Let $D$ be the interior of a circle $C$, and let $f(z)$ be a function that is: (i) Analytic in the domain $D$ (ii) Continuous on the closure $\overline{D} = D \cup C$. If $|f(z)|$ is constant on $C$, prove that either: 1. $f(z)$ is constant, or 2. $f(z)$ has at least one zero in $D$.
**Proof:**  
Assume \( f(z) \) has no zeros in \( D \). Then \( g(z) = 1/f(z) \) is analytic in \( D \) and continuous on $\overline{D}$. On $C$, $|f(z)|=M$, so $|g(z)|=1/M$. By the **Maximum Modulus Principle**, $|f(z)| \leq M$ and $|g(z)| \leq 1/M$ in $D$, implying $|f(z)| \geq M$. Thus, $|f(z)| \equiv M$, forcing $f(z)$ to be constant (obtained through the **C-R equations**). 


---


### 1.3 
####  Let $f(z)$ and $g(z)$ be analytic functions on a domain $D$. If $|f(z)| = |g(z)|$ holds for all $z$ in $D$, then there exists a constant $c \in \mathbb{C}$ with $|c|=1$ such that $f(z) = c \cdot g(z)$ in $D$.
**Proof:**  
If $g(z) \equiv 0$ in $D$, then $|f(z)|=|g(z)|=0$ implies $f(z) \equiv 0$ in $D$, and the result holds trivially with any constant $c \in \mathbb{C}$ satisfying $|c|=1$.  

Suppose $g(z) \not\equiv 0$ in $D$. Define $h(z) = \frac{f(z)}{g(z)}$ on $D \setminus \{ z : g(z) = 0 \}$. Since $|f(z)|=|g(z)|$ for all $z \in D$, we have $|h(z)|=1$ wherever $h(z)$ is defined.  

Let $z_0 \in D$ be a zero of $g(z)$ of order $m$. Then $|f(z_0)|=|g(z_0)|=0$ implies $z_0$ is also a zero of $f(z)$ of the same order $m$. Near $z_0$, we can write  
$$
f(z) = (z - z_0)^m \tilde{f}(z), \quad g(z) = (z - z_0)^m \tilde{g}(z)
$$where $\tilde{f}(z)$ and $\tilde{g}(z)$ are analytic and non-vanishing at $z_0$. Thus,  
$$
h(z):= \frac{\tilde{f}(z)}{\tilde{g}(z)}
$$  is analytic at $z_0$. Repeating this argument for all zeros of $g(z)$, we conclude that $h(z)$ extends to an analytic function on the entire domain $D$.  

Since $|h(z)|=1$ everywhere on $D$, the **Maximum Modulus Principle** implies $h(z)$ is constant. Let $c=h(z)$. Then $|c|=1$, and $f(z)=c \cdot g(z)$ holds throughout $D$.     


---


### 1.4 
####  Let $f(z)$ be a polynomial function. Suppose $f\left(\frac{1}{n}\right)$ is real for $n=1,2,\dots$. Prove that $f$ takes real values on the real axis.
It is known that  
$$
h(z) := f(z) - \overline{f(\overline{z})}
$$  
is a polynomial function. For $n \in \mathbb{N}$, since $f(\frac{1}{n}) \in \mathbb{R}$ we have:
$$
h\left( \frac{1}{n} \right) = f\left( \frac{1}{n} \right) - \overline{f\left( \frac{1}{n} \right)} = f\left( \frac{1}{n} \right) - f\left( \frac{1}{n} \right) = 0
$$

Here, $f\left( \frac{1}{n} \right)$ is real, so its conjugate equals itself. The sequence \(\left\{ \frac{1}{n} \right\}\) converges to 0, and since $h$ is continuous, it follows that:
$$
h(0) = \lim_{n \to \infty} h\left( \frac{1}{n} \right) = 0
$$

Thus, $h(z)$ vanishes on the set \(\left\{ \frac{1}{n} \right\} \cup \left\{ 0 \right\}\), which has an accumulation point at 0. By the **identity theorem for analytic functions**, $h(z) \equiv 0$ holds on the entire complex plane. That is:
$$
f(z) = \overline{f(z)}, \quad \forall z \in \mathbb{C}
$$
In particular, for any real number $x$, $\overline{x} = x$, so:
$$
f(x) = \overline{f(x)}
$$
This implies that $f$ takes real values on the real axis.

---

### 1.5 
####  一些函数的可微性

| 函数               | $ z=0 $ 处的导数 | 其他点的导数      |
|--------------------|-------------------|------------------|
| $ f(z) = \|z\| $      | $ f'(0) $ 不存在 | $ f'(z) $ 不存在 |
| $ f(z) = \|z\|^2 $    | $ f'(0) = 0 $    | $ f'(z) $ 不存在 |
| $ f(z) = \Re z $     | $ f'(0) = 0 $    | $ f'(z) $ 不存在 |
| $ f(z) = \arg(z) $    | $ f'(0) $ 不存在 | $ f'(z) $ 不存在 |

### 1.6 
####  设 $f$ 和 $g$ 都在$z_0$处可微，且$f(z_0)=g(z_0)=0,g'(z_0)\ne0$. 则$ \displaystyle  \lim_{z\to z_0} \frac{f(z)}{g(z)} = \frac{f'(z_0)}{g'(z_0)}. $

### 1.7
#### 设 $f$ 和 $g$ 分别是域$D$和域$G$上的全纯函数，如果$f(D)\subset G$，那么$g\circ f$也是$D$上的全纯函数，而且 $$       \big(g\circ f\big)'(z) = g'\big(f(z)\big)f'(z). $$


### 1.8
####  设域$G$和域$D$关于实轴对称.如果$f(z)$是$D$上的全纯函数，那么$\overline{f(\overline{z} )} $是$G$上的全纯函数.

### 1.9 
####  设$D$是$\mathbb{C}$中的域，$f\in H(D),f$在$D$中不取零值.证明：对任意$p>0$，有 $$  \bigg(\frac{\partial^2 }{\partial x^2} + \frac{\partial^2 }{\partial y^2} \bigg)|f(z)|^p = p^2|f(z)|^{p-2} |f'(z)|^2. $$ 特别地,当 $f \in H(D)$ 时,有$$\begin{vmatrix}\frac{\partial u}{\partial x} & \frac{\partial u}{\partial y} \\\frac{\partial v}{\partial x} & \frac{\partial v}{\partial y}\end{vmatrix}= |f'|^2.$$

### 1.10 
####  设$D$是域，$f:D\to\mathbb{C}\backslash(-\infty,0]$是非常数的全纯函数，则$\log |f(z)|$和$\arg f(z)$是$D$上的调和函数，而$|f(z)|$不是$D$上的调和函数.

### 1.11 
####  $\log |z|$ 是 $B(0,1)\backslash\{0\}$上的调和函数，它不是$B(0,1)\backslash\{0\}$上全纯函数的实部.

### 1.12 
####  若 $u(x,y)$ 是 $x,y$的调和多项式，则 $$ f(z) = 2u\bigg( \frac{z}{2}, \frac{z}{2i} \bigg) - u(0,0) $$   是$\mathbb{C}$上的全纯函数，并且对任意$z=x+i y\in\mathbb{C},\Re f(z)=u(x,y)$.

### 1.13 
####  若 $\frac{p}{q}(q>0)$是有理数，则 $z^{\frac{p}{q}}=\big(\sqrt[q]{z} \big)^p$.

### 1.14 
####  称 $\varphi(z)=\frac{1}{2}(z+\frac1z)$ 为 Rokovsky函数.

|四个单叶性域 |上半平面$\{z\in\mathbb{C}:\Im z>0\}$ |下半平面$\{z\in\mathbb{C}:\Im z<0\}$ | 无心单位圆盘$\{z\in\mathbb{C}:0<\|z\|<1\}$ | 单位圆盘的外部$\{z\in\mathbb{C}:\|z\|>1\}$ |
|-- |--------------------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
|$\varphi$ 作用下的像集 | $\mathbb{C} \backslash (-\infty,-1] \cup [1,+\infty) $  | $\mathbb{C} \backslash (-\infty,-1] \cup [1,+\infty)$|$ \mathbb{C} \backslash [-1,1] $| $\mathbb{C} \backslash [-1,1] $|





### 1.15 
####  $$\begin{align*}w=&\cos z \text{将半条形域 } \{z\in\mathbb{C}: 0 < \Re z < 2\pi, \Im z > 0\} \text{一一地映为} \mathbb{C}\backslash[-1,+\infty) \\ w=&\sin  z \text{将半条形域 } \{z\in\mathbb{C}: -\frac{\pi}{2} < \Re z < \frac{\pi}{2}, \Im z > 0\} \text{一一地映为上半平面}\end{align*}$$

### 1.16 
####  设单叶全纯映射 $f$ 将域 $D$ 一一地映为 $G$，则 $G$ 的面积为 $\displaystyle  \iint \limits_D |f'(z)|^2 dxdy. $


### 1.17 
####  设$f$是域$D$上的单叶全纯映射，$z=\gamma(t)$（$\alpha\le t\le\beta$）是 $D$ 中的光滑曲线. ：$w=f\big(\gamma(t)\big)$的长度为$\displaystyle  \int_{\alpha}^{\beta} |f'(\gamma(t))| |\gamma'(t)| dt.$ 

### 1.18
####  设 $f \in H(D)$, 并且满足下列条件之一:
(1) $\text{Re} f(z)$ 是常数;
(2) $\text{Im} f(z)$ 是常数;
(3) $|f(z)|$ 是常数;
(4) $\arg f(z)$ 是常数;
(5) $\text{Re} f(z) = (\text{Im} f(z))^2, z \in D$,
#### 那么 $f$ 是一常数.


