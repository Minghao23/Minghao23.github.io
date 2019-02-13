地址 https://arxiv.org/pdf/1503.00269.pdf

一种基于最大似然理论解决半监督学习问题的方法
contrastive：至少要达到使用有label的数据监督学习的结果
pessimistic：对于unlabel的数据要始终考虑最差的情形

Background
最大对数似然（生成模型）

$$
\begin{align*}
L(\theta \vert X) & = \sum_{i=1}^{N}{\log p(x_i,y_i \vert \theta)}\\
& = \sum_{k=1}^K\sum_{j=1}^{N_k}\log p(x_{kj},k \vert \theta)
\end{align*}
$$

有监督学习的ML

$$
\hat{\theta}_{sup}=\mathop{\arg\max}\limits_{\theta \in \Theta} L(\theta \vert X)
$$
