---
layout: single
author_profile: true
header:
  image: /assets/images/basa.jpg
# other options
---

<!-- # osks -->
<!-- ## 统计学

[ave](https://github.com/infinite-knowledge/infinite-knowledge.github.io/blob/master/_posts/%E5%B9%B3%E5%9D%87%E6%95%B0.md)

## Linux

## PowerShell

## VBA

## MATLAB

## 其他 -->
<ul>
  {% for post in site.posts %}
    <li><a href="{{post.url}}">{{post.title}}</a></li>
  {% endfor %}
</ul>





