---
url: https://p-adic.github.io/yukicoder-writer-statistics
layout: project
title: yukicoder過去問writer別統計
date: 2025-07-26
excerpt: "yukicoderの過去問のwriter別の難易度に関する統計データです。"
parent: competitive-programming-project
prev-child: yukicoder-difficulty-statistics-solution-name
next-child: 
project: true
image-directory: competitive-programming
tags: [競技プログラミング,数学]
---

yukicoder contest 358 (2022-08-26) 以降に出題されたyuicoderの問題をwriter別に分析しました。具体的には

- writer想定レベル（★の数）と実際の難易度（difficulty）の組み合わせ
- （筆者がupsolveして解法を登録した問題に絞った上で）各解法が問われた（非想定解も含む）回数

を集計しました。


## 集計方法

データ取得元、集計方法、集計の進捗状況などは[yukicode過去問解法別難易度統計]({{ site.url }}/yukicoder-difficulty-statistics)に準じます。そちらの注意点もご参照ください。同ページの[writer想定レベルごとに算出した実際の難易度の平均値]({{ site.url }}/yukicoder-difficulty-statistics#average_difficulty)も比較用に合わせてご利用ください。


### 特殊な文字の表記

writer名は基本的に登録名をそのまま表記していますが、例外として

- [(微生物の絵文字)みどりむしさん](https://yukicoder.me/users/19141)
- [Nauclhlt(蓮の花の絵文字)さん](https://yukicoder.me/users/21654)

はこちらの自動化処理環境の都合

- みどりむしさん
- Nauclhltさん

と記載させていただきます。


## [nmnmnmnmnmnmnmさん](https://yukicoder.me/users/25)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="green">938</font>](https://yukicoder.me/problems/no/2194)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問


## [snukeさん](https://yukicoder.me/users/75)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★5／diff <font color="darkgoldenrod ">3257</font>](https://yukicoder.me/problems/no/2151)

### 過去問の解法頻度

- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [彩色の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#彩色の構築) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問


## [startcppさん](https://yukicoder.me/users/108)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="gray">365</font>](https://yukicoder.me/problems/no/2614)
- [★2／diff <font color="green">958</font>](https://yukicoder.me/problems/no/2615)
- [★3／diff <font color="yellowgreen">2143</font>](https://yukicoder.me/problems/no/2616)
- [★3／diff <font color="yellowgreen">2255</font>](https://yukicoder.me/problems/no/2618)
- [★3／diff <font color="yellowgreen">2349</font>](https://yukicoder.me/problems/no/2619)
- [★3／diff <font color="orange">2491</font>](https://yukicoder.me/problems/no/2617)
- [★3.5／diff <font color="red">2862</font>](https://yukicoder.me/problems/no/2620)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 2問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 2問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [グラフの頂点の次数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの頂点の次数計算) × 1問
- [サンプルに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルに帰着) × 1問
- [ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニム和) × 1問
- [ファンデルモンドの畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#ファンデルモンドの畳み込み) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#高さ奇数ニム和) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [制約からグラフの種類を特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#制約からグラフの種類を特定) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [二・多項係数を組み合わせに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#二・多項係数を組み合わせに翻訳) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量を保つ戦略) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [文字列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列の構築) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [tailsさん](https://yukicoder.me/users/385)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="yellowgreen">2246</font>](https://yukicoder.me/problems/no/2147)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰的構造に沿った再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構造に沿った再帰) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [akakimidoriさん](https://yukicoder.me/users/437)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4.5／diff <font color="red">3103</font>](https://yukicoder.me/problems/no/2580)
- [★4.5／diff <font color="darkgoldenrod ">3382</font>](https://yukicoder.me/problems/no/2163)
- [★5／diff <font color="red">3115</font>](https://yukicoder.me/problems/no/2990)
- [★5／diff <font color="red">3196</font>](https://yukicoder.me/problems/no/2587)

### 過去問の解法頻度

- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 2問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 2問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [Polynomial Taylor shift](https://p-adic.github.io/yukicoder-difficulty-statistics/#Polynomial Taylor shift) × 1問
- [XOR畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#XOR畳み込み) × 1問
- [グロタンディーク化](https://p-adic.github.io/yukicoder-difficulty-statistics/#グロタンディーク化) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ファウルハーバーの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ファウルハーバーの公式) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間多項式和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間多項式和取得) × 1問
- [高速アダマール逆変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速アダマール逆変換) × 1問
- [高速アダマール変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速アダマール変換) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [重軽分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#重軽分解) × 1問
- [遅延セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#遅延セグメント木) × 1問
- [低次項の追加による線形化](https://p-adic.github.io/yukicoder-difficulty-statistics/#低次項の追加による線形化) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [配列をセグ木状に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列をセグ木状に分割して管理) × 1問


## [testestestさん](https://yukicoder.me/users/939)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4／diff <font color="orange">2567</font>](https://yukicoder.me/problems/no/2207)
- [★4／diff <font color="red">2885</font>](https://yukicoder.me/problems/no/2979)
- [★4.5／diff <font color="darkgoldenrod ">3309</font>](https://yukicoder.me/problems/no/2996)

### 過去問の解法頻度

- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [ディオファントス方程式の解の数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の数え上げ) × 1問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 1問
- [ピタゴラス数数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ピタゴラス数数え上げ) × 1問
- [ファウルハーバーの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ファウルハーバーの公式) × 1問
- [メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウス変換) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [奇数条件を緩和して$2$冪で包除](https://p-adic.github.io/yukicoder-difficulty-statistics/#奇数条件を緩和して$2$冪で包除) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [原始ピタゴラス数木](https://p-adic.github.io/yukicoder-difficulty-statistics/#原始ピタゴラス数木) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [最小素因数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小素因数計算) × 1問
- [十分大きな法で計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#十分大きな法で計算) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [商のfloorの値ごとに纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの値ごとに纏め上げ) × 1問
- [商のfloorの分子を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの分子を止める総和計算) × 1問
- [商のfloorの分母を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの分母を止める総和計算) × 1問
- [剰余による確率的判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余による確率的判定) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [凸集合の格子点数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸集合の格子点数え上げ) × 1問
- [二項定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項定理) × 1問
- [倍数メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数メビウス変換) × 1問
- [非単射関数の値で纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の値で纏め上げ) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [平方分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方分割) × 1問
- [約数の走査を倍数の走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の走査を倍数の走査に帰着) × 1問
- [約数包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数包除原理) × 1問


## [addeight2さん](https://yukicoder.me/users/2329)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diffデータなし](https://yukicoder.me/problems/no/3001)

### 過去問の解法頻度

- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [周期性判定を長さの素因数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性判定を長さの素因数に帰着) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素数逆数和を用いた計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数逆数和を用いた計算量評価) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問


## [cleanttedさん](https://yukicoder.me/users/2340)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1376</font>](https://yukicoder.me/problems/no/2387)

### 過去問の解法頻度

- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問


## [Nafmo2さん](https://yukicoder.me/users/3130)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">159</font>](https://yukicoder.me/problems/no/2706)
- [★1／diff <font color="gray">188</font>](https://yukicoder.me/problems/no/2414)
- [★1／diff <font color="gray">188</font>](https://yukicoder.me/problems/no/2415)
- [★1／diff <font color="gray">217</font>](https://yukicoder.me/problems/no/2707)
- [★1／diff <font color="gray">219</font>](https://yukicoder.me/problems/no/2322)
- [★1.5／diff <font color="gray">385</font>](https://yukicoder.me/problems/no/2323)
- [★1.5／diff <font color="brown">736</font>](https://yukicoder.me/problems/no/2708)
- [★1.5／diff <font color="green">990</font>](https://yukicoder.me/problems/no/2710)
- [★2／diff <font color="brown">691</font>](https://yukicoder.me/problems/no/2418)
- [★2／diff <font color="green">1143</font>](https://yukicoder.me/problems/no/2709)
- [★2／diff <font color="deepskyblue">1228</font>](https://yukicoder.me/problems/no/2420)
- [★2／diff <font color="deepskyblue">1396</font>](https://yukicoder.me/problems/no/2711)
- [★2.5／diff <font color="blue">1749</font>](https://yukicoder.me/problems/no/2712)
- [★2.5／diff <font color="blue">1774</font>](https://yukicoder.me/problems/no/2329)
- [★3／diff <font color="blue">1959</font>](https://yukicoder.me/problems/no/2713)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 4問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 3問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 3問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 3問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 2問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 2問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [符号なし64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#符号なし64bit整数) × 2問
- [01列とグリッド上の経路の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列とグリッド上の経路の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [lower_bound・upper_bound取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#lower_bound・upper_bound取得) × 1問
- [★1の64bit整数要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1の64bit整数要求) × 1問
- [４重以上のループ](https://p-adic.github.io/yukicoder-difficulty-statistics/#４重以上のループ) × 1問
- [オーバーフロー回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#オーバーフロー回避) × 1問
- [コストなしナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#コストなしナップサック最適化) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [フロー](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロー) × 1問
- [ベルマン・フォード法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ベルマン・フォード法) × 1問
- [位取り記法表示・桁和を用いた倍数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示・桁和を用いた倍数判定) × 1問
- [価値上限ありナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#価値上限ありナップサック最適化) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間要素数取得を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得を指定始切片数え上げに帰着) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [経路全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路全探索) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰による多重ループ実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰による多重ループ実装) × 1問
- [最小カット計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小カット計算) × 1問
- [最大流計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大流計算) × 1問
- [最大流最小カット定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大流最小カット定理) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [重複選択可ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック最適化) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [切り上げ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#切り上げ計算) × 1問
- [選択組み合わせ報酬付きナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択組み合わせ報酬付きナップサック最適化) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [超頂点追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#超頂点追加) × 1問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [半分全列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#半分全列挙) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [符号なし64bit整数によるオーバーフロー回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#符号なし64bit整数によるオーバーフロー回避) × 1問
- [負閉路検出](https://p-adic.github.io/yukicoder-difficulty-statistics/#負閉路検出) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [閉路検出](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉路検出) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [butsurizukiさん](https://yukicoder.me/users/4323)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1545</font>](https://yukicoder.me/problems/no/3159)

### 過去問の解法頻度

- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [数列・配列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#数列・配列の構築) × 1問
- [素数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列挙) × 1問


## [ei1333333さん](https://yukicoder.me/users/4746)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="yellowgreen">2246</font>](https://yukicoder.me/problems/no/2148)

### 過去問の解法頻度

- [ウノ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#ウノ計算) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問


## [tatyamさん](https://yukicoder.me/users/5232)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="darkgoldenrod ">3386</font>](https://yukicoder.me/problems/no/2632)
- [★4.5／diff <font color="red">3115</font>](https://yukicoder.me/problems/no/2988)

### 過去問の解法頻度

- [SMAWKアルゴリズム](https://p-adic.github.io/yukicoder-difficulty-statistics/#SMAWKアルゴリズム) × 1問
- [monge性](https://p-adic.github.io/yukicoder-difficulty-statistics/#monge性) × 1問
- [monotone minima](https://p-adic.github.io/yukicoder-difficulty-statistics/#monotone minima) × 1問
- [totally monotonic性](https://p-adic.github.io/yukicoder-difficulty-statistics/#totally monotonic性) × 1問
- [２変数関数の１変数を固定した最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数関数の１変数を固定した最大・最小値計算) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [凸最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸最適化) × 1問
- [配列をセグ木状に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列をセグ木状に分割して管理) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問


## [p-adic](https://yukicoder.me/users/5376)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">229</font>](https://yukicoder.me/problems/no/2392)
- [★1／diff <font color="gray">371</font>](https://yukicoder.me/problems/no/2533)
- [★1／diff <font color="brown">708</font>](https://yukicoder.me/problems/no/2781)
- [★1／diff <font color="brown">730</font>](https://yukicoder.me/problems/no/2184)
- [★1／diff <font color="green">987</font>](https://yukicoder.me/problems/no/2088)
- [★1.5／diff <font color="gray">152</font>](https://yukicoder.me/problems/no/2441)
- [★1.5／diff <font color="gray">165</font>](https://yukicoder.me/problems/no/2086)
- [★1.5／diff <font color="brown">526</font>](https://yukicoder.me/problems/no/2117)
- [★1.5／diff <font color="brown">596</font>](https://yukicoder.me/problems/no/2087)
- [★1.5／diff <font color="brown">610</font>](https://yukicoder.me/problems/no/2534)
- [★1.5／diff <font color="brown">671</font>](https://yukicoder.me/problems/no/2969)
- [★1.5／diff <font color="brown">708</font>](https://yukicoder.me/problems/no/2782)
- [★1.5／diff <font color="green">1011</font>](https://yukicoder.me/problems/no/2186)
- [★1.5／diff <font color="green">1069</font>](https://yukicoder.me/problems/no/2185)
- [★1.5／diff <font color="deepskyblue">1258</font>](https://yukicoder.me/problems/no/2267)
- [★1.5／diff <font color="deepskyblue">1306</font>](https://yukicoder.me/problems/no/2268)
- [★1.5／diff <font color="deepskyblue">1343</font>](https://yukicoder.me/problems/no/2118)
- [★1.5／diff <font color="deepskyblue">1351</font>](https://yukicoder.me/problems/no/2749)
- [★1.5／diff <font color="deepskyblue">1464</font>](https://yukicoder.me/problems/no/3133)
- [★2／diff <font color="deepskyblue">1228</font>](https://yukicoder.me/problems/no/2130)
- [★2／diff <font color="deepskyblue">1242</font>](https://yukicoder.me/problems/no/2910)
- [★2／diff <font color="deepskyblue">1325</font>](https://yukicoder.me/problems/no/2089)
- [★2／diff <font color="deepskyblue">1345</font>](https://yukicoder.me/problems/no/2970)
- [★2／diff <font color="deepskyblue">1358</font>](https://yukicoder.me/problems/no/2090)
- [★2／diff <font color="deepskyblue">1402</font>](https://yukicoder.me/problems/no/2752)
- [★2／diff <font color="deepskyblue">1442</font>](https://yukicoder.me/problems/no/2394)
- [★2／diff <font color="deepskyblue">1484</font>](https://yukicoder.me/problems/no/2971)
- [★2／diff <font color="deepskyblue">1506</font>](https://yukicoder.me/problems/no/2535)
- [★2／diff <font color="deepskyblue">1567</font>](https://yukicoder.me/problems/no/2911)
- [★2／diff <font color="blue">1673</font>](https://yukicoder.me/problems/no/2785)
- [★2／diff <font color="blue">1767</font>](https://yukicoder.me/problems/no/2784)
- [★2／diff <font color="yellowgreen">2034</font>](https://yukicoder.me/problems/no/2269)
- [★2／diff <font color="yellowgreen">2115</font>](https://yukicoder.me/problems/no/2187)
- [★2／diff <font color="yellowgreen">2148</font>](https://yukicoder.me/problems/no/2188)
- [★2.5／diff <font color="deepskyblue">1429</font>](https://yukicoder.me/problems/no/2912)
- [★2.5／diff <font color="deepskyblue">1567</font>](https://yukicoder.me/problems/no/2913)
- [★2.5／diff <font color="deepskyblue">1598</font>](https://yukicoder.me/problems/no/2972)
- [★2.5／diff <font color="blue">1612</font>](https://yukicoder.me/problems/no/2536)
- [★2.5／diff <font color="blue">1714</font>](https://yukicoder.me/problems/no/2442)
- [★2.5／diff <font color="blue">1828</font>](https://yukicoder.me/problems/no/2119)
- [★2.5／diff <font color="blue">1854</font>](https://yukicoder.me/problems/no/2753)
- [★2.5／diff <font color="blue">1957</font>](https://yukicoder.me/problems/no/2897)
- [★2.5／diff <font color="blue">1969</font>](https://yukicoder.me/problems/no/2443)
- [★2.5／diff <font color="yellowgreen">2021</font>](https://yukicoder.me/problems/no/2537)
- [★2.5／diff <font color="yellowgreen">2066</font>](https://yukicoder.me/problems/no/2270)
- [★2.5／diff <font color="yellowgreen">2339</font>](https://yukicoder.me/problems/no/2189)
- [★2.5／diff <font color="orange">2788</font>](https://yukicoder.me/problems/no/2271)
- [★3／diff <font color="blue">1627</font>](https://yukicoder.me/problems/no/2395)
- [★3／diff <font color="blue">1932</font>](https://yukicoder.me/problems/no/3024)
- [★3／diff <font color="yellowgreen">2051</font>](https://yukicoder.me/problems/no/3022)
- [★3／diff <font color="yellowgreen">2076</font>](https://yukicoder.me/problems/no/2916)
- [★3／diff <font color="yellowgreen">2187</font>](https://yukicoder.me/problems/no/2914)
- [★3／diff <font color="yellowgreen">2321</font>](https://yukicoder.me/problems/no/2915)
- [★3／diff <font color="yellowgreen">2342</font>](https://yukicoder.me/problems/no/2975)
- [★3／diff <font color="yellowgreen">2365</font>](https://yukicoder.me/problems/no/2445)
- [★3／diff <font color="yellowgreen">2385</font>](https://yukicoder.me/problems/no/2191)
- [★3／diff <font color="orange">2436</font>](https://yukicoder.me/problems/no/2538)
- [★3／diff <font color="orange">2513</font>](https://yukicoder.me/problems/no/2272)
- [★3／diff <font color="orange">2545</font>](https://yukicoder.me/problems/no/2190)
- [★3／diff <font color="orange">2609</font>](https://yukicoder.me/problems/no/2444)
- [★3／diff <font color="orange">2698</font>](https://yukicoder.me/problems/no/2755)
- [★3／diff <font color="red">2831</font>](https://yukicoder.me/problems/no/2787)
- [★3.5／diff <font color="blue">1940</font>](https://yukicoder.me/problems/no/2120)
- [★3.5／diff <font color="yellowgreen">2326</font>](https://yukicoder.me/problems/no/2121)
- [★3.5／diff <font color="orange">2556</font>](https://yukicoder.me/problems/no/2122)
- [★3.5／diff <font color="orange">2567</font>](https://yukicoder.me/problems/no/2973)
- [★3.5／diff <font color="orange">2708</font>](https://yukicoder.me/problems/no/2273)
- [★3.5／diff <font color="red">3014</font>](https://yukicoder.me/problems/no/2539)
- [★3.5／diff <font color="red">3030</font>](https://yukicoder.me/problems/no/2974)
- [★3.5／diff <font color="red">3117</font>](https://yukicoder.me/problems/no/2192)
- [★3.5／diff <font color="darkgoldenrod ">3217</font>](https://yukicoder.me/problems/no/2540)
- [★4／diff <font color="orange">2609</font>](https://yukicoder.me/problems/no/2446)
- [★4／diff <font color="orange">2660</font>](https://yukicoder.me/problems/no/2917)
- [★4／diff <font color="orange">2719</font>](https://yukicoder.me/problems/no/2396)
- [★4／diff <font color="orange">2749</font>](https://yukicoder.me/problems/no/2193)
- [★4／diff <font color="red">2880</font>](https://yukicoder.me/problems/no/2274)
- [★4／diff <font color="red">3030</font>](https://yukicoder.me/problems/no/2976)
- [★4／diff <font color="red">3053</font>](https://yukicoder.me/problems/no/2447)
- [★4／diff <font color="red">3178</font>](https://yukicoder.me/problems/no/2397)
- [★4／diff <font color="red">3185</font>](https://yukicoder.me/problems/no/2448)
- [★4.5／diffデータなし](https://yukicoder.me/problems/no/2993)
- [★5／diff <font color="red">3178</font>](https://yukicoder.me/problems/no/2398)
- [★5／diff <font color="darkgoldenrod ">3577</font>](https://yukicoder.me/problems/no/2168)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 19問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 17問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 15問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 15問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 14問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 11問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 11問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 10問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 10問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 9問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 9問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 9問
- [グロタンディーク化](https://p-adic.github.io/yukicoder-difficulty-statistics/#グロタンディーク化) × 8問
- [テイラー展開](https://p-adic.github.io/yukicoder-difficulty-statistics/#テイラー展開) × 8問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 8問
- [商の反復による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商の反復による付値計算) × 8問
- [中国剰余定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#中国剰余定理) × 8問
- [合成数を法とする数値を零と素因数の冪乗と可逆元に分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成数を法とする数値を零と素因数の冪乗と可逆元に分解) × 7問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 7問
- [遺伝的記法](https://p-adic.github.io/yukicoder-difficulty-statistics/#遺伝的記法) × 6問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 6問
- [整礎性](https://p-adic.github.io/yukicoder-difficulty-statistics/#整礎性) × 6問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 6問
- [平方剰余判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方剰余判定) × 6問
- [breakに関する考察](https://p-adic.github.io/yukicoder-difficulty-statistics/#breakに関する考察) × 5問
- [オーバーフロー回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#オーバーフロー回避) × 5問
- [解の公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#解の公式) × 5問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 5問
- [合成数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成数を法とする逆元計算) × 5問
- [再帰的構造に沿った再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構造に沿った再帰) × 5問
- [順序数に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#順序数に翻訳) × 5問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 5問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 5問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 5問
- [微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分計算) × 5問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 5問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 5問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 4問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 4問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 4問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 4問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 4問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 4問
- [行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列式計算) × 4問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 4問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 4問
- [二項定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項定理) × 4問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 4問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 4問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 4問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 4問
- [Garnerのアルゴリズム](https://p-adic.github.io/yukicoder-difficulty-statistics/#Garnerのアルゴリズム) × 3問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 3問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 3問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 3問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 3問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 3問
- [外積・サラスの公式による行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積・サラスの公式による行列式計算) × 3問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 3問
- [基底に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#基底に帰着) × 3問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 3問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 3問
- [構文解析](https://p-adic.github.io/yukicoder-difficulty-statistics/#構文解析) × 3問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 3問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 3問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 3問
- [順序数表記](https://p-adic.github.io/yukicoder-difficulty-statistics/#順序数表記) × 3問
- [疎な行列演算の計算結果書き出しによる高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#疎な行列演算の計算結果書き出しによる高速化) × 3問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 3問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 3問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 3問
- [多倍長整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#多倍長整数) × 3問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 3問
- [付値と合同式による平方剰余判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値と合同式による平方剰余判定) × 3問
- [累積積による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による二項係数計算) × 3問
- [bit演算による$64$並列](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit演算による$64$並列) × 2問
- [bool値の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#bool値の充足可能性判定) × 2問
- [４重以上のループ](https://p-adic.github.io/yukicoder-difficulty-statistics/#４重以上のループ) × 2問
- [オイラーの規準](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーの規準) × 2問
- [オイラーの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーの定理) × 2問
- [カントール標準形](https://p-adic.github.io/yukicoder-difficulty-statistics/#カントール標準形) × 2問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 2問
- [グラフの辺の削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の削除更新) × 2問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 2問
- [グランディ数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グランディ数計算) × 2問
- [ド・モルガンの法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#ド・モルガンの法則) × 2問
- [ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニム和) × 2問
- [ホモロジー計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#ホモロジー計算) × 2問
- [ポテンシャル付き素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポテンシャル付き素集合データ構造) × 2問
- [ラプラスの展開公式による逆行列計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#ラプラスの展開公式による逆行列計算) × 2問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 2問
- [一対一対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#一対一対応) × 2問
- [因数分解による素因数分解・付値計算の分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#因数分解による素因数分解・付値計算の分割統治) × 2問
- [階数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階数計算) × 2問
- [基底計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#基底計算) × 2問
- [基本列](https://p-adic.github.io/yukicoder-difficulty-statistics/#基本列) × 2問
- [逆行列計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆行列計算) × 2問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 2問
- [区間積取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間積取得) × 2問
- [行列の階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の階段化) × 2問
- [行列の簡約階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の簡約階段化) × 2問
- [行列式と面積・体積の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列式と面積・体積の関係) × 2問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 2問
- [合成数を法とする二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成数を法とする二項係数計算) × 2問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 2問
- [再帰による多重ループ実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰による多重ループ実装) × 2問
- [次元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#次元計算) × 2問
- [次元定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#次元定理) × 2問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 2問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 2問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 2問
- [剰余を取る前に符号や大小を計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余を取る前に符号や大小を計算) × 2問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 2問
- [素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数判定) × 2問
- [掃き出し法](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法) × 2問
- [多変数演算に関する条件を$2$変数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#多変数演算に関する条件を$2$変数に帰着) × 2問
- [低次項の追加による線形化](https://p-adic.github.io/yukicoder-difficulty-statistics/#低次項の追加による線形化) × 2問
- [停止性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#停止性判定) × 2問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 2問
- [到達可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#到達可能性判定) × 2問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [任意mod畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#任意mod畳み込み) × 2問
- [汎関数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#汎関数計算) × 2問
- [部分集合の要素全探索を全体集合の要素全探索に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分集合の要素全探索を全体集合の要素全探索に帰着) × 2問
- [平均値の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平均値の定理) × 2問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 2問
- [平方剰余の相互法則・補充法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方剰余の相互法則・補充法則) × 2問
- [閉路検出](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉路検出) × 2問
- [法B係数連立一次方程式の解の存在判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の存在判定) × 2問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 2問
- [乱択による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択による構築) × 2問
- [累積積](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積) × 2問
- [$1$の原始根計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#$1$の原始根計算) × 1問
- [$\epsilon N$論法](https://p-adic.github.io/yukicoder-difficulty-statistics/#$\epsilon N$論法) × 1問
- [2元集合族の選択関数の像の要素数最大化](https://p-adic.github.io/yukicoder-difficulty-statistics/#2元集合族の選択関数の像の要素数最大化) × 1問
- [2集合間距離計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#2集合間距離計算) × 1問
- [Bostan-Mori法](https://p-adic.github.io/yukicoder-difficulty-statistics/#Bostan-Mori法) × 1問
- [B進法位取り記法と法Bベクトルの対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#B進法位取り記法と法Bベクトルの対応) × 1問
- [OR畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#OR畳み込み) × 1問
- [Toeplitz行列](https://p-adic.github.io/yukicoder-difficulty-statistics/#Toeplitz行列) × 1問
- [bitDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitDP) × 1問
- [bitset高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitset高速化) × 1問
- [functional completeness](https://p-adic.github.io/yukicoder-difficulty-statistics/#functional completeness) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [next DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#next DP) × 1問
- [slope trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#slope trick) × 1問
- [★1の64bit整数要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1の64bit整数要求) × 1問
- [１変数一次方程式・不等式の求解](https://p-adic.github.io/yukicoder-difficulty-statistics/#１変数一次方程式・不等式の求解) × 1問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [エラトステネスの篩による素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩による素数判定) × 1問
- [オイラーの定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーの定理による逆元計算) × 1問
- [カーマイケル関数](https://p-adic.github.io/yukicoder-difficulty-statistics/#カーマイケル関数) × 1問
- [クエリソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリソート) × 1問
- [グラフ・状態の圧縮による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフ・状態の圧縮による次元削減) × 1問
- [グランスキーの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#グランスキーの定理) × 1問
- [ケーリーの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ケーリーの公式) × 1問
- [コーシー・グルサの積分公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#コーシー・グルサの積分公式) × 1問
- [コストなしナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#コストなしナップサック割り当て数え上げ) × 1問
- [サンプルに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルに帰着) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [シュミットの直交化法](https://p-adic.github.io/yukicoder-difficulty-statistics/#シュミットの直交化法) × 1問
- [ジョルダン標準形](https://p-adic.github.io/yukicoder-difficulty-statistics/#ジョルダン標準形) × 1問
- [ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ変換) × 1問
- [ゼロ除算回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼロ除算回避) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ソフィー・ジェルマンの恒等式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソフィー・ジェルマンの恒等式) × 1問
- [ディオファントス方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の構築) × 1問
- [ディオファントス方程式の解の数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の数え上げ) × 1問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 1問
- [ニュートン法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニュートン法) × 1問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 1問
- [ファンデルモンドの畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#ファンデルモンドの畳み込み) × 1問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 1問
- [フロー](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロー) × 1問
- [ブレント・キュングの合成アルゴリズム](https://p-adic.github.io/yukicoder-difficulty-statistics/#ブレント・キュングの合成アルゴリズム) × 1問
- [ベイズの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#ベイズの定理) × 1問
- [ベルマン・フォード法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ベルマン・フォード法) × 1問
- [ポテンシャル付きダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポテンシャル付きダイクストラ法) × 1問
- [ポラードの$\rho$](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポラードの$\rho$) × 1問
- [マーラー変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#マーラー変換) × 1問
- [ミラー・ラビン素数判定法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー・ラビン素数判定法) × 1問
- [メモ化再帰の計算量を再帰深度で評価する考察](https://p-adic.github.io/yukicoder-difficulty-statistics/#メモ化再帰の計算量を再帰深度で評価する考察) × 1問
- [モノイド演算に関する区間更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間更新) × 1問
- [モンテカルロ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#モンテカルロ法) × 1問
- [ラグランジュ・ビューアマンの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ラグランジュ・ビューアマンの公式) × 1問
- [ラグランジュの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#ラグランジュの定理) × 1問
- [ラグランジュの反転公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ラグランジュの反転公式) × 1問
- [ランベルトの$W$関数](https://p-adic.github.io/yukicoder-difficulty-statistics/#ランベルトの$W$関数) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [ルジャンドルの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ルジャンドルの公式) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [ワーシャル・フロイド法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ワーシャル・フロイド法) × 1問
- [ヴェブレン関数](https://p-adic.github.io/yukicoder-difficulty-statistics/#ヴェブレン関数) × 1問
- [解と係数の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#解と係数の関係) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [極限の打ち切り計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#極限の打ち切り計算) × 1問
- [極小互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#極小互換表示) × 1問
- [極値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#極値計算) × 1問
- [極値計算による最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#極値計算による最大・最小値計算) × 1問
- [区間作用更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間作用更新) × 1問
- [区間乗算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間乗算更新) × 1問
- [区間多項式加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間多項式加算更新) × 1問
- [区分求積法](https://p-adic.github.io/yukicoder-difficulty-statistics/#区分求積法) × 1問
- [形式冪級数の逆関数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#形式冪級数の逆関数計算) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [高階差分](https://p-adic.github.io/yukicoder-difficulty-statistics/#高階差分) × 1問
- [高階微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#高階微分計算) × 1問
- [合成関数の微分法](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成関数の微分法) × 1問
- [最大二部マッチング](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大二部マッチング) × 1問
- [三項間漸化式の求解](https://p-adic.github.io/yukicoder-difficulty-statistics/#三項間漸化式の求解) × 1問
- [四元数演算](https://p-adic.github.io/yukicoder-difficulty-statistics/#四元数演算) × 1問
- [四平方定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#四平方定理) × 1問
- [指数と対数による冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#指数と対数による冪乗計算) × 1問
- [自己写像に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#自己写像に翻訳) × 1問
- [自由加群](https://p-adic.github.io/yukicoder-difficulty-statistics/#自由加群) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [集合の要素数による各要素の不一致性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の要素数による各要素の不一致性判定) × 1問
- [集合変数の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合変数の充足可能性判定) × 1問
- [十分大きな法で計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#十分大きな法で計算) × 1問
- [巡回畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回畳み込み) × 1問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 1問
- [商の剰余計算を大きい法に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#商の剰余計算を大きい法に帰着) × 1問
- [小さい法に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さい法に帰着) × 1問
- [証明をなぞる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#証明をなぞる構築) × 1問
- [剰余による確率的判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余による確率的判定) × 1問
- [真理値表](https://p-adic.github.io/yukicoder-difficulty-statistics/#真理値表) × 1問
- [整数のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#整数のリアクティブによる特定) × 1問
- [整数の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#整数の構築) × 1問
- [線形空間の数え上げを次元計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形空間の数え上げを次元計算に帰着) × 1問
- [遷移の収束](https://p-adic.github.io/yukicoder-difficulty-statistics/#遷移の収束) × 1問
- [全要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#全要素数取得) × 1問
- [素因数分解による素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による素数判定) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [素数計数関数前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数計数関数前計算) × 1問
- [組合せ論的種](https://p-adic.github.io/yukicoder-difficulty-statistics/#組合せ論的種) × 1問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 1問
- [多次元コストを一次元に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元コストを一次元に翻訳) × 1問
- [対角化](https://p-adic.github.io/yukicoder-difficulty-statistics/#対角化) × 1問
- [対角線論法](https://p-adic.github.io/yukicoder-difficulty-statistics/#対角線論法) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [代数拡大](https://p-adic.github.io/yukicoder-difficulty-statistics/#代数拡大) × 1問
- [第二種チェビシェフ多項式](https://p-adic.github.io/yukicoder-difficulty-statistics/#第二種チェビシェフ多項式) × 1問
- [単位の分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#単位の分解) × 1問
- [探索・求解アルゴリズムによる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#探索・求解アルゴリズムによる構築) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [置換の合成](https://p-adic.github.io/yukicoder-difficulty-statistics/#置換の合成) × 1問
- [置換の符号計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#置換の符号計算) × 1問
- [中間値の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#中間値の定理) × 1問
- [超頂点追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#超頂点追加) × 1問
- [頂点倍化](https://p-adic.github.io/yukicoder-difficulty-statistics/#頂点倍化) × 1問
- [転倒数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#転倒数計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [同値関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#同値関係) × 1問
- [二部グラフ判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#二部グラフ判定) × 1問
- [二分法](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分法) × 1問
- [任意・存在を総AND・ORに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#任意・存在を総AND・ORに翻訳) × 1問
- [半分全列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#半分全列挙) × 1問
- [非結合的マグマ演算に関する区間更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#非結合的マグマ演算に関する区間更新) × 1問
- [非結合的マグマ演算を自己写像に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#非結合的マグマ演算を自己写像に翻訳) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [符号なし64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#符号なし64bit整数) × 1問
- [負閉路検出](https://p-adic.github.io/yukicoder-difficulty-statistics/#負閉路検出) × 1問
- [部分集合対全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分集合対全探索) × 1問
- [部分分数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分分数分解) × 1問
- [複素数演算](https://p-adic.github.io/yukicoder-difficulty-statistics/#複素数演算) × 1問
- [文字列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列の構築) × 1問
- [平方数前計算による平方剰余判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方数前計算による平方剰余判定) × 1問
- [平方分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方分割) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [法B係数連立一次方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の構築) × 1問
- [法B係数連立一次方程式の解の数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の数え上げ) × 1問
- [埋め込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#埋め込み) × 1問
- [有理数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#有理数型) × 1問
- [余因子展開](https://p-adic.github.io/yukicoder-difficulty-statistics/#余因子展開) × 1問
- [立方根計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#立方根計算) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [冪乗との最大公約数の収束](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗との最大公約数の収束) × 1問
- [冪乗タワー計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗タワー計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [nu50218さん](https://yukicoder.me/users/6056)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1920</font>](https://yukicoder.me/problems/no/2674)
- [★3.5／diff <font color="yellowgreen">2196</font>](https://yukicoder.me/problems/no/2677)
- [★3.5／diff <font color="orange">2615</font>](https://yukicoder.me/problems/no/2675)

### 過去問の解法頻度

- [bool値の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#bool値の充足可能性判定) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [法B係数連立一次方程式の解の存在判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の存在判定) × 1問


## [okkuukenkenさん](https://yukicoder.me/users/6186)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diffデータなし](https://yukicoder.me/problems/no/2069)

### 過去問の解法頻度

- [構文解析](https://p-adic.github.io/yukicoder-difficulty-statistics/#構文解析) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰的構造に沿った再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構造に沿った再帰) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問


## [noshi91さん](https://yukicoder.me/users/6250)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4／diff <font color="darkgoldenrod ">3309</font>](https://yukicoder.me/problems/no/2995)
- [★5／diff <font color="red">3196</font>](https://yukicoder.me/problems/no/2579)

### 過去問の解法頻度

- [Bostan-Mori法](https://p-adic.github.io/yukicoder-difficulty-statistics/#Bostan-Mori法) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 1問
- [期待値漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値漸化式) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [巡回畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回畳み込み) × 1問
- [剰余の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余の定理) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [多項式のユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項式のユークリッドの互除法) × 1問
- [多項式を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項式を法とする逆元計算) × 1問
- [単位の分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#単位の分解) × 1問
- [低次項の追加による線形化](https://p-adic.github.io/yukicoder-difficulty-statistics/#低次項の追加による線形化) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問


## [hitonanodeさん](https://yukicoder.me/users/6298)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★5／diff <font color="darkgoldenrod ">3503</font>](https://yukicoder.me/problems/no/2594)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [first_vilさん](https://yukicoder.me/users/6913)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4／diff <font color="red">3086</font>](https://yukicoder.me/problems/no/2169)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [kenken714さん](https://yukicoder.me/users/7164)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="yellowgreen">2176</font>](https://yukicoder.me/problems/no/2631)
- [★3／diff <font color="yellowgreen">2236</font>](https://yukicoder.me/problems/no/3117)
- [★4／diff <font color="orange">2591</font>](https://yukicoder.me/problems/no/3123)
- [★4／diff <font color="red">2884</font>](https://yukicoder.me/problems/no/2439)

### 過去問の解法頻度

- [XOR・反転が2回で戻ることに注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#XOR・反転が2回で戻ることに注目) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [グラフ・状態の圧縮による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフ・状態の圧縮による次元削減) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [累積XOR](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積XOR) × 1問


## [Sumitacchanさん](https://yukicoder.me/users/7400)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="yellowgreen">2139</font>](https://yukicoder.me/problems/no/2104)
- [★3／diff <font color="blue">1934</font>](https://yukicoder.me/problems/no/2103)
- [★3.5／diff <font color="yellowgreen">2327</font>](https://yukicoder.me/problems/no/2105)
- [★3.5／diff <font color="orange">2532</font>](https://yukicoder.me/problems/no/2106)
- [★4.5／diffデータなし](https://yukicoder.me/problems/no/2107)
- [★4.5／diff <font color="red">3159</font>](https://yukicoder.me/problems/no/2108)

### 過去問の解法頻度

- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [括弧列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#括弧列DP) × 1問
- [括弧列のワイルドカードを左右から貪欲に開き・閉じ括弧に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#括弧列のワイルドカードを左右から貪欲に開き・閉じ括弧に翻訳) × 1問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 1問
- [最終手番のターン数に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番のターン数に注目) × 1問
- [最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番の任意性) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [入れ子の深さを記録する走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#入れ子の深さを記録する走査) × 1問
- [閉じた括弧列判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉じた括弧列判定) × 1問


## [tko919さん](https://yukicoder.me/users/7482)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="yellowgreen">2241</font>](https://yukicoder.me/problems/no/2980)
- [★4.5／diff <font color="darkgoldenrod ">3316</font>](https://yukicoder.me/problems/no/2597)
- [★4.5／diff <font color="darkgoldenrod ">3382</font>](https://yukicoder.me/problems/no/2173)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [グラフの頂点の次数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの頂点の次数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [事象の確率を保つ全射](https://p-adic.github.io/yukicoder-difficulty-statistics/#事象の確率を保つ全射) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問


## [KowerKoint2010さん](https://yukicoder.me/users/7583)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4／diff <font color="orange">2485</font>](https://yukicoder.me/problems/no/2158)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [NyaanNyaanさん](https://yukicoder.me/users/7896)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4.5／diff <font color="red">3115</font>](https://yukicoder.me/problems/no/3000)
- [★5／diff <font color="darkgoldenrod ">3316</font>](https://yukicoder.me/problems/no/2583)
- [★5.5／diff <font color="darkgoldenrod ">3577</font>](https://yukicoder.me/problems/no/2166)

### 過去問の解法頻度

- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 2問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 2問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 2問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 2問
- [P-再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#P-再帰) × 1問
- [Polynomial Taylor shift](https://p-adic.github.io/yukicoder-difficulty-statistics/#Polynomial Taylor shift) × 1問
- [データ構造をマージする一般的なテク](https://p-adic.github.io/yukicoder-difficulty-statistics/#データ構造をマージする一般的なテク) × 1問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [一次分数変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次分数変換) × 1問
- [一次分数変換と対数関数による変数変換の合成](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次分数変換と対数関数による変数変換の合成) × 1問
- [演算の反復の分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#演算の反復の分割統治) × 1問
- [高階微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#高階微分計算) × 1問
- [指数関数による変数変換と一次分数変換の合成](https://p-adic.github.io/yukicoder-difficulty-statistics/#指数関数による変数変換と一次分数変換の合成) × 1問
- [多点評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点評価) × 1問
- [微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分計算) × 1問
- [微分作用素を変数変換で簡易化](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分作用素を変数変換で簡易化) × 1問
- [評価点シフト](https://p-adic.github.io/yukicoder-difficulty-statistics/#評価点シフト) × 1問
- [部分積分](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分積分) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問


## [nullさん](https://yukicoder.me/users/8315)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="orange">2491</font>](https://yukicoder.me/problems/no/2165)
- [★3／diff <font color="yellowgreen">2323</font>](https://yukicoder.me/problems/no/2577)
- [★3／diff <font color="orange">2429</font>](https://yukicoder.me/problems/no/2592)

### 過去問の解法頻度

- [１つの桁・成分のみ特定する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#１つの桁・成分のみ特定する質問) × 1問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [ド・モルガンの法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#ド・モルガンの法則) × 1問
- [ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニム和) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [十分大きな法で計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#十分大きな法で計算) × 1問
- [順列のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#順列のリアクティブによる特定) × 1問
- [剰余による確率的判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余による確率的判定) × 1問
- [剰余の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余の定理) × 1問
- [多倍長整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#多倍長整数) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [必勝戦略のリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#必勝戦略のリアクティブ化) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [複数底の位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数底の位取り記法表示) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問


## [tute7627さん](https://yukicoder.me/users/8361)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1777</font>](https://yukicoder.me/problems/no/3056)
- [★2.5／diff <font color="yellowgreen">2089</font>](https://yukicoder.me/problems/no/3057)
- [★3／diff <font color="orange">2622</font>](https://yukicoder.me/problems/no/3058)
- [★3／diff <font color="orange">2783</font>](https://yukicoder.me/problems/no/3062)
- [★3／diff <font color="red">2971</font>](https://yukicoder.me/problems/no/3059)
- [★3／diff <font color="red">2971</font>](https://yukicoder.me/problems/no/3061)
- [★3／diff <font color="darkgoldenrod ">3217</font>](https://yukicoder.me/problems/no/3060)
- [★3.5／diff <font color="orange">2758</font>](https://yukicoder.me/problems/no/2171)
- [★3.5／diff <font color="darkgoldenrod ">3414</font>](https://yukicoder.me/problems/no/3063)
- [★4／diff <font color="red">3026</font>](https://yukicoder.me/problems/no/2588)

### 過去問の解法頻度

- [Disjoint Sparse Table](https://p-adic.github.io/yukicoder-difficulty-statistics/#Disjoint Sparse Table) × 2問
- [Sparse Table](https://p-adic.github.io/yukicoder-difficulty-statistics/#Sparse Table) × 2問
- [グラフの構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの構築) × 2問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 2問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 2問
- [区間max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min取得) × 2問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 2問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 2問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [Cartesian tree](https://p-adic.github.io/yukicoder-difficulty-statistics/#Cartesian tree) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [コスト１ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#コスト１ナップサック最適化) × 1問
- [スライド最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#スライド最大・最小化) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [可変コスト上限ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#可変コスト上限ナップサック最適化) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [彩色の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#彩色の構築) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [独立事象の積への分解による確率計算・数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#独立事象の積への分解による確率計算・数え上げ) × 1問
- [非連結なグラフの構築を境界の構築に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#非連結なグラフの構築を境界の構築に帰着) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [複数価値ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数価値ナップサック最適化) × 1問
- [文字列・配列の追加・挿入の事前処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列・配列の追加・挿入の事前処理) × 1問
- [木の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の構築) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問


## [miscalcさん](https://yukicoder.me/users/8431)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">831</font>](https://yukicoder.me/problems/no/2275)
- [★2.5／diff <font color="deepskyblue">1331</font>](https://yukicoder.me/problems/no/2276)
- [★3／diff <font color="yellowgreen">2153</font>](https://yukicoder.me/problems/no/2278)
- [★3.5／diff <font color="orange">2452</font>](https://yukicoder.me/problems/no/2280)
- [★4／diff <font color="red">2903</font>](https://yukicoder.me/problems/no/2162)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 2問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [inplace DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#inplace DP) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [ループ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ループ戦略) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [区間max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min更新) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 1問
- [最終手番のターン数に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番のターン数に注目) × 1問
- [最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番の任意性) × 1問
- [最長共通接頭辞計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最長共通接頭辞計算) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [双対セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#双対セグメント木) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問


## [ngtkanaさん](https://yukicoder.me/users/8492)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1515</font>](https://yukicoder.me/problems/no/3015)

### 過去問の解法頻度

- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [hotman78さん](https://yukicoder.me/users/8996)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">715</font>](https://yukicoder.me/problems/no/3108)
- [★4.5／diff <font color="orange">2749</font>](https://yukicoder.me/problems/no/2575)
- [★4.5／diff <font color="darkgoldenrod ">3382</font>](https://yukicoder.me/problems/no/2159)

### 過去問の解法頻度

- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問


## [zer0-starさん](https://yukicoder.me/users/9206)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1717</font>](https://yukicoder.me/problems/no/2640)

### 過去問の解法頻度

- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [ワーシャル・フロイド法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ワーシャル・フロイド法) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問


## [SPD_9X2さん](https://yukicoder.me/users/9323)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">721</font>](https://yukicoder.me/problems/no/2679)
- [★2／diffデータなし](https://yukicoder.me/problems/no/2363)
- [★2／diffデータなし](https://yukicoder.me/problems/no/2469)
- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2474)
- [★3.5／diffデータなし](https://yukicoder.me/problems/no/2468)
- [★3.5／diff <font color="red">2804</font>](https://yukicoder.me/problems/no/2170)
- [★4／diffデータなし](https://yukicoder.me/problems/no/2470)
- [★4／diffデータなし](https://yukicoder.me/problems/no/2472)
- [★4.5／diffデータなし](https://yukicoder.me/problems/no/2471)
- [★4.5／diff <font color="red">3177</font>](https://yukicoder.me/problems/no/2689)
- [★5.5／diffデータなし](https://yukicoder.me/problems/no/2473)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [サンプルに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルに帰着) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [一対一対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#一対一対応) × 1問
- [円周角の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#円周角の定理) × 1問
- [解と係数の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#解と係数の関係) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間を切片の差に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を切片の差に翻訳) × 1問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問


## [MZKiさん](https://yukicoder.me/users/9437)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">1026</font>](https://yukicoder.me/problems/no/2750)
- [★3／diff <font color="blue">1751</font>](https://yukicoder.me/problems/no/2756)

### 過去問の解法頻度

- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 2問
- [素数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列挙) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [オーバーフロー回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#オーバーフロー回避) × 1問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 1問
- [最小素因数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小素因数計算) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問


## [timiさん](https://yukicoder.me/users/9606)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1803</font>](https://yukicoder.me/problems/no/2696)

### 過去問の解法頻度

- [距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#距離空間の重み付きグラフ化) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問


## [ebi_flyさん](https://yukicoder.me/users/9720)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="orange">2476</font>](https://yukicoder.me/problems/no/2634)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [abap34さん](https://yukicoder.me/users/9726)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="yellowgreen">2249</font>](https://yukicoder.me/problems/no/2642)
- [★4／diff <font color="darkgoldenrod ">3227</font>](https://yukicoder.me/problems/no/2438)

### 過去問の解法頻度

- [ダブリング](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダブリング) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [最近共通祖先計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最近共通祖先計算) × 1問
- [最小全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小全域木計算) × 1問
- [重み付き木上の頂点間距離取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#重み付き木上の頂点間距離取得) × 1問
- [全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全域木計算) × 1問


## [箱星さん](https://yukicoder.me/users/10052)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="green">803</font>](https://yukicoder.me/problems/no/2789)
- [★1／diff <font color="green">1017</font>](https://yukicoder.me/problems/no/2138)
- [★1.5／diff <font color="brown">406</font>](https://yukicoder.me/problems/no/2092)
- [★1.5／diff <font color="brown">719</font>](https://yukicoder.me/problems/no/2379)
- [★1.5／diff <font color="green">934</font>](https://yukicoder.me/problems/no/2790)
- [★1.5／diff <font color="green">1069</font>](https://yukicoder.me/problems/no/2203)
- [★2／diffデータなし](https://yukicoder.me/problems/no/2466)
- [★2／diff <font color="deepskyblue">1221</font>](https://yukicoder.me/problems/no/2791)
- [★2／diff <font color="deepskyblue">1233</font>](https://yukicoder.me/problems/no/2380)
- [★2／diff <font color="deepskyblue">1518</font>](https://yukicoder.me/problems/no/2095)
- [★2.5／diff <font color="deepskyblue">1550</font>](https://yukicoder.me/problems/no/2382)
- [★2.5／diff <font color="blue">1661</font>](https://yukicoder.me/problems/no/2197)
- [★2.5／diff <font color="blue">1859</font>](https://yukicoder.me/problems/no/2381)
- [★3／diff <font color="blue">1813</font>](https://yukicoder.me/problems/no/2792)
- [★3／diff <font color="yellowgreen">2141</font>](https://yukicoder.me/problems/no/2754)
- [★3／diff <font color="yellowgreen">2183</font>](https://yukicoder.me/problems/no/2383)
- [★3.5／diff <font color="orange">2487</font>](https://yukicoder.me/problems/no/2199)
- [★4／diff <font color="red">3038</font>](https://yukicoder.me/problems/no/2793)
- [★5／diff <font color="orange">2795</font>](https://yukicoder.me/problems/no/2556)
- [★5／diff <font color="red">3017</font>](https://yukicoder.me/problems/no/2384)
- [★5／diff <font color="red">3086</font>](https://yukicoder.me/problems/no/2149)
- [★5／diff <font color="darkgoldenrod ">3495</font>](https://yukicoder.me/problems/no/2794)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 6問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 4問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 4問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 4問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 4問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 4問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 4問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 4問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 3問
- [01列とグリッド上の経路の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列とグリッド上の経路の対応) × 2問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 2問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 2問
- [ド・モルガンの法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#ド・モルガンの法則) × 2問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 2問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 2問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 2問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 2問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 2問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 2問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 2問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 2問
- [累積和・グリッド上のDPを経路数え上げに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和・グリッド上のDPを経路数え上げに翻訳) × 2問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 2問
- [01列とヤング図形の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列とヤング図形の対応) × 1問
- [01列と単調増加列・分割の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と単調増加列・分割の対応) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [Lindstrom-Gessel-Viennotの補題](https://p-adic.github.io/yukicoder-difficulty-statistics/#Lindstrom-Gessel-Viennotの補題) × 1問
- [カタランの三角形計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カタランの三角形計算) × 1問
- [カレンダー計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カレンダー計算) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [コーシー・フロベニウスの補題](https://p-adic.github.io/yukicoder-difficulty-statistics/#コーシー・フロベニウスの補題) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [データ構造をマージする一般的なテク](https://p-adic.github.io/yukicoder-difficulty-statistics/#データ構造をマージする一般的なテク) × 1問
- [ファンデルモンドの行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#ファンデルモンドの行列式計算) × 1問
- [フック長公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#フック長公式) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [ラマヌジャンの無限根号](https://p-adic.github.io/yukicoder-difficulty-statistics/#ラマヌジャンの無限根号) × 1問
- [ループ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ループ戦略) × 1問
- [ルジャンドルの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ルジャンドルの公式) × 1問
- [一次式の最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の最大・最小値計算) × 1問
- [演算の反復の分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#演算の反復の分割統治) × 1問
- [階乗による多項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による多項係数計算) × 1問
- [外積による三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積による三角形の面積計算) × 1問
- [外積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積計算) × 1問
- [極限の打ち切り計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#極限の打ち切り計算) × 1問
- [極小基本互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#極小基本互換表示) × 1問
- [区間の重複度計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の重複度計算) × 1問
- [区間を切片の差に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を切片の差に翻訳) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#互換表示) × 1問
- [行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列式計算) × 1問
- [高階累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#高階累積和) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [差積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差積計算) × 1問
- [三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の面積計算) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [多項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項係数計算) × 1問
- [多点評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点評価) × 1問
- [単調列数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調列数え上げ) × 1問
- [置換の位数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#置換の位数計算) × 1問
- [置換の符号計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#置換の符号計算) × 1問
- [転倒数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#転倒数計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二面体群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#二面体群の構造に注目) × 1問
- [排他的被覆数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#排他的被覆数え上げ) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [半標準ヤングタブローとGelfand-Tsetlinパターンの対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#半標準ヤングタブローとGelfand-Tsetlinパターンの対応) × 1問
- [半標準ヤングタブローと非交差経路の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#半標準ヤングタブローと非交差経路の対応) × 1問
- [半標準ヤングタブローに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#半標準ヤングタブローに翻訳) × 1問
- [微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分計算) × 1問
- [標準ヤングタブローに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#標準ヤングタブローに翻訳) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問


## [logxさん](https://yukicoder.me/users/10223)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1352</font>](https://yukicoder.me/problems/no/2364)
- [★3／diff <font color="yellowgreen">2294</font>](https://yukicoder.me/problems/no/2366)

### 過去問の解法頻度

- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [bitDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitDP) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [ヘルド・カープ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ヘルド・カープ法) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [可負コストナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#可負コストナップサック最適化) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [不明な想定解](https://p-adic.github.io/yukicoder-difficulty-statistics/#不明な想定解) × 1問


## [stoqさん](https://yukicoder.me/users/10224)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="gray">344</font>](https://yukicoder.me/problems/no/2216)
- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2200)
- [★2.5／diff <font color="deepskyblue">1200</font>](https://yukicoder.me/problems/no/2217)
- [★2.5／diff <font color="deepskyblue">1200</font>](https://yukicoder.me/problems/no/2218)
- [★2.5／diff <font color="blue">1622</font>](https://yukicoder.me/problems/no/2219)
- [★3／diff <font color="blue">1927</font>](https://yukicoder.me/problems/no/2220)
- [★3.5／diff <font color="orange">2471</font>](https://yukicoder.me/problems/no/2221)
- [★3.5／diff <font color="red">2841</font>](https://yukicoder.me/problems/no/2222)
- [★4／diff <font color="orange">2791</font>](https://yukicoder.me/problems/no/2223)

### 過去問の解法頻度

- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 2問
- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [mex取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#mex取得) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [sorted set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted set) × 1問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [サンプルから推測](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルから推測) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [期待値漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値漸化式) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [最小全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小全域木計算) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [最長単調増加部分列長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最長単調増加部分列長計算) × 1問
- [最長歩道計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最長歩道計算) × 1問
- [枝刈り](https://p-adic.github.io/yukicoder-difficulty-statistics/#枝刈り) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全域木計算) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着) × 1問
- [総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和計算の期待値への帰着) × 1問
- [単調関数の像計算を階差の非零点の数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調関数の像計算を階差の非零点の数え上げに帰着) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [分枝限定法](https://p-adic.github.io/yukicoder-difficulty-statistics/#分枝限定法) × 1問
- [門松列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#門松列DP) × 1問
- [冪等重みの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪等重みの最短経路長計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [shobonvipさん](https://yukicoder.me/users/10360)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="gray">361</font>](https://yukicoder.me/problems/no/3099)
- [★2／diff <font color="green">846</font>](https://yukicoder.me/problems/no/2252)
- [★2／diff <font color="deepskyblue">1273</font>](https://yukicoder.me/problems/no/2426)
- [★2.5／diff <font color="blue">1777</font>](https://yukicoder.me/problems/no/3100)
- [★2.5／diff <font color="blue">1838</font>](https://yukicoder.me/problems/no/2241)
- [★3／diff <font color="blue">1777</font>](https://yukicoder.me/problems/no/3101)
- [★3／diff <font color="yellowgreen">2002</font>](https://yukicoder.me/problems/no/3102)
- [★3／diff <font color="yellowgreen">2274</font>](https://yukicoder.me/problems/no/2242)
- [★3.5／diff <font color="orange">2422</font>](https://yukicoder.me/problems/no/2255)
- [★3.5／diff <font color="orange">2432</font>](https://yukicoder.me/problems/no/3103)
- [★3.5／diff <font color="orange">2492</font>](https://yukicoder.me/problems/no/3104)
- [★3.5／diff <font color="orange">2582</font>](https://yukicoder.me/problems/no/2645)
- [★3.5／diff <font color="red">2827</font>](https://yukicoder.me/problems/no/3105)
- [★4／diff <font color="red">2827</font>](https://yukicoder.me/problems/no/3106)
- [★4／diff <font color="red">2871</font>](https://yukicoder.me/problems/no/2135)
- [★4／diff <font color="red">2930</font>](https://yukicoder.me/problems/no/2244)

### 過去問の解法頻度

- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 2問
- [,集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#,集合の変化イベント走査による差分計算) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [オイラーの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーの定理) × 1問
- [オイラーの定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーの定理による逆元計算) × 1問
- [クエリソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリソート) × 1問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [ダブリング](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダブリング) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [モンテカルロ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#モンテカルロ法) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [一要素重複挿入更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素重複挿入更新) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [外積による三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積による三角形の面積計算) × 1問
- [外積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積計算) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [言及する成分数を最大化する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#言及する成分数を最大化する質問) × 1問
- [合成数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成数を法とする逆元計算) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 1問
- [最小素因数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小素因数計算) × 1問
- [最大非自明約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大非自明約数計算) × 1問
- [最適遷移を自己写像に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#最適遷移を自己写像に翻訳) × 1問
- [三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の面積計算) × 1問
- [三角形分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形分割) × 1問
- [自己写像に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#自己写像に翻訳) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [順列のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#順列のリアクティブによる特定) × 1問
- [商の反復による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商の反復による付値計算) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [整礎性](https://p-adic.github.io/yukicoder-difficulty-statistics/#整礎性) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [凸多角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸多角形の面積計算) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [非単射関数の像の濃度による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の像の濃度による計算量評価) × 1問
- [非単射関数の値で纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の値で纏め上げ) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [平方根のfloorの種類数による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloorの種類数による計算量評価) × 1問
- [平方根のfloorの値で纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloorの値で纏め上げ) × 1問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 1問
- [閉じた括弧列判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉じた括弧列判定) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [hamamuさん](https://yukicoder.me/users/10411)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1210</font>](https://yukicoder.me/problems/no/2655)
- [★2.5／diff <font color="blue">1726</font>](https://yukicoder.me/problems/no/2656)
- [★3／diff <font color="yellowgreen">2117</font>](https://yukicoder.me/problems/no/2657)
- [★3.5／diff <font color="red">2822</font>](https://yukicoder.me/problems/no/2658)
- [★4.5／diffデータなし](https://yukicoder.me/problems/no/2659)
- [★4.5／diff <font color="red">3023</font>](https://yukicoder.me/problems/no/2660)
- [★5／diff <font color="darkgoldenrod ">3406</font>](https://yukicoder.me/problems/no/2661)

### 過去問の解法頻度

- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [01列・部分集合の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列・部分集合の構築) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [区間max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min更新) × 1問
- [区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮) × 1問
- [区間一次式max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間一次式max・min更新) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#終点からの最短経路長計算) × 1問
- [証明をなぞる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#証明をなぞる構築) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [双対セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#双対セグメント木) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [冪等重みの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪等重みの最短経路長計算) × 1問


## [simasima_71さん](https://yukicoder.me/users/10427)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">680</font>](https://yukicoder.me/problems/no/2425)

### 過去問の解法頻度

- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問


## [蜜蜂さん](https://yukicoder.me/users/10429)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">1070</font>](https://yukicoder.me/problems/no/2607)
- [★2／diff <font color="green">1123</font>](https://yukicoder.me/problems/no/3183)
- [★2／diff <font color="deepskyblue">1247</font>](https://yukicoder.me/problems/no/2608)
- [★2／diff <font color="deepskyblue">1323</font>](https://yukicoder.me/problems/no/3184)
- [★2.5／diff <font color="deepskyblue">1401</font>](https://yukicoder.me/problems/no/3185)
- [★2.5／diff <font color="deepskyblue">1531</font>](https://yukicoder.me/problems/no/2609)
- [★2.5／diff <font color="yellowgreen">2008</font>](https://yukicoder.me/problems/no/2895)
- [★3／diff <font color="yellowgreen">2129</font>](https://yukicoder.me/problems/no/2610)
- [★3／diff <font color="yellowgreen">2242</font>](https://yukicoder.me/problems/no/3187)
- [★3／diff <font color="yellowgreen">2397</font>](https://yukicoder.me/problems/no/2898)
- [★3／diff <font color="orange">2753</font>](https://yukicoder.me/problems/no/3186)
- [★3／diff <font color="red">2833</font>](https://yukicoder.me/problems/no/2612)
- [★3.5／diff <font color="orange">2568</font>](https://yukicoder.me/problems/no/3189)
- [★3.5／diff <font color="orange">2604</font>](https://yukicoder.me/problems/no/2611)
- [★3.5／diff <font color="orange">2753</font>](https://yukicoder.me/problems/no/3188)
- [★4／diff <font color="orange">2571</font>](https://yukicoder.me/problems/no/2613)
- [★4／diff <font color="red">2984</font>](https://yukicoder.me/problems/no/3190)

### 過去問の解法頻度

- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 6問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 3問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 3問
- [01列・部分集合の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列・部分集合の構築) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 2問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 2問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 2問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 2問
- [数列・配列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#数列・配列の構築) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 2問
- [素数を用いた構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を用いた構築) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 2問
- [$45$度回転](https://p-adic.github.io/yukicoder-difficulty-statistics/#$45$度回転) × 1問
- [B進法位取り記法と法Bベクトルの対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#B進法位取り記法と法Bベクトルの対応) × 1問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [suffix array](https://p-adic.github.io/yukicoder-difficulty-statistics/#suffix array) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ディオファントス方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の構築) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [バブルソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#バブルソート) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 1問
- [位取り記法による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法による構築) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [階数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階数計算) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [極小基本互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#極小基本互換表示) × 1問
- [区間の部分列をわたる総和計算をモノイド演算に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の部分列をわたる総和計算をモノイド演算に翻訳) × 1問
- [区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮) × 1問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#互換表示) × 1問
- [行列の簡約階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の簡約階段化) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [再帰的構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構築) × 1問
- [最小被覆半径計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小被覆半径計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 1問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 1問
- [商のfloorの値ごとに纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの値ごとに纏め上げ) × 1問
- [商の反復による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商の反復による付値計算) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [証明をなぞる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#証明をなぞる構築) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [掃き出し法](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法) × 1問
- [総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和計算の期待値への帰着) × 1問
- [多倍長整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#多倍長整数) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [探索・求解アルゴリズムによる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#探索・求解アルゴリズムによる構築) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二項係数・順列の第１引数を渡る総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数・順列の第１引数を渡る総和計算) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [配列の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列の変化イベント走査による差分計算) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [符号全探索による絶対値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#符号全探索による絶対値計算) × 1問
- [部分和と補部分和の差の最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分和と補部分和の差の最大・最小化) × 1問
- [部分和の差の最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分和の差の最大・最小化) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [文字列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列の構築) × 1問
- [平方分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方分割) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [法B係数連立一次方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の構築) × 1問
- [法B係数連立一次方程式の解の存在判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の存在判定) × 1問
- [約数の走査を倍数の走査に帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の走査を倍数の走査に帰) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [有理数を分母の上限以下の各正整数倍のfloorから計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#有理数を分母の上限以下の各正整数倍のfloorから計算) × 1問
- [累積max・min](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積max・min) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問


## [SSRSさん](https://yukicoder.me/users/10449)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="gray">342</font>](https://yukicoder.me/problems/no/2334)
- [★2／diff <font color="green">1025</font>](https://yukicoder.me/problems/no/2335)
- [★3／diff <font color="yellowgreen">2056</font>](https://yukicoder.me/problems/no/2337)
- [★3／diff <font color="yellowgreen">2237</font>](https://yukicoder.me/problems/no/2336)
- [★3.5／diff <font color="orange">2498</font>](https://yukicoder.me/problems/no/2338)
- [★3.5／diff <font color="orange">2550</font>](https://yukicoder.me/problems/no/2339)
- [★4／diff <font color="red">2965</font>](https://yukicoder.me/problems/no/2340)
- [★4.5／diff <font color="darkgoldenrod ">3284</font>](https://yukicoder.me/problems/no/2341)
- [★4.5／diff <font color="darkgoldenrod ">3316</font>](https://yukicoder.me/problems/no/2595)
- [★5／diff <font color="darkgoldenrod ">3395</font>](https://yukicoder.me/problems/no/2342)

### 過去問の解法頻度

- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 2問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [parallel tree contraction](https://p-adic.github.io/yukicoder-difficulty-statistics/#parallel tree contraction) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ダブリング](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダブリング) × 1問
- [データ構造をマージする一般的なテク](https://p-adic.github.io/yukicoder-difficulty-statistics/#データ構造をマージする一般的なテク) × 1問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 1問
- [フェルマーの小定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理による逆元計算) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [レベル祖先計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#レベル祖先計算) × 1問
- [一対一対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#一対一対応) × 1問
- [演算の適用を一次式の合成に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#演算の適用を一次式の合成に翻訳) × 1問
- [演算の反復の分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#演算の反復の分割統治) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [構文解析](https://p-adic.github.io/yukicoder-difficulty-statistics/#構文解析) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰的構造に沿った再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構造に沿った再帰) × 1問
- [最近共通祖先計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最近共通祖先計算) × 1問
- [事象の確率を保つ全射](https://p-adic.github.io/yukicoder-difficulty-statistics/#事象の確率を保つ全射) × 1問
- [重軽分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#重軽分解) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [多倍長整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#多倍長整数) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [木の頂点の重さ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の頂点の重さ計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [chineristACさん](https://yukicoder.me/users/10535)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1486</font>](https://yukicoder.me/problems/no/2072)
- [★3／diff <font color="yellowgreen">2047</font>](https://yukicoder.me/problems/no/2074)
- [★3.5／diff <font color="orange">2707</font>](https://yukicoder.me/problems/no/2077)
- [★3.5／diff <font color="red">3019</font>](https://yukicoder.me/problems/no/2167)

### 過去問の解法頻度

- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [オイラーの規準](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーの規準) × 1問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [グラフの辺の削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の削除更新) × 1問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [ポラードの$\rho$](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポラードの$\rho$) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [区間kth取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間kth取得) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [互いに素に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#互いに素に帰着) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [十分大きな法で計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#十分大きな法で計算) × 1問
- [剰余による確率的判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余による確率的判定) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [平方剰余判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方剰余判定) × 1問
- [平方数の積への分解を用いた平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方数の積への分解を用いた平方数判定) × 1問
- [平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方数判定) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問


## [noya2さん](https://yukicoder.me/users/10759)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="green">812</font>](https://yukicoder.me/problems/no/3191)
- [★1／diff <font color="green">967</font>](https://yukicoder.me/problems/no/2637)
- [★1.5／diff <font color="green">812</font>](https://yukicoder.me/problems/no/3192)
- [★1.5／diff <font color="green">1060</font>](https://yukicoder.me/problems/no/2239)
- [★2／diff <font color="green">873</font>](https://yukicoder.me/problems/no/2795)
- [★2／diff <font color="deepskyblue">1273</font>](https://yukicoder.me/problems/no/2427)
- [★2／diff <font color="deepskyblue">1373</font>](https://yukicoder.me/problems/no/2240)
- [★2.5／diff <font color="deepskyblue">1591</font>](https://yukicoder.me/problems/no/2639)
- [★2.5／diff <font color="blue">1768</font>](https://yukicoder.me/problems/no/2253)
- [★2.5／diff <font color="blue">1848</font>](https://yukicoder.me/problems/no/2796)
- [★2.5／diff <font color="yellowgreen">2025</font>](https://yukicoder.me/problems/no/2628)
- [★2.5／diff <font color="yellowgreen">2328</font>](https://yukicoder.me/problems/no/2797)
- [★3／diffデータなし](https://yukicoder.me/problems/no/2183)
- [★3／diff <font color="yellowgreen">2134</font>](https://yukicoder.me/problems/no/2798)
- [★3.5／diff <font color="yellowgreen">2187</font>](https://yukicoder.me/problems/no/2254)
- [★3.5／diff <font color="red">2854</font>](https://yukicoder.me/problems/no/2799)
- [★4／diff <font color="orange">2666</font>](https://yukicoder.me/problems/no/2243)
- [★4／diff <font color="red">2877</font>](https://yukicoder.me/problems/no/2245)
- [★4／diff <font color="red">2905</font>](https://yukicoder.me/problems/no/3193)
- [★4／diff <font color="darkgoldenrod ">3236</font>](https://yukicoder.me/problems/no/2800)
- [★4.5／diffデータなし](https://yukicoder.me/problems/no/2801)
- [★4.5／diff <font color="red">3026</font>](https://yukicoder.me/problems/no/3194)
- [★4.5／diff <font color="darkgoldenrod ">3556</font>](https://yukicoder.me/problems/no/2256)
- [★5／diff <font color="darkgoldenrod ">3556</font>](https://yukicoder.me/problems/no/2257)

### 過去問の解法頻度

- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 3問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 3問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 2問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 2問
- [2項演算の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#2項演算の構築) × 1問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [Dilworthの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#Dilworthの定理) × 1問
- [Vieta Jumping](https://p-adic.github.io/yukicoder-difficulty-statistics/#Vieta Jumping) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [★1の64bit整数要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1の64bit整数要求) × 1問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [グラフの構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの構築) × 1問
- [グラフの頂点の次数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの頂点の次数計算) × 1問
- [サンプルに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルに帰着) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [タイリング・LightsOutの解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#タイリング・LightsOutの解の構築) × 1問
- [トポロジカルソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#トポロジカルソート) × 1問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 1問
- [ポラードの$\rho$](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポラードの$\rho$) × 1問
- [一次式の最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の最大・最小値計算) × 1問
- [解と係数の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#解と係数の関係) × 1問
- [解の公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#解の公式) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [区間の重複度計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の重複度計算) × 1問
- [区間スケジューリング](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間スケジューリング) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [鎖への分割数の最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#鎖への分割数の最小化) × 1問
- [最長歩道計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最長歩道計算) × 1問
- [三項間漸化式の求解](https://p-adic.github.io/yukicoder-difficulty-statistics/#三項間漸化式の求解) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [周期的構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期的構築) × 1問
- [重複選択可ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック割り当て数え上げ) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [制約からグラフの種類を特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#制約からグラフの種類を特定) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [素数列による試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列による試し割り法) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [相似](https://p-adic.github.io/yukicoder-difficulty-statistics/#相似) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [凸最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸最適化) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [入れ子の深さを記録する走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#入れ子の深さを記録する走査) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [分割数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割数計算) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [分割方法数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割方法数え上げ) × 1問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [閉じた括弧列判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉じた括弧列判定) × 1問
- [変数の対称性](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数の対称性) × 1問
- [埋め込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#埋め込み) × 1問
- [約数の走査を倍数の走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の走査を倍数の走査に帰着) × 1問


## [kumakumaさん](https://yukicoder.me/users/11008)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="orange">2486</font>](https://yukicoder.me/problems/no/2238)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [nok0さん](https://yukicoder.me/users/11122)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="yellowgreen">2008</font>](https://yukicoder.me/problems/no/2059)
- [★3／diffデータなし](https://yukicoder.me/problems/no/2476)
- [★3／diff <font color="yellowgreen">2191</font>](https://yukicoder.me/problems/no/2132)
- [★4／diffデータなし](https://yukicoder.me/problems/no/2475)
- [★4.5／diffデータなし](https://yukicoder.me/problems/no/2478)

### 過去問の解法頻度

- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 2問
- [タイリングによるミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#タイリングによるミラー戦略) × 1問
- [ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニム和) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#高さ奇数ニム和) × 1問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量を保つ戦略) × 1問
- [不明な想定解](https://p-adic.github.io/yukicoder-difficulty-statistics/#不明な想定解) × 1問


## [deuteridayoさん](https://yukicoder.me/users/11153)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">140</font>](https://yukicoder.me/problems/no/2557)
- [★2／diff <font color="brown">775</font>](https://yukicoder.me/problems/no/2561)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [next_permutation](https://p-adic.github.io/yukicoder-difficulty-statistics/#next_permutation) × 1問
- [４重以上のループ](https://p-adic.github.io/yukicoder-difficulty-statistics/#４重以上のループ) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰による多重ループ実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰による多重ループ実装) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問


## [t98sliderさん](https://yukicoder.me/users/11210)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="brown">780</font>](https://yukicoder.me/problems/no/3171)
- [★2／diff <font color="green">849</font>](https://yukicoder.me/problems/no/2289)
- [★2.5／diff <font color="deepskyblue">1302</font>](https://yukicoder.me/problems/no/2290)
- [★2.5／diff <font color="deepskyblue">1396</font>](https://yukicoder.me/problems/no/3173)
- [★2.5／diff <font color="deepskyblue">1595</font>](https://yukicoder.me/problems/no/3172)
- [★2.5／diff <font color="blue">1795</font>](https://yukicoder.me/problems/no/2291)
- [★2.5／diff <font color="yellowgreen">2237</font>](https://yukicoder.me/problems/no/2293)
- [★3／diff <font color="orange">2489</font>](https://yukicoder.me/problems/no/2292)
- [★3.5／diff <font color="yellowgreen">2315</font>](https://yukicoder.me/problems/no/3174)
- [★3.5／diff <font color="orange">2470</font>](https://yukicoder.me/problems/no/3175)
- [★3.5／diff <font color="orange">2702</font>](https://yukicoder.me/problems/no/2295)
- [★3.5／diff <font color="orange">2748</font>](https://yukicoder.me/problems/no/2294)
- [★4／diff <font color="red">2916</font>](https://yukicoder.me/problems/no/3176)
- [★4／diff <font color="red">3084</font>](https://yukicoder.me/problems/no/2296)

### 過去問の解法頻度

- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 4問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 4問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 3問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 3問
- [next_permutation](https://p-adic.github.io/yukicoder-difficulty-statistics/#next_permutation) × 2問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 2問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 2問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 2問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 2問
- [超頂点追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#超頂点追加) × 2問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 2問
- [01列とグリッド上の経路の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列とグリッド上の経路の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [bool値の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#bool値の充足可能性判定) × 1問
- [sorted set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted set) × 1問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [データ構造の変更箇所のみを戻す初期化](https://p-adic.github.io/yukicoder-difficulty-statistics/#データ構造の変更箇所のみを戻す初期化) × 1問
- [ディオファントス方程式の解の数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の数え上げ) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [パスカルの三角形](https://p-adic.github.io/yukicoder-difficulty-statistics/#パスカルの三角形) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [フロー](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロー) × 1問
- [ポテンシャル付き素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポテンシャル付き素集合データ構造) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [帰属区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#帰属区間取得) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [極小互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#極小互換表示) × 1問
- [区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮) × 1問
- [区間削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間削除更新) × 1問
- [区間挿入更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間挿入更新) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [最大二部マッチング](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大二部マッチング) × 1問
- [最大流計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大流計算) × 1問
- [試行回数・順位の期待値を各試行の実施確率・各項の先着確率の和に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#試行回数・順位の期待値を各試行の実施確率・各項の先着確率の和に帰着) × 1問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [積和の公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の公式) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [頂点倍化](https://p-adic.github.io/yukicoder-difficulty-statistics/#頂点倍化) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [二部グラフ判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#二部グラフ判定) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [複数ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数ナップサック最適化) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [法B係数連立一次方程式の解の数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の数え上げ) × 1問
- [法B係数連立一次方程式の解の存在判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の存在判定) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [AngrySadEightさん](https://yukicoder.me/users/11268)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">132</font>](https://yukicoder.me/problems/no/2407)
- [★1／diff <font color="gray">205</font>](https://yukicoder.me/problems/no/2621)
- [★1／diff <font color="brown">420</font>](https://yukicoder.me/problems/no/2350)
- [★1／diff <font color="brown">469</font>](https://yukicoder.me/problems/no/2842)
- [★1／diff <font color="brown">544</font>](https://yukicoder.me/problems/no/2224)
- [★1／diff <font color="brown">731</font>](https://yukicoder.me/problems/no/3064)
- [★1.5／diff <font color="green">826</font>](https://yukicoder.me/problems/no/3065)
- [★1.5／diff <font color="green">826</font>](https://yukicoder.me/problems/no/3066)
- [★1.5／diff <font color="green">844</font>](https://yukicoder.me/problems/no/2843)
- [★1.5／diff <font color="green">919</font>](https://yukicoder.me/problems/no/2729)
- [★1.5／diff <font color="green">999</font>](https://yukicoder.me/problems/no/2225)
- [★1.5／diff <font color="deepskyblue">1250</font>](https://yukicoder.me/problems/no/3067)
- [★1.5／diff <font color="deepskyblue">1356</font>](https://yukicoder.me/problems/no/2562)
- [★2／diff <font color="brown">657</font>](https://yukicoder.me/problems/no/2408)
- [★2／diff <font color="brown">777</font>](https://yukicoder.me/problems/no/2351)
- [★2／diff <font color="green">996</font>](https://yukicoder.me/problems/no/2409)
- [★2／diff <font color="green">1029</font>](https://yukicoder.me/problems/no/2622)
- [★2／diff <font color="deepskyblue">1250</font>](https://yukicoder.me/problems/no/3069)
- [★2／diff <font color="deepskyblue">1275</font>](https://yukicoder.me/problems/no/2131)
- [★2／diff <font color="deepskyblue">1373</font>](https://yukicoder.me/problems/no/3070)
- [★2／diff <font color="deepskyblue">1482</font>](https://yukicoder.me/problems/no/2094)
- [★2／diff <font color="deepskyblue">1551</font>](https://yukicoder.me/problems/no/2226)
- [★2／diff <font color="yellowgreen">2082</font>](https://yukicoder.me/problems/no/3068)
- [★2.5／diff <font color="deepskyblue">1318</font>](https://yukicoder.me/problems/no/2410)
- [★2.5／diff <font color="deepskyblue">1328</font>](https://yukicoder.me/problems/no/2623)
- [★2.5／diff <font color="deepskyblue">1473</font>](https://yukicoder.me/problems/no/2844)
- [★2.5／diff <font color="deepskyblue">1560</font>](https://yukicoder.me/problems/no/2352)
- [★2.5／diff <font color="blue">1612</font>](https://yukicoder.me/problems/no/2566)
- [★2.5／diff <font color="blue">1654</font>](https://yukicoder.me/problems/no/2625)
- [★2.5／diff <font color="blue">1670</font>](https://yukicoder.me/problems/no/2353)
- [★2.5／diff <font color="blue">1670</font>](https://yukicoder.me/problems/no/2354)
- [★2.5／diff <font color="blue">1671</font>](https://yukicoder.me/problems/no/3072)
- [★2.5／diff <font color="blue">1773</font>](https://yukicoder.me/problems/no/2227)
- [★2.5／diff <font color="blue">1802</font>](https://yukicoder.me/problems/no/2073)
- [★2.5／diff <font color="blue">1919</font>](https://yukicoder.me/problems/no/2355)
- [★2.5／diff <font color="blue">1933</font>](https://yukicoder.me/problems/no/2228)
- [★2.5／diff <font color="blue">1945</font>](https://yukicoder.me/problems/no/3073)
- [★2.5／diff <font color="blue">1947</font>](https://yukicoder.me/problems/no/2845)
- [★2.5／diff <font color="yellowgreen">2011</font>](https://yukicoder.me/problems/no/3071)
- [★2.5／diff <font color="yellowgreen">2042</font>](https://yukicoder.me/problems/no/2530)
- [★3／diff <font color="blue">1735</font>](https://yukicoder.me/problems/no/2624)
- [★3／diff <font color="blue">1865</font>](https://yukicoder.me/problems/no/2229)
- [★3／diff <font color="blue">1951</font>](https://yukicoder.me/problems/no/2531)
- [★3／diff <font color="yellowgreen">2034</font>](https://yukicoder.me/problems/no/2734)
- [★3／diff <font color="yellowgreen">2050</font>](https://yukicoder.me/problems/no/2198)
- [★3／diff <font color="yellowgreen">2116</font>](https://yukicoder.me/problems/no/2846)
- [★3／diff <font color="yellowgreen">2169</font>](https://yukicoder.me/problems/no/2230)
- [★3／diff <font color="yellowgreen">2182</font>](https://yukicoder.me/problems/no/2356)
- [★3／diff <font color="orange">2620</font>](https://yukicoder.me/problems/no/2076)
- [★3.5／diff <font color="yellowgreen">2068</font>](https://yukicoder.me/problems/no/2411)
- [★3.5／diff <font color="yellowgreen">2137</font>](https://yukicoder.me/problems/no/2626)
- [★3.5／diff <font color="yellowgreen">2176</font>](https://yukicoder.me/problems/no/2412)
- [★3.5／diff <font color="orange">2416</font>](https://yukicoder.me/problems/no/2847)
- [★3.5／diff <font color="orange">2467</font>](https://yukicoder.me/problems/no/2848)
- [★3.5／diff <font color="orange">2595</font>](https://yukicoder.me/problems/no/2161)
- [★3.5／diff <font color="orange">2690</font>](https://yukicoder.me/problems/no/2096)
- [★4／diff <font color="orange">2731</font>](https://yukicoder.me/problems/no/2849)
- [★4／diff <font color="orange">2771</font>](https://yukicoder.me/problems/no/2413)
- [★4／diff <font color="red">2862</font>](https://yukicoder.me/problems/no/2627)
- [★4.5／diff <font color="orange">2690</font>](https://yukicoder.me/problems/no/2231)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 13問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 11問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 10問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 10問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 9問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 9問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 8問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 7問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 7問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 7問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 7問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 7問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 6問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 5問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 5問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 5問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 4問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 3問
- [フェルマーの小定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理による逆元計算) × 3問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 3問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 3問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 3問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 3問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 3問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 3問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 3問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 3問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 3問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 2問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 2問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 2問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 2問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 2問
- [ループ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ループ戦略) × 2問
- [位取り記法による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法による構築) × 2問
- [一次式の最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の最大・最小値計算) × 2問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 2問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 2問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 2問
- [確率漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#確率漸化式) × 2問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 2問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 2問
- [経路復元](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路復元) × 2問
- [合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成による次元削減) × 2問
- [最近点計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最近点計算) × 2問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 2問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 2問
- [周期的構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期的構築) × 2問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 2問
- [探索・求解アルゴリズムによる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#探索・求解アルゴリズムによる構築) × 2問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 2問
- [同値関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#同値関係) × 2問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 2問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 2問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 2問
- [有理数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#有理数型) × 2問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 2問
- [01BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#01BFS) × 1問
- [2集合間距離距離計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#2集合間距離距離計算) × 1問
- [inplace DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#inplace DP) × 1問
- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [next DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#next DP) × 1問
- [★1の64bit整数要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1の64bit整数要求) × 1問
- [２種の数値を足し引きして１種に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#２種の数値を足し引きして１種に帰着) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [カレンダー計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カレンダー計算) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [グラフの構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの構築) × 1問
- [グリッド上の価値最大化](https://p-adic.github.io/yukicoder-difficulty-statistics/#グリッド上の価値最大化) × 1問
- [コストなしナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#コストなしナップサック最適化) × 1問
- [ソート前の添字復元](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート前の添字復元) × 1問
- [タイリング・LightsOutの解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#タイリング・LightsOutの解の構築) × 1問
- [タイリング・LightsOut可能性判定を領域の細分による不変量計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#タイリング・LightsOut可能性判定を領域の細分による不変量計算に帰着) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ディオファントス方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の構築) × 1問
- [ド・モルガンの法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#ド・モルガンの法則) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [ナップサック分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック分割統治) × 1問
- [ハミルトン路構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#ハミルトン路構築) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#距離空間の重み付きグラフ化) × 1問
- [極限の打ち切り計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#極限の打ち切り計算) × 1問
- [区間max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min更新) × 1問
- [区間max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min取得) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [矩形max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#矩形max・min取得) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [決め打ちによる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#決め打ちによる構築) × 1問
- [交替性転向反応を模した構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#交替性転向反応を模した構築) × 1問
- [行列の階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の階段化) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [最遠点計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最遠点計算) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [始点と終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#始点と終点からの最短経路長計算) × 1問
- [終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#終点からの最短経路長計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [重複選択可ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック割り当て数え上げ) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [小数型の許容誤差付き二分探索・二分法](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型の許容誤差付き二分探索・二分法) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [数列・配列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#数列・配列の構築) × 1問
- [制約からグラフの種類を特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#制約からグラフの種類を特定) × 1問
- [整数の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#整数の構築) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [選択順依存価値ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択順依存価値ナップサック最適化) × 1問
- [双対セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#双対セグメント木) × 1問
- [掃き出し法](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [単調関数のファイバーの緩和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調関数のファイバーの緩和計算) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [二分法](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分法) × 1問
- [半分全列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#半分全列挙) × 1問
- [比の集合の対称性](https://p-adic.github.io/yukicoder-difficulty-statistics/#比の集合の対称性) × 1問
- [非連結なグラフの構築を境界の構築に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#非連結なグラフの構築を境界の構築に帰着) × 1問
- [非連結性を壁の８方向移動による連結性に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#非連結性を壁の８方向移動による連結性に翻訳) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [分割方法数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割方法数え上げ) × 1問
- [文字列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列の構築) × 1問
- [閉路と残りに分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉路と残りに分割) × 1問
- [閉路検出](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉路検出) × 1問
- [偏角ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#偏角ソート) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [累積max・min](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積max・min) × 1問
- [連長圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#連長圧縮) × 1問
- [連立一次不等式の２変数以外を決め打ちして２変数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#連立一次不等式の２変数以外を決め打ちして２変数に帰着) × 1問
- [連立一次不等式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#連立一次不等式の解の構築) × 1問
- [連立一次方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#連立一次方程式の解の構築) × 1問
- [貪欲法による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法による構築) × 1問


## [Kazunさん](https://yukicoder.me/users/11274)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">738</font>](https://yukicoder.me/problems/no/3163)
- [★1／diff <font color="brown">783</font>](https://yukicoder.me/problems/no/2647)
- [★1／diff <font color="green">862</font>](https://yukicoder.me/problems/no/2098)
- [★2／diff <font color="green">812</font>](https://yukicoder.me/problems/no/2306)
- [★2／diff <font color="green">912</font>](https://yukicoder.me/problems/no/2648)
- [★2／diff <font color="deepskyblue">1322</font>](https://yukicoder.me/problems/no/2649)
- [★2／diff <font color="deepskyblue">1345</font>](https://yukicoder.me/problems/no/2307)
- [★2／diff <font color="deepskyblue">1532</font>](https://yukicoder.me/problems/no/3164)
- [★2／diff <font color="deepskyblue">1532</font>](https://yukicoder.me/problems/no/3165)
- [★2／diff <font color="deepskyblue">1577</font>](https://yukicoder.me/problems/no/2100)
- [★2／diff <font color="blue">1730</font>](https://yukicoder.me/problems/no/2099)
- [★2.5／diff <font color="deepskyblue">1448</font>](https://yukicoder.me/problems/no/2650)
- [★2.5／diff <font color="blue">1674</font>](https://yukicoder.me/problems/no/3166)
- [★2.5／diff <font color="blue">1851</font>](https://yukicoder.me/problems/no/2308)
- [★2.5／diff <font color="yellowgreen">2193</font>](https://yukicoder.me/problems/no/2309)
- [★2.5／diff <font color="orange">2401</font>](https://yukicoder.me/problems/no/2581)
- [★2.5／diff <font color="orange">2723</font>](https://yukicoder.me/problems/no/2984)
- [★3／diff <font color="blue">1738</font>](https://yukicoder.me/problems/no/3168)
- [★3／diff <font color="yellowgreen">2004</font>](https://yukicoder.me/problems/no/2652)
- [★3／diff <font color="yellowgreen">2049</font>](https://yukicoder.me/problems/no/2101)
- [★3／diff <font color="yellowgreen">2141</font>](https://yukicoder.me/problems/no/3167)
- [★3／diff <font color="yellowgreen">2247</font>](https://yukicoder.me/problems/no/2653)
- [★3／diff <font color="yellowgreen">2301</font>](https://yukicoder.me/problems/no/2651)
- [★3／diff <font color="yellowgreen">2344</font>](https://yukicoder.me/problems/no/2152)
- [★3.5／diff <font color="blue">1948</font>](https://yukicoder.me/problems/no/2102)
- [★3.5／diff <font color="orange">2464</font>](https://yukicoder.me/problems/no/2310)
- [★3.5／diff <font color="orange">2724</font>](https://yukicoder.me/problems/no/2654)
- [★4／diff <font color="orange">2620</font>](https://yukicoder.me/problems/no/3170)
- [★4／diff <font color="red">2904</font>](https://yukicoder.me/problems/no/3169)
- [★4／diff <font color="red">2920</font>](https://yukicoder.me/problems/no/2311)
- [★5／diff <font color="red">2846</font>](https://yukicoder.me/problems/no/2305)

### 過去問の解法頻度

- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 7問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 6問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 5問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 4問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 3問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 3問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 3問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 3問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 3問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 3問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 2問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 2問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 2問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 2問
- [帰属区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#帰属区間取得) × 2問
- [区間kth取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間kth取得) × 2問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 2問
- [区間代入更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間代入更新) × 2問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 2問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 2問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 2問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 2問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 2問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 2問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 2問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 2問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [Moのアルゴリズム](https://p-adic.github.io/yukicoder-difficulty-statistics/#Moのアルゴリズム) × 1問
- [bitDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitDP) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [getline](https://p-adic.github.io/yukicoder-difficulty-statistics/#getline) × 1問
- [max・min・絶対値による区間クエリを集合管理と一次式の一点更新に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値による区間クエリを集合管理と一次式の一点更新に翻訳) × 1問
- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [sorted set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted set) × 1問
- [★1の64bit整数要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1の64bit整数要求) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [ウノ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#ウノ計算) × 1問
- [クエリソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリソート) × 1問
- [クエリ先読みによる連結リストの成分順前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読みによる連結リストの成分順前計算) × 1問
- [グロタンディーク化](https://p-adic.github.io/yukicoder-difficulty-statistics/#グロタンディーク化) × 1問
- [ジョルダン標準形](https://p-adic.github.io/yukicoder-difficulty-statistics/#ジョルダン標準形) × 1問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 1問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 1問
- [フェルマーの小定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理による逆元計算) × 1問
- [リフルシャッフル](https://p-adic.github.io/yukicoder-difficulty-statistics/#リフルシャッフル) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [ワイルドカードの値を変数化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ワイルドカードの値を変数化) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [円環の倍化実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#円環の倍化実装) × 1問
- [解と係数の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#解と係数の関係) × 1問
- [解の公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#解の公式) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [極小互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#極小互換表示) × 1問
- [区間max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min更新) × 1問
- [区間を切片の差に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を切片の差に翻訳) × 1問
- [区間要素数取得を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得を指定始切片数え上げに帰着) × 1問
- [行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列式計算) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [三平方の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#三平方の定理) × 1問
- [四捨五入計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#四捨五入計算) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [十分大きな法で計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#十分大きな法で計算) × 1問
- [重複選択可ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック最適化) × 1問
- [重複選択個数の線形関係式](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択個数の線形関係式) × 1問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 1問
- [商の剰余計算を大きい法に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#商の剰余計算を大きい法に帰着) × 1問
- [焼きなまし法](https://p-adic.github.io/yukicoder-difficulty-statistics/#焼きなまし法) × 1問
- [剰余による確率的判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余による確率的判定) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [遷移の収束](https://p-adic.github.io/yukicoder-difficulty-statistics/#遷移の収束) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [組分けの余りに注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#組分けの余りに注目) × 1問
- [双対セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#双対セグメント木) × 1問
- [多次元コストナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元コストナップサック最適化) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [楕円の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#楕円の面積計算) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [代数拡大](https://p-adic.github.io/yukicoder-difficulty-statistics/#代数拡大) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [二次拡大](https://p-adic.github.io/yukicoder-difficulty-statistics/#二次拡大) × 1問
- [配列の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列の変化イベント走査による差分計算) × 1問
- [半分全列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#半分全列挙) × 1問
- [汎関数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#汎関数計算) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [複素共役による絶対値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#複素共役による絶対値計算) × 1問
- [複素数演算](https://p-adic.github.io/yukicoder-difficulty-statistics/#複素数演算) × 1問
- [文字列・配列の追加・挿入の事前処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列・配列の追加・挿入の事前処理) × 1問
- [平方分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方分割) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [余因子展開](https://p-adic.github.io/yukicoder-difficulty-statistics/#余因子展開) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問
- [離散対数問題](https://p-adic.github.io/yukicoder-difficulty-statistics/#離散対数問題) × 1問
- [隣接不等式管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#隣接不等式管理) × 1問
- [連結リスト](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結リスト) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問


## [netyo715さん](https://yukicoder.me/users/11468)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="orange">2401</font>](https://yukicoder.me/problems/no/2585)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [変数の対称性](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数の対称性) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [amesyuさん](https://yukicoder.me/users/11512)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">357</font>](https://yukicoder.me/problems/no/3203)
- [★2／diff <font color="green">1133</font>](https://yukicoder.me/problems/no/3204)
- [★2／diff <font color="deepskyblue">1535</font>](https://yukicoder.me/problems/no/2928)
- [★2.5／diff <font color="green">1133</font>](https://yukicoder.me/problems/no/3205)
- [★3.5／diff <font color="blue">1774</font>](https://yukicoder.me/problems/no/3206)
- [★3.5／diff <font color="orange">2562</font>](https://yukicoder.me/problems/no/3207)
- [★4／diff <font color="yellowgreen">2352</font>](https://yukicoder.me/problems/no/3208)

### 過去問の解法頻度

- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 1問
- [★1.5以下の高校２年生以上の数学知識要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高校２年生以上の数学知識要求) × 1問
- [★1の高校以上の数学知識要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1の高校以上の数学知識要求) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [円周率の無理数性](https://p-adic.github.io/yukicoder-difficulty-statistics/#円周率の無理数性) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [経路全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路全探索) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全方位木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#全方位木DP) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [木の根の変更における頂点の高さと深さの関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の根の変更における頂点の高さと深さの関係) × 1問
- [木の頂点の高さ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の頂点の高さ計算) × 1問
- [木の頂点の深さ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の頂点の深さ計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問


## [Kanten4205さん](https://yukicoder.me/users/11588)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1578</font>](https://yukicoder.me/problems/no/2374)

### 過去問の解法頻度

- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [門松列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#門松列DP) × 1問


## [tnodinoさん](https://yukicoder.me/users/11714)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">1008</font>](https://yukicoder.me/problems/no/2924)
- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2932)
- [★3／diffデータなし](https://yukicoder.me/problems/no/2934)

### 過去問の解法頻度

- [01列とグリッド上の経路の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列とグリッド上の経路の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [スタック](https://p-adic.github.io/yukicoder-difficulty-statistics/#スタック) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [指定序数の値の計算を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を指定始切片数え上げに帰着) × 1問
- [上界制約を無視した数え上げを桁ごとに前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#上界制約を無視した数え上げを桁ごとに前計算) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [単調列数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調列数え上げ) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [入れ子の深さを記録する走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#入れ子の深さを記録する走査) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [連結リスト](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結リスト) × 1問
- [連長圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#連長圧縮) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [遭難者さん](https://yukicoder.me/users/11797)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">1158</font>](https://yukicoder.me/problems/no/2124)
- [★2／diff <font color="deepskyblue">1397</font>](https://yukicoder.me/problems/no/2358)
- [★2.5／diff <font color="blue">1743</font>](https://yukicoder.me/problems/no/2357)
- [★2.5／diff <font color="blue">1803</font>](https://yukicoder.me/problems/no/2126)
- [★2.5／diff <font color="yellowgreen">2291</font>](https://yukicoder.me/problems/no/2125)
- [★3／diff <font color="blue">1696</font>](https://yukicoder.me/problems/no/2065)
- [★3／diff <font color="yellowgreen">2165</font>](https://yukicoder.me/problems/no/2359)
- [★3／diff <font color="yellowgreen">2322</font>](https://yukicoder.me/problems/no/2360)
- [★3／diff <font color="yellowgreen">2393</font>](https://yukicoder.me/problems/no/2127)
- [★3／diff <font color="orange">2430</font>](https://yukicoder.me/problems/no/2128)
- [★3／diff <font color="orange">2566</font>](https://yukicoder.me/problems/no/2068)
- [★3.5／diff <font color="orange">2721</font>](https://yukicoder.me/problems/no/2361)
- [★3.5／diff <font color="red">2892</font>](https://yukicoder.me/problems/no/2129)
- [★4.5／diff <font color="darkgoldenrod ">3487</font>](https://yukicoder.me/problems/no/2362)

### 過去問の解法頻度

- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 4問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 3問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 2問
- [ディオファントス方程式の因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の因数分解) × 2問
- [ディオファントス方程式の求解](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の求解) × 2問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 2問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 2問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 2問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 2問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 2問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 2問
- [平方分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方分割) × 2問
- [変数の対称性](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数の対称性) × 2問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 2問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [クエリソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリソート) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [一次式のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式のリアクティブによる特定) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [互いに素に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#互いに素に帰着) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [順列のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#順列のリアクティブによる特定) × 1問
- [商のfloorの値ごとに纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの値ごとに纏め上げ) × 1問
- [商のfloorの分子を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの分子を止める総和計算) × 1問
- [上限・下限値に言及する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#上限・下限値に言及する質問) × 1問
- [剰余の被除数を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余の被除数を止める総和計算) × 1問
- [剰余の法を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余の法を止める総和計算) × 1問
- [剰余を商のfloorに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余を商のfloorに翻訳) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [整数のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#整数のリアクティブによる特定) × 1問
- [全方位木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#全方位木DP) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和計算の期待値への帰着) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [非単射関数の値で纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の値で纏め上げ) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [Cyanmondさん](https://yukicoder.me/users/11820)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4.5／diff <font color="red">3181</font>](https://yukicoder.me/problems/no/2491)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [shiomusubi496さん](https://yukicoder.me/users/11821)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1706</font>](https://yukicoder.me/problems/no/2481)
- [★4／diff <font color="orange">2587</font>](https://yukicoder.me/problems/no/2488)

### 過去問の解法頻度

- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問


## [Kak1_n0_taneさん](https://yukicoder.me/users/11842)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1887</font>](https://yukicoder.me/problems/no/2365)
- [★3.5／diff <font color="orange">2627</font>](https://yukicoder.me/problems/no/2369)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [素数列による試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列による試し割り法) × 1問
- [不明な想定解](https://p-adic.github.io/yukicoder-difficulty-statistics/#不明な想定解) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [約数の走査を倍数の走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の走査を倍数の走査に帰着) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [ygussanyさん](https://yukicoder.me/users/12049)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4／diff <font color="darkgoldenrod ">3309</font>](https://yukicoder.me/problems/no/2998)

### 過去問の解法頻度

- [グラフの構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの構築) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [彩色の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#彩色の構築) × 1問
- [全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全域木計算) × 1問
- [全域有向木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全域有向木計算) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [虹色全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#虹色全域木計算) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [木の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の構築) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [bayashikoさん](https://yukicoder.me/users/12073)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">689</font>](https://yukicoder.me/problems/no/2246)
- [★1.5／diff <font color="green">1095</font>](https://yukicoder.me/problems/no/2109)
- [★2／diff <font color="green">1095</font>](https://yukicoder.me/problems/no/2110)
- [★2.5／diff <font color="deepskyblue">1206</font>](https://yukicoder.me/problems/no/2111)
- [★2.5／diff <font color="blue">1604</font>](https://yukicoder.me/problems/no/2247)
- [★3／diff <font color="blue">1861</font>](https://yukicoder.me/problems/no/2248)
- [★3／diff <font color="blue">1983</font>](https://yukicoder.me/problems/no/2249)
- [★3／diff <font color="yellowgreen">2039</font>](https://yukicoder.me/problems/no/2112)
- [★3／diff <font color="yellowgreen">2168</font>](https://yukicoder.me/problems/no/2113)
- [★3／diff <font color="yellowgreen">2170</font>](https://yukicoder.me/problems/no/2250)
- [★3.5／diff <font color="orange">2535</font>](https://yukicoder.me/problems/no/2251)
- [★3.5／diff <font color="red">2833</font>](https://yukicoder.me/problems/no/2115)
- [★3.5／diff <font color="darkgoldenrod ">3384</font>](https://yukicoder.me/problems/no/2114)
- [★4.5／diff <font color="darkgoldenrod ">3384</font>](https://yukicoder.me/problems/no/2116)

### 過去問の解法頻度

- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 5問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 4問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 2問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 2問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [オイラー関数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラー関数計算) × 1問
- [カレンダー計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カレンダー計算) × 1問
- [サンプルに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルに帰着) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の構築) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [最短完全二部マッチング計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短完全二部マッチング計算) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [指定序数の値の計算を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を指定始切片数え上げに帰着) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [重複選択可ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック最適化) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [組分けの余りに注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#組分けの余りに注目) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和計算の期待値への帰着) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多次元コストナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元コストナップサック最適化) × 1問
- [転倒数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#転倒数計算) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [配列の成分のシフトを添え字のシフトに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列の成分のシフトを添え字のシフトに翻訳) × 1問
- [配列の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列の変化イベント走査による差分計算) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [倍数走査によるオイラー関数前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数走査によるオイラー関数前計算) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [約数の走査を倍数の走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の走査を倍数の走査に帰着) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [magstaさん](https://yukicoder.me/users/12114)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1683</font>](https://yukicoder.me/problems/no/2277)
- [★3／diff <font color="yellowgreen">2153</font>](https://yukicoder.me/problems/no/2279)
- [★4／diff <font color="red">2905</font>](https://yukicoder.me/problems/no/2281)

### 過去問の解法頻度

- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 1問
- [bool値の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#bool値の充足可能性判定) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [ディオファントス方程式の解の数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の数え上げ) × 1問
- [ポテンシャル付き素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポテンシャル付き素集合データ構造) × 1問
- [区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [頂点倍化](https://p-adic.github.io/yukicoder-difficulty-statistics/#頂点倍化) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二部グラフ判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#二部グラフ判定) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [法B係数連立一次方程式の解の数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の数え上げ) × 1問
- [法B係数連立一次方程式の解の存在判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の存在判定) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [だれさん](https://yukicoder.me/users/12179)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diffデータなし](https://yukicoder.me/problems/no/2467)
- [★2／diff <font color="green">939</font>](https://yukicoder.me/problems/no/2233)
- [★2／diff <font color="deepskyblue">1447</font>](https://yukicoder.me/problems/no/2682)
- [★2.5／diff <font color="blue">1839</font>](https://yukicoder.me/problems/no/2528)
- [★3／diffデータなし](https://yukicoder.me/problems/no/2477)
- [★3／diff <font color="yellowgreen">2245</font>](https://yukicoder.me/problems/no/2134)
- [★3.5／diffデータなし](https://yukicoder.me/problems/no/2085)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 2問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [B進法位取り記法と法Bベクトルの対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#B進法位取り記法と法Bベクトルの対応) × 1問
- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [bitset高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitset高速化) × 1問
- [bit演算による$64$並列](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit演算による$64$並列) × 1問
- [breakに関する考察](https://p-adic.github.io/yukicoder-difficulty-statistics/#breakに関する考察) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [ハミルトン路構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#ハミルトン路構築) × 1問
- [ポラードの$\rho$](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポラードの$\rho$) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [階数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階数計算) × 1問
- [基底に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#基底に帰着) × 1問
- [基底計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#基底計算) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列の階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の階段化) × 1問
- [行列の簡約階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の簡約階段化) × 1問
- [最小公倍数の約数関係判定を最大公約数の最小公倍数計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小公倍数の約数関係判定を最大公約数の最小公倍数計算に帰着) × 1問
- [最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小公倍数計算) × 1問
- [最大公約数による最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数による最小公倍数計算) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [次元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#次元計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [集合族による帰属関係で類別](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合族による帰属関係で類別) × 1問
- [線形空間の数え上げを次元計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形空間の数え上げを次元計算に帰着) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [遷移の収束](https://p-adic.github.io/yukicoder-difficulty-statistics/#遷移の収束) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [掃き出し法](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [多項定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項定理) × 1問
- [同値関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#同値関係) × 1問
- [二・多項係数を組み合わせに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#二・多項係数を組み合わせに翻訳) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [辺を頂点とするグラフに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#辺を頂点とするグラフに翻訳) × 1問


## [H20さん](https://yukicoder.me/users/12388)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">769</font>](https://yukicoder.me/problems/no/2201)
- [★2／diff <font color="deepskyblue">1254</font>](https://yukicoder.me/problems/no/2202)
- [★2／diff <font color="yellowgreen">2121</font>](https://yukicoder.me/problems/no/2591)
- [★2.5／diff <font color="blue">1842</font>](https://yukicoder.me/problems/no/2576)

### 過去問の解法頻度

- [bool値の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#bool値の充足可能性判定) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [ポテンシャル付き素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポテンシャル付き素集合データ構造) × 1問
- [括弧列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#括弧列DP) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [頂点倍化](https://p-adic.github.io/yukicoder-difficulty-statistics/#頂点倍化) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [二部グラフ判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#二部グラフ判定) × 1問
- [入れ子の深さを記録する走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#入れ子の深さを記録する走査) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [閉じた括弧列判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉じた括弧列判定) × 1問
- [法B係数連立一次方程式の解の存在判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の存在判定) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [karinohitoさん](https://yukicoder.me/users/12457)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1258</font>](https://yukicoder.me/problems/no/2260)
- [★2.5／diff <font color="deepskyblue">1536</font>](https://yukicoder.me/problems/no/2261)
- [★3／diff <font color="red">2944</font>](https://yukicoder.me/problems/no/2698)

### 過去問の解法頻度

- [$45$度回転](https://p-adic.github.io/yukicoder-difficulty-statistics/#$45$度回転) × 1問
- [convex hull trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#convex hull trick) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [slope trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#slope trick) × 1問
- [一次式の族の最大・最小値取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の族の最大・最小値取得) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [最遠点計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最遠点計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分計算) × 1問
- [符号全探索による絶対値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#符号全探索による絶対値計算) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [PCTprobabilityさん](https://yukicoder.me/users/12482)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="blue">1951</font>](https://yukicoder.me/problems/no/2529)
- [★3.5／diff <font color="orange">2673</font>](https://yukicoder.me/problems/no/2164)
- [★4／diff <font color="orange">2791</font>](https://yukicoder.me/problems/no/2514)
- [★4／diff <font color="red">2804</font>](https://yukicoder.me/problems/no/2391)

### 過去問の解法頻度

- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [データ構造をマージする一般的なテク](https://p-adic.github.io/yukicoder-difficulty-statistics/#データ構造をマージする一般的なテク) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [演算の反復の分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#演算の反復の分割統治) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問


## [Nachiaさん](https://yukicoder.me/users/12532)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">222</font>](https://yukicoder.me/problems/no/2460)
- [★1.5／diff <font color="green">959</font>](https://yukicoder.me/problems/no/2461)
- [★2.5／diff <font color="deepskyblue">1358</font>](https://yukicoder.me/problems/no/2462)
- [★2.5／diff <font color="blue">1838</font>](https://yukicoder.me/problems/no/2463)
- [★3／diff <font color="red">2852</font>](https://yukicoder.me/problems/no/2172)
- [★3.5／diff <font color="orange">2470</font>](https://yukicoder.me/problems/no/2464)
- [★3.5／diff <font color="red">2960</font>](https://yukicoder.me/problems/no/2584)
- [★4.5／diff <font color="red">3115</font>](https://yukicoder.me/problems/no/2985)
- [★5／diffデータなし](https://yukicoder.me/problems/no/2465)
- [★5／diff <font color="darkgoldenrod ">3309</font>](https://yukicoder.me/problems/no/2987)
- [★5／diff <font color="darkgoldenrod ">3382</font>](https://yukicoder.me/problems/no/2160)
- [★5.5／diffデータなし](https://yukicoder.me/problems/no/2258)

### 過去問の解法頻度

- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 3問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 2問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [01列の累積和との内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列の累積和との内積計算) × 1問
- [COMPLETE法](https://p-adic.github.io/yukicoder-difficulty-statistics/#COMPLETE法) × 1問
- [cyclic orderつき全方位木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#cyclic orderつき全方位木DP) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [グラフの頂点の次数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの頂点の次数計算) × 1問
- [ディオファントス方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の構築) × 1問
- [トポロジカルソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#トポロジカルソート) × 1問
- [ド・モルガンの法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#ド・モルガンの法則) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [階数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階数計算) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [強連結成分分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#強連結成分分解) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [行列の簡約階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の簡約階段化) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [最小辺彩色数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小辺彩色数計算) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [最長共通接頭辞計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最長共通接頭辞計算) × 1問
- [彩色の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#彩色の構築) × 1問
- [山登り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#山登り法) × 1問
- [残余ネットワーク](https://p-adic.github.io/yukicoder-difficulty-statistics/#残余ネットワーク) × 1問
- [試行回数・順位の期待値を各試行の実施確率・各項の先着確率の和に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#試行回数・順位の期待値を各試行の実施確率・各項の先着確率の和に帰着) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [制約からグラフの種類を特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#制約からグラフの種類を特定) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [選択肢の分割・纏め上げ・追加で良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択肢の分割・纏め上げ・追加で良いケースに帰着) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [全方位木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#全方位木DP) × 1問
- [掃き出し法](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [探索・求解アルゴリズムによる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#探索・求解アルゴリズムによる構築) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [等差数列との内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列との内積計算) × 1問
- [等比数列との内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列との内積計算) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [同値関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#同値関係) × 1問
- [内積と転置の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積と転置の関係) × 1問
- [内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積計算) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [部分グラフ数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分グラフ数え上げ) × 1問
- [複数ナップサック割り当て可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数ナップサック割り当て可能性判定) × 1問
- [複数配列への範囲加算更新を１つの配列に纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数配列への範囲加算更新を１つの配列に纏め上げ) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [法B係数連立一次方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の構築) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [有向辺反転](https://p-adic.github.io/yukicoder-difficulty-statistics/#有向辺反転) × 1問
- [誘導部分グラフ数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#誘導部分グラフ数え上げ) × 1問
- [誘導部分グラフ数え上げを部分グラフ数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#誘導部分グラフ数え上げを部分グラフ数え上げに帰着) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [suisenさん](https://yukicoder.me/users/12562)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1204</font>](https://yukicoder.me/problems/no/2663)
- [★2／diff <font color="deepskyblue">1274</font>](https://yukicoder.me/problems/no/3048)
- [★2／diff <font color="deepskyblue">1301</font>](https://yukicoder.me/problems/no/2664)
- [★2.5／diff <font color="deepskyblue">1480</font>](https://yukicoder.me/problems/no/3049)
- [★2.5／diff <font color="deepskyblue">1540</font>](https://yukicoder.me/problems/no/2665)
- [★2.5／diff <font color="blue">1996</font>](https://yukicoder.me/problems/no/2500)
- [★2.5／diff <font color="yellowgreen">2064</font>](https://yukicoder.me/problems/no/2501)
- [★2.5／diff <font color="orange">2503</font>](https://yukicoder.me/problems/no/2502)
- [★3／diff <font color="blue">1976</font>](https://yukicoder.me/problems/no/3050)
- [★3.5／diff <font color="yellowgreen">2152</font>](https://yukicoder.me/problems/no/2666)
- [★3.5／diff <font color="yellowgreen">2330</font>](https://yukicoder.me/problems/no/2667)
- [★3.5／diff <font color="yellowgreen">2359</font>](https://yukicoder.me/problems/no/2668)
- [★3.5／diff <font color="orange">2552</font>](https://yukicoder.me/problems/no/2504)
- [★3.5／diff <font color="orange">2603</font>](https://yukicoder.me/problems/no/2503)
- [★3.5／diff <font color="orange">2622</font>](https://yukicoder.me/problems/no/3051)
- [★3.5／diff <font color="orange">2622</font>](https://yukicoder.me/problems/no/3052)
- [★3.5／diff <font color="red">3048</font>](https://yukicoder.me/problems/no/2505)
- [★4／diff <font color="orange">2795</font>](https://yukicoder.me/problems/no/2578)
- [★4／diff <font color="red">2894</font>](https://yukicoder.me/problems/no/2507)
- [★4／diff <font color="red">2917</font>](https://yukicoder.me/problems/no/3053)
- [★4／diff <font color="red">2935</font>](https://yukicoder.me/problems/no/2669)
- [★4／diff <font color="red">2935</font>](https://yukicoder.me/problems/no/2670)
- [★4／diff <font color="red">3144</font>](https://yukicoder.me/problems/no/3054)
- [★4／diff <font color="red">3145</font>](https://yukicoder.me/problems/no/2506)
- [★4／diff <font color="darkgoldenrod ">3335</font>](https://yukicoder.me/problems/no/3055)

### 過去問の解法頻度

- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 4問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 3問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 3問
- [最適化を各寄与の最適化に緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#最適化を各寄与の最適化に緩和) × 2問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [01列の累積和との内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列の累積和との内積計算) × 1問
- [OR畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#OR畳み込み) × 1問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 1問
- [bool値の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#bool値の充足可能性判定) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ変換) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [ポテンシャル付き素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポテンシャル付き素集合データ構造) × 1問
- [ポラードの$\rho$](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポラードの$\rho$) × 1問
- [メビウスの反転公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウスの反転公式) × 1問
- [メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウス変換) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [位取り記法による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法による構築) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [決め打ちによる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#決め打ちによる構築) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の構築) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [高速ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速ゼータ変換) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#終点からの最短経路長計算) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [上限・下限値に言及する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#上限・下限値に言及する質問) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [頂点倍化](https://p-adic.github.io/yukicoder-difficulty-statistics/#頂点倍化) × 1問
- [転倒数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#転倒数計算) × 1問
- [等差数列の累積和との内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和との内積計算) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [内積と転置の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積と転置の関係) × 1問
- [内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積計算) × 1問
- [二部グラフ判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#二部グラフ判定) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [必勝戦略のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#必勝戦略のリアクティブによる特定) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [分割の均等化](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割の均等化) × 1問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [変数の対称性](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数の対称性) × 1問
- [法B係数連立一次方程式の解の存在判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の存在判定) × 1問
- [約数ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数ゼータ変換) × 1問
- [約数メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数メビウス変換) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問


## [hibit_atさん](https://yukicoder.me/users/12664)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">313</font>](https://yukicoder.me/problems/no/2371)
- [★1.5／diff <font color="brown">566</font>](https://yukicoder.me/problems/no/2153)
- [★1.5／diff <font color="green">885</font>](https://yukicoder.me/problems/no/2691)
- [★2.5／diff <font color="deepskyblue">1220</font>](https://yukicoder.me/problems/no/2156)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [カレンダー計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カレンダー計算) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [門松列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#門松列DP) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [potato167さん](https://yukicoder.me/users/13086)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="orange">2478</font>](https://yukicoder.me/problems/no/2989)
- [★3／diff <font color="orange">2666</font>](https://yukicoder.me/problems/no/3138)
- [★3.5／diff <font color="orange">2433</font>](https://yukicoder.me/problems/no/3025)
- [★3.5／diff <font color="orange">2681</font>](https://yukicoder.me/problems/no/2633)
- [★3.5／diff <font color="red">2990</font>](https://yukicoder.me/problems/no/2635)
- [★4／diffデータなし](https://yukicoder.me/problems/no/3139)
- [★4／diff <font color="orange">2519</font>](https://yukicoder.me/problems/no/2237)
- [★4／diff <font color="red">2954</font>](https://yukicoder.me/problems/no/3026)

### 過去問の解法頻度

- [01列と括弧列の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と括弧列の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [グラフの辺の削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の削除更新) × 1問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 1問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 1問
- [フィボナッチ数列の法B周期計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フィボナッチ数列の法B周期計算) × 1問
- [フィボナッチ数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フィボナッチ数列の累積和計算) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間を切片の差に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を切片の差に翻訳) × 1問
- [区間和の指定された区間数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和の指定された区間数え上げ) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [辞書順最小01部分列計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#辞書順最小01部分列計算) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [平方分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方分割) × 1問
- [隣接頂点和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#隣接頂点和取得) × 1問
- [累積積による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による二項係数計算) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [NokonoKotlinさん](https://yukicoder.me/users/13116)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="deepskyblue">1416</font>](https://yukicoder.me/problems/no/2672)
- [★3.5／diff <font color="orange">2615</font>](https://yukicoder.me/problems/no/2678)
- [★3.5／diff <font color="orange">2662</font>](https://yukicoder.me/problems/no/2676)

### 過去問の解法頻度

- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問


## [tassei903さん](https://yukicoder.me/users/13452)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">1124</font>](https://yukicoder.me/problems/no/2629)
- [★2／diff <font color="deepskyblue">1366</font>](https://yukicoder.me/problems/no/2740)
- [★2.5／diff <font color="blue">1969</font>](https://yukicoder.me/problems/no/2742)
- [★2.5／diff <font color="yellowgreen">2191</font>](https://yukicoder.me/problems/no/2432)
- [★3.5／diff <font color="yellowgreen">2345</font>](https://yukicoder.me/problems/no/2747)

### 過去問の解法頻度

- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 2問
- [サンプルから推測](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルから推測) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小公倍数計算) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [最大公約数による最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数による最小公倍数計算) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [遷移の収束](https://p-adic.github.io/yukicoder-difficulty-statistics/#遷移の収束) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [反射の倍化実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#反射の倍化実装) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [連結リスト](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結リスト) × 1問


## [milkcoffeeさん](https://yukicoder.me/users/13469)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="green">864</font>](https://yukicoder.me/problems/no/2140)
- [★2／diff <font color="green">819</font>](https://yukicoder.me/problems/no/2835)
- [★2／diff <font color="deepskyblue">1356</font>](https://yukicoder.me/problems/no/2141)
- [★2.5／diff <font color="deepskyblue">1318</font>](https://yukicoder.me/problems/no/2836)
- [★2.5／diff <font color="blue">1606</font>](https://yukicoder.me/problems/no/2143)
- [★2.5／diff <font color="blue">1632</font>](https://yukicoder.me/problems/no/2142)
- [★3／diff <font color="yellowgreen">2305</font>](https://yukicoder.me/problems/no/2838)
- [★3／diff <font color="orange">2420</font>](https://yukicoder.me/problems/no/2263)
- [★3／diff <font color="orange">2648</font>](https://yukicoder.me/problems/no/2839)
- [★3.5／diff <font color="yellowgreen">2099</font>](https://yukicoder.me/problems/no/2837)
- [★3.5／diff <font color="yellowgreen">2357</font>](https://yukicoder.me/problems/no/2840)
- [★3.5／diff <font color="orange">2500</font>](https://yukicoder.me/problems/no/2144)
- [★3.5／diff <font color="red">2915</font>](https://yukicoder.me/problems/no/2145)
- [★4／diff <font color="red">2866</font>](https://yukicoder.me/problems/no/2146)
- [★4／diff <font color="red">2872</font>](https://yukicoder.me/problems/no/2841)

### 過去問の解法頻度

- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 4問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 2問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [サンプルから推測](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルから推測) × 1問
- [タイリング・LightsOutの解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#タイリング・LightsOutの解の構築) × 1問
- [タイリング・LightsOut可能性判定を領域の細分による不変量計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#タイリング・LightsOut可能性判定を領域の細分による不変量計算に帰着) × 1問
- [フロー](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロー) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [階乗による多項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による多項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [完全二部マッチング](https://p-adic.github.io/yukicoder-difficulty-statistics/#完全二部マッチング) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間和の指定された区間数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和の指定された区間数え上げ) × 1問
- [交代和](https://p-adic.github.io/yukicoder-difficulty-statistics/#交代和) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [最大二部マッチング](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大二部マッチング) × 1問
- [三角形の成立条件](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の成立条件) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項係数計算) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [超頂点追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#超頂点追加) × 1問
- [到達可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#到達可能性判定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同値関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#同値関係) × 1問
- [分割の均等化](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割の均等化) × 1問
- [閉じた括弧列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉じた括弧列の構築) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問


## [hahhoさん](https://yukicoder.me/users/13612)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="orange">2799</font>](https://yukicoder.me/problems/no/2901)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [とりゐさん](https://yukicoder.me/users/13891)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">969</font>](https://yukicoder.me/problems/no/2063)
- [★2.5／diff <font color="deepskyblue">1582</font>](https://yukicoder.me/problems/no/2064)
- [★2.5／diff <font color="orange">2533</font>](https://yukicoder.me/problems/no/2991)
- [★3.5／diffデータなし](https://yukicoder.me/problems/no/2313)
- [★3.5／diff <font color="yellowgreen">2381</font>](https://yukicoder.me/problems/no/2206)
- [★3.5／diff <font color="orange">2401</font>](https://yukicoder.me/problems/no/2582)
- [★3.5／diff <font color="orange">2648</font>](https://yukicoder.me/problems/no/2066)
- [★3.5／diff <font color="orange">2737</font>](https://yukicoder.me/problems/no/2067)
- [★4／diff <font color="red">3018</font>](https://yukicoder.me/problems/no/2262)
- [★4／diff <font color="red">3138</font>](https://yukicoder.me/problems/no/2265)
- [★4.5／diffデータなし](https://yukicoder.me/problems/no/2266)

### 過去問の解法頻度

- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 3問
- [指定序数の値の計算を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を指定始切片数え上げに帰着) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [Moのアルゴリズム](https://p-adic.github.io/yukicoder-difficulty-statistics/#Moのアルゴリズム) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ変換) × 1問
- [テイラー展開](https://p-adic.github.io/yukicoder-difficulty-statistics/#テイラー展開) × 1問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 1問
- [フビニの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フビニの定理) × 1問
- [フロベニウス数に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロベニウス数に注目) × 1問
- [メビウスの反転公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウスの反転公式) × 1問
- [メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウス変換) × 1問
- [メモ化再帰の計算量を再帰深度で評価する考察](https://p-adic.github.io/yukicoder-difficulty-statistics/#メモ化再帰の計算量を再帰深度で評価する考察) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [互いに素に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#互いに素に帰着) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の構築) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰的構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構築) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [商のfloorの分母を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの分母を止める総和計算) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [積分漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#積分漸化式) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [多項定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項定理) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [二項係数の第２引数を渡る総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数の第２引数を渡る総和計算) × 1問
- [倍数走査による約数列挙前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数走査による約数列挙前計算) × 1問
- [比の集合の対称性](https://p-adic.github.io/yukicoder-difficulty-statistics/#比の集合の対称性) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [平方分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方分割) × 1問
- [約数ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数ゼータ変換) × 1問
- [約数メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数メビウス変換) × 1問
- [約数走査を倍数走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数走査を倍数走査に帰着) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [ramdosさん](https://yukicoder.me/users/13949)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">427</font>](https://yukicoder.me/problems/no/3107)
- [★2／diff <font color="deepskyblue">1449</font>](https://yukicoder.me/problems/no/2430)
- [★2／diff <font color="blue">1624</font>](https://yukicoder.me/problems/no/2638)
- [★2／diff <font color="blue">1909</font>](https://yukicoder.me/problems/no/2150)

### 過去問の解法頻度

- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [グラフの頂点の次数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの頂点の次数計算) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#包除原理) × 1問


## [matcharate12さん](https://yukicoder.me/users/14008)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">1132</font>](https://yukicoder.me/problems/no/2766)
- [★2／diffデータなし](https://yukicoder.me/problems/no/2636)
- [★2／diff <font color="deepskyblue">1565</font>](https://yukicoder.me/problems/no/2759)
- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2646)
- [★2.5／diff <font color="blue">1659</font>](https://yukicoder.me/problems/no/2758)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [グラフの状態や目的地の変化を有向辺に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの状態や目的地の変化を有向辺に翻訳) × 2問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 2問
- [01BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#01BFS) × 1問
- [クエリソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリソート) × 1問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ソート前の添字復元](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート前の添字復元) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間を切片の差に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を切片の差に翻訳) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [最小素因数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小素因数計算) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [整礎性](https://p-adic.github.io/yukicoder-difficulty-statistics/#整礎性) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 1問
- [到達可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#到達可能性判定) × 1問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [倍数判定を約数列挙に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数判定を約数列挙に帰着) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [約数計数関数による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数計数関数による計算量評価) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問


## [cho435さん](https://yukicoder.me/users/14113)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">216</font>](https://yukicoder.me/problems/no/2736)
- [★2／diff <font color="blue">1695</font>](https://yukicoder.me/problems/no/2739)
- [★3.5／diff <font color="orange">2628</font>](https://yukicoder.me/problems/no/2436)
- [★3.5／diff <font color="orange">2670</font>](https://yukicoder.me/problems/no/2644)

### 過去問の解法頻度

- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [多次元コストを一次元に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元コストを一次元に翻訳) × 1問


## [Shirotsumeさん](https://yukicoder.me/users/14227)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">331</font>](https://yukicoder.me/problems/no/2297)
- [★1／diff <font color="brown">443</font>](https://yukicoder.me/problems/no/2208)
- [★1.5／diff <font color="green">813</font>](https://yukicoder.me/problems/no/2298)
- [★1.5／diff <font color="deepskyblue">1314</font>](https://yukicoder.me/problems/no/2196)
- [★2／diff <font color="brown">606</font>](https://yukicoder.me/problems/no/2541)
- [★2／diff <font color="green">1008</font>](https://yukicoder.me/problems/no/2209)
- [★2／diff <font color="green">1049</font>](https://yukicoder.me/problems/no/2299)
- [★2／diff <font color="green">1093</font>](https://yukicoder.me/problems/no/2195)
- [★2.5／diff <font color="deepskyblue">1257</font>](https://yukicoder.me/problems/no/2300)
- [★2.5／diff <font color="deepskyblue">1469</font>](https://yukicoder.me/problems/no/2542)
- [★2.5／diff <font color="deepskyblue">1488</font>](https://yukicoder.me/problems/no/2518)
- [★2.5／diff <font color="deepskyblue">1489</font>](https://yukicoder.me/problems/no/2210)
- [★2.5／diff <font color="deepskyblue">1499</font>](https://yukicoder.me/problems/no/2301)
- [★2.5／diff <font color="blue">1607</font>](https://yukicoder.me/problems/no/2211)
- [★3／diff <font color="blue">1959</font>](https://yukicoder.me/problems/no/2139)
- [★3／diff <font color="blue">1985</font>](https://yukicoder.me/problems/no/2543)
- [★3／diff <font color="yellowgreen">2086</font>](https://yukicoder.me/problems/no/2213)
- [★3／diff <font color="yellowgreen">2348</font>](https://yukicoder.me/problems/no/2586)
- [★3／diff <font color="yellowgreen">2357</font>](https://yukicoder.me/problems/no/2521)
- [★3／diff <font color="orange">2424</font>](https://yukicoder.me/problems/no/2214)
- [★3.5／diff <font color="blue">1971</font>](https://yukicoder.me/problems/no/2212)
- [★3.5／diff <font color="yellowgreen">2154</font>](https://yukicoder.me/problems/no/2544)
- [★3.5／diff <font color="yellowgreen">2166</font>](https://yukicoder.me/problems/no/2302)
- [★3.5／diff <font color="yellowgreen">2191</font>](https://yukicoder.me/problems/no/2303)
- [★3.5／diff <font color="orange">2436</font>](https://yukicoder.me/problems/no/2524)
- [★3.5／diff <font color="orange">2612</font>](https://yukicoder.me/problems/no/2545)
- [★3.5／diff <font color="orange">2775</font>](https://yukicoder.me/problems/no/2546)
- [★4／diff <font color="orange">2532</font>](https://yukicoder.me/problems/no/2304)
- [★4／diff <font color="orange">2658</font>](https://yukicoder.me/problems/no/2215)

### 過去問の解法頻度

- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 4問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 4問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 3問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 3問
- [ド・モルガンの法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#ド・モルガンの法則) × 2問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 2問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 2問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 2問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 2問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 2問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 2問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 2問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [sorted set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted set) × 1問
- [キュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#キュー) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [サンプルから推測](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルから推測) × 1問
- [サンプルに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルに帰着) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [シュトルツ・チェザロの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#シュトルツ・チェザロの定理) × 1問
- [スライド最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#スライド最大・最小化) × 1問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 1問
- [ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ変換) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ダブリング](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダブリング) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [メビウスの反転公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウスの反転公式) × 1問
- [メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウス変換) × 1問
- [移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動回数の期待値を距離で割った値の極限計算を平均移動速度に帰着) × 1問
- [一次式の最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の最大・最小値計算) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [確率漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#確率漸化式) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#距離空間の重み付きグラフ化) × 1問
- [区間max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min取得) × 1問
- [区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮) × 1問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 1問
- [区間スケジューリング](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間スケジューリング) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の構築) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [再帰的構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構築) × 1問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [最適遷移を自己写像に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#最適遷移を自己写像に翻訳) × 1問
- [試行回数・順位の期待値を各試行の実施確率・各項の先着確率の和に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#試行回数・順位の期待値を各試行の実施確率・各項の先着確率の和に帰着) × 1問
- [自己写像に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#自己写像に翻訳) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [重複選択可ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック最適化) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [制約からグラフの種類を特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#制約からグラフの種類を特定) × 1問
- [組分けの余りに注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#組分けの余りに注目) × 1問
- [挿入ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#挿入ソート) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [倍数ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数ゼータ変換) × 1問
- [倍数メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数メビウス変換) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [部分和と補部分和の差の最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分和と補部分和の差の最大・最小化) × 1問
- [部分和の差の最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分和の差の最大・最小化) × 1問
- [閉路と残りに分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉路と残りに分割) × 1問
- [閉路検出](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉路検出) × 1問
- [包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#包除原理) × 1問
- [約数の走査を倍数の走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の走査を倍数の走査に帰着) × 1問
- [隣接不等式管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#隣接不等式管理) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [連続回数制約を分割の区間長制約に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#連続回数制約を分割の区間長制約に翻訳) × 1問
- [連長圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#連長圧縮) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [ytqm3さん](https://yukicoder.me/users/14296)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="blue">1999</font>](https://yukicoder.me/problems/no/2343)
- [★3.5／diff <font color="orange">2488</font>](https://yukicoder.me/problems/no/2485)
- [★3.5／diff <font color="orange">2587</font>](https://yukicoder.me/problems/no/2487)
- [★3.5／diff <font color="orange">2678</font>](https://yukicoder.me/problems/no/2345)
- [★3.5／diff <font color="orange">2798</font>](https://yukicoder.me/problems/no/2483)
- [★3.5／diff <font color="red">2816</font>](https://yukicoder.me/problems/no/2346)
- [★3.5／diff <font color="red">2965</font>](https://yukicoder.me/problems/no/2489)
- [★4／diff <font color="orange">2768</font>](https://yukicoder.me/problems/no/2344)
- [★4／diff <font color="red">3168</font>](https://yukicoder.me/problems/no/2348)
- [★4／diff <font color="darkgoldenrod ">3256</font>](https://yukicoder.me/problems/no/2347)
- [★4.5／diff <font color="red">3060</font>](https://yukicoder.me/problems/no/2490)
- [★5／diffデータなし](https://yukicoder.me/problems/no/2349)

### 過去問の解法頻度

- [一対一対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#一対一対応) × 2問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [リュカの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#リュカの定理) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [小さい法に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さい法に帰着) × 1問
- [剰余の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余の定理) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [単調列数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調列数え上げ) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#包除原理) × 1問
- [冪乗との最大公約数の収束](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗との最大公約数の収束) × 1問


## [taiga0629kyoproさん](https://yukicoder.me/users/14401)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="brown">683</font>](https://yukicoder.me/problems/no/2056)
- [★2／diff <font color="deepskyblue">1261</font>](https://yukicoder.me/problems/no/2079)
- [★2／diff <font color="blue">1728</font>](https://yukicoder.me/problems/no/2057)
- [★2.5／diff <font color="deepskyblue">1529</font>](https://yukicoder.me/problems/no/2078)
- [★2.5／diff <font color="blue">1641</font>](https://yukicoder.me/problems/no/2071)
- [★2.5／diff <font color="blue">1649</font>](https://yukicoder.me/problems/no/2080)
- [★2.5／diff <font color="yellowgreen">2047</font>](https://yukicoder.me/problems/no/2060)
- [★3／diff <font color="yellowgreen">2008</font>](https://yukicoder.me/problems/no/2058)
- [★3／diff <font color="yellowgreen">2167</font>](https://yukicoder.me/problems/no/2081)
- [★3／diff <font color="yellowgreen">2295</font>](https://yukicoder.me/problems/no/2061)
- [★3／diff <font color="yellowgreen">2306</font>](https://yukicoder.me/problems/no/2075)
- [★3／diff <font color="orange">2501</font>](https://yukicoder.me/problems/no/2082)
- [★3.5／diff <font color="orange">2643</font>](https://yukicoder.me/problems/no/2083)
- [★4／diff <font color="orange">2571</font>](https://yukicoder.me/problems/no/2137)
- [★4／diff <font color="red">2833</font>](https://yukicoder.me/problems/no/2084)
- [★4.5／diff <font color="orange">2553</font>](https://yukicoder.me/problems/no/2062)
- [★4.5／diff <font color="darkgoldenrod ">3219</font>](https://yukicoder.me/problems/no/2097)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 5問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 4問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 4問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 4問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 3問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 3問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 3問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 3問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 2問
- [一対一対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#一対一対応) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 2問
- [約数の走査を倍数の走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の走査を倍数の走査に帰着) × 2問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 2問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 2問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [lower_bound・upper_bound取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#lower_bound・upper_bound取得) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ変換) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [メビウスの反転公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウスの反転公式) × 1問
- [メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウス変換) × 1問
- [位取り記法による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法による構築) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [一次式の最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の最大・最小値計算) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [帰属区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#帰属区間取得) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [最小素因数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小素因数計算) × 1問
- [指数と対数による冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#指数と対数による冪乗計算) × 1問
- [自己写像に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#自己写像に翻訳) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [数列・配列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#数列・配列の構築) × 1問
- [疎な多項式の畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#疎な多項式の畳み込み) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [素数を用いた構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を用いた構築) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [総和の指定された部分列数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和の指定された部分列数え上げ) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多項定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項定理) × 1問
- [第二種スターリング数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#第二種スターリング数計算) × 1問
- [単調列数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調列数え上げ) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [二・多項係数を組み合わせに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#二・多項係数を組み合わせに翻訳) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [二分木に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分木に翻訳) × 1問
- [倍数ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数ゼータ変換) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量を保つ戦略) × 1問
- [包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#包除原理) × 1問
- [約数メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数メビウス変換) × 1問
- [約数包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数包除原理) × 1問


## [ecotteaさん](https://yukicoder.me/users/14450)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">595</font>](https://yukicoder.me/problems/no/2714)
- [★2／diff <font color="deepskyblue">1482</font>](https://yukicoder.me/problems/no/2715)
- [★2.5／diff <font color="blue">1789</font>](https://yukicoder.me/problems/no/2717)
- [★2.5／diff <font color="blue">1809</font>](https://yukicoder.me/problems/no/2716)
- [★3／diff <font color="yellowgreen">2161</font>](https://yukicoder.me/problems/no/2718)
- [★3.5／diff <font color="orange">2522</font>](https://yukicoder.me/problems/no/2719)
- [★4.5／diff <font color="red">3133</font>](https://yukicoder.me/problems/no/2720)

### 過去問の解法頻度

- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 2問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [next_permutation](https://p-adic.github.io/yukicoder-difficulty-statistics/#next_permutation) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [ソートによる多重集合の一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソートによる多重集合の一致判定) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [集合・多重集合の一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合・多重集合の一致判定) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [順列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#順列の構築) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二項定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項定理) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [dyktr_06さん](https://yukicoder.me/users/14510)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">624</font>](https://yukicoder.me/problems/no/2850)
- [★1／diff <font color="brown">774</font>](https://yukicoder.me/problems/no/2851)
- [★1.5／diff <font color="gray">304</font>](https://yukicoder.me/problems/no/2416)
- [★1.5／diff <font color="brown">774</font>](https://yukicoder.me/problems/no/2852)
- [★1.5／diff <font color="brown">774</font>](https://yukicoder.me/problems/no/2853)
- [★1.5／diff <font color="brown">781</font>](https://yukicoder.me/problems/no/2417)
- [★2／diff <font color="green">884</font>](https://yukicoder.me/problems/no/2549)
- [★2／diff <font color="green">1165</font>](https://yukicoder.me/problems/no/2854)
- [★2／diff <font color="deepskyblue">1510</font>](https://yukicoder.me/problems/no/2855)
- [★2.5／diff <font color="green">810</font>](https://yukicoder.me/problems/no/2419)
- [★2.5／diff <font color="green">1174</font>](https://yukicoder.me/problems/no/2325)
- [★2.5／diff <font color="blue">1629</font>](https://yukicoder.me/problems/no/2550)
- [★2.5／diff <font color="blue">1788</font>](https://yukicoder.me/problems/no/2421)
- [★2.5／diff <font color="blue">1824</font>](https://yukicoder.me/problems/no/2856)
- [★2.5／diff <font color="blue">1891</font>](https://yukicoder.me/problems/no/2857)
- [★2.5／diff <font color="orange">2501</font>](https://yukicoder.me/problems/no/2551)
- [★2.5／diff <font color="orange">2533</font>](https://yukicoder.me/problems/no/2982)
- [★3／diffデータなし](https://yukicoder.me/problems/no/2554)
- [★3／diff <font color="blue">1915</font>](https://yukicoder.me/problems/no/2328)
- [★3／diff <font color="yellowgreen">2147</font>](https://yukicoder.me/problems/no/2858)
- [★3／diff <font color="yellowgreen">2258</font>](https://yukicoder.me/problems/no/2330)
- [★3／diff <font color="yellowgreen">2353</font>](https://yukicoder.me/problems/no/2422)
- [★3／diff <font color="orange">2454</font>](https://yukicoder.me/problems/no/2859)
- [★3／diff <font color="orange">2521</font>](https://yukicoder.me/problems/no/2423)
- [★3.5／diff <font color="yellowgreen">2334</font>](https://yukicoder.me/problems/no/2860)
- [★3.5／diff <font color="yellowgreen">2387</font>](https://yukicoder.me/problems/no/2332)
- [★3.5／diff <font color="orange">2537</font>](https://yukicoder.me/problems/no/2333)
- [★3.5／diff <font color="red">2973</font>](https://yukicoder.me/problems/no/2861)

### 過去問の解法頻度

- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 6問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 3問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 3問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 3問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 3問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 3問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 2問
- [inplace DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#inplace DP) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 2問
- [２種の数値を足し引きして１種に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#２種の数値を足し引きして１種に帰着) × 2問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 2問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 2問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 2問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 2問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 2問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 2問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 2問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 2問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 2問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 2問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 2問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 2問
- [操作コスト最小化を最短経路長計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作コスト最小化を最短経路長計算に帰着) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [$45$度回転](https://p-adic.github.io/yukicoder-difficulty-statistics/#$45$度回転) × 1問
- [01BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#01BFS) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [bit演算による$64$並列](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit演算による$64$並列) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [next DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#next DP) × 1問
- [sorted set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted set) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [グラフ・状態の圧縮による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフ・状態の圧縮による次元削減) × 1問
- [グリッド上の価値最大化](https://p-adic.github.io/yukicoder-difficulty-statistics/#グリッド上の価値最大化) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [コスト１ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#コスト１ナップサック最適化) × 1問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 1問
- [ゼロ除算回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼロ除算回避) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [円環の倍化実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#円環の倍化実装) × 1問
- [回文判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#回文判定) × 1問
- [帰属区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#帰属区間取得) × 1問
- [区間max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min更新) × 1問
- [区間max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min取得) × 1問
- [区間の部分列をわたる総和計算をモノイド演算に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の部分列をわたる総和計算をモノイド演算に翻訳) × 1問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [矩形max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#矩形max・min取得) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [個数上限１複数ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#個数上限１複数ナップサック最適化) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [十分大きな法で計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#十分大きな法で計算) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [商のfloorの種類数による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの種類数による計算量評価) × 1問
- [商のfloorの値ごとに纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの値ごとに纏め上げ) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [全順序集合を状態に持つゲームをP状態とN状態の区間に分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#全順序集合を状態に持つゲームをP状態とN状態の区間に分割) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 1問
- [双対セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#双対セグメント木) × 1問
- [操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作回数上限以内の達成可能性判定を操作回数最小値計算に帰着) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [内積の畳み込み計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積の畳み込み計算) × 1問
- [内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積計算) × 1問
- [二項定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項定理) × 1問
- [非単射関数の像の濃度による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の像の濃度による計算量評価) × 1問
- [非単射関数の値で纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の値で纏め上げ) × 1問
- [非連結性を壁の８方向移動による連結性に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#非連結性を壁の８方向移動による連結性に翻訳) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [部分回文列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分回文列挙) × 1問
- [複数ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数ナップサック最適化) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [門松列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#門松列DP) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問
- [隣接行列による遷移計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#隣接行列による遷移計算) × 1問
- [累積max・min](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積max・min) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問


## [kenchoさん](https://yukicoder.me/users/14741)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="orange">2765</font>](https://yukicoder.me/problems/no/3162)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [MasKoaTSさん](https://yukicoder.me/users/14952)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">371</font>](https://yukicoder.me/problems/no/2515)
- [★1／diff <font color="brown">569</font>](https://yukicoder.me/problems/no/2175)
- [★1.5／diff <font color="brown">426</font>](https://yukicoder.me/problems/no/2721)
- [★1.5／diff <font color="brown">627</font>](https://yukicoder.me/problems/no/2516)
- [★2／diff <font color="green">1139</font>](https://yukicoder.me/problems/no/2176)
- [★2／diff <font color="deepskyblue">1212</font>](https://yukicoder.me/problems/no/2517)
- [★2.5／diff <font color="deepskyblue">1588</font>](https://yukicoder.me/problems/no/2722)
- [★2.5／diff <font color="blue">1771</font>](https://yukicoder.me/problems/no/2723)
- [★2.5／diff <font color="blue">1845</font>](https://yukicoder.me/problems/no/2724)
- [★2.5／diff <font color="blue">1856</font>](https://yukicoder.me/problems/no/2177)
- [★2.5／diff <font color="yellowgreen">2044</font>](https://yukicoder.me/problems/no/2179)
- [★2.5／diff <font color="orange">2493</font>](https://yukicoder.me/problems/no/2522)
- [★3／diff <font color="blue">1989</font>](https://yukicoder.me/problems/no/2178)
- [★3／diff <font color="yellowgreen">2046</font>](https://yukicoder.me/problems/no/2726)
- [★3／diff <font color="yellowgreen">2069</font>](https://yukicoder.me/problems/no/2519)
- [★3／diff <font color="yellowgreen">2284</font>](https://yukicoder.me/problems/no/2520)
- [★3.5／diff <font color="blue">1944</font>](https://yukicoder.me/problems/no/2725)
- [★3.5／diff <font color="orange">2421</font>](https://yukicoder.me/problems/no/2727)
- [★3.5／diff <font color="orange">2553</font>](https://yukicoder.me/problems/no/2523)
- [★3.5／diff <font color="orange">2708</font>](https://yukicoder.me/problems/no/2181)
- [★3.5／diff <font color="red">3010</font>](https://yukicoder.me/problems/no/2180)
- [★4／diff <font color="red">3010</font>](https://yukicoder.me/problems/no/2182)

### 過去問の解法頻度

- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 7問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 4問
- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 3問
- [最終手番のターン数に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番のターン数に注目) × 3問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 3問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 3問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 3問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 3問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 2問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 2問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 2問
- [外積・サラスの公式による行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積・サラスの公式による行列式計算) × 2問
- [行列式と面積・体積の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列式と面積・体積の関係) × 2問
- [行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列式計算) × 2問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 2問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 2問
- [素数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列挙) × 2問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [$45$度回転](https://p-adic.github.io/yukicoder-difficulty-statistics/#$45$度回転) × 1問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [minimax法](https://p-adic.github.io/yukicoder-difficulty-statistics/#minimax法) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [setprecision・format](https://p-adic.github.io/yukicoder-difficulty-statistics/#setprecision・format) × 1問
- [strategy stealing argument](https://p-adic.github.io/yukicoder-difficulty-statistics/#strategy stealing argument) × 1問
- [２種の数値を足し引きして１種に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#２種の数値を足し引きして１種に帰着) × 1問
- [エラトステネスの篩による素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩による素数判定) × 1問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 1問
- [グランディ数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グランディ数計算) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニム和) × 1問
- [フロベニウス数に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロベニウス数に注目) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [位取り記法表示で全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示で全探索) × 1問
- [円周角の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#円周角の定理) × 1問
- [解の公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#解の公式) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#距離空間の重み付きグラフ化) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [矩形加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#矩形加算更新) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [高さ奇数ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#高さ奇数ニム和) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [最小全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小全域木計算) × 1問
- [最小素因数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小素因数計算) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の面積計算) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [剰余を取る前に符号や大小を計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余を取る前に符号や大小を計算) × 1問
- [全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全域木計算) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [素数計数関数前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数計数関数前計算) × 1問
- [素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数判定) × 1問
- [掃き出し法による行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法による行列式計算) × 1問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [超頂点追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#超頂点追加) × 1問
- [底辺と高さを用いた三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#底辺と高さを用いた三角形の面積計算) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [二次元imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#二次元imos法) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量を保つ戦略) × 1問
- [平方根のfloor計算による平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算による平方数判定) × 1問
- [平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方数判定) × 1問
- [木の頂点の深さ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の頂点の深さ計算) × 1問
- [約数の個数の偶奇による平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の個数の偶奇による平方数判定) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [冪等重みの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪等重みの最短経路長計算) × 1問


## [aradさん](https://yukicoder.me/users/15012)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="yellowgreen">2031</font>](https://yukicoder.me/problems/no/2683)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [フビニの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フビニの定理) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成による次元削減) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [独立事象の積への分解による確率計算・数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#独立事象の積への分解による確率計算・数え上げ) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問


## [みここさん](https://yukicoder.me/users/15018)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">912</font>](https://yukicoder.me/problems/no/2282)
- [★2.5／diff <font color="blue">1628</font>](https://yukicoder.me/problems/no/2283)
- [★2.5／diff <font color="blue">1758</font>](https://yukicoder.me/problems/no/2284)
- [★3.5／diff <font color="orange">2450</font>](https://yukicoder.me/problems/no/2285)
- [★4／diff <font color="orange">2524</font>](https://yukicoder.me/problems/no/2286)
- [★4／diff <font color="red">2936</font>](https://yukicoder.me/problems/no/2287)
- [★5／diff <font color="red">3174</font>](https://yukicoder.me/problems/no/2288)

### 過去問の解法頻度

- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 2問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [グランディ数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グランディ数計算) × 1問
- [ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニム和) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [円環の倍化実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#円環の倍化実装) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [左右から走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#左右から走査) × 1問
- [最適化を各寄与の最適化に緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#最適化を各寄与の最適化に緩和) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [TKTYIさん](https://yukicoder.me/users/15072)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="blue">1632</font>](https://yukicoder.me/problems/no/3157)

### 過去問の解法頻度

- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [位取り記法表示・桁和を用いた倍数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示・桁和を用いた倍数判定) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問


## [otoshigoさん](https://yukicoder.me/users/15158)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="yellowgreen">2042</font>](https://yukicoder.me/problems/no/2433)

### 過去問の解法頻度

- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問


## [mymelochanさん](https://yukicoder.me/users/15163)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">786</font>](https://yukicoder.me/problems/no/2923)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [sotanishyさん](https://yukicoder.me/users/15255)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">744</font>](https://yukicoder.me/problems/no/2259)
- [★3.5／diff <font color="orange">2512</font>](https://yukicoder.me/problems/no/2264)

### 過去問の解法頻度

- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問


## [Kyo_s_sさん](https://yukicoder.me/users/15447)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">540</font>](https://yukicoder.me/problems/no/2560)
- [★2／diff <font color="green">1179</font>](https://yukicoder.me/problems/no/2567)

### 過去問の解法頻度

- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [分割の均等化](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割の均等化) × 1問


## [kaichou243さん](https://yukicoder.me/users/15520)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★4／diff <font color="red">2871</font>](https://yukicoder.me/problems/no/2136)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [KumaTachiRenさん](https://yukicoder.me/users/15577)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">422</font>](https://yukicoder.me/problems/no/2492)
- [★2／diff <font color="green">1031</font>](https://yukicoder.me/problems/no/2494)
- [★2／diff <font color="green">1182</font>](https://yukicoder.me/problems/no/2493)
- [★3／diff <font color="yellowgreen">2209</font>](https://yukicoder.me/problems/no/2497)
- [★3.5／diff <font color="yellowgreen">2309</font>](https://yukicoder.me/problems/no/2496)
- [★3.5／diff <font color="orange">2421</font>](https://yukicoder.me/problems/no/2495)
- [★3.5／diff <font color="red">2885</font>](https://yukicoder.me/problems/no/2981)
- [★3.5／diff <font color="red">2898</font>](https://yukicoder.me/problems/no/2499)
- [★3.5／diff <font color="red">3031</font>](https://yukicoder.me/problems/no/2498)
- [★5／diff <font color="darkgoldenrod ">3503</font>](https://yukicoder.me/problems/no/2589)

### 過去問の解法頻度

- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 3問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [01列と根付き木の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と根付き木の対応) × 1問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [B進法位取り記法と法Bベクトルの対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#B進法位取り記法と法Bベクトルの対応) × 1問
- [convex hull trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#convex hull trick) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [slope trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#slope trick) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [グラフ畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフ畳み込み) × 1問
- [ソート前の添字復元](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート前の添字復元) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ベルトラン・チェビシェフの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#ベルトラン・チェビシェフの定理) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [一次式の族の最大・最小値取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の族の最大・最小値取得) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [言及する成分数を最大化する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#言及する成分数を最大化する質問) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列の階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の階段化) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [三分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#三分探索) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [写像の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#写像の構築) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [全単射の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#全単射の構築) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [素数に注目する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数に注目する質問) × 1問
- [掃き出し法](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [対角線に言及する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#対角線に言及する質問) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [凸最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸最適化) × 1問
- [配列のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列のリアクティブによる特定) × 1問
- [微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分計算) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [冪乗による根号消去](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗による根号消去) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [冪等重みの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪等重みの最短経路長計算) × 1問


## [kyawaさん](https://yukicoder.me/users/15779)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="orange">2438</font>](https://yukicoder.me/problems/no/2687)

### 過去問の解法頻度

- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間挿入更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間挿入更新) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [相対運動に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#相対運動に翻訳) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問


## [meruuu61779999さん](https://yukicoder.me/users/15780)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diffデータなし](https://yukicoder.me/problems/no/2370)

### 過去問の解法頻度

- [コストなしナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#コストなしナップサック最適化) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [指定序数の値の計算を被覆の先頭項管理で処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を被覆の先頭項管理で処理) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [半分全列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#半分全列挙) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問


## [ma_twさん](https://yukicoder.me/users/15810)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1983</font>](https://yukicoder.me/problems/no/2685)
- [★4／diff <font color="orange">2604</font>](https://yukicoder.me/problems/no/2688)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [期待値漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値漸化式) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [kusirakusiraさん](https://yukicoder.me/users/15921)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">406</font>](https://yukicoder.me/problems/no/2919)
- [★1／diff <font color="brown">674</font>](https://yukicoder.me/problems/no/2728)
- [★1.5／diff <font color="brown">670</font>](https://yukicoder.me/problems/no/2921)
- [★2／diff <font color="green">851</font>](https://yukicoder.me/problems/no/2563)
- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2931)
- [★2.5／diff <font color="deepskyblue">1279</font>](https://yukicoder.me/problems/no/2730)
- [★2.5／diff <font color="deepskyblue">1442</font>](https://yukicoder.me/problems/no/2731)
- [★3／diff <font color="yellowgreen">2203</font>](https://yukicoder.me/problems/no/2732)
- [★3.5／diff <font color="orange">2698</font>](https://yukicoder.me/problems/no/2735)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 4問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 2問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 2問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 2問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [breakに関する考察](https://p-adic.github.io/yukicoder-difficulty-statistics/#breakに関する考察) × 1問
- [next_permutation](https://p-adic.github.io/yukicoder-difficulty-statistics/#next_permutation) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [ナップサック分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック分割統治) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [決め打ちによる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#決め打ちによる構築) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [順列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#順列の構築) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問
- [乱択による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択による構築) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [ymmtr(せるたわーしーぷ!)さん](https://yukicoder.me/users/15955)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2662)

### 過去問の解法頻度

- [SIMD高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#SIMD高速化) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [区間一次式加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間一次式加算更新) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [高階差分](https://p-adic.github.io/yukicoder-difficulty-statistics/#高階差分) × 1問


## [MMさん](https://yukicoder.me/users/16002)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1276</font>](https://yukicoder.me/problems/no/2694)

### 過去問の解法頻度

- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [区間線形結合取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間線形結合取得) × 1問
- [区間選択ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間選択ナップサック最適化) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問


## [Nzt3さん](https://yukicoder.me/users/16054)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1557</font>](https://yukicoder.me/problems/no/2741)
- [★2.5／diff <font color="deepskyblue">1435</font>](https://yukicoder.me/problems/no/2630)
- [★2.5／diff <font color="blue">1823</font>](https://yukicoder.me/problems/no/3115)
- [★2.5／diff <font color="yellowgreen">2309</font>](https://yukicoder.me/problems/no/2743)
- [★2.5／diff <font color="yellowgreen">2309</font>](https://yukicoder.me/problems/no/2744)
- [★2.5／diff <font color="yellowgreen">2309</font>](https://yukicoder.me/problems/no/2745)
- [★3／diff <font color="yellowgreen">2288</font>](https://yukicoder.me/problems/no/3120)
- [★3／diff <font color="yellowgreen">2315</font>](https://yukicoder.me/problems/no/3119)
- [★3／diff <font color="orange">2423</font>](https://yukicoder.me/problems/no/2746)
- [★3／diff <font color="orange">2436</font>](https://yukicoder.me/problems/no/3121)
- [★3.5／diff <font color="orange">2628</font>](https://yukicoder.me/problems/no/2437)
- [★3.5／diff <font color="red">2912</font>](https://yukicoder.me/problems/no/2748)

### 過去問の解法頻度

- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 4問
- [合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成による次元削減) × 3問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 3問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 2問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 2問
- [ナップサック分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック分割統治) × 2問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 2問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [エラトステネスの篩による素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩による素数判定) × 1問
- [オイラーの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーの定理) × 1問
- [グラフ・状態の圧縮による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフ・状態の圧縮による次元削減) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ソート前の添字復元](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート前の添字復元) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ド・モルガンの法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#ド・モルガンの法則) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [リアクティブによるブラックボックス操作](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによるブラックボックス操作) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [合成数を法とする数値を零と素因数の冪乗と可逆元に分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成数を法とする数値を零と素因数の冪乗と可逆元に分解) × 1問
- [左右から走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#左右から走査) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [最近点計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最近点計算) × 1問
- [始切片選択ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#始切片選択ナップサック最適化) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [商の反復による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商の反復による付値計算) × 1問
- [剰余を取る前に符号や大小を計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余を取る前に符号や大小を計算) × 1問
- [整数のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#整数のリアクティブによる特定) × 1問
- [選択肢の分割・纏め上げ・追加で良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択肢の分割・纏め上げ・追加で良いケースに帰着) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数判定) × 1問
- [素数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列挙) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [操作コスト最小化を最短経路長計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作コスト最小化を最短経路長計算に帰着) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多次元の最適化を一次元の最適化に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元の最適化を一次元の最適化に帰着) × 1問
- [多次元コストを一次元に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元コストを一次元に翻訳) × 1問
- [多次元コストナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元コストナップサック最適化) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [中国剰余定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#中国剰余定理) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [必勝戦略のリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#必勝戦略のリアクティブ化) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量を保つ戦略) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [複数ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数ナップサック最適化) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [累積max・min](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積max・min) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [ponjuiceさん](https://yukicoder.me/users/16259)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">514</font>](https://yukicoder.me/problems/no/2737)
- [★1.5／diff <font color="deepskyblue">1245</font>](https://yukicoder.me/problems/no/2738)
- [★3／diff <font color="yellowgreen">2158</font>](https://yukicoder.me/problems/no/2641)

### 過去問の解法頻度

- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 2問
- [$45$度回転](https://p-adic.github.io/yukicoder-difficulty-statistics/#$45$度回転) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [帰属区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#帰属区間取得) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [描画可能性を実際に描画して判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#描画可能性を実際に描画して判定) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問


## [yuyu_5510さん](https://yukicoder.me/users/16425)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="yellowgreen">2274</font>](https://yukicoder.me/problems/no/2435)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [nouka28さん](https://yukicoder.me/users/16467)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="blue">1727</font>](https://yukicoder.me/problems/no/2930)
- [★2.5／diff <font color="blue">1894</font>](https://yukicoder.me/problems/no/2949)
- [★3／diff <font color="blue">1928</font>](https://yukicoder.me/problems/no/2977)
- [★3／diff <font color="yellowgreen">2100</font>](https://yukicoder.me/problems/no/2697)
- [★3／diff <font color="orange">2581</font>](https://yukicoder.me/problems/no/2950)
- [★3／diff <font color="orange">2581</font>](https://yukicoder.me/problems/no/2951)
- [★3.5／diff <font color="red">2823</font>](https://yukicoder.me/problems/no/2952)
- [★4／diffデータなし](https://yukicoder.me/problems/no/2935)
- [★4／diffデータなし](https://yukicoder.me/problems/no/2936)

### 過去問の解法頻度

- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 3問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 3問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [区間代入更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間代入更新) × 2問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 2問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 2問
- [遅延セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#遅延セグメント木) × 2問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 2問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [XOR畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#XOR畳み込み) × 1問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [mex取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#mex取得) × 1問
- [multiset](https://p-adic.github.io/yukicoder-difficulty-statistics/#multiset) × 1問
- [スタック](https://p-adic.github.io/yukicoder-difficulty-statistics/#スタック) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [区間の部分列をわたる総和計算をモノイド演算に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の部分列をわたる総和計算をモノイド演算に翻訳) × 1問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [最長単調増加部分列長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最長単調増加部分列長計算) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [指定序数の値の計算を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を指定始切片数え上げに帰着) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [全方位木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#全方位木DP) × 1問
- [第二種スターリング数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#第二種スターリング数計算) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [二分木に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分木に翻訳) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [累積max・min](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積max・min) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [連長圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#連長圧縮) × 1問


## [keisuke6さん](https://yukicoder.me/users/16526)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">588</font>](https://yukicoder.me/problems/no/2070)
- [★1.5／diffデータなし](https://yukicoder.me/problems/no/2123)
- [★2／diff <font color="deepskyblue">1433</font>](https://yukicoder.me/problems/no/2480)
- [★3／diff <font color="blue">1738</font>](https://yukicoder.me/problems/no/2157)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [★1の64bit整数要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1の64bit整数要求) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [サンプルに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルに帰着) × 1問
- [期待値漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値漸化式) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 1問
- [相似](https://p-adic.github.io/yukicoder-difficulty-statistics/#相似) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問


## [Magentorさん](https://yukicoder.me/users/16545)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">905</font>](https://yukicoder.me/problems/no/2564)
- [★2／diff <font color="blue">1632</font>](https://yukicoder.me/problems/no/2568)
- [★2.5／diff <font color="deepskyblue">1276</font>](https://yukicoder.me/problems/no/2699)
- [★2.5／diff <font color="blue">1900</font>](https://yukicoder.me/problems/no/2701)
- [★3／diff <font color="yellowgreen">2056</font>](https://yukicoder.me/problems/no/2482)
- [★3／diff <font color="orange">2411</font>](https://yukicoder.me/problems/no/2378)
- [★3／diff <font color="orange">2723</font>](https://yukicoder.me/problems/no/2815)
- [★3.5／diff <font color="yellowgreen">2392</font>](https://yukicoder.me/problems/no/2571)
- [★4／diff <font color="orange">2488</font>](https://yukicoder.me/problems/no/2484)
- [★4／diff <font color="red">3124</font>](https://yukicoder.me/problems/no/2704)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 2問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 2問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [inplace DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#inplace DP) × 1問
- [コストなしナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#コストなしナップサック割り当て数え上げ) × 1問
- [サンプルから推測](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルから推測) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 1問
- [フェルマーの小定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理による逆元計算) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [交代和](https://p-adic.github.io/yukicoder-difficulty-statistics/#交代和) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [重複選択可ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック割り当て数え上げ) × 1問
- [重複選択可ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック最適化) × 1問
- [剰余計算を桁の線形和に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余計算を桁の線形和に帰着) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [選択回数依存コスト重複選択可ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択回数依存コスト重複選択可ナップサック最適化) × 1問
- [選択回数上限付き重複選択可ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択回数上限付き重複選択可ナップサック割り当て数え上げ) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [弾性衝突を通過に翻訳して位置関係から復元](https://p-adic.github.io/yukicoder-difficulty-statistics/#弾性衝突を通過に翻訳して位置関係から復元) × 1問
- [部分列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分列DP) × 1問
- [複数価値ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数価値ナップサック割り当て数え上げ) × 1問


## [sepa38さん](https://yukicoder.me/users/16649)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">198</font>](https://yukicoder.me/problems/no/2547)
- [★1.5／diff <font color="gray">343</font>](https://yukicoder.me/problems/no/2548)
- [★2／diff <font color="blue">1605</font>](https://yukicoder.me/problems/no/2326)
- [★2／diff <font color="blue">1698</font>](https://yukicoder.me/problems/no/2324)
- [★2.5／diff <font color="yellowgreen">2235</font>](https://yukicoder.me/problems/no/2552)
- [★3／diff <font color="yellowgreen">2121</font>](https://yukicoder.me/problems/no/2327)
- [★3／diff <font color="yellowgreen">2147</font>](https://yukicoder.me/problems/no/2331)
- [★3／diff <font color="red">2858</font>](https://yukicoder.me/problems/no/2553)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [オイラー関数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラー関数計算) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 1問
- [ルジャンドルの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ルジャンドルの公式) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [外積による三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積による三角形の面積計算) × 1問
- [外積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積計算) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成による次元削減) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の面積計算) × 1問
- [四角形を三角形２つや対角線２本に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#四角形を三角形２つや対角線２本に翻訳) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和計算の期待値への帰着) × 1問
- [転倒数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#転倒数計算) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [倍数走査によるオイラー関数前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数走査によるオイラー関数前計算) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [約数の走査を倍数の走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の走査を倍数の走査に帰着) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [srjywrdnprktさん](https://yukicoder.me/users/16741)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">140</font>](https://yukicoder.me/problems/no/2450)
- [★2／diff <font color="green">1063</font>](https://yukicoder.me/problems/no/2527)
- [★2／diff <font color="green">1158</font>](https://yukicoder.me/problems/no/2451)
- [★2／diff <font color="deepskyblue">1205</font>](https://yukicoder.me/problems/no/2526)
- [★2／diff <font color="deepskyblue">1516</font>](https://yukicoder.me/problems/no/2767)
- [★2／diff <font color="deepskyblue">1548</font>](https://yukicoder.me/problems/no/2768)
- [★2.5／diff <font color="deepskyblue">1389</font>](https://yukicoder.me/problems/no/2232)
- [★2.5／diff <font color="deepskyblue">1544</font>](https://yukicoder.me/problems/no/2453)
- [★2.5／diff <font color="blue">1661</font>](https://yukicoder.me/problems/no/2204)
- [★2.5／diff <font color="blue">1661</font>](https://yukicoder.me/problems/no/2205)
- [★2.5／diff <font color="blue">1849</font>](https://yukicoder.me/problems/no/2454)
- [★3／diff <font color="blue">1849</font>](https://yukicoder.me/problems/no/2770)
- [★3／diff <font color="blue">1891</font>](https://yukicoder.me/problems/no/2452)
- [★3／diff <font color="blue">1922</font>](https://yukicoder.me/problems/no/2235)
- [★3／diff <font color="blue">1998</font>](https://yukicoder.me/problems/no/2456)
- [★3／diff <font color="yellowgreen">2003</font>](https://yukicoder.me/problems/no/2769)
- [★3／diff <font color="yellowgreen">2170</font>](https://yukicoder.me/problems/no/2771)
- [★3／diff <font color="yellowgreen">2175</font>](https://yukicoder.me/problems/no/2236)
- [★3／diff <font color="yellowgreen">2213</font>](https://yukicoder.me/problems/no/2455)
- [★3／diff <font color="yellowgreen">2358</font>](https://yukicoder.me/problems/no/2457)
- [★3.5／diff <font color="orange">2459</font>](https://yukicoder.me/problems/no/2458)
- [★4.5／diff <font color="red">2809</font>](https://yukicoder.me/problems/no/2459)

### 過去問の解法頻度

- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 5問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 4問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 4問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 3問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 3問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 3問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 2問
- [フェルマーの小定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理による逆元計算) × 2問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 2問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 2問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 2問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 2問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 2問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 2問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 2問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 2問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 2問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 2問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 2問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 2問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 2問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 2問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 2問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [XOR・反転が2回で戻ることに注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#XOR・反転が2回で戻ることに注目) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [１つの桁・成分のみ特定する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#１つの桁・成分のみ特定する質問) × 1問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [キュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#キュー) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [バケット分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#バケット分割) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [回文判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#回文判定) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [区間を切片の差に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を切片の差に翻訳) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [矩形加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#矩形加算更新) × 1問
- [矩形和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#矩形和取得) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成による次元削減) × 1問
- [最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小公倍数計算) × 1問
- [最大公約数による最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数による最小公倍数計算) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [最長共通接頭辞計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最長共通接頭辞計算) × 1問
- [四角形を三角形２つや対角線２本に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#四角形を三角形２つや対角線２本に翻訳) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [指定序数の値の計算を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を指定始切片数え上げに帰着) × 1問
- [指定序数の値の計算を被覆の先頭項管理で処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を被覆の先頭項管理で処理) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [十分大きな法で計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#十分大きな法で計算) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [商のfloorの値ごとに纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの値ごとに纏め上げ) × 1問
- [商のfloorの分母を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの分母を止める総和計算) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [中国剰余定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#中国剰余定理) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [内積の畳み込み計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積の畳み込み計算) × 1問
- [内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積計算) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [二次元imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#二次元imos法) × 1問
- [二次元累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#二次元累積和) × 1問
- [任意mod畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#任意mod畳み込み) × 1問
- [半分全列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#半分全列挙) × 1問
- [非単射関数の値で纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の値で纏め上げ) × 1問
- [描画可能性を実際に描画して判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#描画可能性を実際に描画して判定) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [部分回文列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分回文列挙) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [文字列のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列のリアクティブによる特定) × 1問
- [平方分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方分割) × 1問
- [包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#包除原理) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問


## [Michirakaraさん](https://yukicoder.me/users/16743)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">711</font>](https://yukicoder.me/problems/no/2154)
- [★1.5／diff <font color="deepskyblue">1235</font>](https://yukicoder.me/problems/no/2946)
- [★1.5／diff <font color="deepskyblue">1389</font>](https://yukicoder.me/problems/no/2947)
- [★2／diff <font color="green">878</font>](https://yukicoder.me/problems/no/2155)
- [★2.5／diff <font color="yellowgreen">2306</font>](https://yukicoder.me/problems/no/2376)

### 過去問の解法頻度

- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [ワーシャル・フロイド法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ワーシャル・フロイド法) × 1問
- [外積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積計算) × 1問
- [距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#距離空間の重み付きグラフ化) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [線分の交差判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#線分の交差判定) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [単位の分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#単位の分解) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問


## [Mizarさん](https://yukicoder.me/users/16780)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">650</font>](https://yukicoder.me/problems/no/2385)
- [★3.5／diffデータなし](https://yukicoder.me/problems/no/2440)
- [★4／diffデータなし](https://yukicoder.me/problems/no/3047)
- [★5／diffデータなし](https://yukicoder.me/problems/no/2908)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問


## [tohohogisuさん](https://yukicoder.me/users/16802)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diffデータなし](https://yukicoder.me/problems/no/2091)
- [★1／diffデータなし](https://yukicoder.me/problems/no/2312)
- [★1.5／diff <font color="deepskyblue">1211</font>](https://yukicoder.me/problems/no/2693)
- [★2／diff <font color="green">843</font>](https://yukicoder.me/problems/no/2093)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [kinugoshi8928さん](https://yukicoder.me/users/16856)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1689</font>](https://yukicoder.me/problems/no/2806)

### 過去問の解法頻度

- [breakに関する考察](https://p-adic.github.io/yukicoder-difficulty-statistics/#breakに関する考察) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [約数計数関数による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数計数関数による計算量評価) × 1問


## [maguroflyさん](https://yukicoder.me/users/17109)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diffデータなし](https://yukicoder.me/problems/no/2757)
- [★1.5／diff <font color="yellowgreen">2185</font>](https://yukicoder.me/problems/no/2590)
- [★3／diff <font color="blue">1960</font>](https://yukicoder.me/problems/no/2761)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [getline](https://p-adic.github.io/yukicoder-difficulty-statistics/#getline) × 1問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [seekworserさん](https://yukicoder.me/users/17128)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="green">846</font>](https://yukicoder.me/problems/no/2886)
- [★1.5／diff <font color="brown">769</font>](https://yukicoder.me/problems/no/2887)
- [★2／diff <font color="deepskyblue">1521</font>](https://yukicoder.me/problems/no/2888)
- [★2.5／diff <font color="blue">1669</font>](https://yukicoder.me/problems/no/2889)
- [★2.5／diff <font color="yellowgreen">2275</font>](https://yukicoder.me/problems/no/2890)
- [★3／diff <font color="blue">1967</font>](https://yukicoder.me/problems/no/2891)
- [★3／diff <font color="yellowgreen">2162</font>](https://yukicoder.me/problems/no/2786)
- [★3／diff <font color="yellowgreen">2282</font>](https://yukicoder.me/problems/no/2388)
- [★3.5／diff <font color="orange">2488</font>](https://yukicoder.me/problems/no/2892)
- [★4／diff <font color="darkgoldenrod ">3356</font>](https://yukicoder.me/problems/no/2893)

### 過去問の解法頻度

- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 1問
- [コストなしナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#コストなしナップサック最適化) × 1問
- [サンプルから推測](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルから推測) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [円環の倍化実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#円環の倍化実装) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [区間選択ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間選択ナップサック最適化) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [重複選択可ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択可ナップサック最適化) × 1問
- [商のfloorの種類数による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの種類数による計算量評価) × 1問
- [商のfloorの値ごとに纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの値ごとに纏め上げ) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [剰余の被除数を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余の被除数を止める総和計算) × 1問
- [剰余を商のfloorに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余を商のfloorに翻訳) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [非単射関数の像の濃度による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の像の濃度による計算量評価) × 1問
- [非単射関数の値で纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の値で纏め上げ) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [文字列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列の構築) × 1問
- [並列二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#並列二分探索) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [冪等重みの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪等重みの最短経路長計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [GlinTFrauleinさん](https://yukicoder.me/users/17194)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">982</font>](https://yukicoder.me/problems/no/2386)
- [★2.5／diff <font color="yellowgreen">2304</font>](https://yukicoder.me/problems/no/2390)
- [★3／diff <font color="yellowgreen">2273</font>](https://yukicoder.me/problems/no/2511)
- [★4／diff <font color="red">2944</font>](https://yukicoder.me/problems/no/2512)

### 過去問の解法頻度

- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [重複選択個数の線形関係式](https://p-adic.github.io/yukicoder-difficulty-statistics/#重複選択個数の線形関係式) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問


## [primenumber11さん](https://yukicoder.me/users/17307)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1313</font>](https://yukicoder.me/problems/no/2372)
- [★2／diff <font color="blue">1779</font>](https://yukicoder.me/problems/no/2804)

### 過去問の解法頻度

- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 2問
- [multiset](https://p-adic.github.io/yukicoder-difficulty-statistics/#multiset) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問


## [warabi0906さん](https://yukicoder.me/users/17391)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="yellowgreen">2278</font>](https://yukicoder.me/problems/no/2813)

### 過去問の解法頻度

- [グランディ数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グランディ数計算) × 1問
- [ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニム和) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰的構造に沿った再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構造に沿った再帰) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問


## [黒狗さん。さん](https://yukicoder.me/users/17393)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="blue">1720</font>](https://yukicoder.me/problems/no/2805)

### 過去問の解法頻度

- [グラフの状態や目的地の変化を有向辺に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの状態や目的地の変化を有向辺に翻訳) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [始点と終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#始点と終点からの最短経路長計算) × 1問
- [終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#終点からの最短経路長計算) × 1問


## [iro_さん](https://yukicoder.me/users/17440)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="orange">2649</font>](https://yukicoder.me/problems/no/2133)

### 過去問の解法頻度

- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [カタラン数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カタラン数計算) × 1問
- [区間の重複度計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の重複度計算) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [集合族による帰属関係で類別](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合族による帰属関係で類別) × 1問
- [同値関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#同値関係) × 1問


## [KA37RIさん](https://yukicoder.me/users/17678)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">1081</font>](https://yukicoder.me/problems/no/2926)
- [★2／diff <font color="blue">1980</font>](https://yukicoder.me/problems/no/2509)
- [★2.5／diff <font color="yellowgreen">2219</font>](https://yukicoder.me/problems/no/2510)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [定数倍メモリ削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#定数倍メモリ削減) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [半分全列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#半分全列挙) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問


## [poyonさん](https://yukicoder.me/users/17703)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="yellowgreen">2103</font>](https://yukicoder.me/problems/no/2377)

### 過去問の解法頻度

- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [dolpさん](https://yukicoder.me/users/17723)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diffデータなし](https://yukicoder.me/problems/no/2174)

### 過去問の解法頻度

- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問


## [hiro1729さん](https://yukicoder.me/users/17790)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="yellowgreen">2275</font>](https://yukicoder.me/problems/no/2593)
- [★2.5／diff <font color="green">1050</font>](https://yukicoder.me/problems/no/2393)
- [★2.5／diff <font color="blue">1977</font>](https://yukicoder.me/problems/no/2733)

### 過去問の解法頻度

- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [位取り記法表示で全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示で全探索) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [剰余計算を桁の線形和に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余計算を桁の線形和に帰着) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [中国剰余定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#中国剰余定理) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問


## [csharpythonさん](https://yukicoder.me/users/17904)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">1000</font>](https://yukicoder.me/problems/no/2234)

### 過去問の解法頻度

- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問


## [hiryuNさん](https://yukicoder.me/users/17962)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2449)

### 過去問の解法頻度

- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [同値関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#同値関係) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [Carpenters-Catさん](https://yukicoder.me/users/17987)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="orange">2475</font>](https://yukicoder.me/problems/no/2368)
- [★3.5／diff <font color="orange">2627</font>](https://yukicoder.me/problems/no/2367)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [watasou1543さん](https://yukicoder.me/users/18009)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1890</font>](https://yukicoder.me/problems/no/2375)
- [★3.5／diff <font color="orange">2433</font>](https://yukicoder.me/problems/no/2808)

### 過去問の解法頻度

- [bitDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitDP) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [ヘルド・カープ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ヘルド・カープ法) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問


## [amentorimaruさん](https://yukicoder.me/users/18080)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">340</font>](https://yukicoder.me/problems/no/2314)
- [★1／diff <font color="gray">352</font>](https://yukicoder.me/problems/no/2599)
- [★1.5／diff <font color="brown">592</font>](https://yukicoder.me/problems/no/2315)
- [★1.5／diff <font color="brown">686</font>](https://yukicoder.me/problems/no/2600)
- [★2／diff <font color="brown">718</font>](https://yukicoder.me/problems/no/2316)
- [★2／diff <font color="green">875</font>](https://yukicoder.me/problems/no/2317)
- [★2／diff <font color="green">1032</font>](https://yukicoder.me/problems/no/2601)
- [★3／diff <font color="yellowgreen">2016</font>](https://yukicoder.me/problems/no/2318)
- [★3／diff <font color="yellowgreen">2048</font>](https://yukicoder.me/problems/no/2604)
- [★3／diff <font color="orange">2419</font>](https://yukicoder.me/problems/no/2602)
- [★3／diff <font color="orange">2536</font>](https://yukicoder.me/problems/no/2603)
- [★3.5／diff <font color="yellowgreen">2122</font>](https://yukicoder.me/problems/no/2319)
- [★3.5／diff <font color="yellowgreen">2280</font>](https://yukicoder.me/problems/no/2605)
- [★4／diff <font color="yellowgreen">2295</font>](https://yukicoder.me/problems/no/2320)
- [★4／diff <font color="orange">2664</font>](https://yukicoder.me/problems/no/2606)
- [★4／diff <font color="red">3005</font>](https://yukicoder.me/problems/no/2513)
- [★4.5／diff <font color="red">3044</font>](https://yukicoder.me/problems/no/2321)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 3問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [２種の数値を足し引きして１種に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#２種の数値を足し引きして１種に帰着) × 1問
- [オーバーフロー回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#オーバーフロー回避) × 1問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [フロー](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロー) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [円環の倍化実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#円環の倍化実装) × 1問
- [円周角の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#円周角の定理) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [外接円計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外接円計算) × 1問
- [最小費用流計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小費用流計算) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 1問
- [商の反復による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商の反復による付値計算) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多次元コストナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元コストナップサック最適化) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [多倍長整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#多倍長整数) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [第二余弦定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#第二余弦定理) × 1問
- [単調列数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調列数え上げ) × 1問
- [超頂点追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#超頂点追加) × 1問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積計算) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [有理数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#有理数型) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [連分数展開](https://p-adic.github.io/yukicoder-difficulty-statistics/#連分数展開) × 1問
- [冪乗による根号消去](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗による根号消去) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [loop0919さん](https://yukicoder.me/users/18086)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">306</font>](https://yukicoder.me/problems/no/2558)
- [★1／diff <font color="gray">311</font>](https://yukicoder.me/problems/no/2920)
- [★1／diff <font color="brown">434</font>](https://yukicoder.me/problems/no/3124)
- [★1／diff <font color="green">1088</font>](https://yukicoder.me/problems/no/3019)
- [★1.5／diff <font color="brown">705</font>](https://yukicoder.me/problems/no/3125)
- [★1.5／diff <font color="green">830</font>](https://yukicoder.me/problems/no/3210)
- [★1.5／diff <font color="green">832</font>](https://yukicoder.me/problems/no/3012)
- [★1.5／diff <font color="green">972</font>](https://yukicoder.me/problems/no/2565)
- [★1.5／diff <font color="green">1075</font>](https://yukicoder.me/problems/no/3126)
- [★1.5／diff <font color="green">1133</font>](https://yukicoder.me/problems/no/2894)
- [★1.5／diff <font color="green">1180</font>](https://yukicoder.me/problems/no/2925)
- [★2／diff <font color="green">1128</font>](https://yukicoder.me/problems/no/3127)
- [★2／diff <font color="blue">1604</font>](https://yukicoder.me/problems/no/3021)
- [★2／diff <font color="blue">1773</font>](https://yukicoder.me/problems/no/3211)
- [★2／diff <font color="blue">1824</font>](https://yukicoder.me/problems/no/2927)
- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2802)
- [★2.5／diff <font color="deepskyblue">1227</font>](https://yukicoder.me/problems/no/3128)
- [★2.5／diff <font color="deepskyblue">1507</font>](https://yukicoder.me/problems/no/3129)
- [★2.5／diff <font color="blue">1659</font>](https://yukicoder.me/problems/no/2978)
- [★2.5／diff <font color="blue">1689</font>](https://yukicoder.me/problems/no/2896)
- [★2.5／diff <font color="blue">1709</font>](https://yukicoder.me/problems/no/3018)
- [★3／diffデータなし](https://yukicoder.me/problems/no/2933)
- [★3／diff <font color="yellowgreen">2066</font>](https://yukicoder.me/problems/no/3137)
- [★3／diff <font color="yellowgreen">2187</font>](https://yukicoder.me/problems/no/3130)
- [★3.5／diff <font color="red">2843</font>](https://yukicoder.me/problems/no/3131)

### 過去問の解法頻度

- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 8問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 5問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 3問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 3問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 3問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 3問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 3問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 2問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 2問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 2問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 2問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 2問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 2問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 2問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 2問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 2問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 2問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 2問
- [$1$の原始根を用いた文字種シフトの実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#$1$の原始根を用いた文字種シフトの実装) × 1問
- [$1$の原始根計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#$1$の原始根計算) × 1問
- [01列とグリッド上の経路の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列とグリッド上の経路の対応) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [２種の数値を足し引きして１種に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#２種の数値を足し引きして１種に帰着) × 1問
- [４重以上のループ](https://p-adic.github.io/yukicoder-difficulty-statistics/#４重以上のループ) × 1問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [エラトステネスの篩による素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩による素数判定) × 1問
- [グラフの構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの構築) × 1問
- [サンプルに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#サンプルに帰着) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [スタック](https://p-adic.github.io/yukicoder-difficulty-statistics/#スタック) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [トーナメントによる最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#トーナメントによる最大・最小値計算) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [円の弦による非交差分割計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#円の弦による非交差分割計算) × 1問
- [可負価値ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#可負価値ナップサック最適化) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [狭義単調関数の単射性](https://p-adic.github.io/yukicoder-difficulty-statistics/#狭義単調関数の単射性) × 1問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間乗算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間乗算更新) × 1問
- [区間選択ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間選択ナップサック最適化) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 1問
- [言及する成分数を最大化する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#言及する成分数を最大化する質問) × 1問
- [左右から走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#左右から走査) × 1問
- [座標のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標のリアクティブによる特定) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰による多重ループ実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰による多重ループ実装) × 1問
- [最小素因数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小素因数計算) × 1問
- [最大・最小値のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小値のリアクティブによる特定) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [枝刈り](https://p-adic.github.io/yukicoder-difficulty-statistics/#枝刈り) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#終点からの最短経路長計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [制約からグラフの種類を特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#制約からグラフの種類を特定) × 1問
- [全事象探索による確率・期待値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全事象探索による確率・期待値計算) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数判定) × 1問
- [素数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列挙) × 1問
- [双対セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#双対セグメント木) × 1問
- [操作・質問の全探索による操作の構築・質問決定](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・質問の全探索による操作の構築・質問決定) × 1問
- [相手の選択肢をなくす戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#相手の選択肢をなくす戦略) × 1問
- [単調関数のファイバーの緩和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調関数のファイバーの緩和計算) × 1問
- [遅延セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#遅延セグメント木) × 1問
- [中国剰余定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#中国剰余定理) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [二分法](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分法) × 1問
- [入れ子の深さを記録する走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#入れ子の深さを記録する走査) × 1問
- [必勝戦略のリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#必勝戦略のリアクティブ化) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [部分列の二項関係をデータ構造で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分列の二項関係をデータ構造で管理) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [閉路と残りに分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉路と残りに分割) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問
- [累積積による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による二項係数計算) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [連長圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#連長圧縮) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [bluebery1001さん](https://yukicoder.me/users/18132)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">306</font>](https://yukicoder.me/problems/no/2559)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問


## [tkmsさん](https://yukicoder.me/users/18170)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1337</font>](https://yukicoder.me/problems/no/2695)

### 過去問の解法頻度

- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#距離空間の重み付きグラフ化) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問


## [Furinaさん](https://yukicoder.me/users/18331)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="blue">1961</font>](https://yukicoder.me/problems/no/2555)

### 過去問の解法頻度

- [三角形の成立条件](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の成立条件) × 1問
- [三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の面積計算) × 1問
- [正弦定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#正弦定理) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [底辺と高さを用いた三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#底辺と高さを用いた三角形の面積計算) × 1問


## [nikoro256さん](https://yukicoder.me/users/18484)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1498</font>](https://yukicoder.me/problems/no/2760)

### 過去問の解法頻度

- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問


## [aplysiaSheepさん](https://yukicoder.me/users/18516)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="yellowgreen">2392</font>](https://yukicoder.me/problems/no/2573)
- [★3.5／diff <font color="orange">2559</font>](https://yukicoder.me/problems/no/2574)

### 過去問の解法頻度

筆者がまだupsolveしていないか解法の登録が終わっていないためデータがありません。


## [eoeoさん](https://yukicoder.me/users/18534)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">1012</font>](https://yukicoder.me/problems/no/2671)
- [★2.5／diff <font color="blue">1806</font>](https://yukicoder.me/problems/no/2673)
- [★3／diffデータなし](https://yukicoder.me/problems/no/2690)

### 過去問の解法頻度

- [あみだくじと置換の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#あみだくじと置換の対応) × 2問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 2問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 2問
- [置換の互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#置換の互換表示) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [01BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#01BFS) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [lower_bound・upper_bound取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#lower_bound・upper_bound取得) × 1問
- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [slope trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#slope trick) × 1問
- [sorted set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted set) × 1問
- [４重以上のループ](https://p-adic.github.io/yukicoder-difficulty-statistics/#４重以上のループ) × 1問
- [グラフの状態や目的地の変化を有向辺に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの状態や目的地の変化を有向辺に翻訳) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [区間一次式max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間一次式max・min更新) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰による多重ループ実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰による多重ループ実装) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [双対セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#双対セグメント木) × 1問
- [操作コスト最小化を最短経路長計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作コスト最小化を最短経路長計算に帰着) × 1問
- [微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分計算) × 1問


## [tatesotoさん](https://yukicoder.me/users/18586)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">886</font>](https://yukicoder.me/problems/no/3156)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 1問
- [平方根のfloor計算による平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算による平方数判定) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方数判定) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問


## [Koiさん](https://yukicoder.me/users/18621)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1907</font>](https://yukicoder.me/problems/no/2429)
- [★3／diff <font color="orange">2765</font>](https://yukicoder.me/problems/no/2643)

### 過去問の解法頻度

- [１変数連立一次不等式の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#１変数連立一次不等式の充足可能性判定) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [ポテンシャル付き素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポテンシャル付き素集合データ構造) × 1問
- [ワイルドカードの値を変数化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ワイルドカードの値を変数化) × 1問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問


## [lgswdnさん](https://yukicoder.me/users/18648)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="orange">2477</font>](https://yukicoder.me/problems/no/2899)
- [★3／diff <font color="orange">2799</font>](https://yukicoder.me/problems/no/2900)

### 過去問の解法頻度

- [01列・部分集合の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列・部分集合の構築) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [グラフの頂点の次数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの頂点の次数計算) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [再帰的構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構築) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 1問
- [乱択による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択による構築) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問
- [貪欲法による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法による構築) × 1問


## [rotti_coderさん](https://yukicoder.me/users/18712)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1778</font>](https://yukicoder.me/problems/no/2948)

### 過去問の解法頻度

- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [bitDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitDP) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [ヘルド・カープ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ヘルド・カープ法) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [部分集合DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分集合DP) × 1問
- [部分集合対全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分集合対全探索) × 1問


## [hirayuu_ycさん](https://yukicoder.me/users/18741)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">424</font>](https://yukicoder.me/problems/no/2525)
- [★1.5／diff <font color="green">837</font>](https://yukicoder.me/problems/no/2922)
- [★1.5／diff <font color="red">2960</font>](https://yukicoder.me/problems/no/2596)
- [★2／diff <font color="green">939</font>](https://yukicoder.me/problems/no/2803)
- [★2／diff <font color="blue">1608</font>](https://yukicoder.me/problems/no/2929)
- [★2.5／diffデータなし](https://yukicoder.me/problems/no/2598)
- [★2.5／diff <font color="blue">1996</font>](https://yukicoder.me/problems/no/2532)
- [★2.5／diff <font color="yellowgreen">2030</font>](https://yukicoder.me/problems/no/2700)
- [★3／diff <font color="yellowgreen">2145</font>](https://yukicoder.me/problems/no/2816)
- [★3／diff <font color="orange">2799</font>](https://yukicoder.me/problems/no/2983)
- [★3.5／diff <font color="orange">2528</font>](https://yukicoder.me/problems/no/2702)
- [★3.5／diff <font color="red">2876</font>](https://yukicoder.me/problems/no/2703)
- [★4／diff <font color="darkgoldenrod ">3244</font>](https://yukicoder.me/problems/no/2705)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 3問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 3問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 2問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 2問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 2問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 2問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 2問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 2問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [minimax法](https://p-adic.github.io/yukicoder-difficulty-statistics/#minimax法) × 1問
- [グラフの構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの構築) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ソート前の添字復元](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート前の添字復元) × 1問
- [テストケースの構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#テストケースの構築) × 1問
- [位取り記法表示・桁和を用いた倍数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示・桁和を用いた倍数判定) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [最近点計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最近点計算) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [制約からグラフの種類を特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#制約からグラフの種類を特定) × 1問
- [積和の和積化](https://p-adic.github.io/yukicoder-difficulty-statistics/#積和の和積化) × 1問
- [全方位木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#全方位木DP) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [素数を用いた構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を用いた構築) × 1問
- [総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和計算の期待値への帰着) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [埋め込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#埋め込み) × 1問
- [木の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の構築) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [連結部分集合列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結部分集合列挙) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [nwoさん](https://yukicoder.me/users/18753)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">1182</font>](https://yukicoder.me/problems/no/2373)

### 過去問の解法頻度

- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問


## [tfltkpcさん](https://yukicoder.me/users/18804)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1260</font>](https://yukicoder.me/problems/no/2811)
- [★3／diff <font color="yellowgreen">2004</font>](https://yukicoder.me/problems/no/2807)

### 過去問の解法頻度

- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#包除原理) × 1問


## [highlighterさん](https://yukicoder.me/users/18808)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diff <font color="yellowgreen">2364</font>](https://yukicoder.me/problems/no/2809)
- [★3.5／diff <font color="orange">2464</font>](https://yukicoder.me/problems/no/2817)
- [★3.5／diff <font color="red">2823</font>](https://yukicoder.me/problems/no/2818)
- [★4／diff <font color="orange">2662</font>](https://yukicoder.me/problems/no/2810)

### 過去問の解法頻度

- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [区間kth取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間kth取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問


## [Astral__さん](https://yukicoder.me/users/18869)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="orange">2721</font>](https://yukicoder.me/problems/no/2434)

### 過去問の解法頻度

- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問


## [獅子座じゃない人さん](https://yukicoder.me/users/19068)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">280</font>](https://yukicoder.me/problems/no/2399)
- [★1／diff <font color="gray">344</font>](https://yukicoder.me/problems/no/2400)
- [★1.5／diff <font color="brown">603</font>](https://yukicoder.me/problems/no/2401)
- [★1.5／diff <font color="green">1027</font>](https://yukicoder.me/problems/no/2508)
- [★2／diff <font color="green">822</font>](https://yukicoder.me/problems/no/2402)
- [★3／diff <font color="deepskyblue">1406</font>](https://yukicoder.me/problems/no/2902)
- [★3／diff <font color="blue">1900</font>](https://yukicoder.me/problems/no/2903)
- [★3／diff <font color="yellowgreen">2123</font>](https://yukicoder.me/problems/no/2403)
- [★3／diff <font color="yellowgreen">2284</font>](https://yukicoder.me/problems/no/2406)
- [★3／diff <font color="yellowgreen">2337</font>](https://yukicoder.me/problems/no/2404)
- [★3／diff <font color="orange">2451</font>](https://yukicoder.me/problems/no/2389)
- [★3.5／diff <font color="blue">1900</font>](https://yukicoder.me/problems/no/2904)
- [★3.5／diff <font color="orange">2741</font>](https://yukicoder.me/problems/no/2405)
- [★3.5／diff <font color="red">2807</font>](https://yukicoder.me/problems/no/2905)
- [★4.5／diff <font color="red">2991</font>](https://yukicoder.me/problems/no/2906)
- [★4.5／diff <font color="red">2991</font>](https://yukicoder.me/problems/no/2907)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 3問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [bitDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitDP) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [convex hull trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#convex hull trick) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [slope trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#slope trick) × 1問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [オイラーグラフ判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーグラフ判定) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ変換) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [メビウスの反転公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウスの反転公式) × 1問
- [メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#メビウス変換) × 1問
- [ルジャンドルの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ルジャンドルの公式) × 1問
- [一次式の族の最大・最小値取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の族の最大・最小値取得) × 1問
- [解の公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#解の公式) × 1問
- [階数因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#階数因数分解) × 1問
- [階数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階数計算) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [期待値漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値漸化式) × 1問
- [狭義単調関数の単射性](https://p-adic.github.io/yukicoder-difficulty-statistics/#狭義単調関数の単射性) × 1問
- [行列の階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の階段化) × 1問
- [行列の簡約階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の簡約階段化) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [素数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列挙) × 1問
- [掃き出し法](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [総和計算を終切片の逆像の数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和計算を終切片の逆像の数え上げに帰着) × 1問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 1問
- [中間値の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#中間値の定理) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [到達可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#到達可能性判定) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [凸関数の高々２対１性](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸関数の高々２対１性) × 1問
- [凸最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸最適化) × 1問
- [倍数走査による約数列挙前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数走査による約数列挙前計算) × 1問
- [微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分計算) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [複素数演算](https://p-adic.github.io/yukicoder-difficulty-statistics/#複素数演算) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#包除原理) × 1問
- [約数ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数ゼータ変換) × 1問
- [約数メビウス変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数メビウス変換) × 1問
- [約数走査を倍数走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数走査を倍数走査に帰着) × 1問
- [約数包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数包除原理) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [冪乗数である約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗数である約数列挙) × 1問


## [Yoyoyo8128さん](https://yukicoder.me/users/19113)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="blue">1698</font>](https://yukicoder.me/problems/no/2812)
- [★3／diff <font color="orange">2676</font>](https://yukicoder.me/problems/no/2814)

### 過去問の解法頻度

- [最終手番に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番に注目) × 2問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [リュカの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#リュカの定理) × 1問
- [最終手番の任意性](https://p-adic.github.io/yukicoder-difficulty-statistics/#最終手番の任意性) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問


## [みどりむしさん](https://yukicoder.me/users/19141)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="blue">1807</font>](https://yukicoder.me/problems/no/2820)
- [★2.5／diff <font color="deepskyblue">1596</font>](https://yukicoder.me/problems/no/2819)
- [★3／diff <font color="blue">1905</font>](https://yukicoder.me/problems/no/2821)
- [★3.5／diff <font color="yellowgreen">2376</font>](https://yukicoder.me/problems/no/2822)
- [★3.5／diff <font color="red">2849</font>](https://yukicoder.me/problems/no/2823)
- [★4／diff <font color="red">2988</font>](https://yukicoder.me/problems/no/2824)
- [★4／diff <font color="red">2988</font>](https://yukicoder.me/problems/no/2826)
- [★4.5／diff <font color="orange">2618</font>](https://yukicoder.me/problems/no/2825)

### 過去問の解法頻度

- [bool値のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#bool値のリアクティブによる特定) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰的構造に沿った再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構造に沿った再帰) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・質問の全探索による操作の構築・質問決定](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・質問の全探索による操作の構築・質問決定) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [無向木の有向化](https://p-adic.github.io/yukicoder-difficulty-statistics/#無向木の有向化) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問


## [bortikさん](https://yukicoder.me/users/19215)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="orange">2628</font>](https://yukicoder.me/problems/no/2431)

### 過去問の解法頻度

- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問


## [ragnaさん](https://yukicoder.me/users/19263)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1385</font>](https://yukicoder.me/problems/no/2569)
- [★2.5／diff <font color="blue">1638</font>](https://yukicoder.me/problems/no/2570)
- [★3.5／diff <font color="orange">2559</font>](https://yukicoder.me/problems/no/2572)

### 過去問の解法頻度

- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#終点からの最短経路長計算) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [有向辺反転](https://p-adic.github.io/yukicoder-difficulty-statistics/#有向辺反転) × 1問


## [Ayunaさん](https://yukicoder.me/users/19431)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1790</font>](https://yukicoder.me/problems/no/2684)

### 過去問の解法頻度

- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問


## [chebrinkoさん](https://yukicoder.me/users/19439)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">769</font>](https://yukicoder.me/problems/no/2424)

### 過去問の解法頻度

- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [Kirby0717さん](https://yukicoder.me/users/19441)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="deepskyblue">1585</font>](https://yukicoder.me/problems/no/2428)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小公倍数計算) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による最小公倍数計算) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [置換の合成](https://p-adic.github.io/yukicoder-difficulty-statistics/#置換の合成) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [binapさん](https://yukicoder.me/users/19515)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1208</font>](https://yukicoder.me/problems/no/2953)
- [★2.5／diff <font color="deepskyblue">1341</font>](https://yukicoder.me/problems/no/3075)
- [★2.5／diff <font color="blue">1728</font>](https://yukicoder.me/problems/no/2955)
- [★2.5／diff <font color="blue">1782</font>](https://yukicoder.me/problems/no/3076)
- [★2.5／diff <font color="blue">1942</font>](https://yukicoder.me/problems/no/3074)
- [★3／diff <font color="blue">1925</font>](https://yukicoder.me/problems/no/2772)
- [★3／diff <font color="blue">1941</font>](https://yukicoder.me/problems/no/2954)
- [★3／diff <font color="blue">1942</font>](https://yukicoder.me/problems/no/3078)
- [★3／diff <font color="yellowgreen">2246</font>](https://yukicoder.me/problems/no/3077)
- [★3／diff <font color="yellowgreen">2354</font>](https://yukicoder.me/problems/no/2764)
- [★3／diff <font color="orange">2585</font>](https://yukicoder.me/problems/no/2957)
- [★3／diff <font color="red">2860</font>](https://yukicoder.me/problems/no/2958)
- [★3.5／diff <font color="yellowgreen">2197</font>](https://yukicoder.me/problems/no/3079)
- [★3.5／diff <font color="yellowgreen">2386</font>](https://yukicoder.me/problems/no/2956)
- [★3.5／diff <font color="orange">2675</font>](https://yukicoder.me/problems/no/3082)
- [★4／diff <font color="yellowgreen">2270</font>](https://yukicoder.me/problems/no/2763)
- [★4／diff <font color="orange">2446</font>](https://yukicoder.me/problems/no/2762)
- [★4／diff <font color="orange">2675</font>](https://yukicoder.me/problems/no/3080)
- [★4／diff <font color="red">2860</font>](https://yukicoder.me/problems/no/2959)
- [★4／diff <font color="red">3102</font>](https://yukicoder.me/problems/no/3081)

### 過去問の解法頻度

- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 5問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 5問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 4問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 3問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 3問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 3問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 3問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 3問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 3問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 2問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 2問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 2問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 2問
- [選択順依存コストナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択順依存コストナップサック最適化) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 2問
- [乱択](https://p-adic.github.io/yukicoder-difficulty-statistics/#乱択) × 2問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [Bostan-Mori法](https://p-adic.github.io/yukicoder-difficulty-statistics/#Bostan-Mori法) × 1問
- [SIMD高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#SIMD高速化) × 1問
- [bitDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitDP) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [convex hull trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#convex hull trick) × 1問
- [max・min・絶対値による区間クエリを集合管理と一次式の一点更新に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値による区間クエリを集合管理と一次式の一点更新に翻訳) × 1問
- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [merge-sort tree](https://p-adic.github.io/yukicoder-difficulty-statistics/#merge-sort tree) × 1問
- [mex取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#mex取得) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [monotone minima](https://p-adic.github.io/yukicoder-difficulty-statistics/#monotone minima) × 1問
- [slope trick](https://p-adic.github.io/yukicoder-difficulty-statistics/#slope trick) × 1問
- [sorted set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted set) × 1問
- [２種の数値を足し引きして１種に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#２種の数値を足し引きして１種に帰着) × 1問
- [２変数関数の１変数を固定した最大・最小値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数関数の１変数を固定した最大・最小値計算) × 1問
- [２変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#２変数決め打ち) × 1問
- [４重以上のループ](https://p-adic.github.io/yukicoder-difficulty-statistics/#４重以上のループ) × 1問
- [クエリソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリソート) × 1問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [コスト変化をコスト上限変化に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#コスト変化をコスト上限変化に翻訳) × 1問
- [ゼータ関数による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ関数による計算量評価) × 1問
- [タイリング・LightsOutの解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#タイリング・LightsOutの解の構築) × 1問
- [タイリング・LightsOut可能性判定を領域の細分による不変量計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#タイリング・LightsOut可能性判定を領域の細分による不変量計算に帰着) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [データ構造をマージする一般的なテク](https://p-adic.github.io/yukicoder-difficulty-statistics/#データ構造をマージする一般的なテク) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [ヘルド・カープ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ヘルド・カープ法) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [ローリングハッシュ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ローリングハッシュ) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [一次式の族の最大・最小値取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式の族の最大・最小値取得) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [可変コスト上限ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#可変コスト上限ナップサック最適化) × 1問
- [回文判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#回文判定) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [期待値漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値漸化式) × 1問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 1問
- [区間和の指定された区間数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和の指定された区間数え上げ) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [左右から走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#左右から走査) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰による多重ループ実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰による多重ループ実装) × 1問
- [最小全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小全域木計算) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除更新) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [最適化を各寄与の最適化に緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#最適化を各寄与の最適化に緩和) × 1問
- [三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の面積計算) × 1問
- [三平方の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#三平方の定理) × 1問
- [始点と終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#始点と終点からの最短経路長計算) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [周期的構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期的構築) × 1問
- [終点からの最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#終点からの最短経路長計算) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [上界制約を無視した数え上げを桁ごとに前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#上界制約を無視した数え上げを桁ごとに前計算) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全域木計算) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解による付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による付値計算) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [底辺と高さを用いた三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#底辺と高さを用いた三角形の面積計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [同値関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#同値関係) × 1問
- [凸最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸最適化) × 1問
- [微分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#微分計算) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [付値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#付値計算) × 1問
- [部分集合DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分集合DP) × 1問
- [部分集合対全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分集合対全探索) × 1問
- [分割統治法（狭義：devide-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（狭義：devide-and-conquer）) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [平均の指定された区間数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#平均の指定された区間数え上げ) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問


## [takumaiqさん](https://yukicoder.me/users/19600)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="brown">779</font>](https://yukicoder.me/problems/no/2479)
- [★2.5／diff <font color="brown">712</font>](https://yukicoder.me/problems/no/2486)

### 過去問の解法頻度

- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成による次元削減) × 1問
- [数列・配列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#数列・配列の構築) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問
- [貪欲法による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法による構築) × 1問


## [DeltaStructさん](https://yukicoder.me/users/19645)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">884</font>](https://yukicoder.me/problems/no/3011)

### 過去問の解法頻度

- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [整数のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#整数のリアクティブによる特定) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問


## [RiRinbaruさん](https://yukicoder.me/users/19688)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1254</font>](https://yukicoder.me/problems/no/3091)
- [★2.5／diff <font color="blue">1783</font>](https://yukicoder.me/problems/no/3093)
- [★2.5／diff <font color="blue">1844</font>](https://yukicoder.me/problems/no/3092)
- [★3／diff <font color="blue">1904</font>](https://yukicoder.me/problems/no/3094)
- [★3.5／diff <font color="orange">2457</font>](https://yukicoder.me/problems/no/3096)
- [★4／diff <font color="orange">2673</font>](https://yukicoder.me/problems/no/3098)
- [★4／diff <font color="orange">2798</font>](https://yukicoder.me/problems/no/3097)

### 過去問の解法頻度

- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [あみだくじと置換の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#あみだくじと置換の対応) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 1問
- [区間max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min取得) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [区間作用更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間作用更新) × 1問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 1問
- [互換と置換の交換関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#互換と置換の交換関係) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の構築) × 1問
- [再帰的構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構築) × 1問
- [最小元の個数計算を最小値とその個数計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小元の個数計算を最小値とその個数計算に帰着) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [小さいケースの構築を拡張](https://p-adic.github.io/yukicoder-difficulty-statistics/#小さいケースの構築を拡張) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [遅延セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#遅延セグメント木) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [YY-otterさん](https://yukicoder.me/users/19760)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">511</font>](https://yukicoder.me/problems/no/3195)
- [★1／diff <font color="brown">621</font>](https://yukicoder.me/problems/no/3196)
- [★1／diff <font color="brown">650</font>](https://yukicoder.me/problems/no/2765)
- [★1.5／diff <font color="brown">621</font>](https://yukicoder.me/problems/no/3197)
- [★2／diff <font color="deepskyblue">1351</font>](https://yukicoder.me/problems/no/2751)
- [★2／diff <font color="blue">1705</font>](https://yukicoder.me/problems/no/2783)
- [★2.5／diff <font color="brown">621</font>](https://yukicoder.me/problems/no/3198)
- [★3／diff <font color="green">1192</font>](https://yukicoder.me/problems/no/3200)
- [★3／diff <font color="deepskyblue">1246</font>](https://yukicoder.me/problems/no/3199)
- [★3／diff <font color="yellowgreen">2297</font>](https://yukicoder.me/problems/no/2788)
- [★3.5／diff <font color="blue">1855</font>](https://yukicoder.me/problems/no/3201)
- [★3.5／diff <font color="yellowgreen">2399</font>](https://yukicoder.me/problems/no/3202)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 4問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 3問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [クエリ先読み](https://p-adic.github.io/yukicoder-difficulty-statistics/#クエリ先読み) × 2問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 2問
- [Disjoint Sparse Table](https://p-adic.github.io/yukicoder-difficulty-statistics/#Disjoint Sparse Table) × 1問
- [Sparse Table](https://p-adic.github.io/yukicoder-difficulty-statistics/#Sparse Table) × 1問
- [エラトステネスの篩](https://p-adic.github.io/yukicoder-difficulty-statistics/#エラトステネスの篩) × 1問
- [グラフの辺の削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の削除更新) × 1問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 1問
- [コストなしナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#コストなしナップサック最適化) × 1問
- [スライド最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#スライド最大・最小化) × 1問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [フロー](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロー) × 1問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [一点max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一点max・min更新) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [外積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積計算) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min取得) × 1問
- [区間の部分列をわたる総和計算をモノイド演算に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の部分列をわたる総和計算をモノイド演算に翻訳) × 1問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [最小カット計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小カット計算) × 1問
- [最大流計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大流計算) × 1問
- [最大流最小カット定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大流最小カット定理) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [選択組み合わせ報酬付きナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択組み合わせ報酬付きナップサック最適化) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [素数列による試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列による試し割り法) × 1問
- [素数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数列挙) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [操作逆順](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作逆順) × 1問
- [総和の指定された部分列数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#総和の指定された部分列数え上げ) × 1問
- [多次元コストナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元コストナップサック割り当て数え上げ) × 1問
- [超頂点追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#超頂点追加) × 1問
- [低次項の追加による線形化](https://p-adic.github.io/yukicoder-difficulty-statistics/#低次項の追加による線形化) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [文字列・配列の追加・挿入の事前処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列・配列の追加・挿入の事前処理) × 1問
- [末尾挿入更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#末尾挿入更新) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問


## [ZOI-dayoさん](https://yukicoder.me/users/19778)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1540</font>](https://yukicoder.me/problems/no/3113)
- [★3／diff <font color="blue">1745</font>](https://yukicoder.me/problems/no/3116)

### 過去問の解法頻度

- [max・min・絶対値の場合分けによる一次式への翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#max・min・絶対値の場合分けによる一次式への翻訳) × 1問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [区間max・min取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間max・min取得) × 1問
- [区間一次式max・min更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間一次式max・min更新) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [双対セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#双対セグメント木) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [木の直径計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の直径計算) × 1問


## [Yama.canさん](https://yukicoder.me/users/19785)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1398</font>](https://yukicoder.me/problems/no/3014)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [next DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#next DP) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [可負価値ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#可負価値ナップサック最適化) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問


## [kjqwさん](https://yukicoder.me/users/20004)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">922</font>](https://yukicoder.me/problems/no/2680)

### 過去問の解法頻度

- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問


## [kikueplさん](https://yukicoder.me/users/20056)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">934</font>](https://yukicoder.me/problems/no/2692)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問


## [kosuke-noriさん](https://yukicoder.me/users/20075)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="yellowgreen">2031</font>](https://yukicoder.me/problems/no/2686)

### 過去問の解法頻度

- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [OR畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#OR畳み込み) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ変換) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [ナップサック分割統治](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック分割統治) × 1問
- [高速ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速ゼータ変換) × 1問
- [合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成による次元削減) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [複数ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数ナップサック最適化) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問


## [sakuraajisaiさん](https://yukicoder.me/users/20115)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">1133</font>](https://yukicoder.me/problems/no/2681)

### 過去問の解法頻度

- [貨幣計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#貨幣計算) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [切り上げ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#切り上げ計算) × 1問
- [選択肢の分割・纏め上げ・追加で良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#選択肢の分割・纏め上げ・追加で良いケースに帰着) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [yuusaanさん](https://yukicoder.me/users/20148)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">212</font>](https://yukicoder.me/problems/no/2773)
- [★1／diff <font color="gray">314</font>](https://yukicoder.me/problems/no/2778)
- [★1／diff <font color="gray">326</font>](https://yukicoder.me/problems/no/3209)
- [★1／diff <font color="brown">444</font>](https://yukicoder.me/problems/no/3083)
- [★1／diff <font color="brown">528</font>](https://yukicoder.me/problems/no/2775)
- [★1／diff <font color="brown">747</font>](https://yukicoder.me/problems/no/2862)
- [★1.5／diff <font color="brown">596</font>](https://yukicoder.me/problems/no/3084)
- [★1.5／diff <font color="brown">683</font>](https://yukicoder.me/problems/no/2776)
- [★1.5／diff <font color="brown">683</font>](https://yukicoder.me/problems/no/2777)
- [★1.5／diff <font color="brown">747</font>](https://yukicoder.me/problems/no/2863)
- [★1.5／diff <font color="green">941</font>](https://yukicoder.me/problems/no/2864)
- [★2／diff <font color="brown">612</font>](https://yukicoder.me/problems/no/2774)
- [★2／diff <font color="green">951</font>](https://yukicoder.me/problems/no/2779)
- [★2／diff <font color="green">1019</font>](https://yukicoder.me/problems/no/2865)
- [★2／diff <font color="green">1040</font>](https://yukicoder.me/problems/no/3085)
- [★2.5／diff <font color="deepskyblue">1350</font>](https://yukicoder.me/problems/no/3087)
- [★2.5／diff <font color="deepskyblue">1389</font>](https://yukicoder.me/problems/no/3086)
- [★2.5／diff <font color="deepskyblue">1542</font>](https://yukicoder.me/problems/no/2780)
- [★2.5／diff <font color="blue">1611</font>](https://yukicoder.me/problems/no/2866)
- [★2.5／diff <font color="blue">1757</font>](https://yukicoder.me/problems/no/2867)
- [★2.5／diff <font color="yellowgreen">2092</font>](https://yukicoder.me/problems/no/3212)
- [★3／diff <font color="deepskyblue">1463</font>](https://yukicoder.me/problems/no/3088)
- [★3／diff <font color="yellowgreen">2048</font>](https://yukicoder.me/problems/no/3089)
- [★3／diff <font color="yellowgreen">2191</font>](https://yukicoder.me/problems/no/2868)
- [★3.5／diff <font color="yellowgreen">2230</font>](https://yukicoder.me/problems/no/2869)
- [★3.5／diff <font color="yellowgreen">2288</font>](https://yukicoder.me/problems/no/3090)
- [★4／diff <font color="yellowgreen">2397</font>](https://yukicoder.me/problems/no/3215)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 8問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 5問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 3問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 3問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 2問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 2問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 2問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 2問
- [整数のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#整数のリアクティブによる特定) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 2問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 2問
- [１つの桁・成分のみ特定する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#１つの桁・成分のみ特定する質問) × 1問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [スタック](https://p-adic.github.io/yukicoder-difficulty-statistics/#スタック) × 1問
- [トポロジカルソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#トポロジカルソート) × 1問
- [ナップサックDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサックDP) × 1問
- [ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック割り当て数え上げ) × 1問
- [ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#ナップサック最適化) × 1問
- [ニム和](https://p-adic.github.io/yukicoder-difficulty-statistics/#ニム和) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [一次式のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#一次式のリアクティブによる特定) × 1問
- [可負コストナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#可負コストナップサック割り当て数え上げ) × 1問
- [可負コストナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#可負コストナップサック最適化) × 1問
- [可負価値ナップサック割り当て数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#可負価値ナップサック割り当て数え上げ) × 1問
- [可負価値ナップサック最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#可負価値ナップサック最適化) × 1問
- [貨幣計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#貨幣計算) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [強連結成分分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#強連結成分分解) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [合成による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#合成による次元削減) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [再帰的構造に沿った再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構造に沿った再帰) × 1問
- [最小全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小全域木計算) × 1問
- [最大全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大全域木計算) × 1問
- [指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算や指定始切片数え上げや一次元最近点計算をソートに帰着) × 1問
- [指定序数の値の計算を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を指定始切片数え上げに帰着) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [勝利を押し付ける戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#勝利を押し付ける戦略) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [上界制約を無視した数え上げを桁ごとに前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#上界制約を無視した数え上げを桁ごとに前計算) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [切り上げ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#切り上げ計算) × 1問
- [全域木計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全域木計算) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多倍長整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#多倍長整数) × 1問
- [単調関数のファイバーの緩和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#単調関数のファイバーの緩和計算) × 1問
- [到達可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#到達可能性判定) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [独立事象の積への分解による確率計算・数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#独立事象の積への分解による確率計算・数え上げ) × 1問
- [二分法](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分法) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問
- [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量を保つ戦略) × 1問
- [複数底の位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#複数底の位取り記法表示) × 1問
- [分割の均等化](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割の均等化) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [寝癖さん](https://yukicoder.me/users/20337)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">544</font>](https://yukicoder.me/problems/no/2870)
- [★1.5／diff <font color="deepskyblue">1372</font>](https://yukicoder.me/problems/no/2871)
- [★2／diff <font color="deepskyblue">1330</font>](https://yukicoder.me/problems/no/2872)
- [★2.5／diff <font color="blue">1712</font>](https://yukicoder.me/problems/no/2873)
- [★2.5／diff <font color="yellowgreen">2016</font>](https://yukicoder.me/problems/no/2874)
- [★2.5／diff <font color="yellowgreen">2191</font>](https://yukicoder.me/problems/no/2875)
- [★3.5／diff <font color="orange">2584</font>](https://yukicoder.me/problems/no/2876)
- [★4／diff <font color="orange">2533</font>](https://yukicoder.me/problems/no/2877)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 2問
- [01列と括弧列の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と括弧列の対応) × 1問
- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [１変数一次方程式・不等式の求解](https://p-adic.github.io/yukicoder-difficulty-statistics/#１変数一次方程式・不等式の求解) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [既存のアルゴリズムの変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#既存のアルゴリズムの変形) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [期待値漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値漸化式) × 1問
- [極限の打ち切り計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#極限の打ち切り計算) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [座標圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標圧縮) × 1問
- [試行回数・順位の期待値を各試行の実施確率・各項の先着確率の和に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#試行回数・順位の期待値を各試行の実施確率・各項の先着確率の和に帰着) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [遷移の収束](https://p-adic.github.io/yukicoder-difficulty-statistics/#遷移の収束) × 1問
- [全事象探索による確率・期待値計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#全事象探索による確率・期待値計算) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [入れ子の深さを記録する走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#入れ子の深さを記録する走査) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問
- [部分集合の要素全探索を全体集合の要素全探索に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分集合の要素全探索を全体集合の要素全探索に帰着) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [文字列・配列の追加・挿入の事前処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列・配列の追加・挿入の事前処理) × 1問
- [平面走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#平面走査) × 1問
- [閉じた括弧列判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉じた括弧列判定) × 1問
- [変数の対称性](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数の対称性) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [hamo21さん](https://yukicoder.me/users/20489)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="blue">1904</font>](https://yukicoder.me/problems/no/3095)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [Iroha_3856さん](https://yukicoder.me/users/20569)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">576</font>](https://yukicoder.me/problems/no/2878)
- [★1.5／diff <font color="green">989</font>](https://yukicoder.me/problems/no/2879)
- [★2.5／diff <font color="blue">1653</font>](https://yukicoder.me/problems/no/2880)
- [★2.5／diff <font color="blue">1713</font>](https://yukicoder.me/problems/no/2881)
- [★3／diff <font color="yellowgreen">2174</font>](https://yukicoder.me/problems/no/2883)
- [★3／diff <font color="yellowgreen">2248</font>](https://yukicoder.me/problems/no/2882)
- [★3.5／diff <font color="yellowgreen">2335</font>](https://yukicoder.me/problems/no/2885)
- [★3.5／diff <font color="orange">2444</font>](https://yukicoder.me/problems/no/2884)
- [★3.5／diff <font color="orange">2478</font>](https://yukicoder.me/problems/no/2992)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 3問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 2問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [１変数一次方程式・不等式の求解](https://p-adic.github.io/yukicoder-difficulty-statistics/#１変数一次方程式・不等式の求解) × 1問
- [イベントソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#イベントソート) × 1問
- [セグメント木](https://p-adic.github.io/yukicoder-difficulty-statistics/#セグメント木) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [マージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#マージ) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [モノイド演算に関する区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#モノイド演算に関する区間取得) × 1問
- [位取り記法による構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法による構築) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [関数のグラフ形状の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#関数のグラフ形状の変化イベント走査による差分計算) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間の部分列をわたる総和計算をモノイド演算に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の部分列をわたる総和計算をモノイド演算に翻訳) × 1問
- [区間を中間で分割してマージ](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間を中間で分割してマージ) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [最大・最小要素削除](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除) × 1問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [商・剰余の差分計算を約数列挙に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#商・剰余の差分計算を約数列挙に帰着) × 1問
- [商のfloorの種類数による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの種類数による計算量評価) × 1問
- [商のfloorの値ごとに纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの値ごとに纏め上げ) × 1問
- [剰余の被除数を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余の被除数を止める総和計算) × 1問
- [剰余を商のfloorに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余を商のfloorに翻訳) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [代数拡大](https://p-adic.github.io/yukicoder-difficulty-statistics/#代数拡大) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [低次項の追加による線形化](https://p-adic.github.io/yukicoder-difficulty-statistics/#低次項の追加による線形化) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [二項定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項定理) × 1問
- [二次拡大](https://p-adic.github.io/yukicoder-difficulty-statistics/#二次拡大) × 1問
- [倍数走査による約数列挙前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数走査による約数列挙前計算) × 1問
- [非単射関数の像の濃度による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の像の濃度による計算量評価) × 1問
- [非単射関数の値で纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#非単射関数の値で纏め上げ) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [約数走査を倍数走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数走査を倍数走査に帰着) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [kagakukenkyuubuさん](https://yukicoder.me/users/20669)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="green">1174</font>](https://yukicoder.me/problems/no/2945)

### 過去問の解法頻度

- [カレンダー計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カレンダー計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問


## [ArcAkiさん](https://yukicoder.me/users/20672)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3.5／diffデータなし](https://yukicoder.me/problems/no/2909)
- [★4／diff <font color="red">2833</font>](https://yukicoder.me/problems/no/3023)

### 過去問の解法頻度

- [kd木](https://p-adic.github.io/yukicoder-difficulty-statistics/#kd木) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [距離空間の重み付きグラフ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#距離空間の重み付きグラフ化) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [最近点計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最近点計算) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [四分木](https://p-adic.github.io/yukicoder-difficulty-statistics/#四分木) × 1問
- [枝刈り](https://p-adic.github.io/yukicoder-difficulty-statistics/#枝刈り) × 1問
- [写像の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#写像の構築) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [分枝限定法](https://p-adic.github.io/yukicoder-difficulty-statistics/#分枝限定法) × 1問


## [ねしんさん](https://yukicoder.me/users/20998)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">735</font>](https://yukicoder.me/problems/no/2827)
- [★1／diff <font color="green">812</font>](https://yukicoder.me/problems/no/2960)
- [★1.5／diff <font color="green">940</font>](https://yukicoder.me/problems/no/2961)
- [★2.5／diff <font color="deepskyblue">1509</font>](https://yukicoder.me/problems/no/2963)
- [★2.5／diff <font color="deepskyblue">1579</font>](https://yukicoder.me/problems/no/2962)
- [★2.5／diff <font color="blue">1696</font>](https://yukicoder.me/problems/no/2828)
- [★2.5／diff <font color="blue">1762</font>](https://yukicoder.me/problems/no/2964)
- [★2.5／diff <font color="orange">2525</font>](https://yukicoder.me/problems/no/2830)
- [★3／diff <font color="yellowgreen">2025</font>](https://yukicoder.me/problems/no/2829)
- [★3／diff <font color="yellowgreen">2130</font>](https://yukicoder.me/problems/no/2966)
- [★3／diff <font color="orange">2613</font>](https://yukicoder.me/problems/no/2965)
- [★3／diff <font color="orange">2729</font>](https://yukicoder.me/problems/no/2833)
- [★3／diff <font color="red">2812</font>](https://yukicoder.me/problems/no/2832)
- [★3／diff <font color="red">3011</font>](https://yukicoder.me/problems/no/2834)
- [★3.5／diffデータなし](https://yukicoder.me/problems/no/2968)
- [★3.5／diff <font color="orange">2426</font>](https://yukicoder.me/problems/no/2967)
- [★3.5／diff <font color="red">3143</font>](https://yukicoder.me/problems/no/2831)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 7問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 6問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 5問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 5問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 4問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 4問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 4問
- [１つの桁・成分のみ特定する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#１つの桁・成分のみ特定する質問) × 3問
- [整数のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#整数のリアクティブによる特定) × 3問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 3問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 3問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 3問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 2問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 2問
- [フェルマーの小定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理による逆元計算) × 2問
- [リアクティブによるブラックボックス操作](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによるブラックボックス操作) × 2問
- [確率漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#確率漸化式) × 2問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 2問
- [座標のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標のリアクティブによる特定) × 2問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 2問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 2問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 2問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 2問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 2問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 2問
- [01列とグリッド上の経路の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列とグリッド上の経路の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [DPのデータ構造高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#DPのデータ構造高速化) × 1問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 1問
- [next DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#next DP) × 1問
- [setprecision・format](https://p-adic.github.io/yukicoder-difficulty-statistics/#setprecision・format) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [オイラー関数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラー関数計算) × 1問
- [キュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#キュー) × 1問
- [グラフ・状態の圧縮による次元削減](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフ・状態の圧縮による次元削減) × 1問
- [グラフの状態や目的地の変化を有向辺に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの状態や目的地の変化を有向辺に翻訳) × 1問
- [シミュレーション](https://p-adic.github.io/yukicoder-difficulty-statistics/#シミュレーション) × 1問
- [ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゼータ変換) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ド・モルガンの法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#ド・モルガンの法則) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [ラグランジュ補間](https://p-adic.github.io/yukicoder-difficulty-statistics/#ラグランジュ補間) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [円周角の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#円周角の定理) × 1問
- [階差数列](https://p-adic.github.io/yukicoder-difficulty-statistics/#階差数列) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [期待値の線形性](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値の線形性) × 1問
- [期待値漸化式](https://p-adic.github.io/yukicoder-difficulty-statistics/#期待値漸化式) × 1問
- [逆行列計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆行列計算) × 1問
- [区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間の分割を始切片の分割と終切片の組に翻訳して境目を管理する次元圧縮) × 1問
- [区間乗算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間乗算更新) × 1問
- [経路数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路数え上げ) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [高階累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#高階累積和) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 1問
- [三分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#三分探索) × 1問
- [三平方の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#三平方の定理) × 1問
- [指数と対数による冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#指数と対数による冪乗計算) × 1問
- [試し割り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#試し割り法) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [小数型の許容誤差付き二分探索・二分法](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型の許容誤差付き二分探索・二分法) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [素因数分解](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解) × 1問
- [素因数分解によるオイラー関数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解によるオイラー関数計算) × 1問
- [素因数分解による約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#素因数分解による約数列挙) × 1問
- [操作・遷移の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・遷移の纏め上げ) × 1問
- [多次元の最適化を一次元の最適化に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#多次元の最適化を一次元の最適化に帰着) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 1問
- [凸最適化](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸最適化) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [配列を像・頻度表で管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#配列を像・頻度表で管理) × 1問
- [倍数走査による約数列挙前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数走査による約数列挙前計算) × 1問
- [約数ゼータ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数ゼータ変換) × 1問
- [約数計数関数による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数計数関数による計算量評価) × 1問
- [約数走査を倍数走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数走査を倍数走査に帰着) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [隣接行列による遷移計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#隣接行列による遷移計算) × 1問
- [累積積による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による二項係数計算) × 1問
- [累積和・グリッド上のDPを経路数え上げに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和・グリッド上のDPを経路数え上げに翻訳) × 1問
- [連続回数制約を分割の区間長制約に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#連続回数制約を分割の区間長制約に翻訳) × 1問


## [みうねさん](https://yukicoder.me/users/21077)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2.5／diff <font color="blue">1856</font>](https://yukicoder.me/problems/no/3160)

### 過去問の解法頻度

- [01列の累積和との内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列の累積和との内積計算) × 1問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [一点を切片の差に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#一点を切片の差に翻訳) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [等差数列の累積和との内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和との内積計算) × 1問
- [内積と転置の関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積と転置の関係) × 1問
- [内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積計算) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問


## [高橋ゆにさん](https://yukicoder.me/users/21277)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="gray">143</font>](https://yukicoder.me/problems/no/3010)
- [★2.5／diff <font color="deepskyblue">1549</font>](https://yukicoder.me/problems/no/3017)
- [★4／diffデータなし](https://yukicoder.me/problems/no/2918)

### 過去問の解法頻度

- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 2問
- [next_permutation](https://p-adic.github.io/yukicoder-difficulty-statistics/#next_permutation) × 1問
- [スタック](https://p-adic.github.io/yukicoder-difficulty-statistics/#スタック) × 1問
- [解法場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#解法場合分け) × 1問
- [区間削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間削除更新) × 1問
- [区間挿入更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間挿入更新) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [区間長総和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間長総和取得) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [半分全列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#半分全列挙) × 1問
- [部分和の差の最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分和の差の最大・最小化) × 1問


## [friedriceさん](https://yukicoder.me/users/21376)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="yellowgreen">2377</font>](https://yukicoder.me/problems/no/2999)

### 過去問の解法頻度

- [DAG上のDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#DAG上のDP) × 1問
- [inplace DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#inplace DP) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [最遠点計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最遠点計算) × 1問
- [到達可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#到達可能性判定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [kazuppaさん](https://yukicoder.me/users/21418)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">726</font>](https://yukicoder.me/problems/no/2938)
- [★1／diff <font color="green">978</font>](https://yukicoder.me/problems/no/2937)
- [★2／diff <font color="deepskyblue">1277</font>](https://yukicoder.me/problems/no/2939)
- [★2／diff <font color="deepskyblue">1488</font>](https://yukicoder.me/problems/no/2941)
- [★2.5／diff <font color="blue">1661</font>](https://yukicoder.me/problems/no/2940)
- [★2.5／diff <font color="blue">1752</font>](https://yukicoder.me/problems/no/2942)
- [★2.5／diff <font color="blue">1957</font>](https://yukicoder.me/problems/no/2943)
- [★3／diff <font color="yellowgreen">2081</font>](https://yukicoder.me/problems/no/2944)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [多重総和・総乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多重総和・総乗計算) × 2問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [01列とヤング図形の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列とヤング図形の対応) × 1問
- [01列と単調増加列・分割の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と単調増加列・分割の対応) × 1問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 1問
- [next DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#next DP) × 1問
- [★1の64bit整数要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1の64bit整数要求) × 1問
- [オーバーフロー回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#オーバーフロー回避) × 1問
- [フェニック木](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェニック木) × 1問
- [マッチ度ごとに管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#マッチ度ごとに管理) × 1問
- [ヤング図形の転置](https://p-adic.github.io/yukicoder-difficulty-statistics/#ヤング図形の転置) × 1問
- [一要素重複挿入更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素重複挿入更新) × 1問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [区間要素数取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間要素数取得) × 1問
- [区間和取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間和取得) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [商・剰余の差分計算を約数列挙に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#商・剰余の差分計算を約数列挙に帰着) × 1問
- [商のfloorの分子を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの分子を止める総和計算) × 1問
- [商のfloorの分母を止める総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#商のfloorの分母を止める総和計算) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [調和数列による計算量評価](https://p-adic.github.io/yukicoder-difficulty-statistics/#調和数列による計算量評価) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [倍数走査による約数列挙前計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#倍数走査による約数列挙前計算) × 1問
- [符号なし64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#符号なし64bit整数) × 1問
- [符号なし64bit整数によるオーバーフロー回避](https://p-adic.github.io/yukicoder-difficulty-statistics/#符号なし64bit整数によるオーバーフロー回避) × 1問
- [分割数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割数計算) × 1問
- [平方数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方数列の累積和計算) × 1問
- [門松列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#門松列DP) × 1問
- [約数走査を倍数走査に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数走査を倍数走査に帰着) × 1問
- [約数列挙](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数列挙) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [Apollo@Kuroさん](https://yukicoder.me/users/21432)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="yellowgreen">2285</font>](https://yukicoder.me/problems/no/2997)
- [★2.5／diff <font color="green">1176</font>](https://yukicoder.me/problems/no/3013)

### 過去問の解法頻度

- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問


## [eiramさん](https://yukicoder.me/users/21594)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">559</font>](https://yukicoder.me/problems/no/3035)
- [★1.5／diff <font color="green">845</font>](https://yukicoder.me/problems/no/3037)
- [★2／diff <font color="brown">684</font>](https://yukicoder.me/problems/no/3039)

### 過去問の解法頻度

- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [imos法](https://p-adic.github.io/yukicoder-difficulty-statistics/#imos法) × 1問
- [区間加算更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間加算更新) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [平方根のfloor計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根のfloor計算) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方数判定) × 1問
- [約数の個数の偶奇による平方数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#約数の個数の偶奇による平方数判定) × 1問


## [Blue_Sさん](https://yukicoder.me/users/21638)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">684</font>](https://yukicoder.me/problems/no/3038)
- [★3／diff <font color="yellowgreen">2113</font>](https://yukicoder.me/problems/no/3042)
- [★4／diff <font color="yellowgreen">2191</font>](https://yukicoder.me/problems/no/3044)

### 過去問の解法頻度

- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [極小基本互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#極小基本互換表示) × 1問
- [互換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#互換表示) × 1問
- [最遠点計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最遠点計算) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [重心計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#重心計算) × 1問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 1問


## [Nauclhltさん](https://yukicoder.me/users/21654)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">440</font>](https://yukicoder.me/problems/no/3140)
- [★1／diff <font color="brown">624</font>](https://yukicoder.me/problems/no/3036)
- [★1.5／diff <font color="brown">571</font>](https://yukicoder.me/problems/no/3141)
- [★2／diff <font color="brown">787</font>](https://yukicoder.me/problems/no/3142)
- [★2／diff <font color="blue">1664</font>](https://yukicoder.me/problems/no/3143)
- [★2.5／diff <font color="deepskyblue">1460</font>](https://yukicoder.me/problems/no/3040)
- [★2.5／diff <font color="blue">1664</font>](https://yukicoder.me/problems/no/3144)
- [★2.5／diff <font color="yellowgreen">2043</font>](https://yukicoder.me/problems/no/3145)
- [★3／diff <font color="blue">1908</font>](https://yukicoder.me/problems/no/3041)
- [★3／diff <font color="blue">1974</font>](https://yukicoder.me/problems/no/3043)
- [★3／diff <font color="yellowgreen">2154</font>](https://yukicoder.me/problems/no/3147)
- [★3／diff <font color="yellowgreen">2236</font>](https://yukicoder.me/problems/no/3146)
- [★3.5／diff <font color="orange">2565</font>](https://yukicoder.me/problems/no/3148)
- [★4／diff <font color="orange">2580</font>](https://yukicoder.me/problems/no/3045)

### 過去問の解法頻度

- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 4問
- [再帰的構造に沿った再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰的構造に沿った再帰) × 4問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 4問
- [入れ子の深さを記録する走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#入れ子の深さを記録する走査) × 4問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 3問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [カタラン数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カタラン数計算) × 2問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 2問
- [スタック](https://p-adic.github.io/yukicoder-difficulty-statistics/#スタック) × 2問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 2問
- [最大・最小要素取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素取得) × 2問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 2問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [閉じた括弧列判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉じた括弧列判定) × 2問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 2問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 2問
- [bitset高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitset高速化) × 1問
- [bit演算による$64$並列](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit演算による$64$並列) × 1問
- [next DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#next DP) × 1問
- [sorted multiset](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted multiset) × 1問
- [sorted set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted set) × 1問
- [カタラン数の畳み込み計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#カタラン数の畳み込み計算) × 1問
- [スライド最大・最小化](https://p-adic.github.io/yukicoder-difficulty-statistics/#スライド最大・最小化) × 1問
- [トポロジカルソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#トポロジカルソート) × 1問
- [一要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#一要素削除更新) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [最大・最小要素削除更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大・最小要素削除更新) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合の変化イベント走査による差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の変化イベント走査による差分計算) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [数え上げを総和計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#数え上げを総和計算に帰着) × 1問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [動的mod](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的mod) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [二項係数の総和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数の総和計算) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [表示可能性DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#表示可能性DP) × 1問
- [文字列の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#文字列の構築) × 1問
- [閉じた括弧列と根付き木の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#閉じた括弧列と根付き木の対応) × 1問
- [木の変形における葉の連続削除をノードの縮約に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の変形における葉の連続削除をノードの縮約に翻訳) × 1問
- [優先度付きキュー](https://p-adic.github.io/yukicoder-difficulty-statistics/#優先度付きキュー) × 1問
- [有理数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#有理数型) × 1問
- [累積積による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による二項係数計算) × 1問
- [累積和](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積和) × 1問


## [ID 21712さん](https://yukicoder.me/users/21712)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="brown">749</font>](https://yukicoder.me/problems/no/3132)
- [★2／diff <font color="blue">1695</font>](https://yukicoder.me/problems/no/3134)
- [★2.5／diff <font color="orange">2654</font>](https://yukicoder.me/problems/no/2986)
- [★3.5／diff <font color="orange">2666</font>](https://yukicoder.me/problems/no/3136)

### 過去問の解法頻度

- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 2問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 2問
- [Cartesian tree](https://p-adic.github.io/yukicoder-difficulty-statistics/#Cartesian tree) × 1問
- [lower_bound・upper_bound取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#lower_bound・upper_bound取得) × 1問
- [next_permutation](https://p-adic.github.io/yukicoder-difficulty-statistics/#next_permutation) × 1問
- [sorted_set](https://p-adic.github.io/yukicoder-difficulty-statistics/#sorted_set) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [位取り記法表示・桁和を用いた倍数判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示・桁和を用いた倍数判定) × 1問
- [帰属区間取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#帰属区間取得) × 1問
- [区間族管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#区間族管理) × 1問
- [経路・手順・遷移の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路・手順・遷移の構築) × 1問
- [桁DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#桁DP) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小公倍数計算) × 1問
- [最大公約数による最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数による最小公倍数計算) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [指定序数の値の計算を指定始切片数え上げに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定序数の値の計算を指定始切片数え上げに帰着) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [巡回置換表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#巡回置換表示) × 1問
- [深さ優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#深さ優先探索) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [置換の位数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#置換の位数計算) × 1問
- [木DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#木DP) × 1問
- [木の頂点の重さ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の頂点の重さ計算) × 1問
- [木の頂点の深さ計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#木の頂点の深さ計算) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問


## [kmmtkmさん](https://yukicoder.me/users/21720)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">1184</font>](https://yukicoder.me/problems/no/3158)

### 過去問の解法頻度

- [01列と非負整数の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と非負整数の対応) × 1問
- [01列と部分集合の対応](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列と部分集合の対応) × 1問
- [01列に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#01列に翻訳) × 1問
- [bitDP](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitDP) × 1問
- [bit全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit全探索) × 1問
- [next_permutation](https://p-adic.github.io/yukicoder-difficulty-statistics/#next_permutation) × 1問
- [ヘルド・カープ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ヘルド・カープ法) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [経路全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#経路全探索) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問


## [jastawayさん](https://yukicoder.me/users/21728)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★3／diff <font color="yellowgreen">2149</font>](https://yukicoder.me/problems/no/3161)

### 過去問の解法頻度

- [kd木](https://p-adic.github.io/yukicoder-difficulty-statistics/#kd木) × 1問
- [１つの桁・成分のみ特定する質問](https://p-adic.github.io/yukicoder-difficulty-statistics/#１つの桁・成分のみ特定する質問) × 1問
- [アルゴリズムのリアクティブ化](https://p-adic.github.io/yukicoder-difficulty-statistics/#アルゴリズムのリアクティブ化) × 1問
- [リアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#リアクティブによる特定) × 1問
- [座標のリアクティブによる特定](https://p-adic.github.io/yukicoder-difficulty-statistics/#座標のリアクティブによる特定) × 1問
- [四分木](https://p-adic.github.io/yukicoder-difficulty-statistics/#四分木) × 1問
- [枝刈り](https://p-adic.github.io/yukicoder-difficulty-statistics/#枝刈り) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [分枝限定法](https://p-adic.github.io/yukicoder-difficulty-statistics/#分枝限定法) × 1問


## [のららさん](https://yukicoder.me/users/21859)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1448</font>](https://yukicoder.me/problems/no/3016)

### 過去問の解法頻度

- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [左右から走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#左右から走査) × 1問
- [差分計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#差分計算) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [変数決め打ち](https://p-adic.github.io/yukicoder-difficulty-statistics/#変数決め打ち) × 1問
- [累積max・min](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積max・min) × 1問


## [ジュ・ビオレ・グレイスさん](https://yukicoder.me/users/21936)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">894</font>](https://yukicoder.me/problems/no/3027)
- [★2／diff <font color="brown">486</font>](https://yukicoder.me/problems/no/3002)
- [★2／diff <font color="brown">486</font>](https://yukicoder.me/problems/no/3003)
- [★2／diff <font color="deepskyblue">1312</font>](https://yukicoder.me/problems/no/3028)
- [★2／diff <font color="deepskyblue">1312</font>](https://yukicoder.me/problems/no/3029)
- [★2／diff <font color="blue">1875</font>](https://yukicoder.me/problems/no/3004)
- [★2.5／diff <font color="deepskyblue">1523</font>](https://yukicoder.me/problems/no/3005)
- [★2.5／diff <font color="deepskyblue">1584</font>](https://yukicoder.me/problems/no/3030)
- [★2.5／diff <font color="blue">1604</font>](https://yukicoder.me/problems/no/3020)
- [★2.5／diff <font color="blue">1828</font>](https://yukicoder.me/problems/no/3006)
- [★3／diff <font color="blue">1985</font>](https://yukicoder.me/problems/no/3031)
- [★3／diff <font color="red">2885</font>](https://yukicoder.me/problems/no/2994)
- [★3／diff <font color="red">2892</font>](https://yukicoder.me/problems/no/3007)
- [★3／diff <font color="red">2892</font>](https://yukicoder.me/problems/no/3008)
- [★3.5／diff <font color="yellowgreen">2257</font>](https://yukicoder.me/problems/no/3032)
- [★3.5／diff <font color="yellowgreen">2373</font>](https://yukicoder.me/problems/no/3033)
- [★3.5／diff <font color="orange">2777</font>](https://yukicoder.me/problems/no/3009)
- [★4／diff <font color="red">2892</font>](https://yukicoder.me/problems/no/3034)

### 過去問の解法頻度

- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 4問
- [線形代数](https://p-adic.github.io/yukicoder-difficulty-statistics/#線形代数) × 4問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 3問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 3問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 3問
- [素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#素集合データ構造) × 3問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 3問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 3問
- [bitset高速化](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitset高速化) × 2問
- [bit演算による$64$並列](https://p-adic.github.io/yukicoder-difficulty-statistics/#bit演算による$64$並列) × 2問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 2問
- [フェルマーの小定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理) × 2問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 2問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 2問
- [実験](https://p-adic.github.io/yukicoder-difficulty-statistics/#実験) × 2問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 2問
- [多点BFS](https://p-adic.github.io/yukicoder-difficulty-statistics/#多点BFS) × 2問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 2問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 2問
- [幅優先探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#幅優先探索) × 2問
- [累積積による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による二項係数計算) × 2問
- [連結成分取得](https://p-adic.github.io/yukicoder-difficulty-statistics/#連結成分取得) × 2問
- [64bit整数](https://p-adic.github.io/yukicoder-difficulty-statistics/#64bit整数) × 1問
- [Polynomial Taylor shift](https://p-adic.github.io/yukicoder-difficulty-statistics/#Polynomial Taylor shift) × 1問
- [bool値の充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#bool値の充足可能性判定) × 1問
- [breakに関する考察](https://p-adic.github.io/yukicoder-difficulty-statistics/#breakに関する考察) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [エルハートの相互律](https://p-adic.github.io/yukicoder-difficulty-statistics/#エルハートの相互律) × 1問
- [エルハートの定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#エルハートの定理) × 1問
- [オイラーの規準](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラーの規準) × 1問
- [グラフの辺の追加更新](https://p-adic.github.io/yukicoder-difficulty-statistics/#グラフの辺の追加更新) × 1問
- [スタック](https://p-adic.github.io/yukicoder-difficulty-statistics/#スタック) × 1問
- [ソートによる多重集合の一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソートによる多重集合の一致判定) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ディオファントス方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#ディオファントス方程式の解の構築) × 1問
- [パスカルの三角形](https://p-adic.github.io/yukicoder-difficulty-statistics/#パスカルの三角形) × 1問
- [フロベニウス準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#フロベニウス準同型) × 1問
- [ホモロジー計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#ホモロジー計算) × 1問
- [ポテンシャル付き素集合データ構造](https://p-adic.github.io/yukicoder-difficulty-statistics/#ポテンシャル付き素集合データ構造) × 1問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 1問
- [ラグランジュ補間](https://p-adic.github.io/yukicoder-difficulty-statistics/#ラグランジュ補間) × 1問
- [右手・左手系判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#右手・左手系判定) × 1問
- [円周角の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#円周角の定理) × 1問
- [回転数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#回転数計算) × 1問
- [階乗による多項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による多項係数計算) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階数計算) × 1問
- [外積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積計算) × 1問
- [基底に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#基底に帰着) × 1問
- [基底計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#基底計算) × 1問
- [既出を検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#既出を検索) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [逆行列計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆行列計算) × 1問
- [互換と置換の交換関係](https://p-adic.github.io/yukicoder-difficulty-statistics/#互換と置換の交換関係) × 1問
- [構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#構築) × 1問
- [行列の階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の階段化) × 1問
- [行列の簡約階段化](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列の簡約階段化) × 1問
- [行列式計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列式計算) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 1問
- [三角形分割](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形分割) × 1問
- [次元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#次元計算) × 1問
- [次元定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#次元定理) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [集合・多重集合の一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合・多重集合の一致判定) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [充足可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#充足可能性判定) × 1問
- [十分大きな法で計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#十分大きな法で計算) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [剰余の定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#剰余の定理) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [線分の交差判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#線分の交差判定) × 1問
- [線分の接触判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#線分の接触判定) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [疎な多項式の畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#疎な多項式の畳み込み) × 1問
- [掃き出し法](https://p-adic.github.io/yukicoder-difficulty-statistics/#掃き出し法) × 1問
- [損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics/#損をしない変形) × 1問
- [多項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項係数計算) × 1問
- [対称群の構造に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#対称群の構造に注目) × 1問
- [代数拡大](https://p-adic.github.io/yukicoder-difficulty-statistics/#代数拡大) × 1問
- [第二余弦定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#第二余弦定理) × 1問
- [探索・求解アルゴリズムによる構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#探索・求解アルゴリズムによる構築) × 1問
- [頂点倍化](https://p-adic.github.io/yukicoder-difficulty-statistics/#頂点倍化) × 1問
- [等比数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等比数列の累積和計算) × 1問
- [到達可能性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#到達可能性判定) × 1問
- [凸集合の格子点数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸集合の格子点数え上げ) × 1問
- [内積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#内積計算) × 1問
- [二次拡大](https://p-adic.github.io/yukicoder-difficulty-statistics/#二次拡大) × 1問
- [二部グラフ判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#二部グラフ判定) × 1問
- [二分探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#二分探索) × 1問
- [任意・存在を総AND・ORに翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#任意・存在を総AND・ORに翻訳) × 1問
- [鳩の巣原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#鳩の巣原理) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [平方剰余の相互法則・補充法則](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方剰余の相互法則・補充法則) × 1問
- [平方剰余判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方剰余判定) × 1問
- [法B係数連立一次方程式の解の構築](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の構築) × 1問
- [法B係数連立一次方程式の解の存在判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#法B係数連立一次方程式の解の存在判定) × 1問
- [良いケースに帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#良いケースに帰着) × 1問
- [連想配列](https://p-adic.github.io/yukicoder-difficulty-statistics/#連想配列) × 1問
- [連立一次不等式の解の数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#連立一次不等式の解の数え上げ) × 1問
- [冪乗による根号消去](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗による根号消去) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


## [Naru820さん](https://yukicoder.me/users/22124)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1.5／diff <font color="green">984</font>](https://yukicoder.me/problems/no/3110)
- [★1.5／diff <font color="green">1170</font>](https://yukicoder.me/problems/no/3109)
- [★2／diff <font color="deepskyblue">1380</font>](https://yukicoder.me/problems/no/3111)
- [★2／diff <font color="deepskyblue">1518</font>](https://yukicoder.me/problems/no/3112)
- [★3／diff <font color="yellowgreen">2018</font>](https://yukicoder.me/problems/no/3118)
- [★3.5／diffデータなし](https://yukicoder.me/problems/no/3046)
- [★3.5／diff <font color="orange">2548</font>](https://yukicoder.me/problems/no/3122)

### 過去問の解法頻度

- [再帰](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰) × 2問
- [不変量に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量に注目) × 2問
- [分割統治法（広義：decrease-and-conquer）](https://p-adic.github.io/yukicoder-difficulty-statistics/#分割統治法（広義：decrease-and-conquer）) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 1問
- [next_permutation](https://p-adic.github.io/yukicoder-difficulty-statistics/#next_permutation) × 1問
- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [４重以上のループ](https://p-adic.github.io/yukicoder-difficulty-statistics/#４重以上のループ) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [ソートによる多重集合の一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソートによる多重集合の一致判定) × 1問
- [ダイクストラ法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ダイクストラ法) × 1問
- [データを不変量別に分割して管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#データを不変量別に分割して管理) × 1問
- [ミラー戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#ミラー戦略) × 1問
- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [移動者の状態や選択履歴を頂点情報に追加](https://p-adic.github.io/yukicoder-difficulty-statistics/#移動者の状態や選択履歴を頂点情報に追加) × 1問
- [再帰による多重ループ実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#再帰による多重ループ実装) × 1問
- [最短経路長計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最短経路長計算) × 1問
- [指定始切片数え上げ・総和計算を桁ごとの計算に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#指定始切片数え上げ・総和計算を桁ごとの計算に帰着) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合・多重集合の一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合・多重集合の一致判定) × 1問
- [集合の要素数による各要素の不一致性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合の要素数による各要素の不一致性判定) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [場合分け](https://p-adic.github.io/yukicoder-difficulty-statistics/#場合分け) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [操作・選択を数値に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#操作・選択を数値に翻訳) × 1問
- [相手の選択肢をなくす戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#相手の選択肢をなくす戦略) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [等差数列の累積和計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#等差数列の累積和計算) × 1問
- [同じ値の纏め上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#同じ値の纏め上げ) × 1問
- [不変量を保つ戦略](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量を保つ戦略) × 1問
- [不変量比較による一致判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#不変量比較による一致判定) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [Cafe1942さん](https://yukicoder.me/users/22144)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">521</font>](https://yukicoder.me/problems/no/3177)
- [★1.5／diff <font color="gray">266</font>](https://yukicoder.me/problems/no/3149)
- [★1.5／diff <font color="brown">780</font>](https://yukicoder.me/problems/no/3150)
- [★1.5／diff <font color="green">1099</font>](https://yukicoder.me/problems/no/3178)
- [★2／diff <font color="brown">780</font>](https://yukicoder.me/problems/no/3152)
- [★2／diff <font color="green">946</font>](https://yukicoder.me/problems/no/3151)
- [★2／diff <font color="deepskyblue">1506</font>](https://yukicoder.me/problems/no/3179)
- [★2.5／diff <font color="deepskyblue">1448</font>](https://yukicoder.me/problems/no/3153)
- [★2.5／diff <font color="blue">1667</font>](https://yukicoder.me/problems/no/3180)
- [★3／diff <font color="deepskyblue">1542</font>](https://yukicoder.me/problems/no/3154)
- [★3／diff <font color="blue">1667</font>](https://yukicoder.me/problems/no/3181)
- [★3／diff <font color="blue">1676</font>](https://yukicoder.me/problems/no/3213)
- [★3.5／diff <font color="yellowgreen">2152</font>](https://yukicoder.me/problems/no/3182)
- [★3.5／diff <font color="yellowgreen">2247</font>](https://yukicoder.me/problems/no/3214)

### 過去問の解法頻度

- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 3問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 3問
- [bitごとに計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#bitごとに計算) × 2問
- [modint型](https://p-adic.github.io/yukicoder-difficulty-statistics/#modint型) × 2問
- [ユークリッドの互除法](https://p-adic.github.io/yukicoder-difficulty-statistics/#ユークリッドの互除法) × 2問
- [一点を切片の差に翻訳](https://p-adic.github.io/yukicoder-difficulty-statistics/#一点を切片の差に翻訳) × 2問
- [緩和](https://p-adic.github.io/yukicoder-difficulty-statistics/#緩和) × 2問
- [検索](https://p-adic.github.io/yukicoder-difficulty-statistics/#検索) × 2問
- [最大公約数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数計算) × 2問
- [素数を法とする逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#素数を法とする逆元計算) × 2問
- [特殊な入出力](https://p-adic.github.io/yukicoder-difficulty-statistics/#特殊な入出力) × 2問
- [独立事象の積への分解による確率計算・数え上げ](https://p-adic.github.io/yukicoder-difficulty-statistics/#独立事象の積への分解による確率計算・数え上げ) × 2問
- [XOR・反転が2回で戻ることに注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#XOR・反転が2回で戻ることに注目) × 1問
- [setprecision・format](https://p-adic.github.io/yukicoder-difficulty-statistics/#setprecision・format) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [オイラー線](https://p-adic.github.io/yukicoder-difficulty-statistics/#オイラー線) × 1問
- [ギャグ](https://p-adic.github.io/yukicoder-difficulty-statistics/#ギャグ) × 1問
- [ゲルファント変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#ゲルファント変換) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [フェルマーの小定理による逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#フェルマーの小定理による逆元計算) × 1問
- [ヘロンの公式](https://p-adic.github.io/yukicoder-difficulty-statistics/#ヘロンの公式) × 1問
- [右手・左手系判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#右手・左手系判定) × 1問
- [加法定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#加法定理) × 1問
- [階乗による多項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による多項係数計算) × 1問
- [階乗による二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗による二項係数計算) × 1問
- [階乗逆元計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗逆元計算) × 1問
- [階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#階乗計算) × 1問
- [外積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#外積計算) × 1問
- [括弧列DP](https://p-adic.github.io/yukicoder-difficulty-statistics/#括弧列DP) × 1問
- [逆元の再帰計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#逆元の再帰計算) × 1問
- [繰り返し二乗法](https://p-adic.github.io/yukicoder-difficulty-statistics/#繰り返し二乗法) × 1問
- [互いに素に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#互いに素に帰着) × 1問
- [行列累乗](https://p-adic.github.io/yukicoder-difficulty-statistics/#行列累乗) × 1問
- [高速フーリエ変換](https://p-adic.github.io/yukicoder-difficulty-statistics/#高速フーリエ変換) × 1問
- [最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最小公倍数計算) × 1問
- [最大公約数による最小公倍数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#最大公約数による最小公倍数計算) × 1問
- [三角形の内接円の半径計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の内接円の半径計算) × 1問
- [三角形の面積計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#三角形の面積計算) × 1問
- [周期性](https://p-adic.github.io/yukicoder-difficulty-statistics/#周期性) × 1問
- [準同型](https://p-adic.github.io/yukicoder-difficulty-statistics/#準同型) × 1問
- [小数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数型) × 1問
- [小数計算を整数に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#小数計算を整数に帰着) × 1問
- [畳み込み](https://p-adic.github.io/yukicoder-difficulty-statistics/#畳み込み) × 1問
- [数値の文字列受け取り](https://p-adic.github.io/yukicoder-difficulty-statistics/#数値の文字列受け取り) × 1問
- [多角形の凸性判定](https://p-adic.github.io/yukicoder-difficulty-statistics/#多角形の凸性判定) × 1問
- [多項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#多項係数計算) × 1問
- [中国剰余定理](https://p-adic.github.io/yukicoder-difficulty-statistics/#中国剰余定理) × 1問
- [低次項の追加による線形化](https://p-adic.github.io/yukicoder-difficulty-statistics/#低次項の追加による線形化) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [凸包計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#凸包計算) × 1問
- [二項係数計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#二項係数計算) × 1問
- [複素数演算](https://p-adic.github.io/yukicoder-difficulty-statistics/#複素数演算) × 1問
- [平方根処理](https://p-adic.github.io/yukicoder-difficulty-statistics/#平方根処理) × 1問
- [偏角ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#偏角ソート) × 1問
- [包除原理](https://p-adic.github.io/yukicoder-difficulty-statistics/#包除原理) × 1問
- [有理数型](https://p-adic.github.io/yukicoder-difficulty-statistics/#有理数型) × 1問
- [余事象に注目](https://p-adic.github.io/yukicoder-difficulty-statistics/#余事象に注目) × 1問
- [累積積による冪乗・階乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#累積積による冪乗・階乗計算) × 1問
- [冪乗計算](https://p-adic.github.io/yukicoder-difficulty-statistics/#冪乗計算) × 1問


## [uruneaさん](https://yukicoder.me/users/22416)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="green">1084</font>](https://yukicoder.me/problems/no/3135)

### 過去問の解法頻度

- [位取り記法表示](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示) × 1問
- [位取り記法表示で全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#位取り記法表示で全探索) × 1問
- [全探索](https://p-adic.github.io/yukicoder-difficulty-statistics/#全探索) × 1問
- [部分集合の要素全探索を全体集合の要素全探索に帰着](https://p-adic.github.io/yukicoder-difficulty-statistics/#部分集合の要素全探索を全体集合の要素全探索に帰着) × 1問


## [fluorineさん](https://yukicoder.me/users/22470)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★1／diff <font color="brown">571</font>](https://yukicoder.me/problems/no/3155)

### 過去問の解法頻度

- [set](https://p-adic.github.io/yukicoder-difficulty-statistics/#set) × 1問
- [★1.5以下の高速化・基本アルゴリズム要求](https://p-adic.github.io/yukicoder-difficulty-statistics/#★1.5以下の高速化・基本アルゴリズム要求) × 1問
- [ソート](https://p-adic.github.io/yukicoder-difficulty-statistics/#ソート) × 1問
- [実装](https://p-adic.github.io/yukicoder-difficulty-statistics/#実装) × 1問
- [集合管理](https://p-adic.github.io/yukicoder-difficulty-statistics/#集合管理) × 1問
- [頻度表](https://p-adic.github.io/yukicoder-difficulty-statistics/#頻度表) × 1問


## [jupiter_68さん](https://yukicoder.me/users/22503)

### 過去問のレベル（星の数）とdifficulty（実際の解け具合）の組み合わせ

- [★2／diff <font color="deepskyblue">1427</font>](https://yukicoder.me/problems/no/3114)

### 過去問の解法頻度

- [尺取り法](https://p-adic.github.io/yukicoder-difficulty-statistics/#尺取り法) × 1問
- [端から確定](https://p-adic.github.io/yukicoder-difficulty-statistics/#端から確定) × 1問
- [動的計画法](https://p-adic.github.io/yukicoder-difficulty-statistics/#動的計画法) × 1問
- [入れ子の深さを記録する走査](https://p-adic.github.io/yukicoder-difficulty-statistics/#入れ子の深さを記録する走査) × 1問
- [貪欲法](https://p-adic.github.io/yukicoder-difficulty-statistics/#貪欲法) × 1問


