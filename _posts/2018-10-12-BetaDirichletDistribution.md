---
layout: post
title: Beta/Dirichlet分布
class: Technology
categories: ["Machine Learning"]
keywords: Beta, Dirichlet, Distribution
---

## **Gamma函数**
$$
\begin{align*}
\Gamma(x) & = \int_{0}^{\infty}t^{x-1}e^{-t}dt
\\
\Gamma(n) & = (n-1)!
\end{align*}
$$

可以把Gamma函数当做阶乘在实数集上的延拓

## **Beta/Dirichlet分布**
$$
\begin{align*}
Beta(p\,|\,\alpha,\beta) & =\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}p^{\alpha-1}(1-p)^{\beta-1}
\\
Dir(\vec{p}\,|\,\vec{\alpha}) & =\frac{\Gamma(\sum_{k=1}^{K}\alpha_k)}{\prod_{k=1}^{K}\Gamma(\alpha_k)}\prod_{k=1}^{K}p_k^{\alpha_k-1}
\end{align*}
$$

都是定义在(0,1)区间内的连续概率分布，在贝叶斯估计的时候，Beta分布可以作为二项分布的共轭先验分布，Dirichlet分布可以作为多项分布的共轭先验分布，且在估计时这两个分布的参数都具有物理意义。Beta分布可以看做Dirichlet分布在参数为一维时的特殊形式。

### **共轭先验**
贝叶斯推断：

> $先验分布 + 实验数据 \rightarrow 后验分布$

如果后验分布与先验分布属于同类，则先验分布与后验分布被称为共轭分布，而先验分布被称为似然函数的共轭先验。
若实验数据（似然函数）符合二项分布，则Beta分布可以作为先验，后验分布仍为Beta分布。且后验分布可以由新的实验数据直接更迭得到：

> $Beta(a, b) + 实验数据 \rightarrow Beta(a + 成功次数, b + 失败次数)$

同理Dirichlet分布相当于Beta分布在高维的延拓，变量变为向量$\vec{p}$，参数变成了向量$\vec\alpha$，$\vec\alpha$同样具有物理计数意义，此时似然函数应符合多项分布。

$$
Dir(\vec{p}\,|\,\vec{\alpha}) + MultCount(\vec{m}) = Dir(\vec{p}\,|\,\vec{\alpha}+\vec{m})
$$

### **Beta/Dirichlet分布的一个性质**
对于符合Beta分布的随机变量，其均值可以估计为：
$$
E(p)=\frac{\alpha}{\alpha+\beta}
$$
对于符合Dirichlet分布的随机变量，其均值可以估计为：
$$
E(\vec{p})=\left(\frac{\alpha_1}{\sum_{i=1}^K\alpha_i},\frac{\alpha_2}{\sum_{i=1}^K\alpha_i},...,\frac{\alpha_K}{\sum_{i=1}^K\alpha_i}\right)
$$
