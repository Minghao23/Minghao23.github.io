---
layout: post
title: 谱聚类（Spectral Clustering）学习
class: Technology
categories: ["Machine Learning"]
keywords: Spectral Clustering
---

谱聚类是一种基于图论的聚类方法，其优点在于对数据集的要求较小，结果常常优于一般的聚类方法。简单来说，谱聚类可以分为构图和切图两个步骤。构图过程根据数据间的相似性将所有数据点构造成图 ，切图过程将图按照一定准则切成若干个子图，每个子图就是聚好的一个cluster。下面介绍详细过程，会涉及到一些线性代数的知识，注意本文所讨论的矩阵都默认是实矩阵。

<center><img src="/images/blog/spectral_example.png"></center>

## 构图

我们假设所有的数据构成一个有权无向图 $G=(V,E)$ ，$W=(w_{ij})$ 是图的权重邻接矩阵，因为是无向图，所以 $W$ 是对称阵，有 $w_{ij} = w_{ji}$ ，且 $w_{ij} = 0$ 表示 $v_i$ 与 $v_j$ 不相连。对于顶点 $v_i \in V$ ，定义顶点的度 $d_i = \sum_j^n w_{ij}$ ，即所有相连边的权重之和。进而定义度矩阵 $D$ 为以 $d_1 ... d_n$ 为对角线的对角阵。

定义 $V$ 的子集 $A \subset V$， $\overline A$ 为 $A$ 的补集。进而定义两种描述 $A$ 的大小的方式：

$$
\begin{align*}
& \vert A \vert := the\ number\  of\  vertices\  in\  A\\
& vol(A) = \sum_{v_i \in A} d_i\\
\end{align*}
$$

上述的定义都是由邻接矩阵W给出的，那我们怎么构造这个W呢？W包含了所有点对之间的权重，我们的目的就是切割较弱权重的边，保留较强权重的边，所以权重即相似度，W又称为相似度矩阵。一般来说，有三种方法可以得到相似度矩阵，前两种方法构造出的是稀疏矩阵，对数据量特别大的情况能够有效提升效率，但同时也会损失很多信息。第三种方法是无信息损失的。

#### The $\varepsilon$-neighborhood graph

计算所有点对的欧式距离 $dist(i,j)$ ，设置一个阈值 $\varepsilon$ ，并简单的定义

$$
w_{ij} =
\begin{cases}
1,  & \mbox{if }dist(i,j) \leq \varepsilon \\
0, & \mbox{if }dist(i,j) > \varepsilon
\end{cases}
$$

如此就得到了一个无权无向图，虽然计算变简单了很多，但是也损失了大量的信息。

#### k-nearest neighbor graph

类似kNN中近邻的定义，只选取每个点最近的k个近邻点相连，其余权重置0。但是这样会导致 $w_{ij} \neq w_{ji}$ ，使图变为有向图。解决方案有两个，一个是直接忽略方向，相连条件是 $v_i \in kNN(v_j)\ or \ v_j \in kNN(v_i)$ ；另一个是只保留互为邻居的连接，即 $v_i \in kNN(v_j)\ and \ v_j \in kNN(v_i)$ 。此时权重的大小包含的信息也可以忽略，同样会得到一个无权无相图。

#### The fully connected graph

全连接所有的点，使用高斯相似度作为权重。

$$
w_{ij} = e^{\frac{-{\parallel x_i - x_j \parallel}^2}{2 \sigma^2}}
$$

其中 $\sigma$ 控制了领域的宽度，比较离散的数据可以选取大一点 $\sigma$ 。使用全连接的方法构图，聚类效果会更准确一点，但是效率偏低，需要根据具体情况衡量。

## 拉普拉斯矩阵及其性质

拉普拉斯矩阵（Graph Laplacian）是谱聚类所应用到的主要工具，它描述了图的很多潜在特征，在聚类、降维、分类等很多领域都有应用。其定义为

$$
L = D - W
$$

其中D是度矩阵，W是上一小节构造出来的邻接矩阵。在有权和无权图中都可以定义拉普拉斯矩阵。在后面的推导中，我们会用到拉普拉斯矩阵如下的一些性质：

1. 对于任意向量 $f \in \mathbb{R}^n$ ，有

$$
f^TLf=\frac{1}{2}\sum_{i,j=1}^nw_{ij}(f_i-f_j)^2
$$

