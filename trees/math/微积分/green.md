
---
title: Green 公式
asref: true
taxon: formula
tag: [](./index.md)
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$
$\gdef\dif{\partial}$

如果 $\Omega\subset \R^2$ 是有界光滑带边区域，那么对任意函数 $P, Q \in C^1(\R^2)$，我们有

$$
\int_{\Omega} \bigg( \frac{\dif Q}{\dif x} - \frac{\dif P}{\dif y} \bigg) \d x \d y 
\spaces= \oint_{\dif \Omega} P \d x + Q \d y
$$

其中 $\dif \Omega$ 取正向, 即逆时针方向 $↺$ 遍历边界曲线, 使得当沿着曲线行走时, 区域 $\Omega$ 始终在左边. [](./green.md) 可视为 [](./kelvin-stokes.md) 的特例, 并在更加一般的意义上由 [](./stokes.md) 统一起来. 

[](./green-1.md#:embed)
