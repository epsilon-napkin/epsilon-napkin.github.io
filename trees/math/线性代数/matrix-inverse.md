
---
title: 矩阵求逆
tag: [](./index.md)
---

单论时间复杂度, [](./matrix-inverse-1.md) $\mathcal{O}(n^3)$ 的复杂度相比 [](./matrix-inverse-2.md) 的 $\mathcal{O}(n^2 \cdot n!)$ 在 $n \gt 2$ 时会更有优势, 这里 $n^2$ 来自于余子式, $n!$ 来自于 $\det$. 但手工计算 $A^{-1}$ 时, 如果能够观察出 $A$ 一些特殊的性质然后打洞, 则 $\det A$ 的实际复杂度就会大大下降, 此时的 [](./matrix-inverse-2.md) 不失为一种好的策略. 本身行列式可用的处理手段也比 [](./gauss-jordan.md) 要多得多.  

[+](./0141.md#:embed)
[+](./0142.md#:embed)
