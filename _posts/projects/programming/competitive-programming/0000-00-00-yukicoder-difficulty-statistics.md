---
layout: project
title: yukicoder過去問解法別難易度統計
date: 2024-10-18
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

通常問題の問題番号2056から2215まで登録し終わりました。先は長いです。


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

後述するように解説ページを手作業で読んで集計するため、upsolveしてない問題も集計してしまうともったいないからです。

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

1. １次式の最大・最小値
1. 特殊な入出力
1. 実装
1. 検索
1. 相似
1. 深さ優先探索
1. 連想配列
1. 三角形の成立条件
1. カレンダー
1. ギャグ
1. 繰り返し二乗法
1. 動的mod
1. 累積積
1. 全探索
1. 累積和
1. ナップサックDP
1. 余事象
1. 充足可能性判定
1. 頂点倍加
1. 多項定理
1. 階乗逆元
1. 場合の数
1. 頻度表
1. 貪欲法
1. DAG上のDP
1. 解の公式
1. 素集合データ構造（UnionFind／UF／DSU）
1. アルゴリズムのリアクティブ化
1. [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)
1. 幅優先探索（BFS）
1. 小数誤差解消
1. 平方根
1. サンプルに帰着
1. 同じ値の纏め上げ
1. 場合分け
1. 最終ターン数に注目
1. 操作逆順
1. 挿入ソート
1. 倍数メビウス変換
1. 区間和の指定された区間計算
1. [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)
1. 区間管理
1. 部分回文列挙
1. 木DP
1. imos法
1. 分枝限定法
1. [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)
1. 端から確定
1. [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)
1. ミラー戦略
1. [最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)
1. 多点BFS（多始点BFS）
1. [高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)
1. クラスカル法（Kruskal法）
1. ダイクストラ法（Dijkstra法）
1. 最短経路長取得
1. 冪等重みの最短経路長取得
1. 変数決め打ち
1. 実験
1. 周期
1. ニム和
1. 不定方程式の因数分解
1. 必勝戦略のリアクティブ化
1. 階差数列
1. [押し付け戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)
1. ソート
1. ゼータ変換
1. メビウス変換
1. 倍数ゼータ変換
1. [距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)
1. 一対一対応
1. クエリ先読み
1. [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)
1. 不変量
1. 動的計画法（DP）
1. 行列累乗
1. 区間和取得
1. クエリソート
1. sorted_set
1. スライド最小化
1. 区間最大・最小値取得
1. 尺取り法
1. bitごとに計算
1. ポラードの$\rho$
1. 平方剰余
1. シミュレーション
1. 操作の纏め上げ
1. フェニック木（BIT）
1. イベントソート
1. 二分探索
1. 区間要素数取得
1. 座標圧縮
1. 平面走査
1. 素数列挙
1. [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)
1. bitset高速化
1. 基底
1. 線形代数
1. 準同型
1. 包除原理
1. 約数メビウス変換
1. 再帰
1. bitDP
1. bit全探索
1. 余因子展開
1. 剰余を商に翻訳
1. 平方分割
1. 枝刈り
1. 変数の対称性
1. 自己写像に翻訳
1. 半分全列挙
1. 連長圧縮（ランレングス圧縮／RLE）
1. 区間加算更新
1. ユークリッドの互除法
1. 最大公約数（GCD）
1. 互いに素に帰着
1. 素因数分解
1. ベン図
1. DPのデータ構造高速化
1. 調和数列
1. B進法
1. 小さいケースの構築を拡張
1. 剰余による確率的判定
1. 最小素因数前計算
1. 交代和
1. 第二種スターリング数
1. floor_sum
1. フロベニウスの硬貨交換問題
1. 像決め打ち二分探索
1. カタラン数
1. 01BFS
1. 区間kth取得
1. ローリングハッシュ
1. 最長共通接頭辞（Z-algorithm／LCP）
1. ２進法
1. 桁DP
1. 同値関係
1. 高速フーリエ変換（数論的変換／FTT／NTT）
1. 畳み込み
1. 期待値の線形性
1. [数え上げの平均化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#数え上げの平均化)
1. 付値管理
1. キュー
1. マージｓ
1. 区間を中間で分割してマージ
1. ２次元DPの１次元圧縮
1. 区間最大・最小値更新
1. 分割統治畳み込み（分割統治FFT）
1. 遅延セグメント木（遅延セグ木）
1. バケット分割
1. 区間二次形式取得
1. 区間二次式取得
1. 最近共通祖先（LCA）
1. 重軽分解（HL分解／HLD）
1. フック長公式
1. ヤング図形
1. トポロジカルソート
1. 強連結成分分解
1. 残余ネットワーク
1. P-再帰（P-recursive）
1. 多点評価
1. 評価点シフト
1. アルゴリズム中に追加処理
1. ハミルトン路
1. マージ
1. 期待値漸化式
1. 構文解析

ただし難易度が未設定の問題があれば、★1と換算します。


　
## 1. １次式の最大・最小値

### 難易度統計

「１次式の最大・最小値」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1/730
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1/443
- 2022年のコンテスト平均難易度/difficulty: 1/1017

### 難易度別問題一覧

「１次式の最大・最小値」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2138">No.2138 Add Bacon</a> (Advent Calendar Contest 2022 (2022-12-01) - A問題, difficulty: 1017)
- <a href="https://yukicoder.me/problems/no/2208">No.2208 Linear Function</a> (yukicoder contest 376 (2023-02-10) - A問題, difficulty: 443)

　
## 2. 特殊な入出力

### 難易度統計

「特殊な入出力」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1/862
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1/862

### 難易度別問題一覧

「特殊な入出力」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)

　
## 3. 実装

