---
layout: ordinary
use_math: true 
---

# Research

From Newton’s mechanics, many scientists and mathematicians have devoted to studying differential equations to explain several phenomena in the nature.  It is  natural to ask whether we can solve boundary value problems of given partial differential equations. If we know an existence of solution of the problem, one can also ask some properties of solutions that have. 

## Elliptic equations with singular drift terms

For several years, I have devoted to studying unique solvability of linear elliptic equations with singular drift terms  in Sobolev spaces.  To explain the results, let $\Omega$ be a bounded Lipschitz domain in $\mathbb{R}^n$, $n\geq 2$. We consider the following Dirichlet problems of elliptic equations of   second-order: 
\begin{equation}\tag{$D$}
-\mathrm{div}(A \nabla u)+\mathrm{div}(u\mathbf{b})=f\quad \text{in } \Omega\qquad u=0\quad \text{on } \partial\Omega 
\end{equation}
and 
\begin{equation}\tag{$D'$}
-\mathrm{div}(A \nabla v)-\mathbf{b}\cdot \nabla v =g\quad \text{in } \Omega\qquad v=0\quad \text{on } \partial\Omega
\end{equation}
Here $A=(a^{ij}):\mathbb{R}^n\rightarrow \mathbb{R}^{n\times n}$ denotes an $n\times n$ real matrix-valued function  which is uniformly elliptic, that is, there exists $0<\delta<1$ such that 
\begin{equation}
\delta|\xi|^2 \leq a^{ij}(x)\xi_i \xi_j\quad \text{and}\quad |a^{ij}(x)|\leq \delta^{-1}\quad    \text{for all } x,\xi \in \mathbb{R}^n, 
\end{equation}
$\mathbf{b}=(b^1,b^2,\dots,b^n) : \Omega\rightarrow \mathbb{R}^n$ is a given vector field. Here we follow the usual summation convention for repeated indices.

When $\mathbf{b}$ is zero or a bounded vector field, $L^p$-theory for these equations is well-known by several authors. One might ask $L^p$-theory for unbounded vector field, $\mathbf{b}\in L^q(\Omega;\mathbb{R}^n)$. 

During the master course, I wrote a research article [[KK18]](https://arxiv.org/abs/1811.12619) with my academic advisor Prof. Hyunseok Kim. At the Republic of Korea Air Force Academy, I wrote two research articles [[K20]](https://www.sciencedirect.com/science/article/abs/pii/S0022247X21002444) and [[K21]](https://arxiv.org/abs/2104.01300). 

1. In a joint work with Hyunseok Kim [[KK18]](https://arxiv.org/abs/1811.12619), when $A=I$ and $\mathbf{b} \in L^{n}(\Omega;\mathbb{R}^n)$, we proved $L^{\alpha,p}$--solvability for the problems $(D)$ on arbitrary bounded Lipschitz domains $\Omega$ in $\mathbb{R}^n$, $n\geq 3$ for appropriate $(\alpha,p)\in \mathscr{A}\cap \mathscr{B}$. Here $L^{\alpha,p}(\Omega)$ denotes the Bessel potential spaces over $\Omega$, which generalizes the classical Sobolev spaces $W^{k,p}(\Omega)$. Here $\mathscr{A}$ is the set of admissible pairs $(\alpha,p)$ such that  the Dirichlet problem for the Poisson equation has a unique solution in $L^{\alpha,p}_0(\Omega) =\{ u\in L^{\alpha,p}(\Omega) : u=0\text{ on } \partial\Omega\}$. Also, $\mathscr{B}$ denotes the set of some pairs $(\alpha,p)$ for which $\mathbf{b} \cdot \nabla u \in L^{\alpha-2,p}(\Omega)$ for all $u\in L_0^{\alpha,p}(\Omega)$. Similar result also proved for the problem $(D')$. This result extends the classical result of Jerison-Kenig [[JK95]](https://www.sciencedirect.com/science/article/pii/S0022123685710671). In the same paper, Neumann problems were also considered. 
2. When $A$ satisfies (1) and $\mathbf{b} \in L^{n,\infty}(\Omega;\mathbb{R}^n)$, $n\geq 2$, $\mathrm{div} \mathbf{b} \geq 0$ in $\Omega$,  I proved that if $q>2$, then there exists $\varepsilon>0$ such that if $g\in W^{-1,q}(\Omega)$,  then there exists a unique $v\in W_0^{1,2+\varepsilon}(\Omega)$ of the problem $(D')$. As an application, I proved that if $f\in \bigcap_{q<2} W^{-1,q}(\Omega)$, there exists a unique $u\in \bigcap_{q<2} W_0^{1,q}(\Omega)$ satisfying the problem $(D)$. The result can be found in [[K20]](https://www.sciencedirect.com/science/article/abs/pii/S0022247X21002444).  When $n=2$, this result extends Kim-Tsai [[KT20]](https://epubs.siam.org/doi/abs/10.1137/19M1282969?mobileUi=0&) and Chernobai-Shilkin [[CS19]](https://www.tandfonline.com/doi/abs/10.1080/17476933.2020.1816980). 
3. In [[K21]](https://arxiv.org/abs/2104.01300), I proved that if $2<p<\infty$, $A$ satisfies mean oscillation in small balls and $\mathrm{div} A \in L^{2}(\Omega;\mathbb{R}^2)$, $\Omega$ is a bounded Lipschitz domain in $\mathbb{R}^2$ which has a small Lipschitz constant, and $\mathbf{b} \in L^{2}(\Omega;\mathbb{R}^2)$, then the problem $(D')$ has a unique solution in $W_0^{1,p}(\Omega)$. A similar result was also proved for the problem $(D)$. Results are new even if $A=I$. The results complement Kim-Kim [[KK15]](https://epubs.siam.org/doi/abs/10.1137/14096270X?journalCode=sjmaah) and Kang-Kim [[KK17]](http://www.aimsciences.org/article/doi/10.3934/cpaa.2017038) when $n=2$. Further research should be done to remove an additional assumption on $\mathrm{div} A$. 

## Mathematical Fluid Dynamics

Recently, I worked on global well-posedness of fluid equations that have fractional dissipations. To explain my result, let us first consider the  generalized [magnetohydrodynamics](https://en.wikipedia.org/wiki/Magnetohydrodynamics) equations:
<div>
\begin{equation}
\left\{\begin{aligned}
\partial_t u -\nu\Lambda^{2\alpha}u+(u\cdot\nabla)u+\nabla p &=(b\cdot \nabla)b,\\\
\partial_t b -\eta\Lambda^{2\beta}b + (u\cdot \nabla)b &=(b\cdot\nabla)u,\\
\mathrm{div}\, u =\mathrm{div}\, b&=0,\\
u=u_0,\quad b=b_0&
\end{aligned}
\right.
\end{equation}
</div>
Here $u:\mathbb{R}^d\times (0,\infty)\rightarrow \mathbb{R}^d$ denotes the velocity field and the magnetic field, respectively. For $s>0$, $\Lambda^s$ denotes the fractional Laplacian which is defined by the Fourier transform:
<div>
\begin{equation}
\widehat{\Lambda^s f}(\xi)=|\xi|^s \hat{f}(\xi).
\end{equation}
</div>
When $\alpha=\beta=1$, the system is reduced to the classical MHD equation which was first introduced by Hannes Alfvén to describe the fluid of motions that were induced by magnetic fields. 

Many researchers have devoted themselves to establishing well-posedness theory and regularity properties of solutions to the equation. Duvaut-Lions [[DL72]](https://link.springer.com/article/10.1007/BF00250512) proved the existence of weak solutions to the equation. Later, the result was extended by Wu [[W03]](https://www.sciencedirect.com/science/article/pii/S0022039603002341) for general $\alpha$ and $\beta$. 

Starting from Arnol'd pioneering work, many researchers studied differential equations via dynamical points of view. It is natural to ask a equilibrium point of the corresponding dynamical systems. Arnol'd considered incompressible Euler equations that are regarded as a geodesic equations to find a fixed point of the equations, which is a steady Euler equation. 

Later, Moffatt considered similar situations by working on magnetic fields. He constructed magnetohydrodyanmics equilibria from ideal MHD equations by letting $t\rightarrow \infty$. This procedure is called a <em>magnetic relaxation</em>. However, his construction has a limitation because of the problem on discontinuity in time variables.
<div>
\begin{equation}
\left\{\begin{aligned}
\partial_t u -\nu\Lambda^{2\alpha}u+(u\cdot\nabla)u+\nabla p &=(b\cdot \nabla)b,\\\
\partial_t b -\eta\Lambda^{2\beta}b + (u\cdot \nabla)b &=(b\cdot\nabla)u,\\
\mathrm{div}\, u =\mathrm{div}\, b&=0,\\
u=u_0,\quad b=b_0&
\end{aligned}
\right.
\end{equation}
</div>

(Writing) 
