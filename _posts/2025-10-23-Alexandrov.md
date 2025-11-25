---
layout: post
comments: true
use_math: true
title:  "Blashcke-Santalo inequality and Aleksandrov estimates"
date:   2025-10-23 10:00:40 
---

Yesterday, while I am attending ICERM conference on [fluid dynamics and turbluence]("https://icerm.brown.edu/program/hot_topics_workshop/htw-25-fdt"), I learned from [Nestor]("https://www.ndguillen.com/") that there is another way to look at the Aleksandrov maximum principle via convex geometry.
I appreciate his passion for sharing this knowledge with me.

In my previous blog post, [Aleksandrov estimate]("https://willkwon-math.kr/2022/07/31/Amax") plays an important role in regularity theory for equations in nondivergence form or fully nonlinear equations. For simplicity, we consider a convex function $h:D\rightarrow\mathbb{R}$ defined on a convex body $D$ satisfying $h=0$ on $\partial D$. Furthermore, we assume that the center of mass of $D$ is the origin. A classical Aleksandrov estimate is that 
<div>
\begin{equation}
\Vert h \Vert_{L^\infty(D)} \leq C_d|D|^{1/d}|\nabla h(D)|
\end{equation}
for some constant $C_d>0$.
</div>

<div>
There is an interesting connection with Blashcke-Santalo inequality and this estimate. To state this, let us define the polar dual
\begin{equation*}
D^*=\{x\in\mathbb{R}^d : x\cdot y \leq 1\quad \text{for all } y \in D\}.
\end{equation*}
In 1939, Mahler proved that 
\begin{equation*}
4^n (n!)^{-2}\leq  |D| |D^*|\leq 4^n.
\end{equation*}
Later, Santalo proved that the upper bound has a precise geometric bound
\begin{equation*}
|D| |D^*|\leq |B_d|^2,
\end{equation*}
where $B_d$ is the $d$-dimensional unit ball. The inequality becomes equality when $D=B_d$. After this work, several interesting improvements were made to determine the precise lower bound for $|D| |D^*|$. I do not have a clear picture of how researchers could obtain optimal estimates by using the geometry of Banach spaces (this is slightly unclear to me). Bourgan-Milman proved the following estimate, which is now called Blashcke-Santalo inequality.
</div>

ongoing....
