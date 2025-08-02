
---
title: Euler 齐次函数定理
taxon: theorem
tag: [](./index.md)
---

$\gdef\dif{\partial}$

$\gdef\spaces#1{~ #1 ~}$

给定开集 $U \subset \mathbb{R}^n$. 若 $f:U \to \mathbb{R}$ 是一个连续可微的 $k$ 次正齐次函数, 则必满足

$$
\begin{equation*}
k f(x_1, \ldots, x_n) \spaces=
\sum_{i=1}^n x_i \frac{\dif }{\dif x_i}f(x_1, \ldots, x_n)
\end{equation*}
$$

$\textbf{Example.}$ 设 $f(x,y) = \sqrt{\frac{x^2+y^2}{xy}}$, $xy > 0$, 求 $x \frac{\dif f}{\dif x} + y \frac{\dif f}{\dif y}$. 根据 $f(tx, ty) = f(x, y)$ 可知 $k=0$, 所以 $x \frac{\dif f}{\dif x} + y \frac{\dif f}{\dif y} = 0$. 