### 難易度統計

「実装」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.2/774
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1/753
- 2022年のコンテスト平均難易度/difficulty: 1.3/787

### 難易度別問題一覧

「実装」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題, difficulty: 569)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題, difficulty: 938)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題, difficulty: 406)
- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題, difficulty: 1095)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題)

　
## 4. 検索

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

　
## 5. 相似

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

　
## 6. 深さ優先探索

### 難易度統計

「深さ優先探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/769
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/769
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「深さ優先探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題, difficulty: 769)

　
## 7. 連想配列

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

　
## 8. 三角形の成立条件

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

　
## 9. カレンダー

### 難易度統計

「カレンダー」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/1095
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.5/1095

### 難易度別問題一覧

「カレンダー」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題, difficulty: 1095)

　
## 10. ギャグ

### 難易度統計

「ギャグ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/1139
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/1139
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「ギャグ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

　
## 11. 繰り返し二乗法

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

　
## 12. 動的mod

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

　
## 13. 累積積

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

　
## 14. 全探索

### 難易度統計

「全探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.7/1335
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.4/981
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

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題, difficulty: 1529)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)
- <a href="https://yukicoder.me/problems/no/2196">No.2196 Pair Bonus</a> (yukicoder contest 374 (2023-01-20) - C問題, difficulty: 1314)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題, difficulty: 2246)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)

　
## 15. 累積和

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

　
## 16. ナップサックDP

### 難易度統計

「ナップサックDP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/843
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/843

### 難易度別問題一覧

「ナップサックDP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題, difficulty: 843)

　
## 17. 余事象

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

　
## 18. 充足可能性判定

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

　
## 19. 頂点倍加

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

　
## 20. 多項定理

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

　
## 21. 階乗逆元

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

　
## 22. 場合の数

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

　
## 23. 頻度表

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

　
## 24. 貪欲法

### 難易度統計

「貪欲法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1483
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
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

　
## 25. DAG上のDP

### 難易度統計

「DAG上のDP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1577
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1577

### 難易度別問題一覧

「DAG上のDP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2100">No.2100 [Cherry Alpha C] Two-way Steps</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - D問題, difficulty: 1577)

　
## 26. 解の公式

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

　
## 27. 素集合データ構造

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

　
## 28. アルゴリズムのリアクティブ化

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

　
## 29. 良いケースに帰着

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

　
## 30. 幅優先探索

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

　
## 31. 小数誤差解消

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

　
## 32. 平方根

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

　
## 33. サンプルに帰着

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

　
## 34. 同じ値の纏め上げ

### 難易度統計

「同じ値の纏め上げ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1577
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1529
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
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題, difficulty: 2381)

　
## 35. 場合分け

### 難易度統計

「場合分け」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1697
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.7/1074
- 2022年のコンテスト平均難易度/difficulty: 2.5/1920

### 難易度別問題一覧

「場合分け」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題, difficulty: 569)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題, difficulty: 938)

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

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2151">No.2151 3 on Torus-Lohkous</a> (Advent Calendar Contest 2022 (2022-12-01) - H問題, difficulty: 3257)

　
## 36. 最終ターン数に注目

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

　
## 37. 操作逆順

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

　
## 38. 挿入ソート

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

　
## 39. 倍数メビウス変換

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

　
## 40. 区間和の指定された区間計算

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

　
## 41. 表示可能性DP

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

　
## 42. 区間管理

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

　
## 43. 部分回文列挙

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

　
## 44. 木DP

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

　
## 45. imos法

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

　
## 46. 分枝限定法

### 難易度統計

「分枝限定法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1758
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1314
- 2022年のコンテスト平均難易度/difficulty: 2.5/1832

### 難易度別問題一覧

