
---
title: Euler 方程
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$

$$
x^ny^{(n)} + p_1x^{n-1}y^{(n-1)} + \cdots + p_{n-1}xy' + p_ny \spaces= f(x)
$$

$p_i$ 为常数. 这类方程的处理也比较固定: 换元 $x = e^t$, 记 $D = \frac{\d}{\d t}$, 则 

$$ x^ky^{(k)} \spaces= D(D-1)\cdots(D-k+1)y $$

代入原方程, 即可化为 [常系数线性微分方程](./常系数线性微分方程.md). 
