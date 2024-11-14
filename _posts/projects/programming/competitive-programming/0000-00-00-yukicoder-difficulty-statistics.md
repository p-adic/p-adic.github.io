---
layout: project
title: yukicoder過去問解法別難易度統計
date: 2024-11-14
excerpt: "yukicoderの過去問の解法別の難易度に関する統計データです。"
parent: competitive-programming-project/
prev-child: competitive-programming-creating-problem-status
next-child: yukicoder-difficulty-statistics-solution-name
project: true
image-directory: competitive-programming
tags: [競技プログラミング,数学]
---

yukicoder contest 358 (2022-08-26) 以降に出題されたyuicoderの問題で筆者（$p$進大好きbot）がupsolveした問題の解法をまとめ、解法別に難易度（writerに設定されたレベルおよび解かれ具合から算出されたdifficuluty）統計をします。難易度投票結果も集計しようか迷いましたが、集計タイミングによって結果が変わってしまうので情報が時々刻々と古くなってしまうことから集計しないことに決めました。


## 進捗

通常問題の問題番号2056から2625までと2953以降を登録し終わりました。先は長いです。


## 用途

主にyukicoderコンテストの問題に対して

- コンテスト中の考察時に
  - 類題を検索する。
  - 該当レベルで頻出なアルゴリズムを検索する。
  - 解法の候補を絞り込む際にその解法の標準的な出題レベルを照会する。
- 作問／tester時に
  - 既出を検索する。
  - 想定解法からレベルの下限を見積もる。

といった使い方をするための自分用の統計ページです。必然的に想定解法に触れることになるので、ネタバレにご注意ください。アルゴリズムのみに注目した難易度統計であるため、ジャッジの特殊性や考察難易度などアルゴリズム以外に難易度に寄与する部分は一切考慮しないため、難易度評価の下界としてのみ参考にすることができます。

コンテスト出題でない単発出題や通常コンテスト以外で出題された問題などは上記の目的に合致しないため、以下のように処理しています：

- 問題番号が2056以上3000以下の問題しか集計しない。（ネタ問題等が集計しない目的）
- コンテスト出題でない単発出題は各解法の難易度別問題一覧には掲載するものの、難易度平均計算時は集計しない。

