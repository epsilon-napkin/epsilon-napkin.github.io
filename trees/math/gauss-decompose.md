
---
title: Gauss 分解
asref: true
tag: [](/math/index.md)
---

$\gdef\d{\operatorname{d}}$
$\gdef\spaces#1{~ #1 ~}$

处理有理函数积分 $\int \frac{P_n(x)}{P_m(x)} \d x$ $(n < m)$ 的一种方法是将其裂项为分子 $\deg(-) \le 1$ 且分母 $\deg(-) \le 2$ 的有理函数之和, 也称为部分分式分解. 系数的确定一般灵活使用 [Heaviside 覆盖法](https://en.wikipedia.org/wiki/Heaviside_cover-up_method), 对于不能表为 $(x-a)^{-k}$ 的项, 额外考虑 $0,1$ 和 $\infty$ 处的取值. 

$\textbf{Example.}$ 分解 $R(x) = \frac{2x+1}{(x^2+x+1)(x+1)}$ 从而计算 $\int R(x) \d x$. 

$$
\frac{2x+1}{(x^2+x+1)(x+1)} \spaces= \frac{A}{x+1} + \frac{Bx+C}{x^2+x+1}
$$

现在确定 $A,B,C$. 注意 $R(0) = A+C=1$. $R(1) = \frac{A}2 + \frac{B+C}3 = \frac{1}{2}$ 即 $3A + 2B + 2C = 3$. $(x+1)R(x)|_{x+1 \to 0} = A = -1$. 解得 $(A,B,C) = (-1,1,2)$. 如此就有 

$$ \int R(x) \d x \spaces= -\int \frac{1}{x+1} \d x + \int \frac{x+2}{x^2+x+1} \d x $$

这里的 $\int \frac{x+2}{x^2+x+1} \d x$ 不太明显, 我们先拆出一个对数部分 $\frac{\d y}{y} = \frac{2x+1}{x^2+x+1}$, 从而将其写成

$$
\begin{aligned}
\int \frac{x+2}{x^2+x+1} \d x 
&\spaces= \frac{1}{2} \int \frac{2x+1}{x^2+x+1} \d x + \frac{3}{2} \int \frac{1}{x^2+x+1} \d x \\
&\spaces= \frac{1}{2} \log(x^2+x+1) + \frac{3}{2} \int \frac{1}{(x+\frac{1}{2})^2 + \frac{3}{4}} \d x \\
&\spaces= \frac{1}{2} \log(x^2+x+1) + \sqrt{3}\tan^{-1} \frac{2x+1}{\sqrt{x}}
\end{aligned}
$$

这里 $\log$ 内没有加绝对值是因为 $(x+\frac{1}{2})^2 + \frac{3}{4} \gt 0$. 综合得到

$$ \square \spaces= -\log|x+1| + \frac{1}{2} \log(x^2+x+1) + \sqrt{3}\tan^{-1} \frac{2x+1}{\sqrt{x}} $$
