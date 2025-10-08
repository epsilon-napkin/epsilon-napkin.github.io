
---
title: Poisson 分布
term: Poisson distribution
tag: [](./index.md)
asref: true
---

$\gdef\E{\mathbb{E}}$
$\gdef\spaces#1{~ #1 ~}$

[Poisson分布](./Poisson分布.md) 表示在固定时间间隔内发生给定数量的事件的概率, 如果这些事件以已知的恒定平均速率发生, 并且独立于自上次事件以来经过的时间. 或者简单地说, 用于给定时间段内 Poisson 型事件发生次数. 其分布律为

$$
P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}, \quad (k \ge 0)
$$

这里常数 $\lambda > 0$, 则称 $X$ 服从参数为 $\lambda$ 的 [Poisson分布](./Poisson分布.md), 记作 $X \sim P(\lambda)$. 不难验证, $\sum_{k \ge 0} P(X = k) = e^{-\lambda} \sum_{k \ge 0} \frac{\lambda^k}{k!} = 1$, 这就是其形式的由来. 

[Poisson分布](./Poisson分布.md) 的 [期望](./期望.md) $\E(X) = \lambda e^{-\lambda} \sum_{k \ge 1} \frac{\lambda^{k-1}}{(k-1)!} = \lambda$. 和 [二项分布](./二项分布.md) 类似, [Poisson分布](./Poisson分布.md) 的 [方差](./方差.md) 计算也要用到 [降阶乘基表示](./降阶乘基表示.md) 这个观察 

$$
\begin{aligned}
\E(X^2) 
&\spaces= e^{-\lambda} \sum_{k \ge 0} k^2 \cdot \frac{\lambda^{k}}{k!} \\
&\spaces= e^{-\lambda} \sum_{k \ge 0} (k+k(k-1)) \cdot \frac{\lambda^{k}}{k!} \\
&\spaces= \E(X) + \lambda^2 e^{-\lambda} \sum_{k \ge 2} \frac{\lambda^{k-2}}{(k-2)!} \\
&\spaces= \lambda + \lambda^2
\end{aligned}
$$

于是 $D(X) = \E(X^2) - (\E X)^2 = \lambda$. 如果用降阶乘基矩表示, 则可以更容易地得到 $D(X) = \E(X(X-1)) + \E X - (\E X)^2 = \lambda$. 
