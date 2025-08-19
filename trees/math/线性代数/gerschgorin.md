
---
title: Gerschgorin 圆盘定理
taxon: theorem
asref: true
tag: [](./index.md)
---

$\gdef\C{\mathbf{C}}$
$\gdef\spaces#1{~ #1 ~}$

熟知一个矩阵的特征值 $\lambda_i$ 一定会落在一个任意矩阵范数为半径, 原点为圆心的圆之内 [^norm]. 而 [](./gerschgorin.md) 就是一个借助矩阵分量给出特征值范围的定理, 其更进一步限制了特征值所落在的圆的信息, 可叙述如下. 

$\textbf{Theorem.}$ 设 $A = (a_{ij}) \in \C^{n \times n}$, 记 $r_i = \sum_{j = 1, j \ne i}^n |a_{ij}|$, 则 $A$ 的所有特征根都落在以下这 $n$ 个圆盘的并中

$$
\bigcup_{1 \le i \le n} \{ z \in \C : |z-a_{ii}| \le r_i \}
$$

这里的 $n$ 个圆直观地看就是: 以第 $i$ 个对角元素为圆心, 第 $i$ 行非对角元素的绝对值之和为半径的圆. 

#### 更进一步的阅读

- [估計特徵值範圍的 Gershgorin 圓 - 線代啟示錄](https://ccjou.wordpress.com/2010/10/29/%E4%BC%B0%E8%A8%88%E7%89%B9%E5%BE%B5%E5%80%BC%E7%AF%84%E5%9C%8D%E7%9A%84-gershgorin-%E5%9C%93/)
- [Gerschgorin 圆盘 - 中文数学 Wiki - Fandom](https://math.fandom.com/zh/wiki/Gerschgorin_%E5%9C%86%E7%9B%98)

[^norm]: 考虑矩阵 $A \in \C^{n \times n}$, 设 $\lambda$ 是 $A$ 的一个特征值, 对应非零特征向量为 $v$, 也即 $Av = \lambda v$. 取任意矩阵范数 $ \|\cdot\|$ 有 $$ |\lambda| \cdot \|v\| \spaces= \|\lambda v\| \spaces= \|Av\| \spaces\le \|A\| \cdot \|v\| $$ 这就表明 $|\lambda| \le \|A\|$, 从而特征值被任意矩阵范数控制. 
