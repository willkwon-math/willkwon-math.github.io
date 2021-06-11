---
layout: ordinary
use_math: true 
---

# Research

From Newton's mechanics, many scientists and mathematicians have devoted to studying differential equations to explain the several phenomenon in the natures.  It is a natural to ask whether we can solve the boundary value problems of given partial differential equations. If we know an existence of solution of the problem, one can also ask some properties of solutions that have. 

## Elliptic equations with singular drift terms

For several years, I have devoted to studying unique solvability of linear elliptic equations with singular drift terms  in Sobolev spaces.  To explain the results, let $\Omega$ be a bounded Lipschitz domain in $\mathbb{R}^n$, $n\geq 2$. For a fixed constant $\lambda \geq 0$, we consider the following Dirichlet problems of elliptic equations of   second-order: 
<center>
$(D)\qquad -\mathrm{div}(A \nabla u)+\mathrm{div}(u\mathbf{b})=f\quad \text{in } \Omega\qquad u=0\quad \text{on } \partial\Omega$
</center>
and 
<center>
$(D')\qquad -\mathrm{div}(A \nabla v)-\mathbf{b}\cdot \nabla v =g\quad \text{in } \Omega\qquad v=0\quad \text{on } \partial\Omega$
</center>
Here $A=(a^{ij}):\mathbb{R}^n\rightarrow \mathbb{R}^{n\times n}$ denotes an $n\times n$ real matrix-valued function  which is uniformly elliptic, that is, there exists $0<\delta<1$ such that 
\begin{equation}\label{eq:uniformly-elliptic} 
\delta|\xi|^2 \leq a^{ij}(x)\xi_i \xi_j\quad \text{and}\quad |a^{ij}(x)|\leq \delta^{-1}\quad    \text{for all } x,\xi \in \mathbb{R}^n, 
\end{equation}
$\mathbf{b}=(b^1,b^2,\dots,b^n) : \Omega\rightarrow \mathbb{R}^n$ is a given vector field. Here we follow the usual summation convention for repeated indices.

When $\mathbf{b}$ is zero or a bounded vector field, $L^p$-theory for these equations is well-known by several authors. One might ask $L^p$-theory for unbounded vector field, $\mathbf{b}\in L^q(\Omega;\mathbb{R}^n)$. 

During the master course, I wrote a research article [[KK18]](https://arxiv.org/abs/1811.12619) with my academic advisor Prof. Hyunseok Kim. At the Republic of Korea Air Force Academy, I wrote two research articles [[K20]](https://www.sciencedirect.com/science/article/abs/pii/S0022247X21002444) and [[K21]](https://arxiv.org/abs/2104.01300). 

1. In a joint work with Hyunseok Kim [[KK18]](https://arxiv.org/abs/1811.12619), when $A=I$ and $\mathbf{b} \in L^{n}(\Omega;\mathbb{R}^n)$, we proved $L^{\alpha,p}$-solvability for the problems $(D)$ on arbitrary bounded Lipschitz domains $\Omega$ in $\mathbb{R}^n$, $n\geq 3$ for appropriate $(\alpha,p)\in \mathscr{A}\cap \mathscr{B}$. Here $L^{\alpha,p}(\Omega)$ denotes the Bessel potential spaces over $\Omega$, which generalizes the classical Sobolev spaces $W^{k,p}(\Omega)$. Here $\mathscr{A}$ is the set of admissible pairs $(\alpha,p)$ such that  the Dirichlet problem for the Poisson equation has a unique solution in $L^{\alpha,p}_0(\Omega) =\{ u\in L^{\alpha,p}(\Omega) : u=0\text{ on } \partial\Omega\}$. Also, $\mathscr{B}$ denotes the set of some pairs $(\alpha,p)$ for which $\mathbf{b} \cdot \nabla u \in L^{\alpha-2,p}(\Omega)$ for all $u\in L_0^{\alpha,p}(\Omega)$. Similar result also proved for the problem $(D')$. This result extends the classical result of Jerison-Kenig [[JK95]](https://www.sciencedirect.com/science/article/pii/S0022123685710671). In the same paper, Neumann problems were also considered. 
2. When $A$ satisfies \eqref{eq:uniformly-elliptic} and $\mathbf{b} \in L^{n,\infty}(\Omega;\mathbb{R}^n)$, $n\geq 2$, $\mathrm{div} \mathbf{b} \geq 0$ in $\Omega$,  I proved that if $q>2$, then there exists $\varepsilon>0$ such that if $g\in W^{-1,q}(\Omega)$,  then there exists a unique $v\in W_0^{1,2+\varepsilon}(\Omega)$ of the problem $(D')$. As an application, I proved that if $f\in \bigcap_{q<2} W^{-1,q}(\Omega)$, there exists a unique $u\in \bigcap_{q<2} W_0^{1,q}(\Omega)$ satisfying the problem $(D)$. The result can be found in [[K20]](https://www.sciencedirect.com/science/article/abs/pii/S0022247X21002444).  When $n=2$, this result extends Kim-Tsai [[KT20]](https://epubs.siam.org/doi/abs/10.1137/19M1282969?mobileUi=0&) and Chernobai-Shilkin [[CS19]](https://www.tandfonline.com/doi/abs/10.1080/17476933.2020.1816980). 