「分枝限定法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題, difficulty: 1728)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2196">No.2196 Pair Bonus</a> (yukicoder contest 374 (2023-01-20) - C問題, difficulty: 1314)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
## 47. 不変量を保つ戦略

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

　
## 48. 端から確定

### 難易度統計

「端から確定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1834
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1661
- 2022年のコンテスト平均難易度/difficulty: 2.5/2008

### 難易度別問題一覧

「端から確定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題, difficulty: 1661)

　
## 49. 損をしない変形

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

　
## 50. ミラー戦略

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

　
## 51. 最終手番の任意性

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

　
## 52. 多点BFS

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

　
## 53. 高さ奇数ニム和

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

　
## 54. クラスカル法

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

　
## 55. ダイクストラ法

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

　
## 56. 最短経路長取得

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

　
## 57. 冪等重みの最短経路長取得

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

　
## 58. 変数決め打ち

### 難易度統計

「変数決め打ち」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2093
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1856
- 2022年のコンテスト平均難易度/difficulty: 2.6/2172

### 難易度別問題一覧

「変数決め打ち」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題, difficulty: 2620)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題, difficulty: 2168)

　
## 59. 実験

### 難易度統計

「実験」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2191
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2191

### 難易度別問題一覧

「実験」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)

　
## 60. 周期

### 難易度統計

「周期」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2191
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2191

### 難易度別問題一覧

「周期」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)

　
## 61. ニム和

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

　
## 62. 不定方程式の因数分解

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

　
## 63. 必勝戦略のリアクティブ化

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

　
## 64. 階差数列

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

　
## 65. 押し付け戦略

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

　
## 66. ソート

### 難易度統計

「ソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1956
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1575
- 2022年のコンテスト平均難易度/difficulty: 2.8/2210

### 難易度別問題一覧

「ソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2210">No.2210 equence Squence Seuence</a> (yukicoder contest 376 (2023-02-10) - C問題, difficulty: 1489)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

　
## 67. ゼータ変換

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

　
## 68. メビウス変換

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

　
## 69. 倍数ゼータ変換

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

　
## 70. 距離空間の重み付きグラフ化

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

　
## 71. 一対一対応

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

　
## 72. クエリ先読み

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

　
## 73. 緩和

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

　
## 74. 不変量

### 難易度統計

「不変量」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2052
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.8/2052

### 難易度別問題一覧

「不変量」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題, difficulty: 2500)

　
## 75. 動的計画法

### 難易度統計

「動的計画法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2084
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1661
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

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)
- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2159">No.2159 Filling 4x4 array</a> (Advent Calendar Contest 2022 (2022-12-01) - J問題, difficulty: 3382)

　
## 76. 行列累乗

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

　
## 77. 区間和取得

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

　
## 78. クエリソート

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

　
## 79. sorted_set

### 難易度統計

「sorted_set」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1959
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「sorted_set」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)

　
## 80. スライド最小化

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

　
## 81. 区間最大・最小値取得

### 難易度統計

「区間最大・最小値取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1959
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「区間最大・最小値取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)

　
## 82. 尺取り法

### 難易度統計

「尺取り法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1988
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1988

### 難易度別問題一覧

「尺取り法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題, difficulty: 1632)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

　
## 83. bitごとに計算

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

　
## 84. ポラードの$\rho$

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

　
## 85. 平方剰余

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

　
## 86. シミュレーション

### 難易度統計

「シミュレーション」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2086
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2086
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「シミュレーション」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

　
## 87. 操作の纏め上げ

### 難易度統計

「操作の纏め上げ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2086
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2086
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「操作の纏め上げ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

　
## 88. フェニック木

### 難易度統計

「フェニック木」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2111
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1661
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

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)

　
## 89. イベントソート

### 難易度統計

「イベントソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2119
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1661
- 2022年のコンテスト平均難易度/difficulty: 3.2/2349

### 難易度別問題一覧

「イベントソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

　
## 90. 二分探索

### 難易度統計

「二分探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2122
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1758
- 2022年のコンテスト平均難易度/difficulty: 3.5/2364

### 難易度別問題一覧

「二分探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題, difficulty: 1661)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)
- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)
- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

　
## 91. 区間要素数取得

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

　
## 92. 座標圧縮

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

　
## 93. 平面走査

### 難易度統計

「平面走査」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2145
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2145

### 難易度別問題一覧

「平面走査」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

　
## 94. 素数列挙

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

　
## 95. 解法場合分け

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

　
## 96. bitset高速化

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

　
## 97. 基底

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

　
## 98. 線形代数

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

　
## 99. 準同型

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

　
## 100. 包除原理

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

　
## 101. 約数メビウス変換

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

　
## 102. 再帰

