
---
title: Taylor 展开
asref: true
tag: [](./index.md)
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$
$\gdef\case#1{\textbf{Case #1.}}$

定义 $\sum_{n \ge 0} \frac{f^{(n)}(a)}{n!}(x-a)^n$ 不做赘述. 主要展示推导常见函数 Maclaurin 展开的简单方法. 指数函数 $e^x = \sum_{n \ge 0} \frac{x^n}{n!}$ 用 $e^x \ge 1+x$ 一直积分即可, 且本身形式就简单, 此处不详细介绍. 以下方法也多次使用积分来计算原本需要求导得到的 Maclaurin 展开式系数, 从粗略的层面上看, 这是由于 [](./newton-leibniz.md) 的存在. 

$\case1$ 对于 $\sin x$ 和 $\cos x$, 我们应当去考虑 $e^{ix}$ 的 Maclaurin 展开 

$$
e^{ix} \spaces= 1 + ix + \frac{(ix)^2}{2!} + \frac{(ix)^3}{3!} + \cdots 
$$

且由于 $e^{ix} = \cos x + i\sin x$, 我们立刻得到

$$ \cos x \spaces= 1 - \frac{x^2}{2} + \frac{x^4}{4!} - \cdots \spaces= \sum_{n \ge 0} \frac{(-1)^n}{(2n)!} \cdot x^{2n} $$

$$ \sin x \spaces= x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots \spaces= \sum_{n \ge 0} \frac{(-1)^n}{(2n+1)!} \cdot x^{2n+1} $$

$\case2$ 随即使用截断项的多项式除法 

$$
\begin{array}{ll}
& \quad x + \frac{x^3}{3} \\
1 - \frac{x^2}{2} + \frac{x^4}{4!}
& \sqrt{x - \frac{x^3}{3!} + \frac{x^5}{5!}} \\
& \quad x - \frac{x^3}{2} + \frac{x^5}{4!} \\
& \text{------------------} \\
& \hspace{2.8em} \frac{x^3}{3} - \frac{x^5}{30} \\
& \hspace{2.8em} \frac{x^3}{3} - \frac{x^5}{6} \\
& \hspace{2.8em} \text{---------} \\
& \hspace{4.8em} \frac{2x^5}{15}
\end{array}
$$

这就给出 $\tan x = x + \frac{x^3}{3} + \frac{2x^5}{15} + \cdots$. 

$\case3$ 对于 $\log(1+x)$ 和 $\arctan x$, 可以考虑它们各自的积分定义 $\int \frac{\d x}{1+x}$ 与 $\int \frac{\d x}{1+x^2}$, 并将积分项展开为幂级数. 

$$
\begin{aligned}
\int \frac{\d x}{1+x} 
&\spaces= \int 1 - x + x^2 - x^3 + \cdots \d x \\
&\spaces= x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots \\
&\spaces= \sum_{n \ge 1} (-1)^{n+1} \frac{x^n}{n} 
\end{aligned}
$$

$$
\begin{aligned}
\arctan x &\spaces= \int \frac{\d x}{1+x^2} \spaces= \int \frac{\d x}{(1+ix)(1-ix)} \\
&\spaces= \int \Re (1-ix+(ix)^2+\cdots)(1+ix+(ix)^2+\cdots) \d x \\
&\spaces= \int 1 + (ix)^2 - (ix)^2 + (ix)^2 + (ix)^4 + \cdots \d x \\
&\spaces= \int 1 - x^2 + x^4 + \cdots \d x \\
&\spaces= x - \frac{x^3}{3} + \frac{x^5}{5} + \cdots \\
&\spaces= \sum_{n \ge 0} \frac{(-1)^n}{2n+1} x^{2n+1}
\end{aligned}
$$

或者注意 $\frac{1}{1+x^2} = \sum_{n \ge 0} (-x^2)^n = \sum_{n \ge 0} (-1)^n x^{2n}$, 立得 $\int \frac{\d x}{1+x^2} = \sum_{n \ge 0} \frac{(-1)^n}{2n+1} x^{2n+1}$. 

$\case4$ 这一类基本可以只观察 $\sqrt{1+x}$, 对此的工具是广义二项式定理

$$
(1+x)^\alpha \spaces= 1 + \alpha x + \frac{\alpha(\alpha-1)}{2!} x^2 + \cdots \spaces= \sum_{n \ge 0} \frac{\alpha^{\underline{n}}}{n!} x^n 
$$

这里 $\alpha^{\underline{n}}$ 是降阶乘或排列数 $\operatorname{P}_\alpha^n$, 或可简单记 $(1+x)^\alpha = \sum_{n \ge 0} {\alpha \choose n} $. 代入 $\alpha = \frac{1}{2}$, 立得 

$$ \sqrt{1+x} \spaces= 1 + \frac{1}{2}x - \frac{1}{8}x^2 + \cdots $$ 

类似地我们可以知道 $(1+x)^{-\frac{1}{2}} = 1 - \frac{1}{2}x + \frac{3}{8}x^2 - \cdots$. 顺带一提, Newton 本人就曾借助广义二项式定理得出过任意函数的 [](./taylor.md).

$\case5$ 对于 $\arcsin x$ 和 $\arccos x = \frac{\pi}{2} - \arcsin x$, 我们可以借助前面得到的 $(1-x^2)^{-\frac{1}{2}} \sim 1 + \frac{1}{2}x^2 + \frac{3}{8}x^4$ 和积分定义得到其展开式. 

$$ \arcsin x \spaces= \int \frac{\d x}{\sqrt{1-x^2}} \spaces= x + \frac{x^3}{6} + \frac{3}{40}x^5 + \cdots $$

$$ \arccos x = \frac{\pi}{2} - \arcsin x = \frac{\pi}{2} - x - \frac{x^3}{6} - \frac{3}{40}x^5 + \cdots $$
