---
layout: project
title: 競技プログラミング作問一覧
excerpt: "競技プログラミングの自作問題へのリンク集です。"
date: 2023-04-16
project: true
class-name: 競技プログラミング
tags: [競技プログラミング,プログラミング,数学]
---


[yukicoder公開済み問題一覧](https://yukicoder.me/users/5376/problems)

- レベル★1
  - [No.2184 A○B問題](https://yukicoder.me/problems/no/2184)
  - [No.2117 中国剰余定理入門](https://yukicoder.me/problems/no/2117)
- レベル★1.5
  - [No.2267 群の公理](https://yukicoder.me/problems/no/2267)
  - [No.2186 冪乗の片側極限](https://yukicoder.me/problems/no/2186)
  - [No.2185 平方数の下６桁](https://yukicoder.me/problems/no/2185)
  - [No.2118 遺伝的有限集合の数え上げ](https://yukicoder.me/problems/no/2118)
  - [No.2088 数当てゲーム](https://yukicoder.me/problems/no/2088)
  - [No.2087 基数の変換](https://yukicoder.me/problems/no/2087)
  - [No.2086 A+B問題](https://yukicoder.me/problems/no/2086)
- レベル★2
  - [No.2269 eN!の整数部分の下１桁](https://yukicoder.me/problems/no/2269)
  - [No.2268 NGワード回避](https://yukicoder.me/problems/no/2268)
  - [No.2188 整数列コイントスゲーム](https://yukicoder.me/problems/no/2188)
  - [No.2187 三立法和 mod 333](https://yukicoder.me/problems/no/2187)
  - [No.2130 分配方法の数え上げ mod 998244353](https://yukicoder.me/problems/no/2130)
  - [No.2119 一般化百五減算](https://yukicoder.me/problems/no/2119)
- レベル★2.5
  - [No.2271 平方根の１３桁精度近似計算](https://yukicoder.me/problems/no/2271)
  - [No.2270 T0空間](https://yukicoder.me/problems/no/2270)
  - [No.2189 六平方和](https://yukicoder.me/problems/no/2189)
  - [No.2090 否定論理積と充足可能性](https://yukicoder.me/problems/no/2090)
  - [No.2089 置換の符号](https://yukicoder.me/problems/no/2089)
- レベル★3
  - [No.2272 多項式乗算 mod 258280327](https://yukicoder.me/problems/no/2272)
  - [No.2191 一元二次式 mod 奇素数](https://yukicoder.me/problems/no/2191)
  - [No.2190 平方数の下１２桁](https://yukicoder.me/problems/no/2190)
- レベル★3.5
  - [No.2273 一点乗除区間積](https://yukicoder.me/problems/no/2273)
  - [No.2192 平方数の下１４桁](https://yukicoder.me/problems/no/2192)
  - [No.2121 帰属関係と充足可能性](https://yukicoder.me/problems/no/2121)
  - [No.2120 場合の数の下８桁](https://yukicoder.me/problems/no/2120)
- レベル★4
  - [No.2274 三角彩色](https://yukicoder.me/problems/no/2274)
  - [No.2193 メガの下１桁](https://yukicoder.me/problems/no/2193)
  - [No.2122 黄金比で擬似乱数生成](https://yukicoder.me/problems/no/2122)
- レベル★4.5
  - 未公開
- レベル★5
  - [No.2168 停止性問題（双頭ヒドラゲーム）](https://yukicoder.me/problems/no/2168)


コンテスト一覧（[開催記はこちら]({{ site.url }}competitive-programming-contest/)）
{% for post in site.posts %}
{% if post.parent != null %}{% if post.parent == "competitive-programming-contest/" %}
- [{{ post.subtitle }}](https://yukicoder.me/contests/{{ post.num }})（{{ post.own }}）
{% endif %}{% endif %}
{% endfor %}
