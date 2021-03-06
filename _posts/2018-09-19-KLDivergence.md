---
layout: post
title: 理解KL散度
class: Technology
categories: ["Machine Learning"]
keywords: KL Divergence, KL散度
---

## **一句话定义**
是一种量化两种概率分布P和Q之间差异的方式，又叫相对熵。

我们经常会用一种更简单的近似的分布来替代观察数据或太复杂的数据，KL散度帮助我们度量使用一个分布来近似另一个分布时所损失的信息。

$$
D_{KL}(p\parallel q)=\sum_{i=1}^N{p(x_i)\ \log{\frac{p(x_i)}{q(x_i)}}}
$$

其中p为观察到的原始概率分布，q为近似分布。

我们知道当log以2为底的时候，熵是衡量一个数据的最小二进制编码位数。也可以以此度量数据蕴含的信息量。当我们使用另一种概率分布来近似原始数据分布的时候，信息一定会发生缺失，KL散度就是用来度量这种信息缺失的。

## **交叉熵**
再复习一下交叉熵。假如我们用分布q去近似分布p来编码，每个取值的信息量会发生变化，但是总体期望仍然是关于真实分布p的，所以交叉熵定义为用q来表示数据所蕴含的信息量，当以2为底时为用q表示数据分布时需要的比特数：

$$
H(p,q)=-\sum_i{p(x_i)\ \log q(x_i)}
$$

交叉熵一定是大于等于熵的，因为错误的分布q会带来更多的信息冗余。于是，从公式就可以很容易推出相对熵（即KL散度）即为交叉熵减原始熵。当相对熵越小的时候，近似分布越接近原始分布。注意KL散度并不相当于距离的概念，因为距离是对称的概念，但根据公式明显有 $KL(p\parallel q)\neq KL(q\parallel p)$。

## **KL散度的用途**
我们知道了如何去衡量近似分布对原始分布的接近程度，就可以以此为基准选择不同的分布来近似原始数据。当近似分布含有参数时，还可以用于选择最佳的参数。所以用神经网络去学习概率分布时，可以将KL散度作为模型的loss function，来训练模型参数。VAE就是这个思路。

平滑：计算过程中如果由于数据缺失遇到log0的情况，一般选择一个比较小的数，比如 $10^{-3}$，替代0。

其实我们熟悉的一般的NN都是使用交叉熵作为损失函数，这是因为在神经网络涉及的范围内，原始分布p的熵是固定的， $KL(p\parallel q)=H(p,q)-H(p)$ 此时最小化交叉熵等价于最小化KL散度。

## **计算 $KL(p\parallel q)$ 和 $KL(q\parallel p)$ 的区别**
在尝试使用KL散度优化时，不同的优化方向可以经验性的认为有如下特性
 $KL(p\parallel q) = - \int{p(x)\log q(x)} - H(p)$ ,我们优化的是参数化的q,当p的值较大时，相应q的值一般要要求较大，这样才能让 $KL(p\parallel q)$ 的值变小，也就是说q会拟合p比较大的值的地方但是可能的副作用是在p比较小的值处q值也比较大，相反当我们优化 $KL(q\parallel p)$ 时, $KL(q\parallel p) = - \int{q(x)\log p(x)} - H(q)$ 此时需要H(q)的值尽量大但是在p比较小的位置q也要比较小，也就是说这种优化方向趋向于在p比较小的位置q也比较小，副作用是在p比较大的位置q也可能会比较小,具体可参考下图。

![](/images/blog/1546085176285_2 2.png)
