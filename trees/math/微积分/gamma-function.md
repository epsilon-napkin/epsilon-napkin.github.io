
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

$\Gamma$ 的记号来自 Legendre, $\Gamma$ 函数的唯一性由 Bohr--Mollerup 定理保证, 即开区间 $(0, \infty) = \R_{\gt 0}$ 上满足如下条件的函数是唯一的

1. 保持阶乘. $f(x+1) = xf(x)$. 
1. 恰当的初值. $f(1) = 1$. 
1. 对数凸. 即 $\log f$ 是凸函数. 这一点来自 Hölder 不等式. 

一般地, 此函数定义为 

$$ \Gamma(s) \spaces{:=} \int_0^{\infty} x^{s-1}e^{-x} \d x $$

也可以按 Haar 测度的写法, 显然乘法群 $\R_{> 0}^\times$ 的不变测度是 $\frac{\d x}{x}$ 

$$ \square \spaces= \int_{\R_{> 0}^\times} x^s e^{-x} \d \log x $$

读者还可以验证其就是 $e^{-x}$ 的 Mellin 变换, 即 $\Gamma(s) = \mathcal{M}(e^{-x})|_s = \int_{\R_{> 0}^\times}$, 此处 $\mathcal{M}_f(s) = \int x^s f(x) \d \log x$. 我们列出 $\Gamma$ 函数的常用特殊值

$$
\def\arraystretch{1.5}
\begin{array}{|c|c|c|c|c|c|c|c|c|}
   \hline
   s & -\frac{1}{2} & \frac{1}{2} & 1 & \frac{3}{2} & 2 & \frac{5}{2} & 3 & \cdots \\ \hline
   \Gamma(s)  & -2\sqrt{\pi} & \sqrt\pi & 1 & \frac{\sqrt{\pi}}{2} & 1 & \frac{3\sqrt{\pi}}{4} & 2 & \cdots \\ \hline
\end{array}
$$

$\Gamma$ 函数在负轴的延拓通过 Euler 反射公式或称余元公式给出

$$ \Gamma(s)\Gamma(1-s) \spaces= \frac{\pi}{\sin \pi s} $$

即 $\Gamma(-s) = \frac{1}{\Gamma(s+1)} \cdot \frac{\pi}{\sin \pi (x+1)}$, 推得 $\Gamma(-s) = -\frac{\Gamma(1-s)}{s}$. 
