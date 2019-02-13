---
layout: wiki
title: LaTeX Q&A
categories: LaTeX
description: LaTeX一些问题与解答
keywords: LaTeX
---

使用LaTeX时遇到的问题汇总。

### 竖线符号与Markdown语法冲突的问题

在Markdown文档中直接打 $\vert$ 和 $\parallel$ 时容易误认为是表格的语法，于是使用下面的LaTeX语法代替

| 语法      | 效果        |
| --------- | ----------- |
| \vert     | $\vert$     |
| \parallel | $\parallel$ |

### 多行公式的对齐
使用`\begin{align*}`和`\end{align*}`包围公式，`&`标记对齐点，`\\`换行

```LaTeX
\begin{align*}
3x + 4y & = 13\\
x + y & = 4 \\
2x & = 6\\
\end{align*}
```
$$
\begin{align*}
3x + 4y & = 13\\
x + y & = 4 \\
2x & = 6\\
\end{align*}
$$

### argmax设置下标的方法
使用`\mathop{}`将`\arg`和`\max`两个符号包装成一个符号，再使用`\limits_`添加为正下标
```LaTeX
\hat{\theta}_{sup}=\mathop{\arg\max}\limits_{\theta \in \Theta} L(\theta \vert X)
```
$$
\hat{\theta}_{sup}=\mathop{\arg\max}\limits_{\theta \in \Theta} L(\theta \vert X)
$$
