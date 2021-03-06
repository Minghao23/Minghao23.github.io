---
layout: post
title: 决策树总结
class: Technology
categories: ["Machine Learning"]
keywords: 决策树, Decision Tree, ID3
---

感觉找不到一篇好的关于决策树的总结，学习的时候太麻烦了，所以这里自己总结一下以便复习。

## **定义**
机器学习中，决策树是一个预测模型；他代表的是对象属性与对象值之间的一种映射关系。树中每个节点表示某个对象，而每个分叉路径则代表的某个可能的属性值，而每个叶结点则对应从根节点到该叶节点所经历的路径所表示的对象的值。决策树仅有单一输出，若欲有复数输出，可以建立独立的决策树以处理不同输出。

从数据产生决策树的机器学习技术叫做决策树学习, 通俗说就是决策树。

<center><img src="/images/blog/decisionTree1.jpg"></center>

既然有了决策树就可以对给定特征的问题进行预测，如何构建决策树就是我们要解决的核心问题。那么哪个特征做root？哪个特征接下来选择呢？由于构建出一个完全最优的决策树是一个NP-hard问题，所以我们只能根据启发式的算法尽可能的构建一个相对优的决策树。

构建决策树的过程也就是训练过程，这里会用到很多种算法，常用的有 ID3，C4.5 和 CART 决策树。其中 ID3 和 C4.5 决策树更倾向于处理类别型的离散属性值，对于连续型属性值，则需要额外利用连续属性离散化技术将其划分成离散型属性值。而 CART 决策树，即分类回归树，直接支持连续型属性值。这里只介绍ID3，其他的方法等用到了再添加。

## **ID3算法**
ID3算法是决策树的一种，它是基于奥卡姆剃刀原理的，即用尽量用较少的东西做更多的事。ID3算法，即Iterative Dichotomiser 3，迭代二叉树3代，是Ross Quinlan发明的一种决策树算法，这个算法的基础是奥卡姆剃刀原理，越是小型的决策树越优于大的决策树，尽管如此，也不总是生成最小的树型结构，而是一个启发式算法。

在信息论中，期望信息越小，那么信息增益就越大，从而纯度就越高。ID3算法的核心思想就是以信息增益来度量属性的选择，选择分裂后信息增益最大的属性进行分裂。该算法采用自顶向下的贪婪搜索遍历可能的决策空间。一般用于分类问题的决策树构建。

## **信息熵与信息增益**
在信息增益中，重要性的衡量标准就是看特征能够为分类系统带来多少信息，带来的信息越多，该特征越重要。在认识信息增益之前，先来看看信息熵的定义。

$$
H(S_l) = \sum_{i=1}^{\left|{y}\right|}-p_i \log_2(p_i)
$$

其中$p_i$是每个结果的出现概率，$y$是结果的总类别数。意思是一个变量的变化情况可能越多，那么它携带的信息量就越大。

信息增益是针对一个一个特征而言的，就是看一个特征，系统有它和没有它时的信息量各是多少，两者的差值就是这个特征给系统带来的信息量，即信息增益。计算公式及如下：

$$
IG(S\vert T) = Entropy(S)-\sum_{value(T)}\frac{\left|S_v\right|}{S}Entropy(S_v)
$$

其中$S$为全部样本集合，$value(T)$ 是属性$T$ 所有取值的集合，$v$ 是$T$ 的其中一个属性值，$S_v$ 是$S$ 中属性$T$的值为$v$的样例集合，$\vert S_v \vert$ 为$S_v$ 中所含样例数。其实后半部分相当于在$T$ 条件下$S$ 的所有分类的熵的期望。

在决策树的每一个非叶子结点划分之前，先计算每一个属性所带来的信息增益，选择最大信息增益的属性来划分，因为信息增益越大，区分样本的能力就越强，越具有代表性，很显然这是一种自顶向下的贪心策略。以上就是ID3算法的核心思想。

## **例子**
以根据天气预报决定是否打球的例子来说明。下面是描述天气数据表，学习目标是play或者not play。

<center><img src="/images/blog/decisionTree2.jpg"></center>

