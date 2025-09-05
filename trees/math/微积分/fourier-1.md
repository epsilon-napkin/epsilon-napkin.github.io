
---
title: Fourier 级数
---

$\gdef\spaces#1{~ #1 ~}$
$\gdef\d{\operatorname{d}}$

$f$ 是以 $2T$ 为周期的函数, 且在周期 $[-T,T]$ 上可积, 则

$$ a_n \spaces= \frac{1}{T} \int_{-T}^T f(x) \cos \frac{n\pi}{T} x \d x $$

$$ b_n \spaces= \frac{1}{\pi} \int_{-T}^T f(x) \sin \frac{n\pi}{T} x \d x $$

是 $f$ 的 fourier 系数. 以 fourier 系数所作的三角函数级数

$$ \frac{a_0 }{2} + \sum_{n \ge 1} a_n\cos \frac{n\pi}{T} x + b_n \sin \frac{n\pi}{T} x $$

称为 $f$ 的 fourier 级数. 
