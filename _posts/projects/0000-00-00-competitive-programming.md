---
layout: project
title: 競技プログラミング作問一覧
excerpt: "競技プログラミングの自作問題へのリンク集です。"
date: 2023-11-09
project: true
class-name: 競技プログラミング
tags: [競技プログラミング,プログラミング,数学]
difficulty-list: [★,★☆,★★,★★☆,★★★,★★★☆,★★★★,★★★★☆,★★★★★]
---


{{ page.date | date: '%Y/%m/%d' }}現在の未公開問題は38問です。大半はtesterさんが見つかっておらず[こちらのツイート](https://twitter.com/non_archimedean/status/1738825428708803019)で募集中ですのでご応募くださると嬉しいです。

{% capture competitive-programming %}競技プログラミング{% endcapture %}
{% assign count-problem = 0 %}
{% for post in site.tags[competitive-programming] %}
  {% if post.blog-class != null %}{% if post.difficulty != null %}
    {% assign count-problem = count-problem | plus: 1 %}
  {% endif %}{% endif %}
{% endfor %}

以下はyukicoderの公開済み問題一覧（{{ count-problem }}問）です。[こちらのリンク](https://yukicoder.me/users/5376/problems)からもご確認いただけます。

{% for level in page.difficulty-list %}
  <ul>
    <li> 難易度：{{ level }} </li>
    <ul>
      {% for post in site.tags[competitive-programming] %}
        {% if post.blog-class != null %}{% if post.difficulty != null %}{% if post.difficulty == level %}
          <li> <a href="https://yukicoder.me/problems/no/{{ post.num }}">No.{{ post.num }} {{ post.title }}</a></li>
        {% endif %}{% endif %}{% endif %}
      {% endfor %}
    </ul>
  </ul>
{% endfor %}
<p>　</p>

コンテスト一覧（[開催記はこちら]({{ site.url }}/competitive-programming-contest/)）
{% for post in site.posts %}
{% if post.parent != null %}{% if post.parent == "competitive-programming-contest/" %}
- [{{ post.subtitle }}](https://yukicoder.me/contests/{{ post.num }})（{{ post.own }}）
{% endif %}{% endif %}
{% endfor %}
