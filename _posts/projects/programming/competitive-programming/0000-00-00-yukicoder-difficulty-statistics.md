---
layout: project
title: yukicoder過去問解法別難易度統計
date: 2024-10-12
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

通常問題の問題番号2056から2111まで登録し終わりました。先は長いです。


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


それでは以下の解法ごとに問題を列挙し、難易度の傾向を表示します：

1. 特殊な入出力
1. 実装
1. サンプルに帰着
1. 検索
1. 相似
1. カレンダー
1. 累積和
1. ナップサックDP
1. 階差数列
1. 二重和中の同じ値の纏め上げ
1. 多項定理
1. ソート
1. 貪欲法
1. DAG上の動的計画法
1. 幅優先探索（BFS）
1. 全探索
1. 場合分け
1. 素集合データ構造（UnionFind／UF／DSU）
1. 操作逆順
1. [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)
1. 区間管理
1. [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)
1. 頻度表
1. 再帰
1. ニム和
1. [高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)
1. １変数決め打ち
1. 動的計画法（DP）
1. 分枝限定法
1. [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)
1. 一対一対応
1. クエリ先読み
1. 区間要素数取得
1. 座標圧縮
1. 平面走査
1. クエリソート
1. ポラードの$\rho$
1. 剰余による確率的判定
1. 平方剰余
1. イベントソート
1. 区間和取得
1. アルゴリズムのリアクティブ化
1. [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)
1. ２進法
1. 素数列挙
1. 準同型
1. DPのデータ構造高速化
1. ゼータ変換
1. メビウス変換
1. 最小素因数前計算
1. 素因数分解
1. 倍数ゼータ変換
1. 包除原理
1. 約数メビウス変換
1. 自己写像に翻訳
1. 連長圧縮（ランレングス圧縮／RLE）
1. フェニック木（BIT）
1. ユークリッドの互除法
1. 互いに素に帰着
1. 桁DP
1. [最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)
1. 高速フーリエ変換
1. 畳み込み
1. bitごとに計算
1. 第二種スターリング数
1. floor_sum
1. フロベニウスの硬貨交換問題
1. 像決め打ち二分探索
1. 二分探索
1. 01BFS
1. 区間kth取得
1. 期待値の線形性
1. [数え上げの平均化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#数え上げの平均化)
1. ハミルトン路
1. マージ
1. 構文解析
1. 木DP

ただし難易度が未設定の問題があれば、★1と換算します。


　
## 1. 特殊な入出力

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

　
## 2. 実装

### 難易度統計

「実装」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.3/787
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.3/787

### 難易度別問題一覧

「実装」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題, difficulty: 406)
- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題, difficulty: 1095)

　
## 3. サンプルに帰着

### 難易度統計

「サンプルに帰着」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/588
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.5/588

### 難易度別問題一覧

「サンプルに帰着」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)

　
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

　
## 6. カレンダー

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

　
## 7. 累積和

### 難易度統計

「累積和」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.7/806
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 1.7/806

### 難易度別問題一覧

「累積和」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題, difficulty: 406)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)

　
## 8. ナップサックDP

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

　
## 9. 階差数列

### 難易度統計

「階差数列」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1206
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1206

### 難易度別問題一覧

「階差数列」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)

　
## 10. 二重和中の同じ値の纏め上げ

### 難易度統計

「二重和中の同じ値の纏め上げ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1206
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1206

### 難易度別問題一覧

「二重和中の同じ値の纏め上げ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)

　
## 11. 多項定理

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

　
## 12. ソート

### 難易度統計

「ソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1482
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1482

### 難易度別問題一覧

「ソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)

　
## 13. 貪欲法

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

　
## 14. DAG上の動的計画法

### 難易度統計

「DAG上の動的計画法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1577
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1577

### 難易度別問題一覧

「DAG上の動的計画法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2100">No.2100 [Cherry Alpha C] Two-way Steps</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - D問題, difficulty: 1577)

　
## 15. 幅優先探索

### 難易度統計

「幅優先探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1582
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2/1582

### 難易度別問題一覧

「幅優先探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2064">No.2064 Smallest Sequence on Grid</a> (yukicoder contest 359 (2022-09-02) - B問題, difficulty: 1582)

　
## 16. 全探索