１つ目のルールの影響で、問題公開後に通常問題タグから別の問題タグに移動した問題についてはあまり直感的でない集計結果となります。例えば数学的知識問題には集計されるもの（[No.2466 Root! Root! Root!](https://yukicoder.me/problems/no/2466)）とされないもの（[No.3094 Character Table](https://yukicoder.me/problems/no/3094)）があります。


## 集計方法

先述したように、解法を集計する対象は筆者がupsolveした問題に限られることにご注意ください。

後述するように解説ページも手作業で読んで集計するため、upsolveしていない問題も集計してしまうともったいないからです。また手作業での集計となるため、解法の勘違いなどで集計のミスをする可能性もあることにご注意ください。

基本的には★3以下の通常問題を全てupsolveしているはずですが、upsolveに時間がかかるため問題公開から数週間の遅れが生じることもあります。★3.5以上はほとんどupsolveしていないのでデータとしては不十分です。


### データ取得元

[yukicoder](https://yukicoder.me/)の問題ページ（解説ページ等含む）とコンテスト順位表ページからdifficulty以外のデータを取得し、[yukicoder problems](https://iilj.github.io/yukicoder-problems/#/list/)のListページからdifficultyのデータを取得しています。

ただし問題の解法は必ずしもタグ登録されていないため、タグ情報ではなく解説ページを用いて自分で考察し直した結果を集計しています。そのため解法の集計にミスがある可能性があります。


### 解法の集計

各問題を、その解法を構成するアルゴリズムや典型考察で類別し、難易度統計を取ります。

１つの問題にはたいてい複数の解法がありますが、その中で主観的に最も簡単なもののみを集計対象とします。

例えばフェニック木（BIT）を用いたシンプルな解法と、遅延評価セグメント木を用いた複雑な解法がある場合、前者のみを集計します。

また集計対象の１つの解法にはたいてい複数のアルゴリズムや典型考察が組み合わさっていますが、その中で主観的に最も難しいものと比較して特筆すべきもののみを集計対象のアルゴリズムと典型考察とします。

例えば集計対象の１つの解法が単純なソートと単純な場合分けのみを用いる場合はソートと場合分けの両方を集計しますが、一方で集計対象の１つの解法が単純なソートと単純な場合分けとConvex Hull Trick（CHT）のみを用いる場合は単純なソートや単純な場合分けが特筆すべきものでないのでConvex Hull Trickのみを集計します。

もし単純なソートや単純な場合分けでなく、ソートすることや場合分けすることに非自明な考察が要求される場合はそれらも集計します。要するに解法に要求されるアルゴリズムや典型考察の中で主観的に特筆すべきものを集計します。

具体的には、64bit整数が集計されているのは★1.5以下の問題だけですし、階乗逆元が集計されているのは★3以下の問題だけです。これは★2以上では64bit整数の使用が特筆するほど高度なテクニックでなく、★3.5以上では階乗逆元が特筆するほど高度なテクニックでないというだけです。★2以上では64bit整数が使われない、★3.5以上では階乗逆元が使われない、という意味ではないのでご注意ください。


### 解法以外の集計

解法以外の集計には解説ページを用いないため、筆者がupsolveした問題以外の問題も集計しています。

問題の日付を記載する際は問題の公開開始日ではなくコンテストの開始日を表します。（特にAdvent Calender Contestで両者にズレが生じます）


### 特殊な文字の表記

問題タイトルは基本的に原題をそのまま表記していますが、例外として

- [No.2403 "Eight" Bridges of K(oの上にウムラウト)nigsberg](https://yukicoder.me/problems/no/2403)
- [No.2473 Fraises dans une bo(iの上にアクサン・シルコンフレクス)te](https://yukicoder.me/problems/no/2473)
- [No.2878 $\mathbb{IGNITION}$](https://yukicoder.me/problems/no/2878)

はこちらの自動化処理環境の都合

- No.2403 "Eight" Bridges of Konigsberg
- No.2473 Fraises dans une boite
- No.2878 IGNITION

と記載させていただきます。同様に解法名の

- Lindstr(oの上にウムラウト)m-Gessel-Viennotの補題

は

- Lindstrom-Gessel-Viennotの補題

と記載させていただきます。


## レベルごとの平均difficulty

問題2056から問題2959のうち

- コンテスト出題であり（単発出題でなく）かつ
- レベルが設定されておりかつ
- difficultyが算出されているもの

を対象にレベルごとにコンテスト平均difficultyを算出したデータです。


### ★

- 全体: diff <font color="brown">520</font>（66問）
- 2024年: diff <font color="brown">618</font>（34問）
- 2023年: diff <font color="gray">370</font>（28問）
- 2022年: diff <font color="brown">742</font>（4問）

### ★☆

- 全体: diff <font color="green">943</font>（92問）
- 2024年: diff <font color="green">982</font>（42問）
- 2023年: diff <font color="green">934</font>（38問）
- 2022年: diff <font color="green">831</font>（12問）

### ★★

- 全体: diff <font color="deepskyblue">1340</font>（131問）
- 2024年: diff <font color="deepskyblue">1429</font>（56問）
- 2023年: diff <font color="deepskyblue">1240</font>（58問）
- 2022年: diff <font color="deepskyblue">1389</font>（17問）

### ★★☆

- 全体: diff <font color="blue">1825</font>（157問）
- 2024年: diff <font color="blue">1838</font>（61問）
- 2023年: diff <font color="blue">1798</font>（78問）
- 2022年: diff <font color="blue">1899</font>（18問）

### ★★★

- 全体: diff <font color="yellowgreen">2241</font>（161問）
- 2024年: diff <font color="yellowgreen">2268</font>（72問）
- 2023年: diff <font color="yellowgreen">2211</font>（67問）
- 2022年: diff <font color="yellowgreen">2245</font>（22問）

### ★★★☆

- 全体: diff <font color="orange">2577</font>（133問）
- 2024年: diff <font color="orange">2566</font>（50問）
- 2023年: diff <font color="orange">2570</font>（63問）
- 2022年: diff <font color="orange">2627</font>（20問）

### ★★★★

- 全体: diff <font color="red">2823</font>（70問）
- 2024年: diff <font color="red">2823</font>（19問）
- 2023年: diff <font color="red">2843</font>（42問）
- 2022年: diff <font color="orange">2724</font>（9問）

### ★★★★☆

- 全体: diff <font color="red">3142</font>（23問）
- 2024年: diff <font color="red">2972</font>（8問）
- 2023年: diff <font color="red">3174</font>（10問）
- 2022年: diff <font color="darkgoldenrod ">3349</font>（5問）

### ★★★★★

- 全体: diff <font color="darkgoldenrod ">3263</font>（21問）
- 2024年: diff <font color="darkgoldenrod ">3450</font>（2問）
- 2023年: diff <font color="red">3199</font>（13問）
- 2022年: diff <font color="darkgoldenrod ">3339</font>（6問）

### ★★★★★☆

- 全体: diffデータなし
- 2024年: diffデータなし
- 2023年: diffデータなし
- 2022年: diffデータなし

### ★★★★★★

- 全体: diffデータなし
- 2024年: diffデータなし
- 2023年: diffデータなし
- 2022年: diffデータなし


## 登録済み解法一覧

以下の解法ごとに問題を列挙し、年ごとの難易度の傾向を表示します（解法名左の数値は「コンテスト平均レベル/コンテスト平均difficulty/問題数」）：

1. （★1.2／diff <font color="brown">609</font>／37問）<a href="#実装" class="tag">実装</a>
1. （★1.2／diff <font color="brown">704</font>／2問）<a href="#カレンダー計算" class="tag">カレンダー計算</a>
1. （★1.4／diff <font color="green">842</font>／14問）<a href="#64bit整数" class="tag">64bit整数</a>
1. （★1.4／diff <font color="green">868</font>／10問）<a href="#数値の文字列受け取り" class="tag">数値の文字列受け取り</a>
1. （★1.4／diff <font color="green">941</font>／12問）<a href="#特殊な入出力" class="tag">特殊な入出力</a>
1. （★1.5／diff <font color="gray">344</font>／1問）<a href="#複素数" class="tag">複素数</a>
1. （★1.5／diff <font color="brown">477</font>／2問）<a href="#基数の変換" class="tag">基数の変換</a>
1. （★1.5／diff <font color="brown">588</font>／1問）<a href="#相似" class="tag">相似</a>
1. （★1.5／diff <font color="brown">627</font>／1問）<a href="#setprecision" class="tag">setprecision</a>
1. （★1.5／diff <font color="brown">708</font>／2問）<a href="#符号なし64bit整数" class="tag">符号なし64bit整数</a>
1. （★1.5／diff <font color="brown">775</font>／1問）<a href="#next_permutation" class="tag">next_permutation</a>
1. （★1.5／diff <font color="brown">775</font>／1問）<a href="#４重以上のループ" class="tag">４重以上のループ</a>
1. （★1.5／diff <font color="brown">775</font>／1問）<a href="#再帰による多重ループ実装" class="tag">再帰による多重ループ実装</a>
1. （★1.5／diff <font color="green">959</font>／1問）<a href="#試行回数の期待値を各試行の実施確率の和に帰着" class="tag">試行回数の期待値を各試行の実施確率の和に帰着</a>
1. （★1.5／diff <font color="green">959</font>／1問）<a href="#等差数列と等比数列の各点積の累積和計算" class="tag">等差数列と等比数列の各点積の累積和計算</a>
1. （★1.5／diff <font color="green">1060</font>／1問）<a href="#場合分けによる絶対値計算" class="tag">場合分けによる絶対値計算</a>
1. （★1.5／diff <font color="deepskyblue">1247</font>／1問）<a href="#証明をなぞる構築" class="tag">証明をなぞる構築</a>
1. （★1.5／diff <font color="deepskyblue">1290</font>／2問）<a href="#中国剰余定理" class="tag">中国剰余定理</a>／CRT
1. （★1.5／diff <font color="deepskyblue">1313</font>／1問）<a href="#multiset" class="tag">multiset</a>
1. （★1.5／diff <font color="deepskyblue">1356</font>／1問）<a href="#決め打ちによる構築" class="tag">決め打ちによる構築</a>
1. （★1.5／diff <font color="yellowgreen">2185</font>／1問）<a href="#getline" class="tag">getline</a>
1. （★1.6／diff <font color="green">1175</font>／6問）<a href="#１次式の最大・最小値計算" class="tag">１次式の最大・最小値計算</a>
1. （★1.6／diff <font color="deepskyblue">1206</font>／3問）<a href="#組分けの余りに注目" class="tag">組分けの余りに注目</a>
1. （★1.7／diff <font color="deepskyblue">1441</font>／2問）<a href="#解の公式" class="tag">解の公式</a>
1. （★1.8／diff <font color="green">1009</font>／5問）<a href="#set" class="tag">set</a>
1. （★1.8／diff <font color="deepskyblue">1348</font>／4問）<a href="#重複選択可ナップサック最適化" class="tag">重複選択可ナップサック最適化</a>
1. （★1.8／diff <font color="deepskyblue">1453</font>／8問）<a href="#連想配列" class="tag">連想配列</a>
1. （★1.9／diff <font color="deepskyblue">1285</font>／16問）<a href="#シミュレーション" class="tag">シミュレーション</a>
1. （★2／diff <font color="brown">657</font>／1問）<a href="#最近点計算" class="tag">最近点計算</a>
1. （★2／diff <font color="green">912</font>／1問）<a href="#グランディ数計算" class="tag">グランディ数計算</a>
1. （★2／diff <font color="green">939</font>／1問）<a href="#遷移の収束" class="tag">遷移の収束</a>
1. （★2／diff <font color="green">1049</font>／1問）<a href="#ド・モルガンの法則" class="tag">ド・モルガンの法則</a>
1. （★2／diff <font color="green">1050</font>／3問）<a href="#巡回置換表示" class="tag">巡回置換表示</a>
1. （★2／diff <font color="deepskyblue">1208</font>／1問）<a href="#三平方の定理" class="tag">三平方の定理</a>
1. （★2／diff <font color="deepskyblue">1257</font>／6問）<a href="#小数誤差" class="tag">小数誤差</a>
1. （★2／diff <font color="deepskyblue">1273</font>／1問）<a href="#整礎性" class="tag">整礎性</a>
1. （★2／diff <font color="deepskyblue">1344</font>／5問）<a href="#等差数列の累積和計算" class="tag">等差数列の累積和計算</a>
1. （★2／diff <font color="deepskyblue">1352</font>／1問）<a href="#負コストナップサック最適化" class="tag">負コストナップサック最適化</a>
1. （★2／diff <font color="deepskyblue">1413</font>／11問）<a href="#頻度表" class="tag">頻度表</a>
1. （★2／diff <font color="deepskyblue">1585</font>／1問）<a href="#素因数分解による最小公倍数計算" class="tag">素因数分解による最小公倍数計算</a>
1. （★2／diff <font color="deepskyblue">1585</font>／1問）<a href="#置換の合成" class="tag">置換の合成</a>
1. （★2／diff <font color="blue">1605</font>／1問）<a href="#ルジャンドルの公式" class="tag">ルジャンドルの公式</a>
1. （★2／diff <font color="blue">1629</font>／1問）<a href="#二項定理" class="tag">二項定理</a>
1. （★2／diff <font color="blue">1644</font>／2問）<a href="#多次元コスト重複選択可ナップサック最適化" class="tag">多次元コスト重複選択可ナップサック最適化</a>
1. （★2／diff <font color="yellowgreen">2275</font>／1問）<a href="#剰余計算を桁の線形和に帰着" class="tag">剰余計算を桁の線形和に帰着</a>
1. （★2.1／diff <font color="deepskyblue">1322</font>／10問）<a href="#ナップサック最適化" class="tag">ナップサック最適化</a>
1. （★2.1／diff <font color="deepskyblue">1358</font>／4問）<a href="#等比数列の累積和計算" class="tag">等比数列の累積和計算</a>
1. （★2.1／diff <font color="deepskyblue">1387</font>／3問）<a href="#多次元コストナップサック最適化" class="tag">多次元コストナップサック最適化</a>
1. （★2.1／diff <font color="deepskyblue">1494</font>／46問）<a href="#場合分け" class="tag">場合分け</a>
1. （★2.1／diff <font color="deepskyblue">1494</font>／63問）<a href="#全探索" class="tag">全探索</a>
1. （★2.1／diff <font color="deepskyblue">1533</font>／3問）<a href="#分割の均等化" class="tag">分割の均等化</a>
1. （★2.1／diff <font color="deepskyblue">1552</font>／13問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作を数値に翻訳)）<a href="#操作を数値に翻訳" class="tag">操作を数値に翻訳</a>
1. （★2.1／diff <font color="deepskyblue">1584</font>／5問）<a href="#動的mod" class="tag">動的mod</a>
1. （★2.1／diff <font color="blue">1674</font>／6問）<a href="#平方根" class="tag">平方根</a>
1. （★2.2／diff <font color="deepskyblue">1335</font>／12問）<a href="#素集合データ構造" class="tag">素集合データ構造</a>／UnionFind／UF／DSU
1. （★2.2／diff <font color="deepskyblue">1335</font>／12問）<a href="#連結成分取得" class="tag">連結成分取得</a>
1. （★2.2／diff <font color="deepskyblue">1346</font>／5問）<a href="#サンプルに帰着" class="tag">サンプルに帰着</a>
1. （★2.2／diff <font color="deepskyblue">1412</font>／2問）<a href="#三角形の成立条件" class="tag">三角形の成立条件</a>
1. （★2.2／diff <font color="deepskyblue">1415</font>／15問）<a href="#幅優先探索" class="tag">幅優先探索</a>／BFS
1. （★2.2／diff <font color="deepskyblue">1421</font>／4問）<a href="#三角形の面積計算" class="tag">三角形の面積計算</a>
1. （★2.2／diff <font color="deepskyblue">1496</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)）<a href="#表示可能性DP" class="tag">表示可能性DP</a>
1. （★2.2／diff <font color="deepskyblue">1517</font>／7問）<a href="#素因数分解による約数の生成式" class="tag">素因数分解による約数の生成式</a>
1. （★2.2／diff <font color="deepskyblue">1517</font>／7問）<a href="#約数列挙" class="tag">約数列挙</a>
1. （★2.2／diff <font color="deepskyblue">1531</font>／24問）<a href="#貪欲法" class="tag">貪欲法</a>
1. （★2.2／diff <font color="deepskyblue">1540</font>／2問）<a href="#ヘルド・カープ法" class="tag">ヘルド・カープ法</a>／Held-Karp法
1. （★2.2／diff <font color="deepskyblue">1572</font>／8問）<a href="#操作の纏め上げ" class="tag">操作の纏め上げ</a>
1. （★2.2／diff <font color="deepskyblue">1586</font>／4問）<a href="#多項係数と組み合わせの関係" class="tag">多項係数と組み合わせの関係</a>
1. （★2.2／diff <font color="deepskyblue">1587</font>／2問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#重複選択個数の線形関係式)）<a href="#重複選択個数の線形関係式" class="tag">重複選択個数の線形関係式</a>
1. （★2.2／diff <font color="blue">1606</font>／9問）<a href="#小数計算の整数への帰着" class="tag">小数計算の整数への帰着</a>
1. （★2.2／diff <font color="blue">1716</font>／2問）<a href="#連長圧縮" class="tag">連長圧縮</a>／ランレングス圧縮／RLE
1. （★2.2／diff <font color="blue">1747</font>／2問）<a href="#括弧列判定" class="tag">括弧列判定</a>
1. （★2.2／diff <font color="blue">1762</font>／2問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)）<a href="#良いケースに帰着" class="tag">良いケースに帰着</a>
1. （★2.2／diff <font color="blue">1795</font>／2問）<a href="#ウノ計算" class="tag">ウノ計算</a>
1. （★2.2／diff <font color="blue">1844</font>／2問）<a href="#不定方程式の因数分解" class="tag">不定方程式の因数分解</a>
1. （★2.3／diff <font color="deepskyblue">1296</font>／5問）<a href="#ナップサックDP" class="tag">ナップサックDP</a>
1. （★2.3／diff <font color="deepskyblue">1307</font>／4問）<a href="#門松列DP" class="tag">門松列DP</a>
1. （★2.3／diff <font color="deepskyblue">1449</font>／9問）<a href="#マッチ度ごとに管理" class="tag">マッチ度ごとに管理</a>
1. （★2.3／diff <font color="deepskyblue">1485</font>／4問）<a href="#実験" class="tag">実験</a>
1. （★2.3／diff <font color="blue">1608</font>／5問）<a href="#一要素削除" class="tag">一要素削除</a>
1. （★2.3／diff <font color="blue">1638</font>／10問）<a href="#同じ値の纏め上げ" class="tag">同じ値の纏め上げ</a>
1. （★2.3／diff <font color="blue">1647</font>／12問）<a href="#試し割り法" class="tag">試し割り法</a>
1. （★2.3／diff <font color="blue">1660</font>／3問）<a href="#最小公倍数計算" class="tag">最小公倍数計算</a>
1. （★2.3／diff <font color="blue">1668</font>／19問）<a href="#累積積" class="tag">累積積</a>
1. （★2.3／diff <font color="blue">1779</font>／30問）<a href="#変数決め打ち" class="tag">変数決め打ち</a>
1. （★2.3／diff <font color="blue">1815</font>／3問）<a href="#円周角の定理" class="tag">円周角の定理</a>／タレスの定理
1. （★2.3／diff <font color="blue">1873</font>／4問）<a href="#アルゴリズムのリアクティブ化" class="tag">アルゴリズムのリアクティブ化</a>
1. （★2.4／diff <font color="deepskyblue">1555</font>／8問）<a href="#余事象" class="tag">余事象</a>
1. （★2.4／diff <font color="blue">1627</font>／10問）<a href="#ギャグ" class="tag">ギャグ</a>
1. （★2.4／diff <font color="blue">1657</font>／16問）<a href="#累積和" class="tag">累積和</a>
1. （★2.4／diff <font color="blue">1671</font>／13問）<a href="#階乗計算" class="tag">階乗計算</a>
1. （★2.4／diff <font color="blue">1684</font>／9問）<a href="#階乗逆元計算" class="tag">階乗逆元計算</a>
1. （★2.4／diff <font color="blue">1753</font>／71問）<a href="#剰余計算" class="tag">剰余計算</a>
1. （★2.4／diff <font color="blue">1799</font>／29問）<a href="#ソート" class="tag">ソート</a>
1. （★2.4／diff <font color="blue">1827</font>／6問）<a href="#２変数決め打ち" class="tag">２変数決め打ち</a>
1. （★2.4／diff <font color="blue">1855</font>／8問）<a href="#最終手番に注目" class="tag">最終手番に注目</a>
1. （★2.5／diff <font color="green">1172</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#合成による次元削減)）<a href="#合成による次元削減" class="tag">合成による次元削減</a>
1. （★2.5／diff <font color="deepskyblue">1200</font>／1問）<a href="#最長歩道計算" class="tag">最長歩道計算</a>
1. （★2.5／diff <font color="deepskyblue">1200</font>／1問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着)）<a href="#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着" class="tag">操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着</a>
1. （★2.5／diff <font color="deepskyblue">1318</font>／1問）<a href="#３進法" class="tag">３進法</a>
1. （★2.5／diff <font color="deepskyblue">1358</font>／1問）<a href="#範囲加算更新を１つの配列に纏め上げ" class="tag">範囲加算更新を１つの配列に纏め上げ</a>
1. （★2.5／diff <font color="deepskyblue">1408</font>／4問）<a href="#DAG上のDP" class="tag">DAG上のDP</a>
1. （★2.5／diff <font color="deepskyblue">1424</font>／2問）<a href="#B進法による構築" class="tag">B進法による構築</a>
1. （★2.5／diff <font color="deepskyblue">1469</font>／1問）<a href="#部分和と補部分和の差の最小化" class="tag">部分和と補部分和の差の最小化</a>
1. （★2.5／diff <font color="deepskyblue">1486</font>／1問）<a href="#操作逆順" class="tag">操作逆順</a>
1. （★2.5／diff <font color="deepskyblue">1488</font>／1問）<a href="#隣接不等式管理" class="tag">隣接不等式管理</a>
1. （★2.5／diff <font color="deepskyblue">1489</font>／1問）<a href="#挿入ソート" class="tag">挿入ソート</a>
1. （★2.5／diff <font color="deepskyblue">1536</font>／1問）<a href="#最遠点計算" class="tag">最遠点計算</a>
1. （★2.5／diff <font color="deepskyblue">1536</font>／1問）<a href="#符号全探索による絶対値計算" class="tag">符号全探索による絶対値計算</a>
1. （★2.5／diff <font color="deepskyblue">1544</font>／2問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を被覆の先頭項管理で処理)）<a href="#指定序数の値の計算を被覆の先頭項管理で処理" class="tag">指定序数の値の計算を被覆の先頭項管理で処理</a>
1. （★2.5／diff <font color="deepskyblue">1577</font>／2問）<a href="#言及する成分数を最大化する質問" class="tag">言及する成分数を最大化する質問</a>
1. （★2.5／diff <font color="blue">1607</font>／1問）<a href="#倍数メビウス変換" class="tag">倍数メビウス変換</a>
1. （★2.5／diff <font color="blue">1619</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不明な想定解)）<a href="#不明な想定解" class="tag">不明な想定解</a>
1. （★2.5／diff <font color="blue">1626</font>／6問）<a href="#階乗による二項係数計算" class="tag">階乗による二項係数計算</a>
1. （★2.5／diff <font color="blue">1653</font>／10問）<a href="#尺取り法" class="tag">尺取り法</a>
1. （★2.5／diff <font color="blue">1661</font>／1問）<a href="#部分回文列挙" class="tag">部分回文列挙</a>
1. （★2.5／diff <font color="blue">1672</font>／11問）<a href="#区間族管理" class="tag">区間族管理</a>
1. （★2.5／diff <font color="blue">1698</font>／2問）<a href="#最大公約数による最小公倍数計算" class="tag">最大公約数による最小公倍数計算</a>
1. （★2.5／diff <font color="blue">1705</font>／2問）<a href="#枝刈り" class="tag">枝刈り</a>
1. （★2.5／diff <font color="blue">1724</font>／3問）<a href="#ポテンシャル付き素集合データ構造" class="tag">ポテンシャル付き素集合データ構造</a>
1. （★2.5／diff <font color="blue">1724</font>／3問）<a href="#頂点倍化" class="tag">頂点倍化</a>
1. （★2.5／diff <font color="blue">1727</font>／3問）<a href="#円環の倍化実装" class="tag">円環の倍化実装</a>
1. （★2.5／diff <font color="blue">1728</font>／1問）<a href="#部分集合DP" class="tag">部分集合DP</a>
1. （★2.5／diff <font color="blue">1742</font>／4問）<a href="#充足可能性判定" class="tag">充足可能性判定</a>
1. （★2.5／diff <font color="blue">1761</font>／12問）<a href="#不変量に注目" class="tag">不変量に注目</a>
1. （★2.5／diff <font color="blue">1764</font>／2問）<a href="#木の頂点の次数計算" class="tag">木の頂点の次数計算</a>
1. （★2.5／diff <font color="blue">1768</font>／1問）<a href="#Vieta Jumping" class="tag">Vieta Jumping</a>／Root Flipping
1. （★2.5／diff <font color="blue">1768</font>／2問）<a href="#解と係数の関係" class="tag">解と係数の関係</a>
1. （★2.5／diff <font color="blue">1774</font>／1問）<a href="#価値上限ありナップサック最適化" class="tag">価値上限ありナップサック最適化</a>
1. （★2.5／diff <font color="blue">1774</font>／1問）<a href="#重複選択可価値上限ありナップサック最適化" class="tag">重複選択可価値上限ありナップサック最適化</a>
1. （★2.5／diff <font color="blue">1816</font>／56問）<a href="#分割統治法" class="tag">分割統治法</a>
1. （★2.5／diff <font color="blue">1818</font>／13問）<a href="#逆元の再帰式" class="tag">逆元の再帰式</a>
1. （★2.5／diff <font color="blue">1831</font>／3問）<a href="#多項定理" class="tag">多項定理</a>
1. （★2.5／diff <font color="blue">1838</font>／1問）<a href="#オイラーの定理" class="tag">オイラーの定理</a>
1. （★2.5／diff <font color="blue">1838</font>／1問）<a href="#オイラーの定理による逆元計算" class="tag">オイラーの定理による逆元計算</a>
1. （★2.5／diff <font color="blue">1838</font>／1問）<a href="#合成数を法とする逆元計算" class="tag">合成数を法とする逆元計算</a>
1. （★2.5／diff <font color="blue">1851</font>／1問）<a href="#区間代入更新" class="tag">区間代入更新</a>
1. （★2.5／diff <font color="blue">1854</font>／22問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)）<a href="#損をしない変形" class="tag">損をしない変形</a>
1. （★2.5／diff <font color="blue">1864</font>／29問）<a href="#二分探索" class="tag">二分探索</a>
1. （★2.5／diff <font color="blue">1868</font>／34問）<a href="#冪乗計算" class="tag">冪乗計算</a>
1. （★2.5／diff <font color="blue">1887</font>／7問）<a href="#階差数列" class="tag">階差数列</a>
1. （★2.5／diff <font color="blue">1887</font>／2問）<a href="#素数列による試し割り法" class="tag">素数列による試し割り法</a>
1. （★2.5／diff <font color="blue">1890</font>／4問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を始切片の数え上げに帰着)）<a href="#指定序数の値の計算を始切片の数え上げに帰着" class="tag">指定序数の値の計算を始切片の数え上げに帰着</a>
1. （★2.5／diff <font color="blue">1891</font>／8問）<a href="#フェルマーの小定理" class="tag">フェルマーの小定理</a>
1. （★2.5／diff <font color="blue">1891</font>／2問）<a href="#区間を切片の差に翻訳" class="tag">区間を切片の差に翻訳</a>
1. （★2.5／diff <font color="blue">1896</font>／27問）<a href="#繰り返し二乗法" class="tag">繰り返し二乗法</a>
1. （★2.5／diff <font color="blue">1902</font>／10問）<a href="#周期に注目" class="tag">周期に注目</a>
1. （★2.5／diff <font color="blue">1934</font>／1問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)）<a href="#最終手番の任意性" class="tag">最終手番の任意性</a>
1. （★2.5／diff <font color="blue">1937</font>／17問）<a href="#集合管理" class="tag">集合管理</a>
1. （★2.5／diff <font color="blue">1940</font>／4問）<a href="#ニム和" class="tag">ニム和</a>
1. （★2.5／diff <font color="blue">1983</font>／2問）<a href="#場合分けによるmin・max計算" class="tag">場合分けによるmin・max計算</a>
1. （★2.5／diff <font color="blue">1989</font>／1問）<a href="#多点BFS" class="tag">多点BFS</a>／多始点BFS
1. （★2.5／diff <font color="blue">1996</font>／1問）<a href="#minimax法" class="tag">minimax法</a>
1. （★2.5／diff <font color="yellowgreen">2044</font>／2問）<a href="#クラスカル法" class="tag">クラスカル法</a>／Kruskal法
1. （★2.5／diff <font color="yellowgreen">2121</font>／1問）<a href="#一要素追加" class="tag">一要素追加</a>
1. （★2.5／diff <font color="yellowgreen">2123</font>／1問）<a href="#オイラーグラフ判定" class="tag">オイラーグラフ判定</a>
1. （★2.5／diff <font color="yellowgreen">2123</font>／2問）<a href="#上限・下限値に言及する質問" class="tag">上限・下限値に言及する質問</a>
1. （★2.5／diff <font color="yellowgreen">2219</font>／1問）<a href="#定数倍メモリ削減" class="tag">定数倍メモリ削減</a>
1. （★2.5／diff <font color="yellowgreen">2323</font>／1問）<a href="#階乗進法" class="tag">階乗進法</a>
1. （★2.5／diff <font color="yellowgreen">2353</font>／1問）<a href="#個数上限１複数ナップサック最適化" class="tag">個数上限１複数ナップサック最適化</a>
1. （★2.5／diff <font color="yellowgreen">2353</font>／1問）<a href="#複数ナップサック最適化" class="tag">複数ナップサック最適化</a>
1. （★2.5／diff <font color="orange">2421</font>／1問）<a href="#三分探索" class="tag">三分探索</a>
1. （★2.5／diff <font color="orange">2491</font>／1問）<a href="#必勝戦略のリアクティブ化" class="tag">必勝戦略のリアクティブ化</a>
1. （★2.5／diff <font color="orange">2501</font>／1問）<a href="#全順序集合を状態に持つゲームをP状態とN状態の区間に分割" class="tag">全順序集合を状態に持つゲームをP状態とN状態の区間に分割</a>
1. （★2.6／diff <font color="blue">1738</font>／5問）<a href="#検索" class="tag">検索</a>
1. （★2.6／diff <font color="blue">1757</font>／4問）<a href="#終点からの経路計算" class="tag">終点からの経路計算</a>
1. （★2.6／diff <font color="blue">1765</font>／7問）<a href="#クエリ先読み" class="tag">クエリ先読み</a>
1. （★2.6／diff <font color="blue">1778</font>／12問）<a href="#差分計算" class="tag">差分計算</a>
1. （★2.6／diff <font color="blue">1821</font>／7問）<a href="#ミラー戦略" class="tag">ミラー戦略</a>
1. （★2.6／diff <font color="blue">1845</font>／18問）<a href="#素因数分解" class="tag">素因数分解</a>
1. （★2.6／diff <font color="blue">1866</font>／21問）<a href="#素数を法とする逆元計算" class="tag">素数を法とする逆元計算</a>
1. （★2.6／diff <font color="blue">1903</font>／10問）<a href="#端から確定" class="tag">端から確定</a>
1. （★2.6／diff <font color="blue">1928</font>／5問）<a href="#エラトステネスの篩" class="tag">エラトステネスの篩</a>
1. （★2.6／diff <font color="blue">1933</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)）<a href="#距離空間の重み付きグラフ化" class="tag">距離空間の重み付きグラフ化</a>
1. （★2.6／diff <font color="blue">1942</font>／3問）<a href="#素数を用いた構築" class="tag">素数を用いた構築</a>
1. （★2.6／diff <font color="blue">1944</font>／4問）<a href="#帰属区間取得" class="tag">帰属区間取得</a>
1. （★2.6／diff <font color="blue">1945</font>／8問）<a href="#フェルマーの小定理による逆元計算" class="tag">フェルマーの小定理による逆元計算</a>
1. （★2.6／diff <font color="blue">1968</font>／4問）<a href="#bitDP" class="tag">bitDP</a>
1. （★2.6／diff <font color="yellowgreen">2002</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)）<a href="#不変量を保つ戦略" class="tag">不変量を保つ戦略</a>
1. （★2.6／diff <font color="yellowgreen">2018</font>／3問）<a href="#オイラー関数計算" class="tag">オイラー関数計算</a>
1. （★2.6／diff <font color="yellowgreen">2027</font>／5問）<a href="#最大・最小要素削除" class="tag">最大・最小要素削除</a>
1. （★2.6／diff <font color="yellowgreen">2034</font>／9問）<a href="#一要素挿入" class="tag">一要素挿入</a>
1. （★2.6／diff <font color="yellowgreen">2143</font>／3問）<a href="#変数の対称性" class="tag">変数の対称性</a>
1. （★2.6／diff <font color="yellowgreen">2301</font>／3問）<a href="#ナップサック割り当て数え上げ" class="tag">ナップサック割り当て数え上げ</a>
1. （★2.7／diff <font color="deepskyblue">1346</font>／2問）<a href="#サンプルから推測" class="tag">サンプルから推測</a>
1. （★2.7／diff <font color="blue">1741</font>／7問）<a href="#深さ優先探索" class="tag">深さ優先探索</a>／DFS
1. （★2.7／diff <font color="blue">1789</font>／7問）<a href="#二項係数計算" class="tag">二項係数計算</a>／場合の数計算
1. （★2.7／diff <font color="blue">1838</font>／4問）<a href="#包除原理" class="tag">包除原理</a>
1. （★2.7／diff <font color="blue">1841</font>／8問）<a href="#ダイクストラ法" class="tag">ダイクストラ法</a>／Dijkstra法
1. （★2.7／diff <font color="blue">1918</font>／7問）<a href="#最短経路長計算" class="tag">最短経路長計算</a>
1. （★2.7／diff <font color="blue">1922</font>／7問）<a href="#bitごとに計算" class="tag">bitごとに計算</a>
1. （★2.7／diff <font color="blue">1956</font>／2問）<a href="#倍数ゼータ変換" class="tag">倍数ゼータ変換</a>
1. （★2.7／diff <font color="blue">1988</font>／65問）<a href="#動的計画法" class="tag">動的計画法</a>／DP
1. （★2.7／diff <font color="yellowgreen">2009</font>／2問）<a href="#区間和の指定された区間数え上げ" class="tag">区間和の指定された区間数え上げ</a>
1. （★2.7／diff <font color="yellowgreen">2050</font>／2問）<a href="#再帰的構築" class="tag">再帰的構築</a>
1. （★2.7／diff <font color="yellowgreen">2106</font>／2問）<a href="#左右から走査" class="tag">左右から走査</a>
1. （★2.7／diff <font color="yellowgreen">2107</font>／2問）<a href="#超頂点追加" class="tag">超頂点追加</a>
1. （★2.7／diff <font color="yellowgreen">2109</font>／2問）<a href="#オイラー関数前計算" class="tag">オイラー関数前計算</a>
1. （★2.7／diff <font color="yellowgreen">2126</font>／3問）<a href="#冪等重みの最短経路長計算" class="tag">冪等重みの最短経路長計算</a>
1. （★2.7／diff <font color="yellowgreen">2145</font>／2問）<a href="#転倒数計算" class="tag">転倒数計算</a>
1. （★2.7／diff <font color="yellowgreen">2147</font>／6問）<a href="#優先度付きキュー" class="tag">優先度付きキュー</a>／priority queue
1. （★2.7／diff <font color="yellowgreen">2178</font>／2問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)）<a href="#高さ奇数ニム和" class="tag">高さ奇数ニム和</a>
1. （★2.7／diff <font color="yellowgreen">2232</font>／6問）<a href="#半分全列挙" class="tag">半分全列挙</a>
1. （★2.7／diff <font color="yellowgreen">2379</font>／2問）<a href="#Convex Hull Trick" class="tag">Convex Hull Trick</a>／CHT
1. （★2.7／diff <font color="yellowgreen">2379</font>／2問）<a href="#一次式の族の最大・最小値取得" class="tag">一次式の族の最大・最小値取得</a>
1. （★2.8／diff <font color="blue">1747</font>／7問）<a href="#区間和取得" class="tag">区間和取得</a>
1. （★2.8／diff <font color="blue">1827</font>／6問）<a href="#データを不変量別に分割して管理" class="tag">データを不変量別に分割して管理</a>
1. （★2.8／diff <font color="blue">1866</font>／5問）<a href="#配列を像・頻度表で管理" class="tag">配列を像・頻度表で管理</a>
1. （★2.8／diff <font color="blue">1973</font>／8問）<a href="#最大公約数計算" class="tag">最大公約数計算</a>
1. （★2.8／diff <font color="blue">1975</font>／6問）<a href="#最大・最小要素取得" class="tag">最大・最小要素取得</a>
1. （★2.8／diff <font color="blue">1990</font>／4問）<a href="#イベントソート" class="tag">イベントソート</a>
1. （★2.8／diff <font color="blue">1992</font>／8問）<a href="#imos法" class="tag">imos法</a>
1. （★2.8／diff <font color="yellowgreen">2040</font>／4問）<a href="#sorted set" class="tag">sorted set</a>
1. （★2.8／diff <font color="yellowgreen">2045</font>／9問）<a href="#平面走査" class="tag">平面走査</a>
1. （★2.8／diff <font color="yellowgreen">2058</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)）<a href="#押し付け戦略" class="tag">押し付け戦略</a>
1. （★2.8／diff <font color="yellowgreen">2069</font>／3問）<a href="#区間kth取得" class="tag">区間kth取得</a>
1. （★2.8／diff <font color="yellowgreen">2081</font>／8問）<a href="#付値管理" class="tag">付値管理</a>
1. （★2.8／diff <font color="yellowgreen">2101</font>／12問）<a href="#フェニック木" class="tag">フェニック木</a>／BIT
1. （★2.8／diff <font color="yellowgreen">2149</font>／3問）<a href="#２種の数値を引き算して１種に帰着" class="tag">２種の数値を引き算して１種に帰着</a>
1. （★2.8／diff <font color="yellowgreen">2189</font>／6問）<a href="#既存のアルゴリズムの変形" class="tag">既存のアルゴリズムの変形</a>
1. （★2.8／diff <font color="yellowgreen">2208</font>／4問）<a href="#区間要素数取得" class="tag">区間要素数取得</a>
1. （★2.8／diff <font color="yellowgreen">2217</font>／3問）<a href="#$45$度回転" class="tag">$45$度回転</a>
1. （★2.8／diff <font color="yellowgreen">2234</font>／6問）<a href="#木DP" class="tag">木DP</a>
1. （★2.9／diff <font color="yellowgreen">2041</font>／7問）<a href="#区間加算更新" class="tag">区間加算更新</a>
1. （★2.9／diff <font color="yellowgreen">2107</font>／8問）<a href="#約数の走査を倍数の走査に帰着" class="tag">約数の走査を倍数の走査に帰着</a>
1. （★2.9／diff <font color="yellowgreen">2193</font>／12問）<a href="#再帰" class="tag">再帰</a>
1. （★2.9／diff <font color="yellowgreen">2258</font>／8問）<a href="#座標圧縮" class="tag">座標圧縮</a>／座圧
1. （★3／diff <font color="blue">1725</font>／2問）<a href="#閉路と残りに分割" class="tag">閉路と残りに分割</a>
1. （★3／diff <font color="blue">1725</font>／2問）<a href="#閉路検出" class="tag">閉路検出</a>
1. （★3／diff <font color="blue">1872</font>／2問）<a href="#クエリソート" class="tag">クエリソート</a>
1. （★3／diff <font color="blue">1919</font>／1問）<a href="#偏角ソート" class="tag">偏角ソート</a>
1. （★3／diff <font color="blue">1927</font>／1問）<a href="#mex取得" class="tag">mex取得</a>
1. （★3／diff <font color="blue">1959</font>／1問）<a href="#スライド最小化" class="tag">スライド最小化</a>
1. （★3／diff <font color="blue">1961</font>／1問）<a href="#正弦定理" class="tag">正弦定理</a>
1. （★3／diff <font color="blue">1985</font>／3問）<a href="#inplace DP" class="tag">inplace DP</a>
1. （★3／diff <font color="blue">1985</font>／1問）<a href="#区間スケジューリング" class="tag">区間スケジューリング</a>
1. （★3／diff <font color="blue">1998</font>／1問）<a href="#２次元累積和" class="tag">２次元累積和</a>
1. （★3／diff <font color="blue">1998</font>／1問）<a href="#矩形和取得" class="tag">矩形和取得</a>
1. （★3／diff <font color="yellowgreen">2042</font>／6問）<a href="#小さいケースの構築を拡張" class="tag">小さいケースの構築を拡張</a>
1. （★3／diff <font color="yellowgreen">2047</font>／1問）<a href="#平方剰余" class="tag">平方剰余</a>
1. （★3／diff <font color="yellowgreen">2048</font>／1問）<a href="#最小費用流計算" class="tag">最小費用流計算</a>
1. （★3／diff <font color="yellowgreen">2051</font>／3問）<a href="#ループ戦略" class="tag">ループ戦略</a>
1. （★3／diff <font color="yellowgreen">2056</font>／1問）<a href="#レベル祖先計算" class="tag">レベル祖先計算</a>
1. （★3／diff <font color="yellowgreen">2056</font>／1問）<a href="#弾性衝突を通過に翻訳して位置関係から復元" class="tag">弾性衝突を通過に翻訳して位置関係から復元</a>
1. （★3／diff <font color="yellowgreen">2056</font>／1問）<a href="#木の頂点の重さ計算" class="tag">木の頂点の重さ計算</a>
1. （★3／diff <font color="yellowgreen">2064</font>／2問）<a href="#区間最大・最小値取得" class="tag">区間最大・最小値取得</a>
1. （★3／diff <font color="yellowgreen">2068</font>／1問）<a href="#経路復元" class="tag">経路復元</a>
1. （★3／diff <font color="yellowgreen">2068</font>／1問）<a href="#始点と終点からの経路計算" class="tag">始点と終点からの経路計算</a>
1. （★3／diff <font color="yellowgreen">2074</font>／4問）<a href="#行列累乗" class="tag">行列累乗</a>
1. （★3／diff <font color="yellowgreen">2097</font>／2問）<a href="#区間の分割の数え上げを切片の分割に帰着" class="tag">区間の分割の数え上げを切片の分割に帰着</a>
1. （★3／diff <font color="yellowgreen">2105</font>／3問）<a href="#ダブリング" class="tag">ダブリング</a>
1. （★3／diff <font color="yellowgreen">2119</font>／4問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)）<a href="#総和計算の期待値への帰着" class="tag">総和計算の期待値への帰着</a>
1. （★3／diff <font color="yellowgreen">2129</font>／2問）<a href="#最適遷移の写像化" class="tag">最適遷移の写像化</a>
1. （★3／diff <font color="yellowgreen">2141</font>／2問）<a href="#２次元imos法" class="tag">２次元imos法</a>
1. （★3／diff <font color="yellowgreen">2141</font>／2問）<a href="#矩形加算更新" class="tag">矩形加算更新</a>
1. （★3／diff <font color="yellowgreen">2143</font>／9問）<a href="#ユークリッドの互除法" class="tag">ユークリッドの互除法</a>
1. （★3／diff <font color="yellowgreen">2143</font>／1問）<a href="#ファンデルモンドの畳み込み" class="tag">ファンデルモンドの畳み込み</a>／ヴァンデルモンドの畳み込み
1. （★3／diff <font color="yellowgreen">2147</font>／1問）<a href="#外積" class="tag">外積</a>
1. （★3／diff <font color="yellowgreen">2155</font>／2問）<a href="#区間の重複度計算" class="tag">区間の重複度計算</a>
1. （★3／diff <font color="yellowgreen">2169</font>／1問）<a href="#グリッド上の価値最大化" class="tag">グリッド上の価値最大化</a>
1. （★3／diff <font color="yellowgreen">2183</font>／1問）<a href="#コーシー・フロベニウスの補題" class="tag">コーシー・フロベニウスの補題</a>／バーンサイドの補題
1. （★3／diff <font color="yellowgreen">2183</font>／1問）<a href="#二面体群" class="tag">二面体群</a>
1. （★3／diff <font color="yellowgreen">2191</font>／1問）<a href="#反射の倍化実装" class="tag">反射の倍化実装</a>
1. （★3／diff <font color="yellowgreen">2201</font>／6問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)）<a href="#解法場合分け" class="tag">解法場合分け</a>
1. （★3／diff <font color="yellowgreen">2234</font>／2問）<a href="#フロー" class="tag">フロー</a>
1. （★3／diff <font color="yellowgreen">2237</font>／1問）<a href="#データ構造初期化" class="tag">データ構造初期化</a>
1. （★3／diff <font color="yellowgreen">2237</font>／1問）<a href="#一対一対応と乱択の可換性" class="tag">一対一対応と乱択の可換性</a>
1. （★3／diff <font color="yellowgreen">2245</font>／1問）<a href="#bitset高速化" class="tag">bitset高速化</a>
1. （★3／diff <font color="yellowgreen">2245</font>／1問）<a href="#基底計算" class="tag">基底計算</a>
1. （★3／diff <font color="yellowgreen">2249</font>／4問）<a href="#無向木の有向化" class="tag">無向木の有向化</a>
1. （★3／diff <font color="yellowgreen">2258</font>／1問）<a href="#内積の畳み込み計算" class="tag">内積の畳み込み計算</a>
1. （★3／diff <font color="yellowgreen">2269</font>／2問）<a href="#floor_sum" class="tag">floor_sum</a>
1. （★3／diff <font color="yellowgreen">2284</font>／1問）<a href="#行列式と面積・体積の関係" class="tag">行列式と面積・体積の関係</a>
1. （★3／diff <font color="yellowgreen">2309</font>／1問）<a href="#ベルトラン・チェビシェフの定理" class="tag">ベルトラン・チェビシェフの定理</a>／ベルトランの公準／ベルトランの仮説
1. （★3／diff <font color="yellowgreen">2309</font>／1問）<a href="#素数に注目する質問" class="tag">素数に注目する質問</a>
1. （★3／diff <font color="yellowgreen">2309</font>／1問）<a href="#対角線に言及する質問" class="tag">対角線に言及する質問</a>
1. （★3／diff <font color="yellowgreen">2344</font>／1問）<a href="#bit全探索" class="tag">bit全探索</a>
1. （★3／diff <font color="yellowgreen">2344</font>／1問）<a href="#余因子展開" class="tag">余因子展開</a>
1. （★3／diff <font color="yellowgreen">2385</font>／6問）<a href="#一対一対応" class="tag">一対一対応</a>
1. （★3／diff <font color="yellowgreen">2386</font>／1問）<a href="#SIMD高速化" class="tag">SIMD高速化</a>
1. （★3／diff <font color="yellowgreen">2386</font>／1問）<a href="#平均の指定された区間数え上げ" class="tag">平均の指定された区間数え上げ</a>
1. （★3／diff <font color="yellowgreen">2393</font>／1問）<a href="#剰余を商に翻訳" class="tag">剰余を商に翻訳</a>
1. （★3／diff <font color="yellowgreen">2394</font>／7問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)）<a href="#緩和" class="tag">緩和</a>
1. （★3／diff <font color="orange">2419</font>／1問）<a href="#外接円計算" class="tag">外接円計算</a>
1. （★3／diff <font color="orange">2419</font>／1問）<a href="#第二余弦定理" class="tag">第二余弦定理</a>
1. （★3／diff <font color="orange">2419</font>／1問）<a href="#有理数の大小比較のオーバーフロー回避" class="tag">有理数の大小比較のオーバーフロー回避</a>
1. （★3／diff <font color="orange">2419</font>／1問）<a href="#連分数展開" class="tag">連分数展開</a>
1. （★3／diff <font color="orange">2420</font>／1問）<a href="#完全二部マッチング" class="tag">完全二部マッチング</a>
1. （★3／diff <font color="orange">2429</font>／1問）<a href="#十分大きな法" class="tag">十分大きな法</a>
1. （★3／diff <font color="orange">2454</font>／4問）<a href="#ローリングハッシュ" class="tag">ローリングハッシュ</a>
1. （★3／diff <font color="orange">2471</font>／1問）<a href="#単調関数の像計算を階差の非零点の数え上げに帰着" class="tag">単調関数の像計算を階差の非零点の数え上げに帰着</a>
1. （★3／diff <font color="orange">2489</font>／1問）<a href="#区間削除更新" class="tag">区間削除更新</a>
1. （★3／diff <font color="orange">2489</font>／1問）<a href="#区間挿入更新" class="tag">区間挿入更新</a>
1. （★3／diff <font color="orange">2501</font>／1問）<a href="#自己写像に翻訳" class="tag">自己写像に翻訳</a>
1. （★3／diff <font color="orange">2521</font>／1問）<a href="#bit高速化" class="tag">bit高速化</a>
1. （★3／diff <font color="orange">2604</font>／2問）<a href="#セグメント木" class="tag">セグメント木</a>／セグ木
1. （★3／diff <font color="orange">2604</font>／2問）<a href="#区間の部分列をわたる総和計算をモノイド演算に翻訳" class="tag">区間の部分列をわたる総和計算をモノイド演算に翻訳</a>
1. （★3／diff <font color="orange">2656</font>／3問）<a href="#準同型" class="tag">準同型</a>
1. （★3／diff <font color="red">2833</font>／1問）<a href="#最小被覆半径計算" class="tag">最小被覆半径計算</a>
1. （★3／diffデータなし／1問）<a href="#タイリングによるミラー戦略" class="tag">タイリングによるミラー戦略</a>
1. （★3／diffデータなし／1問）<a href="#数え上げを総和計算に帰着" class="tag">数え上げを総和計算に帰着</a>
1. （★3／diffデータなし／1問）<a href="#辺を頂点とするグラフに翻訳" class="tag">辺を頂点とするグラフに翻訳</a>
1. （★3.1／diff <font color="yellowgreen">2131</font>／11問）<a href="#B進法" class="tag">B進法</a>
1. （★3.1／diff <font color="yellowgreen">2166</font>／5問）<a href="#制約からグラフの種類を特定" class="tag">制約からグラフの種類を特定</a>
1. （★3.1／diff <font color="yellowgreen">2171</font>／4問）<a href="#始切片の数え上げを桁ごとの計算に帰着" class="tag">始切片の数え上げを桁ごとの計算に帰着</a>
1. （★3.1／diff <font color="yellowgreen">2186</font>／9問）<a href="#DPのデータ構造高速化" class="tag">DPのデータ構造高速化</a>
1. （★3.1／diff <font color="yellowgreen">2186</font>／3問）<a href="#確率漸化式" class="tag">確率漸化式</a>
1. （★3.1／diff <font color="yellowgreen">2234</font>／6問）<a href="#期待値の線形性" class="tag">期待値の線形性</a>
1. （★3.1／diff <font color="yellowgreen">2287</font>／3問）<a href="#周期的構築" class="tag">周期的構築</a>
1. （★3.1／diff <font color="yellowgreen">2313</font>／3問）<a href="#平方分割" class="tag">平方分割</a>
1. （★3.1／diff <font color="yellowgreen">2375</font>／3問）<a href="#互いに素に帰着" class="tag">互いに素に帰着</a>
1. （★3.1／diff <font color="orange">2431</font>／4問）<a href="#ゼータ変換" class="tag">ゼータ変換</a>
1. （★3.1／diff <font color="orange">2431</font>／4問）<a href="#メビウス変換" class="tag">メビウス変換</a>
1. （★3.1／diff <font color="orange">2534</font>／3問）<a href="#最長共通接頭辞計算" class="tag">最長共通接頭辞計算</a>／Z-algorithm／LCP
1. （★3.2／diff <font color="yellowgreen">2307</font>／6問）<a href="#積和の和積化" class="tag">積和の和積化</a>
1. （★3.2／diff <font color="yellowgreen">2358</font>／2問）<a href="#フロベニウス数に注目" class="tag">フロベニウス数に注目</a>
1. （★3.2／diff <font color="yellowgreen">2383</font>／4問）<a href="#調和数列" class="tag">調和数列</a>
1. （★3.2／diff <font color="orange">2447</font>／2問）<a href="#ベン図" class="tag">ベン図</a>
1. （★3.2／diff <font color="orange">2493</font>／2問）<a href="#階数計算" class="tag">階数計算</a>
1. （★3.2／diff <font color="orange">2493</font>／2問）<a href="#行列の簡約階段化" class="tag">行列の簡約階段化</a>
1. （★3.2／diff <font color="orange">2641</font>／3問）<a href="#全方位木DP" class="tag">全方位木DP</a>
1. （★3.2／diff <font color="red">2860</font>／3問）<a href="#既出を検索" class="tag">既出を検索</a>
1. （★3.3／diff <font color="yellowgreen">2290</font>／3問）<a href="#十分大きな法で計算" class="tag">十分大きな法で計算</a>
1. （★3.3／diff <font color="yellowgreen">2308</font>／6問）<a href="#２進法" class="tag">２進法</a>
1. （★3.3／diff <font color="yellowgreen">2347</font>／3問）<a href="#剰余による確率的判定" class="tag">剰余による確率的判定</a>
1. （★3.3／diff <font color="orange">2631</font>／4問）<a href="#マージ" class="tag">マージ</a>
1. （★3.3／diff <font color="orange">2631</font>／3問）<a href="#区間を中間で分割してマージ" class="tag">区間を中間で分割してマージ</a>
1. （★3.3／diff <font color="orange">2686</font>／3問）<a href="#多倍長整数" class="tag">多倍長整数</a>
1. （★3.3／diff <font color="orange">2706</font>／3問）<a href="#約数メビウス変換" class="tag">約数メビウス変換</a>
1. （★3.4／diff <font color="orange">2549</font>／6問）<a href="#同値関係" class="tag">同値関係</a>
1. （★3.5／diff <font color="yellowgreen">2348</font>／1問）<a href="#シュトルツ・チェザロの定理" class="tag">シュトルツ・チェザロの定理</a>
1. （★3.5／diff <font color="yellowgreen">2348</font>／1問）<a href="#移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着" class="tag">移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着</a>
1. （★3.5／diff <font color="yellowgreen">2348</font>／1問）<a href="#整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着" class="tag">整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着</a>
1. （★3.5／diff <font color="yellowgreen">2381</font>／1問）<a href="#Moのアルゴリズム" class="tag">Moのアルゴリズム</a>
1. （★3.5／diff <font color="orange">2400</font>／9問）<a href="#線形代数" class="tag">線形代数</a>
1. （★3.5／diff <font color="orange">2401</font>／1問）<a href="#テイラー展開" class="tag">テイラー展開</a>
1. （★3.5／diff <font color="orange">2401</font>／1問）<a href="#フビニの定理" class="tag">フビニの定理</a>
1. （★3.5／diff <font color="orange">2401</font>／1問）<a href="#積分漸化式" class="tag">積分漸化式</a>
1. （★3.5／diff <font color="orange">2421</font>／2問）<a href="#ポラードの$\rho$" class="tag">ポラードの$\rho$</a>
1. （★3.5／diff <font color="orange">2423</font>／4問）<a href="#期待値漸化式" class="tag">期待値漸化式</a>
1. （★3.5／diff <font color="orange">2436</font>／2問）<a href="#osa_k法" class="tag">osa_k法</a>
1. （★3.5／diff <font color="orange">2500</font>／1問）<a href="#交代和" class="tag">交代和</a>
1. （★3.5／diff <font color="orange">2550</font>／2問）<a href="#メビウスの反転公式" class="tag">メビウスの反転公式</a>
1. （★3.5／diff <font color="orange">2587</font>／1問）<a href="#冪乗との最大公約数の収束" class="tag">冪乗との最大公約数の収束</a>
1. （★3.5／diff <font color="orange">2643</font>／1問）<a href="#第二種スターリング数計算" class="tag">第二種スターリング数計算</a>
1. （★3.5／diff <font color="orange">2649</font>／1問）<a href="#カタラン数計算" class="tag">カタラン数計算</a>
1. （★3.5／diff <font color="orange">2690</font>／1問）<a href="#01BFS" class="tag">01BFS</a>
1. （★3.5／diff <font color="orange">2741</font>／1問）<a href="#階数因数分解" class="tag">階数因数分解</a>
1. （★3.5／diff <font color="red">2860</font>／1問）<a href="#タイリング可能性を領域の細分による不変量計算に帰着" class="tag">タイリング可能性を領域の細分による不変量計算に帰着</a>
1. （★3.5／diff <font color="red">2906</font>／2問）<a href="#約数ゼータ変換" class="tag">約数ゼータ変換</a>
1. （★3.5／diff <font color="red">2960</font>／1問）<a href="#cyclic orderつき全方位木DP" class="tag">cyclic orderつき全方位木DP</a>
1. （★3.6／diff <font color="orange">2474</font>／3問）<a href="#行列式計算" class="tag">行列式計算</a>
1. （★3.6／diff <font color="orange">2762</font>／7問）<a href="#桁DP" class="tag">桁DP</a>
1. （★3.7／diff <font color="yellowgreen">2383</font>／2問）<a href="#有向辺反転" class="tag">有向辺反転</a>
1. （★3.7／diff <font color="orange">2719</font>／2問）<a href="#最近共通祖先計算" class="tag">最近共通祖先計算</a>／LCA
1. （★3.8／diff <font color="yellowgreen">2095</font>／3問）<a href="#ヤング図形" class="tag">ヤング図形</a>
1. （★3.8／diff <font color="orange">2737</font>／3問）<a href="#剰余の定理" class="tag">剰余の定理</a>／因数定理
1. （★3.8／diff <font color="red">2829</font>／3問）<a href="#行列の階段化" class="tag">行列の階段化</a>
1. （★3.8／diff <font color="red">2829</font>／3問）<a href="#掃き出し法" class="tag">掃き出し法</a>
1. （★4／diff <font color="orange">2658</font>／1問）<a href="#キュー" class="tag">キュー</a>／queue
1. （★4／diff <font color="orange">2768</font>／1問）<a href="#リュカの定理" class="tag">リュカの定理</a>
1. （★4／diff <font color="orange">2768</font>／1問）<a href="#小さい法に帰着させる再帰" class="tag">小さい法に帰着させる再帰</a>
1. （★4／diff <font color="orange">2795</font>／1問）<a href="#高速ゼータ変換" class="tag">高速ゼータ変換</a>
1. （★4／diff <font color="red">2903</font>／1問）<a href="#区間最大・最小値更新" class="tag">区間最大・最小値更新</a>
1. （★4.1／diff <font color="red">2872</font>／3問）<a href="#バケット分割" class="tag">バケット分割</a>
1. （★4.2／diff <font color="red">2976</font>／9問）<a href="#高速フーリエ変換" class="tag">高速フーリエ変換</a>／数論的変換／FTT／NTT
1. （★4.2／diff <font color="red">2976</font>／9問）<a href="#畳み込み" class="tag">畳み込み</a>
1. （★4.2／diff <font color="red">3142</font>／2問）<a href="#遅延セグメント木" class="tag">遅延セグメント木</a>／遅延セグ木
1. （★4.3／diff <font color="red">3090</font>／4問）<a href="#データ構造をマージする一般的なテク" class="tag">データ構造をマージする一般的なテク</a>／マージテク
1. （★4.3／diff <font color="red">3090</font>／4問）<a href="#演算の反復の分割統治" class="tag">演算の反復の分割統治</a>
1. （★4.5／diff <font color="red">3103</font>／1問）<a href="#ファウルハーバーの公式" class="tag">ファウルハーバーの公式</a>
1. （★4.5／diff <font color="darkgoldenrod ">3316</font>／1問）<a href="#parallel tree contraction" class="tag">parallel tree contraction</a>／rake and compress
1. （★4.5／diff <font color="darkgoldenrod ">3316</font>／1問）<a href="#演算の適用を１次式の合成に翻訳" class="tag">演算の適用を１次式の合成に翻訳</a>
1. （★4.5／diff <font color="darkgoldenrod ">3316</font>／2問）<a href="#構文解析" class="tag">構文解析</a>
1. （★4.5／diff <font color="darkgoldenrod ">3349</font>／2問）<a href="#重軽分解" class="tag">重軽分解</a>／HL分解／HLD
1. （★4.5／diff <font color="darkgoldenrod ">3382</font>／1問）<a href="#区間二次形式取得" class="tag">区間二次形式取得</a>
1. （★4.5／diff <font color="darkgoldenrod ">3382</font>／1問）<a href="#区間二次式取得" class="tag">区間二次式取得</a>
1. （★4.7／diff <font color="darkgoldenrod ">3209</font>／2問）<a href="#Polynomial Taylor shift" class="tag">Polynomial Taylor shift</a>
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#Lindstrom-Gessel-Viennotの補題" class="tag">Lindstrom-Gessel-Viennotの補題</a>／LGV公式
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#ファンデルモンドの行列式計算" class="tag">ファンデルモンドの行列式計算</a>／ヴァンデルモンドの行列式計算
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#差積計算" class="tag">差積計算</a>
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#半標準ヤングタブロー" class="tag">半標準ヤングタブロー</a>
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#半標準ヤングタブローとGelfand-Tsetlinパターンの対応" class="tag">半標準ヤングタブローとGelfand-Tsetlinパターンの対応</a>
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#半標準ヤングタブローと非交差経路の対応" class="tag">半標準ヤングタブローと非交差経路の対応</a>
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#微分計算" class="tag">微分計算</a>
1. （★5／diff <font color="red">3086</font>／1問）<a href="#フック長公式" class="tag">フック長公式</a>
1. （★5／diff <font color="red">3086</font>／1問）<a href="#標準ヤングタブロー" class="tag">標準ヤングタブロー</a>
1. （★5／diff <font color="red">3186</font>／2問）<a href="#多点評価" class="tag">多点評価</a>
1. （★5／diff <font color="red">3196</font>／1問）<a href="#Bostan-Mori法" class="tag">Bostan-Mori法</a>
1. （★5／diff <font color="red">3196</font>／1問）<a href="#巡回畳み込み" class="tag">巡回畳み込み</a>
1. （★5／diff <font color="red">3196</font>／1問）<a href="#多項式のユークリッドの互除法" class="tag">多項式のユークリッドの互除法</a>
1. （★5／diff <font color="red">3196</font>／1問）<a href="#多項式を法とする逆元計算" class="tag">多項式を法とする逆元計算</a>
1. （★5／diff <font color="red">3196</font>／1問）<a href="#単位の分解" class="tag">単位の分解</a>
1. （★5／diff <font color="darkgoldenrod ">3316</font>／1問）<a href="#一次分数変換" class="tag">一次分数変換</a>
1. （★5／diff <font color="darkgoldenrod ">3316</font>／1問）<a href="#一次分数変換と対数関数による変数変換の合成" class="tag">一次分数変換と対数関数による変数変換の合成</a>
1. （★5／diff <font color="darkgoldenrod ">3316</font>／1問）<a href="#指数関数による変数変換と一次分数変換の合成" class="tag">指数関数による変数変換と一次分数変換の合成</a>
1. （★5／diff <font color="darkgoldenrod ">3316</font>／1問）<a href="#微分作用素を変数変換で簡易化" class="tag">微分作用素を変数変換で簡易化</a>
1. （★5／diff <font color="darkgoldenrod ">3316</font>／1問）<a href="#部分積分" class="tag">部分積分</a>
1. （★5／diff <font color="darkgoldenrod ">3382</font>／1問）<a href="#トポロジカルソート" class="tag">トポロジカルソート</a>
1. （★5／diff <font color="darkgoldenrod ">3382</font>／1問）<a href="#強連結成分分解" class="tag">強連結成分分解</a>／SCC
1. （★5／diff <font color="darkgoldenrod ">3382</font>／1問）<a href="#残余ネットワーク" class="tag">残余ネットワーク</a>
1. （★5／diff <font color="darkgoldenrod ">3503</font>／1問）<a href="#指定序数の値の計算を桁ごとの計算に帰着" class="tag">指定序数の値の計算を桁ごとの計算に帰着</a>
1. （★5／diff <font color="darkgoldenrod ">3503</font>／1問）<a href="#非負整数をB進法でベクトルに翻訳" class="tag">非負整数をB進法でベクトルに翻訳</a>
1. （★5／diff <font color="darkgoldenrod ">3577</font>／1問）<a href="#P-再帰" class="tag">P-再帰</a>／P-recursive
1. （★5／diff <font color="darkgoldenrod ">3577</font>／1問）<a href="#評価点シフト" class="tag">評価点シフト</a>
1. （★データなし／diffデータなし／1問）<a href="#ハミルトン路構築" class="tag">ハミルトン路構築</a>


　
<h2 id="実装">1. 実装</h2>