2. L是对称矩阵，且是半正定的。
3. L最小的特征值是0，对应的特征向量为全1向量。
4. L有n个非负的实特征值，且 $0 \leq \lambda_1 \leq \lambda_2 \leq ... \leq \lambda_n$

对于性质1，推导过程如下：

$$
\begin{align*}
f^TLf & = f^TDf - f^TWf \\
& = \sum_{i,j}f_if_jD_{ij} - \sum_{i,j}f_if_jW_{ij} \\
& = \sum_i{f_i}^2d_{i} - \sum_{i,j}f_if_jw_{ij} \\
& = \frac{1}{2}(\sum_i{f_i}^2d_{i} - 2\sum_{i,j}f_if_jw_{ij} + \sum_j{f_j}^2d_{j}) \\
& = \frac{1}{2}(\sum_{i,j}{f_i}^2w_{ij} - 2\sum_{i,j}f_if_jw_{ij} + \sum_{i,j}{f_j}^2w_{ij}) \\
& = \frac{1}{2}\sum_{i,j}w_{ij}(f_i - f_j)^2
\end{align*}
$$

第一行应用了L的定义。

第二行，因为D和W都是对称矩阵，所以 $f^TDf$ 和 $f^TWf$ 都是 $f$ 的二次型表示。（含有n个变量 $x_1, x_2,...,x_n$ 的二次齐次多项式成为二次型，可以用对称矩阵A唯一表示为 $x^TAx$ 的形式，且有 $x^TAx=\sum_{i,j}x_ix_jA_{ij}$ ）

第三行，因为D是由 $d_1, d_2, ..., d_n$ 组成的对角阵，所以 $D_{ij} = 0\ (i \neq j)$

第四行到第五行，因为度矩阵的定义 $d_i = \sum_jw_{ij}$

由性质1的结论，显然有 $f^TLf \geq 0$，所以很容易得到性质2，即L是半正定的。半正定的性质则保证了L所有的特征值都是大于等于0的，即性质4，这些特征值其实是有一定含义的，这也是拉普拉斯矩阵可以用来描述图的理论依据。

对于性质3，我们通过L的定义可以得知L每行的和都是0，那么显然，如果L左乘一个全1向量，结果必然是0。因此L必然有一个全1的特征向量，其对应特征值为0，又因为L是半正定的，所以这个0特征值也一定是L最小的特征值。

其实拉普拉斯矩阵通常会用在判断一个图包含多少连通子图上，**其特征值为0特征向量的个数即为图中连通子图的个数，且每个特征向量即为对应连通子图的指示向量**。让我们解释一下这个定理，假设一个图是由k个连通子图组成的，我们先考虑 k=1 的情况，即图是全连通的。假设u是特征值为0的特征向量，由性质1可得：

$$
u^TLu = u^T \cdot 0 \cdot u = 0 \\
u^TLu = \frac{1}{2}\sum_{i,j=1}^nw_{ij}(u_i-u_j)^2
$$

对于相连的两点 $v_i$ 和 $v_j$ ，$w_{ij}$ 一定是大于0的，那么想让上式等于0，特征向量就一定要满足 $u_i = u_j$ 。而又因为全连通图中任意两点都是连通的，所以最后所有的 $u_i$ 都应该是相等的，取常数1，即得到全1向量。

再考虑 k>1 的情况，此时图中包含k个连通子图，因为顶点的顺序并不会失去一般性，我们在构造L矩阵的时候将同一子图的点放在一起，最后可以得到一个“块对角”的矩阵，形如：

$$
\begin{bmatrix}
L_1 &&&  \\
& L_2 && \\
&& \ddots & \\
&&& L_k
\end{bmatrix}
$$

其中每个 $L_i$ 都是对应连通子图的一个拉普拉斯矩阵，块与块之间没有连接，所以空白的地方都是0。我们的目标依旧是找到特征值为0的特征向量。对于第i个子图的 $L_i$ ，根据 k=1 的情况，使这部分特征值为0的 $u_i$是一个全1的向量，那么如果想让整体L的特征值也为0，把u的其他位置补上0即可，这样就找到了一个特征值为0的特征向量。我们还发现，这个特征向量值为1的部分，就是子图的顶点们，所以它也天然就是这个子图的指示向量。同理，有多少个子图，我们就能找到多少个这样的特征值为0的特征向量，而由于 $w_{ij}$ 的存在，也无法找到更多的特征值为0的特征向量。因此可以理解为，拉普拉斯矩阵的0特征值个数，就是图中连通子图的个数。其实我们通常就用图的拉普拉斯矩阵倒数第二个特征值是否大于0来判断这个图是否是全连通的图，这个值也成为图的代数连通度（algebraic connectivity）。

