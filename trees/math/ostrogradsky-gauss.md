
---
title: Ostrogradsky--Gauß 公式
taxon: formula
asref: true
tag: [](/math/index.md)
---

$\gdef\dif{\partial}$
$\gdef\d{\operatorname{d}}$
$\gdef\spaces#1{~ #1 ~}$

设 $\Sigma$ 是 $\mathbb{R}^3$ 中的一个光滑简单闭曲面,
$\Sigma$ 围成区域记作 $\Omega$. 设 $P,Q,R$ 是定义在 $\bar\Omega$ 上的光滑函数, 则

$$
\begin{aligned}
\int_{\Omega}\left(
\frac{\partial P}{\partial x}+
\frac{\partial Q}{\partial y}+
\frac{\partial R}{\partial z}
\right) \d x \d y \d z \spaces=\int_{\Sigma}\left( P \d y \d z + Q \d z \d x + R \d x \d y \right)
\end{aligned}
$$