### 難易度統計

「再帰」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2318
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1971
- 2022年のコンテスト平均難易度/difficulty: 3/2491

### 難易度別問題一覧

「再帰」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題, difficulty: 2246)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題, difficulty: 1971)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)

　
## 103. bitDP

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

　
## 104. bit全探索

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

　
## 105. 余因子展開

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

　
## 106. 剰余を商に翻訳

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

　
## 107. 平方分割

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

　
## 108. 枝刈り

### 難易度統計

「枝刈り」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2422
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2086
- 2022年のコンテスト平均難易度/difficulty: 3/2758

### 難易度別問題一覧

「枝刈り」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題, difficulty: 2758)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

　
## 109. 変数の対称性

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

　
## 110. 自己写像に翻訳

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

　
## 111. 半分全列挙

### 難易度統計

「半分全列挙」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2595
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2595

### 難易度別問題一覧

「半分全列挙」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

　
## 112. 連長圧縮

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

　
## 113. 区間加算更新

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

　
## 114. ユークリッドの互除法

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

　
## 115. 最大公約数

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

　
## 116. 互いに素に帰着

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

　
## 117. 素因数分解

### 難易度統計

「素因数分解」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2388
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2567
- 2022年のコンテスト平均難易度/difficulty: 2.7/2298

### 難易度別問題一覧

「素因数分解」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題, difficulty: 2291)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題, difficulty: 2567)

　
## 118. ベン図

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

　
## 119. DPのデータ構造高速化

### 難易度統計

「DPのデータ構造高速化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.3/2332
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.3/2332

### 難易度別問題一覧

「DPのデータ構造高速化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題, difficulty: 2758)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
## 120. 調和数列

### 難易度統計

「調和数列」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.3/2354
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1607
- 2022年のコンテスト平均難易度/difficulty: 3.7/2728

### 難易度別問題一覧

「調和数列」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
## 121. B進法

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

　
## 122. 小さいケースの構築を拡張

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

　
## 123. 剰余による確率的判定

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

　
## 124. 最小素因数前計算

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

　
## 125. 交代和

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

　
## 126. 第二種スターリング数

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

　
## 127. floor_sum

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

　
## 128. フロベニウスの硬貨交換問題

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

　
## 129. 像決め打ち二分探索

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

　
## 130. カタラン数

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

　
## 131. 01BFS

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

　
## 132. 区間kth取得

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

　
## 133. ローリングハッシュ

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

　
## 134. 最長共通接頭辞

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

　
## 135. ２進法

### 難易度統計

「２進法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.6/2536
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.6/2536

### 難易度別問題一覧

「２進法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題, difficulty: 2167)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題, difficulty: 3086)

　
## 136. 桁DP

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

　
## 137. 同値関係

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

　
## 138. 高速フーリエ変換

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

　
## 139. 畳み込み

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

　
## 140. 期待値の線形性

### 難易度統計

「期待値の線形性」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2566
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4/2566

### 難易度別問題一覧

「期待値の線形性」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
## 141. 数え上げの平均化

### 難易度統計

「[数え上げの平均化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#数え上げの平均化)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2566
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4/2566

### 難易度別問題一覧

「[数え上げの平均化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#数え上げの平均化)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
## 142. 付値管理

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

　
## 143. キュー

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

　
## 144. マージｓ

### 難易度統計

「マージｓ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2658
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 4/2658
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「マージｓ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題, difficulty: 2658)

　
## 145. 区間を中間で分割してマージ

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

　
## 146. ２次元DPの１次元圧縮

### 難易度統計

「２次元DPの１次元圧縮」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2903
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4/2903

### 難易度別問題一覧

「２次元DPの１次元圧縮」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
## 147. 区間最大・最小値更新

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

　
## 148. 分割統治畳み込み

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

　
## 149. 遅延セグメント木

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

　
## 150. バケット分割

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

　
## 151. 区間二次形式取得

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

　
## 152. 区間二次式取得

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

　
## 153. 最近共通祖先

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

　
## 154. 重軽分解

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

　
## 155. フック長公式

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

　
## 156. ヤング図形

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

　
## 157. トポロジカルソート

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

　
## 158. 強連結成分分解

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

　
## 159. 残余ネットワーク

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

　
## 160. P-再帰

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

　
## 161. 多点評価

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

　
## 162. 評価点シフト

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

　
## 163. アルゴリズム中に追加処理

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

　
## 164. ハミルトン路

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

　
## 165. マージ

### 難易度統計

「マージ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: データなし
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「マージ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)

　
## 166. 期待値漸化式

### 難易度統計

「期待値漸化式」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: データなし
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「期待値漸化式」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)

　
## 167. 構文解析

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

