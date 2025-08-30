
---
title: 正态分布
term: Normal distribution
tag: [](./index.md)
asref: true
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$

若 $X$ 的概率密度为 

$$ f(x) \spaces= \frac{1}{\sqrt{2\pi} \sigma} \exp\Big({-\frac{(x-\mu)^2}{2 \sigma^2}}\Big), \quad x \in \R $$

则称 $X$ 服从 [正态分布](./gaussian.md) $X \sim N(\mu, \sigma^2)$. [正态分布](./gaussian.md) 有以下显见性质:

1. 关于 $x=\mu$ 对称, 即 $P(X>\mu) = P(X<\mu)=\frac{1}{2}$. 
1. 线性变换. $aX+b \sim N(a\mu+b, a^2\sigma^2)$, $a \ne 0$. 
1. 线性组合. 设 $X \sim N(\mu_1,\sigma_1^2), Y \sim N(\mu_2,\sigma_2^2)$, $X,Y$ 独立, 则 $aX+bY \sim N(a\mu_1 + b\mu_2, a^2\sigma_1^2 + b^2\sigma_2^2)$. 

标准 [正态分布](./gaussian.md) 是化 $X \sim N(\mu, \sigma^2)$ 为 $Z \sim N(0,1)$, 自然 $Z = \frac{X-\mu}{\sigma}$, 此时 $Z$ 的概率密度为 $\varphi(x) = \frac{1}{\sqrt{2\pi}} \exp({-\frac{x^2}{2}})$, 分布函数记为 $\Phi(x)$. 由关于 $x=0$ 对称这一事实, 可以看出下述性质:

1. $\Phi(-x) = 1-\Phi(x)$. 
1. $\Phi(0) = \frac{1}{2}$. 
1. $P(|X|<a) = P(-a<X<a) = 2\Phi(a)-1$.

我们来验证概率密度在整个定义域上的积分是 $1$. 首先置 $t = \frac{x-\mu}{\sqrt 2 \sigma}$, $\d x = \sqrt 2 \sigma \d t$, 积分化为 $\frac{1}{\sqrt\pi} \int_\R e^{-t^2} \d t$, 又熟知 Gauß 积分为 $\sqrt{\pi}$, 立得. 


设 $(X,Y) \sim N(\mu_1, \mu_2, \sigma_1^2, \sigma_2^2, \rho)$ 则

- $X \sim N(\mu_1, \sigma_1^2)$, $X \sim N(\mu_2, \sigma_2^2)$
- $X,Y$ 相互独立 $\iff \rho = 0$. 
- 非零线性组合 $aX+bY$ 仍然服从 [正态分布](./gaussian.md). 