### 難易度統計

「全探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1717
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.2/1717

### 難易度別問題一覧

「全探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題, difficulty: 969)
- <a href="https://yukicoder.me/problems/no/2091">No.2091 Shio Ramen (Easy)</a> (単発出題)

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題, difficulty: 1529)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)

　
## 17. 場合分け

### 難易度統計

「場合分け」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1621
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.3/1621

### 難易度別問題一覧

「場合分け」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題, difficulty: 969)
- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)
- <a href="https://yukicoder.me/problems/no/2102">No.2102 [Cherry Alpha *] Conditional Reflection</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - F問題, difficulty: 1948)

　
## 18. 素集合データ構造

### 難易度統計

「素集合データ構造」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1486
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1486

### 難易度別問題一覧

「素集合データ構造」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題, difficulty: 1486)

　
## 19. 操作逆順

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

　
## 20. 表示可能性DP

### 難易度統計

「表示可能性DP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1641
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1641

### 難易度別問題一覧

「表示可能性DP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)

　
## 21. 区間管理

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

　
## 22. 不変量を保つ戦略

### 難易度統計

「不変量を保つ戦略」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1649
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1649

### 難易度別問題一覧

「不変量を保つ戦略」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)

　
## 23. 頻度表

### 難易度統計

「頻度表」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1802
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1802

### 難易度別問題一覧

「頻度表」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題, difficulty: 1802)

　
## 24. 再帰

### 難易度統計

「再帰」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1916
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/1916

### 難易度別問題一覧

「再帰」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)

　
## 25. ニム和

### 難易度統計

「ニム和」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2008
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2008

### 難易度別問題一覧

「ニム和」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)

　
## 26. 高さ奇数ニム和

### 難易度統計

「高さ奇数ニム和」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2008
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2008

### 難易度別問題一覧

「高さ奇数ニム和」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)

　
## 27. １変数決め打ち

### 難易度統計

「１変数決め打ち」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2175
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.5/2175

### 難易度別問題一覧

「１変数決め打ち」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題, difficulty: 2620)

　
## 28. 動的計画法

### 難易度統計

「動的計画法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.6/2011
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.6/2011

### 難易度別問題一覧

「動的計画法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題, difficulty: 843)
- <a href="https://yukicoder.me/problems/no/2095">No.2095 High Rise</a> (yukicoder contest 363 (2022-10-07) - D問題, difficulty: 1518)
- <a href="https://yukicoder.me/problems/no/2100">No.2100 [Cherry Alpha C] Two-way Steps</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - D問題, difficulty: 1577)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題, difficulty: 2620)
- <a href="https://yukicoder.me/problems/no/2082">No.2082 AND OR XOR</a> (yukicoder contest 361 (2022-09-25) - E問題, difficulty: 2501)
- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)
- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)

　
## 29. 分枝限定法

### 難易度統計

「分枝限定法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1943
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.7/1943

### 難易度別問題一覧

「分枝限定法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題, difficulty: 1728)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
## 30. 損をしない変形

### 難易度統計

「損をしない変形」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/2109
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 2.7/2109

### 難易度別問題一覧

「損をしない変形」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題, difficulty: 1529)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2096">No.2096 Rage With Our Friends</a> (yukicoder contest 363 (2022-10-07) - E問題, difficulty: 2690)

　
## 31. 一対一対応

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

　
## 32. クエリ先読み

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

　
## 33. 区間要素数取得

### 難易度統計

「区間要素数取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1696
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1696

### 難易度別問題一覧

「区間要素数取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)

　
## 34. 座標圧縮

### 難易度統計

「座標圧縮」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1696
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1696

### 難易度別問題一覧

「座標圧縮」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)

　
## 35. 平面走査

### 難易度統計

「平面走査」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1696
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/1696

### 難易度別問題一覧

「平面走査」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)

　
## 36. クエリソート

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

　
## 37. ポラードの$\rho$

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

　
## 38. 剰余による確率的判定

### 難易度統計

「剰余による確率的判定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2047
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2047

### 難易度別問題一覧

