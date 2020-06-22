---
layout: post
title: 基于TextCNN的恶意URL检测实现
class: Technology
categories: ["Machine Learning"]
keywords: TextCNN URL Pytorch
---

## 网络安全之恶意URL检测：基于 TextCNN 的实现

恶意URL的检测一直是网络安全中经久不衰的话题。网络诈骗者将恶意URL嵌入到不同的渠道中，引诱受害者进入钓鱼网站，进而采取一系列的违法活动，换言之，恶意URL成为了许多网络攻击活动的入口。对于公司而言，建立恶意URL的识别和屏蔽机制就是架起了网络安全防范的第一道门。在攻击方的反监测技术越来越强的趋势下，传统的基于规则的解决方案逐渐不可用，机器学习的方案成为了效果更好的选择。在实际场景下，URL文本是公司所能获取的唯一数据，所以文本分类模型是一个直观的实现思路。

文本分类模型可以分为传统的机器学习模型（如朴素贝叶斯，逻辑回归，SVM 等）和深度学习模型（fastText，TextCNN，Bert 等）。相比于传统机器学习方法，深度学习的优势在于可以替代一部分特征工程的工作，当然也需要更大的数据量和更高的性能开销来支持。其中，TextCNN 在短文本分类任务上的表现已经获得了业界的认可，URL 作为一种理想的短文本数据，直观上使用 TextCNN 进行分类可以实现一个不错的效果。本文将从 TextCNN 的模型介绍入手，使用真实的数据集，详细介绍URL检测的整体流程，并辅以 PyTorch 的代码实现进行说明。

### TextCNN 模型介绍

