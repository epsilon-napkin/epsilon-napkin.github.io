
---
title: Green 公式
taxon: formula
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$
$\gdef\dif{\partial}$

如果 $\Omega\subset \R^2$ 是有界光滑带边区域，那么对任意函数 $P, Q \in C^1(\R^2)$，我们有

$$
\int_{\Omega} \bigg( \frac{\dif Q}{\dif x} - \frac{\dif P}{\dif y} \bigg) \d x \d y 
\spaces= \oint_{\dif \Omega} P \d x + Q \d y
$$

其中 $\dif \Omega$ 取正向, 即逆时针方向 $↺$ 遍历边界曲线, 使得当沿着曲线行走时, 区域 $\Omega$ 始终在左边. 

$\textbf{Example.}$ 计算椭圆 $E:\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ 所围区域 $\Omega$ 的面积 $\operatorname{Area}(\Omega)$. 设椭圆的参数方程为 

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