### 難易度統計

「実装」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.2／diff <font color="brown">609</font>
- 2024年: ★1／diff <font color="brown">542</font>
- 2023年: ★1.2／diff <font color="brown">597</font>
- 2022年: ★1.3／diff <font color="brown">787</font>

### レベル別問題一覧

「実装」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題、diff <font color="green">862</font>)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題、diff <font color="brown">569</font>)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題、diff <font color="green">938</font>)
- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題、diff <font color="brown">544</font>)
- <a href="https://yukicoder.me/problems/no/2314">No.2314 Backflip</a> (yukicoder contest 390 (2023-05-26) - A問題、diff <font color="gray">340</font>)
- <a href="https://yukicoder.me/problems/no/2350">No.2350 Four Seasons</a> (yukicoder contest 393 (2023-06-16) - A問題、diff <font color="brown">420</font>)
- <a href="https://yukicoder.me/problems/no/2371">No.2371 最大の試練それは起床</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - A問題、diff <font color="gray">313</font>)
- <a href="https://yukicoder.me/problems/no/2399">No.2399 This Is Truly Final Edition</a> (yukicoder contest 400 (2023-08-04) - A問題、diff <font color="gray">280</font>)
- <a href="https://yukicoder.me/problems/no/2407">No.2407 Bouns 2.0</a> (yukicoder contest 401 (2023-08-11) - A問題、diff <font color="gray">132</font>)
- <a href="https://yukicoder.me/problems/no/2414">No.2414 2 KA 3 KA</a> (MMA Contest 016 (2023-08-12) - A問題、diff <font color="gray">188</font>)
- <a href="https://yukicoder.me/problems/no/2460">No.2460 #強調#</a> (yukicoder contest 404 (2023-09-08) - A問題、diff <font color="gray">222</font>)
- <a href="https://yukicoder.me/problems/no/2492">No.2492 Knapsack Problem?</a> (yukicoder contest 407 (2023-10-06) - A問題、diff <font color="brown">422</font>)
- <a href="https://yukicoder.me/problems/no/2515">No.2515 Similar Triangles</a> (yukicoder contest 410 (2023-10-27) - A問題、diff <font color="gray">371</font>)
- <a href="https://yukicoder.me/problems/no/2547">No.2547 Did you enjoy Chofu Festival?</a> (MMA Contest 017 (2023-11-25) - A問題、diff <font color="gray">198</font>)
- <a href="https://yukicoder.me/problems/no/2557">No.2557 緑以下コンテスト</a> (第2回緑以下コンテスト (2023-12-02) - A問題、diff <font color="gray">140</font>)
- <a href="https://yukicoder.me/problems/no/2559">No.2559 眩しい数直線</a> (第2回緑以下コンテスト (2023-12-02) - C問題、diff <font color="gray">306</font>)
- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)
- <a href="https://yukicoder.me/problems/no/2607">No.2607 Add One Digit</a> (yukicoder contest 415 (2024-01-19) - A問題、diff <font color="green">1070</font>)
- <a href="https://yukicoder.me/problems/no/2621">No.2621 Fee Schedule</a> (yukicoder contest 417 (2024-02-09) - A問題、diff <font color="gray">205</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2091">No.2091 Shio Ramen (Easy)</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題、diff <font color="brown">406</font>)
- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題、diff <font color="green">1095</font>)
- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題、diff <font color="green">999</font>)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)
- <a href="https://yukicoder.me/problems/no/2246">No.2246 1333-like Number</a> (yukicoder contest 381 (2023-03-17) - A問題、diff <font color="brown">689</font>)
- <a href="https://yukicoder.me/problems/no/2312">No.2312 Turtleman and Gaming Console</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2315">No.2315 Flying Camera</a> (yukicoder contest 390 (2023-05-26) - B問題、diff <font color="brown">592</font>)
- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)
- <a href="https://yukicoder.me/problems/no/2385">No.2385 Parse Integer with Radix</a> (yukicoder contest 398 (2023-07-21) - A問題、diff <font color="brown">650</font>)
- <a href="https://yukicoder.me/problems/no/2400">No.2400 Product of Gaussian Integer</a> (yukicoder contest 400 (2023-08-04) - B問題、diff <font color="gray">344</font>)
- <a href="https://yukicoder.me/problems/no/2401">No.2401 Dirty Shoes and Stairs</a> (yukicoder contest 400 (2023-08-04) - C問題、diff <font color="brown">603</font>)
- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)
- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)
- <a href="https://yukicoder.me/problems/no/2564">No.2564 衝突予測</a> (第2回緑以下コンテスト (2023-12-02) - H問題、diff <font color="green">905</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題、diff <font color="green">939</font>)
- <a href="https://yukicoder.me/problems/no/2509">No.2509 Beam Shateki</a> (yukicoder contest 409 (2023-10-20) - B問題、diff <font color="blue">1980</font>)

　
<h2 id="カレンダー計算">2. カレンダー計算</h2>

### 難易度統計

「カレンダー計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.2／diff <font color="brown">704</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1／diff <font color="gray">313</font>
- 2022年: ★1.5／diff <font color="green">1095</font>

### レベル別問題一覧

「カレンダー計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2371">No.2371 最大の試練それは起床</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - A問題、diff <font color="gray">313</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題、diff <font color="green">1095</font>)

　
<h2 id="64bit整数">3. 64bit整数</h2>

### 難易度統計

「64bit整数」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.4／diff <font color="green">842</font>
- 2024年: ★1.5／diff <font color="brown">686</font>
- 2023年: ★1.4／diff <font color="green">857</font>
- 2022年: ★1.5／diff <font color="green">841</font>

### レベル別問題一覧

「64bit整数」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題、diff <font color="brown">544</font>)
- <a href="https://yukicoder.me/problems/no/2560">No.2560 A_1 < A_2 < ... < A_N</a> (第2回緑以下コンテスト (2023-12-02) - D問題、diff <font color="brown">540</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)
- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)
- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2306">No.2306 [Cherry 5th Tune C] ウソツキタマシイ</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - B問題、diff <font color="green">812</font>)
- <a href="https://yukicoder.me/problems/no/2385">No.2385 Parse Integer with Radix</a> (yukicoder contest 398 (2023-07-21) - A問題、diff <font color="brown">650</font>)
- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)
- <a href="https://yukicoder.me/problems/no/2417">No.2417 Div Count</a> (MMA Contest 016 (2023-08-12) - D問題、diff <font color="brown">781</font>)
- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)
- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)
- <a href="https://yukicoder.me/problems/no/2562">No.2562 数字探しゲーム（緑以下コンver.）</a> (第2回緑以下コンテスト (2023-12-02) - F問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)
- <a href="https://yukicoder.me/problems/no/2600">No.2600 Avator Height</a> (yukicoder contest 414 (2024-01-12) - B問題、diff <font color="brown">686</font>)

　
<h2 id="数値の文字列受け取り">4. 数値の文字列受け取り</h2>

### 難易度統計

「数値の文字列受け取り」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.4／diff <font color="green">868</font>
- 2024年: ★2／diff <font color="deepskyblue">1582</font>
- 2023年: ★1.1／diff <font color="brown">495</font>
- 2022年: ★1.5／diff <font color="green">969</font>

### レベル別問題一覧

「数値の文字列受け取り」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題、diff <font color="brown">544</font>)
- <a href="https://yukicoder.me/problems/no/2415">No.2415 偶数判定！Nafmoくん</a> (MMA Contest 016 (2023-08-12) - B問題、diff <font color="gray">188</font>)
- <a href="https://yukicoder.me/problems/no/2450">No.2450 99-like Number</a> (yukicoder contest 403 (2023-09-01) - A問題、diff <font color="gray">140</font>)
- <a href="https://yukicoder.me/problems/no/2525">No.2525 Great Move</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - A問題、diff <font color="brown">424</font>)
- <a href="https://yukicoder.me/problems/no/2607">No.2607 Add One Digit</a> (yukicoder contest 415 (2024-01-19) - A問題、diff <font color="green">1070</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題、diff <font color="green">969</font>)
- <a href="https://yukicoder.me/problems/no/2385">No.2385 Parse Integer with Radix</a> (yukicoder contest 398 (2023-07-21) - A問題、diff <font color="brown">650</font>)
- <a href="https://yukicoder.me/problems/no/2508">No.2508 Discriminant</a> (yukicoder contest 409 (2023-10-20) - A問題、diff <font color="green">1027</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

　
<h2 id="特殊な入出力">5. 特殊な入出力</h2>

### 難易度統計

「特殊な入出力」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.4／diff <font color="green">941</font>
- 2024年: ★2.5／diff <font color="blue">1838</font>
- 2023年: ★1.2／diff <font color="brown">723</font>
- 2022年: ★1.2／diff <font color="green">915</font>

### レベル別問題一覧

「特殊な入出力」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題、diff <font color="green">862</font>)
- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題、diff <font color="brown">544</font>)
- <a href="https://yukicoder.me/problems/no/2415">No.2415 偶数判定！Nafmoくん</a> (MMA Contest 016 (2023-08-12) - B問題、diff <font color="gray">188</font>)
- <a href="https://yukicoder.me/problems/no/2450">No.2450 99-like Number</a> (yukicoder contest 403 (2023-09-01) - A問題、diff <font color="gray">140</font>)
- <a href="https://yukicoder.me/problems/no/2525">No.2525 Great Move</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - A問題、diff <font color="brown">424</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題、diff <font color="green">969</font>)
- <a href="https://yukicoder.me/problems/no/2385">No.2385 Parse Integer with Radix</a> (yukicoder contest 398 (2023-07-21) - A問題、diff <font color="brown">650</font>)
- <a href="https://yukicoder.me/problems/no/2508">No.2508 Discriminant</a> (yukicoder contest 409 (2023-10-20) - A問題、diff <font color="green">1027</font>)
- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)
- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

　
<h2 id="複素数">6. 複素数</h2>

### 難易度統計

「複素数」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="gray">344</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="gray">344</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「複素数」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2400">No.2400 Product of Gaussian Integer</a> (yukicoder contest 400 (2023-08-04) - B問題、diff <font color="gray">344</font>)

　
<h2 id="基数の変換">7. 基数の変換</h2>

### 難易度統計

「基数の変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">477</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="brown">477</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「基数の変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2385">No.2385 Parse Integer with Radix</a> (yukicoder contest 398 (2023-07-21) - A問題、diff <font color="brown">650</font>)
- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)

　
<h2 id="相似">8. 相似</h2>

### 難易度統計

「相似」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">588</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★1.5／diff <font color="brown">588</font>

### レベル別問題一覧

「相似」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)

　
<h2 id="setprecision">9. setprecision</h2>

### 難易度統計

「setprecision」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">627</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="brown">627</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「setprecision」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)

　
<h2 id="符号なし64bit整数">10. 符号なし64bit整数</h2>

### 難易度統計

「符号なし64bit整数」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">708</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="brown">708</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「符号なし64bit整数」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2415">No.2415 偶数判定！Nafmoくん</a> (MMA Contest 016 (2023-08-12) - B問題、diff <font color="gray">188</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2420">No.2420 Simple Problem</a> (MMA Contest 016 (2023-08-12) - G問題、diff <font color="deepskyblue">1228</font>)

　
<h2 id="next_permutation">11. next_permutation</h2>

### 難易度統計

「next_permutation」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">775</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="brown">775</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「next_permutation」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)

　
<h2 id="４重以上のループ">12. ４重以上のループ</h2>

### 難易度統計

「４重以上のループ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">775</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="brown">775</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「４重以上のループ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)

　
<h2 id="再帰による多重ループ実装">13. 再帰による多重ループ実装</h2>

### 難易度統計

「再帰による多重ループ実装」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">775</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="brown">775</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「再帰による多重ループ実装」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)

　
<h2 id="試行回数の期待値を各試行の実施確率の和に帰着">14. 試行回数の期待値を各試行の実施確率の和に帰着</h2>

### 難易度統計

「試行回数の期待値を各試行の実施確率の和に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="green">959</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="green">959</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「試行回数の期待値を各試行の実施確率の和に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)

　
<h2 id="等差数列と等比数列の各点積の累積和計算">15. 等差数列と等比数列の各点積の累積和計算</h2>

### 難易度統計

「等差数列と等比数列の各点積の累積和計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="green">959</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="green">959</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「等差数列と等比数列の各点積の累積和計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)

　
<h2 id="場合分けによる絶対値計算">16. 場合分けによる絶対値計算</h2>

### 難易度統計

「場合分けによる絶対値計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="green">1060</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="green">1060</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「場合分けによる絶対値計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)

　
<h2 id="証明をなぞる構築">17. 証明をなぞる構築</h2>

### 難易度統計

「証明をなぞる構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="deepskyblue">1247</font>
- 2024年: ★1.5／diff <font color="deepskyblue">1247</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「証明をなぞる構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2608">No.2608 Divide into two</a> (yukicoder contest 415 (2024-01-19) - B問題、diff <font color="deepskyblue">1247</font>)

　
<h2 id="中国剰余定理">18. 中国剰余定理</h2>

### 難易度統計

「中国剰余定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="deepskyblue">1290</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="deepskyblue">1290</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「中国剰余定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2558">No.2558 中国剰余定理</a> (第2回緑以下コンテスト (2023-12-02) - B問題、diff <font color="gray">306</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)

　
<h2 id="multiset">19. multiset</h2>

### 難易度統計

「multiset」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="deepskyblue">1313</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="deepskyblue">1313</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「multiset」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)

　
<h2 id="決め打ちによる構築">20. 決め打ちによる構築</h2>

### 難易度統計

「決め打ちによる構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="deepskyblue">1356</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="deepskyblue">1356</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「決め打ちによる構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2562">No.2562 数字探しゲーム（緑以下コンver.）</a> (第2回緑以下コンテスト (2023-12-02) - F問題、diff <font color="deepskyblue">1356</font>)

　
<h2 id="getline">21. getline</h2>

### 難易度統計

「getline」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="yellowgreen">2185</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="yellowgreen">2185</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「getline」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

　
<h2 id="１次式の最大・最小値計算">22. １次式の最大・最小値計算</h2>

### 難易度統計

「１次式の最大・最小値計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.6／diff <font color="green">1175</font>
- 2024年: ★2／diff <font color="green">1029</font>
- 2023年: ★1.6／diff <font color="green">1092</font>
- 2022年: ★1.5／diff <font color="deepskyblue">1372</font>

### レベル別問題一覧

「１次式の最大・最小値計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2138">No.2138 Add Bacon</a> (Advent Calendar Contest 2022 (2022-12-01) - A問題、diff <font color="green">1017</font>)
- <a href="https://yukicoder.me/problems/no/2208">No.2208 Linear Function</a> (yukicoder contest 376 (2023-02-10) - A問題、diff <font color="brown">443</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題、diff <font color="blue">1728</font>)
- <a href="https://yukicoder.me/problems/no/2622">No.2622 Dam</a> (yukicoder contest 417 (2024-02-09) - B問題、diff <font color="green">1029</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)

　
<h2 id="組分けの余りに注目">23. 組分けの余りに注目</h2>

### 難易度統計

「組分けの余りに注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.6／diff <font color="deepskyblue">1206</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.7／diff <font color="deepskyblue">1262</font>
- 2022年: ★1.5／diff <font color="green">1095</font>

### レベル別問題一覧

「組分けの余りに注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題、diff <font color="gray">331</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)

　
<h2 id="解の公式">24. 解の公式</h2>

### 難易度統計

「解の公式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.7／diff <font color="deepskyblue">1441</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.7／diff <font color="deepskyblue">1441</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「解の公式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2508">No.2508 Discriminant</a> (yukicoder contest 409 (2023-10-20) - A問題、diff <font color="green">1027</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)

　
<h2 id="set">25. set</h2>

### 難易度統計

「set」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.8／diff <font color="green">1009</font>
- 2024年: ★1／diff <font color="brown">711</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1307</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「set」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)
- <a href="https://yukicoder.me/problems/no/2607">No.2607 Add One Digit</a> (yukicoder contest 415 (2024-01-19) - A問題、diff <font color="green">1070</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題、diff <font color="deepskyblue">1302</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)

　
<h2 id="重複選択可ナップサック最適化">26. 重複選択可ナップサック最適化</h2>

### 難易度統計

「重複選択可ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.8／diff <font color="deepskyblue">1348</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1432</font>
- 2022年: ★1.5／diff <font color="green">1095</font>

### レベル別問題一覧

「重複選択可ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題、diff <font color="gray">331</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題、diff <font color="blue">1774</font>)

　
<h2 id="連想配列">27. 連想配列</h2>

### 難易度統計

「連想配列」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.8／diff <font color="deepskyblue">1453</font>
- 2024年: ★2／diff <font color="deepskyblue">1369</font>
- 2023年: ★2／diff <font color="blue">1664</font>
- 2022年: ★1／diff <font color="brown">566</font>

### レベル別問題一覧

「連想配列」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2153">No.2153 何コーダーが何人？</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - A問題、diff <font color="brown">566</font>)
- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題、diff <font color="green">1093</font>)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2510">No.2510 Six Cube Sum Counting</a> (yukicoder contest 409 (2023-10-20) - C問題、diff <font color="yellowgreen">2219</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="シミュレーション">28. シミュレーション</h2>

### 難易度統計

「シミュレーション」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.9／diff <font color="deepskyblue">1285</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.9／diff <font color="deepskyblue">1285</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「シミュレーション」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題、diff <font color="green">999</font>)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)
- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題、diff <font color="brown">744</font>)
- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)
- <a href="https://yukicoder.me/problems/no/2401">No.2401 Dirty Shoes and Stairs</a> (yukicoder contest 400 (2023-08-04) - C問題、diff <font color="brown">603</font>)
- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)
- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)
- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)
- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題、diff <font color="green">939</font>)
- <a href="https://yukicoder.me/problems/no/2363">No.2363 k-bonacci</a> (単発出題、diffデータなし)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)
- <a href="https://yukicoder.me/problems/no/2431">No.2431 Viral Hotel</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - H問題、diff <font color="orange">2628</font>)
- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

　
<h2 id="最近点計算">29. 最近点計算</h2>

### 難易度統計

「最近点計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="brown">657</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="brown">657</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最近点計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)

　
<h2 id="グランディ数計算">30. グランディ数計算</h2>

### 難易度統計

「グランディ数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="green">912</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="green">912</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「グランディ数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題、diff <font color="green">912</font>)

　
<h2 id="遷移の収束">31. 遷移の収束</h2>

### 難易度統計

「遷移の収束」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="green">939</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="green">939</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「遷移の収束」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題、diff <font color="green">939</font>)

　
<h2 id="ド・モルガンの法則">32. ド・モルガンの法則</h2>

### 難易度統計

「ド・モルガンの法則」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="green">1049</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="green">1049</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ド・モルガンの法則」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)

　
<h2 id="巡回置換表示">33. 巡回置換表示</h2>

### 難易度統計

「巡回置換表示」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="green">1050</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="green">1050</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「巡回置換表示」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題、diff <font color="green">849</font>)
- <a href="https://yukicoder.me/problems/no/2316">No.2316 Freight Train</a> (yukicoder contest 390 (2023-05-26) - C問題、diff <font color="brown">718</font>)
- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)

　
<h2 id="三平方の定理">34. 三平方の定理</h2>

### 難易度統計

「三平方の定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1208</font>
- 2024年: ★2／diff <font color="deepskyblue">1208</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「三平方の定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

　
<h2 id="小数誤差">35. 小数誤差</h2>

### 難易度統計

「小数誤差」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1257</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.2／diff <font color="deepskyblue">1391</font>
- 2022年: ★1.5／diff <font color="brown">588</font>

### レベル別問題一覧

「小数誤差」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)
- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)
- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2352">No.2352 Sharpened Knife in Fall</a> (yukicoder contest 393 (2023-06-16) - C問題、diff <font color="deepskyblue">1560</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2389">No.2389 Cheating Code Golf</a> (yukicoder contest 398 (2023-07-21) - E問題、diff <font color="orange">2451</font>)

　
<h2 id="整礎性">36. 整礎性</h2>

### 難易度統計

「整礎性」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1273</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1273</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「整礎性」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2426">No.2426 Select Plus or Minus</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - C問題、diff <font color="deepskyblue">1273</font>)

　
<h2 id="等差数列の累積和計算">37. 等差数列の累積和計算</h2>

### 難易度統計

「等差数列の累積和計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1344</font>
- 2024年: ★1.5／diff <font color="deepskyblue">1247</font>
- 2023年: ★2.1／diff <font color="deepskyblue">1368</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「等差数列の累積和計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2560">No.2560 A_1 < A_2 < ... < A_N</a> (第2回緑以下コンテスト (2023-12-02) - D問題、diff <font color="brown">540</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2608">No.2608 Divide into two</a> (yukicoder contest 415 (2024-01-19) - B問題、diff <font color="deepskyblue">1247</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2567">No.2567 A_1 > A_2 > ... > A_N</a> (第2回緑以下コンテスト (2023-12-02) - K問題、diff <font color="green">1179</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題、diff <font color="blue">1865</font>)

　
<h2 id="負コストナップサック最適化">38. 負コストナップサック最適化</h2>

### 難易度統計

「負コストナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1352</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1352</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「負コストナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)

　
<h2 id="頻度表">39. 頻度表</h2>

### 難易度統計

「頻度表」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1413</font>
- 2024年: ★2.3／diff <font color="blue">1664</font>
- 2023年: ★2／diff <font color="deepskyblue">1277</font>
- 2022年: ★2／diff <font color="deepskyblue">1390</font>

### レベル別問題一覧

「頻度表」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2153">No.2153 何コーダーが何人？</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - A問題、diff <font color="brown">566</font>)
- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題、diff <font color="gray">342</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題、diff <font color="green">1093</font>)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題、diff <font color="green">1069</font>)
- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題、diff <font color="blue">1802</font>)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2618">No.2618 除霊</a> (yukicoder contest 416 (2024-01-26) - E問題、diff <font color="yellowgreen">2255</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="素因数分解による最小公倍数計算">40. 素因数分解による最小公倍数計算</h2>

### 難易度統計

「素因数分解による最小公倍数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1585</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1585</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素因数分解による最小公倍数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)

　
<h2 id="置換の合成">41. 置換の合成</h2>

### 難易度統計

「置換の合成」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1585</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1585</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「置換の合成」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)

　
<h2 id="ルジャンドルの公式">42. ルジャンドルの公式</h2>

### 難易度統計

「ルジャンドルの公式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="blue">1605</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="blue">1605</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ルジャンドルの公式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題、diff <font color="blue">1605</font>)

　
<h2 id="二項定理">43. 二項定理</h2>

### 難易度統計

「二項定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="blue">1629</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="blue">1629</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「二項定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2550">No.2550 MORE! JUMP! MORE!</a> (MMA Contest 017 (2023-11-25) - D問題、diff <font color="blue">1629</font>)

　
<h2 id="多次元コスト重複選択可ナップサック最適化">44. 多次元コスト重複選択可ナップサック最適化</h2>

### 難易度統計