可以看出，一共14个样例，包括9个正例和5个负例。那么当前信息的熵计算如下

$$
Entropy(S)=-\frac{9}{14}log_2\frac{9}{14}-\frac{5}{14}log_2\frac{5}{14} = 0.940286
$$

在决策树分类问题中，信息增益就是决策树在进行属性选择划分前和划分后信息的差值。假设利用属性Outlook来分类，那么如下图

<center><img src="/images/blog/decisionTree3.jpg"></center>

划分后，数据被分为三部分了，那么各个分支的信息熵计算如下

$$
\begin{align*}
& Entropy(sunny)=-\frac{2}{5}log_2\frac{2}{5}-\frac{3}{5}log_2\frac{3}{5}=0.970951\\
& Entropy(overcast)=-\frac{4}{4}log_2\frac{4}{4}-0\cdot log_20=0\\
& Entropy(rainy)=-\frac{3}{5}log_2\frac{3}{5}-\frac{2}{5}log_2\frac{2}{5}=0.970951
\end{align*}
$$

那么划分后的信息熵为他们的期望（$Entropy(S\vert T)$ 为特征属性的条件下样本的条件熵）

$$
Entropy(S\vert T) = \frac{5}{14}\cdot 0.970951 + \frac{4}{14}\cdot 0+\frac{5}{14}\cdot 0.970951 = 0.693536
$$

则选择outlook的信息增益为

$$
IG(T) = Entropy(S) - Entropy(S\vert T) = 0.24675
$$

再以同样的方式计算选择其他特征的信息增益得到

$$
\begin{align*}
& IG(temperature) = 0.029\ bits\\
& IG(humidity) = 0.152\ bits\\
& IG(windy) = 0.048\ bits\\
\end{align*}
$$

最后选择信息增益最大的特征作为当前结点，然后再在每个分支下，根据当前的样例集以及特征信息熵，迭代的进行计算，直到某个特征下的信息为0（样例全为一类），或者满足剪枝的条件，或者达到人为设置的限制（最大深度，最多分支等）时，停止分支，决策树就建好了。

<center><img src="/images/blog/decisionTree4.jpg"></center>

## **过度拟合问题**
前面的算法生成的决策树非常详细并且庞大，每个属性都被详细地加以考虑，决策树的树叶节点所覆盖的训练样本都是“纯”的。因此用这个决策树来对训练样本进行分类的话，你会发现对于训练样本而言，这个树表现完好，误差率极低且能够正确得对训练样本集中的样本进行分类。训练样本中的错误数据也会被决策树学习，成为决策树的部分，但是对于测试数据的表现就没有想象的那么好，或者极差，这就是所谓的过拟合(Overfitting)问题。Quinlan教授试验，在数据集中，过拟合的决策树的错误率比经过简化的决策树的错误率要高。



现在问题就在于，如何在原生的过拟合决策树的基础上，生成简化版的决策树？可以通过剪枝的方法来简化过拟合的决策树。剪枝可以分为两种：预剪枝(Pre-Pruning)和后剪枝(Post-Pruning),下面我们来详细学习下这两种方法：

PrePrune：预剪枝，及早的停止树增长，方法可以参考见上面树停止增长的方法。

PostPrune：后剪枝，在已生成过拟合决策树上进行剪枝，可以得到简化版的剪枝决策树。

其实剪枝的准则是如何确定决策树的规模，可以参考的剪枝思路有以下几个：

1. 使用训练集合(Training Set）和验证集合(Validation Set)，来评估剪枝方法在修剪结点上的效用
2. 使用所有的训练集合进行训练，但是用统计测试来估计修剪特定结点是否会改善训练集合外的数据的评估性能，如使用Chi-Square（Quinlan，1986）测试来进一步扩展结点是否能改善整个分类数据的性能，还是仅仅改善了当前训练集合数据上的性能。
3. 使用明确的标准来衡量训练样例和决策树的复杂度，当编码长度最小时，停止树增长，如MDL(Minimum Description Length)准则。

关于剪枝的具体实现，等项目用到了再进行补充。