以上是拉普拉斯矩阵的介绍，作为预备知识，之后会讲到它如何与谱聚类的切图产生联系。

## 切图

接下来的问题是，如何将图切成合理的子图（聚类后的簇）呢？直觉上的想法是，我们要尽量去切那些权重低的边，并尽量使子图内边的权重都足够大，这也是谱聚类的核心思想。这一节会解释谱聚类是如何解决这个问题的。

对于两个不相交的子集 $A,B \subset V$ ，我们定义

$$
cut(A, B) = \sum_{i \in A, j \in B} w_{ij}
$$

假设我们想切出k个子集，如果使每个子集间的cut都足够小，就是要最小化下式

$$
cut(A_1, ..., A_k) = \sum_{i=1}^kcut(A_i, \overline A_i)
$$

那么，如果我们直接去最小化这个式子，很容易出现一个问题，就是算法会倾向于把弱连接的单个顶点切出去。因为这个式子其实只考虑了子集之间的权重关系，而没有考虑子集内部的权重大小。所以我们还要增加约束条件使每个切出去的子集内部要“规模足够大”。两个常用的解决方案是RatioCut和Ncut。RatioCut使用子集内的顶点数来衡量子集大小，而Ncut使用子集内的边权重和来衡量子集大小，它们分别定义为

$$
\begin{align*}
& RatioCut(A_1, ..., A_k) = \sum_{i=1}^k \frac{cut(A_i, \overline A_i)}{\vert A_i \vert} \\
& Ncut(A_1, ..., A_k) = \sum_{i=1}^k \frac{cut(A_i, \overline A_i)}{vol(A_i)} \\
\end{align*}
$$

可以看出，这两个式子也不是要求每个子集规模越大越好，而是倾向于使每个子集规模相同，达到一种平衡。而找到这种平衡条件被证明是一个NP-hard的问题，接下来我们看看大神们是如何找到了一个近似的方法来解决这个问题的。

### RatioCut

RatioCut考虑了目标子图的大小，避免了单个样本点作为一个簇的情况发生，平衡了各个子图的大小。RatioCut的目标同样是最小化各子图的连边权重和

$$
min\ \  RatioCut(A_1, ..., A_k)
$$

这里我们引入**切图后**各个子图 $\{A_1, ..., A_k\}$ 的指示向量 $h_i \in \{h_1, ..., h_k\}$ ，具体为

$$
h_{ij} =
\begin{cases}
\frac{1}{\sqrt{\vert A_i \vert}},  & \mbox{if }v_j \in A_i \\
0, & \mbox{if }v_j \notin A_i
\end{cases}
$$

其中i是子集的下标，j是样本的下标。当第j个样本属于第i个子集时， $h_{ij} = \frac{1}{\sqrt{\vert A_i \vert}}$ ，否则为0。这个数值也保证了每个 $h_i$ 的模始终为1。接着我们用这个指示向量代入到拉普拉斯矩阵的性质1公式里，看看可以得到什么。

$$
\begin{align*}
h_i^TLh_i & = \frac{1}{2}\sum_m\sum_n w_{mn}(h_{im} - h_{in})^2 \\
& = \frac{1}{2} (\sum_{m \in A_i, n \in \overline A_i} w_{mn}(\frac{1}{\sqrt{\vert A_i \vert}} - 0)^2 + \sum_{m \in \overline A_i, n \in A_i} w_{mn}(0 - \frac{1}{\sqrt{\vert A_i \vert}})^2) \\
& = \frac{1}{2} (\sum_{m \in A_i, n \in \overline A_i} w_{mn}\frac{1}{\vert A_i \vert} + \sum_{m \in \overline A_i, n \in A_i} w_{mn}\frac{1}{\vert A_i \vert}) \\
& = \frac{1}{2} (cut(A_i, \overline A_i)\frac{1}{\vert A_i \vert} + cut(\overline A_i,  A_i)\frac{1}{\vert A_i \vert}) \\
& = \frac{cut(A_i, \overline A_i)}{\vert A_i \vert} \\
& = RatioCut(A_i, \overline A_i)
\end{align*}
$$