「剰余による確率的判定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)

　
## 39. 平方剰余

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

　
## 40. イベントソート

### 難易度統計

「イベントソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2049
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2049

### 難易度別問題一覧

「イベントソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)

　
## 41. 区間和取得

### 難易度統計

「区間和取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2049
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2049

### 難易度別問題一覧

「区間和取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)

　
## 42. アルゴリズムのリアクティブ化

### 難易度統計

「アルゴリズムのリアクティブ化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2139
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2139

### 難易度別問題一覧

「アルゴリズムのリアクティブ化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題, difficulty: 2139)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)

　
## 43. 解法場合分け

### 難易度統計

「解法場合分け」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2144
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2144

### 難易度別問題一覧

「解法場合分け」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
## 44. ２進法

### 難易度統計

「２進法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2167
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2167

### 難易度別問題一覧

「２進法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題, difficulty: 2167)

　
## 45. 素数列挙

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

　
## 46. 準同型

### 難易度統計

「準同型」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2295
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2295

### 難易度別問題一覧

「準同型」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題, difficulty: 2295)

　
## 47. DPのデータ構造高速化

### 難易度統計

「DPのデータ構造高速化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2306
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「DPのデータ構造高速化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
## 48. ゼータ変換

### 難易度統計

「ゼータ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2306
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「ゼータ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
## 49. メビウス変換

### 難易度統計

「メビウス変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2306
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「メビウス変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
## 50. 最小素因数前計算

### 難易度統計

「最小素因数前計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2306
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「最小素因数前計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
## 51. 素因数分解

### 難易度統計

「素因数分解」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2306
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「素因数分解」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
## 52. 倍数ゼータ変換

### 難易度統計

「倍数ゼータ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2306
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「倍数ゼータ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
## 53. 包除原理

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

　
## 54. 約数メビウス変換

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

　
## 55. 自己写像に翻訳

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

　
## 56. 連長圧縮

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

　
## 57. フェニック木

### 難易度統計

「フェニック木」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2150
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.1/2150

### 難易度別問題一覧

「フェニック木」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)

　
## 58. ユークリッドの互除法

### 難易度統計

「ユークリッドの互除法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2278
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.1/2278

### 難易度別問題一覧

「ユークリッドの互除法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題, difficulty: 2139)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
## 59. 互いに素に帰着

### 難易度統計

「互いに素に帰着」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.2/2347
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.2/2347

### 難易度別問題一覧

「互いに素に帰着」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
## 60. 桁DP

### 難易度統計

「桁DP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.3/2450
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.3/2450

### 難易度別問題一覧

「桁DP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題, difficulty: 2047)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
## 61. 最終手番の任意性

### 難易度統計

「最終手番の任意性」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/1948
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/1948

### 難易度別問題一覧

「最終手番の任意性」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2102">No.2102 [Cherry Alpha *] Conditional Reflection</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - F問題, difficulty: 1948)

　
## 62. 高速フーリエ変換

### 難易度統計

「高速フーリエ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2553
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2553

### 難易度別問題一覧

「高速フーリエ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

　
## 63. 畳み込み

### 難易度統計

「畳み込み」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2553
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2553

### 難易度別問題一覧

「畳み込み」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

　
## 64. bitごとに計算

### 難易度統計

「bitごとに計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2643
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2643

### 難易度別問題一覧

「bitごとに計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)

　
## 65. 第二種スターリング数

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

　
## 66. floor_sum

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

　
## 67. フロベニウスの硬貨交換問題

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

　
## 68. 像決め打ち二分探索

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

　
## 69. 二分探索

### 難易度統計

「二分探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2677
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2677

### 難易度別問題一覧

「二分探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)
- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)
- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)

　
## 70. 01BFS

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

　
## 71. 区間kth取得

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

　
## 72. 期待値の線形性

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

　
## 73. 数え上げの平均化

### 難易度統計

「数え上げの平均化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 4/2566
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 4/2566

### 難易度別問題一覧

「数え上げの平均化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
## 74. ハミルトン路

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

　
## 75. マージ

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

　
## 76. 構文解析

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

　
## 77. 木DP

### 難易度統計

「木DP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: データなし
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「木DP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)

