---
layout: post
comments: true
use_math: true
title:  "A representation of functions $f$ in negative parabolic Sobolev spaces on bounded domain"
date:   2023-07-04 10:00:40 
---
 

<div>
While I am preparing new paper, I found that I need to use the parabolic analogue result of the following proposition.

<blockquote>
 <strong>Proposition.</strong> Let $\Omega$ be a bounded domain in $\mathbb{R}^d$, $d\geq 2$ and $1<p<\infty$. If $f\in W^{-1}_{p}(\Omega)$, then there exists $\mathbf{F} \in L_p(\Omega)$ such that $f=\mathrm{div}\,\mathbf{F}$ in $\Omega$, i.e.,
                                                                                                     $$\left<f,\varphi \right>=-\int_\Omega \mathbf{F}\cdot\nabla \varphi$$
   for all $\varphi \in C_0^\infty(\Omega)$.
</blockquote>
</div>
  Proof of this fact requires Riesz representation theorem on $W^{-1}_p(\Omega)$ and Calderon-Zygmund estimates for Poisson equations, see Kim-Tsai [[Lemma 3.9,KT20]](https://arxiv.org/pdf/1811.03201.pdf)  A similar strategy also works for negative parabolic Sobolev spaces: recall that for $1< s,q<\infty$, we define 
$$ \mathbb{H}^{-1}_{s,q}((S,T)\times \Omega) = \{ u : u=f+\mathrm{div} F\quad\text{in } (S,T)\times \Omega \}.$$    

<blockquote>
<strong>Proposition.</strong> Let $\Omega$ be a bounded domain in $\mathbb{R}^d$, $d\geq 2$ and $1<s,q<\infty$. If $u\in \mathbb{H}^{-1}_{s,q}((S,T)\times \Omega)$, then there exists $G\in L_{s,q}((S,T)\times \Omega)$ satisfying 
$$ u= \mathrm{div}\,G$$
                                                                                                   and 
                                                                                                   $$\Vert G\Vert_{s,q}\leq C \Vert{u}\Vert_{\mathbb{H}^{-1}_{s,q}}.$$
</blockquote>
<div>
Proof. The idea is essentially the same with some modification. Since $\Omega$ is bounded, choose $R>0$ so that $\Omega \subset B_{2R}$. Fix a.e. $t\in (S,T)$. Then there exists a unique $v(t)\in\mathring{W}^1_q(B_{2R})\cap W^{2}_q(B_{2R})$ satisfying 
$$ -\Delta v(t) = f \quad \text{in } B_{2R}\quad v(t)=0\quad \text{on } \partial B_{2R}.$$
A bit problematic one is that it is not clear whether $(t,x)\mapsto v(t,x)$ is measurable. To handle this issue, we use a Green function of $-\Delta$. Let $G$ be a Green function of $-\Delta$ on $B_{2R}$. Then 
$$v(t,x)=\int_{B_{2R}} G(x,y) f(t,y)dy.$$
From this representation formula, it is easy to show that $v$ is measurable in $(t,x)$. Define 
$$ G(t,x) = \nabla_x v(t,x)|_{\Omega} + F(t,x).$$
Then it is easy to show that 
$$ \mathrm{div}\, G = f+\mathrm{div}\, F=u\quad\text{in } (S,T)\times \Omega \text{and}\quad \Vert G\Vert_{L_{s,q}((S,T)\times \Omega)}\leq N (\Vert{f}\Vert_{L_{s,q}((S,T)\times \Omega)}+\Vert{G}\Vert_{L_{s,q}((S,T)\times \Omega)}),$$
 where the constant $N$ depends on the diameter of $\Omega$, $s$, $q$, and $d$. This completes the proof.
</div>
