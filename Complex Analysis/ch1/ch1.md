
## <p style="color:green">CH1 Holomorphic Function</p>
### 1.1 A function $u(x, y)$ is harmonic on the complex plane $\mathbb{C}$, and $u(x, y) \geq a$, where $a$ is a constant. Prove that $u(x, y)$ is constant.
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
<div style="text-align: right;font-size: 20px;">▢</div>

### 1.2 Let $D$ be the interior of a circle $C$, and let $f(z)$ be a function that is: (i) Analytic in the domain $D$ (ii) Continuous on the closure $\overline{D} = D \cup C$. If $|f(z)|$ is constant on $C$, prove that either: 1. $f(z)$ is constant, or 2. $f(z)$ has at least one zero in $D$.
**Proof:**  
Assume \( f(z) \) has no zeros in \( D \). Then \( g(z) = 1/f(z) \) is analytic in \( D \) and continuous on $\overline{D}$. On $C$, $|f(z)|=M$, so $|g(z)|=1/M$. By the **Maximum Modulus Principle**, $|f(z)| \leq M$ and $|g(z)| \leq 1/M$ in $D$, implying $|f(z)| \geq M$. Thus, $|f(z)| \equiv M$, forcing $f(z)$ to be constant (obtained through the **C-R equations**). 
 <div style="text-align: right;font-size: 20px;">▢</div>

### 1.3 Let $f(z)$ and $g(z)$ be analytic functions on a domain $D$. If $|f(z)| = |g(z)|$ holds for all $z$ in $D$, then there exists a constant $c \in \mathbb{C}$ with $|c|=1$ such that $f(z) = c \cdot g(z)$ in $D$.
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
 <div style="text-align: right;font-size: 20px;">▢</div>

### 1.4 Let $f(z)$ be a polynomial function. Suppose $f\left(\frac{1}{n}\right)$ is real for $n=1,2,\dots$. Prove that $f$ takes real values on the real axis.
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










