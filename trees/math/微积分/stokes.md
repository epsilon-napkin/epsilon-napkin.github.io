
---
title: Stokes 公式
asref: true
taxon: formula
tag: [](./index.md)
---

$\gdef\d{\operatorname{d}}$
$\gdef\dif{\partial}$
$\gdef\spaces#1{~ #1 ~}$

设 $M$ 是定向带边 $n$ 维光滑流形, $\omega$ 是 $M$ 上的紧支 $(n−1)$-形式. 则

$$
\int_M \d \omega = \int_{\dif M} \omega
$$

Stokes 公式有若干常用特例, 分别是: 

- [](./newton-leibniz.md). 取 $M=[a,b]$ 即带边 $1$ 维光滑流形, 此时 $\dif M = \{b\} \to \{a\}$, $\omega$ 是 $0$ 形式. 取 $M$ 为 $1$ 维流形, 即曲线 $\gamma$, $\partial M$ 是曲线的两个端点, 得 [](./梯度定理.md).
- [](./green.md). 取 $M$ 为 $\R^2$ 中光滑简单闭曲线围成的区域 $\Omega$, $\omega = P \d x + Q \d y$ 
  $$
  \begin{aligned}
  \d \omega 
  &\spaces= \d P \wedge \d x + \d Q \wedge \d y \\
  &\spaces= \bigg( \frac{\dif P}{\dif x} \d x + \frac{\dif P}{\dif y} \d y \bigg) \wedge \d x + \bigg( \frac{\dif Q}{\dif x} \d x + \frac{\dif Q}{\dif y} \d y \bigg) \wedge \d y \\
  &\spaces= \bigg( \frac{\dif Q}{\dif x} - \frac{\dif P}{\dif y} \bigg) \mathrm{d}x \wedge \mathrm{d}y
  \end{aligned}
  $$
- [](./kelvin-stokes.md) 取 $M=\Sigma$, $\omega=Pdx+Qdy+Rdz$. 也即 [](./旋度定理.md). 
- [](./ostrogradsky-gauss.md). 取 $\omega = P \d y \d z + Q \d z \d x + R \d x \d y$, $\d \omega$ 可类似算得 $$ \d \omega \spaces= \bigg( \frac{\dif P}{\dif x} + \frac{\dif Q}{\dif y} + \frac{\dif R}{\dif z} \bigg) \d x \d y \d z $$

[](./stokes.md) 与 [](./散度定理.md) 可以互相推出.
