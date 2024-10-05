---
layout: post
comments: true
use_math: true
title:  "Lower bound for $L^2$ norm of second-order polynomials on a ball"
date:   2024-10-05 10:00:40 
---
 
<div>
Set 
$$  \phi(r,X_0)=\sup_{t\in (t_0-r^2,t_0)} \frac{c}{r^2}\left(\fint_{B_r(x_0)} |u(t,x)-q_{X_0,r}(x)|^2 \myd{x}\right)^{1/2} $$
for some $q_{X_0,r}(x)=a_{X_0,r}+ b_{X_0,r} \cdot (x-x_0) + (x-x_0)^T C_{X_0,r}(x-x_0)$. 
  </div>
  

If we take
<div>
\begin{align*}
 q_{X_0,r}-q_{X_0,\kappa r} &= (a_{X_0,r}-a_{X_0,\kappa r}) + (b_{X_0,r}-b_{X_0,\kappa r})\cdot (x-x_0)\\
 &\quad+ (x-x_0)^T (C_{X_0,r}-C_{X_0,\kappa r})(x-x_0),
\end{align*}  
</div>
 then a change of variable reduces the problem into
<div>
$$ \frac{c}{r^2} \left(\fint_{B_r(x_0)} |q(x)|^2 \myd{x}\right)^{1/2}=\frac{c}{r^{d/2+2}} \left(\int_{B_r}\left|a+b\cdot y + y^T Ay\right|^2 \myd{y}\right)^{1/2}. $$  
</div>
Let 
<div>
$$  q(x)=a+ b\cdot x + x^T A x. $$
</div>
Then we claim that
<div>
$$ \frac{c}{r^2}\left(\fint_{B_r} |q(x)|^2 \myd{x}\right)^{1/2}\apprge |A|.$$
</div>
Note that 
<div>
\begin{align*}
\left|a+b\cdot y + y^T Ay\right|^2&=a^2 + (b\cdot y)^2 +|y^T A y|^2 \\
&\relphantom{=}+2 a (b\cdot y) + 2a(y^T Ay)+2(b\cdot y) y^T A y.
\end{align*}
Using polar coordinates and oddness of $(b\cdot y)$ and $2(b\cdot y)y^T Ay$, we have 
\begin{align*}
&\int_{B_r} |a + b\cdot y + y^T A y|^2 \myd{y}\\
&=\int_{B_r} a^2 +(b\cdot y)^2 +|y^T Ay|^2 + 2a(y^T Ay)\myd{y}\\
&=\int_{\mathbb{S}^{d-1}}\int_0^r \left(a^2 + \rho^2(b\cdot \omega)^2+\rho^4 |\omega^T A \omega|^2 +2a\rho^2(\omega^T A \omega)\right) \rho^{d-1}d\rho d\sigma(\omega)\\
&=\int_{\mathbb{S}^{d-1}} \frac{a^2}{d}r^d+\frac{(b\cdot \omega)^2}{d+2} r^{d+2}+\frac{|\omega^T A\omega|^2}{d+4}r^{d+4}+\frac{2a(\omega^T A\omega)}{d+2}r^{d+2} d\sigma(\omega).
\end{align*}
</div>

By Young's inequality, we have 
<div>
$$ |a(\omega^T A\omega)r^{d+2}| \leq \varepsilon a^2 r^d +\frac{1}{4\varepsilon} (\omega^T A\omega)^2r^{d+4}$$
</div>
for any $\varepsilon>0$. This implies that 
<div>
\begin{align*}
&\int_{B_r} |a + b\cdot y + y^T A y|^2 \myd{y}\\
&\geq \int_{\mathbb{S}^{d-1}} \left(\frac{1}{d}-\frac{2\varepsilon}{d+2}\right)a^2 r^d +\frac{(b\cdot \omega)^2}{d+2}r^{d+2}\myd{\sigma(\omega)}\\
&\quad+ \int_{\mathbb{S}^{d-1}} \left(\frac{1}{d+4}-\frac{1}{2\varepsilon(d+2)}\right)(\omega^T A\omega)^2 r^{d+4} d\sigma(\omega).
\end{align*}
</div>
We can choose $\varepsilon>0$ so that the numbers in parenthesis become positive numbers since $d(d+4)<(d+2)^2$. This implies that 
<div>
\begin{align*}
\fint_{B_r} |a+b\cdot y +y^T A y|^2 \myd{y}&\geq cr^4 \int_{\mathbb{S}^{d-1}} (\omega^T A\omega)^2 \myd{\sigma(\omega)}.
\end{align*}
</div>

On the other hand, note that 
<div>
$$ \int_{\mathbb{S}^{d-1}} \omega_i \omega_j \omega_k \omega_l \myd{\sigma(\omega)}=\begin{cases}
1 &\quad \text{if } (i,j)=(k,l)\\
0 &\quad \text{otherwise}.
\end{cases}
$$
</div>

Hence it follows that 
<div>
$$
\int_{\mathbb{S}^{d-1}} (\omega^T A\omega)^2 \myd{\sigma(\omega)} =\int_{\mathbb{S}^{d-1}} (\omega_i A_{ij} \omega_j)(\omega_k A_{kl} \omega_l) \myd{\sigma(\omega)}\geq c\sum_{i,j} A_{ij}^2.
$$
</div>
This implies the desired result.
