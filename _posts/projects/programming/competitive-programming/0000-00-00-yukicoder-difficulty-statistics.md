---
layout: project
title: yukicoder過去問解法別難易度統計
date: 2024-10-21
excerpt: "yukicoderの過去問の解法別の難易度に関する統計データです。"
parent: competitive-programming-project/
prev-child: competitive-programming-creating-problem-status
next-child: yukicoder-difficulty-statistics-solution-name
project: true
image-directory: competitive-programming
tags: [競技プログラミング,数学]
---

yukicoder contest 358 (2022-08-26) 以降に出題されたyuicoderの問題で筆者（$p$進大好きbot）がupsolveした問題の解法をまとめ、解法別に難易度統計をします。


## 進捗

通常問題の問題番号2056から2237まで登録し終わりました。先は長いです。


## 用途

主にyukicoderコンテストの問題に対して

- コンテスト中の考察時に「過去２年の傾向から、このアルゴリズムがこの難易度で出題される可能性はあまりないな」と判断する。
- 作問／tester時に「過去１年の傾向から、このアルゴリズムを想定解とするならば難易度は少なくともこれ以上にした方がいいな」と判断する。

といった使い方をするための自分用の統計ページです。必然的に想定解に触れることになるので、ネタバレにご注意ください。アルゴリズムのみに注目した難易度統計であるため、ジャッジの特殊性や考察難易度などアルゴリズム以外に難易度に寄与する部分は一切考慮しないため、難易度評価の下界としてのみ参考にすることができます。

コンテスト出題でない単発出題や通常コンテスト以外で出題された問題などは上記の目的に合致しないため、以下のように処理しています：

- 問題番号が2056以上3000以下の問題しか集計しない。（ネタ問題等が集計しない目的）
- コンテスト出題でない単発出題は各解法の難易度別問題一覧には掲載するものの、難易度平均計算時は集計しない。

