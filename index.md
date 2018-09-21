---
layout: single
author_profile: true
header:
  overlay_image: /assets/images/pink.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "this[**TEST**](https://python.com)"
  actions:
    - label: "Download"
      url: "https://github.com"
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