「多次元コスト重複選択可ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="blue">1644</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2193</font>
- 2022年: ★1.5／diff <font color="green">1095</font>

### レベル別問題一覧

「多次元コスト重複選択可ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)

　
<h2 id="剰余計算を桁の線形和に帰着">45. 剰余計算を桁の線形和に帰着</h2>

### 難易度統計

「剰余計算を桁の線形和に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="yellowgreen">2275</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="yellowgreen">2275</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「剰余計算を桁の線形和に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)

　
<h2 id="ナップサック最適化">46. ナップサック最適化</h2>

### 難易度統計

「ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1322</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.1／diff <font color="deepskyblue">1411</font>
- 2022年: ★1.7／diff <font color="green">969</font>

### レベル別問題一覧

「ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題、diff <font color="gray">331</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題、diff <font color="green">843</font>)
- <a href="https://yukicoder.me/problems/no/2232">No.2232 Miser's Gift</a> (yukicoder contest 379 (2023-03-03) - A問題、diff <font color="deepskyblue">1389</font>)
- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題、diff <font color="green">875</font>)
- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題、diff <font color="blue">1774</font>)
- <a href="https://yukicoder.me/problems/no/2429">No.2429 Happiest Tabehodai Ways</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - F問題、diff <font color="blue">1907</font>)
- <a href="https://yukicoder.me/problems/no/2542">No.2542 Yokan for Two</a> (yukicoder contest 413 (2023-11-24) - B問題、diff <font color="deepskyblue">1469</font>)

　
<h2 id="等比数列の累積和計算">47. 等比数列の累積和計算</h2>

### 難易度統計

「等比数列の累積和計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1358</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.1／diff <font color="deepskyblue">1358</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「等比数列の累積和計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)
- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2393">No.2393 Bit Grid Connected Component</a> (yukicoder contest 399 (2023-07-28) - B問題、diff <font color="green">1050</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)

　
<h2 id="多次元コストナップサック最適化">48. 多次元コストナップサック最適化</h2>

### 難易度統計

「多次元コストナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1387</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1534</font>
- 2022年: ★1.5／diff <font color="green">1095</font>

### レベル別問題一覧

「多次元コストナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題、diff <font color="green">875</font>)

　
<h2 id="場合分け">49. 場合分け</h2>

### 難易度統計

「場合分け」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1494</font>
- 2024年: ★2.1／diff <font color="deepskyblue">1447</font>
- 2023年: ★1.9／diff <font color="deepskyblue">1257</font>
- 2022年: ★2.5／diff <font color="blue">1907</font>

### レベル別問題一覧

「場合分け」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題、diff <font color="green">862</font>)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題、diff <font color="brown">569</font>)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題、diff <font color="green">938</font>)
- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題、diff <font color="brown">544</font>)
- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題、diff <font color="gray">331</font>)
- <a href="https://yukicoder.me/problems/no/2350">No.2350 Four Seasons</a> (yukicoder contest 393 (2023-06-16) - A問題、diff <font color="brown">420</font>)
- <a href="https://yukicoder.me/problems/no/2371">No.2371 最大の試練それは起床</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - A問題、diff <font color="gray">313</font>)
- <a href="https://yukicoder.me/problems/no/2557">No.2557 緑以下コンテスト</a> (第2回緑以下コンテスト (2023-12-02) - A問題、diff <font color="gray">140</font>)
- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題、diff <font color="green">969</font>)
- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)
- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題、diff <font color="brown">769</font>)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)
- <a href="https://yukicoder.me/problems/no/2564">No.2564 衝突予測</a> (第2回緑以下コンテスト (2023-12-02) - H問題、diff <font color="green">905</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題、diff <font color="blue">1728</font>)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2209">No.2209 Flip and Reverse</a> (yukicoder contest 376 (2023-02-10) - B問題、diff <font color="green">1008</font>)
- <a href="https://yukicoder.me/problems/no/2247">No.2247 01 ZigZag</a> (yukicoder contest 381 (2023-03-17) - B問題、diff <font color="blue">1604</font>)
- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)
- <a href="https://yukicoder.me/problems/no/2541">No.2541 Divide 01 String</a> (yukicoder contest 413 (2023-11-24) - A問題、diff <font color="brown">606</font>)
- <a href="https://yukicoder.me/problems/no/2565">No.2565 はじめてのおつかい</a> (第2回緑以下コンテスト (2023-12-02) - I問題、diff <font color="green">972</font>)
- <a href="https://yukicoder.me/problems/no/2622">No.2622 Dam</a> (yukicoder contest 417 (2024-02-09) - B問題、diff <font color="green">1029</font>)
- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題、diff <font color="blue">1641</font>)
- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題、diff <font color="blue">1934</font>)
- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題、diff <font color="yellowgreen">2039</font>)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2569">No.2569 はじめてのおつかいHard</a> (緑以下コンテスト  Extra (2023-12-02) - A問題、diff <font color="deepskyblue">1385</font>)
- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題、diff <font color="yellowgreen">2327</font>)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)
- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2366">No.2366 登校</a> (yukicoder contest 395 (2023-06-30) - C問題、diff <font color="yellowgreen">2294</font>)
- <a href="https://yukicoder.me/problems/no/2519">No.2519 Coins in Array</a> (yukicoder contest 410 (2023-10-27) - E問題、diff <font color="yellowgreen">2069</font>)
- <a href="https://yukicoder.me/problems/no/2553">No.2553 Holidays</a> (MMA Contest 017 (2023-11-25) - G問題、diff <font color="red">2858</font>)
- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2151">No.2151 3 on Torus-Lohkous</a> (Advent Calendar Contest 2022 (2022-12-01) - H問題、diff <font color="darkgoldenrod ">3257</font>)

　
<h2 id="全探索">50. 全探索</h2>

### 難易度統計

「全探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1494</font>
- 2024年: ★2.5／diff <font color="blue">1955</font>
- 2023年: ★2／diff <font color="deepskyblue">1374</font>
- 2022年: ★2.2／diff <font color="blue">1822</font>

### レベル別問題一覧

「全探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2138">No.2138 Add Bacon</a> (Advent Calendar Contest 2022 (2022-12-01) - A問題、diff <font color="green">1017</font>)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題、diff <font color="brown">569</font>)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題、diff <font color="green">938</font>)
- <a href="https://yukicoder.me/problems/no/2208">No.2208 Linear Function</a> (yukicoder contest 376 (2023-02-10) - A問題、diff <font color="brown">443</font>)
- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題、diff <font color="gray">331</font>)
- <a href="https://yukicoder.me/problems/no/2492">No.2492 Knapsack Problem?</a> (yukicoder contest 407 (2023-10-06) - A問題、diff <font color="brown">422</font>)
- <a href="https://yukicoder.me/problems/no/2558">No.2558 中国剰余定理</a> (第2回緑以下コンテスト (2023-12-02) - B問題、diff <font color="gray">306</font>)
- <a href="https://yukicoder.me/problems/no/2559">No.2559 眩しい数直線</a> (第2回緑以下コンテスト (2023-12-02) - C問題、diff <font color="gray">306</font>)
- <a href="https://yukicoder.me/problems/no/2607">No.2607 Add One Digit</a> (yukicoder contest 415 (2024-01-19) - A問題、diff <font color="green">1070</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題、diff <font color="green">969</font>)
- <a href="https://yukicoder.me/problems/no/2091">No.2091 Shio Ramen (Easy)</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題、diff <font color="brown">769</font>)
- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題、diff <font color="green">999</font>)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)
- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題、diff <font color="brown">744</font>)
- <a href="https://yukicoder.me/problems/no/2315">No.2315 Flying Camera</a> (yukicoder contest 390 (2023-05-26) - B問題、diff <font color="brown">592</font>)
- <a href="https://yukicoder.me/problems/no/2493">No.2493 K-th in L2 with L1</a> (yukicoder contest 407 (2023-10-06) - B問題、diff <font color="green">1182</font>)
- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)
- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題、diff <font color="deepskyblue">1529</font>)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)
- <a href="https://yukicoder.me/problems/no/2196">No.2196 Pair Bonus</a> (yukicoder contest 374 (2023-01-20) - C問題、diff <font color="deepskyblue">1314</font>)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題、diff <font color="deepskyblue">1551</font>)
- <a href="https://yukicoder.me/problems/no/2234">No.2234 palindromer</a> (yukicoder contest 379 (2023-03-03) - C問題、diff <font color="green">1000</font>)
- <a href="https://yukicoder.me/problems/no/2247">No.2247 01 ZigZag</a> (yukicoder contest 381 (2023-03-17) - B問題、diff <font color="blue">1604</font>)
- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2363">No.2363 k-bonacci</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2374">No.2374 ASKT Subsequences</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - D問題、diff <font color="deepskyblue">1578</font>)
- <a href="https://yukicoder.me/problems/no/2386">No.2386 Udon Coupon (Easy)</a> (yukicoder contest 398 (2023-07-21) - B問題、diff <font color="green">982</font>)
- <a href="https://yukicoder.me/problems/no/2509">No.2509 Beam Shateki</a> (yukicoder contest 409 (2023-10-20) - B問題、diff <font color="blue">1980</font>)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)
- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)
- <a href="https://yukicoder.me/problems/no/2601">No.2601 Very Poor</a> (yukicoder contest 414 (2024-01-12) - C問題、diff <font color="green">1032</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題、diff <font color="deepskyblue">1331</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2449">No.2449 square_permutation</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2463">No.2463 ストレートフラッシュ</a> (yukicoder contest 404 (2023-09-08) - D問題、diff <font color="blue">1838</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)
- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題、diff <font color="orange">2620</font>)
- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題、diff <font color="orange">2471</font>)
- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2519">No.2519 Coins in Array</a> (yukicoder contest 410 (2023-10-27) - E問題、diff <font color="yellowgreen">2069</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)
- <a href="https://yukicoder.me/problems/no/2555">No.2555 Intriguing Triangle</a> (Advent Calendar Contest 2023 (2023-12-01) - A問題、diff <font color="blue">1961</font>)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)

　
<h2 id="分割の均等化">51. 分割の均等化</h2>

### 難易度統計

「分割の均等化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1533</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.2／diff <font color="blue">1621</font>
- 2022年: ★2／diff <font color="deepskyblue">1356</font>

### レベル別問題一覧

「分割の均等化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2567">No.2567 A_1 > A_2 > ... > A_N</a> (第2回緑以下コンテスト (2023-12-02) - K問題、diff <font color="green">1179</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2501">No.2501 Maximum Inversion Number</a> (yukicoder contest 408 (2023-10-13) - B問題、diff <font color="yellowgreen">2064</font>)

　
<h2 id="操作を数値に翻訳">52. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作を数値に翻訳">操作を数値に翻訳</a></h2>

### 難易度統計

「[操作を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作を数値に翻訳)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1552</font>
- 2024年: ★3／diff <font color="orange">2491</font>
- 2023年: ★2.1／diff <font color="deepskyblue">1443</font>
- 2022年: ★2／diff <font color="blue">1629</font>

### レベル別問題一覧

「[操作を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作を数値に翻訳)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題、diff <font color="gray">331</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題、diff <font color="deepskyblue">1529</font>)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題、diff <font color="deepskyblue">1551</font>)
- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題、diff <font color="green">831</font>)
- <a href="https://yukicoder.me/problems/no/2386">No.2386 Udon Coupon (Easy)</a> (yukicoder contest 398 (2023-07-21) - B問題、diff <font color="green">982</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題、diff <font color="deepskyblue">1331</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題、diff <font color="yellowgreen">2175</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)

　
<h2 id="動的mod">53. 動的mod</h2>

### 難易度統計

「動的mod」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1584</font>
- 2024年: ★3／diff <font color="orange">2536</font>
- 2023年: ★1.8／diff <font color="deepskyblue">1347</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「動的mod」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2558">No.2558 中国剰余定理</a> (第2回緑以下コンテスト (2023-12-02) - B問題、diff <font color="gray">306</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2562">No.2562 数字探しゲーム（緑以下コンver.）</a> (第2回緑以下コンテスト (2023-12-02) - F問題、diff <font color="deepskyblue">1356</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="平方根">54. 平方根</h2>

### 難易度統計

「平方根」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="blue">1674</font>
- 2024年: ★3／diff <font color="orange">2419</font>
- 2023年: ★2／diff <font color="deepskyblue">1525</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「平方根」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2479">No.2479 Sum of Squares</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - A問題、diff <font color="brown">779</font>)
- <a href="https://yukicoder.me/problems/no/2493">No.2493 K-th in L2 with L1</a> (yukicoder contest 407 (2023-10-06) - B問題、diff <font color="green">1182</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題、diff <font color="blue">1768</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

　
<h2 id="素集合データ構造">55. 素集合データ構造</h2>

### 難易度統計

「素集合データ構造」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1335</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.1／diff <font color="deepskyblue">1321</font>
- 2022年: ★2.5／diff <font color="deepskyblue">1486</font>

### レベル別問題一覧

「素集合データ構造」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2418">No.2418 情報通だよ！Nafmoくん</a> (MMA Contest 016 (2023-08-12) - E問題、diff <font color="brown">691</font>)
- <a href="https://yukicoder.me/problems/no/2563">No.2563 色ごとのグループ</a> (第2回緑以下コンテスト (2023-12-02) - G問題、diff <font color="green">851</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題、diff <font color="green">849</font>)
- <a href="https://yukicoder.me/problems/no/2316">No.2316 Freight Train</a> (yukicoder contest 390 (2023-05-26) - C問題、diff <font color="brown">718</font>)
- <a href="https://yukicoder.me/problems/no/2494">No.2494 Sum within Components</a> (yukicoder contest 407 (2023-10-06) - C問題、diff <font color="green">1031</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題、diff <font color="deepskyblue">1486</font>)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題、diff <font color="deepskyblue">1302</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2403">No.2403 "Eight" Bridges of Konigsberg</a> (yukicoder contest 400 (2023-08-04) - E問題、diff <font color="yellowgreen">2123</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="連結成分取得">56. 連結成分取得</h2>

### 難易度統計

「連結成分取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1335</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.1／diff <font color="deepskyblue">1321</font>
- 2022年: ★2.5／diff <font color="deepskyblue">1486</font>

### レベル別問題一覧

「連結成分取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2418">No.2418 情報通だよ！Nafmoくん</a> (MMA Contest 016 (2023-08-12) - E問題、diff <font color="brown">691</font>)
- <a href="https://yukicoder.me/problems/no/2563">No.2563 色ごとのグループ</a> (第2回緑以下コンテスト (2023-12-02) - G問題、diff <font color="green">851</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題、diff <font color="green">849</font>)
- <a href="https://yukicoder.me/problems/no/2316">No.2316 Freight Train</a> (yukicoder contest 390 (2023-05-26) - C問題、diff <font color="brown">718</font>)
- <a href="https://yukicoder.me/problems/no/2494">No.2494 Sum within Components</a> (yukicoder contest 407 (2023-10-06) - C問題、diff <font color="green">1031</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題、diff <font color="deepskyblue">1486</font>)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題、diff <font color="deepskyblue">1302</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2403">No.2403 "Eight" Bridges of Konigsberg</a> (yukicoder contest 400 (2023-08-04) - E問題、diff <font color="yellowgreen">2123</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="サンプルに帰着">57. サンプルに帰着</h2>

### 難易度統計

「サンプルに帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1346</font>
- 2024年: ★1.5／diff <font color="gray">365</font>
- 2023年: ★2.7／diff <font color="blue">1869</font>
- 2022年: ★2／diff <font color="deepskyblue">1313</font>

### レベル別問題一覧

「サンプルに帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)
- <a href="https://yukicoder.me/problems/no/2614">No.2614 Delete ABC</a> (yukicoder contest 416 (2024-01-26) - A問題、diff <font color="gray">365</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題、diff <font color="yellowgreen">2039</font>)
- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題、diff <font color="blue">1768</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題、diff <font color="blue">1971</font>)

　
<h2 id="三角形の成立条件">58. 三角形の成立条件</h2>

### 難易度統計

「三角形の成立条件」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1412</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1961</font>
- 2022年: ★1.5／diff <font color="green">864</font>

### レベル別問題一覧

「三角形の成立条件」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2140">No.2140 Triangle</a> (yukicoder contest 370 (2022-12-02) - A問題、diff <font color="green">864</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2555">No.2555 Intriguing Triangle</a> (Advent Calendar Contest 2023 (2023-12-01) - A問題、diff <font color="blue">1961</font>)

　
<h2 id="幅優先探索">59. 幅優先探索</h2>

### 難易度統計

「幅優先探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1415</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.2／diff <font color="deepskyblue">1404</font>
- 2022年: ★2／diff <font color="deepskyblue">1582</font>

### レベル別問題一覧

「幅優先探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2418">No.2418 情報通だよ！Nafmoくん</a> (MMA Contest 016 (2023-08-12) - E問題、diff <font color="brown">691</font>)
- <a href="https://yukicoder.me/problems/no/2563">No.2563 色ごとのグループ</a> (第2回緑以下コンテスト (2023-12-02) - G問題、diff <font color="green">851</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2064">No.2064 Smallest Sequence on Grid</a> (yukicoder contest 359 (2022-09-02) - B問題、diff <font color="deepskyblue">1582</font>)
- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題、diff <font color="green">849</font>)
- <a href="https://yukicoder.me/problems/no/2316">No.2316 Freight Train</a> (yukicoder contest 390 (2023-05-26) - C問題、diff <font color="brown">718</font>)
- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題、diff <font color="green">1174</font>)
- <a href="https://yukicoder.me/problems/no/2494">No.2494 Sum within Components</a> (yukicoder contest 407 (2023-10-06) - C問題、diff <font color="green">1031</font>)
- <a href="https://yukicoder.me/problems/no/2565">No.2565 はじめてのおつかい</a> (第2回緑以下コンテスト (2023-12-02) - I問題、diff <font color="green">972</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題、diff <font color="blue">1989</font>)
- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2403">No.2403 "Eight" Bridges of Konigsberg</a> (yukicoder contest 400 (2023-08-04) - E問題、diff <font color="yellowgreen">2123</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)

　
<h2 id="三角形の面積計算">60. 三角形の面積計算</h2>

### 難易度統計

「三角形の面積計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1421</font>
- 2024年: ★2／diff <font color="deepskyblue">1208</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1493</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「三角形の面積計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2515">No.2515 Similar Triangles</a> (yukicoder contest 410 (2023-10-27) - A問題、diff <font color="gray">371</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)
- <a href="https://yukicoder.me/problems/no/2555">No.2555 Intriguing Triangle</a> (Advent Calendar Contest 2023 (2023-12-01) - A問題、diff <font color="blue">1961</font>)

　
<h2 id="表示可能性DP">61. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP">表示可能性DP</a></h2>

### 難易度統計

「[表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1496</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1352</font>
- 2022年: ★2.5／diff <font color="blue">1641</font>

### レベル別問題一覧

「[表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題、diff <font color="blue">1641</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)

　
<h2 id="素因数分解による約数の生成式">62. 素因数分解による約数の生成式</h2>

### 難易度統計

「素因数分解による約数の生成式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1517</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.1／diff <font color="deepskyblue">1388</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2291</font>

### レベル別問題一覧

「素因数分解による約数の生成式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2417">No.2417 Div Count</a> (MMA Contest 016 (2023-08-12) - D問題、diff <font color="brown">781</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2480">No.2480 Sequence Sum</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - B問題、diff <font color="deepskyblue">1433</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)

　
<h2 id="約数列挙">63. 約数列挙</h2>

### 難易度統計

「約数列挙」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1517</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.1／diff <font color="deepskyblue">1388</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2291</font>

### レベル別問題一覧

「約数列挙」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2417">No.2417 Div Count</a> (MMA Contest 016 (2023-08-12) - D問題、diff <font color="brown">781</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2480">No.2480 Sequence Sum</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - B問題、diff <font color="deepskyblue">1433</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)

　
<h2 id="貪欲法">64. 貪欲法</h2>

### 難易度統計

「貪欲法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1531</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2235</font>
- 2023年: ★2.1／diff <font color="deepskyblue">1325</font>
- 2022年: ★2／diff <font color="deepskyblue">1483</font>

### レベル別問題一覧

「貪欲法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2424">No.2424 Josouzai</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - A問題、diff <font color="brown">769</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)
- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題、diff <font color="gray">342</font>)
- <a href="https://yukicoder.me/problems/no/2479">No.2479 Sum of Squares</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - A問題、diff <font color="brown">779</font>)
- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2056">No.2056 非力なレッド</a> (yukicoder contest 358 (2022-08-26) - A問題、diff <font color="brown">683</font>)
- <a href="https://yukicoder.me/problems/no/2064">No.2064 Smallest Sequence on Grid</a> (yukicoder contest 359 (2022-09-02) - B問題、diff <font color="deepskyblue">1582</font>)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題、diff <font color="green">849</font>)
- <a href="https://yukicoder.me/problems/no/2307">No.2307 [Cherry 5 th Tune *] Cool 46</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - C問題、diff <font color="deepskyblue">1345</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題、diff <font color="blue">1802</font>)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2422">No.2422 regisys?</a> (MMA Contest 016 (2023-08-12) - I問題、diff <font color="yellowgreen">2353</font>)
- <a href="https://yukicoder.me/problems/no/2449">No.2449 square_permutation</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2501">No.2501 Maximum Inversion Number</a> (yukicoder contest 408 (2023-10-13) - B問題、diff <font color="yellowgreen">2064</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2623">No.2623 Room Allocation</a> (yukicoder contest 417 (2024-02-09) - C問題、diff <font color="deepskyblue">1328</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="ヘルド・カープ法">65. ヘルド・カープ法</h2>

### 難易度統計

「ヘルド・カープ法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1540</font>
- 2024年: ★2.5／diff <font color="blue">1728</font>
- 2023年: ★2／diff <font color="deepskyblue">1352</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ヘルド・カープ法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2955">No.2955 Pizza Delivery Plan</a> (yukicoder contest 452 (2024-11-08) - C問題、diff <font color="blue">1728</font>)

　
<h2 id="操作の纏め上げ">66. 操作の纏め上げ</h2>

### 難易度統計

「操作の纏め上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1572</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.2／diff <font color="deepskyblue">1572</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「操作の纏め上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)
- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2426">No.2426 Select Plus or Minus</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - C問題、diff <font color="deepskyblue">1273</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)

　
<h2 id="多項係数と組み合わせの関係">67. 多項係数と組み合わせの関係</h2>

### 難易度統計

「多項係数と組み合わせの関係」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1586</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2／diffデータなし
- 2022年: ★2／diff <font color="deepskyblue">1308</font>

### レベル別問題一覧

「多項係数と組み合わせの関係」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題、diff <font color="deepskyblue">1261</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2467">No.2467 Sum of Product of Binomial Coefficients</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - A問題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="重複選択個数の線形関係式">68. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#重複選択個数の線形関係式">重複選択個数の線形関係式</a></h2>

### 難易度統計

「[重複選択個数の線形関係式](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#重複選択個数の線形関係式)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1587</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.2／diff <font color="deepskyblue">1587</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[重複選択個数の線形関係式](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#重複選択個数の線形関係式)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2386">No.2386 Udon Coupon (Easy)</a> (yukicoder contest 398 (2023-07-21) - B問題、diff <font color="green">982</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)

　
<h2 id="小数計算の整数への帰着">69. 小数計算の整数への帰着</h2>

### 難易度統計

「小数計算の整数への帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1606</font>
- 2024年: ★2.6／diff <font color="yellowgreen">2031</font>
- 2023年: ★2／diff <font color="deepskyblue">1393</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「小数計算の整数への帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2407">No.2407 Bouns 2.0</a> (yukicoder contest 401 (2023-08-11) - A問題、diff <font color="gray">132</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2493">No.2493 K-th in L2 with L1</a> (yukicoder contest 407 (2023-10-06) - B問題、diff <font color="green">1182</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)
- <a href="https://yukicoder.me/problems/no/2420">No.2420 Simple Problem</a> (MMA Contest 016 (2023-08-12) - G問題、diff <font color="deepskyblue">1228</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

　
<h2 id="連長圧縮">70. 連長圧縮</h2>

### 難易度統計

「連長圧縮」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1716</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="green">813</font>
- 2022年: ★3／diff <font color="orange">2620</font>

### レベル別問題一覧

「連長圧縮」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2298">No.2298 yukicounter</a> (yukicoder contest 388 (2023-05-12) - B問題、diff <font color="green">813</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題、diff <font color="orange">2620</font>)

　
<h2 id="括弧列判定">71. 括弧列判定</h2>

### 難易度統計

「括弧列判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1747</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.2／diff <font color="blue">1747</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「括弧列判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2240">No.2240 WAC</a> (yukicoder contest 380 (2023-03-10) - B問題、diff <font color="deepskyblue">1373</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

　
<h2 id="良いケースに帰着">72. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着">良いケースに帰着</a></h2>

### 難易度統計

「[良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1762</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.2／diff <font color="blue">1762</font>

### レベル別問題一覧

「[良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)

　
<h2 id="ウノ計算">73. ウノ計算</h2>

### 難易度統計

「ウノ計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1345</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2246</font>

### レベル別問題一覧

「ウノ計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2307">No.2307 [Cherry 5 th Tune *] Cool 46</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - C問題、diff <font color="deepskyblue">1345</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題、diff <font color="yellowgreen">2246</font>)

　
<h2 id="不定方程式の因数分解">74. 不定方程式の因数分解</h2>

### 難易度統計

「不定方程式の因数分解」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1844</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1397</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2291</font>

### レベル別問題一覧

「不定方程式の因数分解」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)

　
<h2 id="ナップサックDP">75. ナップサックDP</h2>

### 難易度統計

「ナップサックDP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="deepskyblue">1296</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.3／diff <font color="deepskyblue">1410</font>
- 2022年: ★2／diff <font color="green">843</font>

### レベル別問題一覧

「ナップサックDP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題、diff <font color="green">843</font>)
- <a href="https://yukicoder.me/problems/no/2232">No.2232 Miser's Gift</a> (yukicoder contest 379 (2023-03-03) - A問題、diff <font color="deepskyblue">1389</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題、diff <font color="green">875</font>)
- <a href="https://yukicoder.me/problems/no/2429">No.2429 Happiest Tabehodai Ways</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - F問題、diff <font color="blue">1907</font>)
- <a href="https://yukicoder.me/problems/no/2542">No.2542 Yokan for Two</a> (yukicoder contest 413 (2023-11-24) - B問題、diff <font color="deepskyblue">1469</font>)

　
<h2 id="門松列DP">76. 門松列DP</h2>

### 難易度統計

「門松列DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="deepskyblue">1307</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.1／diff <font color="deepskyblue">1336</font>
- 2022年: ★3／diff <font color="deepskyblue">1220</font>

### レベル別問題一覧

「門松列DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2374">No.2374 ASKT Subsequences</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - D問題、diff <font color="deepskyblue">1578</font>)
- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)

　
<h2 id="マッチ度ごとに管理">77. マッチ度ごとに管理</h2>

### 難易度統計

「マッチ度ごとに管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="deepskyblue">1449</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.3／diff <font color="deepskyblue">1517</font>
- 2022年: ★2.5／diff <font color="deepskyblue">1247</font>

### レベル別問題一覧

「マッチ度ごとに管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2373">No.2373 wa, wo, n</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - C問題、diff <font color="green">1182</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2374">No.2374 ASKT Subsequences</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - D問題、diff <font color="deepskyblue">1578</font>)
- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)

　
<h2 id="実験">78. 実験</h2>

### 難易度統計

「実験」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="deepskyblue">1485</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.3／diff <font color="deepskyblue">1250</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2191</font>

### レベル別問題一覧

「実験」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2216">No.2216 Pa1indr0me</a> (yukicoder contest 377 (2023-02-17) - A問題、diff <font color="gray">344</font>)
- <a href="https://yukicoder.me/problems/no/2393">No.2393 Bit Grid Connected Component</a> (yukicoder contest 399 (2023-07-28) - B問題、diff <font color="green">1050</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題、diff <font color="yellowgreen">2191</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2521">No.2521 Don't be Same</a> (yukicoder contest 410 (2023-10-27) - G問題、diff <font color="yellowgreen">2357</font>)

　
<h2 id="一要素削除">79. 一要素削除</h2>

### 難易度統計

「一要素削除」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1608</font>
- 2024年: ★1／diff <font color="gray">352</font>
- 2023年: ★2.5／diff <font color="blue">1909</font>
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「一要素削除」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)

　
<h2 id="同じ値の纏め上げ">80. 同じ値の纏め上げ</h2>

### 難易度統計

「同じ値の纏め上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1638</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.4／diff <font color="blue">1645</font>
- 2022年: ★2.3／diff <font color="blue">1624</font>

### レベル別問題一覧

「同じ値の纏め上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題、diff <font color="deepskyblue">1206</font>)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題、diff <font color="green">1069</font>)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題、diff <font color="deepskyblue">1258</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題、diff <font color="blue">1865</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)

　
<h2 id="試し割り法">81. 試し割り法</h2>

### 難易度統計

「試し割り法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1647</font>
- 2024年: ★2.5／diff <font color="blue">1941</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1554</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2291</font>

### レベル別問題一覧

「試し割り法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2417">No.2417 Div Count</a> (MMA Contest 016 (2023-08-12) - D問題、diff <font color="brown">781</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2480">No.2480 Sequence Sum</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - B問題、diff <font color="deepskyblue">1433</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="最小公倍数計算">82. 最小公倍数計算</h2>

### 難易度統計

「最小公倍数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1660</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.3／diff <font color="blue">1660</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最小公倍数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

　
<h2 id="累積積">83. 累積積</h2>

### 難易度統計

「累積積」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1668</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1550</font>
- 2023年: ★2.3／diff <font color="blue">1638</font>
- 2022年: ★2.3／diff <font color="blue">1786</font>

### レベル別問題一覧

