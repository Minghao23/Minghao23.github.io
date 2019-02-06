---
layout: page
title: Wiki
description: 人越学越觉得自己无知
keywords: 维基, Wiki
comments: false
menu: 维基
permalink: /wiki/
---

## 永远记不住的命令和语法

<ul class="listing">
{% for wiki in site.wiki %}
{% if wiki.title != "Wiki Template" %}
<li class="listing-item"><a href="{{ site.url }}{{ wiki.url }}">{{ wiki.title }}</a></li>
{% endif %}
{% endfor %}
</ul>

## 超实用的网站

{% for website in site.data.bookmarks %}
* [{{ website.name }}]({{ website.url }})：{{website.desc}}
{% endfor %}