TextCNN 是在 Yoon Kim 在他 2014 年的论文 [Convolutional Neural Networks for Sentence Classification](https://arxiv.org/abs/1408.5882) 中提出的。模型借鉴了在图像领域大获成功的卷积神经网络，将其使用在了自然语言领域。TextCNN 的经典的结构是：输入层-卷积层-池化层-全连接层-输出层。其网络结构如下。

<center><img src="/images/blog/textcnn_structure.png"></center>

#### 输入层

类似于处理图像的 CNN 模型，TextCNN 的输入也是一个二维的矩阵。不同的是，图像数据样本通常有 RGB 三个通道，而文本数据是单通道的。这个输入矩阵的行数为分词后文档的长度，列数为词向量的维度。为了适应输入矩阵的长度，输入的文本数据需要进行合适的预处理使其长度固定。输入矩阵的宽度是词向量的维数，需要通过词嵌入的方式得到，在下面的具体实现中，会进一步介绍本例所采用的词嵌入的方式 word2vec。在图示的例子中，输入矩阵是一个 7 * 5 的矩阵。

#### 卷积层

接下来是卷积层。TextCNN 所使用的的卷积核与传统CNN的区别是，卷积核的宽度是与输入矩阵等宽的。这是因为，卷积核在文本模型中的作用是捕获不同区域上下文之间的关系，上下文的信息储存在输入矩阵的列方向上，而输入矩阵的行涵盖了词向量的所有特征信息，是不需要做卷积的。因此，一个长度为 k 的卷积核对长度为 n 的输入矩阵做卷积之后，输出的矩阵维度应该是 (n - k + 1, 1)。

在图示的例子中，卷积层使用了三种长度的卷积核，分别是 2，3，4。每种卷积核各两个。多种长度的卷积核可以抽取到更多的上下文特征，且为了使损失函数收敛，每个卷积核会倾向于学习不同的特征。如果考虑到句子边缘 token 的影响，这里还可以为输入矩阵增加上下方向的 padding value，此时输出矩阵会变长。

矩阵在卷积操作后会经过一个激活函数实现网络的非线性映射，一般选用 ReLU 激活函数。

#### 池化层

卷积层的输出会接入一个 1-Max pooling 层，值得注意的是，池化层的 filter 与卷积层的输出（池化层的输入）是等长等宽的。这意味着池化层会直接选择矩阵中的最大值作为输出，这个输出浓缩了对应卷积核所提取的所有信息。卷积层每个通道的输出都会池化为一个值，最后会将这些单个的值拼接起来形成一个向量。

#### 全连接层

全连接层的设置是为了整合数据并输出分类标签。输入是一个向量，输出是用于二分类的向量。为了对网络正则化，这里一般会对网络参数进行 Dropout 操作。因为在设计上全连接层不参与特征提取，所以这一层直接采用线性函数即可。

#### 输出层

分类问题的输出层一般使用 softmax 函数，将输出映射为概率。

TextCNN 的结构就是如此简单，有时候为了扩大卷积核的感受野，可以多叠几层卷积层，但是核心的思想基本不变。下面让我们结合代码看看在真实的URL检测例子中是怎样使用它的。

### 恶意URL检测的实现

#### 问题定义

URL检测的目标是使用分类器将恶意的URL和善意的URL分类。如果将URL看作由字母、数字和符号组成的文本，这个问题就转变为了短文本的分类。在实际场景中，恶意URL会仿照知名公司的域名关键字欺骗用户，或者在链接中加入随机的字符扰乱读者。正常的URL则通常有一定的规则，一定的参数，或者一定的语义性等。在数据集充足的情况下，深度学习模型可以自动挖掘出这些特征。

#### 数据集

实验数据集是从这里获取的，本例从中选取了正样本和负样本各 50000 个，并以 7:3 的比例分为了训练集与测试集。

#### 数据处理和特征工程

文本分类的第一件事就是数据的预处理和分词。常见的英文文本带有空格可以自动分割语义单元，但URL是没有的。一个容易想到的方式是直接按照字符分词，但是这个方式会带来如下问题。第一，字符没有明显的上下文语义特征，词嵌入的效果很差。第二，以字符分割的文本过长，经过池化层后会损失掉大量信息。因此本例采用了另一个方案，根据特殊符号进行分词。在URL中，很多符号都是有明确意义的，比如“?”用于连接路径与参数，“=”用于连接参数的键值等等。那么使用这些特殊符号分词，就可以提取出一定有意义的 token 来。分词后还需要做一些必要的数据清理，例如去除空字符串，字母小写化等。

使用本例的训练集分词后，Vocabulary 的大小达到了 10 万左右。按照词频排序后发现，前 1000 个词的词频大于 50，前 5000 个词的词频大于 9，前 10000 个词的词频大于 5，整体的分布较为分散。因为低词频的 token 对分类不具有参考性，所以本例只考虑前 10000 个词作为有效的 token，其余的低频词和测试集中的未知词都标为 [unk]。

接下来是词嵌入的过程，本例使用 word2vec 模型生成词向量。word2vec 是考虑前后相邻词的词嵌入模型。例如，I like basketball 和 I love basketball 都在语料中经常出现，那么 like 和 love 的词向量就会很接近。word2vec 有两种经典的实现方法，CBOW 的输入是前后相邻词，输出是当前词，Skip-gram 的输入是当前词，输出是前后相邻词。以 CBOW 为例，模型结构是一个三层线性神经网络（如下图）。训练 like 时，输入 I 和 basketball 的 one-hot 向量，经过一个隐藏层，输出 like 的 one-hot 向量。所有语料训练完成后，一个 token 输入网络后隐藏层的向量即作为此 token 的词向量。模型本质上一个降维过程。其中可调节的超参数有词向量的维度和定义前后词的窗口，本例使用的是 64 和 2 （前后各 2 个）。Python 的 gensim 库提供了很方便的 word2vec 实现。

<center><img src="/images/blog/textcnn_word2vec.png"></center>

由于 TextCNN 的网络输入是一个定长宽的矩阵，所以每个 URL 训练样本都需要处理为等长的 token list。对本例分词后所有的训练样本做统计后发现，样本长度的99分位数为 31，为了简便，本例取 30 作为输入矩阵的行数，短的补零，长的截断。

数据处理与特征工程的具体代码如下。

```python
class FeatureEngineering(object):
    split_chars = ['.', '\-', '?', '=', '&', '#', '_', ';', '/']  # “-”在正则里有特殊含义，故使用转义符转义

    def tokenize(self, x):
        """
        对原始文本进行分词和处理
        """
        tokens = re.split('[{}]'.format(''.join(self.split_chars)), x)
        tokens = list(filter(lambda tok: tok != '', tokens))  # 去除空字符
        tokens = list(map(lambda tok: tok.lower(), tokens))  # 字母变小写
        return tokens

    def gen_vocab(self, tokens, size=10000):
        """
        根据词频生成词典
        """
        count_result = nltk.FreqDist(samples=tokens)
        valid_tokens = count_result.most_common(size - 1)
        self._vocab = set(list(zip(*valid_tokens))[0])  # set类型

    def mark_unk(self, word_corpus):
        """
        标记低频词和未知词为 [unk]
        """
        new_corpus = []
        for tokens in word_corpus:
            # handle empty docs
            if len(tokens) == 0:
                new_corpus.append(['[unk]'])
                continue
            new_tokens = list(map(lambda tok: '[unk]' if tok not in self._vocab else tok, tokens))
            new_corpus.append(new_tokens)
        return new_corpus

    def gen_corpus_tensor(self, word_corpus):
        """
        生成适合网络输入的张量
        """
        max_len = Config.input_len  # 30

        # generate tensor
        corpus_tensor = []
        for tokens in word_corpus:
            sentence_matrix = []
            for tok in tokens:
                sentence_matrix.append(self.w2v_model[tok])  # 词向量
            if len(sentence_matrix) > max_len:
                sentence_matrix = np.array(sentence_matrix[:max_len])  # 截断
            else:
                sentence_matrix = np.pad(sentence_matrix, ((0, max_len - len(sentence_matrix)), (0, 0)), 'constant')  # 补零
            corpus_tensor.append(sentence_matrix)
        return np.array(corpus_tensor)

    def fit_transform(self, corpus):
        tokens = []
        word_corpus = []
        for doc in corpus:
            cur_tokens = self.tokenize(doc)
            word_corpus.append(cur_tokens)
            tokens.extend(cur_tokens)
        self.gen_vocab(tokens)
        word_corpus = self.mark_unk(word_corpus)
        self.w2v_model = Word2Vec(word_corpus, size=Config.embed_dim, window=Config.embed_window, min_count=0, workers=4)
        X = self.gen_corpus_tensor(word_corpus)
        return X

    def transform(self, corpus):
        word_corpus = []
        for doc in corpus:
            cur_tokens = self.tokenize(doc)
            word_corpus.append(cur_tokens)
        word_corpus = self.mark_unk(word_corpus)
        X = self.gen_corpus_tensor(word_corpus)
        return X
```

#### 模型搭建

本例完全按照基础的 TextCNN 模型结构搭建。参数如下：

```python
class Config(object):
    input_len = 30
    embed_dim = 64
    embed_window = 2
    n_class = 2
    n_channel = 1
    n_kernel = 2
    kernel_lens = (2, 3, 4)
    dropout = 0.3
    epoch_num = 100
    lr = 0.1
```

本例使用了 3 种卷积核，可以使用 nn.ModuleList 一起注册。注意卷积核的宽度要与输入矩阵的列数相等，池化层的长度要与卷积层输出矩阵的长度相等。在 PyTorch 种，卷积层的输入是一个 (batch_size, n_channel, height, width) 的张量，在本例中 n_channel 是 1。因为每种卷积核使用了两个，所以每个卷积操作的输出 n_channel 是 2。

全连接层的输入长度是所有的卷积核数，在本例是 3 * 2 = 6 个，输出长度是分类数量，在本例是 2 个（正样本或负样本）。最后用 softmax 函数将输出转化为概率值。

具体代码如下，为了更容易理解，在 forward 函数中，用本文的例子注释了运算张量 shape 的变化。

```python
class TextCNN(nn.Module):

    def __init__(self):
        super(TextCNN, self).__init__()

        self.convs = nn.ModuleList([
            nn.Sequential(
                nn.Conv2d(in_channels=Config.n_channel, out_channels=Config.n_kernel,
                          kernel_size=(kernel_len, Config.embed_dim)),
                nn.ReLU(),
                nn.MaxPool2d(kernel_size=(Config.input_len - kernel_len + 1, 1))
            )
            for kernel_len in Config.kernel_lens
        ])
        self.dropout = nn.Dropout(Config.dropout)
        self.fc = nn.Linear(Config.n_kernel * len(Config.kernel_lens), Config.n_class)
        self.sm = nn.Softmax(0)

    def forward(self, x):
        # x: (70000, 1, 30, 64)
        batch_size = x.size(0)
        out = [conv(x) for conv in self.convs]
        # out: [(70000, 2, 1, 1), (70000, 2, 1, 1), (70000, 2, 1, 1)]
        out = torch.cat(out, dim=1)  # concat on channel dim
        # out: (70000, 6, 1, 1)
        out = out.view(batch_size, -1)
        # out: (70000, 6)
        out = self.dropout(out)
        # out: (70000, 6)
        out = self.fc(out)
        # out: (70000，2)
        return out
```

#### 训练

接下来选择合适的 epoch 轮次和 learning_rate 训练。需要注意的是，训练前要把输入向量的形状变成卷积层接受的输入形状。损失函数选用二分类问题常用的交叉熵损失函数，配合 softmax 的概率输出，简化梯度下降过程。

```python
def train_textcnn(net, train_X, train_y):

    # np.array -> torch.Tensor
    X = torch.from_numpy(train_X.astype('float32'))
    y = torch.from_numpy(train_y.astype('long'))  # target_label 必须为 Long
    n, h, w = X.shape
    X = X.view(n, 1, h, w)  # channel 设为 1，适应网络输入

    net.train()
    optimizer = optim.Adam(net.parameters(), lr=Config.lr)
    loss_func = nn.CrossEntropyLoss()
    for i in range(Config.epoch_num):
        optimizer.zero_grad()
        output = net(X)
        loss = loss_func(output, y)
        loss.backward()
        optimizer.step()
        print("Epoch {}/{}: loss = {}".format(i + 1, Config.epoch_num, str(loss.item())))
```

#### 测试

预测时选择输出层最大值的索引作为预测的类标签，忽略 dropout，反向传播等操作。

```python
def test_textcnn(net, test_X):
    X = torch.from_numpy(test_X.astype('float32'))
    n, h, w = X.shape
    X = X.view(n, 1, h, w)

    net.eval()  # 自动忽略 dropout 等操作
    with torch.no_grad():
        outputs = net(X)
        _, y_pred = torch.max(outputs.data, 1)  # 返回 tuple(最大值（忽略），最大值的索引即预测类)

    return y_pred
```

### 效果评估

使用本例的数据集训练并测试，得到了 0.927 的 F1-score 和 0.932 的 AUC。效果与传统的机器学习方法（如逻辑回归和随机森林）持平。经过思考有如下几个改进的方向。第一，URL 文本 token 呈长尾分布，大部分的低频 token 无法得到很好的词向量，在模型中被忽略，而他们有时反而是分类的重要特征。可以考虑采用其他特征选择方式筛选特征，如卡方检验等。第二，在卷积操作时，由于 [unk] 太多，卷积核无法有效的提取有意义的 token 之间的特征。这个问题可以通过增加一层卷积层来改善。第三，数据集太小或样本不均匀。深度学习模型在大批量高质量的数据上效果提升明显，且泛化性更强。如何采集、处理、储存数据在工程实践上的重要性不亚于模型设计，往往模型效果的上限也是由数据和特征工程来决定的。

