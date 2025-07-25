
---
title: 级数敛散性
asref: true
method: [](/math/方法.md)
tag: [](/math/index.md)
---

$\gdef\spaces#1{~ #1 ~}$

概念是平凡的, 所以我们只介绍收敛判别法. 

1. 双边控制, 又称夹逼. 设有三个实数序列 $(a_n) \le (x_n) \le (b_n)$, 这里的 $\le$ 要求每一项都成立. 如果 $\lim_{n \to \infty} a_n = b_n = X$, 则 $\lim_{n \to \infty} x_n = X$. 

2. 上界控制, 即放大. 设有非负实数序列 $(x_n) \le (y_n)$, 如果 $\lim_{n \to \infty} y_n = 0$, 则 $\lim_{n \to \infty} x_n = 0$. 为了证明一个级数 $\sum_k a_k$ 收敛, 很多情况下只要说明它绝对收敛 $\sum_k |a_k|$ 即可, 再配合放大 $\sum_k |a_k| \le \sum_k b_k$ 选择恰当的 $b_k$, 从而得到 $a_k$ 收敛. 

$\textbf{Example.}$ $\zeta(2) = \sum_{n \ge 1}\frac{1}{n^2}$ 收敛. 因为 $n^2 \ge n(n-1)$ 有

$$
\begin{aligned}
\sum_{n \ge 1}\frac{1}{n^2} 
&\spaces\le 1 + \sum_{n \ge 2}\frac{1}{n(n-1)} \\
&\spaces= 1 + \sum_{n \ge 2}\Big( \frac{1}{n-1} - \frac{1}{n}\Big) \\
&\spaces= 2
\end{aligned}
$$
