
---
title: 积分坐标变换
tag: [](./index.md)
---

$\gdef\d{\operatorname{d}}$
$\gdef\spaces#1{~ #1 ~}$
$\gdef\Jac{\operatorname{Jac}}$

设 $\Phi: U \to V$ 是 $\R^n$ 中两个区域之间的微分同胚, 各自的坐标分别记为 $x = (x_i)$, $y = (y_i)$. 对应的 Riemann 积分的换元公式可以写为

$$ \d y \spaces= \Phi_*(|\det \Jac \Phi| \d x) $$

坐标变换并不一定要计算行列式, 例如 $(x,y) \to (r \cos \theta, r \sin \theta)$, 所以

$$
\d x \spaces= \cos \theta \d r - r \sin \theta \d \theta \\
\d y \spaces= \sin \theta \d r + r \cos \theta \d \theta 
$$

则我们展开 $\d x \d y$ 为 $\square \d r \d \theta$

$$
\begin{aligned}
\d x \land \d y 
&\spaces= r \cos^2 \theta \d r \land \d \theta - r \sin^2 \theta \d \theta \land \d r \\
&\spaces= (r \cos^2 \theta + r \sin^2 \theta) \d r \land \d \theta \\
&\spaces= r \d r \land \d \theta
\end{aligned}
$$

这和 Jacobian 是一致的

$$
\def\arraystretch{1.5}
\begin{vmatrix} 
\frac{\partial f_1}{\partial x_1} & \cdots & \frac{\partial f_1}{\partial x_n} \\ 
\vdots & \ddots & \vdots \\
\frac{\partial f_m}{\partial x_1} & \cdots & \frac{\partial f_m}{\partial x_n} 
\end{vmatrix}
\spaces= 
\def\arraystretch{1.2}
\begin{vmatrix} \cos \theta & - r \sin \theta \\ \sin \theta & r \cos \theta 
\end{vmatrix}
\spaces=
r
$$