「累積積」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題、diff <font color="deepskyblue">1258</font>)
- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)
- <a href="https://yukicoder.me/problems/no/2494">No.2494 Sum within Components</a> (yukicoder contest 407 (2023-10-06) - C問題、diff <font color="green">1031</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2615">No.2615 ペアの作り方</a> (yukicoder contest 416 (2024-01-26) - B問題、diff <font color="green">958</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)
- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="変数決め打ち">84. 変数決め打ち</h2>

### 難易度統計

「変数決め打ち」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1779</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2177</font>
- 2023年: ★2.2／diff <font color="blue">1623</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2061</font>

### レベル別問題一覧

「変数決め打ち」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)
- <a href="https://yukicoder.me/problems/no/2562">No.2562 数字探しゲーム（緑以下コンver.）</a> (第2回緑以下コンテスト (2023-12-02) - F問題、diff <font color="deepskyblue">1356</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題、diff <font color="blue">1728</font>)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)
- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2374">No.2374 ASKT Subsequences</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - D問題、diff <font color="deepskyblue">1578</font>)
- <a href="https://yukicoder.me/problems/no/2386">No.2386 Udon Coupon (Easy)</a> (yukicoder contest 398 (2023-07-21) - B問題、diff <font color="green">982</font>)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)
- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)
- <a href="https://yukicoder.me/problems/no/2601">No.2601 Very Poor</a> (yukicoder contest 414 (2024-01-12) - C問題、diff <font color="green">1032</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2463">No.2463 ストレートフラッシュ</a> (yukicoder contest 404 (2023-09-08) - D問題、diff <font color="blue">1838</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題、diff <font color="orange">2620</font>)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題、diff <font color="yellowgreen">2168</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="円周角の定理">85. 円周角の定理</h2>

### 難易度統計

「円周角の定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1815</font>
- 2024年: ★3／diff <font color="orange">2419</font>
- 2023年: ★2／diff <font color="deepskyblue">1212</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「円周角の定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2469">No.2469 Umbrella Queries</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - C問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

　
<h2 id="アルゴリズムのリアクティブ化">86. アルゴリズムのリアクティブ化</h2>

### 難易度統計

「アルゴリズムのリアクティブ化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1873</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2323</font>
- 2022年: ★2.2／diff <font color="blue">1648</font>

### レベル別問題一覧

「アルゴリズムのリアクティブ化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2124">No.2124 Guess the Permutation</a> (yukicoder contest 368 (2022-11-18) - A問題、diff <font color="green">1158</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題、diff <font color="yellowgreen">2139</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)

　
<h2 id="余事象">87. 余事象</h2>

### 難易度統計

「余事象」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="deepskyblue">1555</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.4／diff <font color="deepskyblue">1555</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「余事象」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題、diff <font color="brown">769</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2486">No.2486 Don't come next to me</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - A問題、diff <font color="brown">712</font>)
- <a href="https://yukicoder.me/problems/no/2585">No.2585 How many "Who is Santa?"</a> (Advent Calendar Contest 2023 (2023-12-01) - M問題、diff <font color="orange">2401</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)

　
<h2 id="ギャグ">88. ギャグ</h2>

### 難易度統計

「ギャグ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1627</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1685</font>
- 2022年: ★2.2／diff <font color="deepskyblue">1423</font>

### レベル別問題一覧

「ギャグ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題、diff <font color="deepskyblue">1206</font>)
- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題、diff <font color="green">912</font>)
- <a href="https://yukicoder.me/problems/no/2425">No.2425 Power Range GCD</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - B問題、diff <font color="brown">680</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題、diff <font color="blue">1641</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題、diff <font color="blue">1983</font>)
- <a href="https://yukicoder.me/problems/no/2366">No.2366 登校</a> (yukicoder contest 395 (2023-06-30) - C問題、diff <font color="yellowgreen">2294</font>)
- <a href="https://yukicoder.me/problems/no/2434">No.2434 RAKUTAN de RAKUTAN</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - K問題、diff <font color="orange">2721</font>)
- <a href="https://yukicoder.me/problems/no/2519">No.2519 Coins in Array</a> (yukicoder contest 410 (2023-10-27) - E問題、diff <font color="yellowgreen">2069</font>)

　
<h2 id="累積和">89. 累積和</h2>

### 難易度統計

「累積和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1657</font>
- 2024年: ★3／diff <font color="yellowgreen">2177</font>
- 2023年: ★2.5／diff <font color="blue">1732</font>
- 2022年: ★1.8／diff <font color="green">1100</font>

### レベル別問題一覧

「累積和」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題、diff <font color="brown">406</font>)
- <a href="https://yukicoder.me/problems/no/2124">No.2124 Guess the Permutation</a> (yukicoder contest 368 (2022-11-18) - A問題、diff <font color="green">1158</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題、diff <font color="deepskyblue">1206</font>)
- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題、diff <font color="blue">1632</font>)
- <a href="https://yukicoder.me/problems/no/2352">No.2352 Sharpened Knife in Fall</a> (yukicoder contest 393 (2023-06-16) - C問題、diff <font color="deepskyblue">1560</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2625">No.2625 Bouns Ai</a> (yukicoder contest 417 (2024-02-09) - E問題、diff <font color="blue">1654</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="階乗計算">90. 階乗計算</h2>

### 難易度統計

「階乗計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1671</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1550</font>
- 2023年: ★2.5／diff <font color="blue">1748</font>
- 2022年: ★2.1／diff <font color="deepskyblue">1546</font>

### レベル別問題一覧

「階乗計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2615">No.2615 ペアの作り方</a> (yukicoder contest 416 (2024-01-26) - B問題、diff <font color="green">958</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)
- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="階乗逆元計算">91. 階乗逆元計算</h2>

### 難易度統計

「階乗逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1684</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2.5／diff <font color="blue">1675</font>
- 2022年: ★2.1／diff <font color="deepskyblue">1546</font>

### レベル別問題一覧

「階乗逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="剰余計算">92. 剰余計算</h2>

### 難易度統計

「剰余計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1753</font>
- 2024年: ★2.5／diff <font color="blue">1618</font>
- 2023年: ★2.3／diff <font color="blue">1649</font>
- 2022年: ★2.6／diff <font color="yellowgreen">2059</font>

### レベル別問題一覧

「剰余計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2415">No.2415 偶数判定！Nafmoくん</a> (MMA Contest 016 (2023-08-12) - B問題、diff <font color="gray">188</font>)
- <a href="https://yukicoder.me/problems/no/2558">No.2558 中国剰余定理</a> (第2回緑以下コンテスト (2023-12-02) - B問題、diff <font color="gray">306</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題、diff <font color="green">999</font>)
- <a href="https://yukicoder.me/problems/no/2562">No.2562 数字探しゲーム（緑以下コンver.）</a> (第2回緑以下コンテスト (2023-12-02) - F問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2600">No.2600 Avator Height</a> (yukicoder contest 414 (2024-01-12) - B問題、diff <font color="brown">686</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題、diff <font color="deepskyblue">1261</font>)
- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題、diff <font color="deepskyblue">1206</font>)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題、diff <font color="deepskyblue">1258</font>)
- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題、diff <font color="green">831</font>)
- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)
- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題、diff <font color="blue">1605</font>)
- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2467">No.2467 Sum of Product of Binomial Coefficients</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - A問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2494">No.2494 Sum within Components</a> (yukicoder contest 407 (2023-10-06) - C問題、diff <font color="green">1031</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2541">No.2541 Divide 01 String</a> (yukicoder contest 413 (2023-11-24) - A問題、diff <font color="brown">606</font>)
- <a href="https://yukicoder.me/problems/no/2550">No.2550 MORE! JUMP! MORE!</a> (MMA Contest 017 (2023-11-25) - D問題、diff <font color="blue">1629</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)
- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)
- <a href="https://yukicoder.me/problems/no/2615">No.2615 ペアの作り方</a> (yukicoder contest 416 (2024-01-26) - B問題、diff <font color="green">958</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題、diff <font color="deepskyblue">1331</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2357">No.2357 Guess the Function</a> (yukicoder contest 394 (2023-06-23) - A問題、diff <font color="blue">1743</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)
- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)
- <a href="https://yukicoder.me/problems/no/2528">No.2528 pop_(backfront or not)</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - D問題、diff <font color="blue">1839</font>)
- <a href="https://yukicoder.me/problems/no/2529">No.2529 Treasure Hunter</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - E問題、diff <font color="blue">1951</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2585">No.2585 How many "Who is Santa?"</a> (Advent Calendar Contest 2023 (2023-12-01) - M問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)
- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題、diff <font color="yellowgreen">2327</font>)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題、diff <font color="yellowgreen">2168</font>)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題、diff <font color="orange">2673</font>)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題、diff <font color="orange">2758</font>)
- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題、diff <font color="red">2852</font>)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題、diff <font color="blue">1865</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2625">No.2625 Bouns Ai</a> (yukicoder contest 417 (2024-02-09) - E問題、diff <font color="blue">1654</font>)

　
<h2 id="ソート">93. ソート</h2>

### 難易度統計

「ソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1799</font>
- 2024年: ★2.7／diff <font color="blue">1979</font>
- 2023年: ★2.2／diff <font color="blue">1687</font>
- 2022年: ★2.8／diff <font color="yellowgreen">2210</font>

### レベル別問題一覧

「ソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2424">No.2424 Josouzai</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - A問題、diff <font color="brown">769</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題、diff <font color="gray">342</font>)
- <a href="https://yukicoder.me/problems/no/2493">No.2493 K-th in L2 with L1</a> (yukicoder contest 407 (2023-10-06) - B問題、diff <font color="green">1182</font>)
- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)
- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題、diff <font color="deepskyblue">1551</font>)
- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題、diff <font color="green">1174</font>)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2615">No.2615 ペアの作り方</a> (yukicoder contest 416 (2024-01-26) - B問題、diff <font color="green">958</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2210">No.2210 equence Squence Seuence</a> (yukicoder contest 376 (2023-02-10) - C問題、diff <font color="deepskyblue">1489</font>)
- <a href="https://yukicoder.me/problems/no/2353">No.2353 Guardian Dogs in Spring</a> (yukicoder contest 393 (2023-06-16) - D問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)
- <a href="https://yukicoder.me/problems/no/2501">No.2501 Maximum Inversion Number</a> (yukicoder contest 408 (2023-10-13) - B問題、diff <font color="yellowgreen">2064</font>)
- <a href="https://yukicoder.me/problems/no/2510">No.2510 Six Cube Sum Counting</a> (yukicoder contest 409 (2023-10-20) - C問題、diff <font color="yellowgreen">2219</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2623">No.2623 Room Allocation</a> (yukicoder contest 417 (2024-02-09) - C問題、diff <font color="deepskyblue">1328</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題、diff <font color="yellowgreen">2274</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)
- <a href="https://yukicoder.me/problems/no/2553">No.2553 Holidays</a> (MMA Contest 017 (2023-11-25) - G問題、diff <font color="red">2858</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

　
<h2 id="２変数決め打ち">94. ２変数決め打ち</h2>

### 難易度統計

「２変数決め打ち」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1827</font>
- 2024年: ★3／diff <font color="orange">2491</font>
- 2023年: ★2.3／diff <font color="blue">1695</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「２変数決め打ち」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2386">No.2386 Udon Coupon (Easy)</a> (yukicoder contest 398 (2023-07-21) - B問題、diff <font color="green">982</font>)
- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)

　
<h2 id="最終手番に注目">95. 最終手番に注目</h2>

### 難易度統計

「最終手番に注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1855</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1798</font>
- 2022年: ★2.3／diff <font color="blue">1951</font>

### レベル別問題一覧

「最終手番に注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2209">No.2209 Flip and Reverse</a> (yukicoder contest 376 (2023-02-10) - B問題、diff <font color="green">1008</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題、diff <font color="blue">1934</font>)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題、diff <font color="blue">1838</font>)
- <a href="https://yukicoder.me/problems/no/2502">No.2502 Optimization in the Dark</a> (yukicoder contest 408 (2023-10-13) - C問題、diff <font color="orange">2503</font>)
- <a href="https://yukicoder.me/problems/no/2518">No.2518 Adjacent Larger</a> (yukicoder contest 410 (2023-10-27) - D問題、diff <font color="deepskyblue">1488</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)

　
<h2 id="合成による次元削減">96. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#合成による次元削減">合成による次元削減</a></h2>

### 難易度統計

「[合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#合成による次元削減)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="green">1172</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="green">1172</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#合成による次元削減)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2486">No.2486 Don't come next to me</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - A問題、diff <font color="brown">712</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)

　
<h2 id="最長歩道計算">97. 最長歩道計算</h2>

### 難易度統計

「最長歩道計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1200</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1200</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最長歩道計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)

　
<h2 id="操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着">98. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着">操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着</a></h2>

### 難易度統計

「[操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1200</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1200</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)

　
<h2 id="３進法">99. ３進法</h2>

### 難易度統計

「３進法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1318</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1318</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「３進法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2410">No.2410 Nine Numbers</a> (yukicoder contest 401 (2023-08-11) - D問題、diff <font color="deepskyblue">1318</font>)

　
<h2 id="範囲加算更新を１つの配列に纏め上げ">100. 範囲加算更新を１つの配列に纏め上げ</h2>

### 難易度統計

「範囲加算更新を１つの配列に纏め上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1358</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1358</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「範囲加算更新を１つの配列に纏め上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

　
<h2 id="DAG上のDP">101. DAG上のDP</h2>

### 難易度統計

「DAG上のDP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1408</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="deepskyblue">1324</font>
- 2022年: ★2／diff <font color="deepskyblue">1577</font>

### レベル別問題一覧

「DAG上のDP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2100">No.2100 [Cherry Alpha C] Two-way Steps</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - D問題、diff <font color="deepskyblue">1577</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2430">No.2430 Damage Zone</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - G問題、diff <font color="deepskyblue">1449</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)

　
<h2 id="B進法による構築">102. B進法による構築</h2>

### 難易度統計

「B進法による構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1424</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1531</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1318</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「B進法による構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2410">No.2410 Nine Numbers</a> (yukicoder contest 401 (2023-08-11) - D問題、diff <font color="deepskyblue">1318</font>)
- <a href="https://yukicoder.me/problems/no/2609">No.2609 Decreasing GCDs</a> (yukicoder contest 415 (2024-01-19) - C問題、diff <font color="deepskyblue">1531</font>)

　
<h2 id="部分和と補部分和の差の最小化">103. 部分和と補部分和の差の最小化</h2>

### 難易度統計

「部分和と補部分和の差の最小化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1469</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1469</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「部分和と補部分和の差の最小化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2542">No.2542 Yokan for Two</a> (yukicoder contest 413 (2023-11-24) - B問題、diff <font color="deepskyblue">1469</font>)

　
<h2 id="操作逆順">104. 操作逆順</h2>

### 難易度統計

「操作逆順」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1486</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="deepskyblue">1486</font>

### レベル別問題一覧

「操作逆順」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題、diff <font color="deepskyblue">1486</font>)

　
<h2 id="隣接不等式管理">105. 隣接不等式管理</h2>

### 難易度統計

「隣接不等式管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1488</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1488</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「隣接不等式管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2518">No.2518 Adjacent Larger</a> (yukicoder contest 410 (2023-10-27) - D問題、diff <font color="deepskyblue">1488</font>)

　
<h2 id="挿入ソート">106. 挿入ソート</h2>

### 難易度統計

「挿入ソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1489</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1489</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「挿入ソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2210">No.2210 equence Squence Seuence</a> (yukicoder contest 376 (2023-02-10) - C問題、diff <font color="deepskyblue">1489</font>)

　
<h2 id="最遠点計算">107. 最遠点計算</h2>

### 難易度統計

「最遠点計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1536</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1536</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最遠点計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2261">No.2261 Coffee</a> (yukicoder contest 383 (2023-04-07) - C問題、diff <font color="deepskyblue">1536</font>)

　
<h2 id="符号全探索による絶対値計算">108. 符号全探索による絶対値計算</h2>

### 難易度統計

「符号全探索による絶対値計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1536</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1536</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「符号全探索による絶対値計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2261">No.2261 Coffee</a> (yukicoder contest 383 (2023-04-07) - C問題、diff <font color="deepskyblue">1536</font>)

　
<h2 id="指定序数の値の計算を被覆の先頭項管理で処理">109. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を被覆の先頭項管理で処理">指定序数の値の計算を被覆の先頭項管理で処理</a></h2>

### 難易度統計

「[指定序数の値の計算を被覆の先頭項管理で処理](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を被覆の先頭項管理で処理)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1544</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1544</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[指定序数の値の計算を被覆の先頭項管理で処理](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を被覆の先頭項管理で処理)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)

　
<h2 id="言及する成分数を最大化する質問">110. 言及する成分数を最大化する質問</h2>

### 難易度統計

「言及する成分数を最大化する質問」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1577</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1577</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「言及する成分数を最大化する質問」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2252">No.2252 Find Zero</a> (yukicoder contest 382 (2023-03-24) - A問題、diff <font color="green">846</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2496">No.2496 LCM between Permutations</a> (yukicoder contest 407 (2023-10-06) - E問題、diff <font color="yellowgreen">2309</font>)

　
<h2 id="倍数メビウス変換">111. 倍数メビウス変換</h2>

### 難易度統計

「倍数メビウス変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1607</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1607</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「倍数メビウス変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

　
<h2 id="不明な想定解">112. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不明な想定解">不明な想定解</a></h2>

### 難易度統計

「[不明な想定解](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不明な想定解)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1619</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1619</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[不明な想定解](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不明な想定解)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2476">No.2476 Knight Game</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - J問題、diffデータなし)

　
<h2 id="階乗による二項係数計算">113. 階乗による二項係数計算</h2>

### 難易度統計

「階乗による二項係数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1626</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1444</font>
- 2022年: ★2.2／diff <font color="blue">1641</font>

### レベル別問題一覧

「階乗による二項係数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="尺取り法">114. 尺取り法</h2>

### 難易度統計

「尺取り法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1653</font>
- 2024年: ★2／diff <font color="green">1032</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1590</font>
- 2022年: ★3／diff <font color="blue">1988</font>

### レベル別問題一覧

「尺取り法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2298">No.2298 yukicounter</a> (yukicoder contest 388 (2023-05-12) - B問題、diff <font color="green">813</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2601">No.2601 Very Poor</a> (yukicoder contest 414 (2024-01-12) - C問題、diff <font color="green">1032</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題、diff <font color="blue">1632</font>)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2553">No.2553 Holidays</a> (MMA Contest 017 (2023-11-25) - G問題、diff <font color="red">2858</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)

　
<h2 id="部分回文列挙">115. 部分回文列挙</h2>

### 難易度統計

「部分回文列挙」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1661</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1661</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「部分回文列挙」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題、diff <font color="blue">1661</font>)

　
<h2 id="区間族管理">116. 区間族管理</h2>

### 難易度統計

「区間族管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1672</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1675</font>
- 2022年: ★2.5／diff <font color="blue">1649</font>

### レベル別問題一覧

「区間族管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2298">No.2298 yukicounter</a> (yukicoder contest 388 (2023-05-12) - B問題、diff <font color="green">813</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)
- <a href="https://yukicoder.me/problems/no/2486">No.2486 Don't come next to me</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - A問題、diff <font color="brown">712</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2553">No.2553 Holidays</a> (MMA Contest 017 (2023-11-25) - G問題、diff <font color="red">2858</font>)

　
<h2 id="最大公約数による最小公倍数計算">117. 最大公約数による最小公倍数計算</h2>

### 難易度統計

「最大公約数による最小公倍数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1698</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1698</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最大公約数による最小公倍数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

　
<h2 id="枝刈り">118. 枝刈り</h2>

### 難易度統計

「枝刈り」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1705</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1705</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「枝刈り」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題、diff <font color="green">939</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題、diff <font color="orange">2471</font>)

　
<h2 id="ポテンシャル付き素集合データ構造">119. ポテンシャル付き素集合データ構造</h2>

### 難易度統計

「ポテンシャル付き素集合データ構造」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1724</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1724</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ポテンシャル付き素集合データ構造」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="頂点倍化">120. 頂点倍化</h2>

### 難易度統計

「頂点倍化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1724</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1724</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「頂点倍化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="円環の倍化実装">121. 円環の倍化実装</h2>

### 難易度統計

「円環の倍化実装」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1727</font>
- 2024年: ★2／diff <font color="green">1032</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2074</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「円環の倍化実装」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2601">No.2601 Very Poor</a> (yukicoder contest 414 (2024-01-12) - C問題、diff <font color="green">1032</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2423">No.2423 Merge Stones</a> (MMA Contest 016 (2023-08-12) - J問題、diff <font color="orange">2521</font>)

　
<h2 id="部分集合DP">122. 部分集合DP</h2>

### 難易度統計

「部分集合DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1728</font>
- 2024年: ★2.5／diff <font color="blue">1728</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「部分集合DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2955">No.2955 Pizza Delivery Plan</a> (yukicoder contest 452 (2024-11-08) - C問題、diff <font color="blue">1728</font>)

　
<h2 id="充足可能性判定">123. 充足可能性判定</h2>

### 難易度統計

「充足可能性判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1742</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1742</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「充足可能性判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="不変量に注目">124. 不変量に注目</h2>

### 難易度統計

「不変量に注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1761</font>
- 2024年: ★3／diff <font color="orange">2442</font>
- 2023年: ★2.2／diff <font color="deepskyblue">1442</font>
- 2022年: ★2.8／diff <font color="yellowgreen">2052</font>

### レベル別問題一覧

「不変量に注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2525">No.2525 Great Move</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - A問題、diff <font color="brown">424</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2451">No.2451 Redistribute Integers</a> (yukicoder contest 403 (2023-09-01) - B問題、diff <font color="green">1158</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題、diff <font color="green">912</font>)
- <a href="https://yukicoder.me/problems/no/2335">No.2335 Jump</a> (yukicoder contest 391 (2023-06-02) - B問題、diff <font color="green">1025</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2519">No.2519 Coins in Array</a> (yukicoder contest 410 (2023-10-27) - E問題、diff <font color="yellowgreen">2069</font>)
- <a href="https://yukicoder.me/problems/no/2521">No.2521 Don't be Same</a> (yukicoder contest 410 (2023-10-27) - G問題、diff <font color="yellowgreen">2357</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題、diff <font color="orange">2500</font>)

　
<h2 id="木の頂点の次数計算">125. 木の頂点の次数計算</h2>

### 難易度統計

「木の頂点の次数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1764</font>
- 2024年: ★3／diff <font color="yellowgreen">2255</font>
- 2023年: ★2／diff <font color="deepskyblue">1273</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「木の頂点の次数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2427">No.2427 Tree Distance Two</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - D問題、diff <font color="deepskyblue">1273</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2618">No.2618 除霊</a> (yukicoder contest 416 (2024-01-26) - E問題、diff <font color="yellowgreen">2255</font>)

　
<h2 id="Vieta Jumping">126. Vieta Jumping</h2>

### 難易度統計

「Vieta Jumping」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1768</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1768</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Vieta Jumping」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題、diff <font color="blue">1768</font>)

　
<h2 id="解と係数の関係">127. 解と係数の関係</h2>

### 難易度統計

「解と係数の関係」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1768</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1768</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「解と係数の関係」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題、diff <font color="blue">1768</font>)
- <a href="https://yukicoder.me/problems/no/2474">No.2474 Empty Quartz</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - H問題、diffデータなし)

　
<h2 id="価値上限ありナップサック最適化">128. 価値上限ありナップサック最適化</h2>

### 難易度統計

「価値上限ありナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1774</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1774</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「価値上限ありナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題、diff <font color="blue">1774</font>)

　
<h2 id="重複選択可価値上限ありナップサック最適化">129. 重複選択可価値上限ありナップサック最適化</h2>

### 難易度統計

「重複選択可価値上限ありナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1774</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1774</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「重複選択可価値上限ありナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題、diff <font color="blue">1774</font>)

　
<h2 id="分割統治法">130. 分割統治法</h2>

### 難易度統計

「分割統治法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1816</font>
- 2024年: ★3／diff <font color="yellowgreen">2364</font>
- 2023年: ★2.5／diff <font color="blue">1724</font>
- 2022年: ★2.7／diff <font color="yellowgreen">2022</font>

### レベル別問題一覧

「分割統治法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2563">No.2563 色ごとのグループ</a> (第2回緑以下コンテスト (2023-12-02) - G問題、diff <font color="green">851</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題、diff <font color="blue">1728</font>)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題、diff <font color="deepskyblue">1206</font>)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)
- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題、diff <font color="green">1093</font>)
- <a href="https://yukicoder.me/problems/no/2196">No.2196 Pair Bonus</a> (yukicoder contest 374 (2023-01-20) - C問題、diff <font color="deepskyblue">1314</font>)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題、diff <font color="green">1069</font>)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題、diff <font color="deepskyblue">1258</font>)
- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題、diff <font color="green">831</font>)
- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2374">No.2374 ASKT Subsequences</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - D問題、diff <font color="deepskyblue">1578</font>)
- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)
- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2550">No.2550 MORE! JUMP! MORE!</a> (MMA Contest 017 (2023-11-25) - D問題、diff <font color="blue">1629</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2463">No.2463 ストレートフラッシュ</a> (yukicoder contest 404 (2023-09-08) - D問題、diff <font color="blue">1838</font>)
- <a href="https://yukicoder.me/problems/no/2486">No.2486 Don't come next to me</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - A問題、diff <font color="brown">712</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題、diff <font color="yellowgreen">2168</font>)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題、diff <font color="blue">1865</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2531">No.2531 Coloring Vertices on Namori</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - G問題、diff <font color="blue">1951</font>)
- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題、diff <font color="orange">2737</font>)
- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)
- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題、diff <font color="orange">2566</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="逆元の再帰式">131. 逆元の再帰式</h2>

### 難易度統計

「逆元の再帰式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1818</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2.5／diff <font color="blue">1733</font>
- 2022年: ★2.5／diff <font color="blue">1871</font>

### レベル別問題一覧

「逆元の再帰式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)
- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題、diff <font color="yellowgreen">2327</font>)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="多項定理">132. 多項定理</h2>

### 難易度統計

「多項定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1831</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="orange">2401</font>
- 2022年: ★2／diff <font color="deepskyblue">1261</font>

### レベル別問題一覧

「多項定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題、diff <font color="deepskyblue">1261</font>)
- <a href="https://yukicoder.me/problems/no/2467">No.2467 Sum of Product of Binomial Coefficients</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - A問題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2582">No.2582 Random Average^K</a> (Advent Calendar Contest 2023 (2023-12-01) - J問題、diff <font color="orange">2401</font>)

　
<h2 id="オイラーの定理">133. オイラーの定理</h2>

### 難易度統計

「オイラーの定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1838</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1838</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「オイラーの定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題、diff <font color="blue">1838</font>)

　
<h2 id="オイラーの定理による逆元計算">134. オイラーの定理による逆元計算</h2>

### 難易度統計

「オイラーの定理による逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1838</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1838</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「オイラーの定理による逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題、diff <font color="blue">1838</font>)

　
<h2 id="合成数を法とする逆元計算">135. 合成数を法とする逆元計算</h2>

### 難易度統計

「合成数を法とする逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1838</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1838</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「合成数を法とする逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題、diff <font color="blue">1838</font>)

　
<h2 id="区間代入更新">136. 区間代入更新</h2>

### 難易度統計

「区間代入更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1851</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1851</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間代入更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)

　
<h2 id="損をしない変形">137. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形">損をしない変形</a></h2>

### 難易度統計

「[損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1854</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2149</font>
- 2023年: ★2.4／diff <font color="blue">1734</font>
- 2022年: ★2.6／diff <font color="yellowgreen">2083</font>

### レベル別問題一覧

「[損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題、diff <font color="brown">744</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題、diff <font color="deepskyblue">1529</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2240">No.2240 WAC</a> (yukicoder contest 380 (2023-03-10) - B問題、diff <font color="deepskyblue">1373</font>)
- <a href="https://yukicoder.me/problems/no/2247">No.2247 01 ZigZag</a> (yukicoder contest 381 (2023-03-17) - B問題、diff <font color="blue">1604</font>)
- <a href="https://yukicoder.me/problems/no/2307">No.2307 [Cherry 5 th Tune *] Cool 46</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - C問題、diff <font color="deepskyblue">1345</font>)
- <a href="https://yukicoder.me/problems/no/2386">No.2386 Udon Coupon (Easy)</a> (yukicoder contest 398 (2023-07-21) - B問題、diff <font color="green">982</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題、diff <font color="deepskyblue">1331</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2422">No.2422 regisys?</a> (MMA Contest 016 (2023-08-12) - I問題、diff <font color="yellowgreen">2353</font>)
- <a href="https://yukicoder.me/problems/no/2501">No.2501 Maximum Inversion Number</a> (yukicoder contest 408 (2023-10-13) - B問題、diff <font color="yellowgreen">2064</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2623">No.2623 Room Allocation</a> (yukicoder contest 417 (2024-02-09) - C問題、diff <font color="deepskyblue">1328</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題、diff <font color="orange">2758</font>)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)
- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題、diff <font color="yellowgreen">2175</font>)
- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題、diff <font color="yellowgreen">2274</font>)
- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2096">No.2096 Rage With Our Friends</a> (yukicoder contest 363 (2022-10-07) - E問題、diff <font color="orange">2690</font>)

　
<h2 id="二分探索">138. 二分探索</h2>

### 難易度統計

「二分探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1864</font>
- 2024年: ★2.6／diff <font color="yellowgreen">2177</font>
- 2023年: ★2.4／diff <font color="blue">1753</font>
- 2022年: ★3.5／diff <font color="yellowgreen">2364</font>

### レベル別問題一覧

「二分探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2479">No.2479 Sum of Squares</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - A問題、diff <font color="brown">779</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)
- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題、diff <font color="green">1174</font>)
- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)
- <a href="https://yukicoder.me/problems/no/2420">No.2420 Simple Problem</a> (MMA Contest 016 (2023-08-12) - G問題、diff <font color="deepskyblue">1228</font>)
- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)
- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題、diff <font color="blue">1774</font>)
- <a href="https://yukicoder.me/problems/no/2352">No.2352 Sharpened Knife in Fall</a> (yukicoder contest 393 (2023-06-16) - C問題、diff <font color="deepskyblue">1560</font>)
- <a href="https://yukicoder.me/problems/no/2354">No.2354 Poor Sight in Winter</a> (yukicoder contest 393 (2023-06-16) - E問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2501">No.2501 Maximum Inversion Number</a> (yukicoder contest 408 (2023-10-13) - B問題、diff <font color="yellowgreen">2064</font>)
- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)
- <a href="https://yukicoder.me/problems/no/2387">No.2387 Yokan Factory</a> (yukicoder contest 398 (2023-07-21) - C問題、diff <font color="deepskyblue">1376</font>)
- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)
- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)

　
<h2 id="冪乗計算">139. 冪乗計算</h2>

