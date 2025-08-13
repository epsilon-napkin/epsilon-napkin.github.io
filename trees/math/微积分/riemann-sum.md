
---
title: Riemann 和
asref: true
tag: [](./index.md)
---

$\gdef\d{\operatorname{d}}$
$\gdef\spaces#1{~ #1 ~}$

设 $f(x)$ 在区间 $[a, b]$ 上有定义, 将 $[a, b]$ 分成 $n$ 个子区间，分割点为 $a = x_0 < x_1 < x_2 < \cdots < x_n = b$, 每个子区间的长度为 $\Delta x_i = x_i - x_{i-1}$. 均匀分割时 $\Delta x_i = \frac{b-a}{n}$. 在每个子区间 $[x_{i-1}, x_i]$ 上任取一点 $x_i^*$, 定义 Riemann 和为 $S_n = \sum_{i=1}^n f(x_i^*) \Delta x_i$. 

在均匀分割 $\Delta x_i = \frac{b-a}{n}$ 下, Riemann 和可写成 $S_n = \frac{b-a}{n} \sum_{i=1}^n f(x_i^*)$, 再考虑

  - 取子区间的左端点 $x_i^* = x_{i-1}$, 有左 Riemann 和: 
    $$ S_n = \frac{b-a}{n} \sum_{i=0}^{n-1} f\left(a + i \cdot \frac{b-a}{n}\right) $$

  - 取子区间的右端点 $x_i^* = x_i$, 有右 Riemann 和: 
    $$ S_n = \frac{b-a}{n} \sum_{i=1}^n f\left(a + i \cdot \frac{b-a}{n}\right) $$
    特别的还可以令 $a=1$, $b=2$. 此时 $S_n$ 变为 $\frac{1}{n} \sum_{i=1}^n f\left(1+\frac{i}{n}\right)$. 

对于二元函数 $f(x,y)$ 在矩形区域 $[a,b]×[c,d]$ 上的二重积分, Riemann 和可以表示为:

$$
\iint_{[a,b] \times [c,d]} f(x, y) \d x \d y 
\spaces\approx \sum_{i=1}^n \sum_{j=1}^m f(x_i^*, y_j^*) \Delta x_i \Delta y_j
$$