１つ目のルールの影響で、問題公開後に通常問題タグから別の問題タグに移動した問題についてはあまり直感的でない集計結果となります。例えば数学的知識問題には集計されるもの（[No.2466 Root! Root! Root!](https://yukicoder.me/problems/no/2466)）とされないもの（[No.3094 Character Table](https://yukicoder.me/problems/no/3094)）があります。


## 集計方法

先述したように、集計対象は筆者がupsolveした問題に限られることにご注意ください。

後述するように解説ページも手作業で読んで集計するため、upsolveしていない問題も集計してしまうともったいないからです。また手作業での集計となるため、解法の勘違いなどで集計のミスをする可能性もあることにご注意ください。

基本的には★3以下の通常問題を全てupsolveしているはずですが、upsolveに時間がかかるため問題公開から数週間の遅れが生じることもあります。★3.5以上はほとんどupsolveしていないのでデータとしては不十分です。


### データ取得元

[yukicoder](https://yukicoder.me/)の問題ページとコンテスト順位表ページからDifficulty以外のデータを取得し、[yukicoder Problems](https://iilj.github.io/yukicoder-problems/#/list/)のListページからDifficultyのデータを取得しています。

ただし問題の解法は必ずしもタグ登録されていないため、タグ情報ではなく解説ページを用いて自分で考察し直した結果を集計しています。そのため解法の集計にミスがある可能性があります。


### 解法の集計

各問題を、その解法を構成するアルゴリズムや典型考察で類別し、難易度統計を取ります。

１つの問題にはたいてい複数の解法がありますが、その中で主観的に最も簡単なもののみを集計対象とします。

例えばフェニック木（BIT）を用いたシンプルな解法と、遅延評価セグメント木を用いた複雑な解法がある場合、前者のみを集計します。

また集計対象の１つの解法にはたいてい複数のアルゴリズムや典型考察が組み合わさっていますが、その中で主観的に最も難しいものと比較して特筆すべきもののみを集計対象のアルゴリズムと典型考察とします。

例えば集計対象の１つの解法が単純なソートと単純な場合分けのみを用いる場合はソートと場合分けの両方を集計しますが、一方で集計対象の１つの解法が単純なソートと単純な場合分けとConvex Hull Trick（CHT）のみを用いる場合は単純なソートや単純な場合分けが特筆すべきものでないのでConvex Hull Trickのみを集計します。

もし単純なソートや単純な場合分けでなく、ソートすることや場合分けすることに非自明な考察が要求される場合はそれらも集計します。要するに解法に要求されるアルゴリズムや典型考察の中で主観的に特筆すべきものを集計します。


### 解法以外の集計

問題の日付を記載する際は問題の公開開始日ではなくコンテストの開始日を表します。（特にAdvent Calender Contestで両者にズレが生じます）

また問題タイトルは基本的に原題をそのまま集計していますが、例外として

- [No.2403 "Eight" Bridges of K(oの上にウムラウト)nigsberg](https://yukicoder.me/problems/no/2403)
- [No.2473 Fraises dans une bo(iの上にアクサン・シルコンフレクス)te](https://yukicoder.me/problems/no/2473)
- [No.2878 $\mathbb{IGNITION}$](https://yukicoder.me/problems/no/2878)

はこちらの自動化処理の都合

- No.2403 "Eight" Bridges of K"onigsberg
- No.2473 Fraises dans une bo^ite
- No.2878 IGNITION

と記載させていただきます。


## 登録済み解法一覧

以下の解法ごとに問題を列挙し、難易度の傾向を表示します：

1. [特殊な入出力](#特殊な入出力)
1. [数値の文字列受け取り](#数値の文字列受け取り)
1. [64bit整数](#64bit整数)
1. [検索](#検索)
1. [小数誤差](#小数誤差)
1. [相似](#相似)
1. [連想配列](#連想配列)
1. [三角形の成立条件](#三角形の成立条件)
1. [カレンダー計算](#カレンダー計算)
1. [繰り返し二乗法](#繰り返し二乗法)
1. [動的mod](#動的mod)
1. [累積積](#累積積)
1. [実装](#実装)
1. [ギャグ](#ギャグ)
1. [累積和](#累積和)
1. [全探索](#全探索)
1. [サンプルから推測](#サンプルから推測)
1. [遷移の収束](#遷移の収束)
1. [余事象](#余事象)
1. [充足可能性判定](#充足可能性判定)
1. [頂点倍加](#頂点倍加)
1. [多項定理](#多項定理)
1. [階乗逆元](#階乗逆元)
1. [場合の数](#場合の数)
1. [頻度表](#頻度表)
1. [解の公式](#解の公式)
1. [１次式の最大・最小値](#１次式の最大・最小値)
1. [貪欲法](#貪欲法)
1. [実験](#実験)
1. [深さ優先探索](#深さ優先探索)／DFS
1. [素集合データ構造](#素集合データ構造)／UnionFind／UF／DSU
1. [DAG上のDP](#DAG上のDP)
1. [アルゴリズムのリアクティブ化](#アルゴリズムのリアクティブ化)
1. [良いケースに帰着](#良いケースに帰着)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)）
1. [幅優先探索](#幅優先探索)／BFS
1. [小数誤差解消](#小数誤差解消)
1. [平方根](#平方根)
1. [サンプルに帰着](#サンプルに帰着)
1. [場合分け](#場合分け)
1. [最終ターン数に注目](#最終ターン数に注目)
1. [同じ値の纏め上げ](#同じ値の纏め上げ)
1. [最長歩道取得](#最長歩道取得)
1. [操作回数最小値で判定](#操作回数最小値で判定)
1. [配列を像で管理](#配列を像で管理)
1. [マッチ度ごとに管理](#マッチ度ごとに管理)
1. [操作逆順](#操作逆順)
1. [挿入ソート](#挿入ソート)
1. [倍数メビウス変換](#倍数メビウス変換)
1. [期待値漸化式](#期待値漸化式)
1. [端から確定](#端から確定)
1. [区間和の指定された区間計算](#区間和の指定された区間計算)
1. [表示可能性DP](#表示可能性DP)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)）
1. [区間管理](#区間管理)
1. [部分回文列挙](#部分回文列挙)
1. [木DP](#木DP)
1. [imos法](#imos法)
1. [分枝限定法](#分枝限定法)
1. [場合分けによるmin・max計算](#場合分けによるmin・max計算)
1. [不変量を保つ戦略](#不変量を保つ戦略)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)）
1. [損をしない変形](#損をしない変形)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)）
1. [ソート](#ソート)
1. [ミラー戦略](#ミラー戦略)
1. [逆元](#逆元)
1. [積和の和積化](#積和の和積化)
1. [最終手番の任意性](#最終手番の任意性)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)）
1. [多点BFS](#多点BFS)／多始点BFS
1. [高さ奇数ニム和](#高さ奇数ニム和)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)）
1. [変数決め打ち](#変数決め打ち)
1. [クラスカル法](#クラスカル法)／Kruskal法
1. [ダイクストラ法](#ダイクストラ法)／Dijkstra法
1. [最短経路長取得](#最短経路長取得)
1. [冪等重みの最短経路長取得](#冪等重みの最短経路長取得)
1. [ニム和](#ニム和)
1. [不定方程式の因数分解](#不定方程式の因数分解)
1. [必勝戦略のリアクティブ化](#必勝戦略のリアクティブ化)
1. [シミュレーション](#シミュレーション)
1. [操作の纏め上げ](#操作の纏め上げ)
1. [階差数列](#階差数列)
1. [押し付け戦略](#押し付け戦略)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)）
1. [ゼータ変換](#ゼータ変換)
1. [メビウス変換](#メビウス変換)
1. [倍数ゼータ変換](#倍数ゼータ変換)
1. [周期](#周期)
1. [枝刈り](#枝刈り)
1. [距離空間の重み付きグラフ化](#距離空間の重み付きグラフ化)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)）
1. [一対一対応](#一対一対応)
1. [クエリ先読み](#クエリ先読み)
1. [尺取り法](#尺取り法)
1. [二分探索](#二分探索)
1. [緩和](#緩和)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)）
1. [不変量に注目](#不変量に注目)
1. [動的計画法](#動的計画法)／DP
1. [平面走査](#平面走査)
1. [行列累乗](#行列累乗)
1. [区間和取得](#区間和取得)
1. [クエリソート](#クエリソート)
1. [mex取得](#mex取得)
1. [sorted_set](#sorted_set)
1. [スライド最小化](#スライド最小化)
1. [bitごとに計算](#bitごとに計算)
1. [ポラードの$\rho$](#ポラードの$\rho$)
1. [平方剰余](#平方剰余)
1. [区間最大・最小値取得](#区間最大・最小値取得)
1. [イベントソート](#イベントソート)
1. [素因数分解](#素因数分解)
1. [フェニック木](#フェニック木)／BIT
1. [区間要素数取得](#区間要素数取得)
1. [座標圧縮](#座標圧縮)／座圧
1. [素数列挙](#素数列挙)
1. [グリッド上の価値最大化](#グリッド上の価値最大化)
1. [確率漸化式](#確率漸化式)
1. [再帰](#再帰)
1. [解法場合分け](#解法場合分け)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)）
1. [bitset高速化](#bitset高速化)
1. [基底](#基底)
1. [線形代数](#線形代数)
1. [準同型](#準同型)
1. [包除原理](#包除原理)
1. [約数メビウス変換](#約数メビウス変換)
1. [bitDP](#bitDP)
1. [bit全探索](#bit全探索)
1. [余因子展開](#余因子展開)
1. [半分全列挙](#半分全列挙)
1. [剰余を商に翻訳](#剰余を商に翻訳)
1. [平方分割](#平方分割)
1. [変数の対称性](#変数の対称性)
1. [単調関数の像計算](#単調関数の像計算)
1. [自己写像に翻訳](#自己写像に翻訳)
1. [連長圧縮](#連長圧縮)／ランレングス圧縮／RLE
1. [区間加算更新](#区間加算更新)
1. [ユークリッドの互除法](#ユークリッドの互除法)
1. [最大公約数](#最大公約数)／GCD
1. [互いに素に帰着](#互いに素に帰着)
1. [ナップサックDP](#ナップサックDP)
1. [数え上げの平均化](#数え上げの平均化)（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#数え上げの平均化)）
1. [期待値の線形性](#期待値の線形性)
1. [DPのデータ構造高速化](#DPのデータ構造高速化)
1. [調和数列](#調和数列)
1. [ベン図](#ベン図)
1. [B進法](#B進法)
1. [小さいケースの構築を拡張](#小さいケースの構築を拡張)
1. [剰余による確率的判定](#剰余による確率的判定)
1. [最小素因数前計算](#最小素因数前計算)
1. [２進法](#２進法)
1. [交代和](#交代和)
1. [２次元DPの１次元圧縮](#２次元DPの１次元圧縮)
1. [第二種スターリング数](#第二種スターリング数)
1. [floor_sum](#floor_sum)
1. [フロベニウスの硬貨交換問題](#フロベニウスの硬貨交換問題)
1. [像決め打ち二分探索](#像決め打ち二分探索)
1. [カタラン数](#カタラン数)
1. [01BFS](#01BFS)
1. [区間kth取得](#区間kth取得)
1. [ローリングハッシュ](#ローリングハッシュ)
1. [最長共通接頭辞](#最長共通接頭辞)／Z-algorithm／LCP
1. [桁DP](#桁DP)
1. [同値関係](#同値関係)
1. [高速フーリエ変換](#高速フーリエ変換)／数論的変換／FTT／NTT
1. [畳み込み](#畳み込み)
1. [場合分けによる絶対値計算](#場合分けによる絶対値計算)
1. [付値管理](#付値管理)
1. [キュー](#キュー)
1. [マージ](#マージ)
1. [区間を中間で分割してマージ](#区間を中間で分割してマージ)
1. [区間最大・最小値更新](#区間最大・最小値更新)
1. [分割統治畳み込み](#分割統治畳み込み)／分割統治FFT
1. [遅延セグメント木](#遅延セグメント木)／遅延セグ木
1. [バケット分割](#バケット分割)
1. [区間二次形式取得](#区間二次形式取得)
1. [区間二次式取得](#区間二次式取得)
1. [最近共通祖先](#最近共通祖先)／LCA
1. [重軽分解](#重軽分解)／HL分解／HLD
1. [フック長公式](#フック長公式)
1. [ヤング図形](#ヤング図形)
1. [トポロジカルソート](#トポロジカルソート)
1. [強連結成分分解](#強連結成分分解)／SCC
1. [残余ネットワーク](#残余ネットワーク)
1. [P-再帰](#P-再帰)／P-recursive
1. [多点評価](#多点評価)
1. [評価点シフト](#評価点シフト)
1. [アルゴリズム中に追加処理](#アルゴリズム中に追加処理)
1. [ハミルトン路](#ハミルトン路)
1. [構文解析](#構文解析)

ただし難易度が未設定の問題があれば、★1と換算します。


　
<h2 id="特殊な入出力">1. 特殊な入出力</h2>

### 難易度統計

「特殊な入出力」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.1/791
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1/544
- 2022年のコンテスト平均難易度/difficulty: 1.2/915

### 難易度別問題一覧

「特殊な入出力」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)
- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題, difficulty: 544)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題, difficulty: 969)

　
<h2 id="数値の文字列受け取り">2. 数値の文字列受け取り</h2>

### 難易度統計

「数値の文字列受け取り」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.2/756
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1/544
- 2022年のコンテスト平均難易度/difficulty: 1.5/969

### 難易度別問題一覧

「数値の文字列受け取り」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題, difficulty: 544)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題, difficulty: 969)

　
<h2 id="64bit整数">3. 64bit整数</h2>

### 難易度統計

「64bit整数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.3/841
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.2/841
- 2022年のコンテスト平均難易度/difficulty: 1.5/841

### 難易度別問題一覧

「64bit整数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題, difficulty: 544)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)
- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)
- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

　
<h2 id="検索">4. 検索</h2>

### 難易度統計

「検索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/588
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.5/588

### 難易度別問題一覧

「検索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)

　
<h2 id="小数誤差">5. 小数誤差</h2>

### 難易度統計

「小数誤差」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/588
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.5/588

### 難易度別問題一覧

「小数誤差」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)

　
<h2 id="相似">6. 相似</h2>

### 難易度統計

「相似」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/588
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.5/588

### 難易度別問題一覧

「相似」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)

　
<h2 id="連想配列">7. 連想配列</h2>

### 難易度統計

「連想配列」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/829
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1093
- 2022年のコンテスト平均難易度/difficulty: 1/566

### 難易度別問題一覧

「連想配列」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2153">No.2153 何コーダーが何人？</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - A問題, difficulty: 566)

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題, difficulty: 1093)

　
<h2 id="三角形の成立条件">8. 三角形の成立条件</h2>

### 難易度統計

「三角形の成立条件」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/864
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.5/864

### 難易度別問題一覧

「三角形の成立条件」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2140">No.2140 Triangle</a> (yukicoder contest 370 (2022-12-02) - A問題, difficulty: 864)

　
<h2 id="カレンダー計算">9. カレンダー計算</h2>

### 難易度統計

「カレンダー計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/1095
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.5/1095

### 難易度別問題一覧

「カレンダー計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題, difficulty: 1095)

　
<h2 id="繰り返し二乗法">10. 繰り返し二乗法</h2>

### 難易度統計

「繰り返し二乗法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/1139
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/1139
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「繰り返し二乗法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

　
<h2 id="動的mod">11. 動的mod</h2>

### 難易度統計

「動的mod」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/1139
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/1139
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「動的mod」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

　
<h2 id="累積積">12. 累積積</h2>

### 難易度統計

「累積積」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/1139
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/1139
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「累積積」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

　
<h2 id="実装">13. 実装</h2>

### 難易度統計

「実装」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.6/985
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.7/1084
- 2022年のコンテスト平均難易度/difficulty: 1.3/787

### 難易度別問題一覧

「実装」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題, difficulty: 569)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題, difficulty: 938)
- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題, difficulty: 544)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題, difficulty: 406)
- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題, difficulty: 1095)
- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題, difficulty: 999)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題, difficulty: 939)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2237">No.2237 Xor Sum Hoge</a> (yukicoder contest 379 (2023-03-03) - F問題, difficulty: 2519)

　
<h2 id="ギャグ">14. ギャグ</h2>

### 難易度統計

「ギャグ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.7/1172
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/1139
- 2022年のコンテスト平均難易度/difficulty: 2/1206

### 難易度別問題一覧

「ギャグ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)

　
<h2 id="累積和">15. 累積和</h2>

### 難易度統計

「累積和」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.8/1100
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.8/1100

### 難易度別問題一覧

「累積和」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題, difficulty: 406)
- <a href="https://yukicoder.me/problems/no/2124">No.2124 Guess the Permutation</a> (yukicoder contest 368 (2022-11-18) - A問題, difficulty: 1158)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題, difficulty: 1632)

　
<h2 id="全探索">16. 全探索</h2>

### 難易度統計

「全探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.9/1444
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.9/1311
- 2022年のコンテスト平均難易度/difficulty: 2/1689

### 難易度別問題一覧

「全探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2138">No.2138 Add Bacon</a> (Advent Calendar Contest 2022 (2022-12-01) - A問題, difficulty: 1017)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題, difficulty: 569)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題, difficulty: 938)
- <a href="https://yukicoder.me/problems/no/2208">No.2208 Linear Function</a> (yukicoder contest 376 (2023-02-10) - A問題, difficulty: 443)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題, difficulty: 969)
- <a href="https://yukicoder.me/problems/no/2091">No.2091 Shio Ramen (Easy)</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題, difficulty: 769)
- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題, difficulty: 999)

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題, difficulty: 1529)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)
- <a href="https://yukicoder.me/problems/no/2196">No.2196 Pair Bonus</a> (yukicoder contest 374 (2023-01-20) - C問題, difficulty: 1314)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題, difficulty: 1551)
- <a href="https://yukicoder.me/problems/no/2234">No.2234 palindromer</a> (yukicoder contest 379 (2023-03-03) - C問題, difficulty: 1000)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題, difficulty: 2246)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題, difficulty: 2471)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2237">No.2237 Xor Sum Hoge</a> (yukicoder contest 379 (2023-03-03) - F問題, difficulty: 2519)

　
<h2 id="サンプルから推測">17. サンプルから推測</h2>

### 難易度統計

「サンプルから推測」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/344
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/344
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「サンプルから推測」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2216">No.2216 Pa1indr0me</a> (yukicoder contest 377 (2023-02-17) - A問題, difficulty: 344)

　
<h2 id="遷移の収束">18. 遷移の収束</h2>

### 難易度統計

「遷移の収束」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/939
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/939
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「遷移の収束」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題, difficulty: 939)

　
<h2 id="余事象">19. 余事象</h2>

### 難易度統計

「余事象」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1215
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1215
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「余事象」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題, difficulty: 769)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)

　
<h2 id="充足可能性判定">20. 充足可能性判定</h2>

### 難易度統計

「充足可能性判定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1254
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1254
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「充足可能性判定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)

　
<h2 id="頂点倍加">21. 頂点倍加</h2>

### 難易度統計

「頂点倍加」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1254
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1254
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「頂点倍加」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)

　
<h2 id="多項定理">22. 多項定理</h2>

### 難易度統計

「多項定理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1261
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1261

### 難易度別問題一覧

「多項定理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題, difficulty: 1261)

　
<h2 id="階乗逆元">23. 階乗逆元</h2>

### 難易度統計

「階乗逆元」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1275
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1275

### 難易度別問題一覧

「階乗逆元」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)

　
<h2 id="場合の数">24. 場合の数</h2>

### 難易度統計

「場合の数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1308
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1308

### 難易度別問題一覧

「場合の数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題, difficulty: 1261)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題, difficulty: 1356)

　
<h2 id="頻度表">25. 頻度表</h2>

### 難易度統計

「頻度表」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1323
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.1/1256
- 2022年のコンテスト平均難易度/difficulty: 2/1390

### 難易度別問題一覧

「頻度表」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2153">No.2153 何コーダーが何人？</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - A問題, difficulty: 566)

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題, difficulty: 1093)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題, difficulty: 1069)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題, difficulty: 1802)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題, difficulty: 1803)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

　
<h2 id="解の公式">26. 解の公式</h2>

### 難易度統計

「解の公式」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1856
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1856
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「解の公式」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

　
<h2 id="１次式の最大・最小値">27. １次式の最大・最小値</h2>

### 難易度統計

「１次式の最大・最小値」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.1/1438
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1578
- 2022年のコンテスト平均難易度/difficulty: 1/1017

### 難易度別問題一覧

「１次式の最大・最小値」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2138">No.2138 Add Bacon</a> (Advent Calendar Contest 2022 (2022-12-01) - A問題, difficulty: 1017)
- <a href="https://yukicoder.me/problems/no/2208">No.2208 Linear Function</a> (yukicoder contest 376 (2023-02-10) - A問題, difficulty: 443)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2237">No.2237 Xor Sum Hoge</a> (yukicoder contest 379 (2023-03-03) - F問題, difficulty: 2519)

　
<h2 id="貪欲法">28. 貪欲法</h2>

### 難易度統計

「貪欲法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.1/1447
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1200
- 2022年のコンテスト平均難易度/difficulty: 2/1483

### 難易度別問題一覧

「貪欲法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)

##### ★★

- <a href="https://yukicoder.me/problems/no/2056">No.2056 非力なレッド</a> (yukicoder contest 358 (2022-08-26) - A問題, difficulty: 683)
- <a href="https://yukicoder.me/problems/no/2064">No.2064 Smallest Sequence on Grid</a> (yukicoder contest 359 (2022-09-02) - B問題, difficulty: 1582)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題, difficulty: 1802)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題, difficulty: 1200)

　
<h2 id="実験">29. 実験</h2>

### 難易度統計

「実験」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1267
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/344
- 2022年のコンテスト平均難易度/difficulty: 2.5/2191

### 難易度別問題一覧

「実験」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2216">No.2216 Pa1indr0me</a> (yukicoder contest 377 (2023-02-17) - A問題, difficulty: 344)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)

　
<h2 id="深さ優先探索">30. 深さ優先探索</h2>

### 難易度統計

「深さ優先探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1351
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1351
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「深さ優先探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題, difficulty: 769)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題, difficulty: 1933)

　
<h2 id="素集合データ構造">31. 素集合データ構造</h2>

### 難易度統計

「素集合データ構造」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1370
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1254
- 2022年のコンテスト平均難易度/difficulty: 2.5/1486

### 難易度別問題一覧

「素集合データ構造」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題, difficulty: 1486)

　
<h2 id="DAG上のDP">32. DAG上のDP</h2>

### 難易度統計

「DAG上のDP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1388
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1200
- 2022年のコンテスト平均難易度/difficulty: 2/1577

### 難易度別問題一覧

「DAG上のDP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2100">No.2100 [Cherry Alpha C] Two-way Steps</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - D問題, difficulty: 1577)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)

　
<h2 id="アルゴリズムのリアクティブ化">33. アルゴリズムのリアクティブ化</h2>

### 難易度統計

「アルゴリズムのリアクティブ化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1648
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.2/1648

### 難易度別問題一覧

「アルゴリズムのリアクティブ化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2124">No.2124 Guess the Permutation</a> (yukicoder contest 368 (2022-11-18) - A問題, difficulty: 1158)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題, difficulty: 2139)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)

　
<h2 id="良いケースに帰着">34. 良いケースに帰着</h2>

### 難易度統計

「[良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1762
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.2/1762

### 難易度別問題一覧

「[良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)

　
<h2 id="幅優先探索">35. 幅優先探索</h2>

### 難易度統計

「幅優先探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1785
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1989
- 2022年のコンテスト平均難易度/difficulty: 2/1582

### 難易度別問題一覧

「幅優先探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2064">No.2064 Smallest Sequence on Grid</a> (yukicoder contest 359 (2022-09-02) - B問題, difficulty: 1582)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題, difficulty: 1989)

　
<h2 id="小数誤差解消">36. 小数誤差解消</h2>

### 難易度統計

「小数誤差解消」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1950
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1950
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「小数誤差解消」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)

　
<h2 id="平方根">37. 平方根</h2>

### 難易度統計

「平方根」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1950
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1950
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「平方根」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)

　
<h2 id="サンプルに帰着">38. サンプルに帰着</h2>

### 難易度統計

「サンプルに帰着」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1532
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1971
- 2022年のコンテスト平均難易度/difficulty: 2/1313

### 難易度別問題一覧

「サンプルに帰着」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題, difficulty: 2039)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題, difficulty: 1971)

　
<h2 id="場合分け">39. 場合分け</h2>

### 難易度統計

「場合分け」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1686
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1275
- 2022年のコンテスト平均難易度/difficulty: 2.5/1920

### 難易度別問題一覧

「場合分け」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題, difficulty: 569)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題, difficulty: 938)
- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題, difficulty: 544)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題, difficulty: 969)
- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)
- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題, difficulty: 769)

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2209">No.2209 Flip and Reverse</a> (yukicoder contest 376 (2023-02-10) - B問題, difficulty: 1008)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)
- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題, difficulty: 1934)
- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題, difficulty: 2039)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題, difficulty: 1803)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)
- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題, difficulty: 2246)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2237">No.2237 Xor Sum Hoge</a> (yukicoder contest 379 (2023-03-03) - F問題, difficulty: 2519)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2151">No.2151 3 on Torus-Lohkous</a> (Advent Calendar Contest 2022 (2022-12-01) - H問題, difficulty: 3257)

　
<h2 id="最終ターン数に注目">40. 最終ターン数に注目</h2>

### 難易度統計

「最終ターン数に注目」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1711
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1008
- 2022年のコンテスト平均難易度/difficulty: 2.5/2062

### 難易度別問題一覧

「最終ターン数に注目」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2209">No.2209 Flip and Reverse</a> (yukicoder contest 376 (2023-02-10) - B問題, difficulty: 1008)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題, difficulty: 1934)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)

　
<h2 id="同じ値の纏め上げ">41. 同じ値の纏め上げ</h2>

### 難易度統計

「同じ値の纏め上げ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.4/1618
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1613
- 2022年のコンテスト平均難易度/difficulty: 2.3/1624

### 難易度別問題一覧

「同じ値の纏め上げ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題, difficulty: 1069)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題, difficulty: 1865)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題, difficulty: 2381)

　
<h2 id="最長歩道取得">42. 最長歩道取得</h2>

### 難易度統計

「最長歩道取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1200
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1200
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「最長歩道取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)

　
<h2 id="操作回数最小値で判定">43. 操作回数最小値で判定</h2>

### 難易度統計

「操作回数最小値で判定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1200
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1200
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「操作回数最小値で判定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題, difficulty: 1200)

　
<h2 id="配列を像で管理">44. 配列を像で管理</h2>

### 難易度統計

「配列を像で管理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1200
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1200
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「配列を像で管理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)

　
<h2 id="マッチ度ごとに管理">45. マッチ度ごとに管理</h2>

### 難易度統計

「マッチ度ごとに管理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1372
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1622
- 2022年のコンテスト平均難易度/difficulty: 2.5/1247

### 難易度別問題一覧

「マッチ度ごとに管理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題, difficulty: 1220)

　
<h2 id="操作逆順">46. 操作逆順</h2>

### 難易度統計

「操作逆順」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1486
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1486

### 難易度別問題一覧

「操作逆順」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題, difficulty: 1486)

　
<h2 id="挿入ソート">47. 挿入ソート</h2>

### 難易度統計

「挿入ソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1489
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1489
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「挿入ソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2210">No.2210 equence Squence Seuence</a> (yukicoder contest 376 (2023-02-10) - C問題, difficulty: 1489)

　
<h2 id="倍数メビウス変換">48. 倍数メビウス変換</h2>

### 難易度統計

「倍数メビウス変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1607
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1607
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「倍数メビウス変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

　
<h2 id="期待値漸化式">49. 期待値漸化式</h2>

### 難易度統計

「期待値漸化式」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1622
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1622
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「期待値漸化式」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)

　
<h2 id="端から確定">50. 端から確定</h2>

### 難易度統計

「端から確定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1623
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1430
- 2022年のコンテスト平均難易度/difficulty: 2.5/2008

### 難易度別問題一覧

「端から確定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題, difficulty: 1200)

　
<h2 id="区間和の指定された区間計算">51. 区間和の指定された区間計算</h2>

### 難易度統計

「区間和の指定された区間計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1632
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1632

### 難易度別問題一覧

「区間和の指定された区間計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題, difficulty: 1632)

　
<h2 id="表示可能性DP">52. 表示可能性DP</h2>

### 難易度統計

「[表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1641
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1641

### 難易度別問題一覧

「[表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)

　
<h2 id="区間管理">53. 区間管理</h2>

### 難易度統計

「区間管理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1649
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1649

### 難易度別問題一覧

「区間管理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)

　
<h2 id="部分回文列挙">54. 部分回文列挙</h2>

### 難易度統計

「部分回文列挙」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1661
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1661
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「部分回文列挙」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題, difficulty: 1661)

　
<h2 id="木DP">55. 木DP</h2>

### 難易度統計

「木DP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1661
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1661
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「木DP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題, difficulty: 1661)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)

　
<h2 id="imos法">56. imos法</h2>

### 難易度統計

「imos法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1680
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1680

### 難易度別問題一覧

「imos法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2154">No.2154 あさかつの参加人数</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - B問題, difficulty: 711)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

　
<h2 id="分枝限定法">57. 分枝限定法</h2>

### 難易度統計

「分枝限定法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1762
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.4/1553
- 2022年のコンテスト平均難易度/difficulty: 2.6/1912

### 難易度別問題一覧

「分枝限定法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題, difficulty: 1728)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2196">No.2196 Pair Bonus</a> (yukicoder contest 374 (2023-01-20) - C問題, difficulty: 1314)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題, difficulty: 1069)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題, difficulty: 1865)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)
- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題, difficulty: 2381)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
<h2 id="場合分けによるmin・max計算">58. 場合分けによるmin・max計算</h2>

### 難易度統計

「場合分けによるmin・max計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1773
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1773
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「場合分けによるmin・max計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)

　
<h2 id="不変量を保つ戦略">59. 不変量を保つ戦略</h2>

### 難易度統計

「[不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1828
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1828

### 難易度別問題一覧

「[不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)

　
<h2 id="損をしない変形">60. 損をしない変形</h2>

### 難易度統計

「[損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1858
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1858

### 難易度別問題一覧

「[損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題, difficulty: 1529)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題, difficulty: 1356)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2096">No.2096 Rage With Our Friends</a> (yukicoder contest 363 (2022-10-07) - E問題, difficulty: 2690)

　
<h2 id="ソート">61. ソート</h2>

### 難易度統計

「ソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1888
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1567
- 2022年のコンテスト平均難易度/difficulty: 2.8/2210

### 難易度別問題一覧

「ソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題, difficulty: 1551)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2210">No.2210 equence Squence Seuence</a> (yukicoder contest 376 (2023-02-10) - C問題, difficulty: 1489)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

　
<h2 id="ミラー戦略">62. ミラー戦略</h2>

### 難易度統計

「ミラー戦略」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1905
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1905

### 難易度別問題一覧

「ミラー戦略」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題, difficulty: 1803)

　
<h2 id="逆元">63. 逆元</h2>

### 難易度統計

「逆元」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1922
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1922
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「逆元」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)

　
<h2 id="積和の和積化">64. 積和の和積化</h2>

### 難易度統計

「積和の和積化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1922
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1922
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「積和の和積化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)

　
<h2 id="最終手番の任意性">65. 最終手番の任意性</h2>

### 難易度統計

「[最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1934
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1934

### 難易度別問題一覧

「[最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題, difficulty: 1934)

　
<h2 id="多点BFS">66. 多点BFS</h2>

### 難易度統計

「多点BFS」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1989
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1989
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「多点BFS」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題, difficulty: 1989)

　
<h2 id="高さ奇数ニム和">67. 高さ奇数ニム和</h2>

### 難易度統計

「[高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2008
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2008

### 難易度別問題一覧

「[高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)

　
<h2 id="変数決め打ち">68. 変数決め打ち</h2>

### 難易度統計

「変数決め打ち」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2029
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1814
- 2022年のコンテスト平均難易度/difficulty: 2.6/2172

### 難易度別問題一覧

「変数決め打ち」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題, difficulty: 2620)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題, difficulty: 2168)

　
<h2 id="クラスカル法">69. クラスカル法</h2>

### 難易度統計

「クラスカル法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2044
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/2044
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「クラスカル法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)

　
<h2 id="ダイクストラ法">70. ダイクストラ法</h2>

### 難易度統計

「ダイクストラ法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2044
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/2044
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「ダイクストラ法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)

　
<h2 id="最短経路長取得">71. 最短経路長取得</h2>

### 難易度統計

「最短経路長取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2044
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/2044
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「最短経路長取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)

　
<h2 id="冪等重みの最短経路長取得">72. 冪等重みの最短経路長取得</h2>

### 難易度統計

「冪等重みの最短経路長取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2044
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/2044
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「冪等重みの最短経路長取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)

　
<h2 id="ニム和">73. ニム和</h2>

### 難易度統計

「ニム和」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2249
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2249

### 難易度別問題一覧

「ニム和」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2165">No.2165 Let's Play Nim!</a> (Advent Calendar Contest 2022 (2022-12-01) - P問題, difficulty: 2491)

　
<h2 id="不定方程式の因数分解">74. 不定方程式の因数分解</h2>

### 難易度統計

「不定方程式の因数分解」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2291
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2291

### 難易度別問題一覧

「不定方程式の因数分解」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題, difficulty: 2291)

　
<h2 id="必勝戦略のリアクティブ化">75. 必勝戦略のリアクティブ化</h2>

### 難易度統計

「必勝戦略のリアクティブ化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2491
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2491

### 難易度別問題一覧

「必勝戦略のリアクティブ化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2165">No.2165 Let's Play Nim!</a> (Advent Calendar Contest 2022 (2022-12-01) - P問題, difficulty: 2491)

　
<h2 id="シミュレーション">76. シミュレーション</h2>

### 難易度統計

「シミュレーション」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.6/1635
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.6/1635
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「シミュレーション」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題, difficulty: 999)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題, difficulty: 939)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2237">No.2237 Xor Sum Hoge</a> (yukicoder contest 379 (2023-03-03) - F問題, difficulty: 2519)

　
<h2 id="操作の纏め上げ">77. 操作の纏め上げ</h2>

### 難易度統計

「操作の纏め上げ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1643
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1643
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「操作の纏め上げ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題, difficulty: 1200)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

　
<h2 id="階差数列">78. 階差数列</h2>

### 難易度統計

「階差数列」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1853
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.7/1853

### 難易度別問題一覧

「階差数列」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題, difficulty: 2500)

　
<h2 id="押し付け戦略">79. 押し付け戦略</h2>

### 難易度統計

「[押し付け戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1908
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.7/1908

### 難易度別問題一覧

「[押し付け戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題, difficulty: 2168)

　
<h2 id="ゼータ変換">80. ゼータ変換</h2>

### 難易度統計

「ゼータ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1956
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1607
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「ゼータ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
<h2 id="メビウス変換">81. メビウス変換</h2>

### 難易度統計

「メビウス変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1956
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1607
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「メビウス変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
<h2 id="倍数ゼータ変換">82. 倍数ゼータ変換</h2>

### 難易度統計

「倍数ゼータ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1956
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1607
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「倍数ゼータ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
<h2 id="周期">83. 周期</h2>

### 難易度統計

「周期」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/2062
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1933
- 2022年のコンテスト平均難易度/difficulty: 2.5/2191

### 難易度別問題一覧

「周期」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題, difficulty: 1933)

　
<h2 id="枝刈り">84. 枝刈り</h2>

### 難易度統計

「枝刈り」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/2063
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.6/1832
- 2022年のコンテスト平均難易度/difficulty: 3/2758

### 難易度別問題一覧

「枝刈り」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題, difficulty: 939)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題, difficulty: 2758)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)
- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題, difficulty: 2471)

　
<h2 id="距離空間の重み付きグラフ化">85. 距離空間の重み付きグラフ化</h2>

### 難易度統計

「[距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/2065
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2065
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「[距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

　
<h2 id="一対一対応">86. 一対一対応</h2>

### 難易度統計

「一対一対応」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/2151
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.7/2151

### 難易度別問題一覧

「一対一対応」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題, difficulty: 2295)

　
<h2 id="クエリ先読み">87. クエリ先読み</h2>

### 難易度統計

「クエリ先読み」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/1743
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.8/1743

### 難易度別問題一覧

「クエリ先読み」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題, difficulty: 1486)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)

　
<h2 id="尺取り法">88. 尺取り法</h2>

### 難易度統計

「尺取り法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/1934
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1773
- 2022年のコンテスト平均難易度/difficulty: 3/1988

### 難易度別問題一覧

「尺取り法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題, difficulty: 1632)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

　
<h2 id="二分探索">89. 二分探索</h2>

### 難易度統計

「二分探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/1940
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1622
- 2022年のコンテスト平均難易度/difficulty: 3.5/2364

### 難易度別問題一覧

「二分探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題, difficulty: 1200)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)
- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)
- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

　
<h2 id="緩和">90. 緩和</h2>

### 難易度統計

「[緩和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2019
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1607
- 2022年のコンテスト平均難易度/difficulty: 3/2225

### 難易度別問題一覧

「[緩和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題, difficulty: 1803)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="不変量に注目">91. 不変量に注目</h2>

### 難易度統計

「不変量に注目」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2052
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.8/2052

### 難易度別問題一覧

「不変量に注目」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題, difficulty: 2500)

　
<h2 id="動的計画法">92. 動的計画法</h2>

### 難易度統計

「動的計画法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2061
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1868
- 2022年のコンテスト平均難易度/difficulty: 2.8/2101

### 難易度別問題一覧

「動的計画法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題, difficulty: 843)
- <a href="https://yukicoder.me/problems/no/2095">No.2095 High Rise</a> (yukicoder contest 363 (2022-10-07) - D問題, difficulty: 1518)
- <a href="https://yukicoder.me/problems/no/2100">No.2100 [Cherry Alpha C] Two-way Steps</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - D問題, difficulty: 1577)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2150">No.2150 Site Supporter</a> (Advent Calendar Contest 2022 (2022-12-01) - G問題, difficulty: 1909)
- <a href="https://yukicoder.me/problems/no/2155">No.2155 みちらcolor</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - C問題, difficulty: 878)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題, difficulty: 2246)
- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題, difficulty: 2620)
- <a href="https://yukicoder.me/problems/no/2082">No.2082 AND OR XOR</a> (yukicoder contest 361 (2022-09-25) - E問題, difficulty: 2501)
- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題, difficulty: 2344)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題, difficulty: 1220)
- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題, difficulty: 2673)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題, difficulty: 2758)
- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題, difficulty: 2852)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)
- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2159">No.2159 Filling 4x4 array</a> (Advent Calendar Contest 2022 (2022-12-01) - J問題, difficulty: 3382)
- <a href="https://yukicoder.me/problems/no/2231">No.2231 Surprising Flash!</a> (yukicoder contest 378 (2023-02-24) - H問題, difficulty: 2690)

　
<h2 id="平面走査">93. 平面走査</h2>

### 難易度統計

「平面走査」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.9/1917
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.8/1765
- 2022年のコンテスト平均難易度/difficulty: 3/2145

### 難易度別問題一覧

「平面走査」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

　
<h2 id="行列累乗">94. 行列累乗</h2>

### 難易度統計

「行列累乗」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1220
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1220

### 難易度別問題一覧

「行列累乗」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題, difficulty: 1220)

　
<h2 id="区間和取得">95. 区間和取得</h2>

### 難易度統計

「区間和取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1816
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1661
- 2022年のコンテスト平均難易度/difficulty: 3.2/1893

### 難易度別問題一覧

「区間和取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

　
<h2 id="クエリソート">96. クエリソート</h2>

### 難易度統計

「クエリソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1872
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1872

### 難易度別問題一覧

「クエリソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)

　
<h2 id="mex取得">97. mex取得</h2>

### 難易度統計

「mex取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1927
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1927
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「mex取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)

　
<h2 id="sorted_set">98. sorted_set</h2>

### 難易度統計

「sorted_set」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1943
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1927
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「sorted_set」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)

　
<h2 id="スライド最小化">99. スライド最小化</h2>

### 難易度統計

「スライド最小化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1959
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「スライド最小化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)

　
<h2 id="bitごとに計算">100. bitごとに計算</h2>

### 難易度統計

「bitごとに計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2022
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.8/1815
- 2022年のコンテスト平均難易度/difficulty: 3.5/2643

### 難易度別問題一覧

「bitごとに計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題, difficulty: 1093)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題, difficulty: 1971)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)
- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題, difficulty: 2381)

　
<h2 id="ポラードの$\rho$">101. ポラードの$\rho$</h2>

### 難易度統計

「ポラードの$\rho$」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2047
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2047

### 難易度別問題一覧

「ポラードの$\rho$」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)

　
<h2 id="平方剰余">102. 平方剰余</h2>

### 難易度統計

「平方剰余」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2047
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2047

### 難易度別問題一覧

「平方剰余」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)

　
<h2 id="区間最大・最小値取得">103. 区間最大・最小値取得</h2>

### 難易度統計

「区間最大・最小値取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2064
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2169
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「区間最大・最小値取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

　
<h2 id="イベントソート">104. イベントソート</h2>

### 難易度統計

「イベントソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2071
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1794
- 2022年のコンテスト平均難易度/difficulty: 3.2/2349

### 難易度別問題一覧

「イベントソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

　
<h2 id="素因数分解">105. 素因数分解</h2>

### 難易度統計

「素因数分解」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2091
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3.2/1883
- 2022年のコンテスト平均難易度/difficulty: 2.7/2298

### 難易度別問題一覧

「素因数分解」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題, difficulty: 2291)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題, difficulty: 2567)

　
<h2 id="フェニック木">106. フェニック木</h2>

### 難易度統計

「フェニック木」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2119
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1915
- 2022年のコンテスト平均難易度/difficulty: 3.1/2201

### 難易度別問題一覧

「フェニック木」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)

　
<h2 id="区間要素数取得">107. 区間要素数取得</h2>

### 難易度統計

「区間要素数取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2145
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2145

### 難易度別問題一覧

「区間要素数取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

　
<h2 id="座標圧縮">108. 座標圧縮</h2>

### 難易度統計

「座標圧縮」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2145
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2145

### 難易度別問題一覧

「座標圧縮」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

　
<h2 id="素数列挙">109. 素数列挙</h2>

### 難易度統計

「素数列挙」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2167
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2167

### 難易度別問題一覧

「素数列挙」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題, difficulty: 2167)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題)

　
<h2 id="グリッド上の価値最大化">110. グリッド上の価値最大化</h2>

### 難易度統計

「グリッド上の価値最大化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2169
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2169
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「グリッド上の価値最大化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

　
<h2 id="確率漸化式">111. 確率漸化式</h2>

### 難易度統計

「確率漸化式」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2169
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2169
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「確率漸化式」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

　
<h2 id="再帰">112. 再帰</h2>

### 難易度統計

「再帰」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2221
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1952
- 2022年のコンテスト平均難易度/difficulty: 3/2491

### 難易度別問題一覧

「再帰」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題, difficulty: 2246)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題, difficulty: 1971)
- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題, difficulty: 1933)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)

　
<h2 id="解法場合分け">113. 解法場合分け</h2>

### 難易度統計

「[解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2227
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2227

### 難易度別問題一覧

「[解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="bitset高速化">114. bitset高速化</h2>

### 難易度統計

「bitset高速化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2245
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2245

### 難易度別問題一覧

「bitset高速化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)

　
<h2 id="基底">115. 基底</h2>

### 難易度統計

「基底」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2245
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2245

### 難易度別問題一覧

「基底」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)

　
<h2 id="線形代数">116. 線形代数</h2>

### 難易度統計

「線形代数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2294
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2294

### 難易度別問題一覧

「線形代数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)
- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題, difficulty: 2344)

　
<h2 id="準同型">117. 準同型</h2>

### 難易度統計

「準同型」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2295
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2295

### 難易度別問題一覧

「準同型」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題, difficulty: 2295)

　
<h2 id="包除原理">118. 包除原理</h2>

### 難易度統計

「包除原理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2306
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「包除原理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
<h2 id="約数メビウス変換">119. 約数メビウス変換</h2>

### 難易度統計

「約数メビウス変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2306
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「約数メビウス変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
<h2 id="bitDP">120. bitDP</h2>

### 難易度統計

「bitDP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2344
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2344

### 難易度別問題一覧

「bitDP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題, difficulty: 2344)

　
<h2 id="bit全探索">121. bit全探索</h2>

### 難易度統計

「bit全探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2344
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2344

### 難易度別問題一覧

「bit全探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題, difficulty: 2344)

　
<h2 id="余因子展開">122. 余因子展開</h2>

### 難易度統計

「余因子展開」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2344
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2344

### 難易度別問題一覧

「余因子展開」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題, difficulty: 2344)

　
<h2 id="半分全列挙">123. 半分全列挙</h2>

### 難易度統計

「半分全列挙」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2385
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2175
- 2022年のコンテスト平均難易度/difficulty: 3/2595

### 難易度別問題一覧

「半分全列挙」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)
- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題, difficulty: 2175)

　
<h2 id="剰余を商に翻訳">124. 剰余を商に翻訳</h2>

### 難易度統計

「剰余を商に翻訳」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2393
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2393

### 難易度別問題一覧

「剰余を商に翻訳」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)

　
<h2 id="平方分割">125. 平方分割</h2>

### 難易度統計

「平方分割」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2393
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2393

### 難易度別問題一覧

「平方分割」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)

　
<h2 id="変数の対称性">126. 変数の対称性</h2>

### 難易度統計

「変数の対称性」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2430
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2430

### 難易度別問題一覧

「変数の対称性」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)

　
<h2 id="単調関数の像計算">127. 単調関数の像計算</h2>

### 難易度統計

「単調関数の像計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2471
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2471
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「単調関数の像計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題, difficulty: 2471)

　
<h2 id="自己写像に翻訳">128. 自己写像に翻訳</h2>

### 難易度統計

「自己写像に翻訳」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2501
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2501

### 難易度別問題一覧

「自己写像に翻訳」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2082">No.2082 AND OR XOR</a> (yukicoder contest 361 (2022-09-25) - E問題, difficulty: 2501)

　
<h2 id="連長圧縮">129. 連長圧縮</h2>

### 難易度統計

「連長圧縮」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2620
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2620

### 難易度別問題一覧

「連長圧縮」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題, difficulty: 2620)

　
<h2 id="区間加算更新">130. 区間加算更新</h2>

### 難易度統計

「区間加算更新」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2247
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.1/2247

### 難易度別問題一覧

「区間加算更新」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2154">No.2154 あさかつの参加人数</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - B問題, difficulty: 711)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題, difficulty: 3382)

　
<h2 id="ユークリッドの互除法">131. ユークリッドの互除法</h2>

### 難易度統計

「ユークリッドの互除法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2316
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.1/2316

### 難易度別問題一覧

「ユークリッドの互除法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題, difficulty: 2139)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="最大公約数">132. 最大公約数</h2>

### 難易度統計

「最大公約数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2316
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.1/2316

### 難易度別問題一覧

「最大公約数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題, difficulty: 2139)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="互いに素に帰着">133. 互いに素に帰着</h2>

### 難易度統計

「互いに素に帰着」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2375
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.1/2375

### 難易度別問題一覧

「互いに素に帰着」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="ナップサックDP">134. ナップサックDP</h2>

### 難易度統計

「ナップサックDP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.2/1766
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4.5/2690
- 2022年のコンテスト平均難易度/difficulty: 2/843

### 難易度別問題一覧

「ナップサックDP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題, difficulty: 843)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2231">No.2231 Surprising Flash!</a> (yukicoder contest 378 (2023-02-24) - H問題, difficulty: 2690)

　
<h2 id="数え上げの平均化">135. 数え上げの平均化</h2>

### 難易度統計

「[数え上げの平均化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#数え上げの平均化)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.2/2094
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1622
- 2022年のコンテスト平均難易度/difficulty: 4/2566

### 難易度別問題一覧

「[数え上げの平均化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#数え上げの平均化)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
<h2 id="期待値の線形性">136. 期待値の線形性</h2>

### 難易度統計

「期待値の線形性」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.2/2244
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1922
- 2022年のコンテスト平均難易度/difficulty: 4/2566

### 難易度別問題一覧

「期待値の線形性」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
<h2 id="DPのデータ構造高速化">137. DPのデータ構造高速化</h2>

### 難易度統計

「DPのデータ構造高速化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.2/2305
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2169
- 2022年のコンテスト平均難易度/difficulty: 3.3/2332

### 難易度別問題一覧

「DPのデータ構造高速化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題, difficulty: 2758)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
<h2 id="調和数列">138. 調和数列</h2>

### 難易度統計

「調和数列」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.2/2383
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2039
- 2022年のコンテスト平均難易度/difficulty: 3.7/2728

### 難易度別問題一覧

「調和数列」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題, difficulty: 2471)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
<h2 id="ベン図">139. ベン図</h2>

### 難易度統計

「ベン図」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.2/2447
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.2/2447

### 難易度別問題一覧

「ベン図」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

　
<h2 id="B進法">140. B進法</h2>

### 難易度統計

「B進法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.3/2383
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2019
- 2022年のコンテスト平均難易度/difficulty: 3.6/2529

### 難易度別問題一覧

「B進法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題, difficulty: 1989)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題, difficulty: 2167)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)
- <a href="https://yukicoder.me/problems/no/2198">No.2198 Concon Substrings (COuNt-CONstruct Version)</a> (yukicoder contest 374 (2023-01-20) - E問題, difficulty: 2050)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)
- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題, difficulty: 2500)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題, difficulty: 3086)

　
<h2 id="小さいケースの構築を拡張">141. 小さいケースの構築を拡張</h2>

### 難易度統計

「小さいケースの構築を拡張」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2300
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2300

### 難易度別問題一覧

「小さいケースの構築を拡張」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題, difficulty: 2039)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2143">No.2143 Only One Bracket</a> (yukicoder contest 370 (2022-12-02) - D問題, difficulty: 1606)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2151">No.2151 3 on Torus-Lohkous</a> (Advent Calendar Contest 2022 (2022-12-01) - H問題, difficulty: 3257)

　
<h2 id="剰余による確率的判定">142. 剰余による確率的判定</h2>

### 難易度統計

「剰余による確率的判定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2307
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2567
- 2022年のコンテスト平均難易度/difficulty: 3/2047

### 難易度別問題一覧

「剰余による確率的判定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題, difficulty: 2567)

　
<h2 id="最小素因数前計算">143. 最小素因数前計算</h2>

### 難易度統計

「最小素因数前計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2436
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2567
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「最小素因数前計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題, difficulty: 2567)

　
<h2 id="２進法">144. ２進法</h2>

### 難易度統計

「２進法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2464
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2175
- 2022年のコンテスト平均難易度/difficulty: 3.6/2536

### 難易度別問題一覧

「２進法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題, difficulty: 2167)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)
- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題, difficulty: 2175)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題, difficulty: 3086)

　
<h2 id="交代和">145. 交代和</h2>

### 難易度統計

「交代和」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2500
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2500

### 難易度別問題一覧

「交代和」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題, difficulty: 2500)

　
<h2 id="２次元DPの１次元圧縮">146. ２次元DPの１次元圧縮</h2>

### 難易度統計

「２次元DPの１次元圧縮」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2536
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2169
- 2022年のコンテスト平均難易度/difficulty: 4/2903

### 難易度別問題一覧

「２次元DPの１次元圧縮」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
<h2 id="第二種スターリング数">147. 第二種スターリング数</h2>

### 難易度統計

「第二種スターリング数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2643
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2643

### 難易度別問題一覧

「第二種スターリング数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)

　
<h2 id="floor_sum">148. floor_sum</h2>

### 難易度統計

「floor_sum」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2648
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2648

### 難易度別問題一覧

「floor_sum」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="フロベニウスの硬貨交換問題">149. フロベニウスの硬貨交換問題</h2>

### 難易度統計

「フロベニウスの硬貨交換問題」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2648
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2648

### 難易度別問題一覧

「フロベニウスの硬貨交換問題」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="像決め打ち二分探索">150. 像決め打ち二分探索</h2>

### 難易度統計

「像決め打ち二分探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2648
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2648

### 難易度別問題一覧

「像決め打ち二分探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="カタラン数">151. カタラン数</h2>

### 難易度統計

「カタラン数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2649
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2649

### 難易度別問題一覧

「カタラン数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

　
<h2 id="01BFS">152. 01BFS</h2>

### 難易度統計

「01BFS」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2690
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2690

### 難易度別問題一覧

「01BFS」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2096">No.2096 Rage With Our Friends</a> (yukicoder contest 363 (2022-10-07) - E問題, difficulty: 2690)

　
<h2 id="区間kth取得">153. 区間kth取得</h2>

### 難易度統計

「区間kth取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2707
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2707

### 難易度別問題一覧

「区間kth取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)

　
<h2 id="ローリングハッシュ">154. ローリングハッシュ</h2>

### 難易度統計

「ローリングハッシュ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2877
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2877

### 難易度別問題一覧

「ローリングハッシュ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題, difficulty: 2852)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
<h2 id="最長共通接頭辞">155. 最長共通接頭辞</h2>

### 難易度統計

「最長共通接頭辞」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2877
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2877

### 難易度別問題一覧

「最長共通接頭辞」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題, difficulty: 2852)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
<h2 id="桁DP">156. 桁DP</h2>

### 難易度統計

「桁DP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.6/2622
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3.5/2381
- 2022年のコンテスト平均難易度/difficulty: 3.6/2683

### 難易度別問題一覧

「桁DP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題, difficulty: 2047)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)
- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題, difficulty: 2381)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2159">No.2159 Filling 4x4 array</a> (Advent Calendar Contest 2022 (2022-12-01) - J問題, difficulty: 3382)

　
<h2 id="同値関係">157. 同値関係</h2>

### 難易度統計

「同値関係」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.8/2758
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.8/2758

### 難易度別問題一覧

「同値関係」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題, difficulty: 3382)

　
<h2 id="高速フーリエ変換">158. 高速フーリエ変換</h2>

### 難易度統計

「高速フーリエ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.8/2934
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.8/2934

### 難易度別問題一覧

「高速フーリエ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題, difficulty: 2673)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="畳み込み">159. 畳み込み</h2>

### 難易度統計

「畳み込み」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.8/2934
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.8/2934

### 難易度別問題一覧

「畳み込み」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題, difficulty: 2673)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="場合分けによる絶対値計算">160. 場合分けによる絶対値計算</h2>

### 難易度統計

「場合分けによる絶対値計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2519
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2519
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「場合分けによる絶対値計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2237">No.2237 Xor Sum Hoge</a> (yukicoder contest 379 (2023-03-03) - F問題, difficulty: 2519)

　
<h2 id="付値管理">161. 付値管理</h2>

### 難易度統計

「付値管理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2567
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2567
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「付値管理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題, difficulty: 2567)

　
<h2 id="キュー">162. キュー</h2>

### 難易度統計

「キュー」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2658
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2658
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「キュー」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題, difficulty: 2658)

　
<h2 id="マージ">163. マージ</h2>

### 難易度統計

「マージ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2658
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2658
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「マージ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題, difficulty: 2658)

　
<h2 id="区間を中間で分割してマージ">164. 区間を中間で分割してマージ</h2>

### 難易度統計

「区間を中間で分割してマージ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2658
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2658
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「区間を中間で分割してマージ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題, difficulty: 2658)

　
<h2 id="区間最大・最小値更新">165. 区間最大・最小値更新</h2>

### 難易度統計

「区間最大・最小値更新」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2903
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4/2903

### 難易度別問題一覧

「区間最大・最小値更新」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
<h2 id="分割統治畳み込み">166. 分割統治畳み込み</h2>

### 難易度統計

「分割統治畳み込み」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/3125
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4/3125

### 難易度別問題一覧

「分割統治畳み込み」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題, difficulty: 2673)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="遅延セグメント木">167. 遅延セグメント木</h2>

### 難易度統計

「遅延セグメント木」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4.2/3142
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4.2/3142

### 難易度別問題一覧

「遅延セグメント木」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題, difficulty: 3382)

　
<h2 id="バケット分割">168. バケット分割</h2>

### 難易度統計

「バケット分割」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4.5/3117
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2658
- 2022年のコンテスト平均難易度/difficulty: 5/3577

### 難易度別問題一覧

「バケット分割」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題, difficulty: 2658)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="区間二次形式取得">169. 区間二次形式取得</h2>

### 難易度統計

「区間二次形式取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4.5/3382
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4.5/3382

### 難易度別問題一覧

「区間二次形式取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題, difficulty: 3382)

　
<h2 id="区間二次式取得">170. 区間二次式取得</h2>

### 難易度統計

「区間二次式取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4.5/3382
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4.5/3382

### 難易度別問題一覧

「区間二次式取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題, difficulty: 3382)

　
<h2 id="最近共通祖先">171. 最近共通祖先</h2>

### 難易度統計

「最近共通祖先」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4.5/3382
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4.5/3382

### 難易度別問題一覧

「最近共通祖先」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題, difficulty: 3382)

　
<h2 id="重軽分解">172. 重軽分解</h2>

### 難易度統計

「重軽分解」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4.5/3382
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4.5/3382

### 難易度別問題一覧

「重軽分解」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題, difficulty: 3382)

　
<h2 id="フック長公式">173. フック長公式</h2>

### 難易度統計

「フック長公式」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 5/3086
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 5/3086

### 難易度別問題一覧

「フック長公式」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題, difficulty: 3086)

　
<h2 id="ヤング図形">174. ヤング図形</h2>

### 難易度統計

「ヤング図形」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 5/3086
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 5/3086

### 難易度別問題一覧

「ヤング図形」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題, difficulty: 3086)

　
<h2 id="トポロジカルソート">175. トポロジカルソート</h2>

### 難易度統計

「トポロジカルソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 5/3382
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 5/3382

### 難易度別問題一覧

「トポロジカルソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題, difficulty: 3382)

　
<h2 id="強連結成分分解">176. 強連結成分分解</h2>

