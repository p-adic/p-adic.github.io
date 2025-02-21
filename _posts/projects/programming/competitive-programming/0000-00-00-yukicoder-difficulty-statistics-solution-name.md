---
layout: project
title: yukicoder過去問解法別難易度統計の解法名解説
date: 2024-12-23
excerpt: "yukicoderの過去問の解法別難易度統計ページに記載した解法名の解説です。"
project: true
parent: competitive-programming-project/
prev-child: yukicoder-difficulty-statistics
next-child: 
image-directory: 
tags: [競技プログラミング,数学]
---


[yukicoderの過去問の解法別難易度統計のページ]({{ site.url }}/yukicoder-difficulty-statistics)で用いた、一般的でない解法名の解説ページです。

　
{% assign solution = "不明な想定解" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

解説が存在しないために明らかにされていない想定解を構成する、何かしらの手法。少なくとも実装だけはwriter提出を見れば分かるが、どのような考察（特に正当性の証明）がなされたかが非公開となる。

　
{% assign solution = "解法場合分け" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

入力が大きい場合と小さい場合で別の解法を取る手法。

- $O(B)$解と$O(N/B)$解がある時に$B \leq \sqrt{N}$か否かで解法を切り替える$O(\sqrt{N})$解
- $O(N)$解と$N > M$の時のみ有効な$O(1)$解がある時に$N \leq M$か否かで解法を切り替える$O(M)$解

などが典型。

　
{% assign solution = "良いケースに帰着" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

操作を伴う問題で、初期状態に依存した値を計算する問題を考える。

- 初期状態から１・２回の操作を行うと必ず良い初期状態に遷移する場合
- 最終状態を全探索し、最終状態を変更した上で操作を逆順に実行した時に良い初期状態に戻れる場合

などで一般の１ケースを良い初期状態を持つ有限個のケースに帰着させる手法。

再帰の特別な例だが、再帰深度がせいぜい２程度であり一般の再帰と区別するため、良いケースに帰着させる問題は他に非自明な再帰を行わない限り再帰の問題として集計しない。

　
{% assign solution = "総和計算の期待値への帰着" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

何らかの集合$S$とその部分集合$U$と$S$上の関数$f$が与えられた時に、$U$上での$f$の値の総和$\sum_{u \in U} f(u)$を求める問題を考える。

- もちろん$U = S$としても良く、$S$と$U$を分けているのはその方が計算しやすい（$U$より$S$の方が全探索しやすい）状況があるため。
- $f$が$U$の特性関数$\chi_U$である時、$U$の要素数の数え上げ問題である。

$f$の値の総和を直接求める代わりに、$S$の要素$s$の一様ランダムなサンプリングをした時の$f(s) \chi_U(s)$の期待値を求めてそれに$S$の要素数を掛ける手法。

- $U = S$である時は、$f(s)$の期待値を求めてそれに$S$の要素数を掛けることになる。
- $f = \chi_U$である時は、$s \in U$となる確率$p$を求めてそれに$S$の要素数を掛けることになる。例えば以下の状況で有効になる。
  - $P$が独立事象の積事象で表せ、確率を積で計算しやすい場合。
  - $p$が自然に和に分解され、期待値の線形性が適用しやすい場合。

　
{% assign solution = "損をしない変形" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

何らかの価値を最大化する（またはコストを最小化する）組み合わせ最適化を考える。

可能な操作全体のうち、適当な条件$P$を満たす操作のみに絞って考えれば良いことを示すために「任意の操作$X$に対し、条件$P$を満たすある操作$X'$が存在して、$X'$の価値は$X$の価値以上である」ということを示す手法。

- 非自明な貪欲法の正当性を証明する。
- 可能な操作全体の集合が大きすぎるために、考える操作の個数に計算量が依存する既存のアルゴリズム（全探索、グラフアルゴリズム、動的計画法、etc.）が使えない状況で、最適な操作を少なくとも１つ含む部分集合を構成し、それに対してアルゴリズムを適用する。

などといった目的で使われる。枝刈りの特別な例だが、他に非自明な枝刈りを行わない限り枝刈りの問題として集計しない。

　
{% assign solution = "操作を数値に翻訳" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

いくつかの操作が与えられ、

- 操作を継続できる回数の最大化
- 操作を繰り返すことによって条件が達成できるか否かの判定と、達成できる時の操作回数の最小化
- 操作を繰り返すことによって得られる項の
  - 数え上げ
  - 最大・最小化

などを行う問題を考える。

操作を数値の固定長有限列に翻訳することで、forループなどによる操作の全探索を可能にする手法。

　
{% assign solution = "操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

複数種類の操作と正整数$K$が与えられ、操作を高々$K$回繰り返すことによって項$x$が得られるか否かを判定する問題を考える。

項$x$を得るために必要な操作回数の最小値$f(x)$を決定し、$f(x) \leq K$か否かを判定する手法。

一見当たり前だが、操作が複数種類であれば$K$回以下適用する方法は一意でなく指数関数的に増えるため$K$回以内に得られる項全体の集合は計算が困難である一方で、$x$に注目して$x$のみから一意に定まる数値である$f(x)$の計算に帰着させる考察は見落としやすいかもしれない。

　
{% assign solution = "breakに関する考察" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

全探索や明示式の計算などでループを行う際、最後までループを続けると実行時間制限を超えてしまったりオーバーフローを起こしてしまったりする状況で、

- ループを途中で打ち切れること。
- 打ち切った場合に実行時間制限に間に合うことや、オーバーフローを回避できること

を考察すること。

- $10^9$個の要素から解を探す際、鳩の巣原理で少なくとも$10^6$要素集めれば解があることが分かっている場合は最初の$10^6$個の探索でループを打ち切れば良い。
  - $\oplus$を有限可換群演算として、$\bigoplus_{i=\ell}^{r} A_i = 0$かつ$0 \leq \ell < r < N$を満たす組$(\ell,r)$の構築時にこのような考察が要求される。
  - $x \neq y$かつ$f(x) = f(y)$を満たす解$(x,y)$の構築時にこのような考察が要求される。
- $f(x) < K$を満たす$x \in S$の個数や最大の$x \in S$を求める際、$f(x)$が非負値関数の和で表される時は和を計算していく過程で値が$K$を超えた時点で即座に計算を打ち切れば良い。
  - $f(x) \geq K$を満たす場合の$f(x)$の計算量が大きい場合は高速化になる。
  - $f(x)$の値がオーバーフローしうる場合はオーバーフロー回避になる。

　
{% assign solution = "距離空間の重み付きグラフ化" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

ユークリッド空間を始めとする距離空間において、距離に関する何らかの値を最小化する組み合わせ最適化を考える。

問題設定に応じて距離空間から重み付きグラフ（[単位円盤グラフ](https://en.wikipedia.org/wiki/Unit_disk_graph)や[Vietoris--Rips複体](https://en.wikipedia.org/wiki/Vietoris%E2%80%93Rips_complex)の$1$次元骨格など）を構成し、それに対してグラフアルゴリズムを適用する手法。

- 例えば$(X,d)$を距離空間とする。$X$を頂点集合とし$x_0 \neq x_1$を満たす各$(x_0,x_1) \in X^2$に重み$d(x_0,x_1)$の無向辺を貼った重み付きグラフを考える。構築は$(x_0,x_1)$の全探索により$O(\# X^2)$となる。
- 例えば$n$を正整数とし、$d$を$n$次元格子$\mathbb{Z}^n$の$\ell^1$距離や$\ell^{\infy}$距離とし、$X$を$\mathbb{Z}^n$の部分集合とし、$L$を正整数とする。$X$を頂点集合として$x_0 \neq x_1$かつ$d(x_0,x_1) \leq L$を満たす各$(x_0,x_1) \in X^2$に重み$1$の無向辺を貼ったグラフを考える。構築は$(x_0,x_1)$の全探索または$x_0$の$L$近傍探索により$O(\# X \min \\{\# X,L^n\\})$となる。

　
{% assign solution = "集合管理" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

集合をデータ構造で管理する手法。

- 配列の<a href="{{ site.url }}/yukicoder-difficulty-statistics#ソート>ソート</a>
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#キュー>キュー</a>
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#優先度付き>キュー</a>
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#set>set</a>（c++のunordered set、pythonのset）
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#multiset>multiset</a>（c++のunordered multiset）
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#sorted set>sorted set</a>（c++のset）
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#フェニック木>フェニック木</a>を用いた<a href="{{ site.url }}/yukicoder-difficulty-statistics#配列を像・頻度表で管理>像・頻度表の管理</a>

などがこれに該当する。整数の二進法表記やbool値配列で集合を管理するものは含まない。

　
{% assign solution = "重複選択個数の線形関係式" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

１つの項目が無制限に複数回選択可能なナップサック問題であって、各項目のコストや価値が選択回数に依存しないものを考える。

項目の個数を$N$とし、$N$以下の各正整数$i$に対し項目$i$のコストを$W_i$と置く。もし等式$\sum_{i=1}^{N} a_i W_i = \sum_{i=1}^{N} b_i W_i$を満たす相異なる非負整数係数ベクトル$(a_i)\_{i=1}^{N}$と$(b_i)\_{i=1}^{N}$が存在するならば、最適な選択個数を表す非負整数係数ベクトル$(c_i)\_{i=1}^{N}$を考える際は辞書式順序に関して$(a_i)\_{i=1}^{N} \leq (c_i)\_{i=1}^{N}$か$(b_i)\_{i=1}^{N} \leq (c_i)\_{i=1}^{N}$のいずれか少なくとも一方が成り立たないとして良いので、特に$N$以下のある正整数$i$が存在して$c_i < \max \{a_i,b_i\}$が成り立つとして良い。これによりいくつかの変数を決め打った全探索を行い価値の最大化を行う手法。

$(a_i)\_{i=1}^{N}$と$(b_i)\_{i=1}^{N}$を見つけるには、縦ベクトル$(W_i)\_{i=1}^{N}$に右から掛けて零ベクトルとなる$N$次整数係数縦ベクトルを探してその正成分と負成分に分けて差で表せば良い。

なおコストが$1$次元であるならば、コスト上限を$C$と置くと通常の動的計画法で$O(NC)$で解くことができるので、コストが多次元である場合（例えば個数に制限のある複数個の項目を抱き合わせで選択する必要があるナップサック問題）に特に有効である。次元を$D$と置くと$(W_i)\_{i=1}^{N}$は$D \times N$行列とみなせるため、$(a_i)\_{i=1}^{N}$と$(b_i)\_{i=1}^{N}$の組を$\max \\{0,N-D\\}$次元分探すことが可能である。

　
{% assign solution = "合成による次元削減" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

非空有限集合$S$と関数$f \colon S \to \mathbb{R}$が与えられ、$\max f(S)$を求める問題を考える。$\min f(S)$を求める場合は$f$の代わりに$-f$を考えれば良い。

集合$X,Y$と全単射$i \colon S \to X \times Y$と写像$g_1 \colon X \to \mathbb{R}$と$g_2 \colon Y \to \mathbb{R}$と辞書式順序に関する順序保存写像$h \colon \mathbb{R}^2 \to \mathbb{R}$を用いて$f = h \circ (g_1 \times g_2) \circ i$と表すことで、$\max f(S)$の計算を$h(\max g_1(X),\max g_2(Y))$に帰着させる手法。

平たく言えば、最大化したい関数の値を独立な項に分解してそれぞれを最大化することで全探索などの計算量を下げるテクニックである。

　
{% assign solution = "緩和" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

束縛条件を緩めることで解を求めやすくし、その結果を用いて元の束縛条件における厳密解を求める手法。

- $x^2 \leq N$を満たす整数$x$の最大値を求める際に、代わりに実数の範囲で解いて（つまり$x = \sqrt{N}$として）その近傍にある整数値を探索する。
- 下に凸な可微分関数$f$に整数$x$を代入した時の最小値を求める際に、代わりに実数の範囲で最小値を与える実数$x$を求めてその近傍にある整数値を探索する。
- 単調増加・減少関数$f$を用いた等式条件$f(x) = K$を満たす整数$x$を求める問題において、代わりに$=$を$\leq$／$\geq$に変更した条件を満たす$x$の最小・最大値を求める方法を考え、以下の考察に繋げる：
  - 求解問題を二分探索で解く。
  - 求めたい値の上界である必要十分条件を決定して上界の最小値を計算する。
  - 全順序集合の$K$番目の要素を<a href="#指定序数の値の計算を各値未満の数え上げに帰着" class="tag">各値未満の要素数に関する二分探索</a>で決定する。
- 関数$f(x)$の最大・最小値を求める問題において、$f(x) = g(x) + h(x)$を満たす関数$g(x), h(x)$であって最大・最小値の計算がしやすいものを探し、$f(x)$の$2$変数化$g(x_0) + h(x_1)$の最大・最小値（つまり$g(x), h(x)$の最大・最小値の和）により$f(x)$の最大・最小値の上・下界を得て、以下の考察に繋げる：
  - 得られた上・下界を用いて全探索の枝刈りを行う。
  - 得られた上・下界を実際に達成する（$g(x), h(x)$の最大・最小化を同時に達成する）$x$を構築する。
- 条件$P(i)$を満たす$0 \leq i < N$全体をわたる$f(i)$の総和$a_N$を求める際に、$P(i)$を外すか緩めるか置き換えて$0 \leq i \leq n$全体をわたる$f(i)$の総和を求めた値を$b_n$と置いて、$b_0, b_1, \ldots, b_N$などの値から$a_N$を求める。
  - $P(i)$が$i \in \bigcup_{j in [0,M)} S_j$ならば、$P(i)$を外して包除原理に帰着。
  - $P(i)$が$\textrm{gcd}(i,M) = 1$ならば、$P(i)$を外して約数包除原理に帰着。
  - 特に$P(i)$が$i \equiv 1 \pmod{2}$ならば、$P(i)$を外して$i$に$2$冪を掛ける（もしくは$i \equiv 0 \pmod{2^d}$という条件に置き換える）ことで$b_{\lfloor N \rfloor},b_{\lfloor N/2 \rfloor},b_{\lfloor N/2^2 \rfloor}, \ldots$に関する包除原理に帰着。
  - $P(i)$が「$i$が$D$桁の$B$進法表記を持ち各桁が非零」ならば、$P(i)$を外し$i$に$B$冪を掛ける（もしくは$i \equiv 0 \pmod{B^d}$という条件に置き換える）ことで$b_{\lfloor N \rfloor},b_{\lfloor N/B \rfloor},b_{\lfloor N/B^2 \rfloor}, \ldots$に関する包除原理に帰着。

といった用途がある。

　
{% assign solution = "場合分けによるmax・min・絶対値計算" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

$\max \\{f(x),g(x)\\}$や$\min \\{f(x),g(x)\\}$と$\lvert f(x) \rvert$の最大・最小化や像・逆像計算やこれらの値を用いた更新クエリ処理を考える。

$\max$や$\min$は$f(x) \leq g(x)$の場合と$f(x) > g(x)$の場合で分けて問題を解き、絶対値は$f(x) \leq 0$の場合と$f(x) > 0$の場合で分けて問題を解く手法。

一般に場合分けを定義に含む関数は直接処理することが難しいが、定義に従って場合分けをして簡単な関数に帰着させることで明示的公式やデータ構造により簡単に処理できることがある。

　
{% assign solution = "指定序数の値の計算を始切片の数え上げに帰着" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

有限全順序集合$S$とその要素数以下の正整数$K$が与えられた時、$S$の$K$番目の要素を求める問題を考える。

「$s$未満の$S$の要素の個数が$K$より大きい最小の$s \in S$」を二分探索などで求める手法。

通常の二分探索より非自明な<a href="#緩和" class="tag">緩和</a>の特別な例。

　
{% assign solution = "指定序数の値の計算を被覆の先頭項管理で処理" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

全順序集合$S$とその要素数$N$以下の正整数$K$が与えられ、$S$の$K$番目の要素を求める問題を考える。

$M$を$N$より十分小さい正整数とし、$S$が$M$個の非空部分集合の族$(S_j)_{j=1}^{M}$で被覆され、$M$以下の各正整数$j$に対し後続関数$S_j \setminus \\{\max S_j\\} \to S_j \setminus \\{\min S_j\\}$が高速に計算できるとする。

この時、$S$を管理して$S$から先頭要素を$K$回取り出す代わりに、$M$以下の各正整数$j$に対する$S_j$から先頭要素を取り出した$M$元集合$T$に先頭要素のpopと要素追加を繰り返す手法。

例えば$S$が全順序集合$X,Y,Z$と辞書式順序について順序保存な写像$f \colon X \times Y \to Z$を用いて$S = f(X \times Y)$と表せる時、$S$の分割として$(f(\\{x\\} \times Y))_{x \in X}$を考えれば良い。

　
{% assign solution = "01列に翻訳" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

これは解法別難易度統計のための便宜的な解法名である。まず競技プログラミングでしばしば以下の対象間での相互変換が要求される。

- 01列
- 非負整数
- 非負整数の広義単調増大列
- グリッド上で原点から$x$軸正方向か$y$軸にのみ進む経路
- 括弧列
- 二分木
- ヤング図形

解法別難易度統計において、これらから２つを選ぶ組み合わせそれぞれに解法名を付してしまうと解法名の集計が困難になるため、代わりに01列とそれ以外の翻訳の組み合わせとして解法名を管理している。それらをまとめて参照するために付す統一的な解法名がこの「01列に翻訳」である。

　
{% assign solution = "表示可能性DP" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

演算の集合$S$と配列$A$と項$t$が与えられた時、$A$の成分に（問題設定次第では順番の入れ替えを許して）$S$に属すいずれかの演算を施した時に$t$が構成可能か否かを判定する問題を考える。構文木まで指定されている場合は葉から根に向かう向きに$A$をトポロジカルソートしておく。

「$A$の第$i$成分までで打ち切った配列に$S$に属す演算を施した時に構成可能な項全体の集合$\textrm{dp}[i]$」や「$A$の（連続とは限らない部分列$B$に$S$に属す演算を施した時に構成可能な項全体の集合$\textrm{dp}[B]$」などを管理する動的計画法。

例えば$S$に属す演算が１つのモノイド演算$\oplus$（の定義域を制限したもの）と$\oplus$の単位元を返す$2$変数定数関数と$2$変数第$1$射影である場合は「第$i$成分までで打ち切った配列の連続とは限らない部分列に$\oplus$を施した時に構成可能な項全体の集合$\textrm{dp}[i]$」を管理することに他ならない。
- $\oplus$が順序モノイド演算で、順番の入れ替えを許さない設定での場合は（価値上限付き）コストなし[ナップサックDP]({{ site.url }}/yukicoder-difficulty-statistics#ナップサックDP)となる。
- $(<,\oplus)$が可換順序モノイド構造で、順番の入れ替えを許す設定で上限・下限が部分式にも適用される場合は[ヘルド・カープ法]({{ site.url }}/yukicoder-difficulty-statistics#ヘルド・カープ法)の[bitDP]({{ site.url }}/yukicoder-difficulty-statistics#bitDP)となる。

　
{% assign solution = "不変量を保つ戦略" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

合法手を失ったプレイヤーの負けとなる二人ゲームにおいて、ゲームの状態から定まる不変量が常に敗北局面の不変量と同じ値になるように相手に手番を返す必勝戦略のこと。

例えば最初に$20$個の石があり交互に$1$個以上$4$個以下の石を取っていき取れなくなったら負けのゲームにおいて、石の残数を$5$で割った余りが$0$となるように後手が石を取って先手に手番を渡すことで後手必勝となる。

ニム和を用いたニムの必勝戦略は不変量を保つ戦略の特別な例なので、ニム和の問題は他に不変量を保つ戦略の非自明な考察がない限り不変量を保つ戦略の問題としては集計しない。

　
{% assign solution = "押し付け戦略" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

局面が与えられた時の合法手全体の集合がどちらの手番かに依存しない（勝敗の決め方は対称でなくても良い）二人ゲームを考える。

プレイヤー$A$がある着手$m$を行った場合に$A$の必敗となる（$B$が$m$を行っても$B$の必敗とならなくても良い）ことが分かっている状況で、$B$が$m$を避け続けることで$A$に$m$を強制する戦略。

　
{% assign solution = "高さ奇数ニム和" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

有限非輪状有向グラフの頂点上に石の山があり、石を山から取り除く代わりに有向辺に沿って石を山から山に移動させるニムの亜種であって、任意の頂点$s$から出次数$0$の任意の頂点$t$への経路$p$の経路長の偶奇が$s$のみに依存し$t,p$に依存しない二人ゲームの勝敗を判定する問題を考える。

このゲームの勝敗を、奇数になる$s$のみのニムに帰着させてニム和で決定する手法。

　
{% assign solution = "最終手番の任意性" %}
<h2 id="{{ solution }}"><a href="{{ site.url }}/yukicoder-difficulty-statistics#{{ solution }}">{{ solution }}</a></h2>

規定の手数後の何らかの不変量の値に従って勝敗が決まる二人ゲームにおいて、最終手番で不変量を自由に変更できれば最終手番のプレイヤーが勝つことを用いた考察。

初期状態次第で、

- 最終手番のプレイヤーは最終手番の自由度をなるべく残すことで必勝となる。
- 最終手番のプレイヤーでないプレイヤーは最終手番の自由度をなるべく減らすように操作することが強いられる（自由度を残さざるを得ない場合は必敗となる）。
- いずれかのプレイヤーが最終手番の自由度をなるべく減らすことで途中までで最終手番を確定させて必勝となる。

などといった状況が起こる。

