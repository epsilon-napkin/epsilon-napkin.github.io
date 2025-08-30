
---
title: 概率论与数理统计
index: [](../index.md)
---


我们列出常见分布的期望, 相应的证明见各自条目. 

| 分布 | 符号 | 期望 | 方差 |
| - | - | - | - |
| [二项分布](./二项分布.md) | $X \sim B(n,p)$ | $np$ | $np(1-p)$ |
| [Poisson 分布](./Poisson分布.md) | $X \sim P(\lambda)$ | $\lambda$ | $\lambda$ |
| [几何分布](./几何分布.md) | $X \sim G(p)$ | $\dfrac{1}{p}$ | $\dfrac{1-p}{p^2}$ |
| [超几何分布](./超几何分布.md) | $X \sim H(N,K,n)$ | $n\dfrac{K}{N}$ | $n\dfrac{K(N-K)}{N^2} \dfrac{N-n}{N-1}$ |
| [均匀分布](./均匀分布.md) | $X \sim U(a,b)$ | $\dfrac{a+b}{2}$ | $\dfrac{(b-a)^2}{12}$ |
| [指数分布](./指数分布.md) | $X \sim E(\lambda)$ | $\dfrac{1}{\lambda}$ | $\dfrac{1}{\lambda^2}$ |
| [正态分布](./gaussian.md) | $X \sim N(\mu,\sigma^2)$ | $\mu$ | $\sigma^2$ |

两点分布作为 [二项分布](./二项分布.md) 在 $n=1$ 时的特例, 我们不再单独列出. 
