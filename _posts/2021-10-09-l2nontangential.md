---
layout: post
use_math: true
title:  "On some famous theorem on nontangential maximal functions of harmonic functions (incomplete)"
date:   2021-10-10 10:00:40 
---
  
{:toc}

# Introduction

Maximal functions are naturally introduced when someone wants to study the pointwise convergence of functions. In particular, nontangential maximal functions are naturally used when we want to analyze a nontangential behavior of a function. 

When I wrote a research paper [[KK19]](https://arxiv.org/abs/1811.12619), it was hard to find a proof of the following theorem.

**Theorem 1.** Let $\Omega$ be a bounded Lipschitz domain in $\mathbb{R}^n$, $n\geq 2$. Suppose that $u$ is harmonic in $\Omega$ and $u^* \in L^2 (\partial\Omega)$. Then there exists a function $g$ in $L^2(\partial\Omega)$ such that $u\rightarrow g$ nontangentially a.e. on $\partial\Omega$. 

According to some literature, this theorem was shown by Dahlberg. Since I am not familiar with geometric measure theory, it was hard for me to follow the essence of the proof. The purpose of this post is to prove this well-known theorem by using layer potential technique. I want to point out that the proof is not original since the proof is well-known to experts. However, I will write this post for those who are not familiar with the concept `nontangential convergence'. 

The organization of this post is as follows. We first present the role of nontangential maximal function to study the Dirichlet problem for Poisson equation in half-space. 

# Dirichlet problem for the Poisson equation in half-space
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
<blockquote>
<strong> Theorem 2.</strong>  Let $1\leq p \leq \infty$ and $f\in L^p (\mathbb{R}^n)$, and let $\psi$ be a nonnegative, radial, decreasing and integrable function with $\int_{\mathbb{R}^n} \psi dx=1$.

1. <div>$\sup_{\varepsilon>0} |\psi_\varepsilon *f(x)|\leq Mf(x)$, where $M$ is the Hardy-Littlewood maximal operator and $\psi_\varepsilon(x)=\varepsilon^{-n} \psi(x/\varepsilon)$.</div>
2. <div>$\lim_{y\rightarrow 0+} (\psi_\varepsilon *f)(x)=f(x)$ for almost every $x$.</div>
3. <div>If $1\leq p <\infty$, then $(\psi_\varepsilon *f)\rightarrow f$ in $L^p$ as $\varepsilon\rightarrow  0+$. </div>
</blockquote>

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
Since $\varphi \in L^1$, it follows from the absolute continuity that $|(f_2*\varphi_\eta)(x)|\rightarrow 0$ as $\eta\rightarrow 0$. Since $\Omega f\leq \Omega f_1+\Omega f_2$, it follows that $\Omega f=0$ a.e. on $x\in B$. This completes the proof of (2).</br>

(3) follows from the standard mollifier technique which could be found in a standard real analysis textbook.
</div>
<hr>
<div>
It is easy to see that $P_1 (x)$ satisfies the desired property of $\psi$ in the above theorem. Also, $P_y(x)=y^{-n}P_1(x/y)$. Hence we conclude that the Poisson integral of $f \in L^p$ satisfies the following Dirichlet problem in $\mathbb{R}^{n+1}_+$:
$$ \Delta u=0\quad \text{in } \mathbb{R}^{n+1}_+,\quad u=f\quad \text{on } \mathbb{R}^{n}. $$
Here we interpret the boundary condition as 
$$ \lim_{y\rightarrow 0+} u(x,y)=f(x)\quad \text{a.e. on } x\in \mathbb{R}^n.$$
</div>


# Lipschitz domains

In this section, we list several well-known facts regarding Lipschitz domains that will be used in the next section. 

<div>
We say that a domain $\Omega$ is a Lipschitz domain if for each $q\in \partial\Omega$, there exist a rectangular coordinate system $(x,s)$, $x\in \mathbb{R}^{n-1}$, $s\in \mathbb{R}$, a neighborhood, $U_q \subset \mathbb{R}^n$ containing $q$ and a function $\varphi_q = \varphi : \mathbb{R}^{n-1}\rightarrow \mathbb{R}$ such that 
</div>
1. <div>There exists a constant $C>0$ such that $|\varphi(x)-\varphi(y)|\leq C|x-y|$ for all $x,y \in \mathbb{R}^{n-1}$,</div>
2. <div>$U\cap \Omega = \{ (x,s): x>\varphi(x)\}\cap U$.</div> 

The coordinate systems may always be taken to be a rotation and translation of the standard rectangular coordinates for $\mathbb{R}^n$. 

<div>
By a cylinder $Z_r(x)$, we mean an open, right circular, doubly truncated cylinder centered at $x\in \mathbb{R}^n$ with radius equal to $r$. A coordinate cylinder $Z=Z_r(x)$, $x\partial\Omega$, will be defined by the following properties
</div>

1. The bases of $Z$ have positive distance from $\partial\Omega$.
2. There is a rectangular coordinate system for $\mathbb{R}^n$, $(x,s)$, $x\in \mathbb{R}^{n-1}$, $s\in \mathbb{R}$, with $s$-axis containing the axis of $Z$.
3. <div> There is an associated function $\varphi=\varphi_Z:\mathbb{R}^{n-1}\rightarrow \mathbb{R}$ that is Lipschitz, i.e., $|\varphi(x)-\varphi(y)|\leq C |x-y|$, $C=C_Z<\infty$ for all $x, y \in \mathbb{R}^{n-1}$. </div>
4. $Z\cap \Omega = Z\cap \{(x,s) : s >\varphi(x)\}$
5. $Q=(0,\varphi(0))$

  <div>The pair $(Z,\varphi)$ is called a <em>coordinate pair</em>. For any positive number, $\nu$, $\nu Z_r(q)$ will denote the cylinder $\{x\in \mathbb{R}^n : q+(x-q)/\nu \in Z \}$, i.e., the dilation of $Z$ about $q$ by a factor $\nu$. </div><br>

<div>
Since $\Omega$ is a bounded Lipschitz domain, it follows from the compactness of $\partial\Omega$ that we can cover the boundary by finitely many coordinate cylinders, say $Z_1$, $Z_2$, ..., $Z_N$. We may choose such cylinders by enlarging these for a later purpose. We also choose our coordinate functions $\varphi_j$ to have compact support in $\mathbb{R}^{n-1}$. Also, there exists a number $M>0$ such that $\max_{1\leq j\leq N} \Vert \nabla \varphi_j \Vert_{L^\infty} \leq M$. The smallest such number is called the Lipschitz constant for $\Omega$.
</div><br>

To discuss the nontangential behavior of functions, it is useful to consider cones associated to the domains since we are working on Lipschitz domains. <br>

<div>
By a cone, it is an open, circular, doubly truncated cone with two non-empty, convex components. If $q\in \partial\Omega$, $\Gamma(q)$ will denote a cone with vertex at $q$ and one component in $\Omega$ and the other in $\mathbb{R}^n\setminus \overline{\Omega}$. The component interior to $\Omega$ will be denoted by $\Gamma_i(q)$ and the component exterior to $\overline{\Omega}$ is denoted by $\Gamma_e(q)$. 
</div>
  
<br>

<div>
  We say that a family of cones $\{\Gamma(q) : q\in \partial\Omega \}$ is <em>regular</em> if there is a finite covering of $\partial\Omega$ by coordinate cylinders as described above, such that for each <div> $(Z_r,\varphi)$, there are three cones $\alpha,\beta$, and $\gamma$, each with vertex at the origin and axis along the axis of $Z$ such that 
$$ \alpha \subset \overline{\beta}\setminus \{0\}\subset \gamma$$ 
and for all $(x,\varphi(x))=q\in (4/5)Z^*\cap \partial\Omega$, 
$$ \alpha + q \subset \Gamma(q)\subset \overline{\Gamma(q)}\setminus \{q\}\subset \beta +q, $$ 
$$(\gamma+q)_i \subset \Omega \cap Z^*,\quad \text{and}\quad (\gamma+q)_e \subset Z^*\cap \overline{\Omega}$$

</div>
  
<br>

<div>
Given a function $u$, we define $u^*$, $u^*_i$, $u^*_e$ by 
\begin{align*}
u^*(z) &=N(u,\Gamma)(z)=\sup_{x\in \Gamma(z)}|u(x)|,\\
u^*_i(z) &=N(u,\Gamma_i)(z)=\sup_{x\in \Gamma_i(z)}|u(x)|,\\
u^*_e(z) &=N(u,\Gamma_e)(z)=\sup_{x\in \Gamma_e(z)}|u(x)|
\end{align*}
for $z\in \partial\Omega$. We call these functions as nontangential maximal functions. 
</div>
  
 <br>

Finally, we end this section by introducing well-known approximation scheme of Lipschitz domains.<br> 
  
<div>
<blockquote>
<strong> Theorem 3. </strong> Let $\Omega$ be a bounded Lipschitz domain in $\mathbb{R}^n$, $n\geq 2$. Then the following hold:
  <ol>
<li>There is a regular family of cones $\{\Gamma\}$ for $\Omega$ as described in the above.</li>
<li> There is a sequence of $C^\infty$ domains, $\Omega_j\subset \Omega$ and homeomorphisms, $\Lambda_j:\partial\Omega\rightarrow \partial\Omega_j$ such that $\sup_{z\in \partial\Omega} | z-\Lambda_j(z)|\rightarrow 0$ as $j\rightarrow \infty$ and for all $j$ and all $z\in \partial\Omega$, $\Lambda_j(z)\in \Gamma_i(z)$, </li>
<li>  There is a covering of $\partial\Omega$ by coordinate cylinders, $Z$, so that given a coordinate pair $(Z,\varphi)$, then $Z^*\cap\partial\Omega_j$ is given for each $j$ as the graph of a $C^\infty$ function $\varphi_j$ such that $\varphi_j\rightarrow \varphi$ uniformly, $\Vert \nabla \varphi_j \Vert_{L^\infty} \leq \Vert \nabla \varphi \Vert_{L^\infty}$, and $\nabla \varphi_j\rightarrow \nabla \varphi$ pointwise a.e. and in every $L^q(Z^*\cap \mathbb{R}^{n-1})$, $1\leq q<\infty$.  </li>
<li>  There are positive functions $\omega_j : \partial\Omega \rightarrow \mathbb{R}_+$ bounded away from zero and infinity uniformly in $j$ such that for any measurable set $E\subset \partial\Omega$, $\int_E \omega_j d\sigma=\int_{\Lambda_j(E)} d\sigma_j$, and so that $\omega_j\rightarrow 1$ pointwise a.e. and in every $L^q(\partial\Omega)$, $1\leq q<\infty$. </li>
<li>  The normal vectors to $\Omega_j$, $N(\Lambda_j(z))$ converges pointwise a.e. and in every $L^q(\partial\Omega)$, $1\leq q<\infty$, to $N(z)$. An analogous statement holds for locally defined tangent vectors. </li>
<li>  There exist $C^\infty$ vector fields $\mathbf{h}$, in $\mathbb{R}^n$ such that for all $j$ and $z\in \partial\Omega$, $\left<\mathbf{h}(\Lambda_j(z)),N(\Lambda_j(z)) \right>\geq C>0$, where $C$ depends only on $\mathbf{h}$ and the Lipschitz constant for $\Omega$.  </li>
</ol>
</blockquote>
  </div>

 Proof of the above approximation scheme can be found in the Ph.D. dissertation of Verchota. <br>
  
# Single and double layer potentials

<div>
In this section, we define single and double layer potentials that are crucial to discuss $L^p$-solvability for Dirichlet and Neumann problems for the Poisson equation on Lipschitz domains. 

Let $\Gamma$ be the fundamental solution of the Laplacian defined by 
\begin{equation}
\Gamma(x)=\begin{cases}
-\frac{1}{2\pi} \log |x|,&\quad (n=2),\\
\frac{1}{n(n-2)\omega_n} \frac{1}{|x|^{n-2}},&\quad (n\geq 3),
\end{cases}
\end{equation}
where $\omega_n$ is the Euclidean volume of the unit ball in $\mathbb{R}^n$. Recall the Green formula that 
$$ \int_\Omega u\Delta v-v\Delta u dy =\int_{\partial\Omega} u \frac{\partial v}{\partial \nu}-v\frac{\partial u}{\partial \nu} d\sigma,$$
where  $\nu$ is the unit normal to the boundary $\partial\Omega$, $d\sigma$ is the surface measure on $\partial\Omega$  If we assume that $u$ is harmonic in $\Omega$ and $v(y)=\Gamma(x-y)$, then by the Green formula on $\Omega\setminus B_\varepsilon(x)$, we have 
$$ \int_{\Omega\setminus B_\varepsilon(x)} u(y)\Delta \Gamma(x-y)dy=\int_{\partial(\Omega\setminus B_{\varepsilon(x)})} u(y) \frac{\partial}{\partial \nu_y}\Gamma(x-y) - \Gamma(x-y)\frac{\partial u}{\partial \nu_y}(y)d\sigma.$$
Letting $\varepsilon \rightarrow 0$, we get 
\begin{equation}\label{eq:green-identity-potential} -u(x)=\int_{\partial\Omega} u(y)\frac{\partial }{\partial \nu_y}\Gamma(x-y)-\Gamma(x-y) \frac{\partial u}{\partial \nu_y}(y)d\sigma(y).
\end{equation}
This identity motivates us to define the following operators 
$$ \mathcal{S}f(x)=\int_{\partial\Omega} \Gamma(x-y)f(y)d\sigma(y),\quad x\in \Omega$$
  and 
$$ \mathcal{D}f(x)=\int_{\partial\Omega} \frac{\partial}{\partial \nu_y}\Gamma(x-y)f(y)d\sigma(y),\quad x\in \Omega.$$
We call $\mathcal{S}f$ the single layer potential of $f$ and $\mathcal{D}f$ the double layer potential of $f$.

Observe that 
$$ \frac{\partial}{\partial \nu_y}\Gamma(x-y) =\frac{(x-y)\cdot \nu(y)}{n\omega_n |x-y|^n}. $$
Then the double layer potential operator is given by 
$$  \mathcal{D}f(x)=\frac{1}{n\omega_n}\int_{\partial\Omega} \frac{(x-y)\cdot \nu(y)}{|x-y|^n} f(y)d\sigma(y). $$

To investigate the boundary behavior of the double layer potential operators, for each $\varepsilon>0$, we define 
$$ K_\varepsilon f(x) =\frac{1}{n\omega_n} \int_{y\in \partial\Omega, |x-y|>\varepsilon} \frac{(x-y)\cdot \nu(y)}{|x-y|^n} f(y)d\sigma(y) $$
for $x\in \partial\Omega$. 
</div>
<div>
The following theorem was first shown by Calderon and later by Coifman-Meyer-McIntosh.
<blockquote>

<strong>Theorem 4. </strong> Suppose that $\varphi:\mathbb{R}^{n-1}\rightarrow \mathbb{R}$ is Lipschitz with compact support. For $x,y\in \mathbb{R}^{n-1}$, $x\neq y$, put 
$$ k_j(x,y)= \frac{x_j-y_j}{(|x-y|^2+|\varphi(x)-\varphi(y)|^2)^{n/2}},\quad j=1,2,\dots,n-1 $$
and 
$$ k_n(x,y)=\frac{\varphi(x)-\varphi(y)}{(|x-y|^2 +|\varphi(x)-\varphi(y)|^2)^{n/2}}.$$
Letting $k(x,y)$ stand for any $k_j$, $1\leq j,\leq n$, define 
$$T_\varepsilon f(x)=\int_{|x-y|>\varepsilon} k(x,y)f(y)dy,\quad \varepsilon>0.$$
Then 
$$ T_*f(x)=\sup_{\varepsilon>0}|T_\varepsilon f(x)|$$ 
is a bounded operator on $L^p(\mathbb{R}^{n-1})$, $1<p<\infty$. Moreover, we have 
$$ \Vert T_* f \Vert_{L^p} \leq C \Vert f \Vert_{L^p}, $$
where the constant $C$ depends only on  $n$, $p$, and $\Vert \nabla \varphi \Vert$. 

</blockquote>

As an application of the above theorem, we present the $L^p$-boundedness of truncated boundary double layer potential operator.

<blockquote>


<strong> Theorem 5. </strong> Let $1<p<\infty$. Then there exists a constant $C>0$ depending only on $n$, $p$, and the Lipschitz character of $\Omega$ such that 
$$ \left\Vert {\sup_{\varepsilon>0} |K_\varepsilon f|} \right\Vert_{L^p(\partial\Omega)}\leq C \Vert f \Vert_{L^p(\partial\Omega)}$$
for all $f\in C(\partial\Omega)$. 
</blockquote>


Let $(Z_i,\varphi_i)$ be a coordinate pair associated to the Lipschitz domain $\Omega$ in $\mathbb{R}^n$, $n\geq 2$. Choose a partition of unity $\{\zeta_i\}_{i=1}^m$ so that $0\leq \zeta_i\leq 1$, smooth, finite partition of unity subordinate to the $Z_i$'s. Clearly, 
\[  K_\varepsilon f(x)=\frac{1}{n\omega_n}\sum_{i=1}^m  \int_{y \in \partial\Omega,|x-y|>\varepsilon} \frac{(x-y)\cdot \nu(y)}{|x-y|^n}\zeta_i(y)f(y)d\sigma(y).  \]
Since $(Z_i,\varphi_i)$ is a coordinate pair, it follows that 
\begin{align*}
&K_{\varepsilon}f(x)\\
&=\frac{1}{n\omega_n} \sum_{i=1}^m \int_{|x'-y'|^2+|\varphi_i(x')-\varphi_i(y')|^2 >\varepsilon^2} \frac{\varphi_i(x')-\varphi_i(y')-\nabla \varphi_i(y')\cdot (x'-y')}{|x-y|^n} \zeta_i(y',\varphi_i(y'))f(y',\varphi_i(y'))\sqrt{1+|\nabla \varphi_i(y')|^2}dy'.
\end{align*}
Hence if we define 
$$ K_i(x',y')= \frac{\varphi_i(x')-\varphi_i(y')-\nabla \varphi_i(y')\cdot (x'-y')}{(|x'-y'|^2+|\varphi_i(x')-\varphi_i(y')|^2)^{n/2}},$$
then 
$$ K_\varepsilon f(x)=\frac{1}{n\omega_n} \sum_{i=1}^n \int_{U_\varepsilon^i(x')} K_i(x',y')g(y')dy',$$
where 
$$ g_i(y')=\zeta_i(y',\varphi_i(y'))f(y',\varphi_i(y'))\sqrt{1+|\nabla \varphi_i(y')|^2} $$
and 
$$ U_{\varepsilon}^i(x')=\{y' : |x'-y'|^2+|\varphi_i(x')-\varphi_i(y')|^2>\varepsilon^2\}. $$
Note that $y'\in U_{\varepsilon}^i(x)$ implies $|x'-y'|>\varepsilon /\sqrt{1+\Vert{\nabla \varphi_i}\Vert_{L^\infty}^2}$. 
Furthermore, we define 
$$ V_\varepsilon^i(x')=\{ y' : |x'-y'|>\varepsilon/\sqrt{1+\Vert \nabla \varphi_i\Vert_{L^\infty}^2}.$$
Then it is easy to check that $U_\varepsilon^i(x')\subset V_{\varepsilon}^i(x')$. 
Then for $\varepsilon>0$, we have 
\begin{align*} 
&\left|\int_{U_{\varepsilon}^i(x')}K_i(x',y') g(y')dy'\right|\\
& \leq \left|\int_{V_{\varepsilon}^i(x')} K_i(x',y')g(y')dy' \right| + \left|\int_{V_{\varepsilon}^i(x')\setminus U_\varepsilon^i(x')} K_i(x',y')g(y')dy' \right| .
\end{align*} 
It is easy to check that there exists a constant $C$ depending only on $n$ and the Lipschitz character of $\Omega$ such that  
$$  \left|\int_{V_{\varepsilon}^i(x')\setminus U_\varepsilon^i(x')} K_i(x',y')g(y')dy' \right|\leq C  Mg(x') $$
for all $\varepsilon>0$. Hence it follows from the Coifman-Meyer-McIntosh theorem that 
$$  \Vert \sup_{\varepsilon>0}|K_\varepsilon f| \Vert_{L^p(\partial\Omega)} \leq \sum_{i=1}^m \left(\Vert{T_* g_i}\Vert_{L^p}+C\Vert Mg_i \Vert_{L^p}\right) \leq C \sum_{i=1}^m \Vert g_i \Vert_{L^p}\leq C \Vert f \Vert_{L^p(\partial\Omega)}. $$
This completes the proof. 
</div>

<hr>

By the above theorem, we can conclude that $ \lim_{\varepsilon \rightarrow 0+ }K_\varepsilon f$ exists a.e. and in $L^p(\partial\Omega)$. We define 
$$ Kf(x)=\lim_{\varepsilon\rightarrow 0+} K_\varepsilon f(x).$$


# Nontangential behavior of harmonic function

Now we are ready to present the main theorem of this post.

<blockquote>
<strong> Theorem 6. </strong> Suppose that $u$ is harmonic in $\Omega$ and $u^*\in L^2(\partial\Omega)$. Then there exists $f\in L^2(\partial\Omega)$ such that 
$$ \lim_{z\in \gamma(x), z\rightarrow x} u(x)=f(x)\quad \text{a.e. } x\in \partial\Omega.$$ 
</blockquote>

Choose a sequence of smooth domains $\{\Omega_j\}$ as in Theorem 3 and let $f_j= u|_{\partial\Omega_j}$. Since $u^*\in L^2(\partial\Omega)$, it follows that $\Vert f_j \Vert_{L^2(\partial\Omega)}\leq C<\infty$. Note also that the identity
$$ u= \mathcal{D}_j\left(\left(\frac{1}{2}I+K_j\right)^{-1}f_j \right)\quad \text{on } \Omega_j $$
holds, where $\mathcal{D}_j$ and $K_j$ are the double layer potential and the boundary integral  operator associated to $\Omega_j$, respectively. Moreover, we have 
$$ \left\Vert \left(\frac{1}{2}I+K_j\right)^{-1}f_j  \right\Vert_{L^2(\partial\Omega_j)}\leq C \Vert f_j \Vert_{L^2(\partial\Omega_j)}, $$
where the constant $C$ does not depend on $j$. 
If we define 
$$ g_j = \left(\frac{1}{2}I+K_j\right)^{-1}f_j\circ \Lambda_j,$$
then $\{g_j\}$ is bounded in $L^2(\partial\Omega)$. Hence by the weak compactness result, there exists a function $g\in L^2(\partial\Omega)$ such that $g_j\rightarrow g$ weakly in $L^2(\partial\Omega)$. Moreover, it follows that $\mathcal{D}g_j\rightarrow u$ in $\Omega$. Therefore, 
$$ \mathcal{D}g=u\quad \text{on } \Omega.$$
Hence, we conclude that 
$$\lim_{x\rightarrow x_0;x\in \gamma(x_0)} u(x)=\lim_{x\rightarrow x_0;x\in \gamma(x_0)} \mathcal{D} g(x)=\left(\frac{1}{2}I+K \right)g(x),$$
which proves the desired result since  $\left(\frac{1}{2}I+K \right)g \in L^2(\partial\Omega)$. 

<hr>

# References 

<ol>
  <li> E. M. Stein, Singular integrals... </li>
  <li> G. Verchota, Layer potentials and Regularity for the Dirichlet problem for Laplace's equation in Lipschitz domains. </li>
</ol>
