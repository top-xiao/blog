---
title: "distribution"
date: "2024-12-29"
math: true


---


The Topology of Schwartz Space

In this article, we will discuss the characteristics of the topology of
Schwartz space, defined by $$\begin{aligned}
    \mathcal{S}(\mathbb{R}^d)\coloneqq \{f \in C^{\infty}(\mathbb{R}^d) | \forall n \in \mathbb{N}, p_n(f) < \infty\}, 
  \end{aligned}$$ where $\{p_n\}_{n \in \mathbb{N}}$ is a collection of
seminorms on $C^{\infty}(\mathbb{R}^d)$, defined by $$\begin{aligned}
    p_n(f) \coloneqq \sup_{\substack{x \in \mathbb{R}^d \\ |\alpha |, |\beta | \leq N}} |x^{\alpha }\partial^{\beta }_x f(x)|.
  \end{aligned}$$

First, the natural choice for the topology of Schwartz space must ensure
that all the seminorms defined above are continuous, meaning that for
every positive real number $r$ and natural number $n$, the set
$\{p_n < r \}= \{f \in \mathcal{S}(\mathbb{R}^d) \mid p_n(f) <r\}$ is an
open set. Therefore, the most reasonable choice of the topology of
Schwartz space is the one defined by the topology whose neighborhood
system at the origin is generated by
$\{\{p_n<r\}\mid n \in \mathbb{N}, r \in \mathbb{R}_{>0} \}$.

There are two significant features, non-normablity and complete
metrilisablity, which will be proved in the rest of the article. We will
adopt the notation $S$ for the Schwartz space on $\mathbb{R}^d$.

Let's start with the easier one, non-normablity, meaning that there is
no norm on Schwartz space that induces the same topology we defined
above. Suppose not, i.e. assume there is a norm $\| \cdot \|$ which
induces the same topology we defined above. Since $\{\| \cdot \| < 1 \}$
is open, there exists
$n_1, \ldots n_k \in \mathbb{N}, r_1, \ldots , r_k \in \mathbb{R}_{>0}$
such that
$\cap _{i=1}^{k}\{p_{n_i}< r_i\} \subseteq \{\|\cdot \| < 1 \}$. Denote
the minimum of $r_1, \ldots , r_k$ by $r$. And for every
$x \in \mathcal{S}$, we set $\alpha$ to be maximum of
$p_{n_1}(x), \ldots , p_{n_k}(x)$. Then, we have $\|rx \| \leq 2\alpha$.
Noticing that $\{p_n\}_{n \in \mathbb{N}}$ is a pointwise increasing
sequence, we obtain that there exists two constants
$C \in \mathbb{R}_{>0}$ and $n \in \mathbb{N}$ satisfying
$\| \cdot \| \leq C p_n(\cdot)$. In a similar way, we have that for all
seminorms $p_i$, there exists a constant $C_i$ such that
$p_i(\cdot) \leq C_i \|\cdot \|$, using the fact that $\{p_i < 1\}$ is
open, and there exists a positive real number $r'$ satisfying
$\{\|\cdot\| < r' \} \subseteq \{p_i <1\}$. Thus, all seminorms are
actually equivalent. This is obviously ridiculous, if one pays attention
to the following function $$\begin{aligned}
    f_{N,k}(x) \coloneqq  \exp(-|x|^2) \frac{\sin(Nx)}{N^k}.
  \end{aligned}$$ For $n\leq k-1$, we have $p_n(f_{N,k}) < \infty$ and
$p_n(f_{N,2k+1})$ converges to $0$ as $N \to \infty$. On the other hand,
one can verify that $\limsup_{N \to  \infty} p_{2k+1}(f_{N,k}) \geq 1$
holds from a straightforward calculation. That leads to a contradiction.
In conclusion, there exists no norm on Schwartz space that induces the
same topology generated by seminorms we defined above.

In the next part of this article, we will focus on the metrilisability
of Schwartz space. It is reasonable to suggest that the topology is also
induced by the following metric
$d: \mathcal{S}\times \mathcal{S}\to [0, \infty)$ $$\begin{aligned}
    d(f,g) \coloneqq  \sum_{n=1}^{\infty} \frac{p_n(f-g)}{2^n(1+p_n(f-g))}, \quad \forall f,g \in \mathcal{S}
  \end{aligned}$$ Before the formal proof, observing the metric defined
above would give us some insights and great helps. The idea for this
formulation is based on involving all distances induced by $p_k$ as
summands. First, the distance function has to take finite value, so we
convert each summand into a bounded distant function with upper bound
$1$. Then, we utilise a geometric series ensuring finiteness of the sum.
Those motivations bring about this strange and natural definition.

Let's move on to the proof. We will assume that $d$ is indeed a distant
function, and just check the topology generated by this metric
coninciding with what we defined above.

To show two topologies are equivalent, it suffices to show that they
share the same neighbourhoods at the origin. Let's show the topology
generated by $d$ is finer. $\forall k \in \mathbb{N}, r>0$, take
$\varepsilon >0$ s.t. $2^k \varepsilon /(1-\varepsilon ) < r /2$. Then
$B_d (0, \varepsilon ) \subseteq \{p_k < r\}$, where
$B_d(0,\varepsilon )$ stands for the open ball with radius $\varepsilon$
at 0 $0$. This complete the finer part since the semi-norms are
increasing. For the other direction, $\forall \varepsilon >0$, take the
natural number $m_0$ s.t.
$\sum_{n=m_0+1}^{\infty} 2^{-n}< \varepsilon /2$. So, set
$r = \varepsilon /2$, $\{p_{m_0} < r\} \subseteq B_d(0, \varepsilon )$
because
$d(0,f) \leq \varepsilon /2 + \sum_{n=1}^{m_0} \varepsilon /2^{n+1} < \varepsilon$,
for all $f \in \{p_{m_0}< r\}$.

In the remainder of this article, we will discuss that the convergence
defined in the class is equivalent to the convergence defined by the
metric. However, with the previous preparation, it suffices to show that
a sequence which converges under the topology we defined at the foremost
part in this article if and only if it converges in the sense we
discussed in the class. But this is obvious because of the definition of
the topology of the Schwartz Space.