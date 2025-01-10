---
layout: post
comments: true
use_math: true
title:  "Smoothing estimate for heat equation with compactly supported initial data"
date:   2025-01-09 21:00:40 
---

Today, I learned from [Sammer](https://www.math.ucdavis.edu/~sameer/) the following technique in the [winter school](https://scgp.stonybrook.edu/archives/44203) held at Stony Brook University. For beginner, I decide to give a detailed proof as possible I can (although some argument can be omitted in a professional level). The motivation of this calculation can be found in the recent paper due to [Bedrossian-He-Iyer-Wang](https://arxiv.org/pdf/2405.19233). 

<div>
Let us consider 
\begin{equation}
\partial_t u- u_{xx}=0\quad \text{in } (0,\infty)\times \mathbb{R},\quad u=u_0\quad \text{on } \{t=0\}\times \mathbb{R}.
\end{equation}
It is well-known that if $u_0 \in L^2(\mathbb{R})$, then the solution $u$ is instantaneously smooth for $t>0$. However, the solution does not have good norm control in derivatives. However, if we assume that the initial data has a compact support, say $\mathrm{supp}\, u_0 \subset (-1/4,1/4)$, then we can show that 
$$ u\in L^{\infty}(0,\infty;L^{2}((-2,2)^c). $$
</div>

<div>
To show this, we first recall the global estimate for the heat equation:
\begin{equation}
\int_{\mathbb{R}}|u(t,x)|^2\,{dx}+2\int_0^t \int_{\mathbb{R}} |\partial_x u(t,x)|^2 \,dx=\int_{\mathbb{R}} |u_0(x)|^2 \,dx.
\end{equation}
</div>
 
<div>
Choose a cut-off function $\chi$ so that $\chi=1$ in $(-1,1)$ and $\chi=0$ outside $(-2,2)$. For $h\neq 0$, define $u_h(t,x) = (u(t,x+h)-u(t,x))/h$. Then $u_h$ satisfies 
$$ \partial_t (u_h)-(u_h)_{xx}=0\quad \text{in } (0,\infty)\times \mathbb{R},\quad u_h=(u_0)_h\quad \text{on } \{t=0\}\times \mathbb{R}. 
$$
</div>

<div>
Choose $\chi$ so that $0\leq \chi\leq 1$, $\chi=0$ in $(-1,1)$, and $\chi=1$ on $(-2,2)^c$. Multiplying $u_h \chi$ and taking integration by part, we get 
\begin{equation}
\begin{aligned}
&\frac{1}{2}\int_{\mathbb{R}} |u_h(t)|^2 \chi \,dx + \int_0^t \int_{\mathbb{R}} |\partial_x (u_h)|^2 \chi \,dx ds \\
&=\frac{1}{2}\int_0^t \int_{\mathbb{R}} |u_h|^2 \chi'' \,dxds+\frac{1}{2}\int_{\mathbb{R}} |u_h(0)|^2 \chi\,dx.
\end{aligned}
\end{equation}
For sufficiently small $h$, we note that $u_h(0,x)\chi(x)=0$ since $\mathrm{supp}\, u_0 \subset (-1,1)$ and $\chi=0$ on $(-1,1)$. Hence it follows that
$$ \frac{1}{2}\int_{\mathbb{R}} |u_h(0)|^2 \chi\,dx=0.$$
Hence by a method of finite difference, we get 
$$ \int_{\mathbb{R}} |u_x|^2 \chi \,dx+\int_0^t \int_{\mathbb{R}} |\partial_{xx} u|^2 \chi \,dxds \leq C \int_0^t \int_{\mathbb{R}} |u_x|^2|\chi''| \,d{x}ds. $$
Moreover, it follows from the energy estimate that 
$$ \int_{\mathbb{R}} |u_x(t)|^2 \chi \,dx+\int_0^t \int_{\mathbb{R}} |\partial_{xx} u|^2 \chi \,dxds \leq C \int_{\mathbb{R}} |u_0|^2 \,d{x}. $$
Hence it follows that $u \in L^\infty((0,\infty);H^1((-2,2)^c))$. Then by induction, we can further show that $u\in L^\infty ((0,\infty);H^k((-3,3)^c))$ for any $k$. 
</div>
 
<div>
In fact, we can obtain better smoothing estimate. It belongs to Gevrey $1/s$-class $G^s$ for $0<s<1$ outside $(-1/2,1/2)$. Choose the following parameters 
$$ x_1 = \frac{3}{8},\quad x_{n+1}=x_n+\frac{c_\sigma}{n^{1+\sigma}},\quad y_n = x_n + \frac{c_\sigma}{100 n^{1+\sigma}},$$
where the constant $c_\sigma$ is chosen so that $c_\sigma \sum_{n=1}^\infty \frac{1}{n^{1+\sigma}}<1/8$. Define $\chi_n$ so that $\chi_n(y)=0$ for $-x_n<y<x_n$, and $\chi_n(y)=1$ for $\{-\infty<y<-y_n\}\cup \{y_n<y<\infty\}$ for $n\geq 1$. Then note that 
$$ \bigcap _{n=1}^\infty \{x_n=1\}\supset \left(-\infty,-\frac{1}{2}\right)\cup\left(\frac{1}{2},\infty\right),$$
$$ \mathrm{supp}\, (\nabla^k \chi_{n+1})\subset \{\chi_n=1\},$$
and 
$$ |\partial_x^j \chi_n|\leq C n^{j(1+\sigma)} \chi_{n-1}.$$
Following a similar argument, we get 
$$ \frac{d}{dt}\int_{\mathbb{R}} |\partial_x^{n+1} u|^2 \chi_{n+1}^2 dy + 2\int_{\mathbb{R}} |\partial_x^{n+2} u|^2 \chi_{n+1}^2 dy=\int_{\mathbb{R}} |\partial_x^{n+1} u|^2 \partial_x^2 (\chi_{n+1}^2)\,dx.$$
We will show that 
$$ \sum_{n=0}^\infty \left(\frac{1}{n!}\right)^{2/s} \Vert{\partial_x^n u}\Vert_{L^2}^2<\infty.$$
</div>
 
<div>
Note that 
$$  \partial_y^2 (\chi_{n+1}^2)\leq C (n+1)^{2(1+\sigma)}\chi_n^2.$$
So it follows that 
\begin{equation}
\begin{aligned}
&\int_{\mathbb{R}}|\partial_x^{n+1} u(t)|^2 \chi_{n+1}^2 d{x}+\int_0^t \int_{\mathbb{R}}|\partial_x^{n+2}u|^2 \chi_{n+1}^2 dxds\\
&\leq C(n+1)^{2(1+\sigma)}\int_0^t \int_{\mathbb{R}}|\partial_x^{n+1}u|^2 \chi_n^2 dxds.
\end{aligned}
\end{equation}
 Since $\sigma<1/s-1$, it follows that
\begin{equation}
\begin{aligned}
&\left(\frac{1}{(n+1)!}\right)^{2/s}\int_{\mathbb{R}}|\partial_x^{n+1} u(t)|^2 \chi_{n+1}^2 d{x}+\left(\frac{1}{(n+1)!}\right)^{2/s}\int_0^t \int_{\mathbb{R}}|\partial_x^{n+2}u|^2 \chi_{n+1}^2 dxds\\
&\leq C\left(\frac{1}{n!}\right)^{2/s}\int_0^t \int_{\mathbb{R}}|\partial_x^{n+1}u|^2 \chi_n^2 dxds.
\end{aligned}
\end{equation} 
</div>
 
<div>
If we set 
\begin{equation}
\begin{aligned}
a_n &=\int_{\mathbb{R}}|\partial_x^{n} u(t)|^2 \chi_{n}^2 d{x},\\
b_n &=\int_0^t\int_{\mathbb{R}}|\partial_x^{n+1} u|^2 \chi_{n+1}^2 d{x}ds,
\end{aligned}
\end{equation} 
then by induction, we have 
$$ b_n \leq C^n (n!)^{2(1+\sigma)}\Vert b_0\Vert_{L^2} $$
and so 
$$ \sum_{n=0}^\infty \left(\frac{1}{(n+1)!}\right)^{2/s}a_{n+1} \leq \Vert{b_0}\Vert_{L^2} \sum_{n=0}^\infty C^n \left(\frac{1}{n!} \right)^{2/s-2(1+\sigma)} .$$
Since $2/s-2(1+\sigma)>0$, the series converges. This implies that 
$$ \sum_{n=0}^\infty \left(\frac{1}{n!}\right)^{2/s}\int_{(-1/2,1/2)^c} |\partial_x^n u(t)|^2 dx<\infty.$$
Hence $u$ belongs to $L^\infty(0,\infty;G^{s}((-1/2,1/2)^c))$. 
</div>

As we can see, the above argument does not work if $s=1$.
