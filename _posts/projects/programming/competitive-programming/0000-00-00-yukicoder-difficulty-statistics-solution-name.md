---
layout: project
title: yukicoder過去問解法別難易度統計の解法名解説
date: 2024-10-10
excerpt: "yukicoderの過去問の解法別難易度統計ページに記載した解法名の解説です。"
project: true
parent: competitive-programming-project/
prev-child: yukicoder-difficulty-statistics
next-child: 
image-directory: 
tags: [競技プログラミング,数学]
---


[yukicoderの過去問の解法別難易度統計のページ]({{ site.url }}/yukicoder-difficulty-statistics)で用いた、一般的でない解法名の解説ページです。

　
<h2 id="緩和">緩和</h2>

単調増加／減少関数$f$を用いた等式条件$f(x) = K$を満たす整数$x$を求める問題を考える。

$=$を$\leq$／$\geq$に変更した条件を満たす$x$の最小値／最大値を求める手法。

- 求解問題を二分探索で解く。
- 求めたい値の上界である必要十分条件を決定して上界の最小値を計算する。
- 全順序集合の$K$番目の要素を[上界決め打ち二分探索](#上界決め打ち二分探索)で決定する。

といった考察に繋げる。二分探索はたいてい緩和なので、二分探索の問題は緩和の考察が非自明でない限り緩和の問題として集計しない。

　
<h2 id="上界決め打ち二分探索">上界決め打ち二分探索</h2>

有限全順序集合$S$とその要素数以下の正整数$K$が与えられた時、$S$の$K$番目の要素を求める問題を考える。

「$s$以下の$S$の要素の個数が$K$以上となる最小の$s \in S$」を二分探索で求める手法。

通常の二分探索より非自明な緩和の特別な例。

　
<h2 id="解法場合分け">解法場合分け</h2>

入力が大きい場合と小さい場合で別の解法を取る手法。

- $O(B)$解と$O(N/B)$解がある時に$B \leq \sqrt{N}$か否かで解法を切り替える$O(\sqrt{N})$解
- $O(N)$解と$N > M$の時のみ有効な$O(1)$解がある時に$N \leq M$か否かで解法を切り替える$O(M)$解

などが典型。

　
<h2 id="良いケースに帰着">良いケースに帰着</h2>

操作を伴う問題で、初期状態に依存した値を計算する問題を考える。

- 初期状態から１・２回の操作を行うと必ず良い初期状態に遷移する場合
- 最終状態を全探索し、最終状態を変更した上で操作を逆順に実行した時に良い初期状態に戻れる場合

などで一般の１ケースを良い初期状態を持つ有限個のケースに帰着させる手法。

再帰の特別な例だが、再帰深度がせいぜい２程度であり一般の再帰と区別するため、良いケースに帰着させる問題は他に非自明な再帰を行わない限り再帰の問題として集計しない。

　
<h2 id="損をしない変形">損をしない変形</h2>

何らかの価値を最大化する（またはコストを最小化する）組み合わせ最適化を考える。

可能な操作全体のうち、適当な条件$P$を満たす操作のみに絞って考えれば良いことを示すために「任意の操作$X$に対し、条件$P$を満たすある操作$X'$が存在して、$X'$の価値は$X$の価値以上である」ということを示す手法。

- 非自明な貪欲法の正当性を証明する。
- 可能な操作全体の集合が大きすぎるために、考える操作の個数に計算量が依存する既存のアルゴリズム（全探索、グラフアルゴリズム、動的計画法、etc.）が使えない状況で、最適な操作を少なくとも１つ含む部分集合を構成し、それに対してアルゴリズムを適用する。

などといった目的で使われる。枝刈りの特別な例だが、他に非自明な枝刈りを行わない限り枝刈りの問題として集計しない。

　
<h2 id="距離空間の重み付きグラフ化">距離空間の重み付きグラフ化</h2>

ユークリッド空間を始めとする距離空間において、距離に関する何らかの値を最小化する組み合わせ最適化を考える。

問題設定に応じて距離空間から重み付きグラフ（[単位円盤グラフ](https://en.wikipedia.org/wiki/Unit_disk_graph)や[Vietoris--Rips複体](https://en.wikipedia.org/wiki/Vietoris%E2%80%93Rips_complex)の$1$次元骨格など）を構成し、それに対してグラフアルゴリズムを適用する手法。

　
<h2 id="数え上げの平均化">数え上げの平均化</h2>

成分に関する何らかの条件$P$を満たす配列や順列の個数を素数法で求める問題を考える。

個数を直接求める代わりに、一様ランダムなサンプリングをした時の$P$の成立確率$p$を求めてそれに母数を掛ける手法。特に

- $P$が独立事象の積事象で表せ、確率を積で計算しやすい場合。
- $p$が自然に和に分解され、期待値の線形性が適用しやすい場合。

に用いられる。

　
<h2 id="表示可能性DP">表示可能性DP</h2>

演算の集合$S$と配列$A$と項$t$が与えられた時、$A$の順番を変えずに$S$に属す演算を施した時に$t$が構成可能か否かを判定する問題を考える。

$A$の構文木（例えば左結合なら右端を根とする線形グラフ）で葉から根に向かって頂点$i$を見ていき「$i$を根とする部分木までで打ち切った配列に$S$に属す演算を施した時に構成可能な項全体の集合$\textrm{dp}(i)$」を管理する$i$に関する木DP（例えば線形グラフなら左から途中までで打ち切って構築可能性を管理する動的計画法）。

　
<h2 id="不変量を保つ戦略">不変量を保つ戦略</h2>

合法手を失ったプレイヤーの負けとなる二人ゲームにおいて、ゲームの状態から定まる不変量が常に敗北局面の不変量と同じ値になるように相手に手番を返す必勝戦略のこと。

例えば最初に$20$個の石があり交互に$1$個以上$4$個以下の石を取っていき取れなくなったら負けのゲームにおいて、石の残数を$5$で割った余りが$0$となるように後手が石を取って先手に手番を渡すことで後手必勝となる。

ニム和を用いたニムの必勝戦略は不変量を保つ戦略の特別な例なので、ニム和の問題は他に不変量を保つ戦略の非自明な考察がない限り不変量を保つ戦略の問題としては集計しない。

　
<h2 id="押し付け戦略">押し付け戦略</h2>

局面が与えられた時の合法手全体の集合がどちらの手番かに依存しない（勝敗の決め方は対称でなくても良い）二人ゲームを考える。

プレイヤー$A$がある着手$m$を行った場合に$A$の必敗となる（$B$が$m$を行っても$B$の必敗とならなくても良い）ことが分かっている状況で、$B$が$m$を避け続けることで$A$に$m$を強制する戦略。

　
<h2 id="高さ奇数ニム和">高さ奇数ニム和</h2>

有限非輪状有向グラフの頂点上に石の山があり、石を山から取り除く代わりに有向辺に沿って石を山から山に移動させるニムの亜種であって、任意の頂点$s$から出次数$0$の任意の頂点$t$への経路$p$の経路長の偶奇が$s$のみに依存し$t,p$に依存しない二人ゲームの勝敗を判定する問題を考える。

このゲームの勝敗を、奇数になる$s$のみのニムに帰着させてニム和で決定する手法。


<h2 id="最終手番の任意性">最終手番の任意性</h2>

規定の手数後の何らかの不変量の値に従って勝敗が決まる二人ゲームにおいて、最終手番で不変量を自由に変更できれば最終手番のプレイヤーが勝つことを用いた考察。

初期状態次第で、

- 最終手番のプレイヤーは最終手番の自由度をなるべく残すことで必勝となる。
- 最終手番のプレイヤーでないプレイヤーは最終手番の自由度をなるべく減らすように操作することが強いられる（自由度を残さざるを得ない場合は必敗となる）。
- いずれかのプレイヤーが最終手番の自由度をなるべく減らすことで途中までで最終手番を確定させて必勝となる。

などといった状況が起こる。