### 難易度統計

「冪乗計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1868</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1864</font>
- 2022年: ★2.6／diff <font color="blue">1877</font>

### レベル別問題一覧

「冪乗計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題、diff <font color="deepskyblue">1261</font>)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題、diff <font color="deepskyblue">1258</font>)
- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題、diff <font color="blue">1605</font>)
- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2467">No.2467 Sum of Product of Binomial Coefficients</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - A問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2494">No.2494 Sum within Components</a> (yukicoder contest 407 (2023-10-06) - C問題、diff <font color="green">1031</font>)
- <a href="https://yukicoder.me/problems/no/2550">No.2550 MORE! JUMP! MORE!</a> (MMA Contest 017 (2023-11-25) - D問題、diff <font color="blue">1629</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2585">No.2585 How many "Who is Santa?"</a> (Advent Calendar Contest 2023 (2023-12-01) - M問題、diff <font color="orange">2401</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題、diff <font color="yellowgreen">2168</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="階差数列">140. 階差数列</h2>

### 難易度統計

「階差数列」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1887</font>
- 2024年: ★3／diff <font color="orange">2442</font>
- 2023年: ★2／diff <font color="deepskyblue">1540</font>
- 2022年: ★2.7／diff <font color="blue">1853</font>

### レベル別問題一覧

「階差数列」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2451">No.2451 Redistribute Integers</a> (yukicoder contest 403 (2023-09-01) - B問題、diff <font color="green">1158</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題、diff <font color="deepskyblue">1206</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題、diff <font color="orange">2500</font>)

　
<h2 id="素数列による試し割り法">141. 素数列による試し割り法</h2>

### 難易度統計

「素数列による試し割り法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1887</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1887</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素数列による試し割り法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)

　
<h2 id="指定序数の値の計算を始切片の数え上げに帰着">142. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を始切片の数え上げに帰着">指定序数の値の計算を始切片の数え上げに帰着</a></h2>

### 難易度統計

「[指定序数の値の計算を始切片の数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を始切片の数え上げに帰着)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1890</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.1／diff <font color="blue">1637</font>
- 2022年: ★3.5／diff <font color="orange">2648</font>

### レベル別問題一覧

「[指定序数の値の計算を始切片の数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を始切片の数え上げに帰着)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2246">No.2246 1333-like Number</a> (yukicoder contest 381 (2023-03-17) - A問題、diff <font color="brown">689</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="フェルマーの小定理">143. フェルマーの小定理</h2>

### 難易度統計

「フェルマーの小定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1891</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1814</font>
- 2022年: ★3／diff <font color="orange">2430</font>

### レベル別問題一覧

「フェルマーの小定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題、diff <font color="blue">1605</font>)
- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)

　
<h2 id="区間を切片の差に翻訳">144. 区間を切片の差に翻訳</h2>

### 難易度統計

「区間を切片の差に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1891</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1891</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間を切片の差に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)
- <a href="https://yukicoder.me/problems/no/2474">No.2474 Empty Quartz</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - H問題、diffデータなし)

　
<h2 id="繰り返し二乗法">145. 繰り返し二乗法</h2>

### 難易度統計

「繰り返し二乗法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1896</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1898</font>
- 2022年: ★2.7／diff <font color="blue">1888</font>

### レベル別問題一覧

「繰り返し二乗法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題、diff <font color="deepskyblue">1261</font>)
- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題、diff <font color="blue">1605</font>)
- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2467">No.2467 Sum of Product of Binomial Coefficients</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - A問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2550">No.2550 MORE! JUMP! MORE!</a> (MMA Contest 017 (2023-11-25) - D問題、diff <font color="blue">1629</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2585">No.2585 How many "Who is Santa?"</a> (Advent Calendar Contest 2023 (2023-12-01) - M問題、diff <font color="orange">2401</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題、diff <font color="yellowgreen">2168</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="周期に注目">146. 周期に注目</h2>

### 難易度統計

「周期に注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1902</font>
- 2024年: ★2.7／diff <font color="blue">1944</font>
- 2023年: ★2.5／diff <font color="blue">1849</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2191</font>

### レベル別問題一覧

「周期に注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題、diff <font color="brown">744</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)
- <a href="https://yukicoder.me/problems/no/2622">No.2622 Dam</a> (yukicoder contest 417 (2024-02-09) - B問題、diff <font color="green">1029</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題、diff <font color="yellowgreen">2191</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題、diff <font color="blue">1933</font>)
- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)
- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="最終手番の任意性">147. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性">最終手番の任意性</a></h2>

### 難易度統計

「[最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1934</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="blue">1934</font>

### レベル別問題一覧

「[最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題、diff <font color="blue">1934</font>)

　
<h2 id="集合管理">148. 集合管理</h2>

### 難易度統計

「集合管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1937</font>
- 2024年: ★2.3／diff <font color="blue">1932</font>
- 2023年: ★2.5／diff <font color="blue">1921</font>
- 2022年: ★2.8／diff <font color="blue">1974</font>

### レベル別問題一覧

「集合管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2607">No.2607 Add One Digit</a> (yukicoder contest 415 (2024-01-19) - A問題、diff <font color="green">1070</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="ニム和">149. ニム和</h2>

### 難易度統計

「ニム和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1940</font>
- 2024年: ★3／diff <font color="yellowgreen">2349</font>
- 2023年: ★2／diff <font color="green">912</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2249</font>

### レベル別問題一覧

「ニム和」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題、diff <font color="green">912</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2165">No.2165 Let's Play Nim!</a> (Advent Calendar Contest 2022 (2022-12-01) - P問題、diff <font color="orange">2491</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)

　
<h2 id="場合分けによるmin・max計算">150. 場合分けによるmin・max計算</h2>

### 難易度統計

「場合分けによるmin・max計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1983</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1983</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「場合分けによるmin・max計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)

　
<h2 id="多点BFS">151. 多点BFS</h2>

### 難易度統計

「多点BFS」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1989</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1989</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「多点BFS」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題、diff <font color="blue">1989</font>)

　
<h2 id="minimax法">152. minimax法</h2>

### 難易度統計

「minimax法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1996</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1996</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「minimax法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2532">No.2532 Want Play More</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - H問題、diff <font color="blue">1996</font>)

　
<h2 id="クラスカル法">153. クラスカル法</h2>

### 難易度統計

「クラスカル法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2044</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2044</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「クラスカル法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)

　
<h2 id="一要素追加">154. 一要素追加</h2>

### 難易度統計

「一要素追加」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2121</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2121</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「一要素追加」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

　
<h2 id="オイラーグラフ判定">155. オイラーグラフ判定</h2>

### 難易度統計

「オイラーグラフ判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2123</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2123</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「オイラーグラフ判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2403">No.2403 "Eight" Bridges of Konigsberg</a> (yukicoder contest 400 (2023-08-04) - E問題、diff <font color="yellowgreen">2123</font>)

　
<h2 id="上限・下限値に言及する質問">156. 上限・下限値に言及する質問</h2>

### 難易度統計

「上限・下限値に言及する質問」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2123</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2123</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「上限・下限値に言及する質問」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2357">No.2357 Guess the Function</a> (yukicoder contest 394 (2023-06-23) - A問題、diff <font color="blue">1743</font>)
- <a href="https://yukicoder.me/problems/no/2502">No.2502 Optimization in the Dark</a> (yukicoder contest 408 (2023-10-13) - C問題、diff <font color="orange">2503</font>)

　
<h2 id="定数倍メモリ削減">157. 定数倍メモリ削減</h2>

### 難易度統計

「定数倍メモリ削減」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2219</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2219</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「定数倍メモリ削減」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2510">No.2510 Six Cube Sum Counting</a> (yukicoder contest 409 (2023-10-20) - C問題、diff <font color="yellowgreen">2219</font>)

　
<h2 id="階乗進法">158. 階乗進法</h2>

### 難易度統計

「階乗進法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2323</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2323</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「階乗進法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)

　
<h2 id="個数上限１複数ナップサック最適化">159. 個数上限１複数ナップサック最適化</h2>

### 難易度統計

「個数上限１複数ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2353</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2353</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「個数上限１複数ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2422">No.2422 regisys?</a> (MMA Contest 016 (2023-08-12) - I問題、diff <font color="yellowgreen">2353</font>)

　
<h2 id="複数ナップサック最適化">160. 複数ナップサック最適化</h2>

### 難易度統計

「複数ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2353</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2353</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「複数ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2422">No.2422 regisys?</a> (MMA Contest 016 (2023-08-12) - I問題、diff <font color="yellowgreen">2353</font>)

　
<h2 id="三分探索">161. 三分探索</h2>

### 難易度統計

「三分探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="orange">2421</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="orange">2421</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「三分探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)

　
<h2 id="必勝戦略のリアクティブ化">162. 必勝戦略のリアクティブ化</h2>

### 難易度統計

「必勝戦略のリアクティブ化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="orange">2491</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="orange">2491</font>

### レベル別問題一覧

「必勝戦略のリアクティブ化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2165">No.2165 Let's Play Nim!</a> (Advent Calendar Contest 2022 (2022-12-01) - P問題、diff <font color="orange">2491</font>)

　
<h2 id="全順序集合を状態に持つゲームをP状態とN状態の区間に分割">163. 全順序集合を状態に持つゲームをP状態とN状態の区間に分割</h2>

### 難易度統計

「全順序集合を状態に持つゲームをP状態とN状態の区間に分割」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="orange">2501</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="orange">2501</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「全順序集合を状態に持つゲームをP状態とN状態の区間に分割」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2551">No.2551 2, 3, 5, 7 Game</a> (MMA Contest 017 (2023-11-25) - E問題、diff <font color="orange">2501</font>)

　
<h2 id="検索">164. 検索</h2>

### 難易度統計

「検索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1738</font>
- 2024年: ★3.5／diff <font color="red">2860</font>
- 2023年: ★2.7／diff <font color="blue">1768</font>
- 2022年: ★1.5／diff <font color="brown">588</font>

### レベル別問題一覧

「検索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題、diff <font color="blue">1768</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2476">No.2476 Knight Game</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - J問題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="終点からの経路計算">165. 終点からの経路計算</h2>

### 難易度統計

「終点からの経路計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1757</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="blue">1757</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「終点からの経路計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2565">No.2565 はじめてのおつかい</a> (第2回緑以下コンテスト (2023-12-02) - I問題、diff <font color="green">972</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2569">No.2569 はじめてのおつかいHard</a> (緑以下コンテスト  Extra (2023-12-02) - A問題、diff <font color="deepskyblue">1385</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)

　
<h2 id="クエリ先読み">166. クエリ先読み</h2>

### 難易度統計

「クエリ先読み」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1765</font>
- 2024年: ★1.5／diff <font color="brown">686</font>
- 2023年: ★2.8／diff <font color="yellowgreen">2147</font>
- 2022年: ★2.8／diff <font color="blue">1743</font>

### レベル別問題一覧

「クエリ先読み」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2600">No.2600 Avator Height</a> (yukicoder contest 414 (2024-01-12) - B問題、diff <font color="brown">686</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題、diff <font color="deepskyblue">1486</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)

　
<h2 id="差分計算">167. 差分計算</h2>

### 難易度統計

「差分計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1778</font>
- 2024年: ★3／diff <font color="orange">2420</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1443</font>
- 2022年: ★3.5／diff <font color="orange">2476</font>

### レベル別問題一覧

「差分計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2306">No.2306 [Cherry 5th Tune C] ウソツキタマシイ</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - B問題、diff <font color="green">812</font>)
- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題、diff <font color="deepskyblue">1331</font>)
- <a href="https://yukicoder.me/problems/no/2510">No.2510 Six Cube Sum Counting</a> (yukicoder contest 409 (2023-10-20) - C問題、diff <font color="yellowgreen">2219</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2618">No.2618 除霊</a> (yukicoder contest 416 (2024-01-26) - E問題、diff <font color="yellowgreen">2255</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="ミラー戦略">168. ミラー戦略</h2>

### 難易度統計

「ミラー戦略」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1821</font>
- 2024年: ★3／diff <font color="yellowgreen">2349</font>
- 2023年: ★2.6／diff <font color="deepskyblue">1590</font>
- 2022年: ★2.5／diff <font color="blue">1905</font>

### レベル別問題一覧

「ミラー戦略」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題、diff <font color="green">912</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2481">No.2481 Shiritori</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - C問題、diff <font color="blue">1706</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2476">No.2476 Knight Game</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - J問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)

　
<h2 id="素因数分解">169. 素因数分解</h2>

### 難易度統計

「素因数分解」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1845</font>
- 2024年: ★2.5／diff <font color="blue">1941</font>
- 2023年: ★2.6／diff <font color="blue">1753</font>
- 2022年: ★2.8／diff <font color="yellowgreen">2214</font>

### レベル別問題一覧

「素因数分解」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2417">No.2417 Div Count</a> (MMA Contest 016 (2023-08-12) - D問題、diff <font color="brown">781</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2480">No.2480 Sequence Sum</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - B問題、diff <font color="deepskyblue">1433</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)
- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="素数を法とする逆元計算">170. 素数を法とする逆元計算</h2>

### 難易度統計

「素数を法とする逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1866</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2.6／diff <font color="blue">1805</font>
- 2022年: ★2.5／diff <font color="blue">1964</font>

### レベル別問題一覧

「素数を法とする逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)
- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題、diff <font color="yellowgreen">2327</font>)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="端から確定">171. 端から確定</h2>

### 難易度統計

「端から確定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1903</font>
- 2024年: ★3／diff <font color="yellowgreen">2349</font>
- 2023年: ★2.5／diff <font color="blue">1835</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2008</font>

### レベル別問題一覧

「端から確定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2518">No.2518 Adjacent Larger</a> (yukicoder contest 410 (2023-10-27) - D問題、diff <font color="deepskyblue">1488</font>)
- <a href="https://yukicoder.me/problems/no/2551">No.2551 2, 3, 5, 7 Game</a> (MMA Contest 017 (2023-11-25) - E問題、diff <font color="orange">2501</font>)
- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)

　
<h2 id="エラトステネスの篩">172. エラトステネスの篩</h2>

### 難易度統計

「エラトステネスの篩」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1928</font>
- 2024年: ★2.5／diff <font color="blue">1830</font>
- 2023年: ★2.5／diff <font color="blue">1887</font>
- 2022年: ★3／diff <font color="yellowgreen">2167</font>

### レベル別問題一覧

「エラトステネスの篩」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2609">No.2609 Decreasing GCDs</a> (yukicoder contest 415 (2024-01-19) - C問題、diff <font color="deepskyblue">1531</font>)
- <a href="https://yukicoder.me/problems/no/2610">No.2610 Decreasing LCMs</a> (yukicoder contest 415 (2024-01-19) - D問題、diff <font color="yellowgreen">2129</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)

　
<h2 id="距離空間の重み付きグラフ化">173. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化">距離空間の重み付きグラフ化</a></h2>

### 難易度統計

「[距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1933</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="blue">1933</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2354">No.2354 Poor Sight in Winter</a> (yukicoder contest 393 (2023-06-16) - E問題、diff <font color="blue">1670</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)

　
<h2 id="素数を用いた構築">174. 素数を用いた構築</h2>

### 難易度統計

「素数を用いた構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1942</font>
- 2024年: ★2.5／diff <font color="blue">1830</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2167</font>

### レベル別問題一覧

「素数を用いた構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2609">No.2609 Decreasing GCDs</a> (yukicoder contest 415 (2024-01-19) - C問題、diff <font color="deepskyblue">1531</font>)
- <a href="https://yukicoder.me/problems/no/2610">No.2610 Decreasing LCMs</a> (yukicoder contest 415 (2024-01-19) - D問題、diff <font color="yellowgreen">2129</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)

　
<h2 id="帰属区間取得">175. 帰属区間取得</h2>

### 難易度統計

「帰属区間取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1944</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="yellowgreen">2042</font>
- 2022年: ★2.5／diff <font color="blue">1649</font>

### レベル別問題一覧

「帰属区間取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)

　
<h2 id="フェルマーの小定理による逆元計算">176. フェルマーの小定理による逆元計算</h2>

### 難易度統計

「フェルマーの小定理による逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1945</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="blue">1876</font>
- 2022年: ★3／diff <font color="orange">2430</font>

### レベル別問題一覧

「フェルマーの小定理による逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)

　
<h2 id="bitDP">177. bitDP</h2>

### 難易度統計

「bitDP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1968</font>
- 2024年: ★2.5／diff <font color="blue">1728</font>
- 2023年: ★2.5／diff <font color="blue">1901</font>
- 2022年: ★3／diff <font color="yellowgreen">2344</font>

### レベル別問題一覧

「bitDP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2955">No.2955 Pizza Delivery Plan</a> (yukicoder contest 452 (2024-11-08) - C問題、diff <font color="blue">1728</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)
- <a href="https://yukicoder.me/problems/no/2389">No.2389 Cheating Code Golf</a> (yukicoder contest 398 (2023-07-21) - E問題、diff <font color="orange">2451</font>)

　
<h2 id="不変量を保つ戦略">178. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略">不変量を保つ戦略</a></h2>

### 難易度統計

「[不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2002</font>
- 2024年: ★3／diff <font color="yellowgreen">2349</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="blue">1828</font>

### レベル別問題一覧

「[不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)

　
<h2 id="オイラー関数計算">179. オイラー関数計算</h2>

### 難易度統計

「オイラー関数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2018</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="yellowgreen">2018</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「オイラー関数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題、diff <font color="blue">1838</font>)
- <a href="https://yukicoder.me/problems/no/2552">No.2552 Not Coprime, Not Divisor</a> (MMA Contest 017 (2023-11-25) - F問題、diff <font color="yellowgreen">2235</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題、diff <font color="blue">1983</font>)

　
<h2 id="最大・最小要素削除">180. 最大・最小要素削除</h2>

### 難易度統計

「最大・最小要素削除」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2027</font>
- 2024年: ★3／diff <font color="orange">2585</font>
- 2023年: ★2.5／diff <font color="blue">1842</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最大・最小要素削除」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="一要素挿入">181. 一要素挿入</h2>

### 難易度統計

「一要素挿入」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2034</font>
- 2024年: ★3／diff <font color="orange">2585</font>
- 2023年: ★2.5／diff <font color="blue">1826</font>
- 2022年: ★3／diff <font color="yellowgreen">2277</font>

### レベル別問題一覧

「一要素挿入」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="変数の対称性">182. 変数の対称性</h2>

### 難易度統計

「変数の対称性」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2143</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2000</font>
- 2022年: ★3／diff <font color="orange">2430</font>

### レベル別問題一覧

「変数の対称性」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)

　
<h2 id="ナップサック割り当て数え上げ">183. ナップサック割り当て数え上げ</h2>

### 難易度統計

「ナップサック割り当て数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2301</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2154</font>
- 2022年: ★3／diff <font color="orange">2595</font>

### レベル別問題一覧

「ナップサック割り当て数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2429">No.2429 Happiest Tabehodai Ways</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - F問題、diff <font color="blue">1907</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)

　
<h2 id="サンプルから推測">184. サンプルから推測</h2>

### 難易度統計

「サンプルから推測」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="deepskyblue">1346</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="deepskyblue">1346</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「サンプルから推測」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2216">No.2216 Pa1indr0me</a> (yukicoder contest 377 (2023-02-17) - A問題、diff <font color="gray">344</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

　
<h2 id="深さ優先探索">185. 深さ優先探索</h2>

### 難易度統計

「深さ優先探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1741</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="blue">1741</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「深さ優先探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題、diff <font color="brown">769</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題、diff <font color="blue">1661</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題、diff <font color="blue">1933</font>)
- <a href="https://yukicoder.me/problems/no/2301">No.2301 Namorientation</a> (yukicoder contest 388 (2023-05-12) - E問題、diff <font color="deepskyblue">1499</font>)
- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2531">No.2531 Coloring Vertices on Namori</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - G問題、diff <font color="blue">1951</font>)

　
<h2 id="二項係数計算">186. 二項係数計算</h2>

### 難易度統計

「二項係数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1789</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2.8／diff <font color="blue">1775</font>
- 2022年: ★2.2／diff <font color="blue">1641</font>

### レベル別問題一覧

「二項係数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2344">No.2344 (l+r)^2</a> (yukicoder contest 392 (2023-06-09) - B問題、diff <font color="orange">2768</font>)

　
<h2 id="包除原理">187. 包除原理</h2>

### 難易度統計

「包除原理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1838</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="blue">1683</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「包除原理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)
- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="ダイクストラ法">188. ダイクストラ法</h2>

### 難易度統計

「ダイクストラ法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1841</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="blue">1841</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ダイクストラ法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2328">No.2328 Build Walls</a> (MMA Contest 015  (2023-05-28) - G問題、diff <font color="blue">1915</font>)
- <a href="https://yukicoder.me/problems/no/2354">No.2354 Poor Sight in Winter</a> (yukicoder contest 393 (2023-06-16) - E問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2569">No.2569 はじめてのおつかいHard</a> (緑以下コンテスト  Extra (2023-12-02) - A問題、diff <font color="deepskyblue">1385</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2366">No.2366 登校</a> (yukicoder contest 395 (2023-06-30) - C問題、diff <font color="yellowgreen">2294</font>)
- <a href="https://yukicoder.me/problems/no/2387">No.2387 Yokan Factory</a> (yukicoder contest 398 (2023-07-21) - C問題、diff <font color="deepskyblue">1376</font>)
- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)

　
<h2 id="最短経路長計算">189. 最短経路長計算</h2>

### 難易度統計

「最短経路長計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1918</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="blue">1918</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最短経路長計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2328">No.2328 Build Walls</a> (MMA Contest 015  (2023-05-28) - G問題、diff <font color="blue">1915</font>)
- <a href="https://yukicoder.me/problems/no/2354">No.2354 Poor Sight in Winter</a> (yukicoder contest 393 (2023-06-16) - E問題、diff <font color="blue">1670</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2366">No.2366 登校</a> (yukicoder contest 395 (2023-06-30) - C問題、diff <font color="yellowgreen">2294</font>)
- <a href="https://yukicoder.me/problems/no/2387">No.2387 Yokan Factory</a> (yukicoder contest 398 (2023-07-21) - C問題、diff <font color="deepskyblue">1376</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)

　
<h2 id="bitごとに計算">190. bitごとに計算</h2>

### 難易度統計

「bitごとに計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1922</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="blue">1618</font>
- 2022年: ★3／diff <font color="yellowgreen">2328</font>

### レベル別問題一覧

「bitごとに計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題、diff <font color="green">1093</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)
- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題、diff <font color="blue">1971</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)

　
<h2 id="倍数ゼータ変換">191. 倍数ゼータ変換</h2>

### 難易度統計

「倍数ゼータ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1956</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1607</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「倍数ゼータ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)

　
<h2 id="動的計画法">192. 動的計画法</h2>

### 難易度統計

「動的計画法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1988</font>
- 2024年: ★2.7／diff <font color="blue">1691</font>
- 2023年: ★2.7／diff <font color="blue">1928</font>
- 2022年: ★2.8／diff <font color="yellowgreen">2101</font>

### レベル別問題一覧

「動的計画法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2373">No.2373 wa, wo, n</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - C問題、diff <font color="green">1182</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題、diff <font color="green">843</font>)
- <a href="https://yukicoder.me/problems/no/2095">No.2095 High Rise</a> (yukicoder contest 363 (2022-10-07) - D問題、diff <font color="deepskyblue">1518</font>)
- <a href="https://yukicoder.me/problems/no/2100">No.2100 [Cherry Alpha C] Two-way Steps</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - D問題、diff <font color="deepskyblue">1577</font>)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2150">No.2150 Site Supporter</a> (Advent Calendar Contest 2022 (2022-12-01) - G問題、diff <font color="blue">1909</font>)
- <a href="https://yukicoder.me/problems/no/2155">No.2155 みちらcolor</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - C問題、diff <font color="green">878</font>)
- <a href="https://yukicoder.me/problems/no/2232">No.2232 Miser's Gift</a> (yukicoder contest 379 (2023-03-03) - A問題、diff <font color="deepskyblue">1389</font>)
- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題、diff <font color="green">831</font>)
- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)
- <a href="https://yukicoder.me/problems/no/2374">No.2374 ASKT Subsequences</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - D問題、diff <font color="deepskyblue">1578</font>)
- <a href="https://yukicoder.me/problems/no/2386">No.2386 Udon Coupon (Easy)</a> (yukicoder contest 398 (2023-07-21) - B問題、diff <font color="green">982</font>)
- <a href="https://yukicoder.me/problems/no/2402">No.2402 Dirty Stairs and Shoes</a> (yukicoder contest 400 (2023-08-04) - D問題、diff <font color="green">822</font>)
- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)
- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題、diff <font color="blue">1641</font>)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題、diff <font color="green">875</font>)
- <a href="https://yukicoder.me/problems/no/2429">No.2429 Happiest Tabehodai Ways</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - F問題、diff <font color="blue">1907</font>)
- <a href="https://yukicoder.me/problems/no/2430">No.2430 Damage Zone</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - G問題、diff <font color="deepskyblue">1449</font>)
- <a href="https://yukicoder.me/problems/no/2528">No.2528 pop_(backfront or not)</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - D問題、diff <font color="blue">1839</font>)
- <a href="https://yukicoder.me/problems/no/2529">No.2529 Treasure Hunter</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - E問題、diff <font color="blue">1951</font>)
- <a href="https://yukicoder.me/problems/no/2532">No.2532 Want Play More</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - H問題、diff <font color="blue">1996</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2955">No.2955 Pizza Delivery Plan</a> (yukicoder contest 452 (2024-11-08) - C問題、diff <font color="blue">1728</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題、diff <font color="orange">2620</font>)
- <a href="https://yukicoder.me/problems/no/2082">No.2082 AND OR XOR</a> (yukicoder contest 361 (2022-09-25) - E問題、diff <font color="orange">2501</font>)
- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題、diff <font color="yellowgreen">2327</font>)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題、diff <font color="orange">2673</font>)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題、diff <font color="orange">2758</font>)
- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題、diff <font color="red">2852</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2389">No.2389 Cheating Code Golf</a> (yukicoder contest 398 (2023-07-21) - E問題、diff <font color="orange">2451</font>)
- <a href="https://yukicoder.me/problems/no/2423">No.2423 Merge Stones</a> (MMA Contest 016 (2023-08-12) - J問題、diff <font color="orange">2521</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2434">No.2434 RAKUTAN de RAKUTAN</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - K問題、diff <font color="orange">2721</font>)
- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)
- <a href="https://yukicoder.me/problems/no/2531">No.2531 Coloring Vertices on Namori</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - G問題、diff <font color="blue">1951</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2625">No.2625 Bouns Ai</a> (yukicoder contest 417 (2024-02-09) - E問題、diff <font color="blue">1654</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題、diff <font color="orange">2737</font>)
- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)
- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)
- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)
- <a href="https://yukicoder.me/problems/no/2584">No.2584 The University of Tree</a> (Advent Calendar Contest 2023 (2023-12-01) - L問題、diff <font color="red">2960</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2159">No.2159 Filling 4x4 array</a> (Advent Calendar Contest 2022 (2022-12-01) - J問題、diff <font color="darkgoldenrod ">3382</font>)
- <a href="https://yukicoder.me/problems/no/2580">No.2580 Hyperinflation</a> (Advent Calendar Contest 2023 (2023-12-01) - H問題、diff <font color="red">3103</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)
- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="区間和の指定された区間数え上げ">193. 区間和の指定された区間数え上げ</h2>

### 難易度統計

「区間和の指定された区間数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2009</font>
- 2024年: ★3／diff <font color="yellowgreen">2386</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="blue">1632</font>

### レベル別問題一覧

「区間和の指定された区間数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題、diff <font color="blue">1632</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="再帰的構築">194. 再帰的構築</h2>

### 難易度統計

「再帰的構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2050</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2129</font>
- 2023年: ★3／diff <font color="blue">1971</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「再帰的構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2610">No.2610 Decreasing LCMs</a> (yukicoder contest 415 (2024-01-19) - D問題、diff <font color="yellowgreen">2129</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題、diff <font color="blue">1971</font>)

　
<h2 id="左右から走査">195. 左右から走査</h2>

### 難易度統計

「左右から走査」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2106</font>
- 2024年: ★3／diff <font color="orange">2585</font>
- 2023年: ★2.5／diff <font color="blue">1628</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「左右から走査」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="超頂点追加">196. 超頂点追加</h2>

### 難易度統計

「超頂点追加」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2107</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2107</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「超頂点追加」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2263">No.2263 Perms</a> (yukicoder contest 383 (2023-04-07) - E問題、diff <font color="orange">2420</font>)

　
<h2 id="オイラー関数前計算">197. オイラー関数前計算</h2>

### 難易度統計

「オイラー関数前計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2109</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2109</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「オイラー関数前計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2552">No.2552 Not Coprime, Not Divisor</a> (MMA Contest 017 (2023-11-25) - F問題、diff <font color="yellowgreen">2235</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題、diff <font color="blue">1983</font>)

　
<h2 id="冪等重みの最短経路長計算">198. 冪等重みの最短経路長計算</h2>

### 難易度統計

「冪等重みの最短経路長計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2126</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2126</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「冪等重みの最短経路長計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)

　
<h2 id="転倒数計算">199. 転倒数計算</h2>

### 難易度統計

「転倒数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2145</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2145</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「転倒数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)

　
<h2 id="優先度付きキュー">200. 優先度付きキュー</h2>

### 難易度統計

「優先度付きキュー」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2147</font>
- 2024年: ★3／diff <font color="orange">2585</font>
- 2023年: ★2.6／diff <font color="yellowgreen">2038</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「優先度付きキュー」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2431">No.2431 Viral Hotel</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - H問題、diff <font color="orange">2628</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="高さ奇数ニム和">201. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和">高さ奇数ニム和</a></h2>

