---
layout: post
title: 有偏估计和无偏估计
class: Technology
categories: ["Machine Learning"]
keywords: 有偏估计, 无偏估计, 自由度
---

有偏估计是指由抽样后的样本值估计的某参数值与其真实值之间存在系统误差，误差由抽样产生。实践中因为只可能得到随机变量的样本，故优先使用无偏估计。这里解释一下为何有偏方差与无偏方差公式不同。

随机变量$X$的方差公式：

$$
\sigma^2=\frac{1}{N}\sum_{i=0}^N (X_i-\mu)^2
$$

这里的$\mu$为真实期望，在实际估计中是无法直接得到的，我们只能根据对随机变量抽样得到的样本，估计样本的平均值$\bar{X}$，再计算方差。但是请注意$\bar{X}$其实也是一个随机变量，因为每次抽样都会得到不同的平均值。根据

$$
\begin{align*}
& E(\frac{1}{N}\sum^N{}X) = \frac{1}{N}\sum^N{}E(X) = E(X)
\\
& D(\frac{1}{N}\sum^N{}X) = \frac{1}{N^2}\sum^N{}D(X) = \frac{1}{N}D(X)
\end{align*}
$$

可知$\bar{X}$是一个均值为$\mu$方差为$X$方差$\frac{1}{N}$的随机变量。因为我们想利用样本的$\bar{X}$来估计方差，所以我们把方差公式变形：

$$
\begin{align*}
\sigma^2 & = \frac{1}{N}\sum_{i=0}^N{((X_i-\bar{X})+(\bar{X}-\mu))^2}\\
& =\frac{1}{N}\sum_{i=0}^N{((X_i-\bar{X})^2+(\bar{X}-\mu)^2+2(X_i-\bar{X})(\bar{X}-\mu))}\\
& =\frac{1}{N}\sum_{i=0}^N{(X_i-\bar{X})^2}+\frac{1}{N}\sum_{i=0}^N{(\bar{X}-\mu)^2}+\frac{2(\bar{X}-\mu)}{N}\sum_{i=0}^N(X_i-\bar{X})
\end{align*}
$$

可以看出第三项的求和部分为0，所以第三项得0。第二项就是$(\bar{X}-\mu)^2$，如果M次抽样得到多个$\bar{X}$，这一项的期望即为$\frac{1}{M}\sum_{j=0}^M{(\bar{X}_j-\mu)^2}$也就是$\bar{X}$的方差$\frac{1}{N}\sigma^2$，所以：

$$
\sigma^2=\frac{1}{N}\sum_{i=0}^N{(X_i-\bar{X})^2}+\frac{1}{N}\sigma^2\\
=\frac{1}{N-1}\sum_{i=0}^N{(X_i-\bar{X})^2}
$$

这里的N-1又称为自由度，可以理解为本来是N维的自由度，受限于样本均值偏差的条件，变成了N-1维，具体暂时不予探究。
这就是用样本估计方差时要除以$N-1$的原因。
