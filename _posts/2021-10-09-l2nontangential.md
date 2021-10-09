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
P_y(x) = \frac{c_n y}{(|x|^2+y)^{(n+1)/2}},\quad c_n = \frac{\Gamma((n+1)/2)}{\pi^{(n+1)/2}}. 
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

To show (2), suppose first that $1\leq p<\infty$ and let $\varepsilon>0$ be given. Since $C_c^\infty$ is dense in $L^p$, there exists $f_1 \in C_c^\infty$ such that $\Vert f-f_1 \Vert_{L^p}<\varepsilon$. Note that $f_1*\psi_\eta \rightarrow f_1$ uniformly as $\eta\rightarrow 0$. 
</div>

#### References
1. E. M. Stein, Singular integrals... 
