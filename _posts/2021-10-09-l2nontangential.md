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

#### Dirichlet problem for Poisson equation in half-space

For $x\in \mathbb{R}^n$ and $y>0$, we define the *Poisson kernel* by 
$$P_y(x) = \frac{c_n y}{(|x|^2+y)^{(n+1)/2}},\quad c_n = \frac{\Gamma((n+1)/2)}{\pi^{(n+1)/2}}.$$

For $1\leq p\leq \infty$ and $f\in L^p(\mathbb{R}^n)$, we define the *Poisson integral* of $f$ by 
$$u(x,y)=(P_y * f)(x).$$

In this section, we prove the following theorem.

 **Theorem.** Suppose that $f\in L^p(\mathbb{R}^n)$, $1\leq p\leq \infty$, and let $u(x,y)$ be its Poisson integral. Then 

1. $\sup_{y>0} |u(x,y)|\leq Mf(x)$, where $Mf$ is the Hardy-Littlewood maximal function of $f$.
2.  $\lim_{y\rightarrow 0+} u(x,y)=f(x)$ for almost every $x$.
3. If $p<\infty$, then $u(\cdot,y)\rightarrow f$ in $L^p$ as $y\rightarrow 0+$. 



#### References
1. E. M. Stein, Singular integrals... 
