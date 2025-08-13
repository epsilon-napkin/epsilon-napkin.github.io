
---
title: $\Gamma$ 函数
page-title: Γ 函数
tag: [](./index.md)
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\quads#1{\quad #1 \quad}$
$\gdef\eqq{\quads=}$
$\gdef\d{\operatorname{d}}$
$\gdef\hint#1{\color{grey}#1}$

$$
\begin{aligned}
\Gamma(s) 
&\spaces{:=} \int_0^{+\infty} x^{s-1}e^{-x} \d x
&\hint{\spaces{=} \int_0^{+\infty} x^se^{-x} \frac{\d x}{x} }
&\spaces{=} \mathcal{M}(e^{-x})|_s
\end{aligned}
$$

$\Gamma$ 函数有常用性质: $(i)$ $\Gamma(s+1) = s\Gamma(s)$. $(ii)$ $\Gamma(\frac12) = \sqrt{\pi}$. $(iii)$ $\Gamma(n+1) = n!$. $(iv)$ $\Gamma(s)\Gamma(1-s) = \frac{\pi}{\sin \pi s}$. 
