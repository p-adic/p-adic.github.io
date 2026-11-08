---
url: https://p-adic.github.io/competitive-programming-problem-difficulty-setting
layout: blog
title: 競技プログラミング作問の難易度評価方法
date: 2026-11-04
excerpt: "どのように競技プログラミング作問で難易度評価をしているかを書いていきます。"
parent: competitive-programming-blog
prev-child: FFT-on-Qp
next-child: 
blog: true
tags: [競技プログラミング]
---


## 趣旨

筆者（[$p$進大好きbot](https://x.com/non_archimedean)）のyukicoderコンテストに参加しようか検討している人向けに、筆者がyukicoderで作問する際に現在はどのような基準で★の数を設定しているかについてご説明いたします。

作問そのものに興味がある人は

- [競技プログラミング作問時に心掛けていること](https://p-adic.github.io/ruling-on-creating-prolems-for-competitive-programming/)
- [競技プログラミング作問のノウハウ](https://p-adic.github.io/how-to-create-problems-for-competitive-programming/)

もお楽しみください。


## 前置き

競技プログラミングで作問をする時、難易度の評価をする必要があります。特にyukicoderで作問をする場合、★の数で難易度を表す必要があるのですが、その表し方はwriterさんによって千差万別です。例えば

1. yukicoderの過去問と比較して、同程度の難易度の問題と同じ★の数をつける。
1. yukicoderのヘルプを参考にして、想定解のアルゴリズムに対応する★の数をつける。
1. ★の数とAtCoderのdifficultyの間に対応を決め、difficultyを推定してそれに対応する★の数をつける。

などが一般的な方法かなと思います。「この方法でないといけない」などと持論を述べるつもりはなく、あくまで筆者のコンテストに参加しようとしてくださっている人向けに筆者がどうしているかを述べるだけであることにご留意ください。

ごくたまに[作問用チェックリストに反する出題](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#作問用チェックリスト非準拠問題)を見かけますが、たいていのwriterさんは作問用チェックリストを遵守しているため特筆することではないと思うので、以下では作問用チェックリストは遵守していることを前提とします。


## 難易度によらない指針

まず結論から言うと、先程挙げた方法の1・2を折衷して★の数を決めています。つまりyukicoderの過去問とヘルプの療法を参考にして★の数を合わせているということです。

過去問を参照している理由は、

- 過去問に合わせた方が普段からyukicoderで練習なさっている参加者の方々にストレスを与える難易度設定を避けやすいから。
- 過去問に合わせた方が、★1埋めのような特定の難易度埋めで練習している人の妨害をせずに済むから。

が主です。つまり普段からyukicoderを利用していらっしゃる方々にとってのメリットを優先しています。

ヘルプを参照している理由は、

- 運営さんが「[難易度は、ヘルプのものに合わせようプロジェクト](https://x.com/yukicoder/status/1885346502983528662)」を始動した以上、なるべくヘルプに則した難易度設定にすることが運営さんへの礼儀だと思っているから。
- ヘルプが今後も変わらないという前提のもとで、ヘルプに則した方が普遍的な（既存のdifficultyと違ってコンテスト参加者の偏りや実力のインフレに影響を受けない）難易度設定にできるから。
- ヘルプを重視するwriterさんが増えれば増えるほど、ヘルプに合わせた方が他のwriterさんと整合的な難易度設定になり、普段からyukicoderで練習なさっている参加者の方々にストレスを与える難易度設定を避けやすいから。

が主です。つまり運営さんへの感謝と、難易度インフレへの忌避ですね。

では具体的にどう難易度を決めるかですが、第一の指針として過小（普段からyukicoderで練習なさっている参加者の方々にとって★の数が少なくついているように感じさせてしまう難易度設定）を絶対に避けたいと考えています。

そのための対策として

- 過去1年以内に★3で要求されていない手法は極力★3で出題しない。★3未満をつける際も同様で、例えば過去1年以内に★2.5で要求されていない手法は極力★2.5で出題しない。
- 過去3年以内に★3で出題された問題のほぼ上位互換となる問題を★2.5で出題しない。★3未満をつける際も同様で、例えば過去3年以内に★2.5で出題された問題のほぼ上位互換となる問題を★2で出題しない。
- ★3.5以上はupsolveしていないため同様の措置が取れないが、なるべく過小を避けるためにtesterさんがついている場合はtesterさんの難易度評価との$\max$を取る。
- 特殊ジャッジ問題は考察の難しさと実装の難しさに加え、サンプルの確認しにくさとデバッグしにくさが難しさに大きく寄与する点で通常ジャッジ問題と異なるため直接は過去問やヘルプを参考にしにくく、難易度評価する際は特殊ジャッジ特有の難しさを差し引いた上で過去問やヘルプを参考に評価した後で★0.5個分程度上乗せして最終的な★の数を決める。

という方策を取っています。

ただし[ここ最近は★3以下の難易度インフレが激しく](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#難易度インフレ問題)、それこそ過去1年以内に★3で要求されていない手法がそこそこの頻度で★3で出題されているので、upsolveをし続けるのがとても難しく感じています。従ってこの方法での作問がいつまで続けられるかは分かりません。

またあくまで過小を避ける目的なので、過去問を基準に評価した★の数の下界とヘルプを基準に評価した★の数の下界の$\max$を取って★の数を設定しています。

ただしいくつか例外があります。例えばヘルプで★4に挙げられている行列冪乗はそれより少ない★の数でも出題しています。その理由は、★4典型としての行列冪乗は行列を冪乗するアルゴリズム自体が難しいのではなく、非自明な考察でそれらに帰着させることが難しいからです。

つまり★3相当の考察で自然に行列冪乗に帰着できるのであれば★3に設定することもあり得るということです。アルゴリズムとしての難易度自体は他の★3典型とさほど変わりませんので。

同様にヘルプで★3に挙げられている（応用的な）動的計画法と★3.5に挙げられている桁DPと★4.5に挙げられている高速フーリエ変換もそれより少ない★の数でも出題しています。


## 難易度ごとの指針

過去問とヘルプを参考に決めた、難易度ごとの「こういった問題を出題しない（もっと★の数を多くつけた上で出題する）」という指針です（あくまで指針なので実際にそれに反する出題が絶対にないとはいい切れません）。

### ★

- 問題文の通りに素直に実装すれば解ける問題以外は出題しない。例えば非自明な考察や網羅漏れしやすいほど複雑な場合分けは要求しない。
- 多重ループなどの複雑な実装は要求しない。
- ヘルプで★1.5に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#64bit整数">64bit整数</a>は要求しない。
- ヘルプで★1.5に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#小数型">小数誤差</a>は要求しない。
- ヘルプで★1.5に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#リアクティブ問題">リアクティブ形式</a>にしない。
- 以前運営さんに「★1だと数学知識の要求は中学1年レベルかなと思ったりしてます」とお話しを伺ったことがあるので、中学2年レベル以上の数学を前提知識にする問題は出題しない。（必要な知識を問題ページに明記するなど、前提知識にしないようにする）

### ★☆

- 明らかな愚直解が存在しかつそれがTLEするような問題は出題しない。
- ヘルプに「高校数学１年程度の知識（和の公式など）」と記載されているので、高校2年レベル以上の数学を前提知識にする問題は出題しない。（必要な知識を問題ページに明記するなど、前提知識にしないようにする）
- ヘルプに「1e9+7を使う問題（割り算以外）」と記載されているので、<a href="{{ site.url }}/yukicoder-difficulty-statistics#素数を法とする逆元計算>素数を法とする逆元計算</a>は要求しない。
- ヘルプで★2に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#全探索">全探索</a>（非自明な、問題文にそのまま有界な数データや文字列などの具体的な有限集合として与えられているわけではないデータを多次元の有界な数ベクトルデータなどに翻訳する考察の必要な全探索）は要求しない。
- ヘルプで★2に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#ユークリッドの互除法">ユークリッドの互除法</a>は要求しない。
- ヘルプで★2に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#幅優先探索">幅優先探索</a>／<a href="{{ site.url }}/yukicoder-difficulty-statistics#深さ優先探索>深さ優先探索</a>は要求しない。
- ヘルプで★2に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#エラトステネスの篩">エラトステネスの篩</a>は要求しない。
- ヘルプで★2に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#素因数分解">素因数分解</a>（ここでは実行時計算を指す。$6 = 2 \times 3$などの小さいコンパイル時定数の素因数分解は高校1年レベルの数学の知識に収まるので可）は要求しない。
- ヘルプで★2に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#尺取り法">尺取り法</a>は要求しない。
- ヘルプで★2に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#動的計画法">動的計画法</a>は要求しない。
- ヘルプで★2に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#包除原理">包除原理</a>を用いた考察は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#imos法">imos法</a>は要求しない。

### ★★

- ヘルプに「基本的なDP」と記載されているので、<a href="{{ site.url }}/yukicoder-difficulty-statistics#DPのデータ構造高速化">DPのデータ構造高速化</a>（自然に思い付くDP配列の代わりにその累積和をDP配列とする動的計画法など）は要求しない。
- ヘルプで★2.5に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#ダイクストラ法">ダイクストラ法</a>は要求しない。
- ヘルプで★2.5に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#周期性">周期性</a>（非自明な、問題文にほとんど言及されているわけではない周期性）に注目する考察は要求しない。
- ヘルプで★2.5に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#next_permitation">next_permutation</a>は要求しない。
- ヘルプで★2.5に指定されているad hocな考察は要求しない。
- ヘルプで★2.5に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#多倍長整数">多倍長演算</a>はそれを単体で問う（つまり筆算の実装そのものを問う）以外で要求しない。
- ヘルプで★2.5に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#素数を法とする二項係数計算">素数を法とする二項係数計算</a>は要求しない。
- ヘルプで★2.5に指定されている逆関数（初等的でない、一次式と置換＆逆置換と冪乗&累乗根と$\exp$＆$\log$と三角関数＆逆三角関数の組み合わせ以外の）の考察は要求しない。
- 累積和より高度なデータ構造（<a href="{{ site.url }}/yukicoder-difficulty-statistics#フェニック木">フェニック木</a>、<a href="{{ site.url }}/yukicoder-difficulty-statistics#セグメント木">セグメント木</a>、<a href="{{ site.url }}/yukicoder-difficulty-statistics#素集合データ構造">素集合データ構造</a>など）は要求しない。

### ★★☆

- ヘルプで★3に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#ワーシャル・フロイド法">ワーシャル・フロイド法</a>は要求しない。
- ヘルプで★3に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#非自明なトポロジカルソート">トポロジカルソート</a>（非自明な、問題文で頂点に重みが与えられており重みについてソートするだけで自動的にトポロジカルソートになってしまうタイプでないもの）とそれを包含する強連結成分分解は要求しない。
- ヘルプで★3に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#ニム必勝戦略">ニム必勝戦略</a>の知識は要求しない。
- ヘルプで★3に指定されている<a href="{{ site.url }}/yukicoder-difficulty-statistics#優先度付きキュー">優先度付きキュー</a>およびそれより高度なデータ構造である<a href="{{ site.url }}/yukicoder-difficulty-statistics#sorted set">sorted set</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#ベルマン・フォード法">ベルマン・フォード法</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#最小全域木計算">最小全域木計算</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#ポテンシャル付き素集合データ構造">ポテンシャル付き素集合データ構造</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#双対セグメント木">双対セグメント木</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#二次元imos法">二次元imos法</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#Disjoint Sparse Table">Disjoint Sparse Table</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#行列累乗">行列累乗</a>（非自明な、問題文では行列の積で表されていないものを行列の積で表す考察を含むもの）は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#高速フーリエ変換">高速フーリエ変換</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#Convex Hull Trick">Convex Hull Trick</a>は要求しない。
- 整数論の前提知識は<a href="{{ site.url }}/yukicoder-difficulty-statistics#フェルマーの小定理">フェルマーの小定理</a>より高度なものを仮定しない。（特に<a href="{{ site.url }}/yukicoder-difficulty-statistics#オイラーの定理">オイラーの定理</a>や<a href="{{ site.url }}/yukicoder-difficulty-statistics#中国剰余定理">中国剰余定理</a>を要求する問題は★3以上で出すか必要な知識を問題ページに明記する）

### ★★★

- <a href="{{ site.url }}/yukicoder-difficulty-statistics#二次元累積和">二次元累積和</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#動的セグメント木">動的セグメント木</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#遅延セグメント木">遅延セグメント木</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#最大流計算">最大流計算</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#最小費用流計算">最小費用流計算</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#高速ゼータ変換">高速ゼータ変換</a>／<a href="{{ site.url }}/yukicoder-difficulty-statistics#高速メビウス変換">高速メビウス変換</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#約数ゼータ変換">約数ゼータ変換</a>／<a href="{{ site.url }}/yukicoder-difficulty-statistics#約数メビウス変換">約数メビウス変換</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#倍数ゼータ変換">倍数ゼータ変換</a>／<a href="{{ site.url }}/yukicoder-difficulty-statistics#倍数メビウス変換">倍数メビウス変換</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#monotone minima">monotone minima</a>は要求しない。
- <a href="{{ site.url }}/yukicoder-difficulty-statistics#データ構造をマージする一般的なテク">データ構造をマージする一般的なテク</a>
- 線形代数は前述した<a href="{{ site.url }}/yukicoder-difficulty-statistics#行列累乗">行列累乗</a>を除き、<a href="{{ site.url }}/yukicoder-difficulty-statistics#掃き出し法">掃き出し法</a>およびそれ以上に高度な知識を仮定しない。


## 自分用覚え書き

github pagesで数式を使う際は、閉じ括弧と半角アンダーバーの間に半角スラッシュを入れないとmarkdownからhtmlへの翻訳の仕様でバグるらしい。（波括弧でもたまにバグる）

数式環境をくくる大括弧と数式環境内の中括弧や半角空白や濃度のシャープは半角スラッシュ２つ、改行は半角スラッシュ５つ、その他は基本的に半角スラッシュ１つで良さそう。htmlとmathjaxの関係が難しい。

inline数式内の縦棒はlvertなどを使わないとmarkdownの表と認識される。

大括弧の数式環境はアンパサンドで縦位置を揃えられない。

arrayとalignはどちらも使える。arrayが使えない気がしてしまったのは中括弧につける半角スラッシュの個数を間違えていたから。alignはアンパサンドを等号の右側につけて半角空白を２つ入れると幅がちょうど良さそう。arrayなしだとアンパサンドは使えない。
