---
layout: post
use_math: true
title:  "On some famous theorem on nontangential maximal functions of harmonic functions (incomplete)"
date:   2021-10-10 10:00:40 
---
  
#### Table of Contents
1. [Introduction](#introduction) 

#### Introduction

Maximal functions are naturally introduced when someone wants to study the pointwise convergence of functions. In particular, nontangential maximal functions are naturally used when we want to analyze a nontangential behavior of a function. 

When I wrote a research paper [[KK19]](https://arxiv.org/abs/1811.12619), it was hard to find a proof of the following theorem.

**Theorem.** Let $\Omega$ be a bounded Lipschitz domain in $\mathbb{R}^n$, $n\geq 2$. Suppose that $u$ is harmonic in $\Omega$ and $u^* \in L^2 (\partial\Omega)$. Then there exists a function $g$ in $L^2(\partial\Omega)$ such that $u\rightarrow g$ nontangentially a.e. on $\partial\Omega$. 

According to some literature, this theorem was shown by Dahlberg. Since I am not familiar with geometric measure theory, it was hard for me to follow the essence of the proof. The purpose of this post is to prove this well-known theorem by using layer potential technique. I want to point out that the proof is not original since the proof is well-known to experts. However, I will write this post for those who are not familiar with the concept `nontangential convergence'. 

The organization of this post is as follows. We first present the role of nontangential maximal function to study the Dirichlet problem for Poisson equation in half-space. 

#### Dirichlet problem for the Poisson equation in half-space
<div>
In this section, we consider the Dirichlet problem for the Poisson equation in $\mathbb{R}^{n+1}_+$, where $\mathbb{R}^{n+1}_+ =\{ (x,y) : x\in \mathbb{R}^n, y>0 \}$. 

For $x\in \mathbb{R}^n$ and $y>0$, we define the <em>Poisson kernel</em> by 
\begin{equation}\nonumber
P_y(x) = \frac{c_n y}{(|x|^2+y^2)^{(n+1)/2}},\quad c_n = \frac{\Gamma((n+1)/2)}{\pi^{(n+1)/2}}. 
\end{equation}
The Poisson kernel has several interesting properties. One of important properties is that $\int_{\mathbb{R}^n} P_y(x)dx=1$ for any $y>0$. Hence by Young's convolution theorem, we see that 
\begin{equation}
\Vert P_y *f \Vert_{L^p}\leq \Vert f \Vert_{L^p}
\end{equation}
for any $1\leq p \leq \infty$. 

For a function $f:\mathbb{R}^n\rightarrow \mathbb{R}$ and $y>0$, we define $u(x,y)=(P_y*f)(x)$ and we call it the *Poisson integral* of $f$.  We write 
\begin{equation}
\nonumber
\Delta u = \sum_{j=1}^n \frac{\partial^2 u}{\partial x_j^2}+ \frac{\partial^2 u}{\partial y^2}.
\end{equation}
Then it is easy to check that for $f\in L^p(\mathbb{R}^n)$, $1\leq p\leq \infty$, then the Poisson integral is harmonic in $\mathbb{R}^{n+1}_+$. 

Since $\int_{\mathbb{R}^n} P_y (x)dx=1$ and $P_y(x)>0$, one can easily see that $(P_y *f)(x)\rightarrow f(x)$ as $y\rightarrow 0+$ if $f$ is sufficiently smooth. However, it is unclear if $f\in L^p$ because of the definition of $L^p$. To discuss the behavior of $u$ as $y\rightarrow 0+$, nontangential maximal function estimate gives an useful information. 
</div>
<strong> Theorem.</strong>  Let $1\leq p \leq \infty$ and $f\in L^p (\mathbb{R}^n)$, and let $\psi$ be a nonnegative, radial, decreasing and integrable function with $\int_{\mathbb{R}^n} \psi dx=1$.

1. <div>$\sup_{\varepsilon>0} |\psi_\varepsilon *f(x)|\leq Mf(x)$, where $M$ is the Hardy-Littlewood maximal operator and $\psi_\varepsilon(x)=\varepsilon^{-n} \psi(x/\varepsilon)$.</div>
2. <div>$\lim_{y\rightarrow 0+} (\psi_\varepsilon *f)(x)=f(x)$ for almost every $x$.</div>
3. <div>If $1\leq p <\infty$, then $(\psi_\varepsilon *f)\rightarrow f$ in $L^p$ as $\varepsilon\rightarrow  0+$. </div>

<div>
Proof. (1)  By scaling and translation invariance, it suffices to show that 
$$ |(\psi * f)(0)|\leq \left(\int_{\mathbb{R}^n} \psi dx \right)Mf(0).$$ 

Set 
$$ \lambda(r)=   \int_{\mathbb{S}^{n-1}} f(r\omega) d\sigma(\omega),\quad \Lambda(r)=\int_0^r \lambda(t)t^{n-1}dt.$$
Since $\psi$ is integrable and decreasing radial function, it follows that 
$$ \int_{r\leq |x|\leq 2r} \psi(x) dx \geq cr^n \psi(r) $$
for some constant $c>0$. Hence 
$$ r^n \psi(r)\rightarrow 0$$
as $r\rightarrow 0+$ or $r\rightarrow \infty$. 

Therefore a change of variable and integration by part give
$$  (\psi*f)(0)=\int_0^\infty \Lambda'(r)\psi(r) dr=-\int_0^\infty \Lambda(r)\psi'(r)dr. $$ 
(of course, we should change improper integral into finite integral...) 

Since 
$$ \Lambda(r)=\int_{B_r} f(y)dy \leq |B_r| Mf(0)= \frac{r^n \sigma(\mathbb{S}^{n-1})}{n} Mf(0), $$
it follows that 
$$ -\int_0^\infty \Lambda(r)\psi'(r)dr \leq -Mf(0)\sigma(\mathbb{S}^{n-1}) \int_0^\infty \frac{r^n}{n} \psi'(r)dr$$
since $\psi'(r)\leq 0$. 

Integration by part and a change of variable give
$$\begin{aligned}   -\sigma(\mathbb{S}^{n-1})\int_0^\infty \frac{r^n}{n} \psi'(r)dr
&=\sigma(\mathbb{S}^{n-1})\int_0^\infty r^{n-1}\psi(r)dr\\
& = \int_{\mathbb{R}^n} \psi(x)dx.
\end{aligned}$$
This implies that 
$$ (\psi*f)(0)\leq \left(\int_{\mathbb{R}^n} \psi(x) dx\right) Mf(0).$$
This completes the proof of (1).

To show (2), suppose first that $1\leq p<\infty$. Define 
$$ \Omega f(x) = \limsup_{\eta\rightarrow 0+} (\psi_\eta * f)(x)-\liminf_{\eta\rightarrow 0+} (\psi_\eta * f)(x).  $$
By (1), we have $\Omega(x)\leq 2Mf(x)$.  If $p=1$, then for any $\eta>0$, it follows from the weak $L^1$-bound of maximal function that 
$$ |\{x : \Omega f(x)>\eta \}| \leq |\{ x : Mf(x)>\eta/2 \}|\leq C\eta^{-1}\Vert f \Vert_{L^1}.   $$
If $1<p<\infty$, then for any $\eta>0$, it follows from the $L^p$-boundedness of maximal function and Chebyshev's inequality that 
\begin{align*} 
|\{ x : \Omega f(x) > \eta \}| &\leq |\{ x : Mf (x)>\eta/2 \}| \\
&\leq C \eta^{-p} \Vert Mf \Vert_{L^p}^p \\
&\leq C \eta^{-p} \Vert f \Vert_{L^p}^p. 
\end{align*}
From these estimate, we prove (2). Let $\varepsilon>0$ be given. Then there exists $f_1 \in C_c^\infty$ such that $f=f_1+f_2$, where $\Vert f_2 \Vert_{L^p}<\varepsilon$. Since $f_1 \in C_c^\infty$, it follows that $f_1 *\varphi_\eta \rightarrow f_1$ as $\eta\rightarrow 0+$. Hence $\Omega f_1=0$.  When $p=1$, there exists a constant $C>0$ such that
$$|\{\Omega f >\alpha\}| \leq |\{\Omega f_2>\alpha\}| \leq \frac{C}{\alpha}\Vert{f_2}\Vert_{L^{1}}\leq \frac{C\eta}{\alpha}  $$
for all $\alpha>0$. Similarly, when $1<p<\infty$, there exists a constant $C>0$ such that
$$|\{\Omega f >\alpha\}| \leq |\{\Omega f_2>\alpha\}| \leq \frac{C}{\alpha^p}\Vert{f_2}\Vert_{L^{p}}^p\leq \frac{C\eta^p}{\alpha^p}  $$
for all $\alpha>0$. Hence if we choose sufficiently small $\eta>0$, then we conclude that 
$$   |\{\Omega f >\alpha\}|=0  $$
for all $\alpha>0$, which proves that $|\{ \Omega f>0 \}|=0$. Hence $\Omega f=0$ a.e. on $\mathbb{R}^n$. This proves that $f*\varphi_\eta\rightarrow f$ a.e. as $\eta\rightarrow 0+$. 

If $p=\infty$, fix a ball $B$. We show that $f*\varphi_\eta\rightarrow f$ a.e. $x\in B$. Let $B_1$ be any other ball which strictly contains $B$, and let $\delta=\mathrm{dist}(B,B_1^c)$. Let $f_1=f\chi_{B_1}$ and $f_2=f-f_1$. Then $f_1 \in L^1$ and $\Omega f_1=0$ a.e. on $\mathbb{R}^d$ by the previous step. Note also  that for $x\in B$, we have 
\begin{align*}
|(f_2 *\varphi_\eta)(x)|&\leq \int_{|y|\geq \delta>0} | f_2(x-y)| |\varphi_\eta(y)|dy\\
&\leq \Vert f \Vert_{L^\infty} \int_{|y|\geq \delta/\eta} |\varphi(y)|dy.
\end{align*}
Since $\varphi \in L^1$, it follows from the absolute continuity that $|(f_2*\varphi_\eta)(x)|\rightarrow 0$ as $\eta\rightarrow 0$. Since $\Omega f\leq \Omega f_1+\Omega f_2$, it follows that $\Omega f=0$ a.e. on $x\in B$. This completes the proof of (2).

(3) follows from the standard mollifier technique which could be found in a standard real analysis textbook.
</div>

#### References
1. E. M. Stein, Singular integrals... 
