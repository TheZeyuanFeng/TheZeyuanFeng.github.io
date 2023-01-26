---
layout: post
title: Convex Optimization Ch.1
date: 2023-1-24 21:09:00-0400
description: Introduction
tags: formatting math
categories: math blogs
---
##### __Introduction__
This blog series aims to provide a clear, yet conprehensive note about convex optization based on the ESE 605 course material at UPenn. The goal is that after reading this blog, the readers would be able to
- recognize and formulate problems as convex optimization problems
- develop code for problems of moderate size
- characterize optimal solution, give limits of performance, etc.

The following topics are included
- convex sets, functions, optimization problems
- examples and applications
- algorithms

###### __Canonical form of convex optimization__
<p>
$$\begin{array}{ll}
    \operatorname{minimize} \ f_0(x) \\
    \text { subject to }  f_i(x) \leq b_i, \quad i=1, \ldots, m
\end{array}$$
</p>

- <p>
  where objective and constraint functions are convex 
  $$
  \newline f_i(\alpha x+\beta y)\leq \alpha f_i(X)+\beta f_i(y))
  $$ 
  </p>
  if $$ \alpha+\beta=1,\alpha\geq 0, \beta \geq 0 $$


##### __Convex sets__
For the following definitions, click to expand


<details>
  <summary>
    Lines
    <span class="icon">👇</span>
  </summary>
    all points through x<sub>1</sub>, x<sub>2</sub>
    <p>
      $$\{x \mid x=\theta x_1+(1-\theta) x_2 , \ \theta \in \mathcal{R} \}$$
    </p>
</details>



<details>
  <summary>
    Affine set
    <span class="icon">👇</span>
  </summary>
    contains the line through any two distinct points in the set.
    <p>
    Every affine set can be expressed as solution set of system of linear equations

      example : solution set of linear equations
      $$\{x \mid A x=b\}$$
    </p>
</details>

<details>
  <summary>
    Line segment
    <span class="icon">👇</span>
  </summary>
    all points between x<sub>1</sub>, x<sub>2</sub>
    <p>
      $$\{x \mid x=\theta x_1+(1-\theta) x_2 , \ \theta \in [0,1] \}$$
    </p>
</details>


<details>
  <summary>
    Convex set
    <span class="icon">👇</span>
  </summary>
    contains line segment between any two points in the set
    <p>
      $$x_1, x_2 \in C, \quad 0 \leq \theta \leq 1 \quad \Longrightarrow \quad \theta x_1+(1-\theta) x_2 \in C$$
      Examples:
    </p>
    <div class="row">
      <div class="col-sm mt-3 mt-md-0">
          {% include figure.html path="assets/img/ConvexOptimization/ch1/convex_set_eg.png" title="example image" class="img-fluid rounded z-depth-1" width="500"%}
      </div>
    </div>
</details>

A convex set can be represented by convex combination
<details>
  <summary>
    Convex combination and convex hull
    <span class="icon">👇</span>
  </summary>
    convex combination of x<sub>1</sub>, ..., x<sub>k</sub> includes any point x of the form
    <p>
      $$x=\theta_1 x_1+\theta_2 x_2+\cdots+\theta_k x_k$$
    </p>
    with $$\theta_1+\cdots+\theta_k=1, \theta_i \geq 0$$
    <p>
      convex hull conv(<i>S</i>) is the set of all convex combinations of points in <i>S</i>
    </p>
    <div class="row">
      <div class="col-sm mt-3 mt-md-0">
          {% include figure.html path="assets/img/ConvexOptimization/ch1/convex_hull_eg.png" title="example image" class="img-fluid rounded z-depth-1" width="500"%}
      </div>
    </div>
</details>

