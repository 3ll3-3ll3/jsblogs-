
## <p style="color:green">CH2 Integral Representation of Analytic Functions</p>

### 2.1 
####  设$f\in C^1(D)$，$\gamma$ 是域 $D$ 中分别以 $a$ 和 $b$ 为起点和终点的可求长曲线. 则 $$\displaystyle      \int\limits_\gamma \bigg\{\frac{\partial f(z)}{\partial z} dz+\frac{\partial f(z)}{\partial \overline{z} } d\overline{z}  \bigg\} = f(b) - f(a).$$ 

### 2.2 
####  设 $\gamma$ 是可求长曲线，$\varphi$ 在 $\gamma$ 上全纯，$\Gamma=\varphi(\gamma)$. 则 （1）$\Gamma$也是可求长曲线；（2）如果$f$在$\Gamma$上连续，那么 $$           \int\limits_\Gamma f(w) dw = \int\limits_\gamma f\big(\varphi(z)\big)\varphi'(z) dz. $$
 

### 2.3 
####  $f,g\in H(D)\cap C^1(D)$，$\gamma$ 是域 $D$ 中分别以 $a$ 和 $b$ 为起点和终点的可求长曲线. 则 $$\displaystyle      \int\limits_\gamma f(z)g'(z) dz = f(z)g(z) \bigg|_a^b - \int\limits_\gamma f'(z)g(z) dz. $$

### 2.4 
####  设 $\gamma$ 是正向可求长简单闭曲线，则 $\gamma$ 内部的面积为 $\displaystyle \frac{1}{2i}\int\limits_\gamma \overline{z} dz.$

### 2.5 
####  设单叶全纯映射 $f$ 将可求长简单闭曲线 $\gamma$ 映为正向简单闭曲线 $\Gamma$，则 $\Gamma$ 内部的面积为 $\displaystyle  \frac{1}{2i} \int\limits_\gamma \overline{f(z)}f'(z) dz.$ 

### 2.6 
####  $0<r<R,f$ is harmonic in $B(0,R)$ and $u$ is harmonic in $B(0,R)$. Then : $$ f(0)=\frac{1}{2\pi}\int_{0}^{2\pi} f(re^{i\theta}) d\theta,u(0)=\frac{1}{2\pi}\int_{0}^{2\pi} u(re^{i\theta}) d\theta $$

The first equality can be readily derived from **Cauchy Integral Formula** and the second one can be derived from the first equation and the theorem stating that **every harmonic function on a simply connected domain is the real part of some holomorphic function** .

**eg:** Let $u(x,y)=\log(1-2r \cos \theta + r^2)=\log(x^{2}-2x+1+y^{2})$, it's easy to check that $u$ is harmonic in $B(0,1)$.Then
$$\begin{align*}
 \forall  0\leq r<1, \int_{0}^{\pi} \log(1-2r \cos \theta + r^2) d\theta  &=\frac{1}{2} \int_{0}^{2\pi} \log(1-2r \cos \theta + r^2) d\theta \\
&=\frac{\pi}{2\pi} \int_{0}^{2\pi} u(re^{i\theta}) d\theta=\pi u(0)=0   
\end{align*}$$

---
### 2.7 
####  设 $f$ 是凸域 $D$ 上的全纯函数，如果对每点 $z\in D$，有 $\Re \{f'(z)\}>0$，那么 $f$ 是 $D$ 上的单叶函数.

**PROOF:** 

$$\begin{align*}
\forall z_1,z_2\in D,z_1\ne z_2, \frac{f(z_1)-f(z_2)}{z_1-z_2} &= \frac{1}{z_1-z_2} \int_{z_1}^{z_2} f'(w) dw \\
&=\frac{1}{z_1-z_2} \int_{0}^{1} f'(z_2+(z_1-z_2)t) (z_1-z_2)dt \\
&= \int_{0}^{1} f'(z_2+(z_1-z_2)t) dt \\
&= \int_{0}^{1} \Re \{f'(z_1+(z_2-z_1)t)\} dt \ge \min\limits_{t\in[0,1]} \Re \{f'(z_1+(z_2-z_1)t)\} > 0
\end{align*}$$ 


