---
layout: page
title: 作品タグ一覧
---

作品タグの一覧および、タグでソートされた作品一覧です。

{% capture site_tags %}{% for tag in site.tags %}{{ tag | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
{% assign tags_list = site_tags | split:',' | sort %}

<ul class="entry-meta inline-list">
  {% for item in (0..site.tags.size) %}{% unless forloop.last %}
    {% capture this_word %}{{ tags_list[item] | strip_newlines }}{% endcapture %}
    {% assign i = 0 %}
    {% for post in site.tags[this_word] %}
      {% if post.project || post.project-class != null %}
        {% assign i = i | plus:1 %}
      {% endif %}
    {% endfor %}
    {% if i != 0 %}
  	  <li><a href="#{{ this_word }}" class="tag"><span class="term">{{ this_word }}</span> <span class="count">i</span></a></li>
    {% endif %}
  {% endunless %}{% endfor %}
</ul>

{% for item in (0..site.tags.size) %}{% unless forloop.last %}
  {% capture this_word %}{{ tags_list[item] | strip_newlines }}{% endcapture %}
  <article>
  {% assign i = 0 %}
    {% for post in site.tags[this_word] %}
      {% if post.project || post.project-class != null %}
        {% assign i = i | plus:1 %}
      {% endif %}
    {% endfor %}
    {% if i != 0 %}
      <h2 id="{{ this_word }}" class="tag-heading">{{ this_word }}</h2>
      <ul>
      {% for post in site.tags[this_word] %}
	{% if post.project && post.title != null %}
          <li class="entry-title"><a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
        {% endif %}
      {% endfor %}
      {% for post in site.tags[this_word] %}
	{% if post.project-class != null && post.title != null %}
          <li class="entry-title"><a href="{{ site.url }}/{{ post.project-class }}/index.html#{{ post.aname }}" title="{{ post.title }}">{{ post.title }}</a></li>
        {% endif %}
      {% endfor %}
      </ul>
    {% endif %}
  </article><!-- /.hentry -->
{% endunless %}{% endfor %}
