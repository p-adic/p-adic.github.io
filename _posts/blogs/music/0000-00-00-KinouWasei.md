---
layout: blog
title: 機能和声の実装
date: 2020-01-12
excerpt: "機能和声の実装記事です。"
blog: true
tags: [音楽,機能和声,C++]
---

機能和声について勉強をしつつ、それを数式に翻訳してC++で実装していき、自動作曲を実行することを目標にします。この記事では機能和声の諸概念に対し
- 数式での翻訳
- C++で実装する際の宣言
- C++で実装する際の定義に要請する仕様

を述べていきます。実際の実装例は[C++ソースコード一覧]({{ site.url }}/cpp/)の該当箇所へのリンクを張らせていただきますが、全く同じ実装方法でなくても宣言が一致しており定義に要請する仕様さえ守っていれば最終目標の自動作曲まで実行できるするように展開していくつもりです。

{% for post in site.posts %}
{% if post.parent != null %}{% if post.parent == "KinouWasei/" %}
1. [{{ post.subtitle }}]({{ site.url }}/{{ post.url }})
  (
    {% for class in post.defined-class%}
      `{{ class }}`
    {% endfor %}
  )
{% endif %}{% endif %}
{% endfor %}

クラス索引：
{% for post in site.posts %}
{% if post.parent != null %}{% if post.parent == "KinouWasei/" %}
1. [{{ post.subtitle }}]({{ site.url }}/{{ post.url }})
{% endif %}{% endif %}
{% endfor %}

