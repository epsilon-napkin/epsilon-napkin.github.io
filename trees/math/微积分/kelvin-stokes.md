
---
title: Kelvin--Stokes 公式
asref: true
taxon: formula
tag: [](./index.md)
---

$\gdef\dif{\partial}$
$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$

设 $\Sigma$ 是 $\R^3$ 中一个可定向光滑曲面且带有边界 $C$. $P,Q,R$ 是定义在 $\Sigma$ 上的光滑函数. 则

$$
\begin{aligned}
&\int_C P \d x + Q \d y + R \d z \\
\color{grey}{=~~} & \color{grey}{\int_{\partial \Sigma} \d P \land \d x + \d Q \land \d y + \d R \land \d z} \\
\color{grey}{=~~} & \color{grey}{
  \bigg( \frac{\dif P}{\dif x} \d x + \frac{\dif P}{\dif y} \d y + \frac{\dif P}{\dif z} \d z \bigg) \wedge \d x} + 
  \bigg( \frac{\dif Q}{\dif x} \d x + \frac{\dif Q}{\dif y} \d y + \frac{\dif Q}{\dif z} \d z \bigg) \wedge \d y \\
  & \kern{3.8em} \color{grey}{+ \bigg( \frac{\dif R}{\dif x} \d x + \frac{\dif R}{\dif y} \d y + \frac{\dif R}{\dif z} \d z \bigg) \wedge \d z} \\
=~~ & \int_\Sigma \bigg( \frac{\dif R}{\dif y}-\frac{\dif Q}{\dif z} \bigg) \d y \d z + \bigg( \frac{\dif P}{\dif z}-\frac{\dif R}{\dif x} \bigg) \d z \d x + \bigg( \frac{\dif Q}{\dif x}-\frac{\dif P}{\dif y} \bigg) \d x \d y
\end{aligned}
$$
