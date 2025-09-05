
---
title: Fourier 变换
tag: [](./index.md)
---

$\gdef\Z{\mathbf{Z}}$
$\gdef\R{\mathbf{R}}$
$\gdef\C{\mathbf{C}}$
$\gdef\T{\mathbf{T}}$
$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$

$\theta \to e^{2\pi i \theta}$ 是 $\R/\Z \to \C$ 的典范映射. 特别地我们记圆周群 $\T = \R/\Z$, 其中元素 $t \in [0, 1)$ 当然来自 $x \mod 1$. 

对于全体 $f:S \to \C$, 这些函数的集合形成一个复向量空间. 如果希望为这些函数的集合配备一个正定的内积, 则可以通过讲这些函数表为 Fourier 系数 $\hat{f}$ 和正交基 $e_\xi$ 的线性组合 [^finite]. 

$$
f(x) \spaces= \sum_\xi \hat{f}(\xi) e_\xi
$$

$L^2([-\pi, \pi])$ 函数的 Fourier 级数

$$
\lang f, g \rang \spaces= \frac{1}{2\pi} \int_{[-\pi, \pi]} f(x)\overline{g(x)} \d x
$$

这是一个无限维 Hilbert 空间. 

[](./fourier-1.md#:embed)
[](./fourier-2.md#:embed)
