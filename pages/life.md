---
layout: life
title: Life Articles
description: 生活文章分类
keywords: 生活, 分类
comments: false
menu: 生活
permalink: /life/
---

{% assign this_class = "Life" %}

<section class="container posts-content">
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
    {% assign display = 0 %}
    {% for post in category.last %}
        {% if post.class == this_class %}
            {% assign display = 1 %}
            {% break %}
        {% endif %}
    {% endfor %}
    {% if display == 0 %}
        {% continue %}
    {% endif %}
    <h3>{{ category | first }}</h3>
    <ol class="posts-list" id="{{ category[0] }}">
    {% for post in category.last %}
        {% if post.class != this_class %}
            {% continue %}
        {% endif %}
        <li class="posts-list-item">
        <span class="posts-list-meta">{{ post.date | date:"%Y-%m-%d" }}</span>
        <a class="posts-list-name" href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>
        </li>
    {% endfor %}
    </ol>
{% endfor %}
</section>
<!-- /section.content -->

<!-- /this_class -->

