---
layout: post
title: MLE再再再再再理解
class: Technology
categories: ["Machine Learning"]
keywords: MLE
---

都是大学概率论没学好的锅，别人看一下就理解的东西我得理解好几次，还不算理解透，但是每次都算是进步吧。无力共勉，凑活看吧。

再次回到这个问题是因为偶然看了一个问题：**如何用极大似然估计解释线性回归中的最小二乘法？**

不会啊哈哈哈哈，没关系，学一哈，以后就会了。

首先对于似然函数的解释要再明确一下，似然函数是关于参数$\theta$的函数，在数值上等于某随机事件$X$在给定参数$\theta$下的概率。虽然好多教程里都把这个概率写作$P(X\vert \theta)$，但是我不太喜欢这种写法！这种写法默认了$\theta$也是一个随机变量，而在极大似然估计中，$\theta$不作为一个随机变量考虑，$\theta$是一个假设存在的固定值！也可以说是分布$P$的参数！所以我更喜欢把它写作下面的形式，同理似然函数L也应该这么写。这样写能消除我不少困惑，因为其实这就可以解释为$X$的**分布**了，或者$X$事件发生的**可能性**。

$$
L(\theta)=P(X;\theta)
$$

然后再来说一下我第二个困惑点，$X$是什么？网上对极大似然举的最多的例子就是抛硬币，这里$X$就是硬币正反面的概率，有$X=\{0,1\}$，参数是正面的概率$p$，符合二项分布。而在线性回归的极大似然推导里$L(\theta)=P(Y\vert X;\theta)$，为什么一会是$X$一会是$Y$呢。。

因为我们极大似然要算的是**某事件发生可能性最大时的参数**，在抛硬币中，事件是抛出硬币的正反面；而在一般分类问题中，事件是在数据$X$发生的情况下属于类别$Y$的概率；在线性回归中，事件是$X$条件下$Y$的连续概率分布。总之我们要建模的事件发生的可能性最大时参数才最好，跟$XY$没啥关系，如果非要把$Y$当做标签或者预测值的话，那抛硬币问题的$X$应该用$Y$来表示，而抛硬币的实验显然是没有任何特征的，只有结果变量。这是我之前比较困惑的地方。

所以就清楚了，$P(Y\vert X)$就是我们要建的模型$f(x)$嘛，如果我们已知$f(x)$的形式（或者是$Y\vert X$的分布）了，直接代进去求最大时的参数就好了，可以求导求，求不了就上EM嘛，总之就是优化问题了。

回到最初的问题，线性回归模型用最小二乘法来解，其实是用到了一个假设，就是模型预测值的误差是符合高斯分布的。于是模型可以写为

$$
y = P(y\vert X) + \epsilon = f(X) + \epsilon = \mathbf{w}^TX + \epsilon\\
\epsilon \sim \mathcal{N}(0, \sigma^2)
$$

所以有

$$
y \sim \mathcal{N}(\mathbf{w}^TX, \sigma^2)
$$

然后在对事件**在给定数据$X$下产生$y$**做最大对数似然估计，可以推出

$$
\begin{align}
L(\omega) & = \ln\prod^N_i{P(y_i\vert x_i;\mathbf{w})}\\
& = \ln\prod^N_i{\frac{1}{\sigma\sqrt{2\pi}}\exp(-\frac{(y_i-\mathbf{w}^Tx_i)^2}{2\sigma^2})}\\
& = \sum^N_i{\ln(\frac{1}{\sigma\sqrt{2\pi}}\exp(-\frac{(y_i-\mathbf{w}^Tx_i)^2}{2\sigma^2}))}\\
& = \sum^N_i{-\ln{\sigma\sqrt{2\pi}}-\frac{(y_i-\mathbf{w}^Tx_i)^2}{2\sigma^2}}\\
& = -N\ln{\sigma\sqrt{2\pi}} - \frac{1}{2\sigma^2}\sum^N_i{(y_i - \mathbf{w}^Tx_i)^2}
\end{align}
$$

容易看出，最大化似然函数其实就是最小化y的真实值与估计值的均方差，即最小二乘法。

相似的，Ridge回归其实就是考虑参数分布$\mathbf{w} \sim \mathcal{N}(0, \tau^2)$后$y\vert X$的最大后验估计。

Lasso回归其实就是考虑参数分布$\mathbf{w} \sim \mathcal{Laplace}(0, b)$后$y\vert X$的最大后验估计。

<center><img src="\images\blog\ridge_and_laplace.png"></center>

还有个要注意的地方，Lasso和Ridge用到的MAP所谓的后验是指参数$\theta$的后验，而不是预测值$y$的后验$y\vert X$，不管是MLE还是MAP还是Bayes都是参数估计方法，所示提到的似然和后验也都是参数的似然的后验。用上面的例子，线性回归就是在最大似然$L(\mathbf{w})=P(y\vert X;\mathbf{w})$;Lasso和Ridge就是在最大后验$P(\mathbf{w}\vert (y\vert X))=P((y\vert X)\vert \mathbf{w})P(\mathbf{w})$，此时$\mathbf{w}$被假设是一个随机变量了。

见过一段话特别好的总结了损失函数和MLE、MAP的关系：优化损失函数与正则项，其实代表的是对参数 w 的极大似然或者极大后验估计，不同的损失函数和正则项，反映的我们对参数先验分布和似然函数的不同假设。
