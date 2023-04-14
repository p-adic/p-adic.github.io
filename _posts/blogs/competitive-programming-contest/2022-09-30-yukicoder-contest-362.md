---
layout: blog-child
title: yukicoder contest 362開催記
subtitle: yukicoder contest 362
date: 2022-09-30
excerpt: "yukicoder contest 362の開催記です。"
blog: true
parent: competitive-programming-contest/
prev-child:
next-child: yukicoder-contest-367/
own: 単著
tags: [競技プログラミング,数学]
---


<div>
  {% for post in site.posts %}
    {% if post.blog-class != null %}{% if post.blog-class == page.subtitle %}
      <div class="content" id="{{ post.aname }}">
        <table border="1" rules="none" cellpadding="15">
          <tr>
            <th colspan="3" align="center">
              <h1>{{ post.order }}: {{ post.title }}</h1>
            </th>
          </tr>
          <tr>
            <td>
              <p>問題URL：https://yukicoder.me/problems/no/{{ num }}</p>
              <p>tester：{{ post.tester }}</p>
            </td>
          </tr>
          <tr>
            <td colspan="3">
              {{ post.body }}
            </td>
          </tr>
        </table>
      </div>
    {% endif %}{% endif %}
  {% endfor %}
</div>

