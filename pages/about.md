---
layout: page
title: About
keywords: 胡明昊，Minghao23
comments: true
menu: 关于
permalink: /about/
---

## 关于

我是胡明昊

一个兴趣广泛，热爱生活的人

我觉得人生就是不断学习的过程，而兴趣是学习最大的推动力

这里是一个分享知识，生活，见闻和理想的空间

期待着和你一起进步

## 联系

<hu_minghao@outlook.com>

## 社交媒体

{% for website in site.data.social %}
* {{ website.sitename }}：[@{{ website.name }}]({{ website.url }})
{% endfor %}
