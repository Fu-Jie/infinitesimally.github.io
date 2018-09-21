---
layout: single
author_profile: true
header:
  overlay_image: /assets/images/pink.jpg
  overlay_filter: rgb(12,200,50,0.8) # rgb和透明度
  image_description: 欢迎那到这里!
  caption: "this[**TEST**](https://www.sina.com)"
  actions:
    - label: "Download"
      url: "/assets/images/pink.jpg"
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





