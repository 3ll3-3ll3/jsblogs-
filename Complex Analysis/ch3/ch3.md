## <p style="color:green">CH3 Taylor Expansion of Analytic Functions</p>

### 3.1 $\boxed{Theorem} $  If $$f(z) = \sum_{n=0}^{\infty} c_n (z - a)^n \quad (z \in B(a, R))\tag{1}$$ and if $0 < r < R$, then $$\sum_{n=0}^{\infty} |c_n|^2 r^{2n} = \frac{1}{2\pi} \int_{-\pi}^{\pi} |f(a + re^{i\theta})|^2 \, d\theta.\tag{2}$$
**Proof:** We have
$$
f(a + re^{i\theta}) = \sum_{n=0}^{\infty} c_n r^n e^{in\theta}.\tag{3}
$$

For $r < R$, the series (3) converges uniformly on $[- \pi, \pi]$. Hence

$$
c_n r^n = \frac{1}{2\pi} \int_{-\pi}^{\pi} f(a + re^{i\theta}) e^{-in\theta} \, d\theta \quad (n = 0, 1, 2, \ldots),
$$

and (2) is seen to be a special case of Parseval's formula(real analysis edition).

**Corollary:** If $ f(z) = \sum\limits_{n=0}^{\infty} c_n z^n $ is a bounded holomorphic function on $ B(0,1) $, then $ \sum\limits_{n=0}^{\infty} |c_n|^2 < \infty $.
**Proof:** Suppose 
$$ 
|f(z)|\le M,\forall z\in B(0,1).
$$

From above , we have
$$ 
\sum_{n=0}^{\infty} |c_n|^2 r^{2n} \le \frac{1}{2\pi}\int_{-\pi}^{\pi} M^{2} d\theta=M^{2}, \forall r\in (0,1).
$$

By the series version of **Levi's Theorem**, it follows that
$$ 
M^{2}\ge  \lim_{r \to 1^-} \sum_{n=0}^{\infty} |c_n|^2 r^{2n} = \sum_{n=0}^{\infty} |c_n|^2 .
$$


