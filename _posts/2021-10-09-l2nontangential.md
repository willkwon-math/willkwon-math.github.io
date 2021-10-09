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

In this section, we consider the Dirichlet problem for the Poisson equation in $\mathbb{R}^{n+1}_+$, where $\mathbb{R}^{n+1}_+ =\{ (x,y) : x\in \mathbb{R}^n, y>0 \}$. 

For $x\in \mathbb{R}^n$ and $y>0$, we define the *Poisson kernel* by 
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

** Theorem. ** Let $1\leq p \leq \infty$ and $f\in L^p (\mathbb{R}^n)$, and let $u(x,y)$ be its Poisson integral. 

1. $\sup_{y>0} |u(x,y)|\leq Mf(x)$, where $M$ is the Hardy-Littlewood maximal operator.
2. $\lim_{y\rightarrow 0+} u(x,y)=f(x)$ for almost every $x$.
3. If $1\leq p <\infty$, then $u(\cdot,y)\rightarrow f$ in $L^p$ as $y\rightarrow 0+$. 



 

#### References
1. E. M. Stein, Singular integrals... 


Test 
\[  a=b \] 

#### References
1. E. M. Stein, Singular integrals... 
