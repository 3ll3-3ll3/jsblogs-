Here's a solution that only rests on the following simple trigonometric identity:
$$\cos(a+b)+\cos(a-b)=2\cos(a)\cos(b)\tag{1}$$
We'll get back to it later, but for now, notice that
$$\begin{split}
I_n(x)&=\int_0^{\pi} \frac{\cos(nx)\cos(x) - \cos(nt)\cos(t)}{\cos(x) -\cos(t)}dt\\
&=\int_0^{\pi}\frac{[\cos(nx)-\cos(nt)]\cos(x) + \cos(nt)[\cos(x)-\cos(t)]}{\cos(x) -\cos(t)}dt\\
&=\cos(x)\int_0^{\pi}\frac{\cos(nx)-\cos(nt)}{\cos(x) -\cos(t)}dt+\int_0^\pi\cos(nt)dt
\end{split}$$
In other words, 
$$I_n(x)=\cos(x)J_n(x)+\pi\delta_{n=0}\tag{2}$$
where we define $$J_n(x)=\int_0^\pi \frac{\cos(nx)-\cos(nt)}{\cos(x)-\cos(t)}dt$$
and the Kronecker symbol $\delta_{n=0}$, which is equal $0$, unless $n=0$, in which case it's equal to $1$.

Now, let's go back to (1). Plugging $a=nx$ and $b=x$ into that identity implies that
$$\cos((n+1)x)+\cos((n-1)x)=2\cos x \cos(nx)$$
Subtracting the same equation with $t$ to this one yields
$$
\begin{split}
\cos((n+1)x)-\cos((n+1)t) \\
+\cos((n-1)x)-\cos((n-1)t)=\\
2\cos x \cos(nx)-2\cos(t)\cos(nt)
\end{split}$$
Dividing by $\cos(x)-\cos(t)$, and integrating over $[0,\pi]$ leads to
$$J_{n+1}(x)+J_{n-1}(x)=2I_n(x)\tag{3}$$
Finally, combining [2] and [3] gets us, for $n\geq 0$,
$$J_{n+2}(x)-2\cos(x)J_{n+1}(x)+J_{n}(x)=0$$

The solution to this second-order recurrence relation is 
$$J_n(x)=\alpha e^{inx}+\beta e^{-inx}$$
Since, $J_0=0$ and $J_1=\pi$, 
$$J_n(x)=\frac {\pi \sin(nx)}{\sin x}$$
and 
 
