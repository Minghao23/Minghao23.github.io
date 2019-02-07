---
layout: post
title: 隐狄利克雷分布（LDA）学习
class: Technology
categories: ["Machine Learning"]
keywords: LDA, 隐狄利克雷
---

LDA模型全程Latent Dirichlet Allocation，是文本语义分析中很著名的模型，其涉及的数学知识比较多，包括：Gamma函数，Dirichlet分布，共轭先验，MCMC，Gibbs采样，Variational Inference，贝叶斯文本建模等等。

看模型前需要抽时间补一下相关数学知识，不抠细节，只注重理解。本文大概记录一下知识点，大部分内容学习自Rickjin的[《LDA数学八卦》](https://blog.csdn.net/fengser/article/details/50682528)。

### **综述**
首先明确一下LDA的输入与输出：

<center><img src="/images/blog/lda1.png"></center>

LDA认为一篇文档是有多个主题的，而每个主题又对应着不同的词。一篇文档的构造过程，首先是以一定的概率选择某个主题，然后再在这个主题下以一定的概率选出某一个词，这样就生成了这篇文档的第一个词。不断重复这个过程，就生成了整篇文档。当然这里假定词与词之间是没顺序的。

LDA的使用是上述文档生成的逆过程，它将根据一篇得到的文档，去寻找出这篇文档的主题，以及这些主题对应的词。这里得到的是主题分布以及词分布，如果我们假设主题库和词库的存在，容易看出文档对主题就符合多项式分布，主题对词也符合多项式分布。例如某篇汽车的评论文档经过LDA模型得到的主题分布为0.7×汽车内饰+0.2×汽车外饰+0.3×汽车性能，其中汽车内饰=0.3×方向盘+0.2仪表盘+0.1×座椅+...

LDA是非监督的机器学习模型，并且使用了词袋模型。一篇文档将会用词袋模型构造成词向量。LDA需要我们手动确定要划分的主题的个数，超参数将会在后面讲述，一般超参数对结果无很大影响。

在继续理解模型前需要先了解两个在LDA中比较重要数学知识：MCMC和Dirichlet分布。在其他笔记里有写。

### **参数估计**
上面我们已经知道了topic分布和word分布都属于多项式分布，只是他们的参数（即概率）究竟是什么值我们还不知道，所以LDA模型的目的就是去估计topic分布和word分布的参数值。其中topic数是提前给定的，为K，word数为文档中出现过的所有word数，为V。我们可以用骰子来形象地表达一篇文档的生成过程：

>我们有两类骰子:
>
> - 第一类叫doc-topic骰子，一篇文档有一个，每面代表一个主题，共有K面，各个面的概率为$\vec\theta=(p_1,p_2,...,p_K)$。
> - 第二类叫topic-word骰子，一共有K个，每面代表词库里的一个词，共有V面。K个骰子的参数分别为向量$\vec\phi_1, \vec\phi_2,...,\vec\phi_K$
>
> 一篇文档的生成过程为：
>
> 1. 抛掷它的doc-topic骰子，得到主题编号z
> 2. 选择编号为z的topic-word骰子，得到词w
> 3. 不断重复步骤1和2直到生成所有词

### **极大似然估计**
根据样本，我们可以观测到的东西有文档d和文档里的词w。所以可以由此写出给定第m个文档下第i个词出现的概率：

$$
p(w_i|d_m)=\sum_{k=1}^{K}p(w_i|z_k)p(z_k|d_m)=\sum_{k=1}^{K}\phi_{ki}\theta_{mk}
$$

观察这个式子，其实前面就是词分布$\phi_{kj}$，后面就是主题分布$\theta_{mk}$
再由于我们假设词和词，文档和文档之间是独立的，所以每个文档出现的概率可以由每个词的概率连乘得到，进一步整个语料库L出现的概率就可以求每个文档出现的概率连乘得到。即为：

$$
L=\prod_m\prod_i\sum_{k=1}^{K}p(w_i|z_k)p(z_k|d_m)
$$

根据MLE，求使这个似然函数的值最大的参数就可以了，可以用EM算法求解。到这里为止，我们所讲的模型叫做PLSA模型。

### **贝叶斯估计**
PLSA因为用到了MLE，贝叶斯学派显然是不同意的，所有把参数定死了的方法都是耍流氓。贝叶斯思想认为主题分布和词分布一定是符合一个先验分布的，也就是说，骰子一定不是固定的，骰子本身也是一个符合某个分布的随机变量。由于主题分布和词分布都符合多项分布，所以先验分布一个好的选择就是Dirichlet分布（关于先验分布，参考笔记“Beta/Dirichlet分布”）。设$\theta\sim Dir(\alpha),\,\,\phi\sim Dir(\beta)$，于是我们就得到了LDA模型。LDA的概率图模型表示为：

<center><img src="/images/blog/lda2.png"></center>

图中的两个物理过程分别为：

 1. $\vec\alpha\longrightarrow\vec\theta_m\longrightarrow z_{m,n}$，即生成第m篇文档时，先从$Dir(\vec\alpha)$中生成一个$\vec\theta_m$，在从$Mult(\vec\theta_m)$中生成第n个词的topic索引$z_{m,n}$
 2. $\vec\beta\longrightarrow\vec\phi_k\stackrel{k=z_{m,n}}{\longrightarrow} w_{m,n}$，即对于第k个topic，先从$Dir(\vec\beta)$中生成一个$\vec\phi_k$，生成第m篇文档的第n个词时，在从$Mult(\vec\phi_k)$中生成第n个词$w_{m,n}$

显然，两个过程都是前面符合Dirichlet分布，后面符合多项式分布，所以整体是一个Dirichlet-Multinomial共轭结构。

$$
Dir(\vec{p}\,|\,\vec{\alpha}) + MultCount(\vec{m}) = Dir(\vec{p}\,|\,\vec{\alpha}+\vec{m})
$$

对于第一个过程，我们得到$\theta_m$的后验分布：

$$
p(\vec\theta_m|W,\vec\alpha)=Dir(\vec\theta_m|\vec{n}_m+\vec\alpha)
$$

根据Dirichlet分布的性质，我们取期望作为参数估计有:

$$
\hat{\vec\theta}_m =E(\vec\theta_m)=\left(\frac{n_1+\alpha_1}{\sum_{i=1}^{K}n_i+\alpha_i},\frac{n_2+\alpha_2}{\sum_{i=1}^{K}n_i+\alpha_i},...,\frac{n_K+\alpha_K}{\sum_{i=1}^{K}n_i+\alpha_i}\right)
$$

然后就可以进一步算出文档$z_m$的生成概率:

$$
p(\vec{z}_m|\vec\alpha)=\int{p(\vec{z}_m|\vec\theta_m)p(\vec\theta_m|\vec\alpha)d\vec\theta_m}=\frac{\Delta(\vec{n}_m+\vec\alpha)}{\Delta(\vec\alpha)}
$$

由于M篇文档相互独立，所以整个语料topics的生成概率：

$$
p(\vec{\mathbf{z}}|\vec\alpha)=\prod_{m=1}^M\frac{\Delta(\vec{n}_m+\vec\alpha)}{\Delta(\vec\alpha)}
$$

在真实的操作过程中，两个物理过程的顺序其实是不影响结果的，所以一般在所有单词的topic索引$z_{m,n}$全部生成完毕之后，再将同一主题的词分成一组，一起生成最后的$w_{m,n}$。同理，我们由共轭得到$\phi_k$的后验分布为：

$$
p(\vec\phi_k|W,\vec\beta)=Dir(\vec\phi_k|\vec{n}_k+\vec\beta)
$$

同以上步骤，得到整个语料words的生成概率：

$$
p(\vec{\mathbf{w}}|\vec{\mathbf{z}},\vec\beta)=\prod_{k=1}^K\frac{\Delta(\vec{n}_k+\vec\beta)}{\Delta(\vec\beta)}
$$

结合两式我们得到：

$$
p(\vec{\mathbf{w}},\vec{\mathbf{z}}|\vec\alpha,\vec\beta)=p(\vec{\mathbf{w}}|\vec{\mathbf{z}},\vec\beta)p(\vec{\mathbf{z}}|\vec\alpha)=\prod_{k=1}^K\frac{\Delta(\vec{n}_k+\vec\beta)}{\Delta(\vec\beta)}\prod_{m=1}^M\frac{\Delta(\vec{n}_m+\vec\alpha)}{\Delta(\vec\alpha)}
$$

### **Gibbs Sampling**
有了（w,z）的联合分布，也就是我们可观测到的数据分布，就可以使用Gibbs采样来估计分布了。关于Gibbs采样我了解的不是很详细，它是一种MCMC在高维上的优化方法，每次只在一个维度采样，其他维度固定。由于在训练时，$\vec{\mathbf{w}}$其实是观测到的已知数据，所以实际采样的是$p(\vec{\mathbf{z}}|\vec{\mathbf{w}})$，也就是隐变量的分布，每次根据Gibbs Sampling公式更新状态，也就是更新$\vec{\mathbf{z}}$，直到Gibbs采样收敛。最后我们就得到了真实的$\vec{\mathbf{z}}$的分布的样本。一顿推倒后，Gibbs Sampling公式为：

$$
p(z_i=k|\vec{\mathbf{z}}_{\lnot{i}},\vec{\mathbf{w}})\propto\hat{\theta}_{mk}\cdot\hat{\phi}_{kt}=\frac{n_{m,\lnot{i}}^{(k)}+\alpha_k}{\sum_{z=1}^{K}n_{m,\lnot{i}}^{(z)}+\alpha_z}\cdot\frac{n_{k,\lnot{i}}^{(t)}+\beta_t}{\sum_{v=1}^{V}n_{k,\lnot{i}}^{(v)}+\beta_v}
$$

以上公式可以解释为，初始时随机给文本中的每个单词分配topic,然后统计每个主题z下出现word t的数量以及每个文档m下出现的topic z中的词的数量。每一轮计算，即排除当前词的主题分配，根据其他所有词的主题分配估计当前词分配各个topic的概率。当得到当前词属于所有topic z的分布后，根据这个概率分布为该词sample一个新的topic。然后用同样的方法不断更新下一个词的主题，直到发现每个文档下的topic分布和每个topic下word的分布收敛，算法停止。Gibbs采样过程可以物理理解为在以下K个路径上采样。

<center><img src="/images/blog/lda3.png"></center>

### **训练和推断**
下面说一下实际操作中算法的流程。

#### **Training**

<center><img src="/images/blog/lda4.png"></center>

有了这个矩阵，$\theta$和$\phi$就都可以算了，统计每篇文档中topic的分布，就是主题分布，统计每个主题下每个词的出现概率，即为词分布。词分布$\phi$一般会作为模型参数储存下来，主题分布与原文档相关，在预测新文档的时候不需要，所以一般也没必要保留。通常在LDA训练时，会取收敛后n个迭代结果的平均值来做参数估计，这样模型质量更高一些。
对于新文档的主题预测，Inference的过程和Training基本完全类似，将Gibbs公式中的$\phi$认为是不变的模型参数，重复采样新文档直到收敛，最后的主题分布即为所求。

#### **Inference**

<center><img src="/images/blog/lda5.png"></center>

### **优点**

 1. 可以根据主题分布软聚类
 2. 每个主题会给出描述词和词分布
 3. 贝叶斯方法，更靠近真实情况

### **缺点**
LDA不太适用于短文本，因为在短文本中，P(z|d)的随机性就大太多了。以告警距离，一条告警文本分词处理后可能只剩5个词左右，相当于在当篇文档的doc-topic分布中取了五次样，样本量太少，即使分布收敛后随机性也比较强，这样得出的结果就不准了。可以考虑取分布稳定后几次迭代的均值作为真实分布。
