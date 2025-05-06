---
layout: blog
title: yukicoder contest開催記リンク集
date: 2023-04-16
excerpt: "yukicoder contest開催記のリンク集です。"
parent: competitive-programming-blog
prev-child: 
next-child: introduction-to-competitive-programming
blog: true
tags: [競技プログラミング,数学]
---

yukicoderで
<ul>
  <li> コンテストを自分で開催した時の記録 </li>
  <li> 他の方が開催するオムニバス形式のコンテストに問題提供の形で参戦した時の記録 </li>
</ul>
へのリンク集です。出題意図を説明するために解法に触れることがありますので、ネタバレにご注意ください。（[問題一覧はこちら]({{ site.url }}/competitive-programming-problems/)）

{% for post in site.posts %}
{% if post.parent != null %}{% if post.parent == "competitive-programming-contest/" %}
- [{{ post.title }}]({{ site.url }}{{ post.url }})（{{ post.own }}）
{% endif %}{% endif %}
{% endfor %}