---


### 2.8 
####  <mark>The Schwarz Integral Formula </mark>: Let $f\in H(B(0,R))\cap C(\overline{B(0,R)}),f=u+\mathrm{i}v.$Then for every $z\in B(0,R)$, we have $$ f ( z ) = { \frac { 1 } { 2 \pi } } \int _ { 0 } ^ { 2 \pi } { \frac { R \mathrm { e } ^ { \mathrm { i } \theta } + z } { R \mathrm { e } ^ { \mathrm { i } \theta } - z } } u ( R \mathrm { e } ^ { \mathrm { i } \theta } ) \, \mathrm { d } \theta + \mathrm { i } v ( 0 ). $$

 **PROOF1:**
$$\begin{align*}
I:= { \frac { 1 } { 2 \pi } } \int _ { 0 } ^ { 2 \pi } { \frac { R \mathrm { e } ^ { \mathrm { i } \theta } + z } { R \mathrm { e } ^ { \mathrm { i } \theta } - z } } u ( R \mathrm { e } ^ { \mathrm { i } \theta } ) \, \mathrm { d } \theta &=\frac{1}{2\pi \mathrm{i}}\int\limits_{|w|=R} \frac{w+z}{w-z}u(w) \frac{dw}{w}\\
&=\frac{1}{2\pi \mathrm{i}}\int\limits_{|w|=R} \frac{w+z}{w-z}\frac{f(w)+\overline{f(w)} }{2} \frac{dw}{w}\\
&=\frac{1}{4\pi \mathrm{i}}\int\limits_{|w|=R} (\frac{2}{w-z}-\frac{1}{w})[f(w)+\overline{f(w)} ]dw\\
&=\frac{1}{4\pi \mathrm{i}}\int\limits_{|w|=R} (\frac{2}{w-z}-\frac{1}{w})f(w)dw+\frac{1}{4\pi \mathrm{i}}\int\limits_{|w|=R} (\frac{2}{w-z}-\frac{1}{w})\overline{f(w)} dw\\
&:=I_1+I_2\\
&=f(z)-\frac{f(0)}{2}+I_2
\end{align*}$$

Noting that if we let $\xi=R e ^{\mathrm{i}\theta}$, we have $\displaystyle  \frac{\mathrm{d}\xi}{\xi}=\mathrm{id}\theta=-\frac{\mathrm{d}\overline{\xi} }{\overline{\xi} }$. Then:

$$\begin{align*}
I_2\overset{\xi=\overline{\eta} }{=} \frac{1}{4\pi \mathrm{i}}\int\limits_{(|\eta|=R)^{^-}} (\frac{2}{\overline{\eta}-z }-\frac{1}{\overline{\eta} })\overline{f(\overline{\eta} )} (-1)\frac{\overline{\eta} }{\eta}\mathrm{d}\eta &=   \frac{1}{4\pi \mathrm{i}}\int\limits_{|\eta|=R} (\frac{2\overline{\eta} }{R^{2}-\eta z }-\frac{1}{\overline{\eta} })\overline{f(\overline{\eta} )} (-1)\frac{\overline{\eta} }{\eta}\mathrm{d}\eta           \\
&=\frac{1}{4\pi \mathrm{i}}\int\limits_{|\eta|=R} \frac{2R^{2}\overline{f(\overline{\eta} )} }{R^{2}-\eta z}\cdot \frac{1}{\eta} \mathrm{d}\eta-\frac{\overline{f(\overline{\eta} )} }{\eta} {\huge |} _{\eta=0}           \\
&\overset{(*)}{=} \frac{2\pi \mathrm{i}}{4\pi \mathrm{i}}\frac{2R^{2}\overline{f(\overline{z} )} }{R^{2}-z \eta}{\huge |} _{\eta=0} -\frac{\overline{f(\overline{\eta} )} }{\eta} {\huge |} _{\eta=0} =\frac{\overline{f(0)} }{2}          \\
\end{align*}$$

