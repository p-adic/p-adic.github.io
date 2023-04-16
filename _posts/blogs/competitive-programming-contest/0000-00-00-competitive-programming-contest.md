---
layout: blog
title: yukicoder contest開催記リンク集
date: 2023-04-14
excerpt: "yukicoder contest開催記のリンク集です。"
blog: true
tags: [競技プログラミング,数学]
---

yukicoderでコンテストを開催した時の記録へのリンク集です。出題意図を説明するために解法に触れることがありますので、ネタバレにご注意ください。（[問題一覧はこちら]({{ site.url }}competitive-programming/)）

{% for post in site.posts %}
{% if post.parent != null %}{% if post.parent == "competitive-programming-contest/" %}
- [{{ post.subtitle }}]({{ site.url }}{{ post.url }})（{{ post.own }}）
{% endif %}{% endif %}
{% endfor %}