第二行，可以分为 $(m \in A_i, n \in \overline A_i) (m \in \overline A_i, n \in A_i) (m \in A_i, n \in A_i) (m \in \overline A_i, n \in \overline A_i)$ 四种情况，但是后两种情况根据 $h_i$ 的定义显然有 $h_{im} = h_{in}$ ，所以那些项为0，只剩下前两种情况。第四行是 cut 的定义，是对称的。第六行是 RatioCut 的定义。

我们最后发现，通过引入指示向量，拉普拉斯矩阵竟然能够用来表示RatioCut了！那么我们也许就可以利用拉普拉斯矩阵的一些性质来实现最小化RatioCut的目标。更进一步的，对所有子集计算总的RatioCut，需要引入指示矩阵 $H \in \mathbb{R}^{n \times k}$ ，其中每一列都是一个 $h_i$ ，根据 $h_i$ 的定义，有 $H^TH = I$ 。进而可以用 $H$ 来表示RatioCut

$$
\begin{align*}
RatioCut(A_1, ..., A_k) & = \sum_{i=1}^k h_i^TLh_i \\
& = \sum_{i=1}^k (H^TLH)_{ii} \\
& = Tr(H^TLH)
\end{align*}
$$

Tr表示对角线求和。最后我们将这个极小化问题转化为了

$$
\mathop{\arg\min}\limits_{H} \ \ Tr(H^TLH), \ \ \ \ s.t.\ H^TH = I
$$

注意我们只需要找到一个H使整个式子最小就可以了，因为H包含了每个子集的指示变量，计算出了H也就知道了如何去切图。之前提到过，因为共有 $k*2^n$ 种情况，所有找出这样合适的H是一个NP-hard问题。论文里提到了一个Rayleigh-Ritz theorem，可以**选择L矩阵的前k小的特征值**，再离散为二值向量作为每个 $h_i$ ，这样得到的H就是符合条件的，且把问题的规模从n降到了远小于n的k。为什么可以这么做呢？这里我们不去探究更深入的证明，从特征值的角度去简单的理解一下。因为 $h_i$ 为单位正交基，所以$h_i^TLh_i$ 的最小值是L的最小特征值0，最大值是L的最大特征值。回忆一下PCA，我们的目标是去找协方差矩阵的最大特征值，协方差矩阵是对数据进行描述，各个维度为数据各个特征，所以最大特征值的方向就对应着所有数据共同具有的特征方向。而在谱聚类中，拉普拉斯矩阵是对类进行描述，各个维度为类所包含的数据，所以最大特征值方向就对应着所有类共同具有的数据方向。较小特征值的方向则对应着每个类独有的数据方向，也就是我们最求的代价最小的切割方式。这也帮助我们理解了拉普拉斯矩阵能够通过特征值识别分离连通子图的特性。

得到前k个特征向量后，可以将它们按列排成一个矩阵 $V \in \mathbb{R}^{n \times k}$ 。对于一个全连通的图，去掉最小的0特征值，我们得到的前k个特征向量一定是连续实值的向量，并不能直接作为一个标准的二值指示器，但是其中已经蕴含了类别指示的信息。所以还要对V的每一行做聚类，每行 $(y_i)_{i=1, 2, ..., n}$ 是一个顶点，其特征是它对于每个类的符合程度。所以把它们再聚成k个类，才可以得到真正的one-hot的指示矩阵。因为这里k是给定的，所以一般直接使用kmeans即可。

讲了这么多，都是一些理论的证明和理解，回头看一下会发现算法的实现其实十分简单。见下图

<center><img src="/images/blog/spectral_ratiocut_procedure.png"></center>

### Ncut

Ncut的切法其实与RatioCut基本相似，只是把分母从边数换成了子集内权重和。这样带来的好处是会使L变成归一化的矩阵，这对聚类的过程其实是有好处的。Ncut的指示向量 $h_i$ 定义为

$$
h_{ij} =
\begin{cases}
\frac{1}{\sqrt{vol(A_i)}},  & \mbox{if }v_j \in A_i \\
0, & \mbox{if }v_j \notin A_i
\end{cases}
$$

这种定义为H带来了一种新的约束条件，即 $H^TDH = I$ 。证明如下

