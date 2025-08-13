
---
title: 椭圆面积
taxon: example
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$
$\gdef\dif{\partial}$

计算椭圆 $E:\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ 所围区域 $\Omega$ 的面积 $\operatorname{Area}(\Omega)$. 设椭圆的参数方程为 

$$
\begin{cases}
x = a \cos\theta, \\
y = b \sin\theta, 
\end{cases} 
\quad
0 \le \theta \lt 2\pi
$$

其定向取逆时针方向. 设 $P = -\frac{y}2, Q = \frac{x}2$ 此时 $\frac{\dif Q}{\dif x} - \frac{\dif P}{\dif y} = 1$. 
$$
\begin{aligned}
\operatorname{Area}(\Omega) 
&\spaces= \int_\Omega \d x \d y \\
&\spaces= \frac{1}{2} \int_E x \d y - y \d x \\
&\spaces= \frac{ab}{2} \int_0^{2\pi} \d \theta \\
&\spaces= ab\pi
\end{aligned}
$$
