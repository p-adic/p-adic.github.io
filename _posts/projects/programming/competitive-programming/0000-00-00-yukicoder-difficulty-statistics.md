---
layout: project
title: yukicoder過去問解法別難易度統計
date: 2024-11-29
excerpt: "yukicoderの過去問の解法別の難易度に関する統計データです。"
parent: competitive-programming-project/
prev-child: competitive-programming-creating-problem-status
next-child: yukicoder-difficulty-statistics-solution-name
project: true
image-directory: competitive-programming
tags: [競技プログラミング,数学]
---

yukicoder contest 358 (2022-08-26) 以降に出題されたyuicoderの問題で筆者（$p$進大好きbot）がupsolveした問題の解法をまとめ、解法別に難易度（writerに設定されたレベルおよび解かれ具合から算出されたdifficulty）統計をします。

writer別の統計データは[こちら]({{ site.url }}/yukicoder-writer-statistics)をご確認ください。


## 進捗

通常問題の問題番号2056から2859までと2953以降のupsolve済み問題を登録し終わりました。先は長いです。


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

難易度投票結果も集計しようか迷いましたが、集計タイミングによって結果が変わってしまうので情報が時々刻々と古くなってしまうこと、そして

- [No.2714 Amaou ★1に対する★5.5投票](https://yukicoder.me/problems/no/2714/statistics)
- [No.2721 "Don't say N" Game ★1.5に対する★4.5投票](https://yukicoder.me/problems/no/2721/statistics)
- [No.2722 Kenken Fight ★2.5に対する★6投票](https://yukicoder.me/problems/no/2722/statistics)
- [No.2728 Grid Expansion ★1に対する★3投票](https://yukicoder.me/problems/no/2728/statistics)
- [No.2773 Wake up Record 1 ★1に対する★4投票](https://yukicoder.me/problems/no/2773/statistics)
- [No.2775 Nuisance Balls ★1に対する★6投票](https://yukicoder.me/problems/no/2775/statistics)
- [No.2778 Is there Same letter? ★1に対する★3.5投票](https://yukicoder.me/problems/no/2778/statistics)
- [No.2782 メルセンヌ数総乗 ★1.5に対する★6投票](https://yukicoder.me/problems/no/2782/statistics)

など極端な外れ値が観測されていることから集計しないことに決めました。


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


<h2 id="average_difficulty">レベルごとの平均difficulty</h2>

問題2056から問題2968のうち

- コンテスト出題であり（単発出題でなく）かつ
- レベルが設定されておりかつ
- difficultyが算出されているもの

を対象にレベルごとにコンテスト平均difficultyを算出したデータです。


### ★

- 全体: diff <font color="brown">525</font>（67問）
- 2024年: diff <font color="brown">623</font>（35問）
- 2023年: diff <font color="gray">370</font>（28問）
- 2022年: diff <font color="brown">742</font>（4問）

### ★☆

- 全体: diff <font color="green">943</font>（93問）
- 2024年: diff <font color="green">981</font>（43問）
- 2023年: diff <font color="green">934</font>（38問）
- 2022年: diff <font color="green">831</font>（12問）

### ★★

- 全体: diff <font color="deepskyblue">1340</font>（131問）
- 2024年: diff <font color="deepskyblue">1429</font>（56問）
- 2023年: diff <font color="deepskyblue">1240</font>（58問）
- 2022年: diff <font color="deepskyblue">1389</font>（17問）

### ★★☆

- 全体: diff <font color="blue">1821</font>（160問）
- 2024年: diff <font color="blue">1827</font>（64問）
- 2023年: diff <font color="blue">1798</font>（78問）
- 2022年: diff <font color="blue">1899</font>（18問）

### ★★★

- 全体: diff <font color="yellowgreen">2243</font>（163問）
- 2024年: diff <font color="yellowgreen">2271</font>（74問）
- 2023年: diff <font color="yellowgreen">2211</font>（67問）
- 2022年: diff <font color="yellowgreen">2245</font>（22問）

### ★★★☆

- 全体: diff <font color="orange">2576</font>（134問）
- 2024年: diff <font color="orange">2563</font>（51問）
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

1. （★1／diff <font color="brown">624</font>／1問）<a href="#ゼロ除算回避" class="tag">ゼロ除算回避</a>
1. （★1／diff <font color="brown">783</font>／1問）<a href="#四捨五入計算" class="tag">四捨五入計算</a>
1. （★1.1／diff <font color="brown">670</font>／4問）<a href="#カレンダー計算" class="tag">カレンダー計算</a>
1. （★1.2／diff <font color="brown">646</font>／2問）<a href="#切り上げ" class="tag">切り上げ</a>
1. （★1.2／diff <font color="brown">699</font>／60問）<a href="#実装" class="tag">実装</a>
1. （★1.2／diff <font color="green">830</font>／2問）<a href="#貨幣計算" class="tag">貨幣計算</a>
1. （★1.2／diff <font color="deepskyblue">1523</font>／2問）<a href="#getline" class="tag">getline</a>
1. （★1.4／diff <font color="green">910</font>／20問）<a href="#64bit整数" class="tag">64bit整数</a>
1. （★1.5／diff <font color="brown">708</font>／2問）<a href="#符号なし64bit整数" class="tag">符号なし64bit整数</a>
1. （★1.5／diff <font color="brown">736</font>／1問）<a href="#経路全探索" class="tag">経路全探索</a>
1. （★1.5／diff <font color="brown">774</font>／1問）<a href="#コスト１ナップサック最適化" class="tag">コスト１ナップサック最適化</a>
1. （★1.5／diff <font color="brown">775</font>／1問）<a href="#再帰による多重ループ実装" class="tag">再帰による多重ループ実装</a>
1. （★1.5／diff <font color="green">873</font>／1問）<a href="#埋め込み" class="tag">埋め込み</a>
1. （★1.5／diff <font color="green">919</font>／1問）<a href="#選択順依存価値コストなしナップサック最適化" class="tag">選択順依存価値コストなしナップサック最適化</a>
1. （★1.5／diff <font color="green">959</font>／1問）<a href="#試行回数の期待値を各試行の実施確率の和に帰着" class="tag">試行回数の期待値を各試行の実施確率の和に帰着</a>
1. （★1.5／diff <font color="green">959</font>／1問）<a href="#等差数列と等比数列の各点積の累積和計算" class="tag">等差数列と等比数列の各点積の累積和計算</a>
1. （★1.5／diff <font color="green">976</font>／3問）<a href="#４重以上のループ" class="tag">４重以上のループ</a>
1. （★1.5／diff <font color="green">1026</font>／1問）<a href="#商を用いた積のオーバーフロー回避" class="tag">商を用いた積のオーバーフロー回避</a>
1. （★1.5／diff <font color="deepskyblue">1313</font>／1問）<a href="#multiset" class="tag">multiset</a>
1. （★1.6／diff <font color="green">894</font>／5問）<a href="#基数の変換" class="tag">基数の変換</a>
1. （★1.6／diff <font color="green">990</font>／8問）<a href="#set" class="tag">set</a>
1. （★1.6／diff <font color="green">1175</font>／6問）<a href="#１次式の最大・最小値計算" class="tag">１次式の最大・最小値計算</a>
1. （★1.6／diff <font color="deepskyblue">1206</font>／3問）<a href="#組分けの余りに注目" class="tag">組分けの余りに注目</a>
1. （★1.7／diff <font color="green">1074</font>／13問）<a href="#数値の文字列受け取り" class="tag">数値の文字列受け取り</a>
1. （★1.7／diff <font color="green">1153</font>／17問）<a href="#頻度表" class="tag">頻度表</a>
1. （★1.7／diff <font color="deepskyblue">1202</font>／2問）<a href="#整礎性" class="tag">整礎性</a>
1. （★1.7／diff <font color="deepskyblue">1228</font>／2問）<a href="#証明をなぞる構築" class="tag">証明をなぞる構築</a>
1. （★1.7／diff <font color="deepskyblue">1441</font>／2問）<a href="#解の公式" class="tag">解の公式</a>
1. （★1.7／diff <font color="blue">1775</font>／2問）<a href="#剰余計算を桁の線形和に帰着" class="tag">剰余計算を桁の線形和に帰着</a>
1. （★1.8／diff <font color="deepskyblue">1226</font>／15問）<a href="#特殊な入出力" class="tag">特殊な入出力</a>
1. （★1.8／diff <font color="deepskyblue">1243</font>／3問）<a href="#外積計算" class="tag">外積計算</a>
1. （★1.9／diff <font color="deepskyblue">1335</font>／23問）<a href="#シミュレーション" class="tag">シミュレーション</a>
1. （★1.9／diff <font color="deepskyblue">1361</font>／17問）<a href="#連想配列" class="tag">連想配列</a>
1. （★1.9／diff <font color="deepskyblue">1392</font>／8問）<a href="#指定序数の値の計算や始切片数え上げや１次元最近点計算をソートに帰着" class="tag">指定序数の値の計算や始切片数え上げや１次元最近点計算をソートに帰着</a>
1. （★2／diff <font color="green">1050</font>／3問）<a href="#巡回置換表示" class="tag">巡回置換表示</a>
1. （★2／diff <font color="green">1180</font>／3問）<a href="#底辺と高さを用いた三角形の面積計算" class="tag">底辺と高さを用いた三角形の面積計算</a>
1. （★2／diff <font color="deepskyblue">1228</font>／1問）<a href="#符号なし整数によるオーバーフロー回避" class="tag">符号なし整数によるオーバーフロー回避</a>
1. （★2／diff <font color="deepskyblue">1242</font>／6問）<a href="#サンプルに帰着" class="tag">サンプルに帰着</a>
1. （★2／diff <font color="deepskyblue">1276</font>／1問）<a href="#区間線形結合取得" class="tag">区間線形結合取得</a>
1. （★2／diff <font color="deepskyblue">1276</font>／1問）<a href="#区間選択ナップサック最適化" class="tag">区間選択ナップサック最適化</a>
1. （★2／diff <font color="deepskyblue">1301</font>／3問）<a href="#最近点計算" class="tag">最近点計算</a>
1. （★2／diff <font color="deepskyblue">1306</font>／2問）<a href="#相似" class="tag">相似</a>
1. （★2／diff <font color="deepskyblue">1318</font>／1問）<a href="#始切片の比較を最大要素の比較に帰着" class="tag">始切片の比較を最大要素の比較に帰着</a>
1. （★2／diff <font color="deepskyblue">1319</font>／3問）<a href="#lower_bound・upper_bound取得" class="tag">lower_bound・upper_bound取得</a>
1. （★2／diff <font color="deepskyblue">1322</font>／1問）<a href="#商の剰余計算を大きい法に帰着" class="tag">商の剰余計算を大きい法に帰着</a>
1. （★2／diff <font color="deepskyblue">1352</font>／1問）<a href="#負コストナップサック最適化" class="tag">負コストナップサック最適化</a>
1. （★2／diff <font color="deepskyblue">1356</font>／1問）<a href="#階乗による多項係数計算" class="tag">階乗による多項係数計算</a>
1. （★2／diff <font color="deepskyblue">1356</font>／1問）<a href="#多項係数計算" class="tag">多項係数計算</a>
1. （★2／diff <font color="deepskyblue">1366</font>／1問）<a href="#連結リスト" class="tag">連結リスト</a>
1. （★2／diff <font color="deepskyblue">1379</font>／2問）<a href="#非連結性を壁の８方向移動による連結性に翻訳" class="tag">非連結性を壁の８方向移動による連結性に翻訳</a>
1. （★2／diff <font color="deepskyblue">1447</font>／1問）<a href="#最小公倍数の約数関係判定を最大公約数の最小公倍数計算に帰着" class="tag">最小公倍数の約数関係判定を最大公約数の最小公倍数計算に帰着</a>
1. （★2／diff <font color="deepskyblue">1450</font>／87問）<a href="#全探索" class="tag">全探索</a>
1. （★2／diff <font color="deepskyblue">1458</font>／5問）<a href="#重複選択可ナップサック最適化" class="tag">重複選択可ナップサック最適化</a>
1. （★2／diff <font color="deepskyblue">1476</font>／3問）<a href="#中国剰余定理" class="tag">中国剰余定理</a>／CRT
1. （★2／diff <font color="deepskyblue">1551</font>／5問）<a href="#ソート前の添字復元" class="tag">ソート前の添字復元</a>
1. （★2／diff <font color="deepskyblue">1585</font>／1問）<a href="#素因数分解による最小公倍数計算" class="tag">素因数分解による最小公倍数計算</a>
1. （★2／diff <font color="deepskyblue">1585</font>／1問）<a href="#置換の合成" class="tag">置換の合成</a>
1. （★2／diff <font color="deepskyblue">1596</font>／1問）<a href="#質問の全探索による質問決定" class="tag">質問の全探索による質問決定</a>
1. （★2／diff <font color="blue">1605</font>／1問）<a href="#ルジャンドルの公式" class="tag">ルジャンドルの公式</a>
1. （★2／diff <font color="blue">1626</font>／2問）<a href="#多次元コストを１次元に翻訳" class="tag">多次元コストを１次元に翻訳</a>
1. （★2／diff <font color="blue">1644</font>／2問）<a href="#多次元コスト重複選択可ナップサック最適化" class="tag">多次元コスト重複選択可ナップサック最適化</a>
1. （★2／diff <font color="blue">1659</font>／1問）<a href="#倍数判定を約数列挙に帰着" class="tag">倍数判定を約数列挙に帰着</a>
1. （★2／diff <font color="blue">1695</font>／2問）<a href="#区間要素数取得を始切片数え上げに帰着" class="tag">区間要素数取得を始切片数え上げに帰着</a>
1. （★2.1／diff <font color="deepskyblue">1227</font>／4問）<a href="#到達可能性判定" class="tag">到達可能性判定</a>
1. （★2.1／diff <font color="deepskyblue">1273</font>／3問）<a href="#遷移の収束" class="tag">遷移の収束</a>
1. （★2.1／diff <font color="deepskyblue">1324</font>／5問）<a href="#三角形の面積計算" class="tag">三角形の面積計算</a>
1. （★2.1／diff <font color="deepskyblue">1384</font>／14問）<a href="#ギャグ" class="tag">ギャグ</a>
1. （★2.1／diff <font color="deepskyblue">1430</font>／4問）<a href="#多次元コストナップサック最適化" class="tag">多次元コストナップサック最適化</a>
1. （★2.1／diff <font color="deepskyblue">1452</font>／8問）<a href="#小数型" class="tag">小数型</a>
1. （★2.1／diff <font color="deepskyblue">1473</font>／59問）<a href="#場合分け" class="tag">場合分け</a>
1. （★2.1／diff <font color="deepskyblue">1480</font>／37問）<a href="#貪欲法" class="tag">貪欲法</a>
1. （★2.1／diff <font color="deepskyblue">1533</font>／8問）<a href="#等差数列の累積和計算" class="tag">等差数列の累積和計算</a>
1. （★2.1／diff <font color="deepskyblue">1533</font>／3問）<a href="#分割の均等化" class="tag">分割の均等化</a>
1. （★2.1／diff <font color="deepskyblue">1557</font>／3問）<a href="#オーバーフロー回避" class="tag">オーバーフロー回避</a>
1. （★2.1／diff <font color="deepskyblue">1576</font>／8問）<a href="#平方根計算" class="tag">平方根計算</a>
1. （★2.1／diff <font color="deepskyblue">1579</font>／9問）<a href="#動的mod" class="tag">動的mod</a>
1. （★2.1／diff <font color="deepskyblue">1587</font>／3問）<a href="#決め打ちによる構築" class="tag">決め打ちによる構築</a>
1. （★2.1／diff <font color="blue">1717</font>／3問）<a href="#木の頂点の次数計算" class="tag">木の頂点の次数計算</a>
1. （★2.2／diff <font color="deepskyblue">1200</font>／2問）<a href="#隣接不等式管理" class="tag">隣接不等式管理</a>
1. （★2.2／diff <font color="deepskyblue">1322</font>／2問）<a href="#複素数演算" class="tag">複素数演算</a>
1. （★2.2／diff <font color="deepskyblue">1355</font>／2問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着)）<a href="#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着" class="tag">操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着</a>
1. （★2.2／diff <font color="deepskyblue">1395</font>／2問）<a href="#最長歩道計算" class="tag">最長歩道計算</a>
1. （★2.2／diff <font color="deepskyblue">1412</font>／2問）<a href="#三角形の成立条件" class="tag">三角形の成立条件</a>
1. （★2.2／diff <font color="deepskyblue">1419</font>／9問）<a href="#DAG上のDP" class="tag">DAG上のDP</a>
1. （★2.2／diff <font color="deepskyblue">1420</font>／7問）<a href="#ナップサックDP" class="tag">ナップサックDP</a>
1. （★2.2／diff <font color="deepskyblue">1439</font>／3問）<a href="#コストなしナップサック最適化" class="tag">コストなしナップサック最適化</a>
1. （★2.2／diff <font color="deepskyblue">1479</font>／12問）<a href="#約数列挙" class="tag">約数列挙</a>
1. （★2.2／diff <font color="deepskyblue">1484</font>／21問）<a href="#ナップサック最適化" class="tag">ナップサック最適化</a>
1. （★2.2／diff <font color="deepskyblue">1540</font>／2問）<a href="#外積による三角形の面積計算" class="tag">外積による三角形の面積計算</a>
1. （★2.2／diff <font color="deepskyblue">1540</font>／2問）<a href="#ヘルド・カープ法" class="tag">ヘルド・カープ法</a>／Held-Karp法
1. （★2.2／diff <font color="deepskyblue">1544</font>／14問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作を数値に翻訳)）<a href="#操作を数値に翻訳" class="tag">操作を数値に翻訳</a>
1. （★2.2／diff <font color="deepskyblue">1559</font>／25問）<a href="#幅優先探索" class="tag">幅優先探索</a>／BFS
1. （★2.2／diff <font color="deepskyblue">1581</font>／10問）<a href="#素因数分解による約数列挙" class="tag">素因数分解による約数列挙</a>
1. （★2.2／diff <font color="deepskyblue">1587</font>／2問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#重複選択個数の線形関係式)）<a href="#重複選択個数の線形関係式" class="tag">重複選択個数の線形関係式</a>
1. （★2.2／diff <font color="blue">1607</font>／4問）<a href="#最小公倍数計算" class="tag">最小公倍数計算</a>／LCM計算
1. （★2.2／diff <font color="blue">1619</font>／3問）<a href="#素数列による試し割り法" class="tag">素数列による試し割り法</a>
1. （★2.2／diff <font color="blue">1632</font>／14問）<a href="#小数計算を整数に帰着" class="tag">小数計算を整数に帰着</a>
1. （★2.2／diff <font color="blue">1716</font>／2問）<a href="#連長圧縮" class="tag">連長圧縮</a>／ランレングス圧縮／RLE
1. （★2.2／diff <font color="blue">1747</font>／2問）<a href="#括弧列判定" class="tag">括弧列判定</a>
1. （★2.2／diff <font color="blue">1770</font>／4問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)）<a href="#良いケースに帰着" class="tag">良いケースに帰着</a>
1. （★2.2／diff <font color="blue">1778</font>／2問）<a href="#選択肢の分割・纏め上げで良いケースに帰着" class="tag">選択肢の分割・纏め上げで良いケースに帰着</a>
1. （★2.2／diff <font color="blue">1795</font>／2問）<a href="#ウノ計算" class="tag">ウノ計算</a>
1. （★2.2／diff <font color="blue">1844</font>／2問）<a href="#不定方程式の因数分解" class="tag">不定方程式の因数分解</a>
1. （★2.3／diff <font color="deepskyblue">1307</font>／4問）<a href="#門松列DP" class="tag">門松列DP</a>
1. （★2.3／diff <font color="deepskyblue">1462</font>／18問）<a href="#連結成分取得" class="tag">連結成分取得</a>
1. （★2.3／diff <font color="deepskyblue">1519</font>／7問）<a href="#bit全探索" class="tag">bit全探索</a>
1. （★2.3／diff <font color="deepskyblue">1530</font>／19問）<a href="#素集合データ構造" class="tag">素集合データ構造</a>／Union Find／UF／Disjoint Set Union／DSU
1. （★2.3／diff <font color="deepskyblue">1541</font>／12問）<a href="#余事象に注目" class="tag">余事象に注目</a>
1. （★2.3／diff <font color="blue">1614</font>／3問）<a href="#最大公約数による最小公倍数計算" class="tag">最大公約数による最小公倍数計算</a>
1. （★2.3／diff <font color="blue">1618</font>／4問）<a href="#頂点倍化" class="tag">頂点倍化</a>
1. （★2.3／diff <font color="blue">1618</font>／4問）<a href="#二部グラフ判定" class="tag">二部グラフ判定</a>
1. （★2.3／diff <font color="blue">1672</font>／50問）<a href="#ソート" class="tag">ソート</a>
1. （★2.3／diff <font color="blue">1678</font>／34問）<a href="#累積積による冪乗・階乗計算" class="tag">累積積による冪乗・階乗計算</a>
1. （★2.3／diff <font color="blue">1684</font>／6問）<a href="#等比数列の累積和計算" class="tag">等比数列の累積和計算</a>
1. （★2.3／diff <font color="blue">1702</font>／3問）<a href="#二・多項係数を組み合わせに翻訳" class="tag">二・多項係数を組み合わせに翻訳</a>
1. （★2.3／diff <font color="blue">1779</font>／42問）<a href="#変数決め打ち" class="tag">変数決め打ち</a>
1. （★2.3／diff <font color="blue">1780</font>／13問）<a href="#最終手番に注目" class="tag">最終手番に注目</a>
1. （★2.3／diff <font color="blue">1791</font>／3問）<a href="#約数計数関数による計算量評価" class="tag">約数計数関数による計算量評価</a>
1. （★2.3／diff <font color="blue">1885</font>／4問）<a href="#操作コスト最小化を最短経路長計算に帰着" class="tag">操作コスト最小化を最短経路長計算に帰着</a>
1. （★2.3／diff <font color="blue">1975</font>／5問）<a href="#グラフの状態や目的地の変化を有向辺に翻訳" class="tag">グラフの状態や目的地の変化を有向辺に翻訳</a>
1. （★2.4／diff <font color="deepskyblue">1562</font>／9問）<a href="#深さ優先探索" class="tag">深さ優先探索</a>／DFS
1. （★2.4／diff <font color="deepskyblue">1576</font>／7問）<a href="#ド・モルガンの法則" class="tag">ド・モルガンの法則</a>
1. （★2.4／diff <font color="deepskyblue">1583</font>／5問）<a href="#素数列挙" class="tag">素数列挙</a>
1. （★2.4／diff <font color="blue">1677</font>／11問）<a href="#操作・遷移の纏め上げ" class="tag">操作・遷移の纏め上げ</a>
1. （★2.4／diff <font color="blue">1679</font>／5問）<a href="#bool値の充足可能性判定" class="tag">bool値の充足可能性判定</a>
1. （★2.4／diff <font color="blue">1696</font>／15問）<a href="#試し割り法" class="tag">試し割り法</a>
1. （★2.4／diff <font color="blue">1721</font>／28問）<a href="#累積和" class="tag">累積和</a>
1. （★2.4／diff <font color="blue">1738</font>／35問）<a href="#集合管理" class="tag">集合管理</a>
1. （★2.4／diff <font color="blue">1754</font>／5問）<a href="#区間を切片の差に翻訳" class="tag">区間を切片の差に翻訳</a>
1. （★2.4／diff <font color="blue">1772</font>／30問）<a href="#不変量に注目" class="tag">不変量に注目</a>
1. （★2.4／diff <font color="blue">1820</font>／28問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)）<a href="#損をしない変形" class="tag">損をしない変形</a>
1. （★2.5／diff <font color="deepskyblue">1318</font>／1問）<a href="#３進法" class="tag">３進法</a>
1. （★2.5／diff <font color="deepskyblue">1358</font>／1問）<a href="#複数配列への範囲加算更新を１つの配列に纏め上げ" class="tag">複数配列への範囲加算更新を１つの配列に纏め上げ</a>
1. （★2.5／diff <font color="deepskyblue">1469</font>／1問）<a href="#部分和と補部分和の差の最小化" class="tag">部分和と補部分和の差の最小化</a>
1. （★2.5／diff <font color="deepskyblue">1489</font>／1問）<a href="#挿入ソート" class="tag">挿入ソート</a>
1. （★2.5／diff <font color="deepskyblue">1504</font>／2問）<a href="#最遠点計算" class="tag">最遠点計算</a>
1. （★2.5／diff <font color="deepskyblue">1535</font>／3問）<a href="#平方数判定" class="tag">平方数判定</a>
1. （★2.5／diff <font color="deepskyblue">1536</font>／1問）<a href="#符号全探索による絶対値計算" class="tag">符号全探索による絶対値計算</a>
1. （★2.5／diff <font color="deepskyblue">1544</font>／2問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を被覆の先頭項管理で処理)）<a href="#指定序数の値の計算を被覆の先頭項管理で処理" class="tag">指定序数の値の計算を被覆の先頭項管理で処理</a>
1. （★2.5／diff <font color="deepskyblue">1577</font>／2問）<a href="#言及する成分数を最大化する質問" class="tag">言及する成分数を最大化する質問</a>
1. （★2.5／diff <font color="deepskyblue">1588</font>／1問）<a href="#strategy stealing argument" class="tag">strategy stealing argument</a>
1. （★2.5／diff <font color="blue">1607</font>／1問）<a href="#倍数メビウス変換" class="tag">倍数メビウス変換</a>
1. （★2.5／diff <font color="blue">1619</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不明な想定解)）<a href="#不明な想定解" class="tag">不明な想定解</a>
1. （★2.5／diff <font color="blue">1642</font>／11問）<a href="#マッチ度ごとに管理" class="tag">マッチ度ごとに管理</a>
1. （★2.5／diff <font color="blue">1663</font>／9問）<a href="#経路数え上げ" class="tag">経路数え上げ</a>
1. （★2.5／diff <font color="blue">1666</font>／4問）<a href="#B進法による構築" class="tag">B進法による構築</a>
1. （★2.5／diff <font color="blue">1670</font>／2問）<a href="#ハミルトン路構築" class="tag">ハミルトン路構築</a>
1. （★2.5／diff <font color="blue">1683</font>／8問）<a href="#検索" class="tag">検索</a>
1. （★2.5／diff <font color="blue">1684</font>／9問）<a href="#配列を像・頻度表で管理" class="tag">配列を像・頻度表で管理</a>
1. （★2.5／diff <font color="blue">1704</font>／14問）<a href="#尺取り法" class="tag">尺取り法</a>
1. （★2.5／diff <font color="blue">1709</font>／2問）<a href="#二項定理" class="tag">二項定理</a>
1. （★2.5／diff <font color="blue">1717</font>／1問）<a href="#ワーシャル・フロイド法" class="tag">ワーシャル・フロイド法</a>／Floyd-Warshall法／Warshall-Floyd法
1. （★2.5／diff <font color="blue">1717</font>／19問）<a href="#階乗計算" class="tag">階乗計算</a>
1. （★2.5／diff <font color="blue">1727</font>／3問）<a href="#円環の倍化実装" class="tag">円環の倍化実装</a>
1. （★2.5／diff <font color="blue">1728</font>／1問）<a href="#部分集合DP" class="tag">部分集合DP</a>
1. （★2.5／diff <font color="blue">1749</font>／1問）<a href="#ベルマンフォード法" class="tag">ベルマンフォード法</a>／Bellman-Ford法
1. （★2.5／diff <font color="blue">1749</font>／1問）<a href="#負閉路検出" class="tag">負閉路検出</a>
1. （★2.5／diff <font color="blue">1754</font>／2問）<a href="#差分管理" class="tag">差分管理</a>
1. （★2.5／diff <font color="blue">1762</font>／1問）<a href="#Next DP" class="tag">Next DP</a>
1. （★2.5／diff <font color="blue">1764</font>／17問）<a href="#区間族管理" class="tag">区間族管理</a>
1. （★2.5／diff <font color="blue">1768</font>／16問）<a href="#階乗逆元計算" class="tag">階乗逆元計算</a>
1. （★2.5／diff <font color="blue">1768</font>／1問）<a href="#Vieta Jumping" class="tag">Vieta Jumping</a>／Root Flipping
1. （★2.5／diff <font color="blue">1768</font>／2問）<a href="#解と係数の関係" class="tag">解と係数の関係</a>
1. （★2.5／diff <font color="blue">1769</font>／10問）<a href="#一要素削除" class="tag">一要素削除</a>
1. （★2.5／diff <font color="blue">1774</font>／1問）<a href="#価値上限ありナップサック最適化" class="tag">価値上限ありナップサック最適化</a>
1. （★2.5／diff <font color="blue">1774</font>／1問）<a href="#重複選択可価値上限ありナップサック最適化" class="tag">重複選択可価値上限ありナップサック最適化</a>
1. （★2.5／diff <font color="blue">1795</font>／12問）<a href="#ミラー戦略" class="tag">ミラー戦略</a>
1. （★2.5／diff <font color="blue">1803</font>／6問）<a href="#２種の数値を足し引きして１種に帰着" class="tag">２種の数値を足し引きして１種に帰着</a>
1. （★2.5／diff <font color="blue">1804</font>／26問）<a href="#素因数分解" class="tag">素因数分解</a>
1. （★2.5／diff <font color="blue">1805</font>／19問）<a href="#同じ値の纏め上げ" class="tag">同じ値の纏め上げ</a>
1. （★2.5／diff <font color="blue">1806</font>／2問）<a href="#あみだくじと置換の対応" class="tag">あみだくじと置換の対応</a>
1. （★2.5／diff <font color="blue">1806</font>／2問）<a href="#置換の互換表示" class="tag">置換の互換表示</a>
1. （★2.5／diff <font color="blue">1808</font>／11問）<a href="#最大・最小要素取得" class="tag">最大・最小要素取得</a>
1. （★2.5／diff <font color="blue">1812</font>／16問）<a href="#ダイクストラ法" class="tag">ダイクストラ法</a>／Dijkstra法
1. （★2.5／diff <font color="blue">1813</font>／45問）<a href="#二分探索" class="tag">二分探索</a>
1. （★2.5／diff <font color="blue">1820</font>／107問）<a href="#剰余計算" class="tag">剰余計算</a>
1. （★2.5／diff <font color="blue">1830</font>／6問）<a href="#包除原理" class="tag">包除原理</a>
1. （★2.5／diff <font color="blue">1831</font>／3問）<a href="#多項定理" class="tag">多項定理</a>
1. （★2.5／diff <font color="blue">1832</font>／12問）<a href="#エラトステネスの篩" class="tag">エラトステネスの篩</a>
1. （★2.5／diff <font color="blue">1838</font>／1問）<a href="#オイラーの定理" class="tag">オイラーの定理</a>
1. （★2.5／diff <font color="blue">1838</font>／1問）<a href="#オイラーの定理による逆元計算" class="tag">オイラーの定理による逆元計算</a>
1. （★2.5／diff <font color="blue">1838</font>／1問）<a href="#合成数を法とする逆元計算" class="tag">合成数を法とする逆元計算</a>
1. （★2.5／diff <font color="blue">1845</font>／1問）<a href="#エラトステネスの篩による素数判定" class="tag">エラトステネスの篩による素数判定</a>
1. （★2.5／diff <font color="blue">1845</font>／1問）<a href="#素数計数関数前計算" class="tag">素数計数関数前計算</a>
1. （★2.5／diff <font color="blue">1845</font>／1問）<a href="#素数判定" class="tag">素数判定</a>
1. （★2.5／diff <font color="blue">1848</font>／1問）<a href="#Dilworthの定理" class="tag">Dilworthの定理</a>
1. （★2.5／diff <font color="blue">1848</font>／1問）<a href="#鎖への分割数の最小化" class="tag">鎖への分割数の最小化</a>
1. （★2.5／diff <font color="blue">1848</font>／5問）<a href="#ポテンシャル付き素集合データ構造" class="tag">ポテンシャル付き素集合データ構造</a>
1. （★2.5／diff <font color="blue">1850</font>／7問）<a href="#充足可能性判定" class="tag">充足可能性判定</a>
1. （★2.5／diff <font color="blue">1852</font>／71問）<a href="#分割統治法" class="tag">分割統治法</a>
1. （★2.5／diff <font color="blue">1855</font>／10問）<a href="#階差数列" class="tag">階差数列</a>
1. （★2.5／diff <font color="blue">1863</font>／21問）<a href="#最短経路長計算" class="tag">最短経路長計算</a>
1. （★2.5／diff <font color="blue">1877</font>／55問）<a href="#冪乗計算" class="tag">冪乗計算</a>
1. （★2.5／diff <font color="blue">1882</font>／11問）<a href="#フェルマーの小定理" class="tag">フェルマーの小定理</a>
1. （★2.5／diff <font color="blue">1885</font>／2問）<a href="#setprecision・format" class="tag">setprecision・format</a>
1. （★2.5／diff <font color="blue">1888</font>／2問）<a href="#交代和" class="tag">交代和</a>
1. （★2.5／diff <font color="blue">1890</font>／4問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を始切片の数え上げに帰着)）<a href="#指定序数の値の計算を始切片の数え上げに帰着" class="tag">指定序数の値の計算を始切片の数え上げに帰着</a>
1. （★2.5／diff <font color="blue">1891</font>／1問）<a href="#商のfloorの種類数による計算量評価" class="tag">商のfloorの種類数による計算量評価</a>
1. （★2.5／diff <font color="blue">1892</font>／4問）<a href="#01BFS" class="tag">01BFS</a>
1. （★2.5／diff <font color="blue">1900</font>／1問）<a href="#選択回数依存コストナップサック最適化" class="tag">選択回数依存コストナップサック最適化</a>
1. （★2.5／diff <font color="blue">1902</font>／15問）<a href="#周期性" class="tag">周期性</a>
1. （★2.5／diff <font color="blue">1928</font>／8問）<a href="#最大・最小要素削除" class="tag">最大・最小要素削除</a>
1. （★2.5／diff <font color="blue">1944</font>／2問）<a href="#多次元の最適化を１次元の最適化に帰着" class="tag">多次元の最適化を１次元の最適化に帰着</a>
1. （★2.5／diff <font color="blue">1944</font>／7問）<a href="#２変数決め打ち" class="tag">２変数決め打ち</a>
1. （★2.5／diff <font color="blue">1950</font>／5問）<a href="#凸最適化" class="tag">凸最適化</a>
1. （★2.5／diff <font color="blue">1964</font>／9問）<a href="#優先度付きキュー" class="tag">優先度付きキュー</a>／priority queue
1. （★2.5／diff <font color="blue">1983</font>／2問）<a href="#B進法で全探索" class="tag">B進法で全探索</a>
1. （★2.5／diff <font color="blue">1989</font>／1問）<a href="#多点BFS" class="tag">多点BFS</a>／多始点BFS
1. （★2.5／diff <font color="yellowgreen">2000</font>／2問）<a href="#三分探索" class="tag">三分探索</a>
1. （★2.5／diff <font color="yellowgreen">2031</font>／1問）<a href="#独立事象の確率を積で計算" class="tag">独立事象の確率を積で計算</a>
1. （★2.5／diff <font color="yellowgreen">2057</font>／5問）<a href="#１つの桁・成分のみ特定する質問" class="tag">１つの桁・成分のみ特定する質問</a>
1. （★2.5／diff <font color="yellowgreen">2123</font>／1問）<a href="#オイラーグラフ判定" class="tag">オイラーグラフ判定</a>
1. （★2.5／diff <font color="yellowgreen">2123</font>／2問）<a href="#上限・下限値に言及する質問" class="tag">上限・下限値に言及する質問</a>
1. （★2.5／diff <font color="yellowgreen">2162</font>／1問）<a href="#並列二分探索" class="tag">並列二分探索</a>
1. （★2.5／diff <font color="yellowgreen">2219</font>／1問）<a href="#定数倍メモリ削減" class="tag">定数倍メモリ削減</a>
1. （★2.5／diff <font color="yellowgreen">2323</font>／1問）<a href="#階乗進法" class="tag">階乗進法</a>
1. （★2.5／diff <font color="yellowgreen">2353</font>／1問）<a href="#個数上限１複数ナップサック最適化" class="tag">個数上限１複数ナップサック最適化</a>
1. （★2.5／diff <font color="orange">2491</font>／1問）<a href="#必勝戦略のリアクティブ化" class="tag">必勝戦略のリアクティブ化</a>
1. （★2.5／diff <font color="orange">2501</font>／1問）<a href="#全順序集合を状態に持つゲームをP状態とN状態の区間に分割" class="tag">全順序集合を状態に持つゲームをP状態とN状態の区間に分割</a>
1. （★2.5／diff <font color="orange">2525</font>／1問）<a href="#ラグランジュ補間" class="tag">ラグランジュ補間</a>／ファンデルモンドの逆行列計算
1. （★2.5／diff <font color="orange">2525</font>／1問）<a href="#逆行列計算" class="tag">逆行列計算</a>
1. （★2.6／diff <font color="blue">1705</font>／5問）<a href="#グリッド上の経路を01列や区間の部分集合に翻訳" class="tag">グリッド上の経路を01列や区間の部分集合に翻訳</a>
1. （★2.6／diff <font color="blue">1720</font>／6問）<a href="#操作逆順" class="tag">操作逆順</a>
1. （★2.6／diff <font color="blue">1723</font>／12問）<a href="#階乗による二項係数計算" class="tag">階乗による二項係数計算</a>
1. （★2.6／diff <font color="blue">1745</font>／3問）<a href="#グランディ数計算" class="tag">グランディ数計算</a>
1. （★2.6／diff <font color="blue">1755</font>／5問）<a href="#最終手番のターン数に注目" class="tag">最終手番のターン数に注目</a>
1. （★2.6／diff <font color="blue">1767</font>／15問）<a href="#差分計算" class="tag">差分計算</a>
1. （★2.6／diff <font color="blue">1788</font>／5問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)）<a href="#距離空間の重み付きグラフ化" class="tag">距離空間の重み付きグラフ化</a>
1. （★2.6／diff <font color="blue">1798</font>／10問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#合成による次元削減)）<a href="#合成による次元削減" class="tag">合成による次元削減</a>
1. （★2.6／diff <font color="blue">1799</font>／3問）<a href="#区間代入更新" class="tag">区間代入更新</a>
1. （★2.6／diff <font color="blue">1801</font>／3問）<a href="#クエリソート" class="tag">クエリソート</a>
1. （★2.6／diff <font color="blue">1817</font>／9問）<a href="#bitごとに計算" class="tag">bitごとに計算</a>
1. （★2.6／diff <font color="blue">1820</font>／9問）<a href="#クエリ先読み" class="tag">クエリ先読み</a>
1. （★2.6／diff <font color="blue">1833</font>／3問）<a href="#next_permutation" class="tag">next_permutation</a>
1. （★2.6／diff <font color="blue">1841</font>／28問）<a href="#区間和取得" class="tag">区間和取得</a>
1. （★2.6／diff <font color="blue">1849</font>／5問）<a href="#枝刈り" class="tag">枝刈り</a>
1. （★2.6／diff <font color="blue">1850</font>／8問）<a href="#データを不変量別に分割して管理" class="tag">データを不変量別に分割して管理</a>
1. （★2.6／diff <font color="blue">1861</font>／12問）<a href="#最大公約数計算" class="tag">最大公約数計算</a>／GCD計算
1. （★2.6／diff <font color="blue">1921</font>／11問）<a href="#フェルマーの小定理による逆元計算" class="tag">フェルマーの小定理による逆元計算</a>
1. （★2.6／diff <font color="blue">1928</font>／40問）<a href="#素数を法とする逆元計算" class="tag">素数を法とする逆元計算</a>
1. （★2.6／diff <font color="blue">1931</font>／29問）<a href="#逆元の再帰計算" class="tag">逆元の再帰計算</a>
1. （★2.6／diff <font color="blue">1942</font>／3問）<a href="#素数を用いた構築" class="tag">素数を用いた構築</a>
1. （★2.6／diff <font color="blue">1943</font>／3問）<a href="#転倒数計算" class="tag">転倒数計算</a>
1. （★2.6／diff <font color="blue">1944</font>／20問）<a href="#端から確定" class="tag">端から確定</a>
1. （★2.6／diff <font color="blue">1954</font>／40問）<a href="#繰り返し二乗法" class="tag">繰り返し二乗法</a>
1. （★2.6／diff <font color="blue">1957</font>／11問）<a href="#実験" class="tag">実験</a>
1. （★2.6／diff <font color="blue">1968</font>／4問）<a href="#bitDP" class="tag">bitDP</a>
1. （★2.6／diff <font color="blue">1987</font>／5問）<a href="#帰属区間取得" class="tag">帰属区間取得</a>
1. （★2.6／diff <font color="yellowgreen">2014</font>／6問）<a href="#ニム和" class="tag">ニム和</a>
1. （★2.6／diff <font color="yellowgreen">2047</font>／3問）<a href="#始点と終点からの最短経路長計算" class="tag">始点と終点からの最短経路長計算</a>
1. （★2.6／diff <font color="yellowgreen">2174</font>／3問）<a href="#左右から走査" class="tag">左右から走査</a>
1. （★2.6／diff <font color="yellowgreen">2211</font>／8問）<a href="#アルゴリズムのリアクティブ化" class="tag">アルゴリズムのリアクティブ化</a>
1. （★2.6／diff <font color="yellowgreen">2231</font>／5問）<a href="#変数の対称性" class="tag">変数の対称性</a>
1. （★2.6／diff <font color="yellowgreen">2258</font>／4問）<a href="#円周角の定理" class="tag">円周角の定理</a>／タレスの定理
1. （★2.7／diff <font color="blue">1650</font>／2問）<a href="#最長単調増加部分列長計算" class="tag">最長単調増加部分列長計算</a>／LIS計算
1. （★2.7／diff <font color="blue">1809</font>／2問）<a href="#鳩の巣原理" class="tag">鳩の巣原理</a>
1. （★2.7／diff <font color="blue">1888</font>／7問）<a href="#終点からの最短経路長計算" class="tag">終点からの最短経路長計算</a>
1. （★2.7／diff <font color="blue">1894</font>／7問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)）<a href="#表示可能性DP" class="tag">表示可能性DP</a>
1. （★2.7／diff <font color="blue">1904</font>／2問）<a href="#部分回文列挙" class="tag">部分回文列挙</a>
1. （★2.7／diff <font color="blue">1908</font>／15問）<a href="#二項係数計算" class="tag">二項係数計算</a>／場合の数計算
1. （★2.7／diff <font color="blue">1914</font>／6問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#場合分けによるmax・min・絶対値計算)）<a href="#場合分けによるmax・min・絶対値計算" class="tag">場合分けによるmax・min・絶対値計算</a>
1. （★2.7／diff <font color="blue">1916</font>／2問）<a href="#区間スケジューリング" class="tag">区間スケジューリング</a>
1. （★2.7／diff <font color="blue">1927</font>／2問）<a href="#商による付値計算" class="tag">商による付値計算</a>
1. （★2.7／diff <font color="blue">1942</font>／93問）<a href="#動的計画法" class="tag">動的計画法</a>／DP
1. （★2.7／diff <font color="blue">1954</font>／11問）<a href="#２進法" class="tag">２進法</a>
1. （★2.7／diff <font color="blue">1954</font>／14問）<a href="#ユークリッドの互除法" class="tag">ユークリッドの互除法</a>
1. （★2.7／diff <font color="blue">1956</font>／2問）<a href="#倍数ゼータ変換" class="tag">倍数ゼータ変換</a>
1. （★2.7／diff <font color="yellowgreen">2006</font>／11問）<a href="#付値計算" class="tag">付値計算</a>
1. （★2.7／diff <font color="yellowgreen">2009</font>／2問）<a href="#区間和の指定された区間数え上げ" class="tag">区間和の指定された区間数え上げ</a>
1. （★2.7／diff <font color="yellowgreen">2013</font>／4問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)）<a href="#不変量を保つ戦略" class="tag">不変量を保つ戦略</a>
1. （★2.7／diff <font color="yellowgreen">2020</font>／4問）<a href="#単調列数え上げ" class="tag">単調列数え上げ</a>
1. （★2.7／diff <font color="yellowgreen">2031</font>／4問）<a href="#ナップサック分割統治" class="tag">ナップサック分割統治</a>
1. （★2.7／diff <font color="yellowgreen">2034</font>／12問）<a href="#imos法" class="tag">imos法</a>
1. （★2.7／diff <font color="yellowgreen">2050</font>／2問）<a href="#再帰的構築" class="tag">再帰的構築</a>
1. （★2.7／diff <font color="yellowgreen">2063</font>／8問）<a href="#区間要素数取得" class="tag">区間要素数取得</a>
1. （★2.7／diff <font color="yellowgreen">2078</font>／2問）<a href="#描画可能性を実際に描画して判定" class="tag">描画可能性を実際に描画して判定</a>
1. （★2.7／diff <font color="yellowgreen">2109</font>／2問）<a href="#倍数走査によるオイラー関数前計算" class="tag">倍数走査によるオイラー関数前計算</a>
1. （★2.7／diff <font color="yellowgreen">2121</font>／17問）<a href="#再帰" class="tag">再帰</a>
1. （★2.7／diff <font color="yellowgreen">2146</font>／3問）<a href="#クラスカル法" class="tag">クラスカル法</a>／Kruskal法
1. （★2.7／diff <font color="yellowgreen">2146</font>／3問）<a href="#最小全域木計算" class="tag">最小全域木計算</a>
1. （★2.7／diff <font color="yellowgreen">2149</font>／7問）<a href="#木DP" class="tag">木DP</a>
1. （★2.7／diff <font color="yellowgreen">2175</font>／2問）<a href="#三平方の定理" class="tag">三平方の定理</a>
1. （★2.7／diff <font color="yellowgreen">2232</font>／6問）<a href="#半分全列挙" class="tag">半分全列挙</a>
1. （★2.7／diff <font color="yellowgreen">2263</font>／2問）<a href="#エラトステネスの篩による約数列挙前計算" class="tag">エラトステネスの篩による約数列挙前計算</a>
1. （★2.7／diff <font color="yellowgreen">2351</font>／2問）<a href="#頂点の纏め上げによる次元削減" class="tag">頂点の纏め上げによる次元削減</a>
1. （★2.7／diff <font color="yellowgreen">2351</font>／2問）<a href="#隣接行列による遷移計算" class="tag">隣接行列による遷移計算</a>
1. （★2.8／diff <font color="blue">1733</font>／3問）<a href="#閉路検出" class="tag">閉路検出</a>
1. （★2.8／diff <font color="blue">1882</font>／5問）<a href="#イベントソート" class="tag">イベントソート</a>
1. （★2.8／diff <font color="blue">1896</font>／5問）<a href="#サンプルから推測" class="tag">サンプルから推測</a>
1. （★2.8／diff <font color="blue">1922</font>／6問）<a href="#sorted set" class="tag">sorted set</a>
1. （★2.8／diff <font color="blue">1961</font>／3問）<a href="#最適化を各寄与の最適化に緩和" class="tag">最適化を各寄与の最適化に緩和</a>
1. （★2.8／diff <font color="yellowgreen">2013</font>／16問）<a href="#B進法" class="tag">B進法</a>
1. （★2.8／diff <font color="yellowgreen">2029</font>／13問）<a href="#区間加算更新" class="tag">区間加算更新</a>
1. （★2.8／diff <font color="yellowgreen">2032</font>／9問）<a href="#約数の走査を倍数の走査に帰着" class="tag">約数の走査を倍数の走査に帰着</a>
1. （★2.8／diff <font color="yellowgreen">2035</font>／15問）<a href="#数え上げを総和計算に帰着" class="tag">数え上げを総和計算に帰着</a>
1. （★2.8／diff <font color="yellowgreen">2036</font>／11問）<a href="#平面走査" class="tag">平面走査</a>
1. （★2.8／diff <font color="yellowgreen">2050</font>／18問）<a href="#フェニック木" class="tag">フェニック木</a>／BIT
1. （★2.8／diff <font color="yellowgreen">2052</font>／3問）<a href="#区間の重複度計算" class="tag">区間の重複度計算</a>
1. （★2.8／diff <font color="yellowgreen">2055</font>／4問）<a href="#超頂点追加" class="tag">超頂点追加</a>
1. （★2.8／diff <font color="yellowgreen">2058</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)）<a href="#押し付け戦略" class="tag">押し付け戦略</a>
1. （★2.8／diff <font color="yellowgreen">2076</font>／8問）<a href="#素因数分解による付値計算" class="tag">素因数分解による付値計算</a>
1. （★2.8／diff <font color="yellowgreen">2081</font>／3問）<a href="#オイラー関数計算" class="tag">オイラー関数計算</a>
1. （★2.8／diff <font color="yellowgreen">2125</font>／13問）<a href="#座標圧縮" class="tag">座標圧縮</a>／座圧
1. （★2.8／diff <font color="yellowgreen">2133</font>／5問）<a href="#冪等重みの最短経路長計算" class="tag">冪等重みの最短経路長計算</a>
1. （★2.8／diff <font color="yellowgreen">2134</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)）<a href="#高さ奇数ニム和" class="tag">高さ奇数ニム和</a>
1. （★2.8／diff <font color="yellowgreen">2253</font>／5問）<a href="#$45$度回転" class="tag">$45$度回転</a>
1. （★2.8／diff <font color="yellowgreen">2254</font>／3問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)）<a href="#最終手番の任意性" class="tag">最終手番の任意性</a>
1. （★2.8／diff <font color="yellowgreen">2269</font>／3問）<a href="#複数ナップサック最適化" class="tag">複数ナップサック最適化</a>
1. （★2.8／diff <font color="yellowgreen">2297</font>／9問）<a href="#既存のアルゴリズムの変形" class="tag">既存のアルゴリズムの変形</a>
1. （★2.8／diff <font color="yellowgreen">2310</font>／3問）<a href="#累積max・min" class="tag">累積max・min</a>
1. （★2.8／diff <font color="orange">2514</font>／4問）<a href="#Convex Hull Trick" class="tag">Convex Hull Trick</a>／CHT
1. （★2.8／diff <font color="orange">2514</font>／4問）<a href="#１次式の族の最大・最小値取得" class="tag">１次式の族の最大・最小値取得</a>
1. （★2.8／diff <font color="orange">2514</font>／5問）<a href="#折れ線を直線族で管理" class="tag">折れ線を直線族で管理</a>
1. （★2.9／diff <font color="yellowgreen">2025</font>／5問）<a href="#osa_k法" class="tag">osa_k法</a>
1. （★2.9／diff <font color="yellowgreen">2091</font>／5問）<a href="#平方分割" class="tag">平方分割</a>
1. （★2.9／diff <font color="yellowgreen">2103</font>／8問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)）<a href="#解法場合分け" class="tag">解法場合分け</a>
1. （★2.9／diff <font color="yellowgreen">2121</font>／5問）<a href="#区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮" class="tag">区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮</a>
1. （★2.9／diff <font color="yellowgreen">2126</font>／9問）<a href="#小さいケースの構築を拡張" class="tag">小さいケースの構築を拡張</a>
1. （★2.9／diff <font color="yellowgreen">2166</font>／6問）<a href="#行列累乗" class="tag">行列累乗</a>
1. （★2.9／diff <font color="yellowgreen">2286</font>／7問）<a href="#ナップサック割り当て数え上げ" class="tag">ナップサック割り当て数え上げ</a>
1. （★3／diff <font color="blue">1725</font>／2問）<a href="#閉路と残りに分割" class="tag">閉路と残りに分割</a>
1. （★3／diff <font color="blue">1849</font>／1問）<a href="#任意mod畳み込み" class="tag">任意mod畳み込み</a>
1. （★3／diff <font color="blue">1919</font>／1問）<a href="#偏角ソート" class="tag">偏角ソート</a>
1. （★3／diff <font color="blue">1927</font>／1問）<a href="#mex取得" class="tag">mex取得</a>
1. （★3／diff <font color="blue">1959</font>／1問）<a href="#最小カット計算" class="tag">最小カット計算</a>
1. （★3／diff <font color="blue">1959</font>／1問）<a href="#最大流計算" class="tag">最大流計算</a>／最大フロー計算
1. （★3／diff <font color="blue">1959</font>／1問）<a href="#最大流最小カット定理" class="tag">最大流最小カット定理</a>／最大フロー最小カット定理
1. （★3／diff <font color="blue">1959</font>／1問）<a href="#従属選択コストなしナップサック最適化" class="tag">従属選択コストなしナップサック最適化</a>
1. （★3／diff <font color="blue">1959</font>／1問）<a href="#スライド最小化" class="tag">スライド最小化</a>
1. （★3／diff <font color="blue">1960</font>／1問）<a href="#区間積取得" class="tag">区間積取得</a>
1. （★3／diff <font color="blue">1961</font>／1問）<a href="#正弦定理" class="tag">正弦定理</a>
1. （★3／diff <font color="blue">1998</font>／1問）<a href="#２次元累積和" class="tag">２次元累積和</a>
1. （★3／diff <font color="blue">1998</font>／1問）<a href="#矩形和取得" class="tag">矩形和取得</a>
1. （★3／diff <font color="yellowgreen">2004</font>／1問）<a href="#焼きなまし法" class="tag">焼きなまし法</a>
1. （★3／diff <font color="yellowgreen">2025</font>／1問）<a href="#素因数分解によるオイラー関数計算" class="tag">素因数分解によるオイラー関数計算</a>
1. （★3／diff <font color="yellowgreen">2028</font>／3問）<a href="#累積和・グリッド上のDPを経路数え上げに翻訳" class="tag">累積和・グリッド上のDPを経路数え上げに翻訳</a>
1. （★3／diff <font color="yellowgreen">2046</font>／1問）<a href="#木の頂点の深さ計算" class="tag">木の頂点の深さ計算</a>
1. （★3／diff <font color="yellowgreen">2047</font>／1問）<a href="#オイラーの規準" class="tag">オイラーの規準</a>
1. （★3／diff <font color="yellowgreen">2047</font>／1問）<a href="#平方剰余判定" class="tag">平方剰余判定</a>
1. （★3／diff <font color="yellowgreen">2048</font>／1問）<a href="#最小費用流計算" class="tag">最小費用流計算</a>
1. （★3／diff <font color="yellowgreen">2051</font>／3問）<a href="#ループ戦略" class="tag">ループ戦略</a>
1. （★3／diff <font color="yellowgreen">2053</font>／2問）<a href="#内積の畳み込み計算" class="tag">内積の畳み込み計算</a>
1. （★3／diff <font color="yellowgreen">2056</font>／1問）<a href="#レベル祖先計算" class="tag">レベル祖先計算</a>
1. （★3／diff <font color="yellowgreen">2056</font>／1問）<a href="#弾性衝突を通過に翻訳して位置関係から復元" class="tag">弾性衝突を通過に翻訳して位置関係から復元</a>
1. （★3／diff <font color="yellowgreen">2056</font>／1問）<a href="#木の頂点の重さ計算" class="tag">木の頂点の重さ計算</a>
1. （★3／diff <font color="yellowgreen">2068</font>／1問）<a href="#経路復元" class="tag">経路復元</a>
1. （★3／diff <font color="yellowgreen">2075</font>／2問）<a href="#四角形を三角形２つや対角線２本に翻訳" class="tag">四角形を三角形２つや対角線２本に翻訳</a>
1. （★3／diff <font color="yellowgreen">2102</font>／4問）<a href="#inplace DP" class="tag">inplace DP</a>
1. （★3／diff <font color="yellowgreen">2105</font>／4問）<a href="#ポラードの$\rho$" class="tag">ポラードの$\rho$</a>
1. （★3／diff <font color="yellowgreen">2121</font>／9問）<a href="#期待値の線形性" class="tag">期待値の線形性</a>
1. （★3／diff <font color="yellowgreen">2124</font>／5問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)）<a href="#総和計算の期待値への帰着" class="tag">総和計算の期待値への帰着</a>
1. （★3／diff <font color="yellowgreen">2125</font>／2問）<a href="#重複選択可ナップサック割り当て数え上げ" class="tag">重複選択可ナップサック割り当て数え上げ</a>
1. （★3／diff <font color="yellowgreen">2125</font>／2問）<a href="#分割方法数え上げ" class="tag">分割方法数え上げ</a>
1. （★3／diff <font color="yellowgreen">2129</font>／2問）<a href="#最適遷移を自己写像に翻訳" class="tag">最適遷移を自己写像に翻訳</a>
1. （★3／diff <font color="yellowgreen">2130</font>／1問）<a href="#累積積" class="tag">累積積</a>
1. （★3／diff <font color="yellowgreen">2130</font>／1問）<a href="#累積積による二項係数計算" class="tag">累積積による二項係数計算</a>
1. （★3／diff <font color="yellowgreen">2134</font>／1問）<a href="#分割数計算" class="tag">分割数計算</a>
1. （★3／diff <font color="yellowgreen">2135</font>／2問）<a href="#高階累積和" class="tag">高階累積和</a>
1. （★3／diff <font color="yellowgreen">2141</font>／1問）<a href="#カタランの三角形計算" class="tag">カタランの三角形計算</a>
1. （★3／diff <font color="yellowgreen">2141</font>／4問）<a href="#ダブリング" class="tag">ダブリング</a>
1. （★3／diff <font color="yellowgreen">2141</font>／2問）<a href="#２次元imos法" class="tag">２次元imos法</a>
1. （★3／diff <font color="yellowgreen">2141</font>／2問）<a href="#矩形加算更新" class="tag">矩形加算更新</a>
1. （★3／diff <font color="yellowgreen">2142</font>／3問）<a href="#フロー" class="tag">フロー</a>
1. （★3／diff <font color="yellowgreen">2143</font>／1問）<a href="#ファンデルモンドの畳み込み" class="tag">ファンデルモンドの畳み込み</a>／ヴァンデルモンドの畳み込み
1. （★3／diff <font color="yellowgreen">2152</font>／2問）<a href="#最近共通祖先計算" class="tag">最近共通祖先計算</a>／LCA計算
1. （★3／diff <font color="yellowgreen">2169</font>／14問）<a href="#DPのデータ構造高速化" class="tag">DPのデータ構造高速化</a>
1. （★3／diff <font color="yellowgreen">2183</font>／1問）<a href="#コーシー・フロベニウスの補題" class="tag">コーシー・フロベニウスの補題</a>／バーンサイドの補題
1. （★3／diff <font color="yellowgreen">2183</font>／1問）<a href="#二面体群" class="tag">二面体群</a>
1. （★3／diff <font color="yellowgreen">2191</font>／1問）<a href="#反射の倍化実装" class="tag">反射の倍化実装</a>
1. （★3／diff <font color="yellowgreen">2194</font>／3問）<a href="#区間max・min取得" class="tag">区間max・min取得</a>／区間最大・最小値取得
1. （★3／diff <font color="yellowgreen">2203</font>／1問）<a href="#乱択" class="tag">乱択</a>
1. （★3／diff <font color="yellowgreen">2207</font>／9問）<a href="#積和の和積化" class="tag">積和の和積化</a>
1. （★3／diff <font color="yellowgreen">2208</font>／2問）<a href="#minimax法" class="tag">minimax法</a>
1. （★3／diff <font color="yellowgreen">2211</font>／6問）<a href="#ゼータ変換" class="tag">ゼータ変換</a>
1. （★3／diff <font color="yellowgreen">2216</font>／2問）<a href="#フビニの定理" class="tag">フビニの定理</a>
1. （★3／diff <font color="yellowgreen">2224</font>／4問）<a href="#既出を検索" class="tag">既出を検索</a>
1. （★3／diff <font color="yellowgreen">2226</font>／5問）<a href="#確率漸化式" class="tag">確率漸化式</a>
1. （★3／diff <font color="yellowgreen">2228</font>／9問、[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)）<a href="#緩和" class="tag">緩和</a>
1. （★3／diff <font color="yellowgreen">2237</font>／1問）<a href="#データ構造初期化" class="tag">データ構造初期化</a>
1. （★3／diff <font color="yellowgreen">2237</font>／1問）<a href="#一対一対応と乱択の可換性" class="tag">一対一対応と乱択の可換性</a>
1. （★3／diff <font color="yellowgreen">2245</font>／1問）<a href="#基底計算" class="tag">基底計算</a>
1. （★3／diff <font color="yellowgreen">2249</font>／1問）<a href="#重み付き木上の頂点間距離取得" class="tag">重み付き木上の頂点間距離取得</a>
1. （★3／diff <font color="yellowgreen">2249</font>／4問）<a href="#無向木の有向化" class="tag">無向木の有向化</a>
1. （★3／diff <font color="yellowgreen">2253</font>／3問）<a href="#自己写像に翻訳" class="tag">自己写像に翻訳</a>
1. （★3／diff <font color="yellowgreen">2269</font>／2問）<a href="#商のfloorの分子をわたる総和計算" class="tag">商のfloorの分子をわたる総和計算</a>／floor_sum
1. （★3／diff <font color="yellowgreen">2282</font>／3問）<a href="#セグメント木" class="tag">セグメント木</a>／セグ木
1. （★3／diff <font color="yellowgreen">2295</font>／1問）<a href="#二分木に翻訳" class="tag">二分木に翻訳</a>
1. （★3／diff <font color="yellowgreen">2297</font>／1問）<a href="#多次元コストナップサック割り当て数え上げ" class="tag">多次元コストナップサック割り当て数え上げ</a>
1. （★3／diff <font color="yellowgreen">2297</font>／4問）<a href="#周期的構築" class="tag">周期的構築</a>
1. （★3／diff <font color="yellowgreen">2301</font>／1問）<a href="#複素共役による絶対値計算" class="tag">複素共役による絶対値計算</a>
1. （★3／diff <font color="yellowgreen">2302</font>／3問）<a href="#タイリング・LightOut可能性を領域の細分による不変量計算に帰着" class="tag">タイリング・LightOut可能性を領域の細分による不変量計算に帰着</a>
1. （★3／diff <font color="yellowgreen">2309</font>／1問）<a href="#ベルトラン・チェビシェフの定理" class="tag">ベルトラン・チェビシェフの定理</a>／ベルトランの公準／ベルトランの仮説
1. （★3／diff <font color="yellowgreen">2309</font>／1問）<a href="#素数に注目する質問" class="tag">素数に注目する質問</a>
1. （★3／diff <font color="yellowgreen">2309</font>／1問）<a href="#対角線に言及する質問" class="tag">対角線に言及する質問</a>
1. （★3／diff <font color="yellowgreen">2311</font>／2問）<a href="#グリッド上の価値最大化" class="tag">グリッド上の価値最大化</a>
1. （★3／diff <font color="yellowgreen">2311</font>／2問）<a href="#矩形max・min取得" class="tag">矩形max・min取得</a>／矩形最大・最小値取得
1. （★3／diff <font color="yellowgreen">2320</font>／6問）<a href="#ローリングハッシュ" class="tag">ローリングハッシュ</a>
1. （★3／diff <font color="yellowgreen">2344</font>／2問）<a href="#連続回数制約を分割の区間長制約に翻訳" class="tag">連続回数制約を分割の区間長制約に翻訳</a>
1. （★3／diff <font color="yellowgreen">2344</font>／1問）<a href="#余因子展開" class="tag">余因子展開</a>
1. （★3／diff <font color="yellowgreen">2352</font>／3問）<a href="#区間の部分列をわたる総和計算をモノイド演算に翻訳" class="tag">区間の部分列をわたる総和計算をモノイド演算に翻訳</a>
1. （★3／diff <font color="yellowgreen">2354</font>／1問）<a href="#Monotone Minima" class="tag">Monotone Minima</a>
1. （★3／diff <font color="yellowgreen">2365</font>／2問）<a href="#剰余を取る前に符号や大小を計算" class="tag">剰余を取る前に符号や大小を計算</a>
1. （★3／diff <font color="yellowgreen">2383</font>／2問）<a href="#bitset高速化" class="tag">bitset高速化</a>
1. （★3／diff <font color="yellowgreen">2385</font>／6問）<a href="#一対一対応" class="tag">一対一対応</a>
1. （★3／diff <font color="yellowgreen">2386</font>／2問）<a href="#SIMD高速化" class="tag">SIMD高速化</a>
1. （★3／diff <font color="yellowgreen">2386</font>／1問）<a href="#平均の指定された区間数え上げ" class="tag">平均の指定された区間数え上げ</a>
1. （★3／diff <font color="yellowgreen">2393</font>／1問）<a href="#剰余の法を動かす総和計算" class="tag">剰余の法を動かす総和計算</a>
1. （★3／diff <font color="yellowgreen">2393</font>／1問）<a href="#剰余を商に翻訳" class="tag">剰余を商に翻訳</a>
1. （★3／diff <font color="orange">2419</font>／1問）<a href="#外接円計算" class="tag">外接円計算</a>
1. （★3／diff <font color="orange">2419</font>／1問）<a href="#第二余弦定理" class="tag">第二余弦定理</a>
1. （★3／diff <font color="orange">2419</font>／1問）<a href="#有理数の大小比較のオーバーフロー回避" class="tag">有理数の大小比較のオーバーフロー回避</a>
1. （★3／diff <font color="orange">2419</font>／1問）<a href="#連分数展開" class="tag">連分数展開</a>
1. （★3／diff <font color="orange">2420</font>／1問）<a href="#完全二部マッチング" class="tag">完全二部マッチング</a>
1. （★3／diff <font color="orange">2423</font>／1問）<a href="#始切片選択ナップサック最適化" class="tag">始切片選択ナップサック最適化</a>
1. （★3／diff <font color="orange">2423</font>／1問）<a href="#始切片選択複数ナップサック最適化" class="tag">始切片選択複数ナップサック最適化</a>
1. （★3／diff <font color="orange">2438</font>／1問）<a href="#相対運動に翻訳" class="tag">相対運動に翻訳</a>
1. （★3／diff <font color="orange">2463</font>／2問）<a href="#区間挿入更新" class="tag">区間挿入更新</a>
1. （★3／diff <font color="orange">2471</font>／1問）<a href="#単調関数の像計算を階差の非零点の数え上げに帰着" class="tag">単調関数の像計算を階差の非零点の数え上げに帰着</a>
1. （★3／diff <font color="orange">2471</font>／1問）<a href="#分枝限定法" class="tag">分枝限定法</a>
1. （★3／diff <font color="orange">2489</font>／1問）<a href="#区間削除更新" class="tag">区間削除更新</a>
1. （★3／diff <font color="orange">2506</font>／2問）<a href="#ワイルドカードの値を変数化" class="tag">ワイルドカードの値を変数化</a>
1. （★3／diff <font color="orange">2656</font>／3問）<a href="#準同型" class="tag">準同型</a>
1. （★3／diff <font color="orange">2729</font>／1問）<a href="#区間乗算更新" class="tag">区間乗算更新</a>
1. （★3／diff <font color="orange">2765</font>／1問）<a href="#１次不等式の充足可能性判定" class="tag">１次不等式の充足可能性判定</a>
1. （★3／diff <font color="red">2833</font>／1問）<a href="#最小被覆半径計算" class="tag">最小被覆半径計算</a>
1. （★3／diffデータなし／1問）<a href="#タイリングによるミラー戦略" class="tag">タイリングによるミラー戦略</a>
1. （★3／diffデータなし／1問）<a href="#辺を頂点とするグラフに翻訳" class="tag">辺を頂点とするグラフに翻訳</a>
1. （★3.1／diff <font color="yellowgreen">2122</font>／5問）<a href="#指定序数の値の計算や始切片数え上げを桁ごとの計算に帰着" class="tag">指定序数の値の計算や始切片数え上げを桁ごとの計算に帰着</a>
1. （★3.1／diff <font color="yellowgreen">2166</font>／5問）<a href="#制約からグラフの種類を特定" class="tag">制約からグラフの種類を特定</a>
1. （★3.1／diff <font color="yellowgreen">2171</font>／3問）<a href="#トポロジカルソート" class="tag">トポロジカルソート</a>
1. （★3.1／diff <font color="yellowgreen">2307</font>／3問）<a href="#区間kth取得" class="tag">区間kth取得</a>
1. （★3.1／diff <font color="yellowgreen">2375</font>／3問）<a href="#互いに素に帰着" class="tag">互いに素に帰着</a>
1. （★3.1／diff <font color="orange">2431</font>／4問）<a href="#メビウス変換" class="tag">メビウス変換</a>
1. （★3.1／diff <font color="orange">2440</font>／3問）<a href="#約数ゼータ変換" class="tag">約数ゼータ変換</a>
1. （★3.1／diff <font color="orange">2534</font>／3問）<a href="#最長共通接頭辞計算" class="tag">最長共通接頭辞計算</a>／LCP計算／Z-algorithm
1. （★3.2／diff <font color="yellowgreen">2192</font>／2問）<a href="#Moのアルゴリズム" class="tag">Moのアルゴリズム</a>
1. （★3.2／diff <font color="yellowgreen">2218</font>／6問）<a href="#区間max・min更新" class="tag">区間max・min更新</a>／区間最大・最小値更新／区間chmax・chmin
1. （★3.2／diff <font color="yellowgreen">2218</font>／6問）<a href="#双対セグメント木" class="tag">双対セグメント木</a>
1. （★3.2／diff <font color="yellowgreen">2230</font>／5問）<a href="#十分大きな法で計算" class="tag">十分大きな法で計算</a>
1. （★3.2／diff <font color="yellowgreen">2255</font>／6問）<a href="#期待値漸化式" class="tag">期待値漸化式</a>
1. （★3.2／diff <font color="yellowgreen">2341</font>／2問）<a href="#指数と対数による冪乗計算" class="tag">指数と対数による冪乗計算</a>
1. （★3.2／diff <font color="yellowgreen">2352</font>／2問）<a href="#外積・サラスの公式による行列式計算" class="tag">外積・サラスの公式による行列式計算</a>
1. （★3.2／diff <font color="yellowgreen">2352</font>／2問）<a href="#行列式と面積・体積の関係" class="tag">行列式と面積・体積の関係</a>
1. （★3.2／diff <font color="yellowgreen">2358</font>／2問）<a href="#フロベニウス数に注目" class="tag">フロベニウス数に注目</a>
1. （★3.2／diff <font color="yellowgreen">2383</font>／4問）<a href="#調和数列による計算量評価" class="tag">調和数列による計算量評価</a>
1. （★3.2／diff <font color="yellowgreen">2399</font>／8問）<a href="#同値関係" class="tag">同値関係</a>
1. （★3.2／diff <font color="orange">2425</font>／2問）<a href="#総和の指定された部分列数え上げ" class="tag">総和の指定された部分列数え上げ</a>
1. （★3.2／diff <font color="orange">2447</font>／2問）<a href="#集合族による帰属関係で類別" class="tag">集合族による帰属関係で類別</a>
1. （★3.2／diff <font color="orange">2454</font>／5問）<a href="#マージ" class="tag">マージ</a>
1. （★3.2／diff <font color="orange">2454</font>／4問）<a href="#区間を中間で分割してマージ" class="tag">区間を中間で分割してマージ</a>
1. （★3.2／diff <font color="orange">2493</font>／2問）<a href="#階数計算" class="tag">階数計算</a>
1. （★3.2／diff <font color="orange">2493</font>／2問）<a href="#行列の簡約階段化" class="tag">行列の簡約階段化</a>
1. （★3.2／diff <font color="orange">2641</font>／3問）<a href="#全方位木DP" class="tag">全方位木DP</a>
1. （★3.3／diff <font color="yellowgreen">2347</font>／3問）<a href="#剰余による確率的判定" class="tag">剰余による確率的判定</a>
1. （★3.3／diff <font color="orange">2404</font>／13問）<a href="#線形代数" class="tag">線形代数</a>
1. （★3.3／diff <font color="orange">2412</font>／3問）<a href="#キュー" class="tag">キュー</a>／queue
1. （★3.3／diff <font color="orange">2686</font>／3問）<a href="#多倍長整数" class="tag">多倍長整数</a>
1. （★3.3／diff <font color="orange">2706</font>／3問）<a href="#メビウスの反転公式" class="tag">メビウスの反転公式</a>
1. （★3.3／diff <font color="orange">2706</font>／3問）<a href="#約数メビウス変換" class="tag">約数メビウス変換</a>
1. （★3.5／diff <font color="yellowgreen">2117</font>／2問）<a href="#区間等差数列max・min更新" class="tag">区間等差数列max・min更新</a>／区間等差数列最大・最小値更新／区間等差数列chmax・chmin
1. （★3.5／diff <font color="yellowgreen">2348</font>／1問）<a href="#シュトルツ・チェザロの定理" class="tag">シュトルツ・チェザロの定理</a>
1. （★3.5／diff <font color="yellowgreen">2348</font>／1問）<a href="#移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着" class="tag">移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着</a>
1. （★3.5／diff <font color="yellowgreen">2348</font>／1問）<a href="#整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着" class="tag">整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着</a>
1. （★3.5／diff <font color="yellowgreen">2364</font>／1問）<a href="#操作の纏め上げ" class="tag">操作の纏め上げ</a>
1. （★3.5／diff <font color="orange">2401</font>／1問）<a href="#テイラー展開" class="tag">テイラー展開</a>
1. （★3.5／diff <font color="orange">2401</font>／1問）<a href="#積分漸化式" class="tag">積分漸化式</a>
1. （★3.5／diff <font color="orange">2413</font>／2問）<a href="#高速ゼータ変換" class="tag">高速ゼータ変換</a>
1. （★3.5／diff <font color="orange">2421</font>／1問）<a href="#掃き出し法による行列式計算" class="tag">掃き出し法による行列式計算</a>
1. （★3.5／diff <font color="orange">2587</font>／1問）<a href="#冪乗との最大公約数の収束" class="tag">冪乗との最大公約数の収束</a>
1. （★3.5／diff <font color="orange">2643</font>／1問）<a href="#第二種スターリング数計算" class="tag">第二種スターリング数計算</a>
1. （★3.5／diff <font color="orange">2649</font>／1問）<a href="#カタラン数計算" class="tag">カタラン数計算</a>
1. （★3.5／diff <font color="orange">2657</font>／8問）<a href="#桁DP" class="tag">桁DP</a>
1. （★3.5／diff <font color="orange">2722</font>／2問）<a href="#リュカの定理" class="tag">リュカの定理</a>
1. （★3.5／diff <font color="orange">2741</font>／1問）<a href="#階数因数分解" class="tag">階数因数分解</a>
1. （★3.5／diff <font color="red">2960</font>／1問）<a href="#cyclic orderつき全方位木DP" class="tag">cyclic orderつき全方位木DP</a>
1. （★3.6／diff <font color="orange">2461</font>／4問）<a href="#行列式計算" class="tag">行列式計算</a>
1. （★3.7／diff <font color="yellowgreen">2383</font>／2問）<a href="#有向辺反転" class="tag">有向辺反転</a>
1. （★3.7／diff <font color="orange">2462</font>／2問）<a href="#強連結成分分解" class="tag">強連結成分分解</a>／SCC
1. （★3.7／diff <font color="orange">2741</font>／2問）<a href="#遅延セグメント木" class="tag">遅延セグメント木</a>／遅延セグ木
1. （★3.8／diff <font color="orange">2655</font>／4問）<a href="#バケット分割" class="tag">バケット分割</a>
1. （★3.8／diff <font color="orange">2737</font>／3問）<a href="#剰余の定理" class="tag">剰余の定理</a>／因数定理
1. （★3.8／diff <font color="red">2829</font>／3問）<a href="#行列の階段化" class="tag">行列の階段化</a>
1. （★3.8／diff <font color="red">2829</font>／3問）<a href="#掃き出し法" class="tag">掃き出し法</a>
1. （★3.9／diff <font color="orange">2784</font>／12問）<a href="#畳み込み" class="tag">畳み込み</a>
1. （★4／diff <font color="orange">2768</font>／1問）<a href="#小さい法に帰着させる再帰" class="tag">小さい法に帰着させる再帰</a>
1. （★4／diff <font color="orange">2796</font>／11問）<a href="#高速フーリエ変換" class="tag">高速フーリエ変換</a>／数論的変換／FTT／NTT
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
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#半標準ヤングタブローとGelfand-Tsetlinパターンの対応" class="tag">半標準ヤングタブローとGelfand-Tsetlinパターンの対応</a>
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#半標準ヤングタブローと非交差経路の対応" class="tag">半標準ヤングタブローと非交差経路の対応</a>
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#半標準ヤングタブローに翻訳" class="tag">半標準ヤングタブローに翻訳</a>
1. （★5／diff <font color="orange">2795</font>／1問）<a href="#微分計算" class="tag">微分計算</a>
1. （★5／diff <font color="red">2940</font>／2問）<a href="#ヤング図形に翻訳" class="tag">ヤング図形に翻訳</a>
1. （★5／diff <font color="red">3086</font>／1問）<a href="#フック長公式" class="tag">フック長公式</a>
1. （★5／diff <font color="red">3086</font>／1問）<a href="#標準ヤングタブローに翻訳" class="tag">標準ヤングタブローに翻訳</a>
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
1. （★5／diff <font color="darkgoldenrod ">3382</font>／1問）<a href="#残余ネットワーク" class="tag">残余ネットワーク</a>
1. （★5／diff <font color="darkgoldenrod ">3503</font>／1問）<a href="#非負整数をB進法でベクトルに翻訳" class="tag">非負整数をB進法でベクトルに翻訳</a>
1. （★5／diff <font color="darkgoldenrod ">3577</font>／1問）<a href="#P-再帰" class="tag">P-再帰</a>／P-recursive
1. （★5／diff <font color="darkgoldenrod ">3577</font>／1問）<a href="#評価点シフト" class="tag">評価点シフト</a>
1. （★データなし／diffデータなし／1問）<a href="#区間等差数列加算更新" class="tag">区間等差数列加算更新</a>
1. （★データなし／diffデータなし／1問）<a href="#高階差分" class="tag">高階差分</a>／高階階差数列

登録問題数552、登録解法数523、１問あたりの平均登録解法数5.5、１解法あたりの平均登録問題数5.9です。

　
<h2 id="ゼロ除算回避">1. ゼロ除算回避</h2>

### 難易度統計

「ゼロ除算回避」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1／diff <font color="brown">624</font>
- 2024年: ★1／diff <font color="brown">624</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ゼロ除算回避」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2850">No.2850 Make Slimes</a> (yukicoder contest 442 (2024-08-25) - A問題、diff <font color="brown">624</font>)

　
<h2 id="四捨五入計算">2. 四捨五入計算</h2>

### 難易度統計

「四捨五入計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1／diff <font color="brown">783</font>
- 2024年: ★1／diff <font color="brown">783</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「四捨五入計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2647">No.2647 [Cherry 6th Tune A] Wind</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - A問題、diff <font color="brown">783</font>)

　
<h2 id="カレンダー計算">3. カレンダー計算</h2>

### 難易度統計

「カレンダー計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.1／diff <font color="brown">670</font>
- 2024年: ★1／diff <font color="brown">636</font>
- 2023年: ★1／diff <font color="gray">313</font>
- 2022年: ★1.5／diff <font color="green">1095</font>

### レベル別問題一覧

「カレンダー計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2371">No.2371 最大の試練それは起床</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - A問題、diff <font color="gray">313</font>)
- <a href="https://yukicoder.me/problems/no/2789">No.2789 hako111223’s Master Thesis</a> (yukicoder contest 434 (2024-06-21) - A問題、diff <font color="green">803</font>)
- <a href="https://yukicoder.me/problems/no/2842">No.2842 Birthday</a> (yukicoder contest 441 (2024-08-23) - A問題、diff <font color="brown">469</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題、diff <font color="green">1095</font>)

　
<h2 id="切り上げ">4. 切り上げ</h2>

### 難易度統計

「切り上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.2／diff <font color="brown">646</font>
- 2024年: ★1.2／diff <font color="brown">646</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「切り上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2706">No.2706 One Nafmo</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - A問題、diff <font color="gray">159</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2681">No.2681 ゲームセンターの両替</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - C問題、diff <font color="green">1133</font>)

　
<h2 id="実装">5. 実装</h2>

### 難易度統計

「実装」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.2／diff <font color="brown">699</font>
- 2024年: ★1.2／diff <font color="brown">799</font>
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
- <a href="https://yukicoder.me/problems/no/2691">No.2691 Longest Infection Sequence</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - A問題、diff <font color="green">885</font>)
- <a href="https://yukicoder.me/problems/no/2706">No.2706 One Nafmo</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - A問題、diff <font color="gray">159</font>)
- <a href="https://yukicoder.me/problems/no/2707">No.2707 Bag of Words Encryption</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - B問題、diff <font color="gray">217</font>)
- <a href="https://yukicoder.me/problems/no/2714">No.2714 Amaou</a> (yukicoder contest 426 (2024-04-05) - A問題、diff <font color="brown">595</font>)
- <a href="https://yukicoder.me/problems/no/2728">No.2728 Grid Expansion</a> (yukicoder contest 428 (2024-04-19) - A問題、diff <font color="brown">674</font>)
- <a href="https://yukicoder.me/problems/no/2736">No.2736 About half</a> (CPCTF 2024 : PPC (2024-04-20) - A問題、diff <font color="gray">216</font>)
- <a href="https://yukicoder.me/problems/no/2765">No.2765 Cross Product</a> (yukicoder contest 431 (2024-05-31) - A問題、diff <font color="brown">650</font>)
- <a href="https://yukicoder.me/problems/no/2773">No.2773 Wake up Record 1</a> (yukicoder contest 432 (2024-06-07) - A問題、diff <font color="gray">212</font>)
- <a href="https://yukicoder.me/problems/no/2778">No.2778 Is there Same letter?</a> (yukicoder contest 432 (2024-06-07) - F問題、diff <font color="gray">314</font>)
- <a href="https://yukicoder.me/problems/no/2789">No.2789 hako111223’s Master Thesis</a> (yukicoder contest 434 (2024-06-21) - A問題、diff <font color="green">803</font>)
- <a href="https://yukicoder.me/problems/no/2827">No.2827 Enter User Name to Play</a> (yukicoder contest 439 (2024-08-02) - A問題、diff <font color="brown">735</font>)
- <a href="https://yukicoder.me/problems/no/2842">No.2842 Birthday</a> (yukicoder contest 441 (2024-08-23) - A問題、diff <font color="brown">469</font>)
- <a href="https://yukicoder.me/problems/no/2850">No.2850 Make Slimes</a> (yukicoder contest 442 (2024-08-25) - A問題、diff <font color="brown">624</font>)
- <a href="https://yukicoder.me/problems/no/2851">No.2851 Make Pairs</a> (yukicoder contest 442 (2024-08-25) - B問題、diff <font color="brown">774</font>)
- <a href="https://yukicoder.me/problems/no/2960">No.2960 Judgement</a> (yukicoder contest 453 (2024-11-16) - A問題、diff <font color="green">812</font>)

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
- <a href="https://yukicoder.me/problems/no/2680">No.2680 研究室配属</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - B問題、diff <font color="green">922</font>)
- <a href="https://yukicoder.me/problems/no/2692">No.2692 How Many Times Reached?</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - B問題、diff <font color="green">934</font>)
- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)
- <a href="https://yukicoder.me/problems/no/2776">No.2776 Bigger image</a> (yukicoder contest 432 (2024-06-07) - D問題、diff <font color="brown">683</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題、diff <font color="green">939</font>)
- <a href="https://yukicoder.me/problems/no/2509">No.2509 Beam Shateki</a> (yukicoder contest 409 (2023-10-20) - B問題、diff <font color="blue">1980</font>)
- <a href="https://yukicoder.me/problems/no/2731">No.2731 Two Colors</a> (yukicoder contest 428 (2024-04-19) - D問題、diff <font color="deepskyblue">1442</font>)
- <a href="https://yukicoder.me/problems/no/2804">No.2804 Fixer And Ratism</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - B問題、diff <font color="blue">1779</font>)
- <a href="https://yukicoder.me/problems/no/2820">No.2820 Non-Preferred IUPAC Nomenclature</a> (yukicoder contest 438 (2024-07-26) - B問題、diff <font color="blue">1807</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2771">No.2771 Personal Space</a> (yukicoder contest 431 (2024-05-31) - G問題、diff <font color="yellowgreen">2170</font>)

　
<h2 id="貨幣計算">6. 貨幣計算</h2>

### 難易度統計

「貨幣計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.2／diff <font color="green">830</font>
- 2024年: ★1.2／diff <font color="green">830</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「貨幣計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2775">No.2775 Nuisance Balls</a> (yukicoder contest 432 (2024-06-07) - C問題、diff <font color="brown">528</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2681">No.2681 ゲームセンターの両替</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - C問題、diff <font color="green">1133</font>)

　
<h2 id="getline">7. getline</h2>

### 難易度統計

「getline」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.2／diff <font color="deepskyblue">1523</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★1.5／diff <font color="yellowgreen">2185</font>
- 2022年: ★1／diff <font color="green">862</font>

### レベル別問題一覧

「getline」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題、diff <font color="green">862</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

　
<h2 id="64bit整数">8. 64bit整数</h2>

### 難易度統計

「64bit整数」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.4／diff <font color="green">910</font>
- 2024年: ★1.3／diff <font color="green">1013</font>
- 2023年: ★1.4／diff <font color="green">857</font>
- 2022年: ★1.5／diff <font color="green">841</font>

### レベル別問題一覧

「64bit整数」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題、diff <font color="brown">544</font>)
- <a href="https://yukicoder.me/problems/no/2560">No.2560 A_1 < A_2 < ... < A_N</a> (第2回緑以下コンテスト (2023-12-02) - D問題、diff <font color="brown">540</font>)
- <a href="https://yukicoder.me/problems/no/2637">No.2637 Factorize?</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - A問題、diff <font color="green">967</font>)
- <a href="https://yukicoder.me/problems/no/2647">No.2647 [Cherry 6th Tune A] Wind</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - A問題、diff <font color="brown">783</font>)

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
- <a href="https://yukicoder.me/problems/no/2693">No.2693 Sword</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - C問題、diff <font color="deepskyblue">1211</font>)
- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)
- <a href="https://yukicoder.me/problems/no/2709">No.2709 1975 Powers</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - D問題、diff <font color="green">1143</font>)
- <a href="https://yukicoder.me/problems/no/2750">No.2750 Number of Prime Factors</a> (yukicoder contest 429 (2024-05-10) - B問題、diff <font color="green">1026</font>)

　
<h2 id="符号なし64bit整数">9. 符号なし64bit整数</h2>

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

　
<h2 id="経路全探索">10. 経路全探索</h2>

### 難易度統計

「経路全探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">736</font>
- 2024年: ★1.5／diff <font color="brown">736</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「経路全探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)

　
<h2 id="コスト１ナップサック最適化">11. コスト１ナップサック最適化</h2>

### 難易度統計

「コスト１ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="brown">774</font>
- 2024年: ★1.5／diff <font color="brown">774</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「コスト１ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2852">No.2852 Yakitori Optimization Problem</a> (yukicoder contest 442 (2024-08-25) - C問題、diff <font color="brown">774</font>)

　
<h2 id="再帰による多重ループ実装">12. 再帰による多重ループ実装</h2>

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

　
<h2 id="埋め込み">13. 埋め込み</h2>

### 難易度統計

「埋め込み」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="green">873</font>
- 2024年: ★1.5／diff <font color="green">873</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「埋め込み」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2795">No.2795 Perfect Number</a> (yukicoder contest 435 (2024-06-28) - A問題、diff <font color="green">873</font>)

　
<h2 id="選択順依存価値コストなしナップサック最適化">14. 選択順依存価値コストなしナップサック最適化</h2>

### 難易度統計

「選択順依存価値コストなしナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="green">919</font>
- 2024年: ★1.5／diff <font color="green">919</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「選択順依存価値コストなしナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2729">No.2729 Addition and Multiplication in yukicoder (Easy)</a> (yukicoder contest 428 (2024-04-19) - B問題、diff <font color="green">919</font>)

　
<h2 id="試行回数の期待値を各試行の実施確率の和に帰着">15. 試行回数の期待値を各試行の実施確率の和に帰着</h2>

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

　
<h2 id="等差数列と等比数列の各点積の累積和計算">16. 等差数列と等比数列の各点積の累積和計算</h2>

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

　
<h2 id="４重以上のループ">17. ４重以上のループ</h2>

### 難易度統計

「４重以上のループ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="green">976</font>
- 2024年: ★1.5／diff <font color="green">1077</font>
- 2023年: ★1.5／diff <font color="brown">775</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「４重以上のループ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)
- <a href="https://yukicoder.me/problems/no/2671">No.2671 NUPC Decompressor</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - A問題、diff <font color="green">1012</font>)
- <a href="https://yukicoder.me/problems/no/2709">No.2709 1975 Powers</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - D問題、diff <font color="green">1143</font>)

　
<h2 id="商を用いた積のオーバーフロー回避">18. 商を用いた積のオーバーフロー回避</h2>

### 難易度統計

「商を用いた積のオーバーフロー回避」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.5／diff <font color="green">1026</font>
- 2024年: ★1.5／diff <font color="green">1026</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「商を用いた積のオーバーフロー回避」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2750">No.2750 Number of Prime Factors</a> (yukicoder contest 429 (2024-05-10) - B問題、diff <font color="green">1026</font>)

　
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

　
<h2 id="基数の変換">20. 基数の変換</h2>

### 難易度統計

「基数の変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.6／diff <font color="green">894</font>
- 2024年: ★1.6／diff <font color="green">1172</font>
- 2023年: ★1.5／diff <font color="brown">477</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「基数の変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2385">No.2385 Parse Integer with Radix</a> (yukicoder contest 398 (2023-07-21) - A問題、diff <font color="brown">650</font>)
- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)
- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)
- <a href="https://yukicoder.me/problems/no/2729">No.2729 Addition and Multiplication in yukicoder (Easy)</a> (yukicoder contest 428 (2024-04-19) - B問題、diff <font color="green">919</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2649">No.2649 [Cherry 6th Tune C] Anthem Flower</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - C問題、diff <font color="deepskyblue">1322</font>)

　
<h2 id="set">21. set</h2>

### 難易度統計

「set」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.6／diff <font color="green">990</font>
- 2024年: ★1.3／diff <font color="green">864</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1307</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「set」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)
- <a href="https://yukicoder.me/problems/no/2607">No.2607 Add One Digit</a> (yukicoder contest 415 (2024-01-19) - A問題、diff <font color="green">1070</font>)
- <a href="https://yukicoder.me/problems/no/2714">No.2714 Amaou</a> (yukicoder contest 426 (2024-04-05) - A問題、diff <font color="brown">595</font>)
- <a href="https://yukicoder.me/problems/no/2737">No.2737 Compound Word</a> (CPCTF 2024 : PPC (2024-04-20) - B問題、diff <font color="brown">514</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題、diff <font color="deepskyblue">1302</font>)
- <a href="https://yukicoder.me/problems/no/2684">No.2684 折々の色</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - F問題、diff <font color="blue">1790</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)

　
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

　
<h2 id="数値の文字列受け取り">24. 数値の文字列受け取り</h2>

### 難易度統計

「数値の文字列受け取り」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.7／diff <font color="green">1074</font>
- 2024年: ★2.3／diff <font color="blue">1671</font>
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

##### ★★

- <a href="https://yukicoder.me/problems/no/2649">No.2649 [Cherry 6th Tune C] Anthem Flower</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - C問題、diff <font color="deepskyblue">1322</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2734">No.2734 Addition and Multiplication in yukicoder (Hard)</a> (yukicoder contest 428 (2024-04-19) - G問題、diff <font color="yellowgreen">2034</font>)
- <a href="https://yukicoder.me/problems/no/2772">No.2772 Appearing Even Times</a> (yukicoder contest 431 (2024-05-31) - H問題、diff <font color="blue">1925</font>)

　
<h2 id="頻度表">25. 頻度表</h2>

### 難易度統計

「頻度表」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.7／diff <font color="green">1153</font>
- 2024年: ★1.6／diff <font color="green">1006</font>
- 2023年: ★2／diff <font color="deepskyblue">1277</font>
- 2022年: ★2／diff <font color="deepskyblue">1390</font>

### レベル別問題一覧

「頻度表」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2153">No.2153 何コーダーが何人？</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - A問題、diff <font color="brown">566</font>)
- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)
- <a href="https://yukicoder.me/problems/no/2707">No.2707 Bag of Words Encryption</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - B問題、diff <font color="gray">217</font>)
- <a href="https://yukicoder.me/problems/no/2714">No.2714 Amaou</a> (yukicoder contest 426 (2024-04-05) - A問題、diff <font color="brown">595</font>)
- <a href="https://yukicoder.me/problems/no/2778">No.2778 Is there Same letter?</a> (yukicoder contest 432 (2024-06-07) - F問題、diff <font color="gray">314</font>)
- <a href="https://yukicoder.me/problems/no/2851">No.2851 Make Pairs</a> (yukicoder contest 442 (2024-08-25) - B問題、diff <font color="brown">774</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題、diff <font color="gray">342</font>)
- <a href="https://yukicoder.me/problems/no/2777">No.2777 Wild Flush</a> (yukicoder contest 432 (2024-06-07) - E問題、diff <font color="brown">683</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題、diff <font color="green">1093</font>)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題、diff <font color="green">1069</font>)
- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)
- <a href="https://yukicoder.me/problems/no/2715">No.2715 Unique Chimatagram</a> (yukicoder contest 426 (2024-04-05) - B問題、diff <font color="deepskyblue">1482</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題、diff <font color="blue">1802</font>)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2618">No.2618 除霊</a> (yukicoder contest 416 (2024-01-26) - E問題、diff <font color="yellowgreen">2255</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="整礎性">26. 整礎性</h2>

### 難易度統計

「整礎性」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.7／diff <font color="deepskyblue">1202</font>
- 2024年: ★1.5／diff <font color="green">1132</font>
- 2023年: ★2／diff <font color="deepskyblue">1273</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「整礎性」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2766">No.2766 Delicious Multiply Spice</a> (yukicoder contest 431 (2024-05-31) - B問題、diff <font color="green">1132</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2426">No.2426 Select Plus or Minus</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - C問題、diff <font color="deepskyblue">1273</font>)

　
<h2 id="証明をなぞる構築">27. 証明をなぞる構築</h2>

### 難易度統計

「証明をなぞる構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.7／diff <font color="deepskyblue">1228</font>
- 2024年: ★1.7／diff <font color="deepskyblue">1228</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「証明をなぞる構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2608">No.2608 Divide into two</a> (yukicoder contest 415 (2024-01-19) - B問題、diff <font color="deepskyblue">1247</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2655">No.2655 Increasing Strides</a> (yukicoder contest 419 (2024-03-01) - A問題、diff <font color="deepskyblue">1210</font>)

　
<h2 id="解の公式">28. 解の公式</h2>

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

　
<h2 id="剰余計算を桁の線形和に帰着">29. 剰余計算を桁の線形和に帰着</h2>

### 難易度統計

「剰余計算を桁の線形和に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.7／diff <font color="blue">1775</font>
- 2024年: ★1.5／diff <font color="deepskyblue">1276</font>
- 2023年: ★2／diff <font color="yellowgreen">2275</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「剰余計算を桁の線形和に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)

　
<h2 id="特殊な入出力">30. 特殊な入出力</h2>

### 難易度統計

「特殊な入出力」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.8／diff <font color="deepskyblue">1226</font>
- 2024年: ★2.9／diff <font color="yellowgreen">2155</font>
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

##### ★★★

- <a href="https://yukicoder.me/problems/no/2734">No.2734 Addition and Multiplication in yukicoder (Hard)</a> (yukicoder contest 428 (2024-04-19) - G問題、diff <font color="yellowgreen">2034</font>)
- <a href="https://yukicoder.me/problems/no/2772">No.2772 Appearing Even Times</a> (yukicoder contest 431 (2024-05-31) - H問題、diff <font color="blue">1925</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="外積計算">31. 外積計算</h2>

### 難易度統計

「外積計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.8／diff <font color="deepskyblue">1243</font>
- 2024年: ★1.2／diff <font color="brown">792</font>
- 2023年: ★3／diff <font color="yellowgreen">2147</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「外積計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2765">No.2765 Cross Product</a> (yukicoder contest 431 (2024-05-31) - A問題、diff <font color="brown">650</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2790">No.2790 Athena 3</a> (yukicoder contest 434 (2024-06-21) - B問題、diff <font color="green">934</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)

　
<h2 id="シミュレーション">32. シミュレーション</h2>

### 難易度統計

「シミュレーション」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.9／diff <font color="deepskyblue">1335</font>
- 2024年: ★2／diff <font color="deepskyblue">1529</font>
- 2023年: ★1.9／diff <font color="deepskyblue">1216</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「シミュレーション」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2850">No.2850 Make Slimes</a> (yukicoder contest 442 (2024-08-25) - A問題、diff <font color="brown">624</font>)
- <a href="https://yukicoder.me/problems/no/2960">No.2960 Judgement</a> (yukicoder contest 453 (2024-11-16) - A問題、diff <font color="green">812</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題、diff <font color="green">999</font>)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)
- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題、diff <font color="brown">744</font>)
- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)
- <a href="https://yukicoder.me/problems/no/2401">No.2401 Dirty Shoes and Stairs</a> (yukicoder contest 400 (2023-08-04) - C問題、diff <font color="brown">603</font>)
- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)
- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)
- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)
- <a href="https://yukicoder.me/problems/no/2680">No.2680 研究室配属</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - B問題、diff <font color="green">922</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題、diff <font color="green">939</font>)
- <a href="https://yukicoder.me/problems/no/2363">No.2363 k-bonacci</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2731">No.2731 Two Colors</a> (yukicoder contest 428 (2024-04-19) - D問題、diff <font color="deepskyblue">1442</font>)
- <a href="https://yukicoder.me/problems/no/2804">No.2804 Fixer And Ratism</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - B問題、diff <font color="blue">1779</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)
- <a href="https://yukicoder.me/problems/no/2745">No.2745 String Swap Battle</a> (CPCTF 2024 : PPC (2024-04-20) - J問題、diff <font color="yellowgreen">2309</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)
- <a href="https://yukicoder.me/problems/no/2431">No.2431 Viral Hotel</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - H問題、diff <font color="orange">2628</font>)
- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2631">No.2631 Rectangle Grid Game</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - D問題、diff <font color="yellowgreen">2176</font>)
- <a href="https://yukicoder.me/problems/no/2771">No.2771 Personal Space</a> (yukicoder contest 431 (2024-05-31) - G問題、diff <font color="yellowgreen">2170</font>)

　
<h2 id="連想配列">33. 連想配列</h2>

### 難易度統計

「連想配列」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.9／diff <font color="deepskyblue">1361</font>
- 2024年: ★2／diff <font color="deepskyblue">1245</font>
- 2023年: ★2／diff <font color="blue">1664</font>
- 2022年: ★1.7／diff <font color="green">1184</font>

### レベル別問題一覧

「連想配列」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2153">No.2153 何コーダーが何人？</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - A問題、diff <font color="brown">566</font>)
- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)
- <a href="https://yukicoder.me/problems/no/2707">No.2707 Bag of Words Encryption</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - B問題、diff <font color="gray">217</font>)
- <a href="https://yukicoder.me/problems/no/2714">No.2714 Amaou</a> (yukicoder contest 426 (2024-04-05) - A問題、diff <font color="brown">595</font>)
- <a href="https://yukicoder.me/problems/no/2778">No.2778 Is there Same letter?</a> (yukicoder contest 432 (2024-06-07) - F問題、diff <font color="gray">314</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題、diff <font color="green">1093</font>)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)
- <a href="https://yukicoder.me/problems/no/2715">No.2715 Unique Chimatagram</a> (yukicoder contest 426 (2024-04-05) - B問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2779">No.2779 Don't make Pair</a> (yukicoder contest 432 (2024-06-07) - G問題、diff <font color="green">951</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題、diff <font color="blue">1802</font>)
- <a href="https://yukicoder.me/problems/no/2510">No.2510 Six Cube Sum Counting</a> (yukicoder contest 409 (2023-10-20) - C問題、diff <font color="yellowgreen">2219</font>)
- <a href="https://yukicoder.me/problems/no/2684">No.2684 折々の色</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - F問題、diff <font color="blue">1790</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2769">No.2769 Number of Rhombi</a> (yukicoder contest 431 (2024-05-31) - E問題、diff <font color="yellowgreen">2003</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="指定序数の値の計算や始切片数え上げや１次元最近点計算をソートに帰着">34. 指定序数の値の計算や始切片数え上げや１次元最近点計算をソートに帰着</h2>

### 難易度統計

「指定序数の値の計算や始切片数え上げや１次元最近点計算をソートに帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★1.9／diff <font color="deepskyblue">1392</font>
- 2024年: ★1.8／diff <font color="deepskyblue">1381</font>
- 2023年: ★2.1／diff <font color="deepskyblue">1410</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「指定序数の値の計算や始切片数え上げや１次元最近点計算をソートに帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2671">No.2671 NUPC Decompressor</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - A問題、diff <font color="green">1012</font>)
- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)
- <a href="https://yukicoder.me/problems/no/2803">No.2803 Bocching Star</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - A問題、diff <font color="green">939</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題、diff <font color="green">1174</font>)
- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)
- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)

　
<h2 id="巡回置換表示">35. 巡回置換表示</h2>

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

　
<h2 id="底辺と高さを用いた三角形の面積計算">36. 底辺と高さを用いた三角形の面積計算</h2>

### 難易度統計

「底辺と高さを用いた三角形の面積計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="green">1180</font>
- 2024年: ★2／diff <font color="deepskyblue">1208</font>
- 2023年: ★2／diff <font color="green">1166</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「底辺と高さを用いた三角形の面積計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2515">No.2515 Similar Triangles</a> (yukicoder contest 410 (2023-10-27) - A問題、diff <font color="gray">371</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2555">No.2555 Intriguing Triangle</a> (Advent Calendar Contest 2023 (2023-12-01) - A問題、diff <font color="blue">1961</font>)

　
<h2 id="符号なし整数によるオーバーフロー回避">37. 符号なし整数によるオーバーフロー回避</h2>

### 難易度統計

「符号なし整数によるオーバーフロー回避」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1228</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2／diff <font color="deepskyblue">1228</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「符号なし整数によるオーバーフロー回避」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2420">No.2420 Simple Problem</a> (MMA Contest 016 (2023-08-12) - G問題、diff <font color="deepskyblue">1228</font>)

　
<h2 id="サンプルに帰着">38. サンプルに帰着</h2>

### 難易度統計

「サンプルに帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1242</font>
- 2024年: ★1.5／diff <font color="brown">543</font>
- 2023年: ★2.7／diff <font color="blue">1869</font>
- 2022年: ★2／diff <font color="deepskyblue">1313</font>

### レベル別問題一覧

「サンプルに帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)
- <a href="https://yukicoder.me/problems/no/2614">No.2614 Delete ABC</a> (yukicoder contest 416 (2024-01-26) - A問題、diff <font color="gray">365</font>)
- <a href="https://yukicoder.me/problems/no/2679">No.2679 MODice</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - A問題、diff <font color="brown">721</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題、diff <font color="yellowgreen">2039</font>)
- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題、diff <font color="blue">1768</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題、diff <font color="blue">1971</font>)

　
<h2 id="区間線形結合取得">39. 区間線形結合取得</h2>

### 難易度統計

「区間線形結合取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1276</font>
- 2024年: ★2／diff <font color="deepskyblue">1276</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間線形結合取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2694">No.2694 The Early Bird Catches The Worm</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - D問題、diff <font color="deepskyblue">1276</font>)

　
<h2 id="区間選択ナップサック最適化">40. 区間選択ナップサック最適化</h2>

### 難易度統計

「区間選択ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1276</font>
- 2024年: ★2／diff <font color="deepskyblue">1276</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間選択ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2694">No.2694 The Early Bird Catches The Worm</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - D問題、diff <font color="deepskyblue">1276</font>)

　
<h2 id="最近点計算">41. 最近点計算</h2>

### 難易度統計

「最近点計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1301</font>
- 2024年: ★2／diff <font color="blue">1624</font>
- 2023年: ★2／diff <font color="brown">657</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最近点計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2803">No.2803 Bocching Star</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - A問題、diff <font color="green">939</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)

　
<h2 id="相似">42. 相似</h2>

### 難易度統計

「相似」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1306</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2025</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★1.5／diff <font color="brown">588</font>

### レベル別問題一覧

「相似」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2628">No.2628 Shrinkage</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - A問題、diff <font color="yellowgreen">2025</font>)

　
<h2 id="始切片の比較を最大要素の比較に帰着">43. 始切片の比較を最大要素の比較に帰着</h2>

### 難易度統計

「始切片の比較を最大要素の比較に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1318</font>
- 2024年: ★2／diff <font color="deepskyblue">1318</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「始切片の比較を最大要素の比較に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2836">No.2836 Comment Out</a> (yukicoder contest 440 (2024-08-09) - B問題、diff <font color="deepskyblue">1318</font>)

　
<h2 id="lower_bound・upper_bound取得">44. lower_bound・upper_bound取得</h2>

### 難易度統計

「lower_bound・upper_bound取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1319</font>
- 2024年: ★1.5／diff <font color="green">990</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="blue">1649</font>

### レベル別問題一覧

「lower_bound・upper_bound取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)

　
<h2 id="商の剰余計算を大きい法に帰着">45. 商の剰余計算を大きい法に帰着</h2>

### 難易度統計

「商の剰余計算を大きい法に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1322</font>
- 2024年: ★2／diff <font color="deepskyblue">1322</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「商の剰余計算を大きい法に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2649">No.2649 [Cherry 6th Tune C] Anthem Flower</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - C問題、diff <font color="deepskyblue">1322</font>)

　
<h2 id="負コストナップサック最適化">46. 負コストナップサック最適化</h2>

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

　
<h2 id="階乗による多項係数計算">47. 階乗による多項係数計算</h2>

### 難易度統計

「階乗による多項係数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1356</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★2／diff <font color="deepskyblue">1356</font>

### レベル別問題一覧

「階乗による多項係数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)

　
<h2 id="多項係数計算">48. 多項係数計算</h2>

### 難易度統計

「多項係数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1356</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★2／diff <font color="deepskyblue">1356</font>

### レベル別問題一覧

「多項係数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)

　
<h2 id="連結リスト">49. 連結リスト</h2>

### 難易度統計

「連結リスト」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1366</font>
- 2024年: ★2／diff <font color="deepskyblue">1366</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「連結リスト」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2740">No.2740 Old Maid</a> (CPCTF 2024 : PPC (2024-04-20) - E問題、diff <font color="deepskyblue">1366</font>)

　
<h2 id="非連結性を壁の８方向移動による連結性に翻訳">50. 非連結性を壁の８方向移動による連結性に翻訳</h2>

### 難易度統計

「非連結性を壁の８方向移動による連結性に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1379</font>
- 2024年: ★1.5／diff <font color="green">844</font>
- 2023年: ★2.5／diff <font color="blue">1915</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「非連結性を壁の８方向移動による連結性に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2843">No.2843 Birthday Present Struggle</a> (yukicoder contest 441 (2024-08-23) - B問題、diff <font color="green">844</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2328">No.2328 Build Walls</a> (MMA Contest 015  (2023-05-28) - G問題、diff <font color="blue">1915</font>)

　
<h2 id="最小公倍数の約数関係判定を最大公約数の最小公倍数計算に帰着">51. 最小公倍数の約数関係判定を最大公約数の最小公倍数計算に帰着</h2>

### 難易度統計

「最小公倍数の約数関係判定を最大公約数の最小公倍数計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1447</font>
- 2024年: ★2／diff <font color="deepskyblue">1447</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最小公倍数の約数関係判定を最大公約数の最小公倍数計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)

　
<h2 id="全探索">52. 全探索</h2>

### 難易度統計

「全探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1450</font>
- 2024年: ★2／diff <font color="deepskyblue">1481</font>
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
- <a href="https://yukicoder.me/problems/no/2737">No.2737 Compound Word</a> (CPCTF 2024 : PPC (2024-04-20) - B問題、diff <font color="brown">514</font>)
- <a href="https://yukicoder.me/problems/no/2778">No.2778 Is there Same letter?</a> (yukicoder contest 432 (2024-06-07) - F問題、diff <font color="gray">314</font>)

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
- <a href="https://yukicoder.me/problems/no/2638">No.2638 Initial fare</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - B問題、diff <font color="blue">1624</font>)
- <a href="https://yukicoder.me/problems/no/2671">No.2671 NUPC Decompressor</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - A問題、diff <font color="green">1012</font>)
- <a href="https://yukicoder.me/problems/no/2692">No.2692 How Many Times Reached?</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - B問題、diff <font color="green">934</font>)
- <a href="https://yukicoder.me/problems/no/2693">No.2693 Sword</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - C問題、diff <font color="deepskyblue">1211</font>)
- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)
- <a href="https://yukicoder.me/problems/no/2709">No.2709 1975 Powers</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - D問題、diff <font color="green">1143</font>)
- <a href="https://yukicoder.me/problems/no/2721">No.2721 "Don't say N" Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - A問題、diff <font color="brown">426</font>)
- <a href="https://yukicoder.me/problems/no/2790">No.2790 Athena 3</a> (yukicoder contest 434 (2024-06-21) - B問題、diff <font color="green">934</font>)
- <a href="https://yukicoder.me/problems/no/2803">No.2803 Bocching Star</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - A問題、diff <font color="green">939</font>)

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
- <a href="https://yukicoder.me/problems/no/2711">No.2711 Connecting Lights</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - F問題、diff <font color="deepskyblue">1396</font>)
- <a href="https://yukicoder.me/problems/no/2715">No.2715 Unique Chimatagram</a> (yukicoder contest 426 (2024-04-05) - B問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2730">No.2730 Two Types Luggage</a> (yukicoder contest 428 (2024-04-19) - C問題、diff <font color="deepskyblue">1279</font>)
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)
- <a href="https://yukicoder.me/problems/no/2819">No.2819 Binary Binary-Operator</a> (yukicoder contest 438 (2024-07-26) - A問題、diff <font color="deepskyblue">1596</font>)

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
- <a href="https://yukicoder.me/problems/no/2630">No.2630 Colorful Vertices and Cheapest Paths </a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - C問題、diff <font color="deepskyblue">1435</font>)
- <a href="https://yukicoder.me/problems/no/2672">No.2672 Subset Xor Sum</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - B問題、diff <font color="deepskyblue">1416</font>)
- <a href="https://yukicoder.me/problems/no/2684">No.2684 折々の色</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - F問題、diff <font color="blue">1790</font>)
- <a href="https://yukicoder.me/problems/no/2696">No.2696 Sign Creation</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - F問題、diff <font color="blue">1803</font>)

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
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2725">No.2725 Coprime Game 2</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - E問題、diff <font color="blue">1944</font>)
- <a href="https://yukicoder.me/problems/no/2732">No.2732 Similar Permutations</a> (yukicoder contest 428 (2024-04-19) - E問題、diff <font color="yellowgreen">2203</font>)
- <a href="https://yukicoder.me/problems/no/2858">No.2858 Make a Palindrome</a> (yukicoder contest 442 (2024-08-25) - I問題、diff <font color="yellowgreen">2147</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)

　
<h2 id="重複選択可ナップサック最適化">53. 重複選択可ナップサック最適化</h2>

### 難易度統計

「重複選択可ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1458</font>
- 2024年: ★2.5／diff <font color="blue">1900</font>
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
- <a href="https://yukicoder.me/problems/no/2701">No.2701 A cans -> B cans</a> (yukicoder contest 424 (2024-03-29) - C問題、diff <font color="blue">1900</font>)

　
<h2 id="中国剰余定理">54. 中国剰余定理</h2>

### 難易度統計

「中国剰余定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1476</font>
- 2024年: ★3／diff <font color="blue">1849</font>
- 2023年: ★1.5／diff <font color="deepskyblue">1290</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「中国剰余定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2558">No.2558 中国剰余定理</a> (第2回緑以下コンテスト (2023-12-02) - B問題、diff <font color="gray">306</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)

　
<h2 id="ソート前の添字復元">55. ソート前の添字復元</h2>

### 難易度統計

「ソート前の添字復元」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1551</font>
- 2024年: ★2／diff <font color="blue">1635</font>
- 2023年: ★2／diff <font color="deepskyblue">1426</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ソート前の添字復元」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2493">No.2493 K-th in L2 with L1</a> (yukicoder contest 407 (2023-10-06) - B問題、diff <font color="green">1182</font>)
- <a href="https://yukicoder.me/problems/no/2803">No.2803 Bocching Star</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - A問題、diff <font color="green">939</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2353">No.2353 Guardian Dogs in Spring</a> (yukicoder contest 393 (2023-06-16) - D問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2745">No.2745 String Swap Battle</a> (CPCTF 2024 : PPC (2024-04-20) - J問題、diff <font color="yellowgreen">2309</font>)

　
<h2 id="素因数分解による最小公倍数計算">56. 素因数分解による最小公倍数計算</h2>

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

　
<h2 id="置換の合成">57. 置換の合成</h2>

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

　
<h2 id="質問の全探索による質問決定">58. 質問の全探索による質問決定</h2>

### 難易度統計

「質問の全探索による質問決定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="deepskyblue">1596</font>
- 2024年: ★2／diff <font color="deepskyblue">1596</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「質問の全探索による質問決定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2819">No.2819 Binary Binary-Operator</a> (yukicoder contest 438 (2024-07-26) - A問題、diff <font color="deepskyblue">1596</font>)

　
<h2 id="ルジャンドルの公式">59. ルジャンドルの公式</h2>

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

　
<h2 id="多次元コストを１次元に翻訳">60. 多次元コストを１次元に翻訳</h2>

### 難易度統計

「多次元コストを１次元に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="blue">1626</font>
- 2024年: ★2／diff <font color="blue">1626</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「多次元コストを１次元に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2739">No.2739 Time is money</a> (CPCTF 2024 : PPC (2024-04-20) - D問題、diff <font color="blue">1695</font>)
- <a href="https://yukicoder.me/problems/no/2741">No.2741 Balanced Choice</a> (CPCTF 2024 : PPC (2024-04-20) - F問題、diff <font color="deepskyblue">1557</font>)

　
<h2 id="多次元コスト重複選択可ナップサック最適化">61. 多次元コスト重複選択可ナップサック最適化</h2>

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

　
<h2 id="倍数判定を約数列挙に帰着">62. 倍数判定を約数列挙に帰着</h2>

### 難易度統計

「倍数判定を約数列挙に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="blue">1659</font>
- 2024年: ★2／diff <font color="blue">1659</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「倍数判定を約数列挙に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)

　
<h2 id="区間要素数取得を始切片数え上げに帰着">63. 区間要素数取得を始切片数え上げに帰着</h2>

### 難易度統計

「区間要素数取得を始切片数え上げに帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2／diff <font color="blue">1695</font>
- 2024年: ★1.5／diff <font color="green">990</font>
- 2023年: ★2.5／diff <font color="orange">2401</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間要素数取得を始切片数え上げに帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)

　
<h2 id="到達可能性判定">64. 到達可能性判定</h2>

### 難易度統計

「到達可能性判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1227</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1430</font>
- 2023年: ★2／diff <font color="green">822</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「到達可能性判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2402">No.2402 Dirty Stairs and Shoes</a> (yukicoder contest 400 (2023-08-04) - D問題、diff <font color="green">822</font>)
- <a href="https://yukicoder.me/problems/no/2836">No.2836 Comment Out</a> (yukicoder contest 440 (2024-08-09) - B問題、diff <font color="deepskyblue">1318</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2646">No.2646 Cycle Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2780">No.2780 The Bottle Imp</a> (yukicoder contest 432 (2024-06-07) - H問題、diff <font color="deepskyblue">1542</font>)

　
<h2 id="遷移の収束">65. 遷移の収束</h2>

### 難易度統計

「遷移の収束」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1273</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1440</font>
- 2023年: ★2／diff <font color="green">939</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「遷移の収束」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題、diff <font color="green">939</font>)
- <a href="https://yukicoder.me/problems/no/2648">No.2648 [Cherry 6th Tune D] 一次元の馬</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - B問題、diff <font color="green">912</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2742">No.2742 Car Flow</a> (CPCTF 2024 : PPC (2024-04-20) - G問題、diff <font color="blue">1969</font>)

　
<h2 id="三角形の面積計算">66. 三角形の面積計算</h2>

### 難易度統計

「三角形の面積計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1324</font>
- 2024年: ★1.7／diff <font color="green">1071</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1493</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「三角形の面積計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2515">No.2515 Similar Triangles</a> (yukicoder contest 410 (2023-10-27) - A問題、diff <font color="gray">371</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2790">No.2790 Athena 3</a> (yukicoder contest 434 (2024-06-21) - B問題、diff <font color="green">934</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)
- <a href="https://yukicoder.me/problems/no/2555">No.2555 Intriguing Triangle</a> (Advent Calendar Contest 2023 (2023-12-01) - A問題、diff <font color="blue">1961</font>)

　
<h2 id="ギャグ">67. ギャグ</h2>

### 難易度統計

「ギャグ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1384</font>
- 2024年: ★1.3／diff <font color="green">837</font>
- 2023年: ★2.5／diff <font color="blue">1685</font>
- 2022年: ★2.2／diff <font color="deepskyblue">1423</font>

### レベル別問題一覧

「ギャグ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2637">No.2637 Factorize?</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - A問題、diff <font color="green">967</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2679">No.2679 MODice</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - A問題、diff <font color="brown">721</font>)
- <a href="https://yukicoder.me/problems/no/2835">No.2835 Take and Flip</a> (yukicoder contest 440 (2024-08-09) - A問題、diff <font color="green">819</font>)
- <a href="https://yukicoder.me/problems/no/2843">No.2843 Birthday Present Struggle</a> (yukicoder contest 441 (2024-08-23) - B問題、diff <font color="green">844</font>)

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

　
<h2 id="多次元コストナップサック最適化">68. 多次元コストナップサック最適化</h2>

### 難易度統計

「多次元コストナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1430</font>
- 2024年: ★2／diff <font color="deepskyblue">1557</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1534</font>
- 2022年: ★1.5／diff <font color="green">1095</font>

### レベル別問題一覧

「多次元コストナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2741">No.2741 Balanced Choice</a> (CPCTF 2024 : PPC (2024-04-20) - F問題、diff <font color="deepskyblue">1557</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題、diff <font color="green">875</font>)

　
<h2 id="小数型">69. 小数型</h2>

### 難易度統計

「小数型」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1452</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2038</font>
- 2023年: ★2.2／diff <font color="deepskyblue">1391</font>
- 2022年: ★1.5／diff <font color="brown">588</font>

### レベル別問題一覧

「小数型」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)
- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)
- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)
- <a href="https://yukicoder.me/problems/no/2790">No.2790 Athena 3</a> (yukicoder contest 434 (2024-06-21) - B問題、diff <font color="green">934</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2352">No.2352 Sharpened Knife in Fall</a> (yukicoder contest 393 (2023-06-16) - C問題、diff <font color="deepskyblue">1560</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2389">No.2389 Cheating Code Golf</a> (yukicoder contest 398 (2023-07-21) - E問題、diff <font color="orange">2451</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="場合分け">70. 場合分け</h2>

### 難易度統計

「場合分け」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1473</font>
- 2024年: ★2／diff <font color="deepskyblue">1361</font>
- 2023年: ★2／diff <font color="deepskyblue">1301</font>
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
- <a href="https://yukicoder.me/problems/no/2736">No.2736 About half</a> (CPCTF 2024 : PPC (2024-04-20) - A問題、diff <font color="gray">216</font>)
- <a href="https://yukicoder.me/problems/no/2850">No.2850 Make Slimes</a> (yukicoder contest 442 (2024-08-25) - A問題、diff <font color="brown">624</font>)
- <a href="https://yukicoder.me/problems/no/2960">No.2960 Judgement</a> (yukicoder contest 453 (2024-11-16) - A問題、diff <font color="green">812</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題、diff <font color="green">969</font>)
- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)
- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題、diff <font color="brown">769</font>)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)
- <a href="https://yukicoder.me/problems/no/2564">No.2564 衝突予測</a> (第2回緑以下コンテスト (2023-12-02) - H問題、diff <font color="green">905</font>)
- <a href="https://yukicoder.me/problems/no/2681">No.2681 ゲームセンターの両替</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - C問題、diff <font color="green">1133</font>)
- <a href="https://yukicoder.me/problems/no/2776">No.2776 Bigger image</a> (yukicoder contest 432 (2024-06-07) - D問題、diff <font color="brown">683</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題、diff <font color="blue">1728</font>)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2209">No.2209 Flip and Reverse</a> (yukicoder contest 376 (2023-02-10) - B問題、diff <font color="green">1008</font>)
- <a href="https://yukicoder.me/problems/no/2247">No.2247 01 ZigZag</a> (yukicoder contest 381 (2023-03-17) - B問題、diff <font color="blue">1604</font>)
- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)
- <a href="https://yukicoder.me/problems/no/2541">No.2541 Divide 01 String</a> (yukicoder contest 413 (2023-11-24) - A問題、diff <font color="brown">606</font>)
- <a href="https://yukicoder.me/problems/no/2565">No.2565 はじめてのおつかい</a> (第2回緑以下コンテスト (2023-12-02) - I問題、diff <font color="green">972</font>)
- <a href="https://yukicoder.me/problems/no/2622">No.2622 Dam</a> (yukicoder contest 417 (2024-02-09) - B問題、diff <font color="green">1029</font>)
- <a href="https://yukicoder.me/problems/no/2655">No.2655 Increasing Strides</a> (yukicoder contest 419 (2024-03-01) - A問題、diff <font color="deepskyblue">1210</font>)
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)
- <a href="https://yukicoder.me/problems/no/2819">No.2819 Binary Binary-Operator</a> (yukicoder contest 438 (2024-07-26) - A問題、diff <font color="deepskyblue">1596</font>)
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
- <a href="https://yukicoder.me/problems/no/2585">No.2585 How many "Who is Santa?"</a> (Advent Calendar Contest 2023 (2023-12-01) - M問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)
- <a href="https://yukicoder.me/problems/no/2672">No.2672 Subset Xor Sum</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - B問題、diff <font color="deepskyblue">1416</font>)
- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)
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
- <a href="https://yukicoder.me/problems/no/2631">No.2631 Rectangle Grid Game</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - D問題、diff <font color="yellowgreen">2176</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2151">No.2151 3 on Torus-Lohkous</a> (Advent Calendar Contest 2022 (2022-12-01) - H問題、diff <font color="darkgoldenrod ">3257</font>)

　
<h2 id="貪欲法">71. 貪欲法</h2>

### 難易度統計

「貪欲法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1480</font>
- 2024年: ★2.1／diff <font color="deepskyblue">1595</font>
- 2023年: ★2.1／diff <font color="deepskyblue">1325</font>
- 2022年: ★2／diff <font color="deepskyblue">1483</font>

### レベル別問題一覧

「貪欲法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2424">No.2424 Josouzai</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - A問題、diff <font color="brown">769</font>)
- <a href="https://yukicoder.me/problems/no/2757">No.2757 Pin Game</a> (yukicoder contest 430 (2024-05-17) - A問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2775">No.2775 Nuisance Balls</a> (yukicoder contest 432 (2024-06-07) - C問題、diff <font color="brown">528</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)
- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題、diff <font color="gray">342</font>)
- <a href="https://yukicoder.me/problems/no/2479">No.2479 Sum of Squares</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - A問題、diff <font color="brown">779</font>)
- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)
- <a href="https://yukicoder.me/problems/no/2681">No.2681 ゲームセンターの両替</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - C問題、diff <font color="green">1133</font>)
- <a href="https://yukicoder.me/problems/no/2693">No.2693 Sword</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - C問題、diff <font color="deepskyblue">1211</font>)
- <a href="https://yukicoder.me/problems/no/2729">No.2729 Addition and Multiplication in yukicoder (Easy)</a> (yukicoder contest 428 (2024-04-19) - B問題、diff <font color="green">919</font>)
- <a href="https://yukicoder.me/problems/no/2738">No.2738 CPC To F</a> (CPCTF 2024 : PPC (2024-04-20) - C問題、diff <font color="deepskyblue">1245</font>)
- <a href="https://yukicoder.me/problems/no/2852">No.2852 Yakitori Optimization Problem</a> (yukicoder contest 442 (2024-08-25) - C問題、diff <font color="brown">774</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2056">No.2056 非力なレッド</a> (yukicoder contest 358 (2022-08-26) - A問題、diff <font color="brown">683</font>)
- <a href="https://yukicoder.me/problems/no/2064">No.2064 Smallest Sequence on Grid</a> (yukicoder contest 359 (2022-09-02) - B問題、diff <font color="deepskyblue">1582</font>)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題、diff <font color="green">849</font>)
- <a href="https://yukicoder.me/problems/no/2307">No.2307 [Cherry 5 th Tune *] Cool 46</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - C問題、diff <font color="deepskyblue">1345</font>)
- <a href="https://yukicoder.me/problems/no/2730">No.2730 Two Types Luggage</a> (yukicoder contest 428 (2024-04-19) - C問題、diff <font color="deepskyblue">1279</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題、diff <font color="blue">1802</font>)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2422">No.2422 regisys?</a> (MMA Contest 016 (2023-08-12) - I問題、diff <font color="yellowgreen">2353</font>)
- <a href="https://yukicoder.me/problems/no/2449">No.2449 square_permutation</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2501">No.2501 Maximum Inversion Number</a> (yukicoder contest 408 (2023-10-13) - B問題、diff <font color="yellowgreen">2064</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2623">No.2623 Room Allocation</a> (yukicoder contest 417 (2024-02-09) - C問題、diff <font color="deepskyblue">1328</font>)
- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)
- <a href="https://yukicoder.me/problems/no/2845">No.2845 Birthday Pattern in Two Different Calendars</a> (yukicoder contest 441 (2024-08-23) - D問題、diff <font color="blue">1947</font>)
- <a href="https://yukicoder.me/problems/no/2856">No.2856 Junk Market Game</a> (yukicoder contest 442 (2024-08-25) - G問題、diff <font color="blue">1824</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2734">No.2734 Addition and Multiplication in yukicoder (Hard)</a> (yukicoder contest 428 (2024-04-19) - G問題、diff <font color="yellowgreen">2034</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="等差数列の累積和計算">72. 等差数列の累積和計算</h2>

### 難易度統計

「等差数列の累積和計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1533</font>
- 2024年: ★2.1／diff <font color="blue">1697</font>
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
- <a href="https://yukicoder.me/problems/no/2649">No.2649 [Cherry 6th Tune C] Anthem Flower</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - C問題、diff <font color="deepskyblue">1322</font>)
- <a href="https://yukicoder.me/problems/no/2655">No.2655 Increasing Strides</a> (yukicoder contest 419 (2024-03-01) - A問題、diff <font color="deepskyblue">1210</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題、diff <font color="blue">1865</font>)
- <a href="https://yukicoder.me/problems/no/2834">No.2834 Work to Play</a> (yukicoder contest 439 (2024-08-02) - H問題、diff <font color="red">3011</font>)

　
<h2 id="分割の均等化">73. 分割の均等化</h2>

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

　
<h2 id="オーバーフロー回避">74. オーバーフロー回避</h2>

### 難易度統計

「オーバーフロー回避」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1557</font>
- 2024年: ★2.2／diff <font color="blue">1722</font>
- 2023年: ★2／diff <font color="deepskyblue">1228</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「オーバーフロー回避」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2750">No.2750 Number of Prime Factors</a> (yukicoder contest 429 (2024-05-10) - B問題、diff <font color="green">1026</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2420">No.2420 Simple Problem</a> (MMA Contest 016 (2023-08-12) - G問題、diff <font color="deepskyblue">1228</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

　
<h2 id="平方根計算">75. 平方根計算</h2>

### 難易度統計

「平方根計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1576</font>
- 2024年: ★2.5／diff <font color="blue">1659</font>
- 2023年: ★2／diff <font color="deepskyblue">1525</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「平方根計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2479">No.2479 Sum of Squares</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - A問題、diff <font color="brown">779</font>)
- <a href="https://yukicoder.me/problems/no/2493">No.2493 K-th in L2 with L1</a> (yukicoder contest 407 (2023-10-06) - B問題、diff <font color="green">1182</font>)
- <a href="https://yukicoder.me/problems/no/2721">No.2721 "Don't say N" Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - A問題、diff <font color="brown">426</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題、diff <font color="blue">1768</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)

　
<h2 id="動的mod">76. 動的mod</h2>

### 難易度統計

「動的mod」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1579</font>
- 2024年: ★2.3／diff <font color="blue">1812</font>
- 2023年: ★1.8／diff <font color="deepskyblue">1347</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「動的mod」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2558">No.2558 中国剰余定理</a> (第2回緑以下コンテスト (2023-12-02) - B問題、diff <font color="gray">306</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2562">No.2562 数字探しゲーム（緑以下コンver.）</a> (第2回緑以下コンテスト (2023-12-02) - F問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2709">No.2709 1975 Powers</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - D問題、diff <font color="green">1143</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2649">No.2649 [Cherry 6th Tune C] Anthem Flower</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - C問題、diff <font color="deepskyblue">1322</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2646">No.2646 Cycle Maze</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2653">No.2653 [Cherry 6th Tune] Re: start! (Make it Zero!)</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - G問題、diff <font color="yellowgreen">2247</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="決め打ちによる構築">77. 決め打ちによる構築</h2>

### 難易度統計

「決め打ちによる構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="deepskyblue">1587</font>
- 2024年: ★2.5／diff <font color="blue">1703</font>
- 2023年: ★1.5／diff <font color="deepskyblue">1356</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「決め打ちによる構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2562">No.2562 数字探しゲーム（緑以下コンver.）</a> (第2回緑以下コンテスト (2023-12-02) - F問題、diff <font color="deepskyblue">1356</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2663">No.2663 Zero-Sum Submatrices</a> (yukicoder contest 420 (2024-03-08) - A問題、diff <font color="deepskyblue">1204</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2732">No.2732 Similar Permutations</a> (yukicoder contest 428 (2024-04-19) - E問題、diff <font color="yellowgreen">2203</font>)

　
<h2 id="木の頂点の次数計算">78. 木の頂点の次数計算</h2>

### 難易度統計

「木の頂点の次数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.1／diff <font color="blue">1717</font>
- 2024年: ★2.2／diff <font color="blue">1939</font>
- 2023年: ★2／diff <font color="deepskyblue">1273</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「木の頂点の次数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2638">No.2638 Initial fare</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - B問題、diff <font color="blue">1624</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2427">No.2427 Tree Distance Two</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - D問題、diff <font color="deepskyblue">1273</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2618">No.2618 除霊</a> (yukicoder contest 416 (2024-01-26) - E問題、diff <font color="yellowgreen">2255</font>)

　
<h2 id="隣接不等式管理">79. 隣接不等式管理</h2>

### 難易度統計

「隣接不等式管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1200</font>
- 2024年: ★2／diff <font color="green">912</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1488</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「隣接不等式管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2648">No.2648 [Cherry 6th Tune D] 一次元の馬</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - B問題、diff <font color="green">912</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2518">No.2518 Adjacent Larger</a> (yukicoder contest 410 (2023-10-27) - D問題、diff <font color="deepskyblue">1488</font>)

　
<h2 id="複素数演算">80. 複素数演算</h2>

### 難易度統計

「複素数演算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1322</font>
- 2024年: ★3／diff <font color="yellowgreen">2301</font>
- 2023年: ★1.5／diff <font color="gray">344</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「複素数演算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2400">No.2400 Product of Gaussian Integer</a> (yukicoder contest 400 (2023-08-04) - B問題、diff <font color="gray">344</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)

　
<h2 id="操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着">81. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着">操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着</a></h2>

### 難易度統計

「[操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1355</font>
- 2024年: ★2／diff <font color="deepskyblue">1510</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1200</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2855">No.2855 Move on Grid</a> (yukicoder contest 442 (2024-08-25) - F問題、diff <font color="deepskyblue">1510</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)

　
<h2 id="最長歩道計算">82. 最長歩道計算</h2>

### 難易度統計

「最長歩道計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1395</font>
- 2024年: ★2／diff <font color="deepskyblue">1591</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1200</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最長歩道計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2639">No.2639 Longest Increasing Walk</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - C問題、diff <font color="deepskyblue">1591</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)

　
<h2 id="三角形の成立条件">83. 三角形の成立条件</h2>

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

　
<h2 id="DAG上のDP">84. DAG上のDP</h2>

### 難易度統計

「DAG上のDP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1419</font>
- 2024年: ★2.1／diff <font color="deepskyblue">1577</font>
- 2023年: ★2.5／diff <font color="green">1157</font>
- 2022年: ★2／diff <font color="deepskyblue">1577</font>

### レベル別問題一覧

「DAG上のDP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2100">No.2100 [Cherry Alpha C] Two-way Steps</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - D問題、diff <font color="deepskyblue">1577</font>)
- <a href="https://yukicoder.me/problems/no/2402">No.2402 Dirty Stairs and Shoes</a> (yukicoder contest 400 (2023-08-04) - D問題、diff <font color="green">822</font>)
- <a href="https://yukicoder.me/problems/no/2639">No.2639 Longest Increasing Walk</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - C問題、diff <font color="deepskyblue">1591</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2430">No.2430 Damage Zone</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - G問題、diff <font color="deepskyblue">1449</font>)
- <a href="https://yukicoder.me/problems/no/2733">No.2733 Just K-times TSP</a> (yukicoder contest 428 (2024-04-19) - F問題、diff <font color="blue">1977</font>)
- <a href="https://yukicoder.me/problems/no/2807">No.2807 Have Another Go (Easy)</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - E問題、diff <font color="yellowgreen">2004</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)

　
<h2 id="ナップサックDP">85. ナップサックDP</h2>

### 難易度統計

「ナップサックDP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1420</font>
- 2024年: ★2.2／diff <font color="blue">1728</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1410</font>
- 2022年: ★2／diff <font color="green">843</font>

### レベル別問題一覧

「ナップサックDP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題、diff <font color="green">843</font>)
- <a href="https://yukicoder.me/problems/no/2232">No.2232 Miser's Gift</a> (yukicoder contest 379 (2023-03-03) - A問題、diff <font color="deepskyblue">1389</font>)
- <a href="https://yukicoder.me/problems/no/2741">No.2741 Balanced Choice</a> (CPCTF 2024 : PPC (2024-04-20) - F問題、diff <font color="deepskyblue">1557</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題、diff <font color="green">875</font>)
- <a href="https://yukicoder.me/problems/no/2429">No.2429 Happiest Tabehodai Ways</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - F問題、diff <font color="blue">1907</font>)
- <a href="https://yukicoder.me/problems/no/2542">No.2542 Yokan for Two</a> (yukicoder contest 413 (2023-11-24) - B問題、diff <font color="deepskyblue">1469</font>)
- <a href="https://yukicoder.me/problems/no/2701">No.2701 A cans -> B cans</a> (yukicoder contest 424 (2024-03-29) - C問題、diff <font color="blue">1900</font>)

　
<h2 id="コストなしナップサック最適化">86. コストなしナップサック最適化</h2>

### 難易度統計

「コストなしナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1439</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1439</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「コストなしナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2729">No.2729 Addition and Multiplication in yukicoder (Easy)</a> (yukicoder contest 428 (2024-04-19) - B問題、diff <font color="green">919</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2713">No.2713 Just Solitaire</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - H問題、diff <font color="blue">1959</font>)

　
<h2 id="約数列挙">87. 約数列挙</h2>

### 難易度統計

「約数列挙」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1479</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1427</font>
- 2023年: ★2.1／diff <font color="deepskyblue">1388</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2291</font>

### レベル別問題一覧

「約数列挙」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2417">No.2417 Div Count</a> (MMA Contest 016 (2023-08-12) - D問題、diff <font color="brown">781</font>)
- <a href="https://yukicoder.me/problems/no/2721">No.2721 "Don't say N" Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - A問題、diff <font color="brown">426</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2480">No.2480 Sequence Sum</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - B問題、diff <font color="deepskyblue">1433</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)

　
<h2 id="ナップサック最適化">88. ナップサック最適化</h2>

### 難易度統計

「ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1484</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1568</font>
- 2023年: ★2.2／diff <font color="deepskyblue">1515</font>
- 2022年: ★1.7／diff <font color="green">969</font>

### レベル別問題一覧

「ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題、diff <font color="gray">331</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)
- <a href="https://yukicoder.me/problems/no/2729">No.2729 Addition and Multiplication in yukicoder (Easy)</a> (yukicoder contest 428 (2024-04-19) - B問題、diff <font color="green">919</font>)
- <a href="https://yukicoder.me/problems/no/2852">No.2852 Yakitori Optimization Problem</a> (yukicoder contest 442 (2024-08-25) - C問題、diff <font color="brown">774</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題、diff <font color="green">843</font>)
- <a href="https://yukicoder.me/problems/no/2232">No.2232 Miser's Gift</a> (yukicoder contest 379 (2023-03-03) - A問題、diff <font color="deepskyblue">1389</font>)
- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)
- <a href="https://yukicoder.me/problems/no/2694">No.2694 The Early Bird Catches The Worm</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - D問題、diff <font color="deepskyblue">1276</font>)
- <a href="https://yukicoder.me/problems/no/2730">No.2730 Two Types Luggage</a> (yukicoder contest 428 (2024-04-19) - C問題、diff <font color="deepskyblue">1279</font>)
- <a href="https://yukicoder.me/problems/no/2741">No.2741 Balanced Choice</a> (CPCTF 2024 : PPC (2024-04-20) - F問題、diff <font color="deepskyblue">1557</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題、diff <font color="green">875</font>)
- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題、diff <font color="blue">1774</font>)
- <a href="https://yukicoder.me/problems/no/2422">No.2422 regisys?</a> (MMA Contest 016 (2023-08-12) - I問題、diff <font color="yellowgreen">2353</font>)
- <a href="https://yukicoder.me/problems/no/2429">No.2429 Happiest Tabehodai Ways</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - F問題、diff <font color="blue">1907</font>)
- <a href="https://yukicoder.me/problems/no/2542">No.2542 Yokan for Two</a> (yukicoder contest 413 (2023-11-24) - B問題、diff <font color="deepskyblue">1469</font>)
- <a href="https://yukicoder.me/problems/no/2701">No.2701 A cans -> B cans</a> (yukicoder contest 424 (2024-03-29) - C問題、diff <font color="blue">1900</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2686">No.2686 商品券の使い道</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - H問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2713">No.2713 Just Solitaire</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - H問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)

　
<h2 id="外積による三角形の面積計算">89. 外積による三角形の面積計算</h2>

### 難易度統計

「外積による三角形の面積計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1540</font>
- 2024年: ★1.5／diff <font color="green">934</font>
- 2023年: ★3／diff <font color="yellowgreen">2147</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「外積による三角形の面積計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2790">No.2790 Athena 3</a> (yukicoder contest 434 (2024-06-21) - B問題、diff <font color="green">934</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)

　
<h2 id="ヘルド・カープ法">90. ヘルド・カープ法</h2>

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

　
<h2 id="操作を数値に翻訳">91. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作を数値に翻訳">操作を数値に翻訳</a></h2>

### 難易度統計

「[操作を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#操作を数値に翻訳)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1544</font>
- 2024年: ★2.7／diff <font color="blue">1963</font>
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
- <a href="https://yukicoder.me/problems/no/2630">No.2630 Colorful Vertices and Cheapest Paths </a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - C問題、diff <font color="deepskyblue">1435</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題、diff <font color="yellowgreen">2175</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)

　
<h2 id="幅優先探索">92. 幅優先探索</h2>

### 難易度統計

「幅優先探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1559</font>
- 2024年: ★2.4／diff <font color="blue">1798</font>
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
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)
- <a href="https://yukicoder.me/problems/no/2759">No.2759 Take Pictures, Elements?</a> (yukicoder contest 430 (2024-05-17) - C問題、diff <font color="deepskyblue">1565</font>)
- <a href="https://yukicoder.me/problems/no/2855">No.2855 Move on Grid</a> (yukicoder contest 442 (2024-08-25) - F問題、diff <font color="deepskyblue">1510</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題、diff <font color="blue">1989</font>)
- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2403">No.2403 "Eight" Bridges of Konigsberg</a> (yukicoder contest 400 (2023-08-04) - E問題、diff <font color="yellowgreen">2123</font>)
- <a href="https://yukicoder.me/problems/no/2630">No.2630 Colorful Vertices and Cheapest Paths </a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - C問題、diff <font color="deepskyblue">1435</font>)
- <a href="https://yukicoder.me/problems/no/2646">No.2646 Cycle Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2674">No.2674 k-Walk on Bipartite</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - D問題、diff <font color="blue">1920</font>)
- <a href="https://yukicoder.me/problems/no/2696">No.2696 Sign Creation</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - F問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2643">No.2643 Many Range Sums Problems</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - G問題、diff <font color="orange">2765</font>)
- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)

　
<h2 id="素因数分解による約数列挙">93. 素因数分解による約数列挙</h2>

### 難易度統計

「素因数分解による約数列挙」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="deepskyblue">1581</font>
- 2024年: ★2.3／diff <font color="blue">1733</font>
- 2023年: ★2.1／diff <font color="deepskyblue">1388</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2291</font>

### レベル別問題一覧

「素因数分解による約数列挙」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2417">No.2417 Div Count</a> (MMA Contest 016 (2023-08-12) - D問題、diff <font color="brown">781</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2480">No.2480 Sequence Sum</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - B問題、diff <font color="deepskyblue">1433</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)

　
<h2 id="重複選択個数の線形関係式">94. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#重複選択個数の線形関係式">重複選択個数の線形関係式</a></h2>

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

　
<h2 id="最小公倍数計算">95. 最小公倍数計算</h2>

### 難易度統計

「最小公倍数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1607</font>
- 2024年: ★2／diff <font color="deepskyblue">1447</font>
- 2023年: ★2.3／diff <font color="blue">1660</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最小公倍数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)
- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

　
<h2 id="素数列による試し割り法">96. 素数列による試し割り法</h2>

### 難易度統計

「素数列による試し割り法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1619</font>
- 2024年: ★2／diff <font color="deepskyblue">1351</font>
- 2023年: ★2.5／diff <font color="blue">1887</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素数列による試し割り法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2751">No.2751 429-like Number</a> (yukicoder contest 429 (2024-05-10) - C問題、diff <font color="deepskyblue">1351</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)

　
<h2 id="小数計算を整数に帰着">97. 小数計算を整数に帰着</h2>

### 難易度統計

「小数計算を整数に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1632</font>
- 2024年: ★2.4／diff <font color="blue">1812</font>
- 2023年: ★2／diff <font color="deepskyblue">1393</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「小数計算を整数に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2407">No.2407 Bouns 2.0</a> (yukicoder contest 401 (2023-08-11) - A問題、diff <font color="gray">132</font>)
- <a href="https://yukicoder.me/problems/no/2647">No.2647 [Cherry 6th Tune A] Wind</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - A問題、diff <font color="brown">783</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2493">No.2493 K-th in L2 with L1</a> (yukicoder contest 407 (2023-10-06) - B問題、diff <font color="green">1182</font>)
- <a href="https://yukicoder.me/problems/no/2776">No.2776 Bigger image</a> (yukicoder contest 432 (2024-06-07) - D問題、diff <font color="brown">683</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)
- <a href="https://yukicoder.me/problems/no/2420">No.2420 Simple Problem</a> (MMA Contest 016 (2023-08-12) - G問題、diff <font color="deepskyblue">1228</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2624">No.2624 Prediction by Average</a> (yukicoder contest 417 (2024-02-09) - D問題、diff <font color="blue">1735</font>)
- <a href="https://yukicoder.me/problems/no/2684">No.2684 折々の色</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - F問題、diff <font color="blue">1790</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)
- <a href="https://yukicoder.me/problems/no/2769">No.2769 Number of Rhombi</a> (yukicoder contest 431 (2024-05-31) - E問題、diff <font color="yellowgreen">2003</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="連長圧縮">98. 連長圧縮</h2>

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

　
<h2 id="括弧列判定">99. 括弧列判定</h2>

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

　
<h2 id="良いケースに帰着">100. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着">良いケースに帰着</a></h2>

### 難易度統計

「[良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1770</font>
- 2024年: ★2.2／diff <font color="blue">1778</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.2／diff <font color="blue">1762</font>

### レベル別問題一覧

「[良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題、diff <font color="green">1095</font>)
- <a href="https://yukicoder.me/problems/no/2681">No.2681 ゲームセンターの両替</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - C問題、diff <font color="green">1133</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)

　
<h2 id="選択肢の分割・纏め上げで良いケースに帰着">101. 選択肢の分割・纏め上げで良いケースに帰着</h2>

### 難易度統計

「選択肢の分割・纏め上げで良いケースに帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.2／diff <font color="blue">1778</font>
- 2024年: ★2.2／diff <font color="blue">1778</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「選択肢の分割・纏め上げで良いケースに帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2681">No.2681 ゲームセンターの両替</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - C問題、diff <font color="green">1133</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)

　
<h2 id="ウノ計算">102. ウノ計算</h2>

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

　
<h2 id="不定方程式の因数分解">103. 不定方程式の因数分解</h2>

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

　
<h2 id="門松列DP">104. 門松列DP</h2>

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

　
<h2 id="連結成分取得">105. 連結成分取得</h2>

### 難易度統計

「連結成分取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="deepskyblue">1462</font>
- 2024年: ★2.5／diff <font color="blue">1716</font>
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
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題、diff <font color="deepskyblue">1486</font>)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題、diff <font color="deepskyblue">1302</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2403">No.2403 "Eight" Bridges of Konigsberg</a> (yukicoder contest 400 (2023-08-04) - E問題、diff <font color="yellowgreen">2123</font>)
- <a href="https://yukicoder.me/problems/no/2630">No.2630 Colorful Vertices and Cheapest Paths </a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - C問題、diff <font color="deepskyblue">1435</font>)
- <a href="https://yukicoder.me/problems/no/2696">No.2696 Sign Creation</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - F問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)
- <a href="https://yukicoder.me/problems/no/2786">No.2786 RMQ on Grid Path</a> (yukicoder contest 433 (2024-06-14) - F問題、diff <font color="yellowgreen">2162</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2756">No.2756 GCD Teleporter</a> (yukicoder contest 429 (2024-05-10) - H問題、diff <font color="blue">1751</font>)

　
<h2 id="bit全探索">106. bit全探索</h2>

### 難易度統計

「bit全探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="deepskyblue">1519</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1382</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2344</font>

### レベル別問題一覧

「bit全探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2711">No.2711 Connecting Lights</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - F問題、diff <font color="deepskyblue">1396</font>)
- <a href="https://yukicoder.me/problems/no/2730">No.2730 Two Types Luggage</a> (yukicoder contest 428 (2024-04-19) - C問題、diff <font color="deepskyblue">1279</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2630">No.2630 Colorful Vertices and Cheapest Paths </a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - C問題、diff <font color="deepskyblue">1435</font>)
- <a href="https://yukicoder.me/problems/no/2672">No.2672 Subset Xor Sum</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - B問題、diff <font color="deepskyblue">1416</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)
- <a href="https://yukicoder.me/problems/no/2686">No.2686 商品券の使い道</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - H問題、diff <font color="yellowgreen">2031</font>)

　
<h2 id="素集合データ構造">107. 素集合データ構造</h2>

### 難易度統計

「素集合データ構造」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="deepskyblue">1530</font>
- 2024年: ★2.5／diff <font color="blue">1866</font>
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
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題、diff <font color="deepskyblue">1486</font>)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題、diff <font color="deepskyblue">1302</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2403">No.2403 "Eight" Bridges of Konigsberg</a> (yukicoder contest 400 (2023-08-04) - E問題、diff <font color="yellowgreen">2123</font>)
- <a href="https://yukicoder.me/problems/no/2630">No.2630 Colorful Vertices and Cheapest Paths </a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - C問題、diff <font color="deepskyblue">1435</font>)
- <a href="https://yukicoder.me/problems/no/2696">No.2696 Sign Creation</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - F問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)
- <a href="https://yukicoder.me/problems/no/2786">No.2786 RMQ on Grid Path</a> (yukicoder contest 433 (2024-06-14) - F問題、diff <font color="yellowgreen">2162</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2643">No.2643 Many Range Sums Problems</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - G問題、diff <font color="orange">2765</font>)
- <a href="https://yukicoder.me/problems/no/2756">No.2756 GCD Teleporter</a> (yukicoder contest 429 (2024-05-10) - H問題、diff <font color="blue">1751</font>)

　
<h2 id="余事象に注目">108. 余事象に注目</h2>

### 難易度統計

「余事象に注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="deepskyblue">1541</font>
- 2024年: ★2.3／diff <font color="blue">1696</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1489</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「余事象に注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題、diff <font color="brown">769</font>)
- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)
- <a href="https://yukicoder.me/problems/no/2768">No.2768 Password Crack</a> (yukicoder contest 431 (2024-05-31) - D問題、diff <font color="deepskyblue">1548</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2486">No.2486 Don't come next to me</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - A問題、diff <font color="brown">712</font>)
- <a href="https://yukicoder.me/problems/no/2585">No.2585 How many "Who is Santa?"</a> (Advent Calendar Contest 2023 (2023-12-01) - M問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)

　
<h2 id="最大公約数による最小公倍数計算">109. 最大公約数による最小公倍数計算</h2>

### 難易度統計

「最大公約数による最小公倍数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1614</font>
- 2024年: ★2／diff <font color="deepskyblue">1447</font>
- 2023年: ★2.5／diff <font color="blue">1698</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最大公約数による最小公倍数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)
- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)

　
<h2 id="頂点倍化">110. 頂点倍化</h2>

### 難易度統計

「頂点倍化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1618</font>
- 2024年: ★2／diff <font color="deepskyblue">1301</font>
- 2023年: ★2.5／diff <font color="blue">1724</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「頂点倍化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="二部グラフ判定">111. 二部グラフ判定</h2>

### 難易度統計

「二部グラフ判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1618</font>
- 2024年: ★2／diff <font color="deepskyblue">1301</font>
- 2023年: ★2.5／diff <font color="blue">1724</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「二部グラフ判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="ソート">112. ソート</h2>

### 難易度統計

「ソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1672</font>
- 2024年: ★2.1／diff <font color="deepskyblue">1517</font>
- 2023年: ★2.2／diff <font color="blue">1704</font>
- 2022年: ★3.3／diff <font color="orange">2503</font>

### レベル別問題一覧

「ソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2424">No.2424 Josouzai</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - A問題、diff <font color="brown">769</font>)
- <a href="https://yukicoder.me/problems/no/2714">No.2714 Amaou</a> (yukicoder contest 426 (2024-04-05) - A問題、diff <font color="brown">595</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題、diff <font color="gray">342</font>)
- <a href="https://yukicoder.me/problems/no/2493">No.2493 K-th in L2 with L1</a> (yukicoder contest 407 (2023-10-06) - B問題、diff <font color="green">1182</font>)
- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)
- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)
- <a href="https://yukicoder.me/problems/no/2671">No.2671 NUPC Decompressor</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - A問題、diff <font color="green">1012</font>)
- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)
- <a href="https://yukicoder.me/problems/no/2729">No.2729 Addition and Multiplication in yukicoder (Easy)</a> (yukicoder contest 428 (2024-04-19) - B問題、diff <font color="green">919</font>)
- <a href="https://yukicoder.me/problems/no/2803">No.2803 Bocching Star</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - A問題、diff <font color="green">939</font>)
- <a href="https://yukicoder.me/problems/no/2852">No.2852 Yakitori Optimization Problem</a> (yukicoder contest 442 (2024-08-25) - C問題、diff <font color="brown">774</font>)
- <a href="https://yukicoder.me/problems/no/2961">No.2961 Shiny Monster Master</a> (yukicoder contest 453 (2024-11-16) - B問題、diff <font color="green">940</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題、diff <font color="green">1174</font>)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2615">No.2615 ペアの作り方</a> (yukicoder contest 416 (2024-01-26) - B問題、diff <font color="green">958</font>)
- <a href="https://yukicoder.me/problems/no/2639">No.2639 Longest Increasing Walk</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - C問題、diff <font color="deepskyblue">1591</font>)
- <a href="https://yukicoder.me/problems/no/2715">No.2715 Unique Chimatagram</a> (yukicoder contest 426 (2024-04-05) - B問題、diff <font color="deepskyblue">1482</font>)
- <a href="https://yukicoder.me/problems/no/2730">No.2730 Two Types Luggage</a> (yukicoder contest 428 (2024-04-19) - C問題、diff <font color="deepskyblue">1279</font>)
- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)
- <a href="https://yukicoder.me/problems/no/2774">No.2774 Wake up Record 2</a> (yukicoder contest 432 (2024-06-07) - B問題、diff <font color="brown">612</font>)
- <a href="https://yukicoder.me/problems/no/2804">No.2804 Fixer And Ratism</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - B問題、diff <font color="blue">1779</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2353">No.2353 Guardian Dogs in Spring</a> (yukicoder contest 393 (2023-06-16) - D問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)
- <a href="https://yukicoder.me/problems/no/2501">No.2501 Maximum Inversion Number</a> (yukicoder contest 408 (2023-10-13) - B問題、diff <font color="yellowgreen">2064</font>)
- <a href="https://yukicoder.me/problems/no/2510">No.2510 Six Cube Sum Counting</a> (yukicoder contest 409 (2023-10-20) - C問題、diff <font color="yellowgreen">2219</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2623">No.2623 Room Allocation</a> (yukicoder contest 417 (2024-02-09) - C問題、diff <font color="deepskyblue">1328</font>)
- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)
- <a href="https://yukicoder.me/problems/no/2662">No.2662 Installing Cell Towers</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)
- <a href="https://yukicoder.me/problems/no/2745">No.2745 String Swap Battle</a> (CPCTF 2024 : PPC (2024-04-20) - J問題、diff <font color="yellowgreen">2309</font>)
- <a href="https://yukicoder.me/problems/no/2780">No.2780 The Bottle Imp</a> (yukicoder contest 432 (2024-06-07) - H問題、diff <font color="deepskyblue">1542</font>)
- <a href="https://yukicoder.me/problems/no/2856">No.2856 Junk Market Game</a> (yukicoder contest 442 (2024-08-25) - G問題、diff <font color="blue">1824</font>)

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
- <a href="https://yukicoder.me/problems/no/2652">No.2652 [Cherry 6th Tune N] Δρονε χιρχλινγ</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - F問題、diff <font color="yellowgreen">2004</font>)
- <a href="https://yukicoder.me/problems/no/2734">No.2734 Addition and Multiplication in yukicoder (Hard)</a> (yukicoder contest 428 (2024-04-19) - G問題、diff <font color="yellowgreen">2034</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="累積積による冪乗・階乗計算">113. 累積積による冪乗・階乗計算</h2>

### 難易度統計

「累積積による冪乗・階乗計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1678</font>
- 2024年: ★2.3／diff <font color="blue">1670</font>
- 2023年: ★2.4／diff <font color="blue">1648</font>
- 2022年: ★2.3／diff <font color="blue">1786</font>

### レベル別問題一覧

「累積積による冪乗・階乗計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2709">No.2709 1975 Powers</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - D問題、diff <font color="green">1143</font>)
- <a href="https://yukicoder.me/problems/no/2750">No.2750 Number of Prime Factors</a> (yukicoder contest 429 (2024-05-10) - B問題、diff <font color="green">1026</font>)
- <a href="https://yukicoder.me/problems/no/2853">No.2853 A + B Problem</a> (yukicoder contest 442 (2024-08-25) - D問題、diff <font color="brown">774</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題、diff <font color="deepskyblue">1258</font>)
- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)
- <a href="https://yukicoder.me/problems/no/2494">No.2494 Sum within Components</a> (yukicoder contest 407 (2023-10-06) - C問題、diff <font color="green">1031</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2615">No.2615 ペアの作り方</a> (yukicoder contest 416 (2024-01-26) - B問題、diff <font color="green">958</font>)
- <a href="https://yukicoder.me/problems/no/2636">No.2636 No Waiting in Vain</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)
- <a href="https://yukicoder.me/problems/no/2828">No.2828 Remainder Game</a> (yukicoder contest 439 (2024-08-02) - B問題、diff <font color="blue">1696</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)
- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)
- <a href="https://yukicoder.me/problems/no/2685">No.2685 Cell Proliferation (Easy)</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - G問題、diff <font color="blue">1983</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)
- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)

　
<h2 id="等比数列の累積和計算">114. 等比数列の累積和計算</h2>

### 難易度統計

「等比数列の累積和計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1684</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2335</font>
- 2023年: ★2.1／diff <font color="deepskyblue">1358</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「等比数列の累積和計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)
- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2393">No.2393 Bit Grid Connected Component</a> (yukicoder contest 399 (2023-07-28) - B問題、diff <font color="green">1050</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2830">No.2830 Don't Stop the Game</a> (yukicoder contest 439 (2024-08-02) - D問題、diff <font color="orange">2525</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)

　
<h2 id="二・多項係数を組み合わせに翻訳">115. 二・多項係数を組み合わせに翻訳</h2>

### 難易度統計

「二・多項係数を組み合わせに翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1702</font>
- 2024年: ★3／diff <font color="yellowgreen">2143</font>
- 2023年: ★2／diffデータなし
- 2022年: ★2／diff <font color="deepskyblue">1261</font>

### レベル別問題一覧

「二・多項係数を組み合わせに翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題、diff <font color="deepskyblue">1261</font>)
- <a href="https://yukicoder.me/problems/no/2467">No.2467 Sum of Product of Binomial Coefficients</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - A問題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

　
<h2 id="変数決め打ち">116. 変数決め打ち</h2>

### 難易度統計

「変数決め打ち」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1779</font>
- 2024年: ★2.5／diff <font color="blue">1894</font>
- 2023年: ★2.2／diff <font color="blue">1620</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2069</font>

### レベル別問題一覧

「変数決め打ち」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)
- <a href="https://yukicoder.me/problems/no/2562">No.2562 数字探しゲーム（緑以下コンver.）</a> (第2回緑以下コンテスト (2023-12-02) - F問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2638">No.2638 Initial fare</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - B問題、diff <font color="blue">1624</font>)
- <a href="https://yukicoder.me/problems/no/2693">No.2693 Sword</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - C問題、diff <font color="deepskyblue">1211</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題、diff <font color="blue">1728</font>)
- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題、diff <font color="deepskyblue">1529</font>)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題、diff <font color="deepskyblue">1551</font>)
- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)
- <a href="https://yukicoder.me/problems/no/2374">No.2374 ASKT Subsequences</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - D問題、diff <font color="deepskyblue">1578</font>)
- <a href="https://yukicoder.me/problems/no/2386">No.2386 Udon Coupon (Easy)</a> (yukicoder contest 398 (2023-07-21) - B問題、diff <font color="green">982</font>)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)
- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)
- <a href="https://yukicoder.me/problems/no/2601">No.2601 Very Poor</a> (yukicoder contest 414 (2024-01-12) - C問題、diff <font color="green">1032</font>)
- <a href="https://yukicoder.me/problems/no/2730">No.2730 Two Types Luggage</a> (yukicoder contest 428 (2024-04-19) - C問題、diff <font color="deepskyblue">1279</font>)
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2463">No.2463 ストレートフラッシュ</a> (yukicoder contest 404 (2023-09-08) - D問題、diff <font color="blue">1838</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)
- <a href="https://yukicoder.me/problems/no/2630">No.2630 Colorful Vertices and Cheapest Paths </a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - C問題、diff <font color="deepskyblue">1435</font>)
- <a href="https://yukicoder.me/problems/no/2684">No.2684 折々の色</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - F問題、diff <font color="blue">1790</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題、diff <font color="orange">2620</font>)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題、diff <font color="yellowgreen">2168</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2732">No.2732 Similar Permutations</a> (yukicoder contest 428 (2024-04-19) - E問題、diff <font color="yellowgreen">2203</font>)
- <a href="https://yukicoder.me/problems/no/2858">No.2858 Make a Palindrome</a> (yukicoder contest 442 (2024-08-25) - I問題、diff <font color="yellowgreen">2147</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)

　
<h2 id="最終手番に注目">117. 最終手番に注目</h2>

### 難易度統計

「最終手番に注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1780</font>
- 2024年: ★2.3／diff <font color="blue">1631</font>
- 2023年: ★2.5／diff <font color="blue">1875</font>
- 2022年: ★2.3／diff <font color="blue">1951</font>

### レベル別問題一覧

「最終手番に注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2679">No.2679 MODice</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - A問題、diff <font color="brown">721</font>)
- <a href="https://yukicoder.me/problems/no/2721">No.2721 "Don't say N" Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - A問題、diff <font color="brown">426</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題、diff <font color="blue">1730</font>)
- <a href="https://yukicoder.me/problems/no/2209">No.2209 Flip and Reverse</a> (yukicoder contest 376 (2023-02-10) - B問題、diff <font color="green">1008</font>)
- <a href="https://yukicoder.me/problems/no/2812">No.2812 Plus Minus Blackboard</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - B問題、diff <font color="blue">1698</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題、diff <font color="blue">1934</font>)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題、diff <font color="blue">1838</font>)
- <a href="https://yukicoder.me/problems/no/2502">No.2502 Optimization in the Dark</a> (yukicoder contest 408 (2023-10-13) - C問題、diff <font color="orange">2503</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2814">No.2814 Block Game</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - D問題、diff <font color="orange">2676</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="約数計数関数による計算量評価">118. 約数計数関数による計算量評価</h2>

### 難易度統計

「約数計数関数による計算量評価」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1791</font>
- 2024年: ★2.3／diff <font color="blue">1791</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「約数計数関数による計算量評価」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)
- <a href="https://yukicoder.me/problems/no/2806">No.2806 Cornflake Man</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - D問題、diff <font color="blue">1689</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)

　
<h2 id="操作コスト最小化を最短経路長計算に帰着">119. 操作コスト最小化を最短経路長計算に帰着</h2>

### 難易度統計

「操作コスト最小化を最短経路長計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1885</font>
- 2024年: ★2.3／diff <font color="blue">1875</font>
- 2023年: ★2.5／diff <font color="blue">1915</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「操作コスト最小化を最短経路長計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2855">No.2855 Move on Grid</a> (yukicoder contest 442 (2024-08-25) - F問題、diff <font color="deepskyblue">1510</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2328">No.2328 Build Walls</a> (MMA Contest 015  (2023-05-28) - G問題、diff <font color="blue">1915</font>)
- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)
- <a href="https://yukicoder.me/problems/no/2744">No.2744 Power! or +1</a> (CPCTF 2024 : PPC (2024-04-20) - I問題、diff <font color="yellowgreen">2309</font>)

　
<h2 id="グラフの状態や目的地の変化を有向辺に翻訳">120. グラフの状態や目的地の変化を有向辺に翻訳</h2>

### 難易度統計

「グラフの状態や目的地の変化を有向辺に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.3／diff <font color="blue">1975</font>
- 2024年: ★2.3／diff <font color="blue">1975</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「グラフの状態や目的地の変化を有向辺に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2759">No.2759 Take Pictures, Elements?</a> (yukicoder contest 430 (2024-05-17) - C問題、diff <font color="deepskyblue">1565</font>)
- <a href="https://yukicoder.me/problems/no/2805">No.2805 Go to School</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - C問題、diff <font color="blue">1720</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2646">No.2646 Cycle Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)

　
<h2 id="深さ優先探索">121. 深さ優先探索</h2>

### 難易度統計

「深さ優先探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="deepskyblue">1562</font>
- 2024年: ★1.5／diff <font color="green">934</font>
- 2023年: ★2.7／diff <font color="blue">1741</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「深さ優先探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題、diff <font color="brown">769</font>)
- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)
- <a href="https://yukicoder.me/problems/no/2766">No.2766 Delicious Multiply Spice</a> (yukicoder contest 431 (2024-05-31) - B問題、diff <font color="green">1132</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題、diff <font color="blue">1661</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題、diff <font color="blue">1933</font>)
- <a href="https://yukicoder.me/problems/no/2301">No.2301 Namorientation</a> (yukicoder contest 388 (2023-05-12) - E問題、diff <font color="deepskyblue">1499</font>)
- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2531">No.2531 Coloring Vertices on Namori</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - G問題、diff <font color="blue">1951</font>)

　
<h2 id="ド・モルガンの法則">122. ド・モルガンの法則</h2>

### 難易度統計

「ド・モルガンの法則」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="deepskyblue">1576</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1509</font>
- 2023年: ★2.4／diff <font color="deepskyblue">1587</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ド・モルガンの法則」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2461">No.2461 一点張り</a> (yukicoder contest 404 (2023-09-08) - B問題、diff <font color="green">959</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)

　
<h2 id="素数列挙">123. 素数列挙</h2>

### 難易度統計

「素数列挙」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="deepskyblue">1583</font>
- 2024年: ★2.4／diff <font color="deepskyblue">1583</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素数列挙」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2750">No.2750 Number of Prime Factors</a> (yukicoder contest 429 (2024-05-10) - B問題、diff <font color="green">1026</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2751">No.2751 429-like Number</a> (yukicoder contest 429 (2024-05-10) - C問題、diff <font color="deepskyblue">1351</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2725">No.2725 Coprime Game 2</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - E問題、diff <font color="blue">1944</font>)
- <a href="https://yukicoder.me/problems/no/2756">No.2756 GCD Teleporter</a> (yukicoder contest 429 (2024-05-10) - H問題、diff <font color="blue">1751</font>)

　
<h2 id="操作・遷移の纏め上げ">124. 操作・遷移の纏め上げ</h2>

### 難易度統計

「操作・遷移の纏め上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1677</font>
- 2024年: ★2.8／diff <font color="blue">1921</font>
- 2023年: ★2.2／diff <font color="deepskyblue">1572</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「操作・遷移の纏め上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)
- <a href="https://yukicoder.me/problems/no/2590">No.2590 100000 Days of Christmas</a> (Advent Calendar Contest 2023 (2023-12-01) - R問題、diff <font color="yellowgreen">2185</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2426">No.2426 Select Plus or Minus</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - C問題、diff <font color="deepskyblue">1273</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)
- <a href="https://yukicoder.me/problems/no/2695">No.2695 Warp Zone</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - E問題、diff <font color="deepskyblue">1337</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="bool値の充足可能性判定">125. bool値の充足可能性判定</h2>

### 難易度統計

「bool値の充足可能性判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1679</font>
- 2024年: ★2.2／diff <font color="blue">1610</font>
- 2023年: ★2.5／diff <font color="blue">1724</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「bool値の充足可能性判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2674">No.2674 k-Walk on Bipartite</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - D問題、diff <font color="blue">1920</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)

　
<h2 id="試し割り法">126. 試し割り法</h2>

### 難易度統計

「試し割り法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1696</font>
- 2024年: ★2.6／diff <font color="blue">1904</font>
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
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)
- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="累積和">127. 累積和</h2>

### 難易度統計

「累積和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1721</font>
- 2024年: ★2.5／diff <font color="blue">1880</font>
- 2023年: ★2.5／diff <font color="blue">1732</font>
- 2022年: ★1.8／diff <font color="green">1100</font>

### レベル別問題一覧

「累積和」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題、diff <font color="brown">406</font>)
- <a href="https://yukicoder.me/problems/no/2124">No.2124 Guess the Permutation</a> (yukicoder contest 368 (2022-11-18) - A問題、diff <font color="green">1158</font>)
- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)
- <a href="https://yukicoder.me/problems/no/2961">No.2961 Shiny Monster Master</a> (yukicoder contest 453 (2024-11-16) - B問題、diff <font color="green">940</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題、diff <font color="deepskyblue">1206</font>)
- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)
- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)
- <a href="https://yukicoder.me/problems/no/2694">No.2694 The Early Bird Catches The Worm</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - D問題、diff <font color="deepskyblue">1276</font>)
- <a href="https://yukicoder.me/problems/no/2730">No.2730 Two Types Luggage</a> (yukicoder contest 428 (2024-04-19) - C問題、diff <font color="deepskyblue">1279</font>)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題、diff <font color="blue">1632</font>)
- <a href="https://yukicoder.me/problems/no/2352">No.2352 Sharpened Knife in Fall</a> (yukicoder contest 393 (2023-06-16) - C問題、diff <font color="deepskyblue">1560</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)
- <a href="https://yukicoder.me/problems/no/2716">No.2716 Falcon Method</a> (yukicoder contest 426 (2024-04-05) - C問題、diff <font color="blue">1809</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2625">No.2625 Bouns Ai</a> (yukicoder contest 417 (2024-02-09) - E問題、diff <font color="blue">1654</font>)
- <a href="https://yukicoder.me/problems/no/2643">No.2643 Many Range Sums Problems</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - G問題、diff <font color="orange">2765</font>)
- <a href="https://yukicoder.me/problems/no/2653">No.2653 [Cherry 6th Tune] Re: start! (Make it Zero!)</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - G問題、diff <font color="yellowgreen">2247</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="集合管理">128. 集合管理</h2>

### 難易度統計

「集合管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1738</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1555</font>
- 2023年: ★2.5／diff <font color="blue">1859</font>
- 2022年: ★3／diff <font color="yellowgreen">2121</font>

### レベル別問題一覧

「集合管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)
- <a href="https://yukicoder.me/problems/no/2607">No.2607 Add One Digit</a> (yukicoder contest 415 (2024-01-19) - A問題、diff <font color="green">1070</font>)
- <a href="https://yukicoder.me/problems/no/2714">No.2714 Amaou</a> (yukicoder contest 426 (2024-04-05) - A問題、diff <font color="brown">595</font>)
- <a href="https://yukicoder.me/problems/no/2737">No.2737 Compound Word</a> (CPCTF 2024 : PPC (2024-04-20) - B問題、diff <font color="brown">514</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)
- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2731">No.2731 Two Colors</a> (yukicoder contest 428 (2024-04-19) - D問題、diff <font color="deepskyblue">1442</font>)
- <a href="https://yukicoder.me/problems/no/2740">No.2740 Old Maid</a> (CPCTF 2024 : PPC (2024-04-20) - E問題、diff <font color="deepskyblue">1366</font>)
- <a href="https://yukicoder.me/problems/no/2804">No.2804 Fixer And Ratism</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - B問題、diff <font color="blue">1779</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題、diff <font color="deepskyblue">1302</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)
- <a href="https://yukicoder.me/problems/no/2684">No.2684 折々の色</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - F問題、diff <font color="blue">1790</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)
- <a href="https://yukicoder.me/problems/no/2771">No.2771 Personal Space</a> (yukicoder contest 431 (2024-05-31) - G問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="区間を切片の差に翻訳">129. 区間を切片の差に翻訳</h2>

### 難易度統計

「区間を切片の差に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1754</font>
- 2024年: ★2.3／diff <font color="blue">1709</font>
- 2023年: ★2.5／diff <font color="blue">1891</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間を切片の差に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)
- <a href="https://yukicoder.me/problems/no/2474">No.2474 Empty Quartz</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - H問題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2653">No.2653 [Cherry 6th Tune] Re: start! (Make it Zero!)</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - G問題、diff <font color="yellowgreen">2247</font>)

　
<h2 id="不変量に注目">130. 不変量に注目</h2>

### 難易度統計

「不変量に注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1772</font>
- 2024年: ★2.5／diff <font color="blue">1845</font>
- 2023年: ★2.2／diff <font color="deepskyblue">1442</font>
- 2022年: ★2.8／diff <font color="yellowgreen">2052</font>

### レベル別問題一覧

「不変量に注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2525">No.2525 Great Move</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - A問題、diff <font color="brown">424</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2451">No.2451 Redistribute Integers</a> (yukicoder contest 403 (2023-09-01) - B問題、diff <font color="green">1158</font>)
- <a href="https://yukicoder.me/problems/no/2811">No.2811 Calculation Within Sequence</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - A問題、diff <font color="deepskyblue">1260</font>)
- <a href="https://yukicoder.me/problems/no/2835">No.2835 Take and Flip</a> (yukicoder contest 440 (2024-08-09) - A問題、diff <font color="green">819</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題、diff <font color="green">912</font>)
- <a href="https://yukicoder.me/problems/no/2335">No.2335 Jump</a> (yukicoder contest 391 (2023-06-02) - B問題、diff <font color="green">1025</font>)
- <a href="https://yukicoder.me/problems/no/2629">No.2629 A replace B replace C</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - B問題、diff <font color="green">1124</font>)
- <a href="https://yukicoder.me/problems/no/2648">No.2648 [Cherry 6th Tune D] 一次元の馬</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - B問題、diff <font color="green">912</font>)
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)
- <a href="https://yukicoder.me/problems/no/2812">No.2812 Plus Minus Blackboard</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - B問題、diff <font color="blue">1698</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2628">No.2628 Shrinkage</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - A問題、diff <font color="yellowgreen">2025</font>)
- <a href="https://yukicoder.me/problems/no/2674">No.2674 k-Walk on Bipartite</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - D問題、diff <font color="blue">1920</font>)
- <a href="https://yukicoder.me/problems/no/2723">No.2723 Fortune-telling by Flowers</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - C問題、diff <font color="blue">1771</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)
- <a href="https://yukicoder.me/problems/no/2742">No.2742 Car Flow</a> (CPCTF 2024 : PPC (2024-04-20) - G問題、diff <font color="blue">1969</font>)
- <a href="https://yukicoder.me/problems/no/2796">No.2796 Small Matryoshka</a> (yukicoder contest 435 (2024-06-28) - B問題、diff <font color="blue">1848</font>)
- <a href="https://yukicoder.me/problems/no/2845">No.2845 Birthday Pattern in Two Different Calendars</a> (yukicoder contest 441 (2024-08-23) - D問題、diff <font color="blue">1947</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2519">No.2519 Coins in Array</a> (yukicoder contest 410 (2023-10-27) - E問題、diff <font color="yellowgreen">2069</font>)
- <a href="https://yukicoder.me/problems/no/2521">No.2521 Don't be Same</a> (yukicoder contest 410 (2023-10-27) - G問題、diff <font color="yellowgreen">2357</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)
- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)
- <a href="https://yukicoder.me/problems/no/2814">No.2814 Block Game</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - D問題、diff <font color="orange">2676</font>)
- <a href="https://yukicoder.me/problems/no/2821">No.2821 A[i] ← 2A[j] - A[i]</a> (yukicoder contest 438 (2024-07-26) - C問題、diff <font color="blue">1905</font>)
- <a href="https://yukicoder.me/problems/no/2837">No.2837 Flip Triomino</a> (yukicoder contest 440 (2024-08-09) - C問題、diff <font color="yellowgreen">2099</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題、diff <font color="orange">2500</font>)
- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="損をしない変形">131. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形">損をしない変形</a></h2>

### 難易度統計

「[損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.4／diff <font color="blue">1820</font>
- 2024年: ★2.4／diff <font color="blue">1847</font>
- 2023年: ★2.4／diff <font color="blue">1734</font>
- 2022年: ★2.6／diff <font color="yellowgreen">2083</font>

### レベル別問題一覧

「[損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題、diff <font color="brown">744</font>)
- <a href="https://yukicoder.me/problems/no/2729">No.2729 Addition and Multiplication in yukicoder (Easy)</a> (yukicoder contest 428 (2024-04-19) - B問題、diff <font color="green">919</font>)
- <a href="https://yukicoder.me/problems/no/2738">No.2738 CPC To F</a> (CPCTF 2024 : PPC (2024-04-20) - C問題、diff <font color="deepskyblue">1245</font>)

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
- <a href="https://yukicoder.me/problems/no/2656">No.2656 XOR Slimes</a> (yukicoder contest 419 (2024-03-01) - B問題、diff <font color="blue">1726</font>)
- <a href="https://yukicoder.me/problems/no/2744">No.2744 Power! or +1</a> (CPCTF 2024 : PPC (2024-04-20) - I問題、diff <font color="yellowgreen">2309</font>)
- <a href="https://yukicoder.me/problems/no/2845">No.2845 Birthday Pattern in Two Different Calendars</a> (yukicoder contest 441 (2024-08-23) - D問題、diff <font color="blue">1947</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題、diff <font color="orange">2758</font>)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)
- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題、diff <font color="yellowgreen">2175</font>)
- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題、diff <font color="yellowgreen">2274</font>)
- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2734">No.2734 Addition and Multiplication in yukicoder (Hard)</a> (yukicoder contest 428 (2024-04-19) - G問題、diff <font color="yellowgreen">2034</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2096">No.2096 Rage With Our Friends</a> (yukicoder contest 363 (2022-10-07) - E問題、diff <font color="orange">2690</font>)

　
<h2 id="３進法">132. ３進法</h2>

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

　
<h2 id="複数配列への範囲加算更新を１つの配列に纏め上げ">133. 複数配列への範囲加算更新を１つの配列に纏め上げ</h2>

### 難易度統計

「複数配列への範囲加算更新を１つの配列に纏め上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1358</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="deepskyblue">1358</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「複数配列への範囲加算更新を１つの配列に纏め上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)

　
<h2 id="部分和と補部分和の差の最小化">134. 部分和と補部分和の差の最小化</h2>

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

　
<h2 id="挿入ソート">135. 挿入ソート</h2>

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

　
<h2 id="最遠点計算">136. 最遠点計算</h2>

### 難易度統計

「最遠点計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1504</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1473</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1536</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最遠点計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2261">No.2261 Coffee</a> (yukicoder contest 383 (2023-04-07) - C問題、diff <font color="deepskyblue">1536</font>)
- <a href="https://yukicoder.me/problems/no/2844">No.2844 Birthday Party Decoration</a> (yukicoder contest 441 (2024-08-23) - C問題、diff <font color="deepskyblue">1473</font>)

　
<h2 id="平方数判定">137. 平方数判定</h2>

### 難易度統計

「平方数判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1535</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1280</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「平方数判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2721">No.2721 "Don't say N" Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - A問題、diff <font color="brown">426</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)

　
<h2 id="符号全探索による絶対値計算">138. 符号全探索による絶対値計算</h2>

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

　
<h2 id="指定序数の値の計算を被覆の先頭項管理で処理">139. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を被覆の先頭項管理で処理">指定序数の値の計算を被覆の先頭項管理で処理</a></h2>

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

　
<h2 id="言及する成分数を最大化する質問">140. 言及する成分数を最大化する質問</h2>

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

　
<h2 id="strategy stealing argument">141. strategy stealing argument</h2>

### 難易度統計

「strategy stealing argument」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="deepskyblue">1588</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1588</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「strategy stealing argument」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2722">No.2722 Kenken Fight</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - B問題、diff <font color="deepskyblue">1588</font>)

　
<h2 id="倍数メビウス変換">142. 倍数メビウス変換</h2>

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

　
<h2 id="不明な想定解">143. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不明な想定解">不明な想定解</a></h2>

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

　
<h2 id="マッチ度ごとに管理">144. マッチ度ごとに管理</h2>

### 難易度統計

「マッチ度ごとに管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1642</font>
- 2024年: ★3／diff <font color="orange">2414</font>
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
- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)

　
<h2 id="経路数え上げ">145. 経路数え上げ</h2>

### 難易度統計

「経路数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1663</font>
- 2024年: ★2.5／diff <font color="blue">1813</font>
- 2023年: ★2.2／diff <font color="green">1140</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「経路数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題、diff <font color="green">831</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2430">No.2430 Damage Zone</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - G問題、diff <font color="deepskyblue">1449</font>)
- <a href="https://yukicoder.me/problems/no/2733">No.2733 Just K-times TSP</a> (yukicoder contest 428 (2024-04-19) - F問題、diff <font color="blue">1977</font>)
- <a href="https://yukicoder.me/problems/no/2807">No.2807 Have Another Go (Easy)</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - E問題、diff <font color="yellowgreen">2004</font>)
- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="B進法による構築">146. B進法による構築</h2>

### 難易度統計

「B進法による構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1666</font>
- 2024年: ★2.5／diff <font color="blue">1782</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1318</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「B進法による構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2663">No.2663 Zero-Sum Submatrices</a> (yukicoder contest 420 (2024-03-08) - A問題、diff <font color="deepskyblue">1204</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2410">No.2410 Nine Numbers</a> (yukicoder contest 401 (2023-08-11) - D問題、diff <font color="deepskyblue">1318</font>)
- <a href="https://yukicoder.me/problems/no/2609">No.2609 Decreasing GCDs</a> (yukicoder contest 415 (2024-01-19) - C問題、diff <font color="deepskyblue">1531</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2965">No.2965 Don't Stop the Game again</a> (yukicoder contest 453 (2024-11-16) - F問題、diff <font color="orange">2613</font>)

　
<h2 id="ハミルトン路構築">147. ハミルトン路構築</h2>

### 難易度統計

「ハミルトン路構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1670</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1670</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ハミルトン路構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2353">No.2353 Guardian Dogs in Spring</a> (yukicoder contest 393 (2023-06-16) - D問題、diff <font color="blue">1670</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)

　
<h2 id="検索">148. 検索</h2>

### 難易度統計

「検索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1683</font>
- 2024年: ★2.6／diff <font color="blue">1936</font>
- 2023年: ★2.7／diff <font color="blue">1768</font>
- 2022年: ★1.5／diff <font color="brown">588</font>

### レベル別問題一覧

「検索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題、diff <font color="brown">588</font>)
- <a href="https://yukicoder.me/problems/no/2795">No.2795 Perfect Number</a> (yukicoder contest 435 (2024-06-28) - A問題、diff <font color="green">873</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題、diff <font color="blue">1768</font>)
- <a href="https://yukicoder.me/problems/no/2722">No.2722 Kenken Fight</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - B問題、diff <font color="deepskyblue">1588</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2476">No.2476 Knight Game</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - J問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="配列を像・頻度表で管理">149. 配列を像・頻度表で管理</h2>

### 難易度統計

「配列を像・頻度表で管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1684</font>
- 2024年: ★2.4／diff <font color="deepskyblue">1595</font>
- 2023年: ★2.6／diff <font color="blue">1830</font>
- 2022年: ★3／diff <font color="blue">1696</font>

### レベル別問題一覧

「配列を像・頻度表で管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)
- <a href="https://yukicoder.me/problems/no/2961">No.2961 Shiny Monster Master</a> (yukicoder contest 453 (2024-11-16) - B問題、diff <font color="green">940</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="尺取り法">150. 尺取り法</h2>

### 難易度統計

「尺取り法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1704</font>
- 2024年: ★2.5／diff <font color="blue">1670</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1590</font>
- 2022年: ★3／diff <font color="blue">1988</font>

### レベル別問題一覧

「尺取り法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2298">No.2298 yukicounter</a> (yukicoder contest 388 (2023-05-12) - B問題、diff <font color="green">813</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)
- <a href="https://yukicoder.me/problems/no/2601">No.2601 Very Poor</a> (yukicoder contest 414 (2024-01-12) - C問題、diff <font color="green">1032</font>)
- <a href="https://yukicoder.me/problems/no/2694">No.2694 The Early Bird Catches The Worm</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - D問題、diff <font color="deepskyblue">1276</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題、diff <font color="blue">1632</font>)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)
- <a href="https://yukicoder.me/problems/no/2723">No.2723 Fortune-telling by Flowers</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - C問題、diff <font color="blue">1771</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2553">No.2553 Holidays</a> (MMA Contest 017 (2023-11-25) - G問題、diff <font color="red">2858</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)
- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

　
<h2 id="二項定理">151. 二項定理</h2>

### 難易度統計

「二項定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1709</font>
- 2024年: ★3／diff <font color="blue">1789</font>
- 2023年: ★2／diff <font color="blue">1629</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「二項定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2550">No.2550 MORE! JUMP! MORE!</a> (MMA Contest 017 (2023-11-25) - D問題、diff <font color="blue">1629</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)

　
<h2 id="ワーシャル・フロイド法">152. ワーシャル・フロイド法</h2>

### 難易度統計

「ワーシャル・フロイド法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1717</font>
- 2024年: ★2.5／diff <font color="blue">1717</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ワーシャル・フロイド法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2640">No.2640 traO Stamps</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - D問題、diff <font color="blue">1717</font>)

　
<h2 id="階乗計算">153. 階乗計算</h2>

### 難易度統計

「階乗計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1717</font>
- 2024年: ★2.6／diff <font color="blue">1762</font>
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
- <a href="https://yukicoder.me/problems/no/2636">No.2636 No Waiting in Vain</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

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
- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)

　
<h2 id="円環の倍化実装">154. 円環の倍化実装</h2>

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

　
<h2 id="部分集合DP">155. 部分集合DP</h2>

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

　
<h2 id="ベルマンフォード法">156. ベルマンフォード法</h2>

### 難易度統計

「ベルマンフォード法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1749</font>
- 2024年: ★2.5／diff <font color="blue">1749</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ベルマンフォード法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2712">No.2712 Play more!</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - G問題、diff <font color="blue">1749</font>)

　
<h2 id="負閉路検出">157. 負閉路検出</h2>

### 難易度統計

「負閉路検出」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1749</font>
- 2024年: ★2.5／diff <font color="blue">1749</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「負閉路検出」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2712">No.2712 Play more!</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - G問題、diff <font color="blue">1749</font>)

　
<h2 id="差分管理">158. 差分管理</h2>

### 難易度統計

「差分管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1754</font>
- 2024年: ★2.5／diff <font color="blue">1754</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「差分管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)

　
<h2 id="Next DP">159. Next DP</h2>

### 難易度統計

「Next DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1762</font>
- 2024年: ★2.5／diff <font color="blue">1762</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Next DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

　
<h2 id="区間族管理">160. 区間族管理</h2>

### 難易度統計

「区間族管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1764</font>
- 2024年: ★2.7／diff <font color="blue">1934</font>
- 2023年: ★2.5／diff <font color="blue">1675</font>
- 2022年: ★2.5／diff <font color="blue">1649</font>

### レベル別問題一覧

「区間族管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2298">No.2298 yukicounter</a> (yukicoder contest 388 (2023-05-12) - B問題、diff <font color="green">813</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2779">No.2779 Don't make Pair</a> (yukicoder contest 432 (2024-06-07) - G問題、diff <font color="green">951</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)
- <a href="https://yukicoder.me/problems/no/2486">No.2486 Don't come next to me</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - A問題、diff <font color="brown">712</font>)
- <a href="https://yukicoder.me/problems/no/2500">No.2500 Products in a Range</a> (yukicoder contest 408 (2023-10-13) - A問題、diff <font color="blue">1996</font>)
- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)
- <a href="https://yukicoder.me/problems/no/2723">No.2723 Fortune-telling by Flowers</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - C問題、diff <font color="blue">1771</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2553">No.2553 Holidays</a> (MMA Contest 017 (2023-11-25) - G問題、diff <font color="red">2858</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2771">No.2771 Personal Space</a> (yukicoder contest 431 (2024-05-31) - G問題、diff <font color="yellowgreen">2170</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

　
<h2 id="階乗逆元計算">161. 階乗逆元計算</h2>

### 難易度統計

「階乗逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1768</font>
- 2024年: ★2.8／diff <font color="blue">1957</font>
- 2023年: ★2.5／diff <font color="blue">1675</font>
- 2022年: ★2.1／diff <font color="deepskyblue">1546</font>

### レベル別問題一覧

「階乗逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2636">No.2636 No Waiting in Vain</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="Vieta Jumping">162. Vieta Jumping</h2>

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

　
<h2 id="解と係数の関係">163. 解と係数の関係</h2>

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

　
<h2 id="一要素削除">164. 一要素削除</h2>

### 難易度統計

「一要素削除」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1769</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1382</font>
- 2023年: ★2.5／diff <font color="blue">1909</font>
- 2022年: ★3.2／diff <font color="yellowgreen">2333</font>

### レベル別問題一覧

「一要素削除」を主たる解法に含む問題のレベルごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2599">No.2599 Summer Project</a> (yukicoder contest 414 (2024-01-12) - A問題、diff <font color="gray">352</font>)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2372">No.2372 既視感</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - B問題、diff <font color="deepskyblue">1313</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2740">No.2740 Old Maid</a> (CPCTF 2024 : PPC (2024-04-20) - E問題、diff <font color="deepskyblue">1366</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="価値上限ありナップサック最適化">165. 価値上限ありナップサック最適化</h2>

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

　
<h2 id="重複選択可価値上限ありナップサック最適化">166. 重複選択可価値上限ありナップサック最適化</h2>

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

　
<h2 id="ミラー戦略">167. ミラー戦略</h2>

### 難易度統計

「ミラー戦略」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1795</font>
- 2024年: ★2.5／diff <font color="blue">1861</font>
- 2023年: ★2.6／diff <font color="deepskyblue">1590</font>
- 2022年: ★2.5／diff <font color="blue">1905</font>

### レベル別問題一覧

「ミラー戦略」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2721">No.2721 "Don't say N" Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - A問題、diff <font color="brown">426</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題、diff <font color="green">912</font>)
- <a href="https://yukicoder.me/problems/no/2760">No.2760 not fair position game</a> (yukicoder contest 430 (2024-05-17) - D問題、diff <font color="deepskyblue">1498</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2481">No.2481 Shiritori</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - C問題、diff <font color="blue">1706</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2476">No.2476 Knight Game</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - J問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)
- <a href="https://yukicoder.me/problems/no/2631">No.2631 Rectangle Grid Game</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - D問題、diff <font color="yellowgreen">2176</font>)
- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)
- <a href="https://yukicoder.me/problems/no/2814">No.2814 Block Game</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - D問題、diff <font color="orange">2676</font>)

　
<h2 id="２種の数値を足し引きして１種に帰着">168. ２種の数値を足し引きして１種に帰着</h2>

### 難易度統計

「２種の数値を足し引きして１種に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1803</font>
- 2024年: ★2.5／diff <font color="blue">1803</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「２種の数値を足し引きして１種に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2852">No.2852 Yakitori Optimization Problem</a> (yukicoder contest 442 (2024-08-25) - C問題、diff <font color="brown">774</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2623">No.2623 Room Allocation</a> (yukicoder contest 417 (2024-02-09) - C問題、diff <font color="deepskyblue">1328</font>)
- <a href="https://yukicoder.me/problems/no/2723">No.2723 Fortune-telling by Flowers</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - C問題、diff <font color="blue">1771</font>)
- <a href="https://yukicoder.me/problems/no/2856">No.2856 Junk Market Game</a> (yukicoder contest 442 (2024-08-25) - G問題、diff <font color="blue">1824</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="素因数分解">169. 素因数分解</h2>

### 難易度統計

「素因数分解」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1804</font>
- 2024年: ★2.4／diff <font color="blue">1741</font>
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
- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)
- <a href="https://yukicoder.me/problems/no/2751">No.2751 429-like Number</a> (yukicoder contest 429 (2024-05-10) - C問題、diff <font color="deepskyblue">1351</font>)
- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題、diff <font color="yellowgreen">2291</font>)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2570">No.2570 最大最大公約数</a> (緑以下コンテスト  Extra (2023-12-02) - B問題、diff <font color="blue">1638</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2756">No.2756 GCD Teleporter</a> (yukicoder contest 429 (2024-05-10) - H問題、diff <font color="blue">1751</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)
- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)
- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="同じ値の纏め上げ">170. 同じ値の纏め上げ</h2>

### 難易度統計

「同じ値の纏め上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1805</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2098</font>
- 2023年: ★2.5／diff <font color="blue">1660</font>
- 2022年: ★2.3／diff <font color="blue">1730</font>

### レベル別問題一覧

「同じ値の纏め上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題、diff <font color="deepskyblue">1206</font>)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題、diff <font color="green">1069</font>)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題、diff <font color="deepskyblue">1258</font>)
- <a href="https://yukicoder.me/problems/no/2828">No.2828 Remainder Game</a> (yukicoder contest 439 (2024-08-02) - B問題、diff <font color="blue">1696</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題、diff <font color="blue">1865</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)
- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)
- <a href="https://yukicoder.me/problems/no/2834">No.2834 Work to Play</a> (yukicoder contest 439 (2024-08-02) - H問題、diff <font color="red">3011</font>)

　
<h2 id="あみだくじと置換の対応">171. あみだくじと置換の対応</h2>

### 難易度統計

「あみだくじと置換の対応」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1806</font>
- 2024年: ★2.5／diff <font color="blue">1806</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「あみだくじと置換の対応」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)

　
<h2 id="置換の互換表示">172. 置換の互換表示</h2>

### 難易度統計

「置換の互換表示」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1806</font>
- 2024年: ★2.5／diff <font color="blue">1806</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「置換の互換表示」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)

　
<h2 id="最大・最小要素取得">173. 最大・最小要素取得</h2>

### 難易度統計

「最大・最小要素取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1808</font>
- 2024年: ★2.4／diff <font color="blue">1798</font>
- 2023年: ★2.6／diff <font color="blue">1777</font>
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「最大・最小要素取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2731">No.2731 Two Colors</a> (yukicoder contest 428 (2024-04-19) - D問題、diff <font color="deepskyblue">1442</font>)
- <a href="https://yukicoder.me/problems/no/2740">No.2740 Old Maid</a> (CPCTF 2024 : PPC (2024-04-20) - E問題、diff <font color="deepskyblue">1366</font>)
- <a href="https://yukicoder.me/problems/no/2804">No.2804 Fixer And Ratism</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - B問題、diff <font color="blue">1779</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)
- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2771">No.2771 Personal Space</a> (yukicoder contest 431 (2024-05-31) - G問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="ダイクストラ法">174. ダイクストラ法</h2>

### 難易度統計

「ダイクストラ法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1812</font>
- 2024年: ★2.3／diff <font color="blue">1787</font>
- 2023年: ★2.7／diff <font color="blue">1841</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ダイクストラ法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2739">No.2739 Time is money</a> (CPCTF 2024 : PPC (2024-04-20) - D問題、diff <font color="blue">1695</font>)
- <a href="https://yukicoder.me/problems/no/2759">No.2759 Take Pictures, Elements?</a> (yukicoder contest 430 (2024-05-17) - C問題、diff <font color="deepskyblue">1565</font>)
- <a href="https://yukicoder.me/problems/no/2805">No.2805 Go to School</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - C問題、diff <font color="blue">1720</font>)
- <a href="https://yukicoder.me/problems/no/2855">No.2855 Move on Grid</a> (yukicoder contest 442 (2024-08-25) - F問題、diff <font color="deepskyblue">1510</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2328">No.2328 Build Walls</a> (MMA Contest 015  (2023-05-28) - G問題、diff <font color="blue">1915</font>)
- <a href="https://yukicoder.me/problems/no/2354">No.2354 Poor Sight in Winter</a> (yukicoder contest 393 (2023-06-16) - E問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2569">No.2569 はじめてのおつかいHard</a> (緑以下コンテスト  Extra (2023-12-02) - A問題、diff <font color="deepskyblue">1385</font>)
- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)
- <a href="https://yukicoder.me/problems/no/2695">No.2695 Warp Zone</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - E問題、diff <font color="deepskyblue">1337</font>)
- <a href="https://yukicoder.me/problems/no/2744">No.2744 Power! or +1</a> (CPCTF 2024 : PPC (2024-04-20) - I問題、diff <font color="yellowgreen">2309</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2366">No.2366 登校</a> (yukicoder contest 395 (2023-06-30) - C問題、diff <font color="yellowgreen">2294</font>)
- <a href="https://yukicoder.me/problems/no/2387">No.2387 Yokan Factory</a> (yukicoder contest 398 (2023-07-21) - C問題、diff <font color="deepskyblue">1376</font>)
- <a href="https://yukicoder.me/problems/no/2477">No.2477 Drifting</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - K問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

　
<h2 id="二分探索">175. 二分探索</h2>

### 難易度統計

「二分探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1813</font>
- 2024年: ★2.4／diff <font color="blue">1800</font>
- 2023年: ★2.4／diff <font color="blue">1758</font>
- 2022年: ★3.2／diff <font color="yellowgreen">2185</font>

### レベル別問題一覧

「二分探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2479">No.2479 Sum of Squares</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - A問題、diff <font color="brown">779</font>)
- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)
- <a href="https://yukicoder.me/problems/no/2721">No.2721 "Don't say N" Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - A問題、diff <font color="brown">426</font>)
- <a href="https://yukicoder.me/problems/no/2961">No.2961 Shiny Monster Master</a> (yukicoder contest 453 (2024-11-16) - B問題、diff <font color="green">940</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題、diff <font color="blue">1856</font>)
- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題、diff <font color="green">1174</font>)
- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)
- <a href="https://yukicoder.me/problems/no/2420">No.2420 Simple Problem</a> (MMA Contest 016 (2023-08-12) - G問題、diff <font color="deepskyblue">1228</font>)
- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)
- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)
- <a href="https://yukicoder.me/problems/no/2774">No.2774 Wake up Record 2</a> (yukicoder contest 432 (2024-06-07) - B問題、diff <font color="brown">612</font>)
- <a href="https://yukicoder.me/problems/no/2855">No.2855 Move on Grid</a> (yukicoder contest 442 (2024-08-25) - F問題、diff <font color="deepskyblue">1510</font>)
- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題、diff <font color="yellowgreen">2193</font>)
- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題、diff <font color="blue">1774</font>)
- <a href="https://yukicoder.me/problems/no/2352">No.2352 Sharpened Knife in Fall</a> (yukicoder contest 393 (2023-06-16) - C問題、diff <font color="deepskyblue">1560</font>)
- <a href="https://yukicoder.me/problems/no/2354">No.2354 Poor Sight in Winter</a> (yukicoder contest 393 (2023-06-16) - E問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2501">No.2501 Maximum Inversion Number</a> (yukicoder contest 408 (2023-10-13) - B問題、diff <font color="yellowgreen">2064</font>)
- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2716">No.2716 Falcon Method</a> (yukicoder contest 426 (2024-04-05) - C問題、diff <font color="blue">1809</font>)
- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)
- <a href="https://yukicoder.me/problems/no/2786">No.2786 RMQ on Grid Path</a> (yukicoder contest 433 (2024-06-14) - F問題、diff <font color="yellowgreen">2162</font>)
- <a href="https://yukicoder.me/problems/no/2962">No.2962 Sum Bomb Bomber</a> (yukicoder contest 453 (2024-11-16) - C問題、diff <font color="deepskyblue">1579</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)
- <a href="https://yukicoder.me/problems/no/2387">No.2387 Yokan Factory</a> (yukicoder contest 398 (2023-07-21) - C問題、diff <font color="deepskyblue">1376</font>)
- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)
- <a href="https://yukicoder.me/problems/no/2617">No.2617 容量3のナップザック</a> (yukicoder contest 416 (2024-01-26) - D問題、diff <font color="orange">2491</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)
- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)
- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)
- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="剰余計算">176. 剰余計算</h2>

### 難易度統計

「剰余計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1820</font>
- 2024年: ★2.5／diff <font color="blue">1907</font>
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
- <a href="https://yukicoder.me/problems/no/2679">No.2679 MODice</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - A問題、diff <font color="brown">721</font>)
- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)
- <a href="https://yukicoder.me/problems/no/2709">No.2709 1975 Powers</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - D問題、diff <font color="green">1143</font>)
- <a href="https://yukicoder.me/problems/no/2729">No.2729 Addition and Multiplication in yukicoder (Easy)</a> (yukicoder contest 428 (2024-04-19) - B問題、diff <font color="green">919</font>)

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
- <a href="https://yukicoder.me/problems/no/2636">No.2636 No Waiting in Vain</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2649">No.2649 [Cherry 6th Tune C] Anthem Flower</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - C問題、diff <font color="deepskyblue">1322</font>)
- <a href="https://yukicoder.me/problems/no/2711">No.2711 Connecting Lights</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - F問題、diff <font color="deepskyblue">1396</font>)
- <a href="https://yukicoder.me/problems/no/2783">No.2783 4-33 Easy</a> (yukicoder contest 433 (2024-06-14) - C問題、diff <font color="blue">1705</font>)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

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
- <a href="https://yukicoder.me/problems/no/2646">No.2646 Cycle Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2685">No.2685 Cell Proliferation (Easy)</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - G問題、diff <font color="blue">1983</font>)
- <a href="https://yukicoder.me/problems/no/2807">No.2807 Have Another Go (Easy)</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - E問題、diff <font color="yellowgreen">2004</font>)
- <a href="https://yukicoder.me/problems/no/2830">No.2830 Don't Stop the Game</a> (yukicoder contest 439 (2024-08-02) - D問題、diff <font color="orange">2525</font>)
- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)
- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

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
- <a href="https://yukicoder.me/problems/no/2631">No.2631 Rectangle Grid Game</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - D問題、diff <font color="yellowgreen">2176</font>)
- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)
- <a href="https://yukicoder.me/problems/no/2653">No.2653 [Cherry 6th Tune] Re: start! (Make it Zero!)</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - G問題、diff <font color="yellowgreen">2247</font>)
- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)
- <a href="https://yukicoder.me/problems/no/2734">No.2734 Addition and Multiplication in yukicoder (Hard)</a> (yukicoder contest 428 (2024-04-19) - G問題、diff <font color="yellowgreen">2034</font>)
- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2772">No.2772 Appearing Even Times</a> (yukicoder contest 431 (2024-05-31) - H問題、diff <font color="blue">1925</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2814">No.2814 Block Game</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - D問題、diff <font color="orange">2676</font>)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)
- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)
- <a href="https://yukicoder.me/problems/no/2834">No.2834 Work to Play</a> (yukicoder contest 439 (2024-08-02) - H問題、diff <font color="red">3011</font>)
- <a href="https://yukicoder.me/problems/no/2837">No.2837 Flip Triomino</a> (yukicoder contest 440 (2024-08-09) - C問題、diff <font color="yellowgreen">2099</font>)
- <a href="https://yukicoder.me/problems/no/2838">No.2838 Diagonals</a> (yukicoder contest 440 (2024-08-09) - D問題、diff <font color="yellowgreen">2305</font>)
- <a href="https://yukicoder.me/problems/no/2839">No.2839 AND Constraint</a> (yukicoder contest 440 (2024-08-09) - E問題、diff <font color="orange">2648</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="包除原理">177. 包除原理</h2>

### 難易度統計

「包除原理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1830</font>
- 2024年: ★2／diff <font color="blue">1814</font>
- 2023年: ★2.6／diff <font color="blue">1683</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「包除原理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2638">No.2638 Initial fare</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - B問題、diff <font color="blue">1624</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題、diff <font color="green">1049</font>)
- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2807">No.2807 Have Another Go (Easy)</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - E問題、diff <font color="yellowgreen">2004</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="多項定理">178. 多項定理</h2>

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

　
<h2 id="エラトステネスの篩">179. エラトステネスの篩</h2>

### 難易度統計

「エラトステネスの篩」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1832</font>
- 2024年: ★2.4／diff <font color="blue">1635</font>
- 2023年: ★2.7／diff <font color="orange">2452</font>
- 2022年: ★3／diff <font color="yellowgreen">2167</font>

### レベル別問題一覧

「エラトステネスの篩」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2750">No.2750 Number of Prime Factors</a> (yukicoder contest 429 (2024-05-10) - B問題、diff <font color="green">1026</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2751">No.2751 429-like Number</a> (yukicoder contest 429 (2024-05-10) - C問題、diff <font color="deepskyblue">1351</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2609">No.2609 Decreasing GCDs</a> (yukicoder contest 415 (2024-01-19) - C問題、diff <font color="deepskyblue">1531</font>)
- <a href="https://yukicoder.me/problems/no/2610">No.2610 Decreasing LCMs</a> (yukicoder contest 415 (2024-01-19) - D問題、diff <font color="yellowgreen">2129</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)
- <a href="https://yukicoder.me/problems/no/2725">No.2725 Coprime Game 2</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - E問題、diff <font color="blue">1944</font>)
- <a href="https://yukicoder.me/problems/no/2756">No.2756 GCD Teleporter</a> (yukicoder contest 429 (2024-05-10) - H問題、diff <font color="blue">1751</font>)

　
<h2 id="オイラーの定理">180. オイラーの定理</h2>

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

　
<h2 id="オイラーの定理による逆元計算">181. オイラーの定理による逆元計算</h2>

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

　
<h2 id="合成数を法とする逆元計算">182. 合成数を法とする逆元計算</h2>

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

　
<h2 id="エラトステネスの篩による素数判定">183. エラトステネスの篩による素数判定</h2>

### 難易度統計

「エラトステネスの篩による素数判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1845</font>
- 2024年: ★2.5／diff <font color="blue">1845</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「エラトステネスの篩による素数判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

　
<h2 id="素数計数関数前計算">184. 素数計数関数前計算</h2>

### 難易度統計

「素数計数関数前計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1845</font>
- 2024年: ★2.5／diff <font color="blue">1845</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素数計数関数前計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

　
<h2 id="素数判定">185. 素数判定</h2>

### 難易度統計

「素数判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1845</font>
- 2024年: ★2.5／diff <font color="blue">1845</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素数判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

　
<h2 id="Dilworthの定理">186. Dilworthの定理</h2>

### 難易度統計

「Dilworthの定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1848</font>
- 2024年: ★2.5／diff <font color="blue">1848</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Dilworthの定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2796">No.2796 Small Matryoshka</a> (yukicoder contest 435 (2024-06-28) - B問題、diff <font color="blue">1848</font>)

　
<h2 id="鎖への分割数の最小化">187. 鎖への分割数の最小化</h2>

### 難易度統計

「鎖への分割数の最小化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1848</font>
- 2024年: ★2.5／diff <font color="blue">1848</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「鎖への分割数の最小化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2796">No.2796 Small Matryoshka</a> (yukicoder contest 435 (2024-06-28) - B問題、diff <font color="blue">1848</font>)

　
<h2 id="ポテンシャル付き素集合データ構造">188. ポテンシャル付き素集合データ構造</h2>

### 難易度統計

「ポテンシャル付き素集合データ構造」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1848</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2033</font>
- 2023年: ★2.5／diff <font color="blue">1724</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ポテンシャル付き素集合データ構造」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2643">No.2643 Many Range Sums Problems</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - G問題、diff <font color="orange">2765</font>)

　
<h2 id="充足可能性判定">189. 充足可能性判定</h2>

### 難易度統計

「充足可能性判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1850</font>
- 2024年: ★2.5／diff <font color="blue">1995</font>
- 2023年: ★2.5／diff <font color="blue">1742</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「充足可能性判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題、diff <font color="deepskyblue">1254</font>)
- <a href="https://yukicoder.me/problems/no/2664">No.2664 Prime Sum</a> (yukicoder contest 420 (2024-03-08) - B問題、diff <font color="deepskyblue">1301</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題、diff <font color="blue">1683</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2674">No.2674 k-Walk on Bipartite</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - D問題、diff <font color="blue">1920</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2643">No.2643 Many Range Sums Problems</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - G問題、diff <font color="orange">2765</font>)

　
<h2 id="分割統治法">190. 分割統治法</h2>

### 難易度統計

「分割統治法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1852</font>
- 2024年: ★2.6／diff <font color="yellowgreen">2036</font>
- 2023年: ★2.5／diff <font color="blue">1724</font>
- 2022年: ★2.7／diff <font color="yellowgreen">2022</font>

### レベル別問題一覧

「分割統治法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2563">No.2563 色ごとのグループ</a> (第2回緑以下コンテスト (2023-12-02) - G問題、diff <font color="green">851</font>)
- <a href="https://yukicoder.me/problems/no/2638">No.2638 Initial fare</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - B問題、diff <font color="blue">1624</font>)

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
- <a href="https://yukicoder.me/problems/no/2741">No.2741 Balanced Choice</a> (CPCTF 2024 : PPC (2024-04-20) - F問題、diff <font color="deepskyblue">1557</font>)
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)
- <a href="https://yukicoder.me/problems/no/2828">No.2828 Remainder Game</a> (yukicoder contest 439 (2024-08-02) - B問題、diff <font color="blue">1696</font>)

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
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)
- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)

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
- <a href="https://yukicoder.me/problems/no/2653">No.2653 [Cherry 6th Tune] Re: start! (Make it Zero!)</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - G問題、diff <font color="yellowgreen">2247</font>)
- <a href="https://yukicoder.me/problems/no/2686">No.2686 商品券の使い道</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - H問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)
- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)
- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)
- <a href="https://yukicoder.me/problems/no/2834">No.2834 Work to Play</a> (yukicoder contest 439 (2024-08-02) - H問題、diff <font color="red">3011</font>)
- <a href="https://yukicoder.me/problems/no/2846">No.2846 Birthday Cake</a> (yukicoder contest 441 (2024-08-23) - E問題、diff <font color="yellowgreen">2116</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題、diff <font color="orange">2737</font>)
- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)
- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題、diff <font color="orange">2566</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="階差数列">191. 階差数列</h2>

### 難易度統計

「階差数列」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1855</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2092</font>
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
- <a href="https://yukicoder.me/problems/no/2662">No.2662 Installing Cell Towers</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2962">No.2962 Sum Bomb Bomber</a> (yukicoder contest 453 (2024-11-16) - C問題、diff <font color="deepskyblue">1579</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)
- <a href="https://yukicoder.me/problems/no/2821">No.2821 A[i] ← 2A[j] - A[i]</a> (yukicoder contest 438 (2024-07-26) - C問題、diff <font color="blue">1905</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題、diff <font color="orange">2500</font>)

　
<h2 id="最短経路長計算">192. 最短経路長計算</h2>

### 難易度統計

「最短経路長計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1863</font>
- 2024年: ★2.5／diff <font color="blue">1840</font>
- 2023年: ★2.7／diff <font color="blue">1918</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最短経路長計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2739">No.2739 Time is money</a> (CPCTF 2024 : PPC (2024-04-20) - D問題、diff <font color="blue">1695</font>)
- <a href="https://yukicoder.me/problems/no/2759">No.2759 Take Pictures, Elements?</a> (yukicoder contest 430 (2024-05-17) - C問題、diff <font color="deepskyblue">1565</font>)
- <a href="https://yukicoder.me/problems/no/2805">No.2805 Go to School</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - C問題、diff <font color="blue">1720</font>)
- <a href="https://yukicoder.me/problems/no/2855">No.2855 Move on Grid</a> (yukicoder contest 442 (2024-08-25) - F問題、diff <font color="deepskyblue">1510</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2328">No.2328 Build Walls</a> (MMA Contest 015  (2023-05-28) - G問題、diff <font color="blue">1915</font>)
- <a href="https://yukicoder.me/problems/no/2354">No.2354 Poor Sight in Winter</a> (yukicoder contest 393 (2023-06-16) - E問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)
- <a href="https://yukicoder.me/problems/no/2674">No.2674 k-Walk on Bipartite</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - D問題、diff <font color="blue">1920</font>)
- <a href="https://yukicoder.me/problems/no/2695">No.2695 Warp Zone</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - E問題、diff <font color="deepskyblue">1337</font>)
- <a href="https://yukicoder.me/problems/no/2712">No.2712 Play more!</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - G問題、diff <font color="blue">1749</font>)
- <a href="https://yukicoder.me/problems/no/2744">No.2744 Power! or +1</a> (CPCTF 2024 : PPC (2024-04-20) - I問題、diff <font color="yellowgreen">2309</font>)
- <a href="https://yukicoder.me/problems/no/2786">No.2786 RMQ on Grid Path</a> (yukicoder contest 433 (2024-06-14) - F問題、diff <font color="yellowgreen">2162</font>)
- <a href="https://yukicoder.me/problems/no/2844">No.2844 Birthday Party Decoration</a> (yukicoder contest 441 (2024-08-23) - C問題、diff <font color="deepskyblue">1473</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2366">No.2366 登校</a> (yukicoder contest 395 (2023-06-30) - C問題、diff <font color="yellowgreen">2294</font>)
- <a href="https://yukicoder.me/problems/no/2387">No.2387 Yokan Factory</a> (yukicoder contest 398 (2023-07-21) - C問題、diff <font color="deepskyblue">1376</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)
- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

　
<h2 id="冪乗計算">193. 冪乗計算</h2>

### 難易度統計

「冪乗計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1877</font>
- 2024年: ★2.5／diff <font color="blue">1849</font>
- 2023年: ★2.5／diff <font color="blue">1852</font>
- 2022年: ★2.7／diff <font color="blue">1977</font>

### レベル別問題一覧

「冪乗計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)
- <a href="https://yukicoder.me/problems/no/2709">No.2709 1975 Powers</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - D問題、diff <font color="green">1143</font>)
- <a href="https://yukicoder.me/problems/no/2853">No.2853 A + B Problem</a> (yukicoder contest 442 (2024-08-25) - D問題、diff <font color="brown">774</font>)

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
- <a href="https://yukicoder.me/problems/no/2828">No.2828 Remainder Game</a> (yukicoder contest 439 (2024-08-02) - B問題、diff <font color="blue">1696</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2585">No.2585 How many "Who is Santa?"</a> (Advent Calendar Contest 2023 (2023-12-01) - M問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2685">No.2685 Cell Proliferation (Easy)</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - G問題、diff <font color="blue">1983</font>)
- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)
- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題、diff <font color="yellowgreen">2168</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)
- <a href="https://yukicoder.me/problems/no/2653">No.2653 [Cherry 6th Tune] Re: start! (Make it Zero!)</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - G問題、diff <font color="yellowgreen">2247</font>)
- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)
- <a href="https://yukicoder.me/problems/no/2734">No.2734 Addition and Multiplication in yukicoder (Hard)</a> (yukicoder contest 428 (2024-04-19) - G問題、diff <font color="yellowgreen">2034</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)
- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)
- <a href="https://yukicoder.me/problems/no/2837">No.2837 Flip Triomino</a> (yukicoder contest 440 (2024-08-09) - C問題、diff <font color="yellowgreen">2099</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)
- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="フェルマーの小定理">194. フェルマーの小定理</h2>

### 難易度統計

「フェルマーの小定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1882</font>
- 2024年: ★2.6／diff <font color="blue">1857</font>
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
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)
- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)

　
<h2 id="setprecision・format">195. setprecision・format</h2>

### 難易度統計

「setprecision・format」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1885</font>
- 2024年: ★3.5／diff <font color="red">3143</font>
- 2023年: ★1.5／diff <font color="brown">627</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「setprecision・format」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2516">No.2516 Credit Creation</a> (yukicoder contest 410 (2023-10-27) - B問題、diff <font color="brown">627</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="交代和">196. 交代和</h2>

### 難易度統計

「交代和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1888</font>
- 2024年: ★1.5／diff <font color="deepskyblue">1276</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="orange">2500</font>

### レベル別問題一覧

「交代和」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題、diff <font color="orange">2500</font>)

　
<h2 id="指定序数の値の計算を始切片の数え上げに帰着">197. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#指定序数の値の計算を始切片の数え上げに帰着">指定序数の値の計算を始切片の数え上げに帰着</a></h2>

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

　
<h2 id="商のfloorの種類数による計算量評価">198. 商のfloorの種類数による計算量評価</h2>

### 難易度統計

「商のfloorの種類数による計算量評価」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1891</font>
- 2024年: ★2.5／diff <font color="blue">1891</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「商のfloorの種類数による計算量評価」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)

　
<h2 id="01BFS">199. 01BFS</h2>

### 難易度統計

「01BFS」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1892</font>
- 2024年: ★2.1／diff <font color="blue">1627</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="orange">2690</font>

### レベル別問題一覧

「01BFS」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2759">No.2759 Take Pictures, Elements?</a> (yukicoder contest 430 (2024-05-17) - C問題、diff <font color="deepskyblue">1565</font>)
- <a href="https://yukicoder.me/problems/no/2855">No.2855 Move on Grid</a> (yukicoder contest 442 (2024-08-25) - F問題、diff <font color="deepskyblue">1510</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2096">No.2096 Rage With Our Friends</a> (yukicoder contest 363 (2022-10-07) - E問題、diff <font color="orange">2690</font>)

　
<h2 id="選択回数依存コストナップサック最適化">200. 選択回数依存コストナップサック最適化</h2>

### 難易度統計

「選択回数依存コストナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1900</font>
- 2024年: ★2.5／diff <font color="blue">1900</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「選択回数依存コストナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2701">No.2701 A cans -> B cans</a> (yukicoder contest 424 (2024-03-29) - C問題、diff <font color="blue">1900</font>)

　
<h2 id="周期性">201. 周期性</h2>

### 難易度統計

「周期性」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1902</font>
- 2024年: ★2.5／diff <font color="blue">1913</font>
- 2023年: ★2.5／diff <font color="blue">1849</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2191</font>

### レベル別問題一覧

「周期性」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題、diff <font color="brown">744</font>)
- <a href="https://yukicoder.me/problems/no/2961">No.2961 Shiny Monster Master</a> (yukicoder contest 453 (2024-11-16) - B問題、diff <font color="green">940</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2428">No.2428 Returning Shuffle</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - E問題、diff <font color="deepskyblue">1585</font>)
- <a href="https://yukicoder.me/problems/no/2593">No.2593 Reorder and Mod 120</a> (Advent Calendar Contest 2023 (2023-12-01) - U問題、diff <font color="yellowgreen">2275</font>)
- <a href="https://yukicoder.me/problems/no/2622">No.2622 Dam</a> (yukicoder contest 417 (2024-02-09) - B問題、diff <font color="green">1029</font>)
- <a href="https://yukicoder.me/problems/no/2819">No.2819 Binary Binary-Operator</a> (yukicoder contest 438 (2024-07-26) - A問題、diff <font color="deepskyblue">1596</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2716">No.2716 Falcon Method</a> (yukicoder contest 426 (2024-04-05) - C問題、diff <font color="blue">1809</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題、diff <font color="blue">1933</font>)
- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)
- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2834">No.2834 Work to Play</a> (yukicoder contest 439 (2024-08-02) - H問題、diff <font color="red">3011</font>)
- <a href="https://yukicoder.me/problems/no/2858">No.2858 Make a Palindrome</a> (yukicoder contest 442 (2024-08-25) - I問題、diff <font color="yellowgreen">2147</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="最大・最小要素削除">202. 最大・最小要素削除</h2>

### 難易度統計

「最大・最小要素削除」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1928</font>
- 2024年: ★2.5／diff <font color="blue">1994</font>
- 2023年: ★2.5／diff <font color="blue">1842</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最大・最小要素削除」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2731">No.2731 Two Colors</a> (yukicoder contest 428 (2024-04-19) - D問題、diff <font color="deepskyblue">1442</font>)
- <a href="https://yukicoder.me/problems/no/2804">No.2804 Fixer And Ratism</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - B問題、diff <font color="blue">1779</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2771">No.2771 Personal Space</a> (yukicoder contest 431 (2024-05-31) - G問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="多次元の最適化を１次元の最適化に帰着">203. 多次元の最適化を１次元の最適化に帰着</h2>

### 難易度統計

「多次元の最適化を１次元の最適化に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1944</font>
- 2024年: ★2.5／diff <font color="blue">1944</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「多次元の最適化を１次元の最適化に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)
- <a href="https://yukicoder.me/problems/no/2962">No.2962 Sum Bomb Bomber</a> (yukicoder contest 453 (2024-11-16) - C問題、diff <font color="deepskyblue">1579</font>)

　
<h2 id="２変数決め打ち">204. ２変数決め打ち</h2>

### 難易度統計

「２変数決め打ち」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1944</font>
- 2024年: ★3／diff <font color="orange">2491</font>
- 2023年: ★2.3／diff <font color="blue">1695</font>
- 2022年: ★3.5／diff <font color="orange">2643</font>

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

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)

　
<h2 id="凸最適化">205. 凸最適化</h2>

### 難易度統計

「凸最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1950</font>
- 2024年: ★2.7／diff <font color="blue">1966</font>
- 2023年: ★2.3／diff <font color="blue">1939</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「凸最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2962">No.2962 Sum Bomb Bomber</a> (yukicoder contest 453 (2024-11-16) - C問題、diff <font color="deepskyblue">1579</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2404">No.2404 Vertical Throw Up</a> (yukicoder contest 400 (2023-08-04) - F問題、diff <font color="yellowgreen">2337</font>)
- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

　
<h2 id="優先度付きキュー">206. 優先度付きキュー</h2>

### 難易度統計

「優先度付きキュー」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1964</font>
- 2024年: ★2.5／diff <font color="blue">1890</font>
- 2023年: ★2.6／diff <font color="yellowgreen">2038</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「優先度付きキュー」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2731">No.2731 Two Colors</a> (yukicoder contest 428 (2024-04-19) - D問題、diff <font color="deepskyblue">1442</font>)
- <a href="https://yukicoder.me/problems/no/2740">No.2740 Old Maid</a> (CPCTF 2024 : PPC (2024-04-20) - E問題、diff <font color="deepskyblue">1366</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2453">No.2453 Seat Allocation</a> (yukicoder contest 403 (2023-09-01) - D問題、diff <font color="deepskyblue">1544</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2370">No.2370 He ate many cakes</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2431">No.2431 Viral Hotel</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - H問題、diff <font color="orange">2628</font>)
- <a href="https://yukicoder.me/problems/no/2771">No.2771 Personal Space</a> (yukicoder contest 431 (2024-05-31) - G問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="B進法で全探索">207. B進法で全探索</h2>

### 難易度統計

「B進法で全探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="blue">1983</font>
- 2024年: ★2.5／diff <font color="blue">1977</font>
- 2023年: ★2.5／diff <font color="blue">1989</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「B進法で全探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題、diff <font color="blue">1989</font>)
- <a href="https://yukicoder.me/problems/no/2733">No.2733 Just K-times TSP</a> (yukicoder contest 428 (2024-04-19) - F問題、diff <font color="blue">1977</font>)

　
<h2 id="多点BFS">208. 多点BFS</h2>

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

　
<h2 id="三分探索">209. 三分探索</h2>

### 難易度統計

「三分探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2000</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1579</font>
- 2023年: ★2.5／diff <font color="orange">2421</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「三分探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)
- <a href="https://yukicoder.me/problems/no/2962">No.2962 Sum Bomb Bomber</a> (yukicoder contest 453 (2024-11-16) - C問題、diff <font color="deepskyblue">1579</font>)

　
<h2 id="独立事象の確率を積で計算">210. 独立事象の確率を積で計算</h2>

### 難易度統計

「独立事象の確率を積で計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2031</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2031</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「独立事象の確率を積で計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)

　
<h2 id="１つの桁・成分のみ特定する質問">211. １つの桁・成分のみ特定する質問</h2>

### 難易度統計

「１つの桁・成分のみ特定する質問」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2057</font>
- 2024年: ★2.5／diff <font color="blue">1991</font>
- 2023年: ★2.5／diff <font color="yellowgreen">2323</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「１つの桁・成分のみ特定する質問」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2768">No.2768 Password Crack</a> (yukicoder contest 431 (2024-05-31) - D問題、diff <font color="deepskyblue">1548</font>)
- <a href="https://yukicoder.me/problems/no/2828">No.2828 Remainder Game</a> (yukicoder contest 439 (2024-08-02) - B問題、diff <font color="blue">1696</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)
- <a href="https://yukicoder.me/problems/no/2962">No.2962 Sum Bomb Bomber</a> (yukicoder contest 453 (2024-11-16) - C問題、diff <font color="deepskyblue">1579</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="オイラーグラフ判定">212. オイラーグラフ判定</h2>

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

　
<h2 id="上限・下限値に言及する質問">213. 上限・下限値に言及する質問</h2>

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

　
<h2 id="並列二分探索">214. 並列二分探索</h2>

### 難易度統計

「並列二分探索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="yellowgreen">2162</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2162</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「並列二分探索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2786">No.2786 RMQ on Grid Path</a> (yukicoder contest 433 (2024-06-14) - F問題、diff <font color="yellowgreen">2162</font>)

　
<h2 id="定数倍メモリ削減">215. 定数倍メモリ削減</h2>

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

　
<h2 id="階乗進法">216. 階乗進法</h2>

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

　
<h2 id="個数上限１複数ナップサック最適化">217. 個数上限１複数ナップサック最適化</h2>

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

　
<h2 id="必勝戦略のリアクティブ化">218. 必勝戦略のリアクティブ化</h2>

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

　
<h2 id="全順序集合を状態に持つゲームをP状態とN状態の区間に分割">219. 全順序集合を状態に持つゲームをP状態とN状態の区間に分割</h2>

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

　
<h2 id="ラグランジュ補間">220. ラグランジュ補間</h2>

### 難易度統計

「ラグランジュ補間」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="orange">2525</font>
- 2024年: ★2.5／diff <font color="orange">2525</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ラグランジュ補間」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2830">No.2830 Don't Stop the Game</a> (yukicoder contest 439 (2024-08-02) - D問題、diff <font color="orange">2525</font>)

　
<h2 id="逆行列計算">221. 逆行列計算</h2>

### 難易度統計

「逆行列計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.5／diff <font color="orange">2525</font>
- 2024年: ★2.5／diff <font color="orange">2525</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「逆行列計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2830">No.2830 Don't Stop the Game</a> (yukicoder contest 439 (2024-08-02) - D問題、diff <font color="orange">2525</font>)

　
<h2 id="グリッド上の経路を01列や区間の部分集合に翻訳">222. グリッド上の経路を01列や区間の部分集合に翻訳</h2>

### 難易度統計

「グリッド上の経路を01列や区間の部分集合に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1705</font>
- 2024年: ★2.6／diff <font color="blue">1705</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「グリッド上の経路を01列や区間の部分集合に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="操作逆順">223. 操作逆順</h2>

### 難易度統計

「操作逆順」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1720</font>
- 2024年: ★2.5／diff <font color="blue">1786</font>
- 2023年: ★3／diff <font color="blue">1758</font>
- 2022年: ★2.5／diff <font color="deepskyblue">1486</font>

### レベル別問題一覧

「操作逆順」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2766">No.2766 Delicious Multiply Spice</a> (yukicoder contest 431 (2024-05-31) - B問題、diff <font color="green">1132</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題、diff <font color="deepskyblue">1486</font>)
- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="階乗による二項係数計算">224. 階乗による二項係数計算</h2>

### 難易度統計

「階乗による二項係数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1723</font>
- 2024年: ★2.8／diff <font color="blue">1923</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1444</font>
- 2022年: ★2.2／diff <font color="blue">1641</font>

### レベル別問題一覧

「階乗による二項係数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2636">No.2636 No Waiting in Vain</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)

　
<h2 id="グランディ数計算">225. グランディ数計算</h2>

### 難易度統計

「グランディ数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1745</font>
- 2024年: ★3／diff <font color="yellowgreen">2162</font>
- 2023年: ★2／diff <font color="green">912</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「グランディ数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題、diff <font color="green">912</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)
- <a href="https://yukicoder.me/problems/no/2813">No.2813 Cookie</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - C問題、diff <font color="yellowgreen">2278</font>)

　
<h2 id="最終手番のターン数に注目">226. 最終手番のターン数に注目</h2>

### 難易度統計

「最終手番のターン数に注目」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1755</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1564</font>
- 2023年: ★3／diff <font color="yellowgreen">2153</font>
- 2022年: ★2.5／diff <font color="blue">1934</font>

### レベル別問題一覧

「最終手番のターン数に注目」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2721">No.2721 "Don't say N" Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - A問題、diff <font color="brown">426</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題、diff <font color="blue">1934</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="差分計算">227. 差分計算</h2>

### 難易度統計

「差分計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1767</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2003</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1443</font>
- 2022年: ★3.5／diff <font color="orange">2476</font>

### レベル別問題一覧

「差分計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2306">No.2306 [Cherry 5th Tune C] ウソツキタマシイ</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - B問題、diff <font color="green">812</font>)
- <a href="https://yukicoder.me/problems/no/2548">No.2548 Problem Selection</a> (MMA Contest 017 (2023-11-25) - B問題、diff <font color="gray">343</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)
- <a href="https://yukicoder.me/problems/no/2694">No.2694 The Early Bird Catches The Worm</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - D問題、diff <font color="deepskyblue">1276</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題、diff <font color="blue">1861</font>)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題、diff <font color="deepskyblue">1331</font>)
- <a href="https://yukicoder.me/problems/no/2510">No.2510 Six Cube Sum Counting</a> (yukicoder contest 409 (2023-10-20) - C問題、diff <font color="yellowgreen">2219</font>)
- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2618">No.2618 除霊</a> (yukicoder contest 416 (2024-01-26) - E問題、diff <font color="yellowgreen">2255</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="距離空間の重み付きグラフ化">228. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化">距離空間の重み付きグラフ化</a></h2>

### 難易度統計

「[距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1788</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1570</font>
- 2023年: ★2.6／diff <font color="blue">1933</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2354">No.2354 Poor Sight in Winter</a> (yukicoder contest 393 (2023-06-16) - E問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2695">No.2695 Warp Zone</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - E問題、diff <font color="deepskyblue">1337</font>)
- <a href="https://yukicoder.me/problems/no/2696">No.2696 Sign Creation</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - F問題、diff <font color="blue">1803</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題、diff <font color="yellowgreen">2086</font>)

　
<h2 id="合成による次元削減">229. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#合成による次元削減">合成による次元削減</a></h2>

### 難易度統計

「[合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#合成による次元削減)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1798</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2067</font>
- 2023年: ★2.5／diff <font color="green">1172</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「[合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#合成による次元削減)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2408">No.2408 Lakes and Fish</a> (yukicoder contest 401 (2023-08-11) - B問題、diff <font color="brown">657</font>)
- <a href="https://yukicoder.me/problems/no/2741">No.2741 Balanced Choice</a> (CPCTF 2024 : PPC (2024-04-20) - F問題、diff <font color="deepskyblue">1557</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2486">No.2486 Don't come next to me</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - A問題、diff <font color="brown">712</font>)
- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)
- <a href="https://yukicoder.me/problems/no/2686">No.2686 商品券の使い道</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - H問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)
- <a href="https://yukicoder.me/problems/no/2769">No.2769 Number of Rhombi</a> (yukicoder contest 431 (2024-05-31) - E問題、diff <font color="yellowgreen">2003</font>)
- <a href="https://yukicoder.me/problems/no/2846">No.2846 Birthday Cake</a> (yukicoder contest 441 (2024-08-23) - E問題、diff <font color="yellowgreen">2116</font>)

　
<h2 id="区間代入更新">230. 区間代入更新</h2>

### 難易度統計

「区間代入更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1799</font>
- 2024年: ★2.7／diff <font color="blue">1774</font>
- 2023年: ★2.5／diff <font color="blue">1851</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間代入更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)

　
<h2 id="クエリソート">231. クエリソート</h2>

### 難易度統計

「クエリソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1801</font>
- 2024年: ★2／diff <font color="blue">1659</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="blue">1872</font>

### レベル別問題一覧

「クエリソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)

　
<h2 id="bitごとに計算">232. bitごとに計算</h2>

### 難易度統計

「bitごとに計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1817</font>
- 2024年: ★2／diff <font color="deepskyblue">1450</font>
- 2023年: ★2.6／diff <font color="blue">1618</font>
- 2022年: ★3／diff <font color="yellowgreen">2328</font>

### レベル別問題一覧

「bitごとに計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題、diff <font color="green">1093</font>)
- <a href="https://yukicoder.me/problems/no/2663">No.2663 Zero-Sum Submatrices</a> (yukicoder contest 420 (2024-03-08) - A問題、diff <font color="deepskyblue">1204</font>)
- <a href="https://yukicoder.me/problems/no/2828">No.2828 Remainder Game</a> (yukicoder contest 439 (2024-08-02) - B問題、diff <font color="blue">1696</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題、diff <font color="deepskyblue">1257</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)
- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題、diff <font color="blue">1971</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題、diff <font color="orange">2643</font>)

　
<h2 id="クエリ先読み">233. クエリ先読み</h2>

### 難易度統計

「クエリ先読み」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1820</font>
- 2024年: ★2.3／diff <font color="deepskyblue">1569</font>
- 2023年: ★2.8／diff <font color="yellowgreen">2147</font>
- 2022年: ★2.8／diff <font color="blue">1743</font>

### レベル別問題一覧

「クエリ先読み」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2600">No.2600 Avator Height</a> (yukicoder contest 414 (2024-01-12) - B問題、diff <font color="brown">686</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題、diff <font color="deepskyblue">1486</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="next_permutation">234. next_permutation</h2>

### 難易度統計

「next_permutation」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1833</font>
- 2024年: ★3.2／diff <font color="yellowgreen">2362</font>
- 2023年: ★1.5／diff <font color="brown">775</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「next_permutation」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2732">No.2732 Similar Permutations</a> (yukicoder contest 428 (2024-04-19) - E問題、diff <font color="yellowgreen">2203</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2719">No.2719 Equal Inner Products in Permutation</a> (yukicoder contest 426 (2024-04-05) - F問題、diff <font color="orange">2522</font>)

　
<h2 id="区間和取得">235. 区間和取得</h2>

### 難易度統計

「区間和取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1841</font>
- 2024年: ★2.5／diff <font color="blue">1750</font>
- 2023年: ★2.6／diff <font color="blue">1855</font>
- 2022年: ★3／diff <font color="yellowgreen">2072</font>

### レベル別問題一覧

「区間和取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)
- <a href="https://yukicoder.me/problems/no/2961">No.2961 Shiny Monster Master</a> (yukicoder contest 453 (2024-11-16) - B問題、diff <font color="green">940</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)
- <a href="https://yukicoder.me/problems/no/2694">No.2694 The Early Bird Catches The Worm</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - D問題、diff <font color="deepskyblue">1276</font>)
- <a href="https://yukicoder.me/problems/no/2730">No.2730 Two Types Luggage</a> (yukicoder contest 428 (2024-04-19) - C問題、diff <font color="deepskyblue">1279</font>)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2640">No.2640 traO Stamps</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - D問題、diff <font color="blue">1717</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)
- <a href="https://yukicoder.me/problems/no/2716">No.2716 Falcon Method</a> (yukicoder contest 426 (2024-04-05) - C問題、diff <font color="blue">1809</font>)
- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2625">No.2625 Bouns Ai</a> (yukicoder contest 417 (2024-02-09) - E問題、diff <font color="blue">1654</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)
- <a href="https://yukicoder.me/problems/no/2761">No.2761 Substitute and Search</a> (yukicoder contest 430 (2024-05-17) - E問題、diff <font color="blue">1960</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)
- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="枝刈り">236. 枝刈り</h2>

### 難易度統計

「枝刈り」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1849</font>
- 2024年: ★2.6／diff <font color="blue">1945</font>
- 2023年: ★2.5／diff <font color="blue">1705</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「枝刈り」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題、diff <font color="green">939</font>)
- <a href="https://yukicoder.me/problems/no/2806">No.2806 Cornflake Man</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - D問題、diff <font color="blue">1689</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題、diff <font color="orange">2471</font>)
- <a href="https://yukicoder.me/problems/no/2725">No.2725 Coprime Game 2</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - E問題、diff <font color="blue">1944</font>)
- <a href="https://yukicoder.me/problems/no/2732">No.2732 Similar Permutations</a> (yukicoder contest 428 (2024-04-19) - E問題、diff <font color="yellowgreen">2203</font>)

　
<h2 id="データを不変量別に分割して管理">237. データを不変量別に分割して管理</h2>

### 難易度統計

「データを不変量別に分割して管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1850</font>
- 2024年: ★2.2／diff <font color="blue">1908</font>
- 2023年: ★2.8／diff <font color="blue">1827</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「データを不変量別に分割して管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2563">No.2563 色ごとのグループ</a> (第2回緑以下コンテスト (2023-12-02) - G問題、diff <font color="green">851</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2419">No.2419 MMA文字列2</a> (MMA Contest 016 (2023-08-12) - F問題、diff <font color="green">810</font>)
- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2580">No.2580 Hyperinflation</a> (Advent Calendar Contest 2023 (2023-12-01) - H問題、diff <font color="red">3103</font>)

　
<h2 id="最大公約数計算">238. 最大公約数計算</h2>

### 難易度統計

「最大公約数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1861</font>
- 2024年: ★2.3／diff <font color="deepskyblue">1552</font>
- 2023年: ★2.6／diff <font color="blue">1771</font>
- 2022年: ★3.1／diff <font color="yellowgreen">2316</font>

### レベル別問題一覧

「最大公約数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2811">No.2811 Calculation Within Sequence</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - A問題、diff <font color="deepskyblue">1260</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)
- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)
- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題、diff <font color="yellowgreen">2139</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2725">No.2725 Coprime Game 2</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - E問題、diff <font color="blue">1944</font>)
- <a href="https://yukicoder.me/problems/no/2821">No.2821 A[i] ← 2A[j] - A[i]</a> (yukicoder contest 438 (2024-07-26) - C問題、diff <font color="blue">1905</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="フェルマーの小定理による逆元計算">239. フェルマーの小定理による逆元計算</h2>

### 難易度統計

「フェルマーの小定理による逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1921</font>
- 2024年: ★2.6／diff <font color="blue">1857</font>
- 2023年: ★2.6／diff <font color="blue">1876</font>
- 2022年: ★3／diff <font color="orange">2430</font>

### レベル別問題一覧

「フェルマーの小定理による逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)
- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)

　
<h2 id="素数を法とする逆元計算">240. 素数を法とする逆元計算</h2>

### 難易度統計

「素数を法とする逆元計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1928</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2012</font>
- 2023年: ★2.6／diff <font color="blue">1805</font>
- 2022年: ★2.5／diff <font color="blue">1964</font>

### レベル別問題一覧

「素数を法とする逆元計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2679">No.2679 MODice</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - A問題、diff <font color="brown">721</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2351">No.2351 Butterfly in Summer</a> (yukicoder contest 393 (2023-06-16) - B問題、diff <font color="brown">777</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)
- <a href="https://yukicoder.me/problems/no/2636">No.2636 No Waiting in Vain</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)
- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)
- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2685">No.2685 Cell Proliferation (Easy)</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - G問題、diff <font color="blue">1983</font>)
- <a href="https://yukicoder.me/problems/no/2830">No.2830 Don't Stop the Game</a> (yukicoder contest 439 (2024-08-02) - D問題、diff <font color="orange">2525</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)
- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

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
- <a href="https://yukicoder.me/problems/no/2631">No.2631 Rectangle Grid Game</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - D問題、diff <font color="yellowgreen">2176</font>)
- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)
- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)
- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)
- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="逆元の再帰計算">241. 逆元の再帰計算</h2>

### 難易度統計

「逆元の再帰計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1931</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2043</font>
- 2023年: ★2.5／diff <font color="blue">1733</font>
- 2022年: ★2.5／diff <font color="blue">1871</font>

### レベル別問題一覧

「逆元の再帰計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2679">No.2679 MODice</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - A問題、diff <font color="brown">721</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題、diff <font color="deepskyblue">1356</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2636">No.2636 No Waiting in Vain</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)
- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)
- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2685">No.2685 Cell Proliferation (Easy)</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - G問題、diff <font color="blue">1983</font>)
- <a href="https://yukicoder.me/problems/no/2830">No.2830 Don't Stop the Game</a> (yukicoder contest 439 (2024-08-02) - D問題、diff <font color="orange">2525</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題、diff <font color="yellowgreen">2327</font>)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2631">No.2631 Rectangle Grid Game</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - D問題、diff <font color="yellowgreen">2176</font>)
- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)
- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)
- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="素数を用いた構築">242. 素数を用いた構築</h2>

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

　
<h2 id="転倒数計算">243. 転倒数計算</h2>

### 難易度統計

「転倒数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1943</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1540</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2145</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「転倒数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)

　
<h2 id="端から確定">244. 端から確定</h2>

### 難易度統計

「端から確定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1944</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2115</font>
- 2023年: ★2.5／diff <font color="blue">1783</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2008</font>

### レベル別問題一覧

「端から確定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2629">No.2629 A replace B replace C</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - B問題、diff <font color="green">1124</font>)
- <a href="https://yukicoder.me/problems/no/2806">No.2806 Cornflake Man</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - D問題、diff <font color="blue">1689</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2210">No.2210 equence Squence Seuence</a> (yukicoder contest 376 (2023-02-10) - C問題、diff <font color="deepskyblue">1489</font>)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2353">No.2353 Guardian Dogs in Spring</a> (yukicoder contest 393 (2023-06-16) - D問題、diff <font color="blue">1670</font>)
- <a href="https://yukicoder.me/problems/no/2518">No.2518 Adjacent Larger</a> (yukicoder contest 410 (2023-10-27) - D問題、diff <font color="deepskyblue">1488</font>)
- <a href="https://yukicoder.me/problems/no/2551">No.2551 2, 3, 5, 7 Game</a> (MMA Contest 017 (2023-11-25) - E問題、diff <font color="orange">2501</font>)
- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)
- <a href="https://yukicoder.me/problems/no/2591">No.2591 安上がりな括弧列</a> (Advent Calendar Contest 2023 (2023-12-01) - S問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2700">No.2700 Please Hack Greedy Solution!</a> (yukicoder contest 424 (2024-03-29) - B問題、diff <font color="yellowgreen">2030</font>)
- <a href="https://yukicoder.me/problems/no/2745">No.2745 String Swap Battle</a> (CPCTF 2024 : PPC (2024-04-20) - J問題、diff <font color="yellowgreen">2309</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)
- <a href="https://yukicoder.me/problems/no/2643">No.2643 Many Range Sums Problems</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - G問題、diff <font color="orange">2765</font>)
- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)
- <a href="https://yukicoder.me/problems/no/2838">No.2838 Diagonals</a> (yukicoder contest 440 (2024-08-09) - D問題、diff <font color="yellowgreen">2305</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="繰り返し二乗法">245. 繰り返し二乗法</h2>

### 難易度統計

「繰り返し二乗法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1954</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2062</font>
- 2023年: ★2.5／diff <font color="blue">1898</font>
- 2022年: ★2.7／diff <font color="blue">1946</font>

### レベル別問題一覧

「繰り返し二乗法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題、diff <font color="green">1139</font>)
- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)

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
- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)
- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)
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
- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)
- <a href="https://yukicoder.me/problems/no/2653">No.2653 [Cherry 6th Tune] Re: start! (Make it Zero!)</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - G問題、diff <font color="yellowgreen">2247</font>)
- <a href="https://yukicoder.me/problems/no/2734">No.2734 Addition and Multiplication in yukicoder (Hard)</a> (yukicoder contest 428 (2024-04-19) - G問題、diff <font color="yellowgreen">2034</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)
- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)
- <a href="https://yukicoder.me/problems/no/2837">No.2837 Flip Triomino</a> (yukicoder contest 440 (2024-08-09) - C問題、diff <font color="yellowgreen">2099</font>)
- <a href="https://yukicoder.me/problems/no/2965">No.2965 Don't Stop the Game again</a> (yukicoder contest 453 (2024-11-16) - F問題、diff <font color="orange">2613</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="実験">246. 実験</h2>

### 難易度統計

「実験」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1957</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2227</font>
- 2023年: ★2.3／diff <font color="deepskyblue">1250</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2191</font>

### レベル別問題一覧

「実験」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2216">No.2216 Pa1indr0me</a> (yukicoder contest 377 (2023-02-17) - A問題、diff <font color="gray">344</font>)
- <a href="https://yukicoder.me/problems/no/2393">No.2393 Bit Grid Connected Component</a> (yukicoder contest 399 (2023-07-28) - B問題、diff <font color="green">1050</font>)
- <a href="https://yukicoder.me/problems/no/2819">No.2819 Binary Binary-Operator</a> (yukicoder contest 438 (2024-07-26) - A問題、diff <font color="deepskyblue">1596</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2742">No.2742 Car Flow</a> (CPCTF 2024 : PPC (2024-04-20) - G問題、diff <font color="blue">1969</font>)
- <a href="https://yukicoder.me/problems/no/2797">No.2797 Square Tile</a> (yukicoder contest 435 (2024-06-28) - C問題、diff <font color="yellowgreen">2328</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2521">No.2521 Don't be Same</a> (yukicoder contest 410 (2023-10-27) - G問題、diff <font color="yellowgreen">2357</font>)
- <a href="https://yukicoder.me/problems/no/2631">No.2631 Rectangle Grid Game</a> (traP 作問ハッカソンコンテスト 002(day1) (2024-02-16) - D問題、diff <font color="yellowgreen">2176</font>)
- <a href="https://yukicoder.me/problems/no/2813">No.2813 Cookie</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - C問題、diff <font color="yellowgreen">2278</font>)
- <a href="https://yukicoder.me/problems/no/2815">No.2815 Smaller than all</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - E問題、diff <font color="orange">2723</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2719">No.2719 Equal Inner Products in Permutation</a> (yukicoder contest 426 (2024-04-05) - F問題、diff <font color="orange">2522</font>)

　
<h2 id="bitDP">247. bitDP</h2>

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

　
<h2 id="帰属区間取得">248. 帰属区間取得</h2>

### 難易度統計

「帰属区間取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="blue">1987</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2158</font>
- 2023年: ★2.6／diff <font color="yellowgreen">2042</font>
- 2022年: ★2.5／diff <font color="blue">1649</font>

### レベル別問題一覧

「帰属区間取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)

　
<h2 id="ニム和">249. ニム和</h2>

### 難易度統計

「ニム和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2014</font>
- 2024年: ★3／diff <font color="yellowgreen">2224</font>
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
- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)
- <a href="https://yukicoder.me/problems/no/2813">No.2813 Cookie</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - C問題、diff <font color="yellowgreen">2278</font>)

　
<h2 id="始点と終点からの最短経路長計算">250. 始点と終点からの最短経路長計算</h2>

### 難易度統計

「始点と終点からの最短経路長計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2047</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2037</font>
- 2023年: ★3／diff <font color="yellowgreen">2068</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「始点と終点からの最短経路長計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2805">No.2805 Go to School</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - C問題、diff <font color="blue">1720</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)
- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

　
<h2 id="左右から走査">251. 左右から走査</h2>

### 難易度統計

「左右から走査」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2174</font>
- 2024年: ★2.7／diff <font color="orange">2447</font>
- 2023年: ★2.5／diff <font color="blue">1628</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「左右から走査」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題、diff <font color="blue">1628</font>)
- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="アルゴリズムのリアクティブ化">252. アルゴリズムのリアクティブ化</h2>

### 難易度統計

「アルゴリズムのリアクティブ化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2211</font>
- 2024年: ★2.8／diff <font color="orange">2465</font>
- 2023年: ★2.5／diff <font color="yellowgreen">2323</font>
- 2022年: ★2.2／diff <font color="blue">1648</font>

### レベル別問題一覧

「アルゴリズムのリアクティブ化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2124">No.2124 Guess the Permutation</a> (yukicoder contest 368 (2022-11-18) - A問題、diff <font color="green">1158</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2577">No.2577 Simple Permutation Guess</a> (Advent Calendar Contest 2023 (2023-12-01) - E問題、diff <font color="yellowgreen">2323</font>)
- <a href="https://yukicoder.me/problems/no/2830">No.2830 Don't Stop the Game</a> (yukicoder contest 439 (2024-08-02) - D問題、diff <font color="orange">2525</font>)
- <a href="https://yukicoder.me/problems/no/2962">No.2962 Sum Bomb Bomber</a> (yukicoder contest 453 (2024-11-16) - C問題、diff <font color="deepskyblue">1579</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題、diff <font color="yellowgreen">2139</font>)
- <a href="https://yukicoder.me/problems/no/2965">No.2965 Don't Stop the Game again</a> (yukicoder contest 453 (2024-11-16) - F問題、diff <font color="orange">2613</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="変数の対称性">253. 変数の対称性</h2>

### 難易度統計

「変数の対称性」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2231</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2328</font>
- 2023年: ★2.5／diff <font color="yellowgreen">2133</font>
- 2022年: ★3／diff <font color="orange">2430</font>

### レベル別問題一覧

「変数の対称性」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2358">No.2358 xy+yz+zx=N</a> (yukicoder contest 394 (2023-06-23) - B問題、diff <font color="deepskyblue">1397</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2585">No.2585 How many "Who is Santa?"</a> (Advent Calendar Contest 2023 (2023-12-01) - M問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2797">No.2797 Square Tile</a> (yukicoder contest 435 (2024-06-28) - C問題、diff <font color="yellowgreen">2328</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)

　
<h2 id="円周角の定理">254. 円周角の定理</h2>

### 難易度統計

「円周角の定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.6／diff <font color="yellowgreen">2258</font>
- 2024年: ★3.2／diff <font color="orange">2781</font>
- 2023年: ★2／diff <font color="deepskyblue">1212</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「円周角の定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2469">No.2469 Umbrella Queries</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - C問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2517">No.2517 Right Triangles on Circle</a> (yukicoder contest 410 (2023-10-27) - C問題、diff <font color="deepskyblue">1212</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="最長単調増加部分列長計算">255. 最長単調増加部分列長計算</h2>

### 難易度統計

「最長単調増加部分列長計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1650</font>
- 2024年: ★3／diff <font color="yellowgreen">2100</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1200</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最長単調増加部分列長計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)

　
<h2 id="鳩の巣原理">256. 鳩の巣原理</h2>

### 難易度統計

「鳩の巣原理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1809</font>
- 2024年: ★2.7／diff <font color="blue">1809</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「鳩の巣原理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2672">No.2672 Subset Xor Sum</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - B問題、diff <font color="deepskyblue">1416</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2732">No.2732 Similar Permutations</a> (yukicoder contest 428 (2024-04-19) - E問題、diff <font color="yellowgreen">2203</font>)

　
<h2 id="終点からの最短経路長計算">257. 終点からの最短経路長計算</h2>

### 難易度統計

「終点からの最短経路長計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1888</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2063</font>
- 2023年: ★2.6／diff <font color="blue">1757</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「終点からの最短経路長計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2565">No.2565 はじめてのおつかい</a> (第2回緑以下コンテスト (2023-12-02) - I問題、diff <font color="green">972</font>)
- <a href="https://yukicoder.me/problems/no/2805">No.2805 Go to School</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - C問題、diff <font color="blue">1720</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2569">No.2569 はじめてのおつかいHard</a> (緑以下コンテスト  Extra (2023-12-02) - A問題、diff <font color="deepskyblue">1385</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)
- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

　
<h2 id="表示可能性DP">258. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP">表示可能性DP</a></h2>

### 難易度統計

「[表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1894</font>
- 2024年: ★3／diff <font color="yellowgreen">2094</font>
- 2023年: ★2／diff <font color="deepskyblue">1352</font>
- 2022年: ★2.5／diff <font color="blue">1641</font>

### レベル別問題一覧

「[表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2364">No.2364 Knapsack Problem</a> (yukicoder contest 395 (2023-06-30) - A問題、diff <font color="deepskyblue">1352</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題、diff <font color="blue">1641</font>)
- <a href="https://yukicoder.me/problems/no/2672">No.2672 Subset Xor Sum</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - B問題、diff <font color="deepskyblue">1416</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)
- <a href="https://yukicoder.me/problems/no/2846">No.2846 Birthday Cake</a> (yukicoder contest 441 (2024-08-23) - E問題、diff <font color="yellowgreen">2116</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="部分回文列挙">259. 部分回文列挙</h2>

### 難易度統計

「部分回文列挙」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1904</font>
- 2024年: ★3／diff <font color="yellowgreen">2147</font>
- 2023年: ★2.5／diff <font color="blue">1661</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「部分回文列挙」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題、diff <font color="blue">1661</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2858">No.2858 Make a Palindrome</a> (yukicoder contest 442 (2024-08-25) - I問題、diff <font color="yellowgreen">2147</font>)

　
<h2 id="二項係数計算">260. 二項係数計算</h2>

### 難易度統計

「二項係数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1908</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2060</font>
- 2023年: ★2.8／diff <font color="blue">1775</font>
- 2022年: ★2.2／diff <font color="blue">1641</font>

### レベル別問題一覧

「二項係数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題、diff <font color="deepskyblue">1275</font>)
- <a href="https://yukicoder.me/problems/no/2527">No.2527 H and W</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - C問題、diff <font color="green">1063</font>)
- <a href="https://yukicoder.me/problems/no/2636">No.2636 No Waiting in Vain</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2409">No.2409 Strange Werewolves</a> (yukicoder contest 401 (2023-08-11) - C問題、diff <font color="green">996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2511">No.2511 Mountain Sequence</a> (yukicoder contest 409 (2023-10-20) - D問題、diff <font color="yellowgreen">2273</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2802">No.2802 Pill Bug in Grid Maze</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2814">No.2814 Block Game</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - D問題、diff <font color="orange">2676</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2344">No.2344 (l+r)^2</a> (yukicoder contest 392 (2023-06-09) - B問題、diff <font color="orange">2768</font>)

　
<h2 id="場合分けによるmax・min・絶対値計算">261. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#場合分けによるmax・min・絶対値計算">場合分けによるmax・min・絶対値計算</a></h2>

### 難易度統計

「[場合分けによるmax・min・絶対値計算](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#場合分けによるmax・min・絶対値計算)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1914</font>
- 2024年: ★3.5／diff <font color="yellowgreen">2117</font>
- 2023年: ★2／diff <font color="deepskyblue">1416</font>
- 2022年: ★3.5／diff <font color="orange">2707</font>

### レベル別問題一覧

「[場合分けによるmax・min・絶対値計算](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#場合分けによるmax・min・絶対値計算)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題、diff <font color="green">1060</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題、diff <font color="blue">1773</font>)
- <a href="https://yukicoder.me/problems/no/2662">No.2662 Installing Cell Towers</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

　
<h2 id="区間スケジューリング">262. 区間スケジューリング</h2>

### 難易度統計

「区間スケジューリング」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1916</font>
- 2024年: ★2.5／diff <font color="blue">1848</font>
- 2023年: ★3／diff <font color="blue">1985</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間スケジューリング」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2796">No.2796 Small Matryoshka</a> (yukicoder contest 435 (2024-06-28) - B問題、diff <font color="blue">1848</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)

　
<h2 id="商による付値計算">263. 商による付値計算</h2>

### 難易度統計

「商による付値計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1927</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="blue">1927</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「商による付値計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題、diff <font color="blue">1838</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)

　
<h2 id="動的計画法">264. 動的計画法</h2>

### 難易度統計

「動的計画法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1942</font>
- 2024年: ★2.5／diff <font color="blue">1828</font>
- 2023年: ★2.7／diff <font color="blue">1928</font>
- 2022年: ★2.8／diff <font color="yellowgreen">2101</font>

### レベル別問題一覧

「動的計画法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2373">No.2373 wa, wo, n</a> (yukicoder contest 396 (Asakatsu Presents 2) (2023-07-07) - C問題、diff <font color="green">1182</font>)
- <a href="https://yukicoder.me/problems/no/2693">No.2693 Sword</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - C問題、diff <font color="deepskyblue">1211</font>)
- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)

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
- <a href="https://yukicoder.me/problems/no/2639">No.2639 Longest Increasing Walk</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - C問題、diff <font color="deepskyblue">1591</font>)
- <a href="https://yukicoder.me/problems/no/2711">No.2711 Connecting Lights</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - F問題、diff <font color="deepskyblue">1396</font>)
- <a href="https://yukicoder.me/problems/no/2741">No.2741 Balanced Choice</a> (CPCTF 2024 : PPC (2024-04-20) - F問題、diff <font color="deepskyblue">1557</font>)
- <a href="https://yukicoder.me/problems/no/2759">No.2759 Take Pictures, Elements?</a> (yukicoder contest 430 (2024-05-17) - C問題、diff <font color="deepskyblue">1565</font>)
- <a href="https://yukicoder.me/problems/no/2783">No.2783 4-33 Easy</a> (yukicoder contest 433 (2024-06-14) - C問題、diff <font color="blue">1705</font>)
- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)
- <a href="https://yukicoder.me/problems/no/2820">No.2820 Non-Preferred IUPAC Nomenclature</a> (yukicoder contest 438 (2024-07-26) - B問題、diff <font color="blue">1807</font>)
- <a href="https://yukicoder.me/problems/no/2854">No.2854 -1 Subsequence</a> (yukicoder contest 442 (2024-08-25) - E問題、diff <font color="green">1165</font>)

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
- <a href="https://yukicoder.me/problems/no/2656">No.2656 XOR Slimes</a> (yukicoder contest 419 (2024-03-01) - B問題、diff <font color="blue">1726</font>)
- <a href="https://yukicoder.me/problems/no/2672">No.2672 Subset Xor Sum</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - B問題、diff <font color="deepskyblue">1416</font>)
- <a href="https://yukicoder.me/problems/no/2673">No.2673 A present from B</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - C問題、diff <font color="blue">1806</font>)
- <a href="https://yukicoder.me/problems/no/2685">No.2685 Cell Proliferation (Easy)</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - G問題、diff <font color="blue">1983</font>)
- <a href="https://yukicoder.me/problems/no/2701">No.2701 A cans -> B cans</a> (yukicoder contest 424 (2024-03-29) - C問題、diff <font color="blue">1900</font>)
- <a href="https://yukicoder.me/problems/no/2733">No.2733 Just K-times TSP</a> (yukicoder contest 428 (2024-04-19) - F問題、diff <font color="blue">1977</font>)
- <a href="https://yukicoder.me/problems/no/2807">No.2807 Have Another Go (Easy)</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - E問題、diff <font color="yellowgreen">2004</font>)
- <a href="https://yukicoder.me/problems/no/2955">No.2955 Pizza Delivery Plan</a> (yukicoder contest 452 (2024-11-08) - C問題、diff <font color="blue">1728</font>)
- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

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
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)
- <a href="https://yukicoder.me/problems/no/2772">No.2772 Appearing Even Times</a> (yukicoder contest 431 (2024-05-31) - H問題、diff <font color="blue">1925</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)
- <a href="https://yukicoder.me/problems/no/2839">No.2839 AND Constraint</a> (yukicoder contest 440 (2024-08-09) - E問題、diff <font color="orange">2648</font>)
- <a href="https://yukicoder.me/problems/no/2846">No.2846 Birthday Cake</a> (yukicoder contest 441 (2024-08-23) - E問題、diff <font color="yellowgreen">2116</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題、diff <font color="orange">2737</font>)
- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)
- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)
- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)
- <a href="https://yukicoder.me/problems/no/2584">No.2584 The University of Tree</a> (Advent Calendar Contest 2023 (2023-12-01) - L問題、diff <font color="red">2960</font>)
- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)
- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2159">No.2159 Filling 4x4 array</a> (Advent Calendar Contest 2022 (2022-12-01) - J問題、diff <font color="darkgoldenrod ">3382</font>)
- <a href="https://yukicoder.me/problems/no/2580">No.2580 Hyperinflation</a> (Advent Calendar Contest 2023 (2023-12-01) - H問題、diff <font color="red">3103</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)
- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="２進法">265. ２進法</h2>

### 難易度統計

「２進法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1954</font>
- 2024年: ★2.1／diff <font color="deepskyblue">1529</font>
- 2023年: ★3／diff <font color="yellowgreen">2175</font>
- 2022年: ★3.6／diff <font color="orange">2536</font>

### レベル別問題一覧

「２進法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2708">No.2708 Jewel holder</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - C問題、diff <font color="brown">736</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2663">No.2663 Zero-Sum Submatrices</a> (yukicoder contest 420 (2024-03-08) - A問題、diff <font color="deepskyblue">1204</font>)
- <a href="https://yukicoder.me/problems/no/2711">No.2711 Connecting Lights</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - F問題、diff <font color="deepskyblue">1396</font>)
- <a href="https://yukicoder.me/problems/no/2828">No.2828 Remainder Game</a> (yukicoder contest 439 (2024-08-02) - B問題、diff <font color="blue">1696</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2609">No.2609 Decreasing GCDs</a> (yukicoder contest 415 (2024-01-19) - C問題、diff <font color="deepskyblue">1531</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題、diff <font color="yellowgreen">2175</font>)
- <a href="https://yukicoder.me/problems/no/2965">No.2965 Don't Stop the Game again</a> (yukicoder contest 453 (2024-11-16) - F問題、diff <font color="orange">2613</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)

　
<h2 id="ユークリッドの互除法">266. ユークリッドの互除法</h2>

### 難易度統計

「ユークリッドの互除法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="blue">1954</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1546</font>
- 2023年: ★3.2／diff <font color="yellowgreen">2204</font>
- 2022年: ★3.1／diff <font color="yellowgreen">2316</font>

### レベル別問題一覧

「ユークリッドの互除法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2811">No.2811 Calculation Within Sequence</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - A問題、diff <font color="deepskyblue">1260</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2526">No.2526 Kth Not-divisible Number</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - B問題、diff <font color="deepskyblue">1205</font>)
- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)
- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)
- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2104">No.2104 Multiply-Add</a> (yukicoder contest 365 (2022-10-21) - B問題、diff <font color="yellowgreen">2139</font>)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題、diff <font color="orange">2430</font>)
- <a href="https://yukicoder.me/problems/no/2355">No.2355 Unhappy Back Dance</a> (yukicoder contest 393 (2023-06-16) - F問題、diff <font color="blue">1919</font>)
- <a href="https://yukicoder.me/problems/no/2432">No.2432 Flip and Move</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - I問題、diff <font color="yellowgreen">2191</font>)
- <a href="https://yukicoder.me/problems/no/2725">No.2725 Coprime Game 2</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - E問題、diff <font color="blue">1944</font>)
- <a href="https://yukicoder.me/problems/no/2821">No.2821 A[i] ← 2A[j] - A[i]</a> (yukicoder contest 438 (2024-07-26) - C問題、diff <font color="blue">1905</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="倍数ゼータ変換">267. 倍数ゼータ変換</h2>

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

　
<h2 id="付値計算">268. 付値計算</h2>

### 難易度統計

「付値計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2006</font>
- 2024年: ★2.5／diff <font color="blue">1840</font>
- 2023年: ★2.8／diff <font color="yellowgreen">2068</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「付値計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題、diff <font color="blue">1605</font>)
- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題、diff <font color="blue">1838</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="区間和の指定された区間数え上げ">269. 区間和の指定された区間数え上げ</h2>

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

　
<h2 id="不変量を保つ戦略">270. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略">不変量を保つ戦略</a></h2>

### 難易度統計

「[不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2013</font>
- 2024年: ★3／diff <font color="yellowgreen">2197</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="blue">1828</font>

### レベル別問題一覧

「[不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)
- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)
- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)

　
<h2 id="単調列数え上げ">271. 単調列数え上げ</h2>

### 難易度統計

「単調列数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2020</font>
- 2024年: ★2／diff <font color="deepskyblue">1221</font>
- 2023年: ★3.2／diff <font color="orange">2407</font>
- 2022年: ★2.5／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「単調列数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)

　
<h2 id="ナップサック分割統治">272. ナップサック分割統治</h2>

### 難易度統計

「ナップサック分割統治」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2031</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2031</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ナップサック分割統治」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2741">No.2741 Balanced Choice</a> (CPCTF 2024 : PPC (2024-04-20) - F問題、diff <font color="deepskyblue">1557</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2686">No.2686 商品券の使い道</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - H問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)
- <a href="https://yukicoder.me/problems/no/2846">No.2846 Birthday Cake</a> (yukicoder contest 441 (2024-08-23) - E問題、diff <font color="yellowgreen">2116</font>)

　
<h2 id="imos法">273. imos法</h2>

### 難易度統計

「imos法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2034</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2245</font>
- 2023年: ★2.9／diff <font color="yellowgreen">2008</font>
- 2022年: ★2.5／diff <font color="blue">1680</font>

### レベル別問題一覧

「imos法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2154">No.2154 あさかつの参加人数</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - B問題、diff <font color="brown">711</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)
- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)
- <a href="https://yukicoder.me/problems/no/2662">No.2662 Installing Cell Towers</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2796">No.2796 Small Matryoshka</a> (yukicoder contest 435 (2024-06-28) - B問題、diff <font color="blue">1848</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)
- <a href="https://yukicoder.me/problems/no/2603">No.2603 Tone Correction</a> (yukicoder contest 414 (2024-01-12) - E問題、diff <font color="orange">2536</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

　
<h2 id="再帰的構築">274. 再帰的構築</h2>

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

　
<h2 id="区間要素数取得">275. 区間要素数取得</h2>

### 難易度統計

「区間要素数取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2063</font>
- 2024年: ★2.5／diff <font color="blue">1777</font>
- 2023年: ★2.5／diff <font color="orange">2401</font>
- 2022年: ★3.1／diff <font color="yellowgreen">2332</font>

### レベル別問題一覧

「区間要素数取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)

　
<h2 id="描画可能性を実際に描画して判定">276. 描画可能性を実際に描画して判定</h2>

### 難易度統計

「描画可能性を実際に描画して判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2078</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2158</font>
- 2023年: ★3／diff <font color="blue">1998</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「描画可能性を実際に描画して判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2456">No.2456 Stamp Art</a> (yukicoder contest 403 (2023-09-01) - G問題、diff <font color="blue">1998</font>)

　
<h2 id="倍数走査によるオイラー関数前計算">277. 倍数走査によるオイラー関数前計算</h2>

### 難易度統計

「倍数走査によるオイラー関数前計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2109</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2109</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「倍数走査によるオイラー関数前計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2552">No.2552 Not Coprime, Not Divisor</a> (MMA Contest 017 (2023-11-25) - F問題、diff <font color="yellowgreen">2235</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題、diff <font color="blue">1983</font>)

　
<h2 id="再帰">278. 再帰</h2>

### 難易度統計

「再帰」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2121</font>
- 2024年: ★2.6／diff <font color="yellowgreen">2158</font>
- 2023年: ★2.9／diff <font color="blue">1913</font>
- 2022年: ★3／diff <font color="orange">2491</font>

### レベル別問題一覧

「再帰」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2561">No.2561 みんな大好きmod 998</a> (第2回緑以下コンテスト (2023-12-02) - E問題、diff <font color="brown">775</font>)
- <a href="https://yukicoder.me/problems/no/2766">No.2766 Delicious Multiply Spice</a> (yukicoder contest 431 (2024-05-31) - B問題、diff <font color="green">1132</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2820">No.2820 Non-Preferred IUPAC Nomenclature</a> (yukicoder contest 438 (2024-07-26) - B問題、diff <font color="blue">1807</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題、diff <font color="yellowgreen">2246</font>)
- <a href="https://yukicoder.me/problems/no/2518">No.2518 Adjacent Larger</a> (yukicoder contest 410 (2023-10-27) - D問題、diff <font color="deepskyblue">1488</font>)
- <a href="https://yukicoder.me/problems/no/2610">No.2610 Decreasing LCMs</a> (yukicoder contest 415 (2024-01-19) - D問題、diff <font color="yellowgreen">2129</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題、diff <font color="blue">1971</font>)
- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題、diff <font color="yellowgreen">2016</font>)
- <a href="https://yukicoder.me/problems/no/2602">No.2602 Real Collider</a> (yukicoder contest 414 (2024-01-12) - D問題、diff <font color="orange">2419</font>)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)
- <a href="https://yukicoder.me/problems/no/2813">No.2813 Cookie</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - C問題、diff <font color="yellowgreen">2278</font>)
- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)
- <a href="https://yukicoder.me/problems/no/2839">No.2839 AND Constraint</a> (yukicoder contest 440 (2024-08-09) - E問題、diff <font color="orange">2648</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題、diff <font color="orange">2737</font>)
- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2595">No.2595 Parsing Challenge</a> (Advent Calendar Contest 2023 (2023-12-01) - W問題、diff <font color="darkgoldenrod ">3316</font>)

　
<h2 id="クラスカル法">279. クラスカル法</h2>

### 難易度統計

「クラスカル法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2146</font>
- 2024年: ★3／diff <font color="yellowgreen">2249</font>
- 2023年: ★2.5／diff <font color="yellowgreen">2044</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「クラスカル法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2642">No.2642 Don't cut line!</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - F問題、diff <font color="yellowgreen">2249</font>)

　
<h2 id="最小全域木計算">280. 最小全域木計算</h2>

### 難易度統計

「最小全域木計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2146</font>
- 2024年: ★3／diff <font color="yellowgreen">2249</font>
- 2023年: ★2.5／diff <font color="yellowgreen">2044</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最小全域木計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2642">No.2642 Don't cut line!</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - F問題、diff <font color="yellowgreen">2249</font>)

　
<h2 id="木DP">281. 木DP</h2>

### 難易度統計

「木DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2149</font>
- 2024年: ★2／diff <font color="blue">1807</font>
- 2023年: ★2.8／diff <font color="yellowgreen">2234</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「木DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2820">No.2820 Non-Preferred IUPAC Nomenclature</a> (yukicoder contest 438 (2024-07-26) - B問題、diff <font color="blue">1807</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2205">No.2205 Lights Out on Christmas Tree</a> (yukicoder contest 375 (2023-02-03) - E問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2532">No.2532 Want Play More</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - H問題、diff <font color="blue">1996</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2360">No.2360 Path to Integer</a> (yukicoder contest 394 (2023-06-23) - D問題、diff <font color="yellowgreen">2322</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2584">No.2584 The University of Tree</a> (Advent Calendar Contest 2023 (2023-12-01) - L問題、diff <font color="red">2960</font>)

　
<h2 id="三平方の定理">282. 三平方の定理</h2>

### 難易度統計

「三平方の定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2175</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2175</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「三平方の定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2953">No.2953 Maximum Right Triangle</a> (yukicoder contest 452 (2024-11-08) - A問題、diff <font color="deepskyblue">1208</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2831">No.2831 Cos Bomb Crasher</a> (yukicoder contest 439 (2024-08-02) - E問題、diff <font color="red">3143</font>)

　
<h2 id="半分全列挙">283. 半分全列挙</h2>

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

　
<h2 id="エラトステネスの篩による約数列挙前計算">284. エラトステネスの篩による約数列挙前計算</h2>

### 難易度統計

「エラトステネスの篩による約数列挙前計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2263</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1509</font>
- 2023年: ★3／diff <font color="red">3018</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「エラトステネスの篩による約数列挙前計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

　
<h2 id="頂点の纏め上げによる次元削減">285. 頂点の纏め上げによる次元削減</h2>

### 難易度統計

「頂点の纏め上げによる次元削減」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2351</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2351</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「頂点の纏め上げによる次元削減」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)

　
<h2 id="隣接行列による遷移計算">286. 隣接行列による遷移計算</h2>

### 難易度統計

「隣接行列による遷移計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.7／diff <font color="yellowgreen">2351</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2351</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「隣接行列による遷移計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)

　
<h2 id="閉路検出">287. 閉路検出</h2>

### 難易度統計

「閉路検出」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1733</font>
- 2024年: ★2.5／diff <font color="blue">1749</font>
- 2023年: ★3／diff <font color="blue">1725</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「閉路検出」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2712">No.2712 Play more!</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - G問題、diff <font color="blue">1749</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2301">No.2301 Namorientation</a> (yukicoder contest 388 (2023-05-12) - E問題、diff <font color="deepskyblue">1499</font>)
- <a href="https://yukicoder.me/problems/no/2531">No.2531 Coloring Vertices on Namori</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - G問題、diff <font color="blue">1951</font>)

　
<h2 id="イベントソート">288. イベントソート</h2>

### 難易度統計

「イベントソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1882</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1448</font>
- 2023年: ★2.8／diff <font color="blue">1971</font>
- 2022年: ★3／diff <font color="yellowgreen">2049</font>

### レベル別問題一覧

「イベントソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)
- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2431">No.2431 Viral Hotel</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - H問題、diff <font color="orange">2628</font>)

　
<h2 id="サンプルから推測">289. サンプルから推測</h2>

### 難易度統計

「サンプルから推測」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1896</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2263</font>
- 2023年: ★2.7／diff <font color="deepskyblue">1346</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「サンプルから推測」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2216">No.2216 Pa1indr0me</a> (yukicoder contest 377 (2023-02-17) - A問題、diff <font color="gray">344</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2742">No.2742 Car Flow</a> (CPCTF 2024 : PPC (2024-04-20) - G問題、diff <font color="blue">1969</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2815">No.2815 Smaller than all</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - E問題、diff <font color="orange">2723</font>)
- <a href="https://yukicoder.me/problems/no/2837">No.2837 Flip Triomino</a> (yukicoder contest 440 (2024-08-09) - C問題、diff <font color="yellowgreen">2099</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

　
<h2 id="sorted set">290. sorted set</h2>

### 難易度統計

「sorted set」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1922</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1448</font>
- 2023年: ★2.8／diff <font color="yellowgreen">2068</font>
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「sorted set」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)

　
<h2 id="最適化を各寄与の最適化に緩和">291. 最適化を各寄与の最適化に緩和</h2>

### 難易度統計

「最適化を各寄与の最適化に緩和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="blue">1961</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2062</font>
- 2023年: ★3／diff <font color="blue">1758</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最適化を各寄与の最適化に緩和」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

　
<h2 id="B進法">292. B進法</h2>

### 難易度統計

「B進法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2013</font>
- 2024年: ★2.2／diff <font color="blue">1753</font>
- 2023年: ★2.7／diff <font color="blue">1799</font>
- 2022年: ★3.6／diff <font color="orange">2529</font>

### レベル別問題一覧

「B進法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2416">No.2416 vs Slime</a> (MMA Contest 016 (2023-08-12) - C問題、diff <font color="gray">304</font>)
- <a href="https://yukicoder.me/problems/no/2699">No.2699 Simple Math (Returned)</a> (yukicoder contest 424 (2024-03-29) - A問題、diff <font color="deepskyblue">1276</font>)

##### ★★

- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)
- <a href="https://yukicoder.me/problems/no/2663">No.2663 Zero-Sum Submatrices</a> (yukicoder contest 420 (2024-03-08) - A問題、diff <font color="deepskyblue">1204</font>)
- <a href="https://yukicoder.me/problems/no/2828">No.2828 Remainder Game</a> (yukicoder contest 439 (2024-08-02) - B問題、diff <font color="blue">1696</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題、diff <font color="blue">1989</font>)
- <a href="https://yukicoder.me/problems/no/2410">No.2410 Nine Numbers</a> (yukicoder contest 401 (2023-08-11) - D問題、diff <font color="deepskyblue">1318</font>)
- <a href="https://yukicoder.me/problems/no/2733">No.2733 Just K-times TSP</a> (yukicoder contest 428 (2024-04-19) - F問題、diff <font color="blue">1977</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2198">No.2198 Concon Substrings (COuNt-CONstruct Version)</a> (yukicoder contest 374 (2023-01-20) - E問題、diff <font color="yellowgreen">2050</font>)
- <a href="https://yukicoder.me/problems/no/2965">No.2965 Don't Stop the Game again</a> (yukicoder contest 453 (2024-11-16) - F問題、diff <font color="orange">2613</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)
- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題、diff <font color="orange">2500</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)
- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="区間加算更新">293. 区間加算更新</h2>

### 難易度統計

「区間加算更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2029</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2101</font>
- 2023年: ★2.7／diff <font color="blue">1841</font>
- 2022年: ★3.1／diff <font color="yellowgreen">2247</font>

### レベル別問題一覧

「区間加算更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2154">No.2154 あさかつの参加人数</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - B問題、diff <font color="brown">711</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2462">No.2462 七人カノン</a> (yukicoder contest 404 (2023-09-08) - C問題、diff <font color="deepskyblue">1358</font>)
- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)
- <a href="https://yukicoder.me/problems/no/2662">No.2662 Installing Cell Towers</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2796">No.2796 Small Matryoshka</a> (yukicoder contest 435 (2024-06-28) - B問題、diff <font color="blue">1848</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2761">No.2761 Substitute and Search</a> (yukicoder contest 430 (2024-05-17) - E問題、diff <font color="blue">1960</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="約数の走査を倍数の走査に帰着">294. 約数の走査を倍数の走査に帰着</h2>

### 難易度統計

「約数の走査を倍数の走査に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2032</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1509</font>
- 2023年: ★2.9／diff <font color="yellowgreen">2055</font>
- 2022年: ★3／diff <font color="yellowgreen">2236</font>

### レベル別問題一覧

「約数の走査を倍数の走査に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)
- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2552">No.2552 Not Coprime, Not Divisor</a> (MMA Contest 017 (2023-11-25) - F問題、diff <font color="yellowgreen">2235</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2081">No.2081 Make a Test Case of GCD Subset </a> (yukicoder contest 361 (2022-09-25) - D問題、diff <font color="yellowgreen">2167</font>)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題、diff <font color="blue">1983</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="数え上げを総和計算に帰着">295. 数え上げを総和計算に帰着</h2>

### 難易度統計

「数え上げを総和計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2035</font>
- 2024年: ★2.7／diff <font color="blue">1960</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2042</font>
- 2022年: ★3／diff <font color="yellowgreen">2161</font>

### レベル別問題一覧

「数え上げを総和計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="平面走査">296. 平面走査</h2>

### 難易度統計

「平面走査」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2036</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2130</font>
- 2023年: ★2.8／diff <font color="blue">1917</font>
- 2022年: ★3／diff <font color="yellowgreen">2145</font>

### レベル別問題一覧

「平面走査」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題、diff <font color="deepskyblue">1200</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題、diff <font color="blue">1927</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)
- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="フェニック木">297. フェニック木</h2>

### 難易度統計

「フェニック木」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2050</font>
- 2024年: ★2.9／diff <font color="yellowgreen">2029</font>
- 2023年: ★2.6／diff <font color="yellowgreen">2013</font>
- 2022年: ★3／diff <font color="yellowgreen">2109</font>

### レベル別問題一覧

「フェニック木」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題、diff <font color="blue">1649</font>)
- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)
- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2640">No.2640 traO Stamps</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - D問題、diff <font color="blue">1717</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題、diff <font color="yellowgreen">2049</font>)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2616">No.2616 中央番目の中央値</a> (yukicoder contest 416 (2024-01-26) - C問題、diff <font color="yellowgreen">2143</font>)
- <a href="https://yukicoder.me/problems/no/2761">No.2761 Substitute and Search</a> (yukicoder contest 430 (2024-05-17) - E問題、diff <font color="blue">1960</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="区間の重複度計算">298. 区間の重複度計算</h2>

### 難易度統計

「区間の重複度計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2052</font>
- 2024年: ★2.5／diff <font color="blue">1848</font>
- 2023年: ★2.5／diff <font color="blue">1661</font>
- 2022年: ★3.5／diff <font color="orange">2649</font>

### レベル別問題一覧

「区間の重複度計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題、diff <font color="blue">1661</font>)
- <a href="https://yukicoder.me/problems/no/2796">No.2796 Small Matryoshka</a> (yukicoder contest 435 (2024-06-28) - B問題、diff <font color="blue">1848</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

　
<h2 id="超頂点追加">299. 超頂点追加</h2>

### 難易度統計

「超頂点追加」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2055</font>
- 2024年: ★3／diff <font color="yellowgreen">2003</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2107</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「超頂点追加」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題、diff <font color="blue">1795</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2263">No.2263 Perms</a> (yukicoder contest 383 (2023-04-07) - E問題、diff <font color="orange">2420</font>)
- <a href="https://yukicoder.me/problems/no/2604">No.2604 Initial Motion</a> (yukicoder contest 414 (2024-01-12) - F問題、diff <font color="yellowgreen">2048</font>)
- <a href="https://yukicoder.me/problems/no/2713">No.2713 Just Solitaire</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - H問題、diff <font color="blue">1959</font>)

　
<h2 id="押し付け戦略">300. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略">押し付け戦略</a></h2>

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

　
<h2 id="素因数分解による付値計算">301. 素因数分解による付値計算</h2>

### 難易度統計

「素因数分解による付値計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2076</font>
- 2024年: ★2.5／diff <font color="blue">1840</font>
- 2023年: ★3.1／diff <font color="yellowgreen">2218</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素因数分解による付値計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2576">No.2576 LCM Pattern</a> (Advent Calendar Contest 2023 (2023-12-01) - D問題、diff <font color="blue">1842</font>)
- <a href="https://yukicoder.me/problems/no/2954">No.2954 Calculation of Exponentiation</a> (yukicoder contest 452 (2024-11-08) - B問題、diff <font color="blue">1941</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="オイラー関数計算">302. オイラー関数計算</h2>

### 難易度統計

「オイラー関数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2081</font>
- 2024年: ★3／diff <font color="yellowgreen">2025</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2109</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「オイラー関数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2552">No.2552 Not Coprime, Not Divisor</a> (MMA Contest 017 (2023-11-25) - F問題、diff <font color="yellowgreen">2235</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題、diff <font color="blue">1983</font>)
- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)

　
<h2 id="座標圧縮">303. 座標圧縮</h2>

### 難易度統計

「座標圧縮」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2125</font>
- 2024年: ★2.7／diff <font color="blue">1938</font>
- 2023年: ★2.9／diff <font color="yellowgreen">2303</font>
- 2022年: ★3／diff <font color="yellowgreen">2145</font>

### レベル別問題一覧

「座標圧縮」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2710">No.2710 How many more?</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - E問題、diff <font color="green">990</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2421">No.2421 entersys?</a> (MMA Contest 016 (2023-08-12) - H問題、diff <font color="blue">1788</font>)
- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題、diff <font color="blue">1696</font>)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2434">No.2434 RAKUTAN de RAKUTAN</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - K問題、diff <font color="orange">2721</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="冪等重みの最短経路長計算">304. 冪等重みの最短経路長計算</h2>

### 難易度統計

「冪等重みの最短経路長計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2133</font>
- 2024年: ★3／diff <font color="yellowgreen">2139</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2126</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「冪等重みの最短経路長計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題、diff <font color="yellowgreen">2044</font>)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2786">No.2786 RMQ on Grid Path</a> (yukicoder contest 433 (2024-06-14) - F問題、diff <font color="yellowgreen">2162</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2497">No.2497 GCD of LCMs</a> (yukicoder contest 407 (2023-10-06) - F問題、diff <font color="yellowgreen">2209</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

　
<h2 id="高さ奇数ニム和">305. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和">高さ奇数ニム和</a></h2>

### 難易度統計

「[高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2134</font>
- 2024年: ★3／diff <font color="yellowgreen">2197</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★2.5／diff <font color="yellowgreen">2008</font>

### レベル別問題一覧

「[高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題、diff <font color="yellowgreen">2008</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2619">No.2619 Sorted Nim</a> (yukicoder contest 416 (2024-01-26) - F問題、diff <font color="yellowgreen">2349</font>)
- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)

　
<h2 id="$45$度回転">306. $45$度回転</h2>

### 難易度統計

「$45$度回転」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2253</font>
- 2024年: ★2.8／diff <font color="orange">2481</font>
- 2023年: ★2.7／diff <font color="blue">1910</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「$45$度回転」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2261">No.2261 Coffee</a> (yukicoder contest 383 (2023-04-07) - C問題、diff <font color="deepskyblue">1536</font>)
- <a href="https://yukicoder.me/problems/no/2641">No.2641 draw X</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - E問題、diff <font color="yellowgreen">2158</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)
- <a href="https://yukicoder.me/problems/no/2612">No.2612 Close the Distance</a> (yukicoder contest 415 (2024-01-19) - F問題、diff <font color="red">2833</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

　
<h2 id="最終手番の任意性">307. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性">最終手番の任意性</a></h2>

### 難易度統計

「[最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2254</font>
- 2024年: ★3／diff <font color="orange">2676</font>
- 2023年: ★3／diff <font color="yellowgreen">2153</font>
- 2022年: ★2.5／diff <font color="blue">1934</font>

### レベル別問題一覧

「[最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題、diff <font color="blue">1934</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2814">No.2814 Block Game</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - D問題、diff <font color="orange">2676</font>)

　
<h2 id="複数ナップサック最適化">308. 複数ナップサック最適化</h2>

### 難易度統計

「複数ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2269</font>
- 2024年: ★3／diff <font color="yellowgreen">2227</font>
- 2023年: ★2.5／diff <font color="yellowgreen">2353</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「複数ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2422">No.2422 regisys?</a> (MMA Contest 016 (2023-08-12) - I問題、diff <font color="yellowgreen">2353</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2686">No.2686 商品券の使い道</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - H問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)

　
<h2 id="既存のアルゴリズムの変形">309. 既存のアルゴリズムの変形</h2>

### 難易度統計

「既存のアルゴリズムの変形」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2297</font>
- 2024年: ★3／diff <font color="orange">2442</font>
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
- <a href="https://yukicoder.me/problems/no/2642">No.2642 Don't cut line!</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - F問題、diff <font color="yellowgreen">2249</font>)
- <a href="https://yukicoder.me/problems/no/2698">No.2698 Many Asakatsu</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - H問題、diff <font color="red">2944</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)

　
<h2 id="累積max・min">310. 累積max・min</h2>

### 難易度統計

「累積max・min」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="yellowgreen">2310</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2381</font>
- 2023年: ★3／diff <font color="yellowgreen">2169</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「累積max・min」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2743">No.2743 Twisted Lattice</a> (CPCTF 2024 : PPC (2024-04-20) - H問題、diff <font color="yellowgreen">2309</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

　
<h2 id="Convex Hull Trick">311. Convex Hull Trick</h2>

### 難易度統計

「Convex Hull Trick」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="orange">2514</font>
- 2024年: ★3／diff <font color="orange">2649</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2379</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Convex Hull Trick」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2404">No.2404 Vertical Throw Up</a> (yukicoder contest 400 (2023-08-04) - F問題、diff <font color="yellowgreen">2337</font>)
- <a href="https://yukicoder.me/problems/no/2698">No.2698 Many Asakatsu</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - H問題、diff <font color="red">2944</font>)
- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

　
<h2 id="１次式の族の最大・最小値取得">312. １次式の族の最大・最小値取得</h2>

### 難易度統計

「１次式の族の最大・最小値取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="orange">2514</font>
- 2024年: ★3／diff <font color="orange">2649</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2379</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「１次式の族の最大・最小値取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2404">No.2404 Vertical Throw Up</a> (yukicoder contest 400 (2023-08-04) - F問題、diff <font color="yellowgreen">2337</font>)
- <a href="https://yukicoder.me/problems/no/2698">No.2698 Many Asakatsu</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - H問題、diff <font color="red">2944</font>)
- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

　
<h2 id="折れ線を直線族で管理">313. 折れ線を直線族で管理</h2>

### 難易度統計

「折れ線を直線族で管理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.8／diff <font color="orange">2514</font>
- 2024年: ★3／diff <font color="orange">2649</font>
- 2023年: ★2.7／diff <font color="yellowgreen">2379</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「折れ線を直線族で管理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2495">No.2495 Three Sets</a> (yukicoder contest 407 (2023-10-06) - D問題、diff <font color="orange">2421</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2404">No.2404 Vertical Throw Up</a> (yukicoder contest 400 (2023-08-04) - F問題、diff <font color="yellowgreen">2337</font>)
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2698">No.2698 Many Asakatsu</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - H問題、diff <font color="red">2944</font>)
- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

　
<h2 id="osa_k法">314. osa_k法</h2>

### 難易度統計

「osa_k法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2025</font>
- 2024年: ★2.5／diff <font color="blue">1751</font>
- 2023年: ★4／diff <font color="orange">2567</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「osa_k法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2758">No.2758 RDQ</a> (yukicoder contest 430 (2024-05-17) - B問題、diff <font color="blue">1659</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2724">No.2724 Coprime Game 1</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - D問題、diff <font color="blue">1845</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2756">No.2756 GCD Teleporter</a> (yukicoder contest 429 (2024-05-10) - H問題、diff <font color="blue">1751</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="平方分割">315. 平方分割</h2>

### 難易度統計

「平方分割」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2091</font>
- 2024年: ★2.5／diff <font color="blue">1760</font>
- 2023年: ★3.2／diff <font color="yellowgreen">2273</font>
- 2022年: ★3／diff <font color="yellowgreen">2393</font>

### レベル別問題一覧

「平方分割」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2767">No.2767 Add to Divide</a> (yukicoder contest 431 (2024-05-31) - C問題、diff <font color="deepskyblue">1516</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2652">No.2652 [Cherry 6th Tune N] Δρονε χιρχλινγ</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - F問題、diff <font color="yellowgreen">2004</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題、diff <font color="yellowgreen">2381</font>)

　
<h2 id="解法場合分け">316. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け">解法場合分け</a></h2>

### 難易度統計

「[解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2103</font>
- 2024年: ★2.7／diff <font color="blue">1809</font>
- 2023年: ★3／diff <font color="yellowgreen">2176</font>
- 2022年: ★3／diff <font color="yellowgreen">2227</font>

### レベル別問題一覧

「[解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題、diff <font color="blue">1641</font>)
- <a href="https://yukicoder.me/problems/no/2672">No.2672 Subset Xor Sum</a> (yukicoder contest 421  (NUPC2023) (2024-03-15) - B問題、diff <font color="deepskyblue">1416</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)
- <a href="https://yukicoder.me/problems/no/2359">No.2359 A in S ?</a> (yukicoder contest 394 (2023-06-23) - C問題、diff <font color="yellowgreen">2165</font>)
- <a href="https://yukicoder.me/problems/no/2366">No.2366 登校</a> (yukicoder contest 395 (2023-06-30) - C問題、diff <font color="yellowgreen">2294</font>)
- <a href="https://yukicoder.me/problems/no/2519">No.2519 Coins in Array</a> (yukicoder contest 410 (2023-10-27) - E問題、diff <font color="yellowgreen">2069</font>)
- <a href="https://yukicoder.me/problems/no/2732">No.2732 Similar Permutations</a> (yukicoder contest 428 (2024-04-19) - E問題、diff <font color="yellowgreen">2203</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮">317. 区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮</h2>

### 難易度統計

「区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2121</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2227</font>
- 2023年: ★3／diff <font color="yellowgreen">2097</font>
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2656">No.2656 XOR Slimes</a> (yukicoder contest 419 (2024-03-01) - B問題、diff <font color="blue">1726</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)

　
<h2 id="小さいケースの構築を拡張">318. 小さいケースの構築を拡張</h2>

### 難易度統計

「小さいケースの構築を拡張」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2126</font>
- 2024年: ★2.6／diff <font color="yellowgreen">2039</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="yellowgreen">2300</font>

### レベル別問題一覧

「小さいケースの構築を拡張」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2614">No.2614 Delete ABC</a> (yukicoder contest 416 (2024-01-26) - A問題、diff <font color="gray">365</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題、diff <font color="yellowgreen">2039</font>)
- <a href="https://yukicoder.me/problems/no/2610">No.2610 Decreasing LCMs</a> (yukicoder contest 415 (2024-01-19) - D問題、diff <font color="yellowgreen">2129</font>)
- <a href="https://yukicoder.me/problems/no/2700">No.2700 Please Hack Greedy Solution!</a> (yukicoder contest 424 (2024-03-29) - B問題、diff <font color="yellowgreen">2030</font>)
- <a href="https://yukicoder.me/problems/no/2797">No.2797 Square Tile</a> (yukicoder contest 435 (2024-06-28) - C問題、diff <font color="yellowgreen">2328</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2143">No.2143 Only One Bracket</a> (yukicoder contest 370 (2022-12-02) - D問題、diff <font color="blue">1606</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2719">No.2719 Equal Inner Products in Permutation</a> (yukicoder contest 426 (2024-04-05) - F問題、diff <font color="orange">2522</font>)
- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2151">No.2151 3 on Torus-Lohkous</a> (Advent Calendar Contest 2022 (2022-12-01) - H問題、diff <font color="darkgoldenrod ">3257</font>)

　
<h2 id="行列累乗">319. 行列累乗</h2>

### 難易度統計

「行列累乗」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2166</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2351</font>
- 2023年: ★3／diff <font color="yellowgreen">2359</font>
- 2022年: ★3／diff <font color="deepskyblue">1220</font>

### レベル別問題一覧

「行列累乗」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2503">No.2503 Typical Path Counting Problem on a Grid</a> (yukicoder contest 408 (2023-10-13) - D問題、diff <font color="orange">2603</font>)
- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

　
<h2 id="ナップサック割り当て数え上げ">320. ナップサック割り当て数え上げ</h2>

### 難易度統計

「ナップサック割り当て数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★2.9／diff <font color="yellowgreen">2286</font>
- 2024年: ★3／diff <font color="yellowgreen">2182</font>
- 2023年: ★2.5／diff <font color="yellowgreen">2154</font>
- 2022年: ★3.2／diff <font color="orange">2574</font>

### レベル別問題一覧

「ナップサック割り当て数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2429">No.2429 Happiest Tabehodai Ways</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - F問題、diff <font color="blue">1907</font>)
- <a href="https://yukicoder.me/problems/no/2581">No.2581 [Cherry Anniversary 3] 28輪の桜のブーケ</a> (Advent Calendar Contest 2023 (2023-12-01) - I問題、diff <font color="orange">2401</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題、diff <font color="orange">2595</font>)
- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)
- <a href="https://yukicoder.me/problems/no/2846">No.2846 Birthday Cake</a> (yukicoder contest 441 (2024-08-23) - E問題、diff <font color="yellowgreen">2116</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

　
<h2 id="閉路と残りに分割">321. 閉路と残りに分割</h2>

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

　
<h2 id="任意mod畳み込み">322. 任意mod畳み込み</h2>

### 難易度統計

「任意mod畳み込み」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1849</font>
- 2024年: ★3／diff <font color="blue">1849</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「任意mod畳み込み」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)

　
<h2 id="偏角ソート">323. 偏角ソート</h2>

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

　
<h2 id="mex取得">324. mex取得</h2>

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

　
<h2 id="最小カット計算">325. 最小カット計算</h2>

### 難易度統計

「最小カット計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1959</font>
- 2024年: ★3／diff <font color="blue">1959</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最小カット計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2713">No.2713 Just Solitaire</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - H問題、diff <font color="blue">1959</font>)

　
<h2 id="最大流計算">326. 最大流計算</h2>

### 難易度統計

「最大流計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1959</font>
- 2024年: ★3／diff <font color="blue">1959</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最大流計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2713">No.2713 Just Solitaire</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - H問題、diff <font color="blue">1959</font>)

　
<h2 id="最大流最小カット定理">327. 最大流最小カット定理</h2>

### 難易度統計

「最大流最小カット定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1959</font>
- 2024年: ★3／diff <font color="blue">1959</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最大流最小カット定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2713">No.2713 Just Solitaire</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - H問題、diff <font color="blue">1959</font>)

　
<h2 id="従属選択コストなしナップサック最適化">328. 従属選択コストなしナップサック最適化</h2>

### 難易度統計

「従属選択コストなしナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1959</font>
- 2024年: ★3／diff <font color="blue">1959</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「従属選択コストなしナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2713">No.2713 Just Solitaire</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - H問題、diff <font color="blue">1959</font>)

　
<h2 id="スライド最小化">329. スライド最小化</h2>

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

　
<h2 id="区間積取得">330. 区間積取得</h2>

### 難易度統計

「区間積取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="blue">1960</font>
- 2024年: ★3／diff <font color="blue">1960</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間積取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2761">No.2761 Substitute and Search</a> (yukicoder contest 430 (2024-05-17) - E問題、diff <font color="blue">1960</font>)

　
<h2 id="正弦定理">331. 正弦定理</h2>

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

　
<h2 id="２次元累積和">332. ２次元累積和</h2>

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

　
<h2 id="矩形和取得">333. 矩形和取得</h2>

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

　
<h2 id="焼きなまし法">334. 焼きなまし法</h2>

### 難易度統計

「焼きなまし法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2004</font>
- 2024年: ★3／diff <font color="yellowgreen">2004</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「焼きなまし法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2652">No.2652 [Cherry 6th Tune N] Δρονε χιρχλινγ</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - F問題、diff <font color="yellowgreen">2004</font>)

　
<h2 id="素因数分解によるオイラー関数計算">335. 素因数分解によるオイラー関数計算</h2>

### 難易度統計

「素因数分解によるオイラー関数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2025</font>
- 2024年: ★3／diff <font color="yellowgreen">2025</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「素因数分解によるオイラー関数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)

　
<h2 id="累積和・グリッド上のDPを経路数え上げに翻訳">336. 累積和・グリッド上のDPを経路数え上げに翻訳</h2>

### 難易度統計

「累積和・グリッド上のDPを経路数え上げに翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2028</font>
- 2024年: ★3／diff <font color="yellowgreen">2028</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「累積和・グリッド上のDPを経路数え上げに翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2792">No.2792 Security Cameras on Young Diagram</a> (yukicoder contest 434 (2024-06-21) - D問題、diff <font color="blue">1813</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="木の頂点の深さ計算">337. 木の頂点の深さ計算</h2>

### 難易度統計

「木の頂点の深さ計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2046</font>
- 2024年: ★3／diff <font color="yellowgreen">2046</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「木の頂点の深さ計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2726">No.2726 Rooted Tree Nim</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - F問題、diff <font color="yellowgreen">2046</font>)

　
<h2 id="オイラーの規準">338. オイラーの規準</h2>

### 難易度統計

「オイラーの規準」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2047</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「オイラーの規準」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)

　
<h2 id="平方剰余判定">339. 平方剰余判定</h2>

### 難易度統計

「平方剰余判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2047</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「平方剰余判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)

　
<h2 id="最小費用流計算">340. 最小費用流計算</h2>

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

　
<h2 id="ループ戦略">341. ループ戦略</h2>

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

　
<h2 id="内積の畳み込み計算">342. 内積の畳み込み計算</h2>

### 難易度統計

「内積の畳み込み計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2053</font>
- 2024年: ★3／diff <font color="blue">1849</font>
- 2023年: ★3／diff <font color="yellowgreen">2258</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「内積の畳み込み計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題、diff <font color="yellowgreen">2258</font>)
- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)

　
<h2 id="レベル祖先計算">343. レベル祖先計算</h2>

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

　
<h2 id="弾性衝突を通過に翻訳して位置関係から復元">344. 弾性衝突を通過に翻訳して位置関係から復元</h2>

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

　
<h2 id="木の頂点の重さ計算">345. 木の頂点の重さ計算</h2>

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

　
<h2 id="経路復元">346. 経路復元</h2>

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

　
<h2 id="四角形を三角形２つや対角線２本に翻訳">347. 四角形を三角形２つや対角線２本に翻訳</h2>

### 難易度統計

「四角形を三角形２つや対角線２本に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2075</font>
- 2024年: ★3／diff <font color="yellowgreen">2003</font>
- 2023年: ★3／diff <font color="yellowgreen">2147</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「四角形を三角形２つや対角線２本に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題、diff <font color="yellowgreen">2147</font>)
- <a href="https://yukicoder.me/problems/no/2769">No.2769 Number of Rhombi</a> (yukicoder contest 431 (2024-05-31) - E問題、diff <font color="yellowgreen">2003</font>)

　
<h2 id="inplace DP">348. inplace DP</h2>

### 難易度統計

「inplace DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2102</font>
- 2024年: ★3／diff <font color="orange">2454</font>
- 2023年: ★2.5／diff <font color="deepskyblue">1526</font>
- 2022年: ★4／diff <font color="red">2903</font>

### レベル別問題一覧

「inplace DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2549">No.2549 Paint Eggs</a> (MMA Contest 017 (2023-11-25) - C問題、diff <font color="green">884</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="ポラードの$\rho$">349. ポラードの$\rho$</h2>

### 難易度統計

「ポラードの$\rho$」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2105</font>
- 2024年: ★2.5／diff <font color="blue">1790</font>
- 2023年: ★4／diff <font color="orange">2795</font>
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「ポラードの$\rho$」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2682">No.2682 Visible Divisible</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - D問題、diff <font color="deepskyblue">1447</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="期待値の線形性">350. 期待値の線形性</h2>

### 難易度統計

「期待値の線形性」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2121</font>
- 2024年: ★2.6／diff <font color="blue">1895</font>
- 2023年: ★3／diff <font color="yellowgreen">2168</font>
- 2022年: ★4／diff <font color="orange">2566</font>

### レベル別問題一覧

「期待値の線形性」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2457">No.2457 Stampaholic (Easy)</a> (yukicoder contest 403 (2023-09-01) - H問題、diff <font color="yellowgreen">2358</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題、diff <font color="orange">2566</font>)

　
<h2 id="総和計算の期待値への帰着">351. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着">総和計算の期待値への帰着</a></h2>

### 難易度統計

「[総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2124</font>
- 2024年: ★3／diff <font color="yellowgreen">2145</font>
- 2023年: ★2.6／diff <font color="blue">1971</font>
- 2022年: ★4／diff <font color="orange">2566</font>

### レベル別問題一覧

「[総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題、diff <font color="yellowgreen">2121</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題、diff <font color="yellowgreen">2170</font>)
- <a href="https://yukicoder.me/problems/no/2816">No.2816 At Most Two Moves</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - F問題、diff <font color="yellowgreen">2145</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題、diff <font color="orange">2566</font>)

　
<h2 id="重複選択可ナップサック割り当て数え上げ">352. 重複選択可ナップサック割り当て数え上げ</h2>

### 難易度統計

「重複選択可ナップサック割り当て数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2125</font>
- 2024年: ★3／diff <font color="yellowgreen">2125</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「重複選択可ナップサック割り当て数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)
- <a href="https://yukicoder.me/problems/no/2846">No.2846 Birthday Cake</a> (yukicoder contest 441 (2024-08-23) - E問題、diff <font color="yellowgreen">2116</font>)

　
<h2 id="分割方法数え上げ">353. 分割方法数え上げ</h2>

### 難易度統計

「分割方法数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2125</font>
- 2024年: ★3／diff <font color="yellowgreen">2125</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「分割方法数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)
- <a href="https://yukicoder.me/problems/no/2846">No.2846 Birthday Cake</a> (yukicoder contest 441 (2024-08-23) - E問題、diff <font color="yellowgreen">2116</font>)

　
<h2 id="最適遷移を自己写像に翻訳">354. 最適遷移を自己写像に翻訳</h2>

### 難易度統計

「最適遷移を自己写像に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2129</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2129</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最適遷移を自己写像に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題、diff <font color="yellowgreen">2274</font>)
- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)

　
<h2 id="累積積">355. 累積積</h2>

### 難易度統計

「累積積」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2130</font>
- 2024年: ★3／diff <font color="yellowgreen">2130</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「累積積」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="累積積による二項係数計算">356. 累積積による二項係数計算</h2>

### 難易度統計

「累積積による二項係数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2130</font>
- 2024年: ★3／diff <font color="yellowgreen">2130</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「累積積による二項係数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="分割数計算">357. 分割数計算</h2>

### 難易度統計

「分割数計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2134</font>
- 2024年: ★3／diff <font color="yellowgreen">2134</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「分割数計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2798">No.2798 Multiple Chain</a> (yukicoder contest 435 (2024-06-28) - D問題、diff <font color="yellowgreen">2134</font>)

　
<h2 id="高階累積和">358. 高階累積和</h2>

### 難易度統計

「高階累積和」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2135</font>
- 2024年: ★3／diff <font color="yellowgreen">2135</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「高階累積和」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

　
<h2 id="カタランの三角形計算">359. カタランの三角形計算</h2>

### 難易度統計

「カタランの三角形計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2141</font>
- 2024年: ★3／diff <font color="yellowgreen">2141</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「カタランの三角形計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2754">No.2754 Cumulate and Drop</a> (yukicoder contest 429 (2024-05-10) - F問題、diff <font color="yellowgreen">2141</font>)

　
<h2 id="ダブリング">360. ダブリング</h2>

### 難易度統計

「ダブリング」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2141</font>
- 2024年: ★3／diff <font color="yellowgreen">2249</font>
- 2023年: ★3／diff <font color="yellowgreen">2105</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ダブリング」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題、diff <font color="yellowgreen">2274</font>)
- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)
- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)
- <a href="https://yukicoder.me/problems/no/2642">No.2642 Don't cut line!</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - F問題、diff <font color="yellowgreen">2249</font>)

　
<h2 id="２次元imos法">361. ２次元imos法</h2>

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

　
<h2 id="矩形加算更新">362. 矩形加算更新</h2>

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

　
<h2 id="フロー">363. フロー</h2>

### 難易度統計

「フロー」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2142</font>
- 2024年: ★3／diff <font color="yellowgreen">2003</font>
- 2023年: ★3／diff <font color="orange">2420</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「フロー」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2263">No.2263 Perms</a> (yukicoder contest 383 (2023-04-07) - E問題、diff <font color="orange">2420</font>)
- <a href="https://yukicoder.me/problems/no/2604">No.2604 Initial Motion</a> (yukicoder contest 414 (2024-01-12) - F問題、diff <font color="yellowgreen">2048</font>)
- <a href="https://yukicoder.me/problems/no/2713">No.2713 Just Solitaire</a> (yukicoder contest 425 (MMA Contest 018) (2024-03-31) - H問題、diff <font color="blue">1959</font>)

　
<h2 id="ファンデルモンドの畳み込み">364. ファンデルモンドの畳み込み</h2>

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

　
<h2 id="最近共通祖先計算">365. 最近共通祖先計算</h2>

### 難易度統計

「最近共通祖先計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2152</font>
- 2024年: ★3／diff <font color="yellowgreen">2249</font>
- 2023年: ★3／diff <font color="yellowgreen">2056</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「最近共通祖先計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2337">No.2337 Equidistant</a> (yukicoder contest 391 (2023-06-02) - D問題、diff <font color="yellowgreen">2056</font>)
- <a href="https://yukicoder.me/problems/no/2642">No.2642 Don't cut line!</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - F問題、diff <font color="yellowgreen">2249</font>)

　
<h2 id="DPのデータ構造高速化">366. DPのデータ構造高速化</h2>

### 難易度統計

「DPのデータ構造高速化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2169</font>
- 2024年: ★2.9／diff <font color="yellowgreen">2035</font>
- 2023年: ★3／diff <font color="yellowgreen">2121</font>
- 2022年: ★3.3／diff <font color="yellowgreen">2332</font>

### レベル別問題一覧

「DPのデータ構造高速化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2791">No.2791 Beginner Contest</a> (yukicoder contest 434 (2024-06-21) - C問題、diff <font color="deepskyblue">1221</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題、diff <font color="orange">2758</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題、diff <font color="yellowgreen">2153</font>)
- <a href="https://yukicoder.me/problems/no/2433">No.2433 Min Increasing Sequence</a> (traP 作問ハッカソンコンテスト 001 (2023-08-18) - J問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2625">No.2625 Bouns Ai</a> (yukicoder contest 417 (2024-02-09) - E問題、diff <font color="blue">1654</font>)
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題、diff <font color="blue">1738</font>)
- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="コーシー・フロベニウスの補題">367. コーシー・フロベニウスの補題</h2>

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

　
<h2 id="二面体群">368. 二面体群</h2>

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

　
<h2 id="反射の倍化実装">369. 反射の倍化実装</h2>

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

　
<h2 id="区間max・min取得">370. 区間max・min取得</h2>

### 難易度統計

「区間max・min取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2194</font>
- 2024年: ★3／diff <font color="orange">2454</font>
- 2023年: ★3／diff <font color="yellowgreen">2169</font>
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「区間max・min取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

　
<h2 id="乱択">371. 乱択</h2>

### 難易度統計

「乱択」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2203</font>
- 2024年: ★3／diff <font color="yellowgreen">2203</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「乱択」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2732">No.2732 Similar Permutations</a> (yukicoder contest 428 (2024-04-19) - E問題、diff <font color="yellowgreen">2203</font>)

　
<h2 id="積和の和積化">372. 積和の和積化</h2>

### 難易度統計

「積和の和積化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2207</font>
- 2024年: ★2.8／diff <font color="yellowgreen">2040</font>
- 2023年: ★3.2／diff <font color="yellowgreen">2307</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「積和の和積化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題、diff <font color="blue">1922</font>)
- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題、diff <font color="yellowgreen">2237</font>)
- <a href="https://yukicoder.me/problems/no/2356">No.2356 Back Door Tour in Four Seasons</a> (yukicoder contest 393 (2023-06-16) - G問題、diff <font color="yellowgreen">2182</font>)
- <a href="https://yukicoder.me/problems/no/2598">No.2598 Kadomatsu on Tree</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)
- <a href="https://yukicoder.me/problems/no/2717">No.2717 Sum of Subarray of Subsequence</a> (yukicoder contest 426 (2024-04-05) - D問題、diff <font color="blue">1789</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2582">No.2582 Random Average^K</a> (Advent Calendar Contest 2023 (2023-12-01) - J問題、diff <font color="orange">2401</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="minimax法">373. minimax法</h2>

### 難易度統計

「minimax法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2208</font>
- 2024年: ★3.5／diff <font color="orange">2421</font>
- 2023年: ★2.5／diff <font color="blue">1996</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「minimax法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2532">No.2532 Want Play More</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - H問題、diff <font color="blue">1996</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="ゼータ変換">374. ゼータ変換</h2>

### 難易度統計

「ゼータ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2211</font>
- 2024年: ★2.7／diff <font color="blue">1770</font>
- 2023年: ★3.1／diff <font color="orange">2473</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「ゼータ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)
- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)
- <a href="https://yukicoder.me/problems/no/2686">No.2686 商品券の使い道</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - H問題、diff <font color="yellowgreen">2031</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="フビニの定理">375. フビニの定理</h2>

### 難易度統計

「フビニの定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2216</font>
- 2024年: ★2.5／diff <font color="yellowgreen">2031</font>
- 2023年: ★3.5／diff <font color="orange">2401</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「フビニの定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2683">No.2683 Two Sheets</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - E問題、diff <font color="yellowgreen">2031</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2582">No.2582 Random Average^K</a> (Advent Calendar Contest 2023 (2023-12-01) - J問題、diff <font color="orange">2401</font>)

　
<h2 id="既出を検索">376. 既出を検索</h2>

### 難易度統計

「既出を検索」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2224</font>
- 2024年: ★3／diff <font color="yellowgreen">2224</font>
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「既出を検索」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2722">No.2722 Kenken Fight</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - B問題、diff <font color="deepskyblue">1588</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2476">No.2476 Knight Game</a> (Japan Alumni Group Summer Camp 2023 Day 2 (2023-09-17) - J問題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="確率漸化式">377. 確率漸化式</h2>

### 難易度統計

「確率漸化式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2226</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2287</font>
- 2023年: ★3.1／diff <font color="yellowgreen">2186</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「確率漸化式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2964">No.2964 Obstruction Bingo</a> (yukicoder contest 453 (2024-11-16) - E問題、diff <font color="blue">1762</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2530">No.2530 Yellow Cards</a> (yukicoder contest 411 オムニバスコンテスト (2023-11-03) - F問題、diff <font color="yellowgreen">2042</font>)
- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2586">No.2586 Yet Another Sugoroku Problem</a> (Advent Calendar Contest 2023 (2023-12-01) - N問題、diff <font color="yellowgreen">2348</font>)

　
<h2 id="緩和">378. <a href="https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和">緩和</a></h2>

### 難易度統計

「[緩和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2228</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2062</font>
- 2023年: ★3.1／diff <font color="yellowgreen">2294</font>
- 2022年: ★3／diff <font color="yellowgreen">2252</font>

### レベル別問題一覧

「[緩和](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題、diff <font color="blue">1803</font>)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)
- <a href="https://yukicoder.me/problems/no/2665">No.2665 Minimize Inversions of Deque</a> (yukicoder contest 420 (2024-03-08) - C問題、diff <font color="deepskyblue">1540</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)
- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題、diff <font color="blue">1758</font>)
- <a href="https://yukicoder.me/problems/no/2957">No.2957 Combo Deck Builder</a> (yukicoder contest 452 (2024-11-08) - E問題、diff <font color="orange">2585</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="データ構造初期化">379. データ構造初期化</h2>

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

　
<h2 id="一対一対応と乱択の可換性">380. 一対一対応と乱択の可換性</h2>

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

　
<h2 id="基底計算">381. 基底計算</h2>

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

　
<h2 id="重み付き木上の頂点間距離取得">382. 重み付き木上の頂点間距離取得</h2>

### 難易度統計

「重み付き木上の頂点間距離取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2249</font>
- 2024年: ★3／diff <font color="yellowgreen">2249</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「重み付き木上の頂点間距離取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2642">No.2642 Don't cut line!</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - F問題、diff <font color="yellowgreen">2249</font>)

　
<h2 id="無向木の有向化">383. 無向木の有向化</h2>

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

　
<h2 id="自己写像に翻訳">384. 自己写像に翻訳</h2>

### 難易度統計

「自己写像に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2253</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="yellowgreen">2129</font>
- 2022年: ★3／diff <font color="orange">2501</font>

### レベル別問題一覧

「自己写像に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2082">No.2082 AND OR XOR</a> (yukicoder contest 361 (2022-09-25) - E問題、diff <font color="orange">2501</font>)
- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題、diff <font color="yellowgreen">2274</font>)
- <a href="https://yukicoder.me/problems/no/2543">No.2543 Many Meetings</a> (yukicoder contest 413 (2023-11-24) - C問題、diff <font color="blue">1985</font>)

　
<h2 id="商のfloorの分子をわたる総和計算">385. 商のfloorの分子をわたる総和計算</h2>

### 難易度統計

「商のfloorの分子をわたる総和計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2269</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.5／diff <font color="blue">1891</font>
- 2022年: ★3.5／diff <font color="orange">2648</font>

### レベル別問題一覧

「商のfloorの分子をわたる総和計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2452">No.2452 Incline</a> (yukicoder contest 403 (2023-09-01) - C問題、diff <font color="blue">1891</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題、diff <font color="orange">2648</font>)

　
<h2 id="セグメント木">386. セグメント木</h2>

### 難易度統計

「セグメント木」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2282</font>
- 2024年: ★3／diff <font color="yellowgreen">2282</font>
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「セグメント木」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2611">No.2611 Count 01</a> (yukicoder contest 415 (2024-01-19) - E問題、diff <font color="orange">2604</font>)
- <a href="https://yukicoder.me/problems/no/2761">No.2761 Substitute and Search</a> (yukicoder contest 430 (2024-05-17) - E問題、diff <font color="blue">1960</font>)

　
<h2 id="二分木に翻訳">387. 二分木に翻訳</h2>

### 難易度統計

「二分木に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2295</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2295</font>

### レベル別問題一覧

「二分木に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題、diff <font color="yellowgreen">2295</font>)

　
<h2 id="多次元コストナップサック割り当て数え上げ">388. 多次元コストナップサック割り当て数え上げ</h2>

### 難易度統計

「多次元コストナップサック割り当て数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2297</font>
- 2024年: ★3／diff <font color="yellowgreen">2297</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「多次元コストナップサック割り当て数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)

　
<h2 id="周期的構築">389. 周期的構築</h2>

### 難易度統計

「周期的構築」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2297</font>
- 2024年: ★3／diff <font color="orange">2594</font>
- 2023年: ★3／diff <font color="yellowgreen">2000</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「周期的構築」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2797">No.2797 Square Tile</a> (yukicoder contest 435 (2024-06-28) - C問題、diff <font color="yellowgreen">2328</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題、diff <font color="blue">1933</font>)
- <a href="https://yukicoder.me/problems/no/2411">No.2411 Reverse Directions</a> (yukicoder contest 401 (2023-08-11) - E問題、diff <font color="yellowgreen">2068</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="複素共役による絶対値計算">390. 複素共役による絶対値計算</h2>

### 難易度統計

「複素共役による絶対値計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2301</font>
- 2024年: ★3／diff <font color="yellowgreen">2301</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「複素共役による絶対値計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2651">No.2651 [Cherry 6th Tune B] $\mathbb{C}$omplex комбинат</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - E問題、diff <font color="yellowgreen">2301</font>)

　
<h2 id="タイリング・LightOut可能性を領域の細分による不変量計算に帰着">391. タイリング・LightOut可能性を領域の細分による不変量計算に帰着</h2>

### 難易度統計

「タイリング・LightOut可能性を領域の細分による不変量計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2302</font>
- 2024年: ★3／diff <font color="yellowgreen">2302</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「タイリング・LightOut可能性を領域の細分による不変量計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2845">No.2845 Birthday Pattern in Two Different Calendars</a> (yukicoder contest 441 (2024-08-23) - D問題、diff <font color="blue">1947</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2837">No.2837 Flip Triomino</a> (yukicoder contest 440 (2024-08-09) - C問題、diff <font color="yellowgreen">2099</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

　
<h2 id="ベルトラン・チェビシェフの定理">392. ベルトラン・チェビシェフの定理</h2>

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

　
<h2 id="素数に注目する質問">393. 素数に注目する質問</h2>

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

　
<h2 id="対角線に言及する質問">394. 対角線に言及する質問</h2>

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

　
<h2 id="グリッド上の価値最大化">395. グリッド上の価値最大化</h2>

### 難易度統計

「グリッド上の価値最大化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2311</font>
- 2024年: ★3／diff <font color="orange">2454</font>
- 2023年: ★3／diff <font color="yellowgreen">2169</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「グリッド上の価値最大化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

　
<h2 id="矩形max・min取得">396. 矩形max・min取得</h2>

### 難易度統計

「矩形max・min取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2311</font>
- 2024年: ★3／diff <font color="orange">2454</font>
- 2023年: ★3／diff <font color="yellowgreen">2169</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「矩形max・min取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

　
<h2 id="ローリングハッシュ">397. ローリングハッシュ</h2>

### 難易度統計

「ローリングハッシュ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2320</font>
- 2024年: ★3／diff <font color="yellowgreen">2053</font>
- 2023年: ★2.5／diff <font color="yellowgreen">2030</font>
- 2022年: ★3.5／diff <font color="red">2877</font>

### レベル別問題一覧

「ローリングハッシュ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2568">No.2568 列辞書順列列</a> (第2回緑以下コンテスト (2023-12-02) - L問題、diff <font color="blue">1632</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題、diff <font color="red">2852</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)
- <a href="https://yukicoder.me/problems/no/2761">No.2761 Substitute and Search</a> (yukicoder contest 430 (2024-05-17) - E問題、diff <font color="blue">1960</font>)
- <a href="https://yukicoder.me/problems/no/2858">No.2858 Make a Palindrome</a> (yukicoder contest 442 (2024-08-25) - I問題、diff <font color="yellowgreen">2147</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="連続回数制約を分割の区間長制約に翻訳">398. 連続回数制約を分割の区間長制約に翻訳</h2>

### 難易度統計

「連続回数制約を分割の区間長制約に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2344</font>
- 2024年: ★3／diff <font color="orange">2729</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="blue">1959</font>

### レベル別問題一覧

「連続回数制約を分割の区間長制約に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題、diff <font color="blue">1959</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)

　
<h2 id="余因子展開">399. 余因子展開</h2>

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

　
<h2 id="区間の部分列をわたる総和計算をモノイド演算に翻訳">400. 区間の部分列をわたる総和計算をモノイド演算に翻訳</h2>

### 難易度統計

「区間の部分列をわたる総和計算をモノイド演算に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2352</font>
- 2024年: ★3／diff <font color="yellowgreen">2352</font>
- 2023年: ★3／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間の部分列をわたる総和計算をモノイド演算に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2611">No.2611 Count 01</a> (yukicoder contest 415 (2024-01-19) - E問題、diff <font color="orange">2604</font>)
- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)

　
<h2 id="Monotone Minima">401. Monotone Minima</h2>

### 難易度統計

「Monotone Minima」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2354</font>
- 2024年: ★3／diff <font color="yellowgreen">2354</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Monotone Minima」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2764">No.2764 Warp Drive Spacecraft</a> (yukicoder contest 430 (2024-05-17) - H問題、diff <font color="yellowgreen">2354</font>)

　
<h2 id="剰余を取る前に符号や大小を計算">402. 剰余を取る前に符号や大小を計算</h2>

### 難易度統計

「剰余を取る前に符号や大小を計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2365</font>
- 2024年: ★3／diff <font color="yellowgreen">2365</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「剰余を取る前に符号や大小を計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2744">No.2744 Power! or +1</a> (CPCTF 2024 : PPC (2024-04-20) - I問題、diff <font color="yellowgreen">2309</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="bitset高速化">403. bitset高速化</h2>

### 難易度統計

「bitset高速化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2383</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="orange">2521</font>
- 2022年: ★3／diff <font color="yellowgreen">2245</font>

### レベル別問題一覧

「bitset高速化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2423">No.2423 Merge Stones</a> (MMA Contest 016 (2023-08-12) - J問題、diff <font color="orange">2521</font>)

　
<h2 id="一対一対応">404. 一対一対応</h2>

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

　
<h2 id="SIMD高速化">405. SIMD高速化</h2>

### 難易度統計

「SIMD高速化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2386</font>
- 2024年: ★3／diff <font color="yellowgreen">2386</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「SIMD高速化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2662">No.2662 Installing Cell Towers</a> (単発出題、diffデータなし)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2956">No.2956 Substitute with Average</a> (yukicoder contest 452 (2024-11-08) - D問題、diff <font color="yellowgreen">2386</font>)

　
<h2 id="平均の指定された区間数え上げ">406. 平均の指定された区間数え上げ</h2>

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

　
<h2 id="剰余の法を動かす総和計算">407. 剰余の法を動かす総和計算</h2>

### 難易度統計

「剰余の法を動かす総和計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="yellowgreen">2393</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3／diff <font color="yellowgreen">2393</font>

### レベル別問題一覧

「剰余の法を動かす総和計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題、diff <font color="yellowgreen">2393</font>)

　
<h2 id="剰余を商に翻訳">408. 剰余を商に翻訳</h2>

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

　
<h2 id="外接円計算">409. 外接円計算</h2>

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

　
<h2 id="第二余弦定理">410. 第二余弦定理</h2>

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

　
<h2 id="有理数の大小比較のオーバーフロー回避">411. 有理数の大小比較のオーバーフロー回避</h2>

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

　
<h2 id="連分数展開">412. 連分数展開</h2>

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

　
<h2 id="完全二部マッチング">413. 完全二部マッチング</h2>

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

　
<h2 id="始切片選択ナップサック最適化">414. 始切片選択ナップサック最適化</h2>

### 難易度統計

「始切片選択ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2423</font>
- 2024年: ★3／diff <font color="orange">2423</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「始切片選択ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)

　
<h2 id="始切片選択複数ナップサック最適化">415. 始切片選択複数ナップサック最適化</h2>

### 難易度統計

「始切片選択複数ナップサック最適化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2423</font>
- 2024年: ★3／diff <font color="orange">2423</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「始切片選択複数ナップサック最適化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2746">No.2746 Bicolor Pyramid</a> (CPCTF 2024 : PPC (2024-04-20) - K問題、diff <font color="orange">2423</font>)

　
<h2 id="相対運動に翻訳">416. 相対運動に翻訳</h2>

### 難易度統計

「相対運動に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2438</font>
- 2024年: ★3／diff <font color="orange">2438</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「相対運動に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)

　
<h2 id="区間挿入更新">417. 区間挿入更新</h2>

### 難易度統計

「区間挿入更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2463</font>
- 2024年: ★3／diff <font color="orange">2438</font>
- 2023年: ★3／diff <font color="orange">2489</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間挿入更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題、diff <font color="orange">2489</font>)
- <a href="https://yukicoder.me/problems/no/2687">No.2687 所により大雨</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - I問題、diff <font color="orange">2438</font>)

　
<h2 id="単調関数の像計算を階差の非零点の数え上げに帰着">418. 単調関数の像計算を階差の非零点の数え上げに帰着</h2>

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

　
<h2 id="分枝限定法">419. 分枝限定法</h2>

### 難易度統計

「分枝限定法」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2471</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3／diff <font color="orange">2471</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「分枝限定法」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題、diff <font color="orange">2471</font>)

　
<h2 id="区間削除更新">420. 区間削除更新</h2>

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

　
<h2 id="ワイルドカードの値を変数化">421. ワイルドカードの値を変数化</h2>

### 難易度統計

「ワイルドカードの値を変数化」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2506</font>
- 2024年: ★3／diff <font color="orange">2506</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「ワイルドカードの値を変数化」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2643">No.2643 Many Range Sums Problems</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - G問題、diff <font color="orange">2765</font>)
- <a href="https://yukicoder.me/problems/no/2653">No.2653 [Cherry 6th Tune] Re: start! (Make it Zero!)</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - G問題、diff <font color="yellowgreen">2247</font>)

　
<h2 id="準同型">422. 準同型</h2>

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

　
<h2 id="区間乗算更新">423. 区間乗算更新</h2>

### 難易度統計

「区間乗算更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2729</font>
- 2024年: ★3／diff <font color="orange">2729</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間乗算更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)

　
<h2 id="１次不等式の充足可能性判定">424. １次不等式の充足可能性判定</h2>

### 難易度統計

「１次不等式の充足可能性判定」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3／diff <font color="orange">2765</font>
- 2024年: ★3／diff <font color="orange">2765</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「１次不等式の充足可能性判定」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2643">No.2643 Many Range Sums Problems</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - G問題、diff <font color="orange">2765</font>)

　
<h2 id="最小被覆半径計算">425. 最小被覆半径計算</h2>

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

　
<h2 id="タイリングによるミラー戦略">426. タイリングによるミラー戦略</h2>

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

　
<h2 id="辺を頂点とするグラフに翻訳">427. 辺を頂点とするグラフに翻訳</h2>

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

　
<h2 id="指定序数の値の計算や始切片数え上げを桁ごとの計算に帰着">428. 指定序数の値の計算や始切片数え上げを桁ごとの計算に帰着</h2>

### 難易度統計

「指定序数の値の計算や始切片数え上げを桁ごとの計算に帰着」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2122</font>
- 2024年: ★3／diff <font color="blue">1925</font>
- 2023年: ★3.1／diff <font color="yellowgreen">2171</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「指定序数の値の計算や始切片数え上げを桁ごとの計算に帰着」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2246">No.2246 1333-like Number</a> (yukicoder contest 381 (2023-03-17) - A問題、diff <font color="brown">689</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2455">No.2455 Numbers Dictionary</a> (yukicoder contest 403 (2023-09-01) - F問題、diff <font color="yellowgreen">2213</font>)
- <a href="https://yukicoder.me/problems/no/2772">No.2772 Appearing Even Times</a> (yukicoder contest 431 (2024-05-31) - H問題、diff <font color="blue">1925</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="制約からグラフの種類を特定">429. 制約からグラフの種類を特定</h2>

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

　
<h2 id="トポロジカルソート">430. トポロジカルソート</h2>

### 難易度統計

「トポロジカルソート」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2171</font>
- 2024年: ★2.2／diff <font color="deepskyblue">1566</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「トポロジカルソート」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2639">No.2639 Longest Increasing Walk</a> (traP 作問ハッカソンコンテスト 002(day2) (2024-02-19) - C問題、diff <font color="deepskyblue">1591</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2780">No.2780 The Bottle Imp</a> (yukicoder contest 432 (2024-06-07) - H問題、diff <font color="deepskyblue">1542</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="区間kth取得">431. 区間kth取得</h2>

### 難易度統計

「区間kth取得」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="yellowgreen">2307</font>
- 2024年: ★3.5／diff <font color="yellowgreen">2364</font>
- 2023年: ★2.5／diff <font color="blue">1851</font>
- 2022年: ★3.5／diff <font color="orange">2707</font>

### レベル別問題一覧

「区間kth取得」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題、diff <font color="blue">1851</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題、diff <font color="orange">2707</font>)
- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="互いに素に帰着">432. 互いに素に帰着</h2>

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

　
<h2 id="メビウス変換">433. メビウス変換</h2>

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

　
<h2 id="約数ゼータ変換">434. 約数ゼータ変換</h2>

### 難易度統計

「約数ゼータ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.1／diff <font color="orange">2440</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1509</font>
- 2023年: ★3.5／diff <font color="red">2906</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「約数ゼータ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2963">No.2963 Mecha DESU</a> (yukicoder contest 453 (2024-11-16) - D問題、diff <font color="deepskyblue">1509</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="最長共通接頭辞計算">435. 最長共通接頭辞計算</h2>

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

　
<h2 id="Moのアルゴリズム">436. Moのアルゴリズム</h2>

### 難易度統計

「Moのアルゴリズム」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2192</font>
- 2024年: ★3／diff <font color="yellowgreen">2004</font>
- 2023年: ★3.5／diff <font color="yellowgreen">2381</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「Moのアルゴリズム」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2652">No.2652 [Cherry 6th Tune N] Δρονε χιρχλινγ</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - F問題、diff <font color="yellowgreen">2004</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題、diff <font color="yellowgreen">2381</font>)

　
<h2 id="区間max・min更新">437. 区間max・min更新</h2>

### 難易度統計

「区間max・min更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2218</font>
- 2024年: ★3／diff <font color="yellowgreen">2006</font>
- 2023年: ★3／diff <font color="yellowgreen">2169</font>
- 2022年: ★4／diff <font color="red">2903</font>

### レベル別問題一覧

「区間max・min更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="双対セグメント木">438. 双対セグメント木</h2>

### 難易度統計

「双対セグメント木」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2218</font>
- 2024年: ★3／diff <font color="yellowgreen">2006</font>
- 2023年: ★3／diff <font color="yellowgreen">2169</font>
- 2022年: ★4／diff <font color="red">2903</font>

### レベル別問題一覧

「双対セグメント木」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2650">No.2650 [Cherry 6th Tune *] セイジャク</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - D問題、diff <font color="deepskyblue">1448</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題、diff <font color="yellowgreen">2169</font>)
- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2859">No.2859 Falling Balls</a> (yukicoder contest 442 (2024-08-25) - J問題、diff <font color="orange">2454</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="十分大きな法で計算">439. 十分大きな法で計算</h2>

### 難易度統計

「十分大きな法で計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2230</font>
- 2024年: ★3／diff <font color="blue">1849</font>
- 2023年: ★3.3／diff <font color="orange">2418</font>
- 2022年: ★3／diff <font color="yellowgreen">2047</font>

### レベル別問題一覧

「十分大きな法で計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題、diff <font color="yellowgreen">2047</font>)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題、diff <font color="yellowgreen">2258</font>)
- <a href="https://yukicoder.me/problems/no/2592">No.2592 おでぶなおばけさん 2</a> (Advent Calendar Contest 2023 (2023-12-01) - T問題、diff <font color="orange">2429</font>)
- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題、diff <font color="orange">2567</font>)

　
<h2 id="期待値漸化式">440. 期待値漸化式</h2>

### 難易度統計

「期待値漸化式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2255</font>
- 2024年: ★2.7／diff <font color="yellowgreen">2004</font>
- 2023年: ★3.5／diff <font color="orange">2423</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「期待値漸化式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題、diffデータなし)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題、diff <font color="blue">1622</font>)
- <a href="https://yukicoder.me/problems/no/2685">No.2685 Cell Proliferation (Easy)</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - G問題、diff <font color="blue">1983</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2389">No.2389 Cheating Code Golf</a> (yukicoder contest 398 (2023-07-21) - E問題、diff <font color="orange">2451</font>)
- <a href="https://yukicoder.me/problems/no/2829">No.2829 GCD Divination</a> (yukicoder contest 439 (2024-08-02) - C問題、diff <font color="yellowgreen">2025</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2579">No.2579 Dice Sum Infinity (制約変更版)</a> (Advent Calendar Contest 2023 (2023-12-01) - G問題、diff <font color="red">3196</font>)

　
<h2 id="指数と対数による冪乗計算">441. 指数と対数による冪乗計算</h2>

### 難易度統計

「指数と対数による冪乗計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2341</font>
- 2024年: ★3／diff <font color="yellowgreen">2130</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="orange">2553</font>

### レベル別問題一覧

「指数と対数による冪乗計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

　
<h2 id="外積・サラスの公式による行列式計算">442. 外積・サラスの公式による行列式計算</h2>

### 難易度統計

「外積・サラスの公式による行列式計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2352</font>
- 2024年: ★3.5／diff <font color="orange">2421</font>
- 2023年: ★3／diff <font color="yellowgreen">2284</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「外積・サラスの公式による行列式計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="行列式と面積・体積の関係">443. 行列式と面積・体積の関係</h2>

### 難易度統計

「行列式と面積・体積の関係」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2352</font>
- 2024年: ★3.5／diff <font color="orange">2421</font>
- 2023年: ★3／diff <font color="yellowgreen">2284</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「行列式と面積・体積の関係」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="フロベニウス数に注目">444. フロベニウス数に注目</h2>

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

　
<h2 id="調和数列による計算量評価">445. 調和数列による計算量評価</h2>

### 難易度統計

「調和数列による計算量評価」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2383</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★2.7／diff <font color="yellowgreen">2039</font>
- 2022年: ★3.7／diff <font color="orange">2728</font>

### レベル別問題一覧

「調和数列による計算量評価」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題、diff <font color="blue">1607</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題、diff <font color="orange">2471</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題、diff <font color="red">2903</font>)

　
<h2 id="同値関係">446. 同値関係</h2>

### 難易度統計

「同値関係」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="yellowgreen">2399</font>
- 2024年: ★3／diff <font color="yellowgreen">2302</font>
- 2023年: ★2／diff <font color="blue">1612</font>
- 2022年: ★3.8／diff <font color="orange">2758</font>

### レベル別問題一覧

「同値関係」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2566">No.2566 美しい整数列</a> (第2回緑以下コンテスト (2023-12-02) - J問題、diff <font color="blue">1612</font>)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2449">No.2449 square_permutation</a> (単発出題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2845">No.2845 Birthday Pattern in Two Different Calendars</a> (yukicoder contest 441 (2024-08-23) - D問題、diff <font color="blue">1947</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2837">No.2837 Flip Triomino</a> (yukicoder contest 440 (2024-08-09) - C問題、diff <font color="yellowgreen">2099</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)
- <a href="https://yukicoder.me/problems/no/2958">No.2958 Placing Many L-s</a> (yukicoder contest 452 (2024-11-08) - F問題、diff <font color="red">2860</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="総和の指定された部分列数え上げ">447. 総和の指定された部分列数え上げ</h2>

### 難易度統計

「総和の指定された部分列数え上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="orange">2425</font>
- 2024年: ★3／diff <font color="yellowgreen">2297</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.5／diff <font color="orange">2553</font>

### レベル別問題一覧

「総和の指定された部分列数え上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2788">No.2788 4-33 Hard</a> (yukicoder contest 433 (2024-06-14) - H問題、diff <font color="yellowgreen">2297</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題、diff <font color="orange">2553</font>)

　
<h2 id="集合族による帰属関係で類別">448. 集合族による帰属関係で類別</h2>

### 難易度統計

「集合族による帰属関係で類別」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="orange">2447</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★3.2／diff <font color="orange">2447</font>

### レベル別問題一覧

「集合族による帰属関係で類別」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題、diff <font color="orange">2649</font>)

　
<h2 id="マージ">449. マージ</h2>

### 難易度統計

「マージ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="orange">2454</font>
- 2024年: ★3／diff <font color="yellowgreen">2352</font>
- 2023年: ★3.5／diff <font color="orange">2658</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「マージ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2611">No.2611 Count 01</a> (yukicoder contest 415 (2024-01-19) - E問題、diff <font color="orange">2604</font>)
- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題、diffデータなし)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題、diff <font color="orange">2658</font>)

　
<h2 id="区間を中間で分割してマージ">450. 区間を中間で分割してマージ</h2>

### 難易度統計

「区間を中間で分割してマージ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.2／diff <font color="orange">2454</font>
- 2024年: ★3／diff <font color="yellowgreen">2352</font>
- 2023年: ★3.5／diff <font color="orange">2658</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間を中間で分割してマージ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2554">No.2554 MMA文字列2 (Query Version)</a> (MMA Contest 017 (2023-11-25) - H問題、diffデータなし)
- <a href="https://yukicoder.me/problems/no/2611">No.2611 Count 01</a> (yukicoder contest 415 (2024-01-19) - E問題、diff <font color="orange">2604</font>)
- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題、diff <font color="orange">2658</font>)

　
<h2 id="階数計算">451. 階数計算</h2>

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

　
<h2 id="行列の簡約階段化">452. 行列の簡約階段化</h2>

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

　
<h2 id="全方位木DP">453. 全方位木DP</h2>

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

　
<h2 id="剰余による確率的判定">454. 剰余による確率的判定</h2>

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

　
<h2 id="線形代数">455. 線形代数</h2>

### 難易度統計

「線形代数」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="orange">2404</font>
- 2024年: ★2.8／diff <font color="orange">2412</font>
- 2023年: ★3.7／diff <font color="orange">2632</font>
- 2022年: ★3／diff <font color="blue">1936</font>

### レベル別問題一覧

「線形代数」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2365">No.2365 Present of good number</a> (yukicoder contest 395 (2023-06-30) - B問題、diff <font color="blue">1887</font>)
- <a href="https://yukicoder.me/problems/no/2830">No.2830 Don't Stop the Game</a> (yukicoder contest 439 (2024-08-02) - D問題、diff <font color="orange">2525</font>)
- <a href="https://yukicoder.me/problems/no/2857">No.2857 Div Array</a> (yukicoder contest 442 (2024-08-25) - H問題、diff <font color="blue">1891</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題、diff <font color="yellowgreen">2245</font>)
- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題、diff <font color="deepskyblue">1220</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)
- <a href="https://yukicoder.me/problems/no/2832">No.2832 Nana's Fickle Adventure</a> (yukicoder contest 439 (2024-08-02) - F問題、diff <font color="red">2812</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2405">No.2405 Minimal Matrix Decomposition</a> (yukicoder contest 400 (2023-08-04) - G問題、diff <font color="orange">2741</font>)
- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)
- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)
- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="キュー">456. キュー</h2>

### 難易度統計

「キュー」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="orange">2412</font>
- 2024年: ★3／diff <font color="yellowgreen">2289</font>
- 2023年: ★4／diff <font color="orange">2658</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「キュー」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)
- <a href="https://yukicoder.me/problems/no/2833">No.2833 Count Taiko Results</a> (yukicoder contest 439 (2024-08-02) - G問題、diff <font color="orange">2729</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題、diff <font color="orange">2658</font>)

　
<h2 id="多倍長整数">457. 多倍長整数</h2>

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

　
<h2 id="メビウスの反転公式">458. メビウスの反転公式</h2>

### 難易度統計

「メビウスの反転公式」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.3／diff <font color="orange">2706</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★3.5／diff <font color="red">2906</font>
- 2022年: ★3／diff <font color="yellowgreen">2306</font>

### レベル別問題一覧

「メビウスの反転公式」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題、diff <font color="yellowgreen">2306</font>)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題、diff <font color="red">3018</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="約数メビウス変換">459. 約数メビウス変換</h2>

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

　
<h2 id="区間等差数列max・min更新">460. 区間等差数列max・min更新</h2>

### 難易度統計

「区間等差数列max・min更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="yellowgreen">2117</font>
- 2024年: ★3.5／diff <font color="yellowgreen">2117</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間等差数列max・min更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2690">No.2690 A present from B (Hard)</a> (単発出題、diffデータなし)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2657">No.2657 Falling Block Game</a> (yukicoder contest 419 (2024-03-01) - C問題、diff <font color="yellowgreen">2117</font>)

　
<h2 id="シュトルツ・チェザロの定理">461. シュトルツ・チェザロの定理</h2>

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

　
<h2 id="移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着">462. 移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着</h2>

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

　
<h2 id="整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着">463. 整礎な操作の試行回数の期待値を各状態への到達確率の和に帰着</h2>

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

　
<h2 id="操作の纏め上げ">464. 操作の纏め上げ</h2>

### 難易度統計

「操作の纏め上げ」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="yellowgreen">2364</font>
- 2024年: ★3.5／diff <font color="yellowgreen">2364</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「操作の纏め上げ」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2809">No.2809 Sort Query</a> (yukicoder contest 436 ('09 Contest 002 day1) (2024-07-12) - G問題、diff <font color="yellowgreen">2364</font>)

　
<h2 id="テイラー展開">465. テイラー展開</h2>

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

　
<h2 id="積分漸化式">466. 積分漸化式</h2>

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

　
<h2 id="高速ゼータ変換">467. 高速ゼータ変換</h2>

### 難易度統計

「高速ゼータ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2413</font>
- 2024年: ★3／diff <font color="yellowgreen">2031</font>
- 2023年: ★4／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「高速ゼータ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2686">No.2686 商品券の使い道</a> (yukicoder contest 422 (第１回 競技プログラミング講習会作問企画コンテスト) (2024-03-20) - H問題、diff <font color="yellowgreen">2031</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2578">No.2578 Jewelry Store</a> (Advent Calendar Contest 2023 (2023-12-01) - F問題、diff <font color="orange">2795</font>)

　
<h2 id="掃き出し法による行列式計算">468. 掃き出し法による行列式計算</h2>

### 難易度統計

「掃き出し法による行列式計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2421</font>
- 2024年: ★3.5／diff <font color="orange">2421</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「掃き出し法による行列式計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

　
<h2 id="冪乗との最大公約数の収束">469. 冪乗との最大公約数の収束</h2>

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

　
<h2 id="第二種スターリング数計算">470. 第二種スターリング数計算</h2>

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

　
<h2 id="カタラン数計算">471. カタラン数計算</h2>

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

　
<h2 id="桁DP">472. 桁DP</h2>

### 難易度統計

「桁DP」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2657</font>
- 2024年: ★3／diff <font color="blue">1925</font>
- 2023年: ★3.7／diff <font color="orange">2792</font>
- 2022年: ★3.5／diff <font color="orange">2722</font>

### レベル別問題一覧

「桁DP」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題、diff <font color="yellowgreen">2047</font>)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2388">No.2388 At Least K-Characters</a> (yukicoder contest 398 (2023-07-21) - D問題、diff <font color="yellowgreen">2282</font>)
- <a href="https://yukicoder.me/problems/no/2772">No.2772 Appearing Even Times</a> (yukicoder contest 431 (2024-05-31) - H問題、diff <font color="blue">1925</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題、diff <font color="orange">2737</font>)
- <a href="https://yukicoder.me/problems/no/2483">No.2483 Yet Another Increasing XOR Problem</a> (yukicoder contest 405 技術室奥プログラミングコンテスト#7 Day1 (2023-09-22) - E問題、diff <font color="orange">2798</font>)
- <a href="https://yukicoder.me/problems/no/2487">No.2487 Multiple of M</a> (yukicoder contest 406 技術室奥プログラミングコンテスト#7 Day2 (2023-09-29) - B問題、diff <font color="orange">2587</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2159">No.2159 Filling 4x4 array</a> (Advent Calendar Contest 2022 (2022-12-01) - J問題、diff <font color="darkgoldenrod ">3382</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2589">No.2589 Prepare Integers</a> (Advent Calendar Contest 2023 (2023-12-01) - Q問題、diff <font color="darkgoldenrod ">3503</font>)

　
<h2 id="リュカの定理">473. リュカの定理</h2>

### 難易度統計

「リュカの定理」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.5／diff <font color="orange">2722</font>
- 2024年: ★3／diff <font color="orange">2676</font>
- 2023年: ★4／diff <font color="orange">2768</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「リュカの定理」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2814">No.2814 Block Game</a> (yukicoder contest 437 ('09 Contest 002 day2)  (2024-07-19) - D問題、diff <font color="orange">2676</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2344">No.2344 (l+r)^2</a> (yukicoder contest 392 (2023-06-09) - B問題、diff <font color="orange">2768</font>)

　
<h2 id="階数因数分解">474. 階数因数分解</h2>

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

　
<h2 id="cyclic orderつき全方位木DP">475. cyclic orderつき全方位木DP</h2>

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

　
<h2 id="行列式計算">476. 行列式計算</h2>

### 難易度統計

「行列式計算」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.6／diff <font color="orange">2461</font>
- 2024年: ★3.5／diff <font color="orange">2421</font>
- 2023年: ★4／diff <font color="orange">2539</font>
- 2022年: ★3／diff <font color="yellowgreen">2344</font>

### レベル別問題一覧

「行列式計算」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2152">No.2152 [Cherry Anniversary 2]  19 Petals of Cherry</a> (Advent Calendar Contest 2022 (2022-12-01) - I問題、diff <font color="yellowgreen">2344</font>)
- <a href="https://yukicoder.me/problems/no/2520">No.2520 L1 Explosion</a> (yukicoder contest 410 (2023-10-27) - F問題、diff <font color="yellowgreen">2284</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2727">No.2727 Tetrahedron Game</a> (yukicoder contest 427 (ゲーム問題コンテスト) (2024-04-12) - G問題、diff <font color="orange">2421</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="有向辺反転">477. 有向辺反転</h2>

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

　
<h2 id="強連結成分分解">478. 強連結成分分解</h2>

### 難易度統計

「強連結成分分解」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.7／diff <font color="orange">2462</font>
- 2024年: ★2.5／diff <font color="deepskyblue">1542</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「強連結成分分解」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2780">No.2780 The Bottle Imp</a> (yukicoder contest 432 (2024-06-07) - H問題、diff <font color="deepskyblue">1542</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2160">No.2160 みたりのDominator</a> (Advent Calendar Contest 2022 (2022-12-01) - K問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="遅延セグメント木">479. 遅延セグメント木</h2>

### 難易度統計

「遅延セグメント木」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.7／diff <font color="orange">2741</font>
- 2024年: ★3／diff <font color="yellowgreen">2100</font>
- 2023年: ★データなし／diffデータなし
- 2022年: ★4.5／diff <font color="darkgoldenrod ">3382</font>

### レベル別問題一覧

「遅延セグメント木」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2697">No.2697 Range LIS Query</a> (yukicoder contest 423 (Asakatsu Presents 3) (2024-03-22) - G問題、diff <font color="yellowgreen">2100</font>)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題、diff <font color="darkgoldenrod ">3382</font>)

　
<h2 id="バケット分割">480. バケット分割</h2>

### 難易度統計

「バケット分割」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.8／diff <font color="orange">2655</font>
- 2024年: ★3／diff <font color="yellowgreen">2004</font>
- 2023年: ★3.7／diff <font color="orange">2519</font>
- 2022年: ★5／diff <font color="darkgoldenrod ">3577</font>

### レベル別問題一覧

「バケット分割」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2652">No.2652 [Cherry 6th Tune N] Δρονε χιρχλινγ</a> (yukicoder contest 418 (Re: start!) (2024-02-23) - F問題、diff <font color="yellowgreen">2004</font>)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題、diff <font color="yellowgreen">2381</font>)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2215">No.2215 Slide Subset Sum</a> (yukicoder contest 376 (2023-02-10) - H問題、diff <font color="orange">2658</font>)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題、diff <font color="darkgoldenrod ">3577</font>)

　
<h2 id="剰余の定理">481. 剰余の定理</h2>

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

　
<h2 id="行列の階段化">482. 行列の階段化</h2>

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

　
<h2 id="掃き出し法">483. 掃き出し法</h2>

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

　
<h2 id="畳み込み">484. 畳み込み</h2>

### 難易度統計

「畳み込み」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★3.9／diff <font color="orange">2784</font>
- 2024年: ★3／diff <font color="yellowgreen">2209</font>
- 2023年: ★4.5／diff <font color="red">2997</font>
- 2022年: ★3.8／diff <font color="red">2934</font>

### レベル別問題一覧

「畳み込み」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題、diff <font color="orange">2673</font>)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題、diff <font color="yellowgreen">2258</font>)
- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)
- <a href="https://yukicoder.me/problems/no/2839">No.2839 AND Constraint</a> (yukicoder contest 440 (2024-08-09) - E問題、diff <font color="orange">2648</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

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

　
<h2 id="小さい法に帰着させる再帰">485. 小さい法に帰着させる再帰</h2>

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

　
<h2 id="高速フーリエ変換">486. 高速フーリエ変換</h2>

### 難易度統計

「高速フーリエ変換」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★4／diff <font color="orange">2796</font>
- 2024年: ★3／diff <font color="blue">1989</font>
- 2023年: ★4.5／diff <font color="red">2997</font>
- 2022年: ★3.8／diff <font color="red">2934</font>

### レベル別問題一覧

「高速フーリエ変換」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題、diff <font color="orange">2673</font>)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題、diff <font color="yellowgreen">2258</font>)
- <a href="https://yukicoder.me/problems/no/2770">No.2770 Coupon Optimization</a> (yukicoder contest 431 (2024-05-31) - F問題、diff <font color="blue">1849</font>)
- <a href="https://yukicoder.me/problems/no/2966">No.2966 Simple Plus Minus Problem</a> (yukicoder contest 453 (2024-11-16) - G問題、diff <font color="yellowgreen">2130</font>)

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

　
<h2 id="データ構造をマージする一般的なテク">487. データ構造をマージする一般的なテク</h2>

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

　
<h2 id="演算の反復の分割統治">488. 演算の反復の分割統治</h2>

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

　
<h2 id="ファウルハーバーの公式">489. ファウルハーバーの公式</h2>

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

　
<h2 id="parallel tree contraction">490. parallel tree contraction</h2>

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

　
<h2 id="演算の適用を１次式の合成に翻訳">491. 演算の適用を１次式の合成に翻訳</h2>

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

　
<h2 id="構文解析">492. 構文解析</h2>

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

　
<h2 id="重軽分解">493. 重軽分解</h2>

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

　
<h2 id="区間二次形式取得">494. 区間二次形式取得</h2>

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

　
<h2 id="区間二次式取得">495. 区間二次式取得</h2>

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

　
<h2 id="Polynomial Taylor shift">496. Polynomial Taylor shift</h2>

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

　
<h2 id="Lindstrom-Gessel-Viennotの補題">497. Lindstrom-Gessel-Viennotの補題</h2>

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

　
<h2 id="ファンデルモンドの行列式計算">498. ファンデルモンドの行列式計算</h2>

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

　
<h2 id="差積計算">499. 差積計算</h2>

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

　
<h2 id="半標準ヤングタブローとGelfand-Tsetlinパターンの対応">500. 半標準ヤングタブローとGelfand-Tsetlinパターンの対応</h2>

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

　
<h2 id="半標準ヤングタブローと非交差経路の対応">501. 半標準ヤングタブローと非交差経路の対応</h2>

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

　
<h2 id="半標準ヤングタブローに翻訳">502. 半標準ヤングタブローに翻訳</h2>

### 難易度統計

「半標準ヤングタブローに翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="orange">2795</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「半標準ヤングタブローに翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="微分計算">503. 微分計算</h2>

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

　
<h2 id="ヤング図形に翻訳">504. ヤング図形に翻訳</h2>

### 難易度統計

「ヤング図形に翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">2940</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★5／diff <font color="orange">2795</font>
- 2022年: ★5／diff <font color="red">3086</font>

### レベル別問題一覧

「ヤング図形に翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)
- <a href="https://yukicoder.me/problems/no/2556">No.2556 Increasing Matrix</a> (Advent Calendar Contest 2023 (2023-12-01) - B問題、diff <font color="orange">2795</font>)

　
<h2 id="フック長公式">505. フック長公式</h2>

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

　
<h2 id="標準ヤングタブローに翻訳">506. 標準ヤングタブローに翻訳</h2>

### 難易度統計

「標準ヤングタブローに翻訳」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★5／diff <font color="red">3086</font>
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★5／diff <font color="red">3086</font>

### レベル別問題一覧

「標準ヤングタブローに翻訳」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2149">No.2149 Vanitas Vanitatum</a> (Advent Calendar Contest 2022 (2022-12-01) - F問題、diff <font color="red">3086</font>)

　
<h2 id="多点評価">507. 多点評価</h2>

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

　
<h2 id="Bostan-Mori法">508. Bostan-Mori法</h2>

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

　
<h2 id="巡回畳み込み">509. 巡回畳み込み</h2>

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

　
<h2 id="多項式のユークリッドの互除法">510. 多項式のユークリッドの互除法</h2>

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

　
<h2 id="多項式を法とする逆元計算">511. 多項式を法とする逆元計算</h2>

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

　
<h2 id="単位の分解">512. 単位の分解</h2>

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

　
<h2 id="一次分数変換">513. 一次分数変換</h2>

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

　
<h2 id="一次分数変換と対数関数による変数変換の合成">514. 一次分数変換と対数関数による変数変換の合成</h2>

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

　
<h2 id="指数関数による変数変換と一次分数変換の合成">515. 指数関数による変数変換と一次分数変換の合成</h2>

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

　
<h2 id="微分作用素を変数変換で簡易化">516. 微分作用素を変数変換で簡易化</h2>

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

　
<h2 id="部分積分">517. 部分積分</h2>

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

　
<h2 id="残余ネットワーク">518. 残余ネットワーク</h2>

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

　
<h2 id="非負整数をB進法でベクトルに翻訳">519. 非負整数をB進法でベクトルに翻訳</h2>

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

　
<h2 id="P-再帰">520. P-再帰</h2>

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

　
<h2 id="評価点シフト">521. 評価点シフト</h2>

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

　
<h2 id="区間等差数列加算更新">522. 区間等差数列加算更新</h2>

### 難易度統計

「区間等差数列加算更新」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★データなし／diffデータなし
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「区間等差数列加算更新」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2662">No.2662 Installing Cell Towers</a> (単発出題、diffデータなし)

　
<h2 id="高階差分">523. 高階差分</h2>

### 難易度統計

「高階差分」を主たる解法に含む問題の難易度統計（コンテスト平均レベル／コンテスト平均difficulty）です。
- 全体: ★データなし／diffデータなし
- 2024年: ★データなし／diffデータなし
- 2023年: ★データなし／diffデータなし
- 2022年: ★データなし／diffデータなし

### レベル別問題一覧

「高階差分」を主たる解法に含む問題のレベルごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2662">No.2662 Installing Cell Towers</a> (単発出題、diffデータなし)