### 難易度統計

「[高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2178</font>
- 2024年: ★3／diff <font color="yellowgreen">2349</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="yellowgreen">2008</font>

### レベル別問題一覧

「[高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)

　
<h2 id="半分全列挙">202. 半分全列挙</h2>

### 難易度統計

「半分全列挙」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2232</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="yellowgreen">2142</font>
- 2022年: ★3／diff <font color="orange">2595</font>

### レベル別問題一覧

「半分全列挙」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題、diff <font color="blue">1774</font>)
- <a href="https://yukicoder.me/problems/no/2510">No.2510 Six Cube Sum Counting</a> (yukicoder contest 409 (2023-10-20) - C問題、diff <font color="yellowgreen">2219</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題、diff <font color="yellowgreen">2175</font>)
- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)

　
<h2 id="Convex Hull Trick">203. Convex Hull Trick</h2>

### 難易度統計

「Convex Hull Trick」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2379</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2379</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Convex Hull Trick」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2404">No.2404 Vertical Throw Up</a> (yukicoder contest 400 (2023-08-04) - F問題、diff <font color="yellowgreen">2337</font>)

　
<h2 id="一次式の族の最大・最小値取得">204. 一次式の族の最大・最小値取得</h2>

### 難易度統計

「一次式の族の最大・最小値取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2379</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2379</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「一次式の族の最大・最小値取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2404">No.2404 Vertical Throw Up</a> (yukicoder contest 400 (2023-08-04) - F問題、diff <font color="yellowgreen">2337</font>)

　
<h2 id="区間和取得">205. 区間和取得</h2>

### 難易度統計

「区間和取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1747</font>
- 2024年: ★3／diff <font color="blue">1654</font>
- 2023年: ★2.6／diff <font color="blue">1698</font>
- 2022年: ★3.2／diff <font color="blue">1893</font>

### レベル別問題一覧

「区間和取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2625">No.2625 Bouns Ai</a> (yukicoder contest 417 (2024-02-09) - E問題、diff <font color="blue">1654</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)

　
<h2 id="データを不変量別に分割して管理">206. データを不変量別に分割して管理</h2>

### 難易度統計

「データを不変量別に分割して管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1827</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.8／diff <font color="blue">1827</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「データを不変量別に分割して管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2563">No.2563 色ごとのグループ</a> (第2回緑以下コンテスト (2023-12-02) - G問題、diff <font color="green">851</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2580">No.2580 Hyperinflation</a> (Advent Calendar Contest 2023 (2023-12-01) - H問題、diff <font color="red">3103</font>)

　
<h2 id="配列を像・頻度表で管理">207. 配列を像・頻度表で管理</h2>

### 難易度統計

「配列を像・頻度表で管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1866</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2.6／diff <font color="blue">1830</font>
- 2022年: ★3／diff <font color="blue">1696</font>

### レベル別問題一覧

「配列を像・頻度表で管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="最大公約数計算">208. 最大公約数計算</h2>

### 難易度統計

「最大公約数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1973</font>
- 2024年: ★2／diff <font color="deepskyblue">1208</font>
- 2023年: ★2.6／diff <font color="blue">1771</font>
- 2022年: ★3.1／diff <font color="yellowgreen">2316</font>

### レベル別問題一覧

「最大公約数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)
- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題、diff <font color="yellowgreen">2139</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="最大・最小要素取得">209. 最大・最小要素取得</h2>

### 難易度統計

「最大・最小要素取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1975</font>
- 2024年: ★3／diff <font color="orange">2585</font>
- 2023年: ★2.6／diff <font color="blue">1777</font>
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「最大・最小要素取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="イベントソート">210. イベントソート</h2>

### 難易度統計

「イベントソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1990</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.8／diff <font color="blue">1971</font>
- 2022年: ★3／diff <font color="yellowgreen">2049</font>

### レベル別問題一覧

「イベントソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2431">No.2431 Viral Hotel</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - H問題、diff <font color="orange">2628</font>)

　
<h2 id="imos法">211. imos法</h2>

### 難易度統計

「imos法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1992</font>
- 2024年: ★3／diff <font color="orange">2536</font>
- 2023年: ★2.9／diff <font color="yellowgreen">2008</font>
- 2022年: ★2.5／diff <font color="blue">1680</font>

### レベル別問題一覧

「imos法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2154">No.2154 あさかつの参加人数</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - B問題、diff <font color="brown">711</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

　
<h2 id="sorted set">212. sorted set</h2>

### 難易度統計

「sorted set」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2040</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.8／diff <font color="yellowgreen">2068</font>
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「sorted set」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)

　
<h2 id="平面走査">213. 平面走査</h2>

### 難易度統計

「平面走査」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2045</font>
- 2024年: ★3／diff <font color="yellowgreen">2264</font>
- 2023年: ★2.8／diff <font color="blue">1917</font>
- 2022年: ★3／diff <font color="yellowgreen">2145</font>

### レベル別問題一覧

「平面走査」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="押し付け戦略">214. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略">押し付け戦略</a></h2>

### 難易度統計

「[押し付け戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2058</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2357</font>
- 2022年: ★2.7／diff <font color="blue">1908</font>

### レベル別問題一覧

「[押し付け戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題、diff <font color="yellowgreen">2168</font>)
- <a href="https://yukicoder.me/problems/no/2521">No.2521 Don't be Same</a> (yukicoder contest 410 (2023-10-27) - G問題、diff <font color="yellowgreen">2357</font>)

　
<h2 id="区間kth取得">215. 区間kth取得</h2>

### 難易度統計

「区間kth取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2069</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1851</font>
- 2022年: ★3／diff <font color="yellowgreen">2178</font>

### レベル別問題一覧

「区間kth取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)

　
<h2 id="付値管理">216. 付値管理</h2>

### 難易度統計

「付値管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2081</font>
- 2024年: ★2.5／diff <font color="blue">1941</font>
- 2023年: ★2.9／diff <font color="yellowgreen">2101</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「付値管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題、diff <font color="blue">1605</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="フェニック木">217. フェニック木</h2>

### 難易度統計

「フェニック木」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2101</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2083</font>
- 2022年: ★3／diff <font color="yellowgreen">2109</font>

### レベル別問題一覧

「フェニック木」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)

　
<h2 id="２種の数値を引き算して１種に帰着">218. ２種の数値を引き算して１種に帰着</h2>

### 難易度統計

「２種の数値を引き算して１種に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2149</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2149</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「２種の数値を引き算して１種に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2623">No.2623 Room Allocation</a> (yukicoder contest 417 (2024-02-09) - C問題、diff <font color="deepskyblue">1328</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="既存のアルゴリズムの変形">219. 既存のアルゴリズムの変形</h2>

### 難易度統計

「既存のアルゴリズムの変形」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2189</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2137</font>
- 2022年: ★3／diff <font color="yellowgreen">2344</font>

### レベル別問題一覧

「既存のアルゴリズムの変形」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)

　
<h2 id="区間要素数取得">220. 区間要素数取得</h2>

### 難易度統計

「区間要素数取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2208</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2.5／diff <font color="orange">2401</font>
- 2022年: ★3／diff <font color="yellowgreen">2145</font>

### レベル別問題一覧

「区間要素数取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="$45$度回転">221. $45$度回転</h2>

### 難易度統計

「$45$度回転」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2217</font>
- 2024年: ★3／diff <font color="red">2833</font>
- 2023年: ★2.7／diff <font color="blue">1910</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「$45$度回転」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2261">No.2261 Coffee</a> (yukicoder contest 383 (2023-04-07) - C問題、diff <font color="deepskyblue">1536</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)

　
<h2 id="木DP">222. 木DP</h2>

### 難易度統計

「木DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2234</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.8／diff <font color="yellowgreen">2234</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「木DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2532">No.2532 Want Play More</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - H問題、diff <font color="blue">1996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2584">No.2584 The University of Tree</a> (Advent Calendar Contest 2023 (2023-12-01) - L問題、diff <font color="red">2960</font>)

　
<h2 id="区間加算更新">223. 区間加算更新</h2>

### 難易度統計

「区間加算更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2041</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="blue">1887</font>
- 2022年: ★3.1／diff <font color="yellowgreen">2247</font>

### レベル別問題一覧

「区間加算更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2154">No.2154 あさかつの参加人数</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - B問題、diff <font color="brown">711</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="約数の走査を倍数の走査に帰着">224. 約数の走査を倍数の走査に帰着</h2>

### 難易度統計

「約数の走査を倍数の走査に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2107</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.9／diff <font color="yellowgreen">2055</font>
- 2022年: ★3／diff <font color="yellowgreen">2236</font>

### レベル別問題一覧

「約数の走査を倍数の走査に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2552">No.2552 Not Coprime, Not Divisor</a> (MMA Contest 017 (2023-11-25) - F問題、diff <font color="yellowgreen">2235</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題、diff <font color="blue">1983</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="再帰">225. 再帰</h2>

### 難易度統計

「再帰」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2193</font>
- 2024年: ★2.8／diff <font color="orange">2460</font>
- 2023年: ★2.9／diff <font color="blue">1913</font>
- 2022年: ★3／diff <font color="orange">2491</font>

### レベル別問題一覧

「再帰」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2518">No.2518 Adjacent Larger</a> (yukicoder contest 410 (2023-10-27) - D問題、diff <font color="deepskyblue">1488</font>)
- <a href="https://yukicoder.me/problems/no/2610">No.2610 Decreasing LCMs</a> (yukicoder contest 415 (2024-01-19) - D問題、diff <font color="yellowgreen">2129</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題、diff <font color="blue">1971</font>)
- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題、diff <font color="orange">2737</font>)
- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="座標圧縮">226. 座標圧縮</h2>

### 難易度統計

「座標圧縮」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2258</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.9／diff <font color="yellowgreen">2303</font>
- 2022年: ★3／diff <font color="yellowgreen">2145</font>

### レベル別問題一覧

「座標圧縮」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2434">No.2434 RAKUTAN de RAKUTAN</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - K問題、diff <font color="orange">2721</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)

　
<h2 id="閉路と残りに分割">227. 閉路と残りに分割</h2>

### 難易度統計

「閉路と残りに分割」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1725</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1725</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「閉路と残りに分割」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2301">No.2301 Namorientation</a> (yukicoder contest 388 (2023-05-12) - E問題、diff <font color="deepskyblue">1499</font>)
- <a href="https://yukicoder.me/problems/no/2531">No.2531 Coloring Vertices on Namori</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - G問題、diff <font color="blue">1951</font>)

　
<h2 id="閉路検出">228. 閉路検出</h2>

### 難易度統計

「閉路検出」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1725</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1725</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「閉路検出」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2301">No.2301 Namorientation</a> (yukicoder contest 388 (2023-05-12) - E問題、diff <font color="deepskyblue">1499</font>)
- <a href="https://yukicoder.me/problems/no/2531">No.2531 Coloring Vertices on Namori</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - G問題、diff <font color="blue">1951</font>)

　
<h2 id="クエリソート">229. クエリソート</h2>

### 難易度統計

「クエリソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1872</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="blue">1872</font>

### レベル別問題一覧

「クエリソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)

　
<h2 id="偏角ソート">230. 偏角ソート</h2>

### 難易度統計

「偏角ソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1919</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1919</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「偏角ソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)

　
<h2 id="mex取得">231. mex取得</h2>

### 難易度統計

「mex取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1927</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1927</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「mex取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)

　
<h2 id="スライド最小化">232. スライド最小化</h2>

### 難易度統計

「スライド最小化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1959</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「スライド最小化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)

　
<h2 id="正弦定理">233. 正弦定理</h2>

### 難易度統計

「正弦定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1961</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1961</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「正弦定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2555">No.2555 Intriguing Triangle</a> (Advent Calendar Contest 2023 (2023-12-01) - A問題、diff <font color="blue">1961</font>)

　
<h2 id="inplace DP">234. inplace DP</h2>

### 難易度統計

「inplace DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1985</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1526</font>
- 2022年: ★4／diff <font color="red">2903</font>

### レベル別問題一覧

「inplace DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="区間スケジューリング">235. 区間スケジューリング</h2>

### 難易度統計

「区間スケジューリング」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1985</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1985</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間スケジューリング」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)

　
<h2 id="２次元累積和">236. ２次元累積和</h2>

### 難易度統計

「２次元累積和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1998</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1998</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「２次元累積和」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)

　
<h2 id="矩形和取得">237. 矩形和取得</h2>

### 難易度統計

「矩形和取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1998</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="blue">1998</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「矩形和取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)

　
<h2 id="小さいケースの構築を拡張">238. 小さいケースの構築を拡張</h2>

### 難易度統計

「小さいケースの構築を拡張」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2042</font>
- 2024年: ★2.5／diff <font color="blue">1784</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="yellowgreen">2300</font>

### レベル別問題一覧

「小さいケースの構築を拡張」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2614">No.2614 Delete ABC</a> (yukicoder contest 416 (2024-01-26) - A問題、diff <font color="gray">365</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題、diff <font color="yellowgreen">2039</font>)
- <a href="https://yukicoder.me/problems/no/2610">No.2610 Decreasing LCMs</a> (yukicoder contest 415 (2024-01-19) - D問題、diff <font color="yellowgreen">2129</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2143">No.2143 Only One Bracket</a> (yukicoder contest 370 (2022-12-02) - D問題、diff <font color="blue">1606</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2151">No.2151 3 on Torus-Lohkous</a> (Advent Calendar Contest 2022 (2022-12-01) - H問題、diff <font color="darkgoldenrod ">3257</font>)

　
<h2 id="平方剰余">239. 平方剰余</h2>

### 難易度統計

「平方剰余」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2047</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「平方剰余」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)

　
<h2 id="最小費用流計算">240. 最小費用流計算</h2>

### 難易度統計

「最小費用流計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2048</font>
- 2024年: ★3／diff <font color="yellowgreen">2048</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最小費用流計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2604">No.2604 Initial Motion</a> (yukicoder contest 414 (2024-01-12) - F問題、diff <font color="yellowgreen">2048</font>)

　
<h2 id="ループ戦略">241. ループ戦略</h2>

### 難易度統計

「ループ戦略」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2051</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2051</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ループ戦略」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題、diff <font color="blue">1933</font>)
- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)

　
<h2 id="レベル祖先計算">242. レベル祖先計算</h2>

### 難易度統計

「レベル祖先計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2056</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2056</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「レベル祖先計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)

　
<h2 id="弾性衝突を通過に翻訳して位置関係から復元">243. 弾性衝突を通過に翻訳して位置関係から復元</h2>

### 難易度統計

「弾性衝突を通過に翻訳して位置関係から復元」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2056</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2056</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「弾性衝突を通過に翻訳して位置関係から復元」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2482">No.2482 Sandglasses</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - D問題、diff <font color="yellowgreen">2056</font>)

　
<h2 id="木の頂点の重さ計算">244. 木の頂点の重さ計算</h2>

### 難易度統計

「木の頂点の重さ計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2056</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2056</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「木の頂点の重さ計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)

　
<h2 id="区間最大・最小値取得">245. 区間最大・最小値取得</h2>

### 難易度統計

「区間最大・最小値取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2064</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2169</font>
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「区間最大・最小値取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)

　
<h2 id="経路復元">246. 経路復元</h2>

### 難易度統計

「経路復元」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2068</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2068</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「経路復元」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)

　
<h2 id="始点と終点からの経路計算">247. 始点と終点からの経路計算</h2>

### 難易度統計

「始点と終点からの経路計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2068</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2068</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「始点と終点からの経路計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)

　
<h2 id="行列累乗">248. 行列累乗</h2>

### 難易度統計

「行列累乗」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2074</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2359</font>
- 2022年: ★3／diff <font color="deepskyblue">1220</font>

### レベル別問題一覧

「行列累乗」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="区間の分割の数え上げを切片の分割に帰着">249. 区間の分割の数え上げを切片の分割に帰着</h2>

### 難易度統計

「区間の分割の数え上げを切片の分割に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2097</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2097</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間の分割の数え上げを切片の分割に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)

　
<h2 id="ダブリング">250. ダブリング</h2>

### 難易度統計

「ダブリング」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2105</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2105</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ダブリング」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題、diff <font color="yellowgreen">2274</font>)
- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)
- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)

　
<h2 id="総和計算の期待値への帰着">251. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着">総和計算の期待値への帰着</a></h2>

### 難易度統計

「[総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2119</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.6／diff <font color="blue">1971</font>
- 2022年: ★4／diff <font color="orange">2566</font>

### レベル別問題一覧

「[総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題、diff <font color="orange">2566</font>)

　
<h2 id="最適遷移の写像化">252. 最適遷移の写像化</h2>

### 難易度統計

「最適遷移の写像化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2129</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2129</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最適遷移の写像化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題、diff <font color="yellowgreen">2274</font>)
- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)

　
<h2 id="２次元imos法">253. ２次元imos法</h2>

### 難易度統計

「２次元imos法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2141</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2141</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「２次元imos法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)

　
<h2 id="矩形加算更新">254. 矩形加算更新</h2>

### 難易度統計

「矩形加算更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2141</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2141</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「矩形加算更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)

　
<h2 id="ユークリッドの互除法">255. ユークリッドの互除法</h2>

### 難易度統計

「ユークリッドの互除法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2143</font>
- 2024年: ★2／diff <font color="deepskyblue">1208</font>
- 2023年: ★3.2／diff <font color="yellowgreen">2204</font>
- 2022年: ★3.1／diff <font color="yellowgreen">2316</font>

### レベル別問題一覧

「ユークリッドの互除法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)
- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題、diff <font color="yellowgreen">2139</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="ファンデルモンドの畳み込み">256. ファンデルモンドの畳み込み</h2>

### 難易度統計

「ファンデルモンドの畳み込み」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2143</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ファンデルモンドの畳み込み」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="外積">257. 外積</h2>

### 難易度統計

「外積」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2147</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2147</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「外積」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)

　
<h2 id="区間の重複度計算">258. 区間の重複度計算</h2>

### 難易度統計

「区間の重複度計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2155</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1661</font>
- 2022年: ★3.5／diff <font color="orange">2649</font>

### レベル別問題一覧

「区間の重複度計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

　
<h2 id="グリッド上の価値最大化">259. グリッド上の価値最大化</h2>

### 難易度統計

「グリッド上の価値最大化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2169</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2169</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「グリッド上の価値最大化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)

　
<h2 id="コーシー・フロベニウスの補題">260. コーシー・フロベニウスの補題</h2>

### 難易度統計

「コーシー・フロベニウスの補題」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2183</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2183</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「コーシー・フロベニウスの補題」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2383">No.2383 Naphthol</a> (yukicoder contest 397(群論コンテスト) (2023-07-14) - E問題、diff <font color="yellowgreen">2183</font>)

　
<h2 id="二面体群">261. 二面体群</h2>

### 難易度統計

「二面体群」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2183</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2183</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「二面体群」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2383">No.2383 Naphthol</a> (yukicoder contest 397(群論コンテスト) (2023-07-14) - E問題、diff <font color="yellowgreen">2183</font>)

　
<h2 id="反射の倍化実装">262. 反射の倍化実装</h2>

### 難易度統計

「反射の倍化実装」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2191</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2191</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「反射の倍化実装」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

　
<h2 id="解法場合分け">263. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け">解法場合分け</a></h2>

### 難易度統計

「[解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2201</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2176</font>
- 2022年: ★3／diff <font color="yellowgreen">2227</font>

### レベル別問題一覧

「[解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題、diff <font color="blue">1641</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2366">No.2366 登校</a> (yukicoder contest 395 (2023-06-30) - C問題、diff <font color="yellowgreen">2294</font>)
- <a href="https://yukicoder.me/problems/no/2519">No.2519 Coins in Array</a> (yukicoder contest 410 (2023-10-27) - E問題、diff <font color="yellowgreen">2069</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="フロー">264. フロー</h2>

### 難易度統計

「フロー」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2234</font>
- 2024年: ★3／diff <font color="yellowgreen">2048</font>
- 2023年: ★3／diff <font color="orange">2420</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「フロー」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2263">No.2263 Perms</a> (yukicoder contest 383 (2023-04-07) - E問題、diff <font color="orange">2420</font>)
- <a href="https://yukicoder.me/problems/no/2604">No.2604 Initial Motion</a> (yukicoder contest 414 (2024-01-12) - F問題、diff <font color="yellowgreen">2048</font>)

　
<h2 id="データ構造初期化">265. データ構造初期化</h2>

### 難易度統計

「データ構造初期化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2237</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2237</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「データ構造初期化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="一対一対応と乱択の可換性">266. 一対一対応と乱択の可換性</h2>

### 難易度統計

「一対一対応と乱択の可換性」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2237</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2237</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「一対一対応と乱択の可換性」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="bitset高速化">267. bitset高速化</h2>

### 難易度統計

「bitset高速化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2245</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2245</font>

### レベル別問題一覧

「bitset高速化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

　
<h2 id="基底計算">268. 基底計算</h2>

### 難易度統計

「基底計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2245</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2245</font>

### レベル別問題一覧

「基底計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

　
<h2 id="無向木の有向化">269. 無向木の有向化</h2>

### 難易度統計

「無向木の有向化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2249</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2249</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「無向木の有向化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題、diff <font color="blue">1661</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2584">No.2584 The University of Tree</a> (Advent Calendar Contest 2023 (2023-12-01) - L問題、diff <font color="red">2960</font>)

　
<h2 id="内積の畳み込み計算">270. 内積の畳み込み計算</h2>

### 難易度統計

「内積の畳み込み計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2258</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2258</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「内積の畳み込み計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題、diff <font color="yellowgreen">2258</font>)

　
<h2 id="floor_sum">271. floor_sum</h2>

### 難易度統計

「floor_sum」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2269</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1891</font>
- 2022年: ★3.5／diff <font color="orange">2648</font>

### レベル別問題一覧

「floor_sum」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="行列式と面積・体積の関係">272. 行列式と面積・体積の関係</h2>

### 難易度統計

「行列式と面積・体積の関係」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2284</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2284</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「行列式と面積・体積の関係」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)

　
<h2 id="ベルトラン・チェビシェフの定理">273. ベルトラン・チェビシェフの定理</h2>

### 難易度統計

「ベルトラン・チェビシェフの定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2309</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2309</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ベルトラン・チェビシェフの定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2496">No.2496 LCM between Permutations</a> (yukicoder contest 407 (2023-10-06) - E問題、diff <font color="yellowgreen">2309</font>)

　
<h2 id="素数に注目する質問">274. 素数に注目する質問</h2>

### 難易度統計

「素数に注目する質問」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2309</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2309</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素数に注目する質問」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2496">No.2496 LCM between Permutations</a> (yukicoder contest 407 (2023-10-06) - E問題、diff <font color="yellowgreen">2309</font>)

　
<h2 id="対角線に言及する質問">275. 対角線に言及する質問</h2>

### 難易度統計

「対角線に言及する質問」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2309</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2309</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「対角線に言及する質問」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2496">No.2496 LCM between Permutations</a> (yukicoder contest 407 (2023-10-06) - E問題、diff <font color="yellowgreen">2309</font>)

　
<h2 id="bit全探索">276. bit全探索</h2>

### 難易度統計

「bit全探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2344</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2344</font>

### レベル別問題一覧

「bit全探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)

　
<h2 id="余因子展開">277. 余因子展開</h2>

### 難易度統計

「余因子展開」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2344</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2344</font>

### レベル別問題一覧

「余因子展開」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)

　
<h2 id="一対一対応">278. 一対一対応</h2>

### 難易度統計

「一対一対応」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2385</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.1／diff <font color="orange">2540</font>
- 2022年: ★2.7／diff <font color="yellowgreen">2151</font>

### レベル別問題一覧

「一対一対応」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2474">No.2474 Empty Quartz</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - H問題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)
- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="SIMD高速化">279. SIMD高速化</h2>

### 難易度統計

「SIMD高速化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2386</font>
- 2024年: ★3／diff <font color="yellowgreen">2386</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「SIMD高速化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="平均の指定された区間数え上げ">280. 平均の指定された区間数え上げ</h2>

### 難易度統計

「平均の指定された区間数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2386</font>
- 2024年: ★3／diff <font color="yellowgreen">2386</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「平均の指定された区間数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="剰余を商に翻訳">281. 剰余を商に翻訳</h2>

### 難易度統計

「剰余を商に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2393</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2393</font>

### レベル別問題一覧

「剰余を商に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)

　
<h2 id="緩和">282. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和">緩和</a></h2>

### 難易度統計

「[緩和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2394</font>
- 2024年: ★3／diff <font color="orange">2585</font>
- 2023年: ★3.1／diff <font color="orange">2473</font>
- 2022年: ★3／diff <font color="yellowgreen">2252</font>

### レベル別問題一覧

「[緩和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="外接円計算">283. 外接円計算</h2>

### 難易度統計

「外接円計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2419</font>
- 2024年: ★3／diff <font color="orange">2419</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「外接円計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

　
<h2 id="第二余弦定理">284. 第二余弦定理</h2>

### 難易度統計

「第二余弦定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2419</font>
- 2024年: ★3／diff <font color="orange">2419</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「第二余弦定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

　
<h2 id="有理数の大小比較のオーバーフロー回避">285. 有理数の大小比較のオーバーフロー回避</h2>

### 難易度統計

「有理数の大小比較のオーバーフロー回避」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2419</font>
- 2024年: ★3／diff <font color="orange">2419</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「有理数の大小比較のオーバーフロー回避」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

　
<h2 id="連分数展開">286. 連分数展開</h2>

### 難易度統計

「連分数展開」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2419</font>
- 2024年: ★3／diff <font color="orange">2419</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「連分数展開」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

　
<h2 id="完全二部マッチング">287. 完全二部マッチング</h2>

### 難易度統計

「完全二部マッチング」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2420</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="orange">2420</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「完全二部マッチング」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2263">No.2263 Perms</a> (yukicoder contest 383 (2023-04-07) - E問題、diff <font color="orange">2420</font>)

　
<h2 id="十分大きな法">288. 十分大きな法</h2>

### 難易度統計

「十分大きな法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2429</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="orange">2429</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「十分大きな法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)

　
<h2 id="ローリングハッシュ">289. ローリングハッシュ</h2>

### 難易度統計

「ローリングハッシュ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2454</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="yellowgreen">2030</font>
- 2022年: ★3.5／diff <font color="red">2877</font>

### レベル別問題一覧

「ローリングハッシュ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題、diff <font color="red">2852</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="単調関数の像計算を階差の非零点の数え上げに帰着">290. 単調関数の像計算を階差の非零点の数え上げに帰着</h2>

### 難易度統計

「単調関数の像計算を階差の非零点の数え上げに帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2471</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="orange">2471</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「単調関数の像計算を階差の非零点の数え上げに帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題、diff <font color="orange">2471</font>)

　
<h2 id="区間削除更新">291. 区間削除更新</h2>

### 難易度統計

「区間削除更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2489</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="orange">2489</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間削除更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)

　
<h2 id="区間挿入更新">292. 区間挿入更新</h2>

### 難易度統計

「区間挿入更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2489</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="orange">2489</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間挿入更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)

　
<h2 id="自己写像に翻訳">293. 自己写像に翻訳</h2>

### 難易度統計

「自己写像に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2501</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="orange">2501</font>

### レベル別問題一覧

「自己写像に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2082">No.2082 AND OR XOR</a> (yukicoder contest 361 (2022-09-25) - E問題、diff <font color="orange">2501</font>)

　
<h2 id="bit高速化">294. bit高速化</h2>

### 難易度統計

「bit高速化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2521</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="orange">2521</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「bit高速化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2423">No.2423 Merge Stones</a> (MMA Contest 016 (2023-08-12) - J問題、diff <font color="orange">2521</font>)

　
<h2 id="セグメント木">295. セグメント木</h2>

### 難易度統計

「セグメント木」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2604</font>
- 2024年: ★3／diff <font color="orange">2604</font>
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「セグメント木」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2611">No.2611 Count 01</a> (yukicoder contest 415 (2024-01-19) - E問題、diff <font color="orange">2604</font>)

　
<h2 id="区間の部分列をわたる総和計算をモノイド演算に翻訳">296. 区間の部分列をわたる総和計算をモノイド演算に翻訳</h2>

### 難易度統計

「区間の部分列をわたる総和計算をモノイド演算に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2604</font>
- 2024年: ★3／diff <font color="orange">2604</font>
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間の部分列をわたる総和計算をモノイド演算に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2611">No.2611 Count 01</a> (yukicoder contest 415 (2024-01-19) - E問題、diff <font color="orange">2604</font>)

　
<h2 id="準同型">297. 準同型</h2>

### 難易度統計

「準同型」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2656</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="red">3018</font>
- 2022年: ★3／diff <font color="yellowgreen">2295</font>

### レベル別問題一覧

「準同型」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

　
<h2 id="最小被覆半径計算">298. 最小被覆半径計算</h2>

### 難易度統計

「最小被覆半径計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="red">2833</font>
- 2024年: ★3／diff <font color="red">2833</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最小被覆半径計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)

　
<h2 id="タイリングによるミラー戦略">299. タイリングによるミラー戦略</h2>

### 難易度統計

「タイリングによるミラー戦略」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diffデータなし
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「タイリングによるミラー戦略」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2476">No.2476 Knight Game</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - J問題、diffデータなし)

　
<h2 id="数え上げを総和計算に帰着">300. 数え上げを総和計算に帰着</h2>

### 難易度統計

「数え上げを総和計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diffデータなし
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「数え上げを総和計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)

　
<h2 id="辺を頂点とするグラフに翻訳">301. 辺を頂点とするグラフに翻訳</h2>

### 難易度統計

「辺を頂点とするグラフに翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diffデータなし
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「辺を頂点とするグラフに翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)

　
<h2 id="B進法">302. B進法</h2>

### 難易度統計

「B進法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2131</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="blue">1799</font>
- 2022年: ★3.6／diff <font color="orange">2529</font>

### レベル別問題一覧