It's worth noting that $\overline{f(\overline{\eta} )}$ is holomorphic according to  exercise [1.8](ch1.md#18).   

$(*):$ When $\displaystyle  z\in B(0,R),\frac{R^{2}}{z}$ isn't a singularity of $\displaystyle \frac{2R^{2}\overline{f(\overline{\eta} )} }{R^{2}-\eta z}$, so we can apply Cauchy Integral Formula to it.

Therefore, we have:
$$\begin{align*}
I=f(z)-\mathrm{i}v(0)
\end{align*}$$


**PROOF2:**
According to **Poisson Integral Formula**, we have;
$$\begin{align*}
u(z)=\frac{1}{2\pi}\int_{0}^{2\pi} \frac{R^{2}-|z|^{2}}{|R e^{\mathrm{i}\theta}-z|^{2}}u(R e^{\mathrm{i}\theta})d\theta =\frac{1}{2\pi}\int_{0}^{2\pi} \Re  [\frac{e^{\mathrm{i}\theta}+z}{e^{\mathrm{i}\theta}-z}] u(e^{\mathrm{i}\theta})d\theta 
\end{align*}$$

Since $\displaystyle \widetilde{f}(z) := \frac{1}{2\pi} \int_{0}^{2\pi} \frac{Rr^{\mathrm{i}\theta} + z}{Rr^{\mathrm{i}\theta} - z} u(re^{\mathrm{i}\theta}) \, d\theta$ is holomorphic in $B(0, R)$ and $\Re (\tilde{f} - f) = u - u \equiv 0$, we conclude that $\displaystyle \tilde{f} - f$ is a constant in $B(0, R)$ according to Exercise [1.18](ch1.md#118).

It is straightforward to calculate that $\displaystyle \tilde{f}(0) - f(0) = -\mathrm{i}v(0)$, thus we have $\displaystyle f = \tilde{f} + \mathrm{i}v(0)$ in $B(0, R)$.

---
### 2.9 
#### 设 $f \in H(B(0, R)) \cap C(\overline{B(0, R)})$, $f = u + iv$, 则对任意 $0 < r \leq R$, 有 $$f'(0) = \frac{1}{\pi r} \int_0^{2\pi} u(re^{i\theta}) e^{-i\theta} d\theta.$$

 **PROOF:**
$$\begin{align*}
f'(0)=\frac{1}{2\pi \mathrm{i}}\int \limits_{|\xi|=r} \frac{f(\xi)}{\xi^{2}}d\xi &=\frac{1}{2\pi r}\int_{0}^{2\pi} f(e^{\mathrm{i}\theta})e^{-\mathrm{i}\theta} d\theta\\
&=\frac{1}{2\pi r} \int_{0}^{2\pi} [u(e^{\mathrm{i}\theta})+\mathrm{i}v(e^{\mathrm{i}\theta})]e^{-\mathrm{i}\theta} d\theta\            
\end{align*}$$

于是只要证
$$\begin{align*}
\int_{0}^{2\pi} u(e^{\mathrm{i}\theta})e^{-\mathrm{i}\theta} d\theta &=\mathrm{i}\int_{0}^{2\pi} v(e^{\mathrm{i}\theta})e^{-\mathrm{i}\theta} d\theta\         \\
\Leftrightarrow  \frac{1}{2\pi \mathrm{i}} \int\limits_{|\xi|=r}^{}\frac{\overline{f(\xi)} }{\xi^{2}} d\xi &=0\\
\overset{\xi=\overline{\eta} }{\Longleftrightarrow } \frac{1}{2\pi \mathrm{i}}\int\limits_{|\eta|=r}^{}\frac{\overline{f(\overline{\eta} )} }{r^{2}} d\eta &\overset{\text{Cauchy Integral Formula} }{{\Large =} }0 
\end{align*}$$

 
 ---


### 2.10 
#### 设$f$是整函数，如果当$z\to\infty$时，$f(z)=O(|z|^\alpha),\alpha\ge0$，证明$f$是次数不超过$[\alpha]$的多项式.
 **PROOF:**

$$\begin{align*}
\exists M>0, \forall z \in \mathbb{C},|f(z)|&\le M|z| ^{\alpha},\quad n:=[\alpha]+1>\alpha\\
 \forall z\in \mathbb{C},\text{取}R=|z|,|f^{(n)}(z)|=|\frac{n!}{2\pi \mathrm{i}}\int\limits_{|\xi-z|=R}^{}\frac{f(\xi)}{(\xi-z)^{^n+1}}d\xi|& \le \frac{n!}{2\pi}\frac{2\pi R}{R^{n+1}}\cdot M(|z|+R)^{\alpha}\\
& \le n!M \frac{(2R)^{\alpha}}{R^{n}}\overset{R \to +\infty}{\longrightarrow }0  
\end{align*}$$ 
 
Therefore, $f^{(n)}(z)=0.$ Then it's easy to prove that $f$ is a polynomial of degree at most $n-1=[\alpha]$.

 ---


### 2.11 
#### (1)设$f$是整函数，如果 $ f(\mathbb{C})\subset\{z\in\mathbb{C}:\Im z>0\},$     则$f$是一个常值函数.
#### (2)设$f$是整函数，如果 $ f(\mathbb{C})\subset \mathbb{C}\backslash[0,1],$     则$f$是一个常值函数.
 **HINT:利用分式线性变换构造新函数**

(1):上半平面变为单位圆内部
$$g(z)=\frac{f(z)-i}{f(z)+i},$$

(2)
$$\begin{align*}
z\in \mathbb{C} \overset{f}{\Rightarrow }\omega\in \mathbb{C}\backslash[0,1]  \overset{\xi=\frac{\omega}{\omega-1}}{\Longrightarrow } \xi \in \mathbb{C}\backslash(-\infty,0] \overset{\eta=\sqrt{-\xi}}{\Longrightarrow }\Im \eta>0, \text{再由}(1) 
\end{align*}$$
 
 
 ---

### 2.12 
#### 设 f 在区域 D 上全纯, $z_0 \in D$, $$ F(z) := \begin{cases}\displaystyle \frac{f(z) - f(z_0)}{z - z_0}, & z \in D \setminus \{z_0\}; \\f'(z_0), & z = z_0.\end{cases}$$则$F \in H(D)$.

 **PROOF:**

We have $\displaystyle  \lim_{z \to z_0}F(z)=f'(z_0)=F(z_0) $, and thus $F(z)\in C(D)$. Choose $\delta >0$ such that $\overline{B(z_0,\delta)}\subset D$. Then $F(z)$ is holomorphic on $\overline{B(z_0,\delta)}$.

Since $F\in C(D)$, we can define $M=\max\limits_{\overline{B(z_0,\delta)} }^{}|F(z)|$. For any rectifiable closed curve $\gamma $ in $D$, let $G$ deNOTE the region enclosed by $\gamma$.

- If $z_0 \notin G$, from the **Cauchy Integral Formula**, we have 
  $$
  \begin{align*}
  \int\limits_{\gamma}^{} F(z)dz=0
  \end{align*}
  $$

- If $z_0 \in G$, then
  $$
  \left|\int\limits_{\gamma}^{}F(z)dz \right| \le \left|\int\limits_{|z-z_0|=\epsilon}^{} F(z)dz\right| \le M\cdot 2\pi \epsilon \overset{\epsilon \to 0}{\longrightarrow }0
  $$

According to the **Morera Theorem**, we conclude that $F \in H(D)$.
 
 ---


 
 