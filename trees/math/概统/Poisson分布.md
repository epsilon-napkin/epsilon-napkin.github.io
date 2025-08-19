
---
title: Poisson 分布
term: Poisson distribution
tag: [](./index.md)
---

[Poisson分布](./Poisson分布.md) 表示在固定时间间隔内发生给定数量的事件的概率, 如果这些事件以已知的恒定平均速率发生, 并且独立于自上次事件以来经过的时间. 或者简单地说, 用于给定时间段内 Poisson 型事件发生次数. 其分布律为

$$
P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}, \quad (k \ge 0)
$$

这里常数 $\lambda > 0$, 则称 $X$ 服从参数为 $\lambda$ 的 [Poisson分布](./Poisson分布.md), 记作 $X \sim P(\lambda)$. 不难验证, $\sum_{k \ge 0} P(X = k) = e^{-\lambda} \sum_{k \ge 0} \frac{\lambda^k}{k!} = 1$, 这就是其形式的由来. 
