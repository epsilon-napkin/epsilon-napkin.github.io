
---
title: Gauss 分解
asref: true
tag: [](./index.md)
---

$\gdef\Q{\mathbf{Q}}$
$\gdef\d{\operatorname{d}}$
$\gdef\spaces#1{~ #1 ~}$

处理有理函数积分 $\int \frac{P_n(x)}{P_m(x)} \d x$ $(n < m)$ 的一种方法是将其裂项为分子 $\deg(-) \le 1$ 且分母 $\deg(-) \le 2$ 的有理函数之和, 也称为部分分式分解. 每个 $k$ 重因式 $(x-a)^k$ 会贡献出如下分解项

$$
\frac{A_1}{x-a} + \cdots + \frac{A_k}{(x-a)^k} \spaces= \sum_{1 \le i \le k} \frac{A_i}{(x-a)^i}
$$

而每个二次不可约因式 $(x^2+bx+c)^m$ 可以贡献出

$$
\frac{B_1x+C_1}{x^2+bx+c} + \cdots + \frac{B_kx+C_k}{(x^2+bx+c)^k} \spaces= \sum_{1 \le i \le k} \frac{B_mx+C_m}{(x^2+bx+c)^i}
$$

由代数基本定理和虚根成对, 这些因式的形式没有别的可能了.

- 特别地, 对实二次不可约情形 $\frac{P_2(x)}{(x-a)(x^2+bx+c)}$, 其可以分解为 $\frac{A}{x-a} + \frac{Bx+C}{x^2+bx+c}$. 
- 重因式情形 $\frac{P_2(x)}{(x-a)^2(x-b)}$ 可以分解为 $\frac{A}{x-a} + \frac{B}{(x-a)^2} + \frac{C}{x-b}$. 

系数的确定一般灵活使用 [Heaviside 覆盖法](https://en.wikipedia.org/wiki/Heaviside_cover-up_method), 对于不能表为 $(x-a)^{-k}$ 的项, 额外考虑 $0,1$ 和 $\infty$ 处的取值. 

[](./0021.md#:embed)
[](./0031.md#:embed)
