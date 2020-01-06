---
layout: project
title: イラスト作品一覧
excerpt: "イラスト作品へのリンク集です。"
date: 2020-01-06
project: true
class-name: イラスト
tags: [イラスト]
---

<div>
  {% for post in site.posts %}
    {% if post.project-class != null && post.project-class == 'illustration' %}
      <div class="content" id="{{ post.aname }}">
        <table border="1" rules="none" cellpadding="15">
          <tr>
            <td width="40%">
              <img src = "{{ site.img }}/{{ post.aname }}-logo.png">
            </td>
            <td align="right">
              <p>最終更新日：</p>
              <p>最新話：</p>
            </td>
            <td>
              <p>{{ post.date | date: '%Y/%m/%d' }}</p>
              <p>{{ post.recent }}</p>
            </td>
          </tr>
          <tr>
            <td colspan="3" width="60%" align="center">
              <h2>最新イラスト紹介</h2>
            </td>
          </tr>
          <tr>
            <td colspan="3" valign="top">
              {{ post.excerpt }}
            </td>
          </tr>
          <tr>
            <td align="center">
              <a class="btn zoombtn" href="{{ post.url-ll }}">
                一覧を見る
              </a>
            </td>
            <td align="center">
              <a class="btn zoombtn" href="{{ post.url-final }}">
                最新イラストを見る
              </a>
            </td>
          </tr>
        </table>
      </div>
    {% endif %}
  {% endfor %}
</div>

