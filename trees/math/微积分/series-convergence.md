
---
title: 级数敛散性
asref: true
tag: [](./index.md)
---

$\gdef\spaces#1{~ #1 ~}$

概念是平凡的, 所以我们只介绍收敛判别法. 常用方法如下: 

[](./控制收敛.md#:embed)
[](./绝对收敛.md#:embed)

任意项级数中一种性质较好的情况为交错级数, 即 $A = \sum_{n} (-1)^n a_n$, 此处所有 $a_n$ 同号. 为判断 $A$ 的敛散性, 不妨设 $a_n \ge 0$, 否则考虑 $-A$. 如果 $a_n$ 单调递减且趋于 $0$, 则 $A$ 收敛. 此交错级数判别法又名 Leibniz 判别法. 

Leibniz 判别法有一推广, 名为 Dirichlet 判别法. 其断言, 若 $\sum a_n$ 的部分和有界, $(b_n)_n$ 单调趋于 $0$, 则 $\sum a_n b_n$ 收敛. 另有一类似的 Abel 判别法断言, 若 $\sum a_n$ 收敛, $(b_n)_n$ 单调有界, 则 $\sum a_n b_n$ 收敛. 
