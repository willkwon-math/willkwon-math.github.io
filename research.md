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

During the master course, I wrote a research article [[KK18]](https://www.ams.org/journals/tran/2022-375-09/S0002-9947-2022-08730-4/) with my academic advisor Prof. Hyunseok Kim. At the Republic of Korea Air Force Academy, I wrote two research articles [[K20]](https://www.sciencedirect.com/science/article/abs/pii/S0022247X21002444) and [[K21]](https://arxiv.org/abs/2104.01300). 

1. In a joint work with Hyunseok Kim [[KK18]](https://arxiv.org/abs/1811.12619), when $A=I$ and $\mathbf{b} \in L^{n}(\Omega;\mathbb{R}^n)$, we proved $L^{\alpha,p}$--solvability for the problems $(D)$ on arbitrary bounded Lipschitz domains $\Omega$ in $\mathbb{R}^n$, $n\geq 3$ for appropriate $(\alpha,p)\in \mathscr{A}\cap \mathscr{B}$. Here $L^{\alpha,p}(\Omega)$ denotes the Bessel potential spaces over $\Omega$, which generalizes the classical Sobolev spaces $W^{k,p}(\Omega)$. Here $\mathscr{A}$ is the set of admissible pairs $(\alpha,p)$ such that  the Dirichlet problem for the Poisson equation has a unique solution in $L^{\alpha,p}_0(\Omega) =\{ u\in L^{\alpha,p}(\Omega) : u=0\text{ on } \partial\Omega\}$. Also, $\mathscr{B}$ denotes the set of some pairs $(\alpha,p)$ for which $\mathbf{b} \cdot \nabla u \in L^{\alpha-2,p}(\Omega)$ for all $u\in L_0^{\alpha,p}(\Omega)$. Similar result also proved for the problem $(D')$. This result extends the classical result of Jerison-Kenig [[JK95]](https://www.sciencedirect.com/science/article/pii/S0022123685710671). In the same paper, Neumann problems were also considered. 
2. When $A$ satisfies (1) and $\mathbf{b} \in L^{n,\infty}(\Omega;\mathbb{R}^n)$, $n\geq 2$, $\mathrm{div} \mathbf{b} \geq 0$ in $\Omega$,  I proved that if $q>2$, then there exists $\varepsilon>0$ such that if $g\in W^{-1,q}(\Omega)$,  then there exists a unique $v\in W_0^{1,2+\varepsilon}(\Omega)$ of the problem $(D')$. As an application, I proved that if $f\in \bigcap_{q<2} W^{-1,q}(\Omega)$, there exists a unique $u\in \bigcap_{q<2} W_0^{1,q}(\Omega)$ satisfying the problem $(D)$. The result can be found in [[K20]](https://www.sciencedirect.com/science/article/abs/pii/S0022247X21002444).  When $n=2$, this result extends Kim-Tsai [[KT20]](https://epubs.siam.org/doi/abs/10.1137/19M1282969?mobileUi=0&) and Chernobai-Shilkin [[CS19]](https://www.tandfonline.com/doi/abs/10.1080/17476933.2020.1816980). 
3. In [[K21]](https://arxiv.org/abs/2104.01300), I proved that if $2<p<\infty$, $A$ satisfies mean oscillation in small balls and $\mathrm{div} A \in L^{2}(\Omega;\mathbb{R}^2)$, $\Omega$ is a bounded Lipschitz domain in $\mathbb{R}^2$ which has a small Lipschitz constant, and $\mathbf{b} \in L^{2}(\Omega;\mathbb{R}^2)$, then the problem $(D')$ has a unique solution in $W_0^{1,p}(\Omega)$. A similar result was also proved for the problem $(D)$. Results are new even if $A=I$. The results complement Kim-Kim [[KK15]](https://epubs.siam.org/doi/abs/10.1137/14096270X?journalCode=sjmaah) and Kang-Kim [[KK17]](http://www.aimsciences.org/article/doi/10.3934/cpaa.2017038) when $n=2$. Further research should be done to remove an additional assumption on $\mathrm{div} A$. 

## Mathematical Fluid Dynamics: equations from Magnetohydrodynamics

I also worked on the global well-posedness of fluid equations that have fractional dissipations. To explain my result, let us first consider the  generalized [magnetohydrodynamics](https://en.wikipedia.org/wiki/Magnetohydrodynamics) equations:
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

Later, Moffatt considered similar situations by working on magnetic fields. He constructed magnetohydrodyanmics equilibria from ideal MHD equations by letting $t\rightarrow \infty$. This procedure is called a <em>magnetic relaxation</em>. However, his construction has a limitation because of the problem on discontinuity in time variables. Later, Moffatt suggested a model that could lead to a desirable magnetic relaxation:
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

Moffatt introduced this model when $\alpha=1$ and $\eta=0$. When $\nu,\eta>0$, $\alpha=\beta=1$, and $d=2,3$, McCormick-Robinson-Rodrigo [[MRR14]](http://dx.doi.org/10.1007/s00205-014-0760-y) proved global existence of weak solutions of (4). For the two-dimensional case, they also proved uniqueness and regularity of weak solutions. Recently, Ji-Tan [[JT21]](https://www.aimsciences.org/article/doi/10.3934/dcdsb.2020227) proved global existence of strong solutions of (4)  when $d=3$, $\alpha=1$, and $\beta\geq 3/2$.  On the other hand, when $\nu>0$, $\eta=0$, and $\alpha=0$, Brenier [[B14]](https://link.springer.com/article/10.1007/s00220-014-1967-3) proved  global existence of dissipative weak solutions on the two-dimensional torus $\mathbb{T}^2$. When $\nu>0$, $\eta=0$, and $\alpha=1$, Fefferman et.al. [[FMRR14]](https://www.sciencedirect.com/science/article/pii/S0022123614001505?via%3Dihub) proved local existence and uniqueness of strong solutions of (4) on $\mathbb{R}^d$, $d=2,3$.  Recently, when $\nu>0$, $\eta=0$, and $\alpha>d/2+1$, Beekie-Friedlander-Vicol [[BFV21]](https://link.springer.com/article/10.1007/s00220-021-04289-3)  established global existence of strong solutions of (4)  on the torus $\mathbb{T}^d$, $d=2,3$. Moreover, they also investigated 2D stability and 3D instability as well as the long-time behavior of solutions. One natural question is whether we can relax these regularity assumptions on $\alpha$ and $s$ to guarantee the global solution to this Stokes-Magneto system.

In a joint work with Hyunseok Kim [[HK22]](https://arxiv.org/abs/2302.02046), we proved the existence of global weak solutions of the problem for general $\alpha,\beta$ on whole space $\mathbb{R}^d$, $d\geq 2$. More precisely, if $\alpha$, $\beta$ satisfy $1/2<\alpha<(d+1)/2$, $\beta >0$,
and $\min(\alpha+\beta,2\alpha+\beta-1)>d/2$, then we proved the existence of global weak solutions of (4). Moreover, we also proved that weak solutions are unique  if $\beta \geq 1$ and $\min (\alpha+\beta,2\alpha+\beta-1)\geq d/2+1$, in addition.

<div>
In the previous research work, we only proved the uniqueness of weak solutions when $\beta \geq 1$. Even though we can guarantee the existence of weak solutions for $\beta$ below 1, due to the structure that we used, we cannot proceed to guarantee the uniqueness of weak solutions. In the recent joint work with Hantaek Bae and Jaeyong Shin, we proved that when $\alpha$, $\beta$ satisfy $1/2<\alpha<(d+1)/2$, $\beta>1/2$, $\alpha+\beta<d+1$ (and some additional technical conditions if $\alpha>(d+2)/4$), local-in-time mild solutions exist and global-in-time mild solutions exist for sufficiently small initial data which belongs to the natural scaling critical $L^p$-space corresponding to our Stokes-Magneto system. We also proved that $\lim_{t\rightarrow\infty}\Vert {b}(t) \Vert_{L^p}=0$. In the same paper, when $\eta=0$ and on the torus, we proved that a local-in-time strong solution exists for more irregular data and it becomes global when $\alpha\geq d/2+1$ and $s\geq 1$. Our result gives a partial answer on the global existence part given in Question 1 of Beekie-Friedlander-Vicol when $\alpha \geq d/2+1$.
</div>


  
## Mathematical Fluid Dynamics: local regularity theory for Stokes equations

<div>
Recently, I also worked on local regularity theory for Stokes equations. To explain this result, let us consider nonstationary Stokes equations with variable viscosity coefficients:
$$
\partial_t u - a^{ij}(t,x)D_{ij} u + \nabla p = f,\quad \mathrm{div}\, u=g\quad \text{in } U.
$$
Here $a^{ij}(t,x)$ is uniformly elliptic as in the first section. Also, $U$ is a cylindrical domain in $\mathbb{R}^{d+1}$. Besides mathematical interests, such an equation can be used to model non-Newtonian fluids that have thixotropy, i.e., time-dependent shear thinning properties. Also, the equation is also naturally introduced when we introduce Stokes equations on a manifold.
  
In the case of the heat equation, it is easy to show that if $u \in L^2(Q_1)$ is a very weak solution to heat equations $\partial_t u-\Delta u =0$ in $Q_1$, then $u$ is smooth in $Q_1$. Moreover, one can also show that 
$$ \Vert D^2 u \Vert_{L_{2}(Q_{1/2})}\leq N \Vert u \Vert_{L_{2}(Q_1)}.$$
However, it is not easy to verify that such an estimate holds for Stokes equations due to the presence of pressure. This is captured by a well-known example given by Serrin (1962): consider 
$$ u(t,x)=c(t)\nabla \phi(x),\quad p(t,x)=-c(t)\phi(x),$$
where $\phi$ is harmonic. Then $(u,p)$ satisfies 
$$ \partial_t u -\Delta u + \nabla p=0,\quad \mathrm{div} u= 0.$$
Note that we can choose $c$ as an absolutely continuous function. 
</div>

<div>
When $g=0$ and $a^{ij}=\delta^{ij}$, such estimate was first obtained by Chen-Strain-Yau-Tsai (2008) proved that if $1<s,q<\infty$, then 
$$\Vert D^2 u \Vert_{L_{s,q}(Q_{1/2)} \leq N (\Vert u \Vert_{L_{s,1}(Q_1)} + \Vert f \Vert_{L_{s,q}(Q_1)}).$$
holds. Independently, Jin (2013) and Wolf (2015) also proved the validity of such an estimate when $s=q=2$. Later, Dong-Phan (2021) obtained that if $a^{ij}$ is in $VMO_x$, then such regularity estimate is possible even if $g$ is nonzero. However, they need to assume that $u\in \tilde{W}^{1,2}_{s,q}(Q_1)$ to get the desired regularity estimate, where $\tilde{W}^{1,2}_{s,q}(Q_1)=\{ u, Du, D^2 u \in L_{s,q}(Q_1), \partial_t u\in L_1(Q_1)\}$. In the same paper, they also obtained the corresponding results for Stokes equations in divergence form. In this case, the leading coefficient need not be bounded. Observe that these results are a priori results to obtain such regularity results. Recently, Dong-Li (2023) obtained an interior regularity estimate when $s=q$ and $a^{ij}$ is merely measurable in $t$ and Holder continuous in $x$ via level set argument following Caffarelli-Peral, Wang, Byun, etc. 

Another natural question is the validity of such regularity estimates when we impose boundary conditions. Chang-Kang (2020) proved that it is not possible to obtain a gradient estimate for Stokes equations if we impose a no-slip boundary condition due to the non-local effect near the boundary. Very recently, Dong-Kim-Phan (2022) proved that Hessian estimates for Stokes equations in nondivergence form are possible if we impose the Lions boundary conditions, which are special cases of Navier-slip boundary conditions. These results are also a priori similar to Dong-Phan (2021). Very recently, Chen-Liang-Tsai proved that gradient estimate for very weak solutions is possible if we impose the Navier boundary condition, $d=3$,  $a^{ij}=\delta^{ij}$, and $g=0$.

In the joint work with Hongjie Dong, we proved that ....
</div>
....
