---
layout: project
title: ワヘイヘイの日常
excerpt: "実在の数学者であり漫画家でもあるワヘイヘイさんを題材にした作品です。数学者の日常を描きました。"
parent: wheyhey-no-nichijou/
tags: 
---

<!DOCTYPE html>
<!--[if lt IE 7]><html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if (IE 7)&!(IEMobile)]><html class="no-js lt-ie9 lt-ie8"><![endif]-->
<!--[if (IE 8)&!(IEMobile)]><html class="no-js lt-ie9"><![endif]-->
<!--[if gt IE 8]><!--> <html class="no-js"><!--<![endif]-->
<head>
    {% include head.html %}
</head>
<body>
    {% include nav.html %}
    <!-- Header -->
    <header class="header" role="banner">
        <div class="wrapper animated fadeIn">
            <div class="content">
                <div class="post-title {% if page.feature %} feature {% endif %}">
                    <h1>{{ page.title }}</h1>
                    <h4>{{ page.date | date: '%Y/%m/%d' }}</h4>
                    {% if site.reading_time %}
                        <p class="reading-time">
                            {% include read-time.html %}
                        </p><!-- /.entry-reading-time -->
                    {% endif %}
                    <span style="padding : 10px">
                        <a class="btn zoombtn" href="{{ site.url }}">
                            トップページ
                        </a>
                    </span>
                    <span style="padding : 10px">
                        <a class="btn zoombtn" href="{{ site.url }}/{{ page.parent }}">
                            親記事
                        </a>
                    </span>
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/1.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/2.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/3.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/4.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/5.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/6.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/7.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/8.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/9.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/10.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/11.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/12.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/13.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/14.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/15.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/16.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/17.png">
                </div>
                <div>
                  <img src="{{ site.img }}/waheyhey-no-nichijou/18.png">
                </div>
                <div>
                    <span style="padding : 10px">
                        <a class="btn zoombtn" href="{{ site.url }}/{{ page.parent }}">
                            親記事
                        </a>
                    </span>
                </div>
            </div>
        </div>
    </header>
    {% include scripts.html %}
    {% if site.mathjax == true %}
    <!-- MathJax -->
    <script async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
    {% endif %}
</body>
</html>
