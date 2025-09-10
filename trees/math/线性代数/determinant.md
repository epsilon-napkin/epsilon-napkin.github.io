
---
title: 行列式
tag: [](./index.md)
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\sgn{\operatorname{sgn}}$

交换矩阵 $M$ 两行或两列得到 $N$, 则 $\det M = -\det N$. 这可由逆序数的性质直接得到. 或者使用置换的语言 

$$
\begin{aligned}
\det M 
&\spaces= \sum_{\sigma \in \mathfrak{S}_n} \sgn(\sigma) a_{\sigma(1), 1} \cdots a_{\sigma(n), n} \\ 
&\spaces= \sum_{\sigma \in \mathfrak{S}_n} \sgn(\sigma) a_{1, \sigma(1)} \cdots a_{n, \sigma(n)}
\end{aligned}
$$

自然地, 可以根据以下三点判断 $\det \square = 0$. 

1. 交换矩阵两行或两列后矩阵各分量不变. 
1. 列向量成比例, 即 $M = \alpha M'$, 而 $M'$ 满足 1.
1. 存在全为零的行或列, 也即存在零向量. 

此外, $\det A = 0$ 也有一个充要条件, 可叙述为 $A$ 的 $n$ 个行 (列) 向量 [线性相关](./线性相关.md). 等价地, $\det A \ne 0$ $\iff$ $A$ 的 $n$ 个行 (列) 向量线性无关. 

[+](./0131.md#:embed)
[+](./0132.md#:embed)