### 難易度統計

「強連結成分分解」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 5/3382
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 5/3382

### 難易度別問題一覧

「強連結成分分解」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題, difficulty: 3382)

　
<h2 id="残余ネットワーク">177. 残余ネットワーク</h2>

### 難易度統計

「残余ネットワーク」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 5/3382
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 5/3382

### 難易度別問題一覧

「残余ネットワーク」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題, difficulty: 3382)

　
<h2 id="P-再帰">178. P-再帰</h2>

### 難易度統計

「P-再帰」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 5/3577
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 5/3577

### 難易度別問題一覧

「P-再帰」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="多点評価">179. 多点評価</h2>

### 難易度統計

「多点評価」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 5/3577
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 5/3577

### 難易度別問題一覧

「多点評価」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="評価点シフト">180. 評価点シフト</h2>

### 難易度統計

「評価点シフト」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 5/3577
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 5/3577

### 難易度別問題一覧

「評価点シフト」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="アルゴリズム中に追加処理">181. アルゴリズム中に追加処理</h2>

### 難易度統計

「アルゴリズム中に追加処理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: データなし
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「アルゴリズム中に追加処理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)

　
<h2 id="ハミルトン路">182. ハミルトン路</h2>

### 難易度統計

「ハミルトン路」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: データなし
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「ハミルトン路」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)

　
<h2 id="構文解析">183. 構文解析</h2>

### 難易度統計

「構文解析」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: データなし
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「構文解析」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)