「B進法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題、diff <font color="blue">1989</font>)
- <a href="https://yukicoder.me/problems/no/2410">No.2410 Nine Numbers</a> (yukicoder contest 401 (2023-08-11) - D問題、diff <font color="deepskyblue">1318</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2198">No.2198 Concon Substrings (COuNt-CONstruct Version)</a> (yukicoder contest 374 (2023-01-20) - E問題、diff <font color="yellowgreen">2050</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)
- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題、diff <font color="orange">2500</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)
- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="制約からグラフの種類を特定">303. 制約からグラフの種類を特定</h2>

### 難易度統計

「制約からグラフの種類を特定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2166</font>
- 2024年: ★3／diff <font color="yellowgreen">2255</font>
- 2023年: ★3.1／diff <font color="yellowgreen">2136</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「制約からグラフの種類を特定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2301">No.2301 Namorientation</a> (yukicoder contest 388 (2023-05-12) - E問題、diff <font color="deepskyblue">1499</font>)
- <a href="https://yukicoder.me/problems/no/2531">No.2531 Coloring Vertices on Namori</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - G問題、diff <font color="blue">1951</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2618">No.2618 除霊</a> (yukicoder contest 416 (2024-01-26) - E問題、diff <font color="yellowgreen">2255</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2584">No.2584 The University of Tree</a> (Advent Calendar Contest 2023 (2023-12-01) - L問題、diff <font color="red">2960</font>)

　
<h2 id="始切片の数え上げを桁ごとの計算に帰着">304. 始切片の数え上げを桁ごとの計算に帰着</h2>

### 難易度統計

「始切片の数え上げを桁ごとの計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2171</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.1／diff <font color="yellowgreen">2171</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「始切片の数え上げを桁ごとの計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2246">No.2246 1333-like Number</a> (yukicoder contest 381 (2023-03-17) - A問題、diff <font color="brown">689</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2455">No.2455 Numbers Dictionary</a> (yukicoder contest 403 (2023-09-01) - F問題、diff <font color="yellowgreen">2213</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="DPのデータ構造高速化">305. DPのデータ構造高速化</h2>

### 難易度統計

「DPのデータ構造高速化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2186</font>
- 2024年: ★3／diff <font color="blue">1654</font>
- 2023年: ★3／diff <font color="yellowgreen">2121</font>
- 2022年: ★3.3／diff <font color="yellowgreen">2332</font>

### レベル別問題一覧

「DPのデータ構造高速化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題、diff <font color="orange">2758</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2625">No.2625 Bouns Ai</a> (yukicoder contest 417 (2024-02-09) - E問題、diff <font color="blue">1654</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="確率漸化式">306. 確率漸化式</h2>

### 難易度統計

「確率漸化式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2186</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.1／diff <font color="yellowgreen">2186</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「確率漸化式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

　
<h2 id="期待値の線形性">307. 期待値の線形性</h2>

### 難易度統計

「期待値の線形性」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2234</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2168</font>
- 2022年: ★4／diff <font color="orange">2566</font>

### レベル別問題一覧

「期待値の線形性」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題、diff <font color="orange">2566</font>)

　
<h2 id="周期的構築">308. 周期的構築</h2>

### 難易度統計

「周期的構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2287</font>
- 2024年: ★3.5／diff <font color="red">2860</font>
- 2023年: ★3／diff <font color="yellowgreen">2000</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「周期的構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題、diff <font color="blue">1933</font>)
- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="平方分割">309. 平方分割</h2>

### 難易度統計

「平方分割」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2313</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.2／diff <font color="yellowgreen">2273</font>
- 2022年: ★3／diff <font color="yellowgreen">2393</font>

### レベル別問題一覧

「平方分割」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題、diff <font color="yellowgreen">2381</font>)

　
<h2 id="互いに素に帰着">310. 互いに素に帰着</h2>

### 難易度統計

「互いに素に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2375</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.1／diff <font color="yellowgreen">2375</font>

### レベル別問題一覧

「互いに素に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="ゼータ変換">311. ゼータ変換</h2>

### 難易度統計

「ゼータ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="orange">2431</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.1／diff <font color="orange">2473</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「ゼータ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="メビウス変換">312. メビウス変換</h2>

### 難易度統計

「メビウス変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="orange">2431</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.1／diff <font color="orange">2473</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「メビウス変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="最長共通接頭辞計算">313. 最長共通接頭辞計算</h2>

### 難易度統計

「最長共通接頭辞計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="orange">2534</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1849</font>
- 2022年: ★3.5／diff <font color="red">2877</font>

### レベル別問題一覧

「最長共通接頭辞計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2454">No.2454 Former < Latter</a> (yukicoder contest 403 (2023-09-01) - E問題、diff <font color="blue">1849</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題、diff <font color="red">2852</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="積和の和積化">314. 積和の和積化</h2>

### 難易度統計

「積和の和積化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2307</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.2／diff <font color="yellowgreen">2307</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「積和の和積化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2582">No.2582 Random Average^K</a> (Advent Calendar Contest 2023 (2023-12-01) - J問題、diff <font color="orange">2401</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="フロベニウス数に注目">315. フロベニウス数に注目</h2>

### 難易度統計

「フロベニウス数に注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2358</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2069</font>
- 2022年: ★3.5／diff <font color="orange">2648</font>

### レベル別問題一覧

「フロベニウス数に注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2519">No.2519 Coins in Array</a> (yukicoder contest 410 (2023-10-27) - E問題、diff <font color="yellowgreen">2069</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="調和数列">316. 調和数列</h2>

### 難易度統計

「調和数列」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2383</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2039</font>
- 2022年: ★3.7／diff <font color="orange">2728</font>

### レベル別問題一覧

「調和数列」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題、diff <font color="orange">2471</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="ベン図">317. ベン図</h2>

### 難易度統計

「ベン図」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="orange">2447</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.2／diff <font color="orange">2447</font>

### レベル別問題一覧

「ベン図」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

　
<h2 id="階数計算">318. 階数計算</h2>

### 難易度統計

「階数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="orange">2493</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2741</font>
- 2022年: ★3／diff <font color="yellowgreen">2245</font>

### レベル別問題一覧

「階数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2405">No.2405 Minimal Matrix Decomposition</a> (yukicoder contest 400 (2023-08-04) - G問題、diff <font color="orange">2741</font>)

　
<h2 id="行列の簡約階段化">319. 行列の簡約階段化</h2>

### 難易度統計

「行列の簡約階段化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="orange">2493</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2741</font>
- 2022年: ★3／diff <font color="yellowgreen">2245</font>

### レベル別問題一覧

「行列の簡約階段化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2405">No.2405 Minimal Matrix Decomposition</a> (yukicoder contest 400 (2023-08-04) - G問題、diff <font color="orange">2741</font>)

　
<h2 id="全方位木DP">320. 全方位木DP</h2>

### 難易度統計

「全方位木DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="orange">2641</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.2／diff <font color="orange">2641</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「全方位木DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2584">No.2584 The University of Tree</a> (Advent Calendar Contest 2023 (2023-12-01) - L問題、diff <font color="red">2960</font>)

　
<h2 id="既出を検索">321. 既出を検索</h2>

### 難易度統計

「既出を検索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="red">2860</font>
- 2024年: ★3.5／diff <font color="red">2860</font>
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「既出を検索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2476">No.2476 Knight Game</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - J問題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="十分大きな法で計算">322. 十分大きな法で計算</h2>

### 難易度統計

「十分大きな法で計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="yellowgreen">2290</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2412</font>
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「十分大きな法で計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題、diff <font color="yellowgreen">2258</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="２進法">323. ２進法</h2>

### 難易度統計

「２進法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="yellowgreen">2308</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1531</font>
- 2023年: ★3／diff <font color="yellowgreen">2175</font>
- 2022年: ★3.6／diff <font color="orange">2536</font>

### レベル別問題一覧

「２進法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2609">No.2609 Decreasing GCDs</a> (yukicoder contest 415 (2024-01-19) - C問題、diff <font color="deepskyblue">1531</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題、diff <font color="yellowgreen">2175</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)

　
<h2 id="剰余による確率的判定">324. 剰余による確率的判定</h2>

### 難易度統計

「剰余による確率的判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="yellowgreen">2347</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2498</font>
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「剰余による確率的判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="マージ">325. マージ</h2>

### 難易度統計

「マージ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="orange">2631</font>
- 2024年: ★3／diff <font color="orange">2604</font>
- 2023年: ★3.5／diff <font color="orange">2658</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「マージ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2611">No.2611 Count 01</a> (yukicoder contest 415 (2024-01-19) - E問題、diff <font color="orange">2604</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題、diff <font color="orange">2658</font>)

　
<h2 id="区間を中間で分割してマージ">326. 区間を中間で分割してマージ</h2>

### 難易度統計

「区間を中間で分割してマージ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="orange">2631</font>
- 2024年: ★3／diff <font color="orange">2604</font>
- 2023年: ★3.5／diff <font color="orange">2658</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間を中間で分割してマージ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2611">No.2611 Count 01</a> (yukicoder contest 415 (2024-01-19) - E問題、diff <font color="orange">2604</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題、diff <font color="orange">2658</font>)

　
<h2 id="多倍長整数">327. 多倍長整数</h2>

### 難易度統計

「多倍長整数」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="orange">2686</font>
- 2024年: ★3／diff <font color="orange">2419</font>
- 2023年: ★3.5／diff <font color="red">2819</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「多倍長整数」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="約数メビウス変換">328. 約数メビウス変換</h2>

### 難易度統計

「約数メビウス変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="orange">2706</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="red">2906</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「約数メビウス変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="同値関係">329. 同値関係</h2>

### 難易度統計

「同値関係」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.4／diff <font color="orange">2549</font>
- 2024年: ★3.5／diff <font color="red">2860</font>
- 2023年: ★2／diff <font color="blue">1612</font>
- 2022年: ★3.8／diff <font color="orange">2758</font>

### レベル別問題一覧

「同値関係」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2449">No.2449 square_permutation</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)
- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="シュトルツ・チェザロの定理">330. シュトルツ・チェザロの定理</h2>

### 難易度統計

「シュトルツ・チェザロの定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="yellowgreen">2348</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="yellowgreen">2348</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「シュトルツ・チェザロの定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

　
<h2 id="移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着">331. 移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着</h2>

### 難易度統計

「移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="yellowgreen">2348</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="yellowgreen">2348</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

　
<h2 id="整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着">332. 整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着</h2>

### 難易度統計

「整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="yellowgreen">2348</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="yellowgreen">2348</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

　
<h2 id="Moのアルゴリズム">333. Moのアルゴリズム</h2>

### 難易度統計

「Moのアルゴリズム」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="yellowgreen">2381</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="yellowgreen">2381</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Moのアルゴリズム」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題、diff <font color="yellowgreen">2381</font>)

　
<h2 id="線形代数">334. 線形代数</h2>

### 難易度統計

「線形代数」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2400</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.7／diff <font color="orange">2632</font>
- 2022年: ★3／diff <font color="blue">1936</font>

### レベル別問題一覧

「線形代数」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2405">No.2405 Minimal Matrix Decomposition</a> (yukicoder contest 400 (2023-08-04) - G問題、diff <font color="orange">2741</font>)
- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)
- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="テイラー展開">335. テイラー展開</h2>

### 難易度統計

「テイラー展開」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2401</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2401</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「テイラー展開」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2582">No.2582 Random Average^K</a> (Advent Calendar Contest 2023 (2023-12-01) - J問題、diff <font color="orange">2401</font>)

　
<h2 id="フビニの定理">336. フビニの定理</h2>

### 難易度統計

「フビニの定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2401</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2401</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「フビニの定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2582">No.2582 Random Average^K</a> (Advent Calendar Contest 2023 (2023-12-01) - J問題、diff <font color="orange">2401</font>)

　
<h2 id="積分漸化式">337. 積分漸化式</h2>

### 難易度統計

「積分漸化式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2401</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2401</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「積分漸化式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2582">No.2582 Random Average^K</a> (Advent Calendar Contest 2023 (2023-12-01) - J問題、diff <font color="orange">2401</font>)

　
<h2 id="ポラードの$\rho$">338. ポラードの$\rho$</h2>

### 難易度統計

「ポラードの$\rho$」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2421</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4／diff <font color="orange">2795</font>
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「ポラードの$\rho$」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="期待値漸化式">339. 期待値漸化式</h2>

### 難易度統計

「期待値漸化式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2423</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2423</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「期待値漸化式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題、diffデータなし)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2389">No.2389 Cheating Code Golf</a> (yukicoder contest 398 (2023-07-21) - E問題、diff <font color="orange">2451</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)

　
<h2 id="osa_k法">340. osa_k法</h2>

### 難易度統計

「osa_k法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2436</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4／diff <font color="orange">2567</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「osa_k法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="交代和">341. 交代和</h2>

### 難易度統計

「交代和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2500</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="orange">2500</font>

### レベル別問題一覧

「交代和」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題、diff <font color="orange">2500</font>)

　
<h2 id="メビウスの反転公式">342. メビウスの反転公式</h2>

### 難易度統計

「メビウスの反転公式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2550</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4／diff <font color="orange">2795</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「メビウスの反転公式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="冪乗との最大公約数の収束">343. 冪乗との最大公約数の収束</h2>

### 難易度統計

「冪乗との最大公約数の収束」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2587</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2587</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「冪乗との最大公約数の収束」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="第二種スターリング数計算">344. 第二種スターリング数計算</h2>

### 難易度統計

「第二種スターリング数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2643</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="orange">2643</font>

### レベル別問題一覧

「第二種スターリング数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)

　
<h2 id="カタラン数計算">345. カタラン数計算</h2>

### 難易度統計

「カタラン数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2649</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="orange">2649</font>

### レベル別問題一覧

「カタラン数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

　
<h2 id="01BFS">346. 01BFS</h2>

### 難易度統計

「01BFS」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2690</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="orange">2690</font>

### レベル別問題一覧

「01BFS」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2096">No.2096 Rage With Our Friends</a> (yukicoder contest 363 (2022-10-07) - E問題、diff <font color="orange">2690</font>)

　
<h2 id="階数因数分解">347. 階数因数分解</h2>

### 難易度統計

「階数因数分解」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2741</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="orange">2741</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「階数因数分解」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2405">No.2405 Minimal Matrix Decomposition</a> (yukicoder contest 400 (2023-08-04) - G問題、diff <font color="orange">2741</font>)

　
<h2 id="タイリング可能性を領域の細分による不変量計算に帰着">348. タイリング可能性を領域の細分による不変量計算に帰着</h2>

### 難易度統計

「タイリング可能性を領域の細分による不変量計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="red">2860</font>
- 2024年: ★3.5／diff <font color="red">2860</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「タイリング可能性を領域の細分による不変量計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="約数ゼータ変換">349. 約数ゼータ変換</h2>

### 難易度統計

「約数ゼータ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="red">2906</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="red">2906</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「約数ゼータ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="cyclic orderつき全方位木DP">350. cyclic orderつき全方位木DP</h2>

### 難易度統計

「cyclic orderつき全方位木DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="red">2960</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="red">2960</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「cyclic orderつき全方位木DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2584">No.2584 The University of Tree</a> (Advent Calendar Contest 2023 (2023-12-01) - L問題、diff <font color="red">2960</font>)

　
<h2 id="行列式計算">351. 行列式計算</h2>

### 難易度統計

「行列式計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.6／diff <font color="orange">2474</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4／diff <font color="orange">2539</font>
- 2022年: ★3／diff <font color="yellowgreen">2344</font>

### レベル別問題一覧

「行列式計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="桁DP">352. 桁DP</h2>

### 難易度統計

「桁DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.6／diff <font color="orange">2762</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.7／diff <font color="orange">2792</font>
- 2022年: ★3.5／diff <font color="orange">2722</font>

### レベル別問題一覧

「桁DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題、diff <font color="orange">2737</font>)
- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)
- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2159">No.2159 Filling 4x4 array</a> (Advent Calendar Contest 2022 (2022-12-01) - J問題、diff <font color="darkgoldenrod ">3382</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="有向辺反転">353. 有向辺反転</h2>

### 難易度統計

「有向辺反転」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.7／diff <font color="yellowgreen">2383</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1385</font>
- 2022年: ★5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「有向辺反転」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2569">No.2569 はじめてのおつかいHard</a> (緑以下コンテスト  Extra (2023-12-02) - A問題、diff <font color="deepskyblue">1385</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="最近共通祖先計算">354. 最近共通祖先計算</h2>

### 難易度統計

「最近共通祖先計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.7／diff <font color="orange">2719</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2056</font>
- 2022年: ★4.5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「最近共通祖先計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="ヤング図形">355. ヤング図形</h2>

### 難易度統計

「ヤング図形」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.8／diff <font color="yellowgreen">2095</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★3.2／diff <font color="blue">1746</font>

### レベル別問題一覧

「ヤング図形」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題、diff <font color="brown">406</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)
- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="剰余の定理">356. 剰余の定理</h2>

### 難易度統計

「剰余の定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.8／diff <font color="orange">2737</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.8／diff <font color="orange">2737</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「剰余の定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)

　
<h2 id="行列の階段化">357. 行列の階段化</h2>

### 難易度統計

「行列の階段化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.8／diff <font color="red">2829</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.2／diff <font color="red">3122</font>
- 2022年: ★3／diff <font color="yellowgreen">2245</font>

### レベル別問題一覧

「行列の階段化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2405">No.2405 Minimal Matrix Decomposition</a> (yukicoder contest 400 (2023-08-04) - G問題、diff <font color="orange">2741</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="掃き出し法">358. 掃き出し法</h2>

### 難易度統計

「掃き出し法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.8／diff <font color="red">2829</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.2／diff <font color="red">3122</font>
- 2022年: ★3／diff <font color="yellowgreen">2245</font>

### レベル別問題一覧

「掃き出し法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2405">No.2405 Minimal Matrix Decomposition</a> (yukicoder contest 400 (2023-08-04) - G問題、diff <font color="orange">2741</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="キュー">359. キュー</h2>

### 難易度統計

「キュー」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4／diff <font color="orange">2658</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4／diff <font color="orange">2658</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「キュー」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題、diff <font color="orange">2658</font>)

　
<h2 id="リュカの定理">360. リュカの定理</h2>

### 難易度統計

「リュカの定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4／diff <font color="orange">2768</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4／diff <font color="orange">2768</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「リュカの定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2344">No.2344 (l+r)^2</a> (yukicoder contest 392 (2023-06-09) - B問題、diff <font color="orange">2768</font>)

　
<h2 id="小さい法に帰着させる再帰">361. 小さい法に帰着させる再帰</h2>

### 難易度統計

「小さい法に帰着させる再帰」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4／diff <font color="orange">2768</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4／diff <font color="orange">2768</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「小さい法に帰着させる再帰」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2344">No.2344 (l+r)^2</a> (yukicoder contest 392 (2023-06-09) - B問題、diff <font color="orange">2768</font>)

　
<h2 id="高速ゼータ変換">362. 高速ゼータ変換</h2>

### 難易度統計

「高速ゼータ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「高速ゼータ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="区間最大・最小値更新">363. 区間最大・最小値更新</h2>

### 難易度統計

「区間最大・最小値更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4／diff <font color="red">2903</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★4／diff <font color="red">2903</font>

### レベル別問題一覧

「区間最大・最小値更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="バケット分割">364. バケット分割</h2>

### 難易度統計

「バケット分割」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.1／diff <font color="red">2872</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.7／diff <font color="orange">2519</font>
- 2022年: ★5／diff <font color="darkgoldenrod ">3577</font>

### レベル別問題一覧

「バケット分割」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題、diff <font color="yellowgreen">2381</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題、diff <font color="orange">2658</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)

　
<h2 id="高速フーリエ変換">365. 高速フーリエ変換</h2>

### 難易度統計

「高速フーリエ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.2／diff <font color="red">2976</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.5／diff <font color="red">2997</font>
- 2022年: ★3.8／diff <font color="red">2934</font>

### レベル別問題一覧

「高速フーリエ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題、diff <font color="orange">2673</font>)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題、diff <font color="yellowgreen">2258</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2580">No.2580 Hyperinflation</a> (Advent Calendar Contest 2023 (2023-12-01) - H問題、diff <font color="red">3103</font>)
- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)
- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)
- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)
- <a href="https://yukicoder.me/problems/no/2583">No.2583 Differential Equation (Enhanced version)</a> (Advent Calendar Contest 2023 (2023-12-01) - K問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="畳み込み">366. 畳み込み</h2>

### 難易度統計

「畳み込み」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.2／diff <font color="red">2976</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.5／diff <font color="red">2997</font>
- 2022年: ★3.8／diff <font color="red">2934</font>

### レベル別問題一覧

「畳み込み」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題、diff <font color="orange">2673</font>)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題、diff <font color="yellowgreen">2258</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2580">No.2580 Hyperinflation</a> (Advent Calendar Contest 2023 (2023-12-01) - H問題、diff <font color="red">3103</font>)
- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)
- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)
- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)
- <a href="https://yukicoder.me/problems/no/2583">No.2583 Differential Equation (Enhanced version)</a> (Advent Calendar Contest 2023 (2023-12-01) - K問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="遅延セグメント木">367. 遅延セグメント木</h2>

### 難易度統計

「遅延セグメント木」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.2／diff <font color="red">3142</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★4.2／diff <font color="red">3142</font>

### レベル別問題一覧

「遅延セグメント木」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="データ構造をマージする一般的なテク">368. データ構造をマージする一般的なテク</h2>

### 難易度統計

「データ構造をマージする一般的なテク」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.3／diff <font color="red">3090</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.7／diff <font color="red">3055</font>
- 2022年: ★4／diff <font color="red">3125</font>

### レベル別問題一覧

「データ構造をマージする一般的なテク」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題、diff <font color="orange">2673</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)
- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="演算の反復の分割統治">369. 演算の反復の分割統治</h2>

### 難易度統計

「演算の反復の分割統治」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.3／diff <font color="red">3090</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.7／diff <font color="red">3055</font>
- 2022年: ★4／diff <font color="red">3125</font>

### レベル別問題一覧

「演算の反復の分割統治」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題、diff <font color="orange">2673</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)
- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="ファウルハーバーの公式">370. ファウルハーバーの公式</h2>

### 難易度統計

「ファウルハーバーの公式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.5／diff <font color="red">3103</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.5／diff <font color="red">3103</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ファウルハーバーの公式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2580">No.2580 Hyperinflation</a> (Advent Calendar Contest 2023 (2023-12-01) - H問題、diff <font color="red">3103</font>)

　
<h2 id="parallel tree contraction">371. parallel tree contraction</h2>

### 難易度統計

「parallel tree contraction」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.5／diff <font color="darkgoldenrod ">3316</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「parallel tree contraction」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="演算の適用を１次式の合成に翻訳">372. 演算の適用を１次式の合成に翻訳</h2>

### 難易度統計

「演算の適用を１次式の合成に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.5／diff <font color="darkgoldenrod ">3316</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「演算の適用を１次式の合成に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="構文解析">373. 構文解析</h2>

### 難易度統計

「構文解析」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.5／diff <font color="darkgoldenrod ">3316</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「構文解析」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="重軽分解">374. 重軽分解</h2>

### 難易度統計

「重軽分解」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.5／diff <font color="darkgoldenrod ">3349</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★4.5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「重軽分解」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題、diff <font color="darkgoldenrod ">3382</font>)
- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="区間二次形式取得">375. 区間二次形式取得</h2>

### 難易度統計

「区間二次形式取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.5／diff <font color="darkgoldenrod ">3382</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★4.5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「区間二次形式取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="区間二次式取得">376. 区間二次式取得</h2>

### 難易度統計

「区間二次式取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.5／diff <font color="darkgoldenrod ">3382</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★4.5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「区間二次式取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="Polynomial Taylor shift">377. Polynomial Taylor shift</h2>

### 難易度統計

「Polynomial Taylor shift」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4.7／diff <font color="darkgoldenrod ">3209</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★4.7／diff <font color="darkgoldenrod ">3209</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Polynomial Taylor shift」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2580">No.2580 Hyperinflation</a> (Advent Calendar Contest 2023 (2023-12-01) - H問題、diff <font color="red">3103</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2583">No.2583 Differential Equation (Enhanced version)</a> (Advent Calendar Contest 2023 (2023-12-01) - K問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="Lindstrom-Gessel-Viennotの補題">378. Lindstrom-Gessel-Viennotの補題</h2>

### 難易度統計

「Lindstrom-Gessel-Viennotの補題」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Lindstrom-Gessel-Viennotの補題」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="ファンデルモンドの行列式計算">379. ファンデルモンドの行列式計算</h2>

### 難易度統計

「ファンデルモンドの行列式計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ファンデルモンドの行列式計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="差積計算">380. 差積計算</h2>

### 難易度統計

「差積計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「差積計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="半標準ヤングタブロー">381. 半標準ヤングタブロー</h2>

### 難易度統計

「半標準ヤングタブロー」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「半標準ヤングタブロー」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="半標準ヤングタブローとGelfand-Tsetlinパターンの対応">382. 半標準ヤングタブローとGelfand-Tsetlinパターンの対応</h2>

### 難易度統計

「半標準ヤングタブローとGelfand-Tsetlinパターンの対応」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「半標準ヤングタブローとGelfand-Tsetlinパターンの対応」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="半標準ヤングタブローと非交差経路の対応">383. 半標準ヤングタブローと非交差経路の対応</h2>

### 難易度統計

「半標準ヤングタブローと非交差経路の対応」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「半標準ヤングタブローと非交差経路の対応」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="微分計算">384. 微分計算</h2>

### 難易度統計

「微分計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「微分計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="フック長公式">385. フック長公式</h2>

### 難易度統計

「フック長公式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3086</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="red">3086</font>

### レベル別問題一覧

「フック長公式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)

　
<h2 id="標準ヤングタブロー">386. 標準ヤングタブロー</h2>

### 難易度統計

「標準ヤングタブロー」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3086</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="red">3086</font>

### レベル別問題一覧

「標準ヤングタブロー」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)

　
<h2 id="多点評価">387. 多点評価</h2>

### 難易度統計

「多点評価」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3186</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★5／diff <font color="darkgoldenrod ">3577</font>

### レベル別問題一覧

「多点評価」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)
- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="Bostan-Mori法">388. Bostan-Mori法</h2>

### 難易度統計

「Bostan-Mori法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3196</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="red">3196</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Bostan-Mori法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)

　
<h2 id="巡回畳み込み">389. 巡回畳み込み</h2>

### 難易度統計

「巡回畳み込み」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3196</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="red">3196</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「巡回畳み込み」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)

　
<h2 id="多項式のユークリッドの互除法">390. 多項式のユークリッドの互除法</h2>

### 難易度統計

「多項式のユークリッドの互除法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3196</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="red">3196</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「多項式のユークリッドの互除法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)

　
<h2 id="多項式を法とする逆元計算">391. 多項式を法とする逆元計算</h2>

### 難易度統計

「多項式を法とする逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3196</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="red">3196</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「多項式を法とする逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)

　
<h2 id="単位の分解">392. 単位の分解</h2>

### 難易度統計

「単位の分解」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3196</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="red">3196</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「単位の分解」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)

　
<h2 id="一次分数変換">393. 一次分数変換</h2>

### 難易度統計

「一次分数変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「一次分数変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2583">No.2583 Differential Equation (Enhanced version)</a> (Advent Calendar Contest 2023 (2023-12-01) - K問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="一次分数変換と対数関数による変数変換の合成">394. 一次分数変換と対数関数による変数変換の合成</h2>

### 難易度統計

「一次分数変換と対数関数による変数変換の合成」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「一次分数変換と対数関数による変数変換の合成」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2583">No.2583 Differential Equation (Enhanced version)</a> (Advent Calendar Contest 2023 (2023-12-01) - K問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="指数関数による変数変換と一次分数変換の合成">395. 指数関数による変数変換と一次分数変換の合成</h2>

### 難易度統計

「指数関数による変数変換と一次分数変換の合成」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「指数関数による変数変換と一次分数変換の合成」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2583">No.2583 Differential Equation (Enhanced version)</a> (Advent Calendar Contest 2023 (2023-12-01) - K問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="微分作用素を変数変換で簡易化">396. 微分作用素を変数変換で簡易化</h2>

### 難易度統計

「微分作用素を変数変換で簡易化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「微分作用素を変数変換で簡易化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2583">No.2583 Differential Equation (Enhanced version)</a> (Advent Calendar Contest 2023 (2023-12-01) - K問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="部分積分">397. 部分積分</h2>

### 難易度統計

「部分積分」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="darkgoldenrod ">3316</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「部分積分」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2583">No.2583 Differential Equation (Enhanced version)</a> (Advent Calendar Contest 2023 (2023-12-01) - K問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="トポロジカルソート">398. トポロジカルソート</h2>

### 難易度統計

「トポロジカルソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3382</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「トポロジカルソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="強連結成分分解">399. 強連結成分分解</h2>

### 難易度統計

「強連結成分分解」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3382</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「強連結成分分解」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="残余ネットワーク">400. 残余ネットワーク</h2>

### 難易度統計

「残余ネットワーク」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3382</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「残余ネットワーク」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="指定序数の値の計算を桁ごとの計算に帰着">401. 指定序数の値の計算を桁ごとの計算に帰着</h2>

### 難易度統計

「指定序数の値の計算を桁ごとの計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3503</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="darkgoldenrod ">3503</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「指定序数の値の計算を桁ごとの計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="非負整数をB進法でベクトルに翻訳">402. 非負整数をB進法でベクトルに翻訳</h2>

### 難易度統計

「非負整数をB進法でベクトルに翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3503</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="darkgoldenrod ">3503</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「非負整数をB進法でベクトルに翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="P-再帰">403. P-再帰</h2>

### 難易度統計

「P-再帰」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3577</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="darkgoldenrod ">3577</font>

### レベル別問題一覧

「P-再帰」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)

　
<h2 id="評価点シフト">404. 評価点シフト</h2>

### 難易度統計

「評価点シフト」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="darkgoldenrod ">3577</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="darkgoldenrod ">3577</font>

### レベル別問題一覧

「評価点シフト」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)

　
<h2 id="ハミルトン路構築">405. ハミルトン路構築</h2>

### 難易度統計

「ハミルトン路構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★データなし／diffデータなし
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ハミルトン路構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)

