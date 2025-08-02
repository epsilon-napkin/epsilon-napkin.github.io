
---
title: Bernoulli 方程
---

$\gdef\R{\mathbf{R}}$
$\gdef\spaces#1{~ #1 ~}$

Bernoulli 方程是可以精确求解的非线性常微分方程之一, 具有如下形式

$$ y' + p(x)y \spaces= q(x)y^\alpha, \quad (\alpha \in \R \smallsetminus \{0, 1\}) $$

换元 $z = y^{1-\alpha}$ 得 $z' + (1-\alpha)p(x)z = (1-\alpha)q(x)$. 此时变为 $z$ 的 [](./一阶线性微分方程.md). 此方法有效全是因为 Bernoulli 方程可化成

$$
y^{-\alpha}y' + p(x)y^{1-\alpha} \spaces= q(x)
$$

留意 $z' = (1-\alpha)y^{-\alpha}y'$, 随后同乘 $(1-\alpha)$. 


$\textbf{Example.}$ $y' + \frac{4x}{x^2-1} \cdot y = x\sqrt{y}$. 换元 $\alpha=\frac{1}{2}$, $z = y^{1-\alpha} = \sqrt{y}$, $z' + (1-\alpha)\frac{4x}{x^2-1}z = (1-\alpha)x$, 此时化为 [](./一阶线性微分方程.md). 