$$
\begin{align} h_{i}^{T}Dh_{i} & =\sum_{n=1}h_{i,n}^{2}D_{n,n}  \\
　　& =\sum_{v_{n} \in A_{i}}\frac{1}{vol(A_{i})}D_{n,n} + \sum_{v_{n} \notin A_{i}}0\cdot D_{n,n} \\
　　& = \frac{1}{vol(A_{i})}\sum_{v_{n} \in A_{i}}w_{v_{n} } + 0 \\
　　& = \frac{1}{vol(A_{i})}vol(A_{i}) \\
　　& = 1
　　\end{align}
$$

类似于RatioCut的推导，我们可以得到Ncut的最小化目标

$$
\mathop{\arg\min}\limits_{H} \ \ Tr(H^TLH), \ \ \ \ s.t.\ H^TDH = I
$$

设 $U=D^{\frac{1}{2}}H$ ，我们把这个最小化目标变化一下

$$
\begin{align*}
H^TLH & = (D^{-\frac{1}{2}}U)^TLD^{-\frac{1}{2}}U \\
& = U^TD^{-\frac{1}{2}}LD^{-\frac{1}{2}}U \\
\\
H^TDH & = (D^{-\frac{1}{2}}U)^TDD^{-\frac{1}{2}}U \\
& = U^TD^{-\frac{1}{2}}DD^{-\frac{1}{2}}U \\
& = U^TD^{-\frac{1}{2}}D^{\frac{1}{2}}D^{\frac{1}{2}}D^{-\frac{1}{2}}U \\
& = U^TIIU \\
& = U^TU

\end{align*}
$$

令 $L_{sym} = D^{-\frac{1}{2}}LD^{-\frac{1}{2}}$ ，则最小化目标变成了

$$
\mathop{\arg\min}\limits_{H} \ \ Tr(U^TL_{sym}U), \ \ \ \ s.t.\ U^TU = I
$$

其中，$L_{sym}$ 就是对拉普拉斯矩阵进行了标准化，具体为 $\frac{L_{ij}}{\sqrt{vol(A_i)vol(A_j)}}$ ，这么做的一个好处就是对L中的元素进行标准化处理使得不同元素的量纲得到归一。具体理解就是，同个子集里，不同样本点之间的连边可能大小比较相似，这点没问题，但是对于不同子集，样本点之间的连边大小可能会差异很大，做这一步标准化操作，可以将L中的元素归一化在[-1,1]之间，这样量纲一致，对算法迭代速度，结果的精度都是有很大提升。

于是我们发现，得到 $L_{sym}$ 后，求解方式就和RatioCut一样了，选取 $L_{sym}$ 的前k个特征值即可。另外一点与RatioCut不同的是，这些特征向量在聚类前还需要做一下归一化，即

$$
u_{ij} = \frac{v_{ij}}{(\sum_k v_{ik}^2)^{\frac{1}{2}}}
$$

原因是，RatioCut得到的 $L$ 的特征向量直接可以作为指示向量矩阵 $H$ ，但是Ncut得到的 $L_{sym}$ 的特征向量得到的是 $D^{\frac{1}{2}}H$ 矩阵，每个 $u_i$ 根据 $d_i$ 的不同有很大区别，比如一个度特别小的顶点i，得到的 $u_i$ 也一定很小，而与它相连的顶点j，得到的 $u_j$ 却很大，算法就很难把两个点归为一类。所以这时要对每行做标准化，使每个顶点对每个类的归属度这个概念保持数值上的一致，再用kmeans聚类才能找到合理的聚类结果。

Ncut的流程见下图。

<center><img src="/images/blog/spectral_ncut_procedure.png"></center>

以上就是谱聚类的理论内容。sklean库里已经有了谱聚类的实现，看完这篇文章对其中的参数应该也有深刻的认识了。参数对聚类效果的影响其实很大，需要慢慢实验理解，有时间会在这里补充调参过程。

## 参考

大部分的内容都可以从**第一个链接中的文章**找到，讲解的可以说十分细致了。谱聚类其实可以从很多角度进行解释，是一个比较完美的数学模型，有时间可以再研究一下从马尔可夫链随机游走角度对谱聚类的解释。

<https://www.cs.cmu.edu/~aarti/Class/10701/readings/Luxburg06_TR.pdf>

<https://blog.csdn.net/yc_1993/article/details/52997074>

<https://blog.csdn.net/hx14301009/article/details/80203717>
