---
layout: competitive-programming-contest
subtitle: yukicoder contest 362
date: 2022-09-30
parent: competitive-programming-contest/
prev-child:
next-child: yukicoder-contest-367/
own: 単著
---

<div>
  {% for post in site.posts %}
    {% if post.blog-class != null %}{% if post.blog-class == page.subtitle %}
      <div class="content" id="{{ post.aname }}">
        <table border="1" rules="none" cellpadding="15">
          <tr>
            <th colspan="3" align="center">
              <h1>{{ post.order }} No.{{ post.num }} {{ post.title }}</h1>
            </th>
          </tr>
          <tr>
            <td>
              <p>問題リンク：<a href="https://yukicoder.me/problems/no/{{ post.num }}">https://yukicoder.me/problems/no/{{ post.num }}</a></p>
              <p>tester：{{ post.tester }}</p>
            </td>
          </tr>
          <tr>
            <td colspan="3">
              {{ post.content }}
            </td>
          </tr>
        </table>
      </div>
    {% endif %}{% endif %}
  {% endfor %}
</div>

