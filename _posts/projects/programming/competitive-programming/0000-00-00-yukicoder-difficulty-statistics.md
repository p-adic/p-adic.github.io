---
layout: project
title: yukicoder過去問解法別難易度統計
date: 2024-10-25
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

通常問題の問題番号2056から2336まで登録し終わりました。先は長いです。


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

具体的には、64bit整数が集計されているのは★1.5以下の問題だけですし、階乗逆元が集計されているのは★3以下の問題だけです。これは★2以上では64bit整数の使用が特筆するほど高度なテクニックでなく、★3.5以上では階乗逆元が特筆するほど高度なテクニックでないというだけです。★2以上では64bit整数が使われない、★3.5以上では階乗逆元が使われない、という意味ではないのでご注意ください。


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

1. <a href="#特殊な入出力" class="tag">特殊な入出力</a>×3問
1. <a href="#数値の文字列受け取り" class="tag">数値の文字列受け取り</a>×2問
1. <a href="#実装" class="tag">実装</a>×15問
1. <a href="#64bit整数" class="tag">64bit整数</a>×5問
1. <a href="#小数誤差" class="tag">小数誤差</a>×1問
1. <a href="#相似" class="tag">相似</a>×1問
1. <a href="#指定序数の値の計算を桁ごとの数え上げに帰着" class="tag">指定序数の値の計算を桁ごとの数え上げに帰着</a>×1問
1. <a href="#連想配列" class="tag">連想配列</a>×2問
1. <a href="#三角形の成立条件" class="tag">三角形の成立条件</a>×1問
1. <a href="#場合分けによる絶対値計算" class="tag">場合分けによる絶対値計算</a>×1問
1. <a href="#１次式の最大・最小値" class="tag">１次式の最大・最小値</a>×4問
1. <a href="#カレンダー計算" class="tag">カレンダー計算</a>×1問
1. <a href="#動的mod" class="tag">動的mod</a>×1問
1. <a href="#累積積" class="tag">累積積</a>×1問
1. <a href="#組分けの余りに注目" class="tag">組分けの余りに注目</a>×3問
1. <a href="#シミュレーション" class="tag">シミュレーション</a>×6問
1. <a href="#全探索" class="tag">全探索</a>×26問
1. <a href="#サンプルから推測" class="tag">サンプルから推測</a>×1問
1. <a href="#巡回置換表示" class="tag">巡回置換表示</a>×2問
1. <a href="#言及する成分数を最大化する質問" class="tag">言及する成分数を最大化する質問</a>×1問
1. <a href="#グランディ数" class="tag">グランディ数</a>×1問
1. <a href="#遷移の収束" class="tag">遷移の収束</a>×1問
1. <a href="#ド・モルガンの法則" class="tag">ド・モルガンの法則</a>×1問
1. <a href="#検索" class="tag">検索</a>×3問
1. <a href="#頻度表" class="tag">頻度表</a>×7問
1. <a href="#多項定理" class="tag">多項定理</a>×1問
1. <a href="#場合の数" class="tag">場合の数</a>×2問
1. <a href="#括弧列判定" class="tag">括弧列判定</a>×1問
1. <a href="#操作を数値に翻訳" class="tag">操作を数値に翻訳</a>×9問
1. <a href="#階乗付値" class="tag">階乗付値</a>×1問
1. <a href="#解の公式" class="tag">解の公式</a>×1問
1. <a href="#余事象" class="tag">余事象</a>×4問
1. <a href="#ギャグ" class="tag">ギャグ</a>×5問
1. <a href="#累積和" class="tag">累積和</a>×5問
1. <a href="#幅優先探索" class="tag">幅優先探索</a>／BFS×7問
1. <a href="#貪欲法" class="tag">貪欲法</a>×12問
1. <a href="#実験" class="tag">実験</a>×2問
1. <a href="#素集合データ構造" class="tag">素集合データ構造</a>／UnionFind／UF／DSU×7問
1. <a href="#深さ優先探索" class="tag">深さ優先探索</a>／DFS×2問
1. <a href="#DAG上のDP" class="tag">DAG上のDP</a>×2問
1. <a href="#頂点倍加" class="tag">頂点倍加</a>×2問
1. <a href="#場合分け" class="tag">場合分け</a>×27問
1. <a href="#アルゴリズムのリアクティブ化" class="tag">アルゴリズムのリアクティブ化</a>×3問
1. <a href="#連長圧縮" class="tag">連長圧縮</a>／ランレングス圧縮／RLE×2問
1. <a href="#良いケースに帰着" class="tag">良いケースに帰着</a>×2問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#良いケースに帰着)）
1. <a href="#ウノ計算" class="tag">ウノ計算</a>×2問
1. <a href="#小数誤差解消" class="tag">小数誤差解消</a>×2問
1. <a href="#連結成分取得" class="tag">連結成分取得</a>×8問
1. <a href="#同じ値の纏め上げ" class="tag">同じ値の纏め上げ</a>×9問
1. <a href="#サンプルに帰着" class="tag">サンプルに帰着</a>×4問
1. <a href="#ソート" class="tag">ソート</a>×7問
1. <a href="#階乗逆元" class="tag">階乗逆元</a>×5問
1. <a href="#ニム和" class="tag">ニム和</a>×3問
1. <a href="#平方根" class="tag">平方根</a>×3問
1. <a href="#区間管理" class="tag">区間管理</a>×6問
1. <a href="#損をしない変形" class="tag">損をしない変形</a>×10問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)）
1. <a href="#最終ターン数に注目" class="tag">最終ターン数に注目</a>×6問
1. <a href="#最長歩道取得" class="tag">最長歩道取得</a>×1問
1. <a href="#操作回数最小値で判定" class="tag">操作回数最小値で判定</a>×1問
1. <a href="#配列を像で管理" class="tag">配列を像で管理</a>×1問
1. <a href="#set" class="tag">set</a>×1問
1. <a href="#マッチ度ごとに管理" class="tag">マッチ度ごとに管理</a>×4問
1. <a href="#操作逆順" class="tag">操作逆順</a>×1問
1. <a href="#挿入ソート" class="tag">挿入ソート</a>×1問
1. <a href="#$\ell^1$距離から$\ell^{\infty}$距離への変換" class="tag">$\ell^1$距離から$\ell^{\infty}$距離への変換</a>×1問
1. <a href="#最遠点取得" class="tag">最遠点取得</a>×1問
1. <a href="#符号全探索による絶対値計算" class="tag">符号全探索による絶対値計算</a>×1問
1. <a href="#差分計算" class="tag">差分計算</a>×5問
1. <a href="#倍数メビウス変換" class="tag">倍数メビウス変換</a>×1問
1. <a href="#期待値漸化式" class="tag">期待値漸化式</a>×2問
1. <a href="#端から確定" class="tag">端から確定</a>×3問
1. <a href="#円環の倍化実装" class="tag">円環の倍化実装</a>×1問
1. <a href="#左右から走査" class="tag">左右から走査</a>×1問
1. <a href="#区間和の指定された区間計算" class="tag">区間和の指定された区間計算</a>×1問
1. <a href="#尺取り法" class="tag">尺取り法</a>×7問
1. <a href="#表示可能性DP" class="tag">表示可能性DP</a>×2問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#表示可能性DP)）
1. <a href="#部分回文列挙" class="tag">部分回文列挙</a>×1問
1. <a href="#木DP" class="tag">木DP</a>×2問
1. <a href="#包除原理" class="tag">包除原理</a>×2問
1. <a href="#不変量に注目" class="tag">不変量に注目</a>×6問
1. <a href="#ミラー戦略" class="tag">ミラー戦略</a>×4問
1. <a href="#ポテンシャル付き素集合データ集合" class="tag">ポテンシャル付き素集合データ集合</a>×3問
1. <a href="#充足可能性判定" class="tag">充足可能性判定</a>×4問
1. <a href="#周期" class="tag">周期</a>×4問
1. <a href="#Vieta Jumping" class="tag">Vieta Jumping</a>／Root Flipping×1問
1. <a href="#枝刈り" class="tag">枝刈り</a>×5問
1. <a href="#繰り返し二乗法" class="tag">繰り返し二乗法</a>×10問
1. <a href="#不変量を保つ戦略" class="tag">不変量を保つ戦略</a>×2問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#不変量を保つ戦略)）
1. <a href="#合成数を法とする逆元計算" class="tag">合成数を法とする逆元計算</a>×1問
1. <a href="#区間代入更新" class="tag">区間代入更新</a>×1問
1. <a href="#最大・最小要素削除" class="tag">最大・最小要素削除</a>×1問
1. <a href="#優先度付きキュー" class="tag">優先度付きキュー</a>×1問
1. <a href="#剰余計算" class="tag">剰余計算</a>×38問
1. <a href="#逆元の再帰計算" class="tag">逆元の再帰計算</a>×8問
1. <a href="#最終手番の任意性" class="tag">最終手番の任意性</a>×1問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#最終手番の任意性)）
1. <a href="#ダイクストラ法" class="tag">ダイクストラ法</a>／Dijkstra法×2問
1. <a href="#最短経路長取得" class="tag">最短経路長取得</a>×3問
1. <a href="#場合分けによるmin・max計算" class="tag">場合分けによるmin・max計算</a>×2問
1. <a href="#多点BFS" class="tag">多点BFS</a>／多始点BFS×1問
1. <a href="#高さ奇数ニム和" class="tag">高さ奇数ニム和</a>×1問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#高さ奇数ニム和)）
1. <a href="#変数決め打ち" class="tag">変数決め打ち</a>×7問
1. <a href="#クラスカル法" class="tag">クラスカル法</a>／Kruskal法×2問
1. <a href="#冪等重みの最短経路長取得" class="tag">冪等重みの最短経路長取得</a>×2問
1. <a href="#２変数決め打ち" class="tag">２変数決め打ち</a>×1問
1. <a href="#不定方程式の因数分解" class="tag">不定方程式の因数分解</a>×1問
1. <a href="#必勝戦略のリアクティブ化" class="tag">必勝戦略のリアクティブ化</a>×1問
1. <a href="#分枝限定法" class="tag">分枝限定法</a>×26問
1. <a href="#階差数列" class="tag">階差数列</a>×3問
1. <a href="#imos法" class="tag">imos法</a>×3問
1. <a href="#帰属区間取得" class="tag">帰属区間取得</a>×3問
1. <a href="#素数を法とする逆元" class="tag">素数を法とする逆元</a>×12問
1. <a href="#操作の纏め上げ" class="tag">操作の纏め上げ</a>×3問
1. <a href="#端から順に確定" class="tag">端から順に確定</a>×2問
1. <a href="#押し付け戦略" class="tag">押し付け戦略</a>×2問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#押し付け戦略)）
1. <a href="#オイラー関数" class="tag">オイラー関数</a>×2問
1. <a href="#倍数ゼータ変換" class="tag">倍数ゼータ変換</a>×2問
1. <a href="#二分探索" class="tag">二分探索</a>×12問
1. <a href="#距離空間の重み付きグラフ化" class="tag">距離空間の重み付きグラフ化</a>×2問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#距離空間の重み付きグラフ化)）
1. <a href="#フェルマーの小定理" class="tag">フェルマーの小定理</a>×5問
1. <a href="#積和の和積化" class="tag">積和の和積化</a>×2問
1. <a href="#超頂点追加" class="tag">超頂点追加</a>×2問
1. <a href="#最大・最小要素取得" class="tag">最大・最小要素取得</a>×3問
1. <a href="#クエリ先読み" class="tag">クエリ先読み</a>×4問
1. <a href="#イベントソート" class="tag">イベントソート</a>×3問
1. <a href="#動的計画法" class="tag">動的計画法</a>／DP×34問
1. <a href="#bitごとに計算" class="tag">bitごとに計算</a>×8問
1. <a href="#緩和" class="tag">緩和</a>×3問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#緩和)）
1. <a href="#平面走査" class="tag">平面走査</a>×8問
1. <a href="#一要素挿入" class="tag">一要素挿入</a>×4問
1. <a href="#区間kth取得" class="tag">区間kth取得</a>×3問
1. <a href="#一対一対応" class="tag">一対一対応</a>×3問
1. <a href="#半分全列挙" class="tag">半分全列挙</a>×3問
1. <a href="#ゼータ変換" class="tag">ゼータ変換</a>×3問
1. <a href="#メビウス変換" class="tag">メビウス変換</a>×3問
1. <a href="#フェニック木" class="tag">フェニック木</a>／BIT×10問
1. <a href="#行列累乗" class="tag">行列累乗</a>×1問
1. <a href="#ナップサックDP" class="tag">ナップサックDP</a>×3問
1. <a href="#サイクルと非サイクルに分割" class="tag">サイクルと非サイクルに分割</a>×1問
1. <a href="#クエリソート" class="tag">クエリソート</a>×2問
1. <a href="#mex取得" class="tag">mex取得</a>×1問
1. <a href="#スライド最小化" class="tag">スライド最小化</a>×1問
1. <a href="#オイラー関数前計算" class="tag">オイラー関数前計算</a>×1問
1. <a href="#ループ戦略" class="tag">ループ戦略</a>×2問
1. <a href="#ポラードの$\rho$" class="tag">ポラードの$\rho$</a>×1問
1. <a href="#平方剰余" class="tag">平方剰余</a>×1問
1. <a href="#付値管理" class="tag">付値管理</a>×3問
1. <a href="#区間最大・最小値取得" class="tag">区間最大・最小値取得</a>×2問
1. <a href="#素因数分解" class="tag">素因数分解</a>×6問
1. <a href="#総和計算の期待値への帰着" class="tag">総和計算の期待値への帰着</a>×4問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)）
1. <a href="#sorted set" class="tag">sorted set</a>×3問
1. <a href="#一要素削除" class="tag">一要素削除</a>×3問
1. <a href="#区間要素数取得" class="tag">区間要素数取得</a>×2問
1. <a href="#外積" class="tag">外積</a>×1問
1. <a href="#合成による次元削減" class="tag">合成による次元削減</a>×1問
1. <a href="#区間への分割の右端区間の左端を管理" class="tag">区間への分割の右端区間の左端を管理</a>×1問
1. <a href="#区間の重複度計算" class="tag">区間の重複度計算</a>×2問
1. <a href="#素数列挙" class="tag">素数列挙</a>×2問
1. <a href="#グリッド上の価値最大化" class="tag">グリッド上の価値最大化</a>×1問
1. <a href="#確率漸化式" class="tag">確率漸化式</a>×1問
1. <a href="#再帰" class="tag">再帰</a>×6問
1. <a href="#解法場合分け" class="tag">解法場合分け</a>×3問（[解説ページ](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#解法場合分け)）
1. <a href="#データ構造初期化" class="tag">データ構造初期化</a>×1問
1. <a href="#一対一対応と乱択の可換性" class="tag">一対一対応と乱択の可換性</a>×1問
1. <a href="#素集合データ集合" class="tag">素集合データ集合</a>×1問
1. <a href="#頂点倍化" class="tag">頂点倍化</a>×1問
1. <a href="#bitset高速化" class="tag">bitset高速化</a>×1問
1. <a href="#基底" class="tag">基底</a>×1問
1. <a href="#座標圧縮" class="tag">座標圧縮</a>／座圧×4問
1. <a href="#内積の畳み込み計算" class="tag">内積の畳み込み計算</a>×1問
1. <a href="#ダブリング" class="tag">ダブリング</a>×1問
1. <a href="#線形代数" class="tag">線形代数</a>×2問
1. <a href="#bitDP" class="tag">bitDP</a>×1問
1. <a href="#bit全探索" class="tag">bit全探索</a>×1問
1. <a href="#余因子展開" class="tag">余因子展開</a>×1問
1. <a href="#剰余を商に翻訳" class="tag">剰余を商に翻訳</a>×1問
1. <a href="#平方分割" class="tag">平方分割</a>×1問
1. <a href="#フロー" class="tag">フロー</a>×1問
1. <a href="#完全二部マッチング" class="tag">完全二部マッチング</a>×1問
1. <a href="#変数の対称性" class="tag">変数の対称性</a>×1問
1. <a href="#単調関数の像計算" class="tag">単調関数の像計算</a>×1問
1. <a href="#区間削除更新" class="tag">区間削除更新</a>×1問
1. <a href="#区間挿入更新" class="tag">区間挿入更新</a>×1問
1. <a href="#自己写像に翻訳" class="tag">自己写像に翻訳</a>×1問
1. <a href="#準同型" class="tag">準同型</a>×3問
1. <a href="#約数メビウス変換" class="tag">約数メビウス変換</a>×2問
1. <a href="#指定序数の値の計算を各値未満の数え上げに帰着" class="tag">指定序数の値の計算を各値未満の数え上げに帰着</a>×1問
1. <a href="#約数ゼータ変換" class="tag">約数ゼータ変換</a>×1問
1. <a href="#区間和取得" class="tag">区間和取得</a>×3問
1. <a href="#期待値の線形性" class="tag">期待値の線形性</a>×3問
1. <a href="#区間加算更新" class="tag">区間加算更新</a>×4問
1. <a href="#ユークリッドの互除法" class="tag">ユークリッドの互除法</a>×4問
1. <a href="#最大公約数" class="tag">最大公約数</a>／GCD×4問
1. <a href="#互いに素に帰着" class="tag">互いに素に帰着</a>×3問
1. <a href="#DPのデータ構造高速化" class="tag">DPのデータ構造高速化</a>×7問
1. <a href="#調和数列" class="tag">調和数列</a>×4問
1. <a href="#ベン図" class="tag">ベン図</a>×2問
1. <a href="#十分大きな法で計算" class="tag">十分大きな法で計算</a>×3問
1. <a href="#B進法" class="tag">B進法</a>×7問
1. <a href="#小さいケースの構築を拡張" class="tag">小さいケースの構築を拡張</a>×3問
1. <a href="#剰余による確率的判定" class="tag">剰余による確率的判定</a>×2問
1. <a href="#最小素因数前計算" class="tag">最小素因数前計算</a>×2問
1. <a href="#２進法" class="tag">２進法</a>×5問
1. <a href="#交代和" class="tag">交代和</a>×1問
1. <a href="#inplace DP" class="tag">inplace DP</a>×2問
1. <a href="#第二種スターリング数" class="tag">第二種スターリング数</a>×1問
1. <a href="#floor sum" class="tag">floor sum</a>×1問
1. <a href="#フロベニウスの硬貨交換問題" class="tag">フロベニウスの硬貨交換問題</a>×1問
1. <a href="#像決め打ち二分探索" class="tag">像決め打ち二分探索</a>×1問
1. <a href="#カタラン数" class="tag">カタラン数</a>×1問
1. <a href="#01BFS" class="tag">01BFS</a>×1問
1. <a href="#ローリングハッシュ" class="tag">ローリングハッシュ</a>×2問
1. <a href="#最長共通接頭辞" class="tag">最長共通接頭辞</a>／Z-algorithm／LCP×2問
1. <a href="#桁DP" class="tag">桁DP</a>×5問
1. <a href="#高速フーリエ変換" class="tag">高速フーリエ変換</a>／数論的変換／FTT／NTT×4問
1. <a href="#畳み込み" class="tag">畳み込み</a>×4問
1. <a href="#同値関係" class="tag">同値関係</a>×3問
1. <a href="#キュー" class="tag">キュー</a>×1問
1. <a href="#マージ" class="tag">マージ</a>×2問
1. <a href="#区間を中間で分割してマージ" class="tag">区間を中間で分割してマージ</a>×1問
1. <a href="#区間最大・最小値更新" class="tag">区間最大・最小値更新</a>×1問
1. <a href="#分割統治畳み込み" class="tag">分割統治畳み込み</a>／分割統治FFT×2問
1. <a href="#遅延セグメント木" class="tag">遅延セグメント木</a>／遅延セグ木×2問
1. <a href="#バケット分割" class="tag">バケット分割</a>×2問
1. <a href="#区間二次形式取得" class="tag">区間二次形式取得</a>×1問
1. <a href="#区間二次式取得" class="tag">区間二次式取得</a>×1問
1. <a href="#最近共通祖先" class="tag">最近共通祖先</a>／LCA×1問
1. <a href="#重軽分解" class="tag">重軽分解</a>／HL分解／HLD×1問
1. <a href="#フック長公式" class="tag">フック長公式</a>×1問
1. <a href="#ヤング図形" class="tag">ヤング図形</a>×1問
1. <a href="#トポロジカルソート" class="tag">トポロジカルソート</a>×1問
1. <a href="#強連結成分分解" class="tag">強連結成分分解</a>／SCC×1問
1. <a href="#残余ネットワーク" class="tag">残余ネットワーク</a>×1問
1. <a href="#P-再帰" class="tag">P-再帰</a>／P-recursive×1問
1. <a href="#多点評価" class="tag">多点評価</a>×1問
1. <a href="#評価点シフト" class="tag">評価点シフト</a>×1問
1. <a href="#アルゴリズム中に追加処理" class="tag">アルゴリズム中に追加処理</a>×1問
1. <a href="#ハミルトン路" class="tag">ハミルトン路</a>×1問
1. <a href="#構文解析" class="tag">構文解析</a>×1問

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

　
<h2 id="実装">3. 実装</h2>

### 難易度統計

「実装」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.3/752
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.3/741
- 2022年のコンテスト平均難易度/difficulty: 1.3/787

### 難易度別問題一覧

「実装」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題, difficulty: 569)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題, difficulty: 938)
- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題, difficulty: 544)
- <a href="https://yukicoder.me/problems/no/2314">No.2314 Backflip</a> (yukicoder contest 390 (2023-05-26) - A問題, difficulty: 340)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2091">No.2091 Shio Ramen (Easy)</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2092">No.2092 Conjugation</a> (yukicoder contest 363 (2022-10-07) - A問題, difficulty: 406)
- <a href="https://yukicoder.me/problems/no/2109">No.2109 Special Week</a> (yukicoder contest 366 (2022-10-28) - A問題, difficulty: 1095)
- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題, difficulty: 999)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題, difficulty: 1060)
- <a href="https://yukicoder.me/problems/no/2246">No.2246 1333-like Number</a> (yukicoder contest 381 (2023-03-17) - A問題, difficulty: 689)
- <a href="https://yukicoder.me/problems/no/2312">No.2312 Turtleman and Gaming Console</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2315">No.2315 Flying Camera</a> (yukicoder contest 390 (2023-05-26) - B問題, difficulty: 592)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題, difficulty: 939)

　
<h2 id="64bit整数">4. 64bit整数</h2>

### 難易度統計

「64bit整数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.4/835
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.3/831
- 2022年のコンテスト平均難易度/difficulty: 1.5/841

### 難易度別問題一覧

「64bit整数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題, difficulty: 544)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)
- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)
- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)
- <a href="https://yukicoder.me/problems/no/2306">No.2306 [Cherry 5th Tune C] ウソツキタマシイ</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - B問題, difficulty: 812)

　
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

　
<h2 id="指定序数の値の計算を桁ごとの数え上げに帰着">7. 指定序数の値の計算を桁ごとの数え上げに帰着</h2>

### 難易度統計

「指定序数の値の計算を桁ごとの数え上げに帰着」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/689
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/689
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「指定序数の値の計算を桁ごとの数え上げに帰着」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2246">No.2246 1333-like Number</a> (yukicoder contest 381 (2023-03-17) - A問題, difficulty: 689)

　
<h2 id="連想配列">8. 連想配列</h2>

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

　
<h2 id="三角形の成立条件">9. 三角形の成立条件</h2>

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

　
<h2 id="場合分けによる絶対値計算">10. 場合分けによる絶対値計算</h2>

### 難易度統計

「場合分けによる絶対値計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/1060
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/1060
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「場合分けによる絶対値計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題, difficulty: 1060)

　
<h2 id="１次式の最大・最小値">11. １次式の最大・最小値</h2>

### 難易度統計

「１次式の最大・最小値」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.5/1073
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.6/1092
- 2022年のコンテスト平均難易度/difficulty: 1/1017

### 難易度別問題一覧

「１次式の最大・最小値」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2138">No.2138 Add Bacon</a> (Advent Calendar Contest 2022 (2022-12-01) - A問題, difficulty: 1017)
- <a href="https://yukicoder.me/problems/no/2208">No.2208 Linear Function</a> (yukicoder contest 376 (2023-02-10) - A問題, difficulty: 443)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題, difficulty: 1060)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)

　
<h2 id="カレンダー計算">12. カレンダー計算</h2>

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

　
<h2 id="動的mod">13. 動的mod</h2>

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

　
<h2 id="累積積">14. 累積積</h2>

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

　
<h2 id="組分けの余りに注目">15. 組分けの余りに注目</h2>

### 難易度統計

「組分けの余りに注目」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.6/1206
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.7/1262
- 2022年のコンテスト平均難易度/difficulty: 1.5/1095

### 難易度別問題一覧

「組分けの余りに注目」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題, difficulty: 331)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)

　
<h2 id="シミュレーション">16. シミュレーション</h2>

### 難易度統計

「シミュレーション」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.9/1165
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.9/1165
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「シミュレーション」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題, difficulty: 999)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題, difficulty: 1060)
- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題, difficulty: 744)

##### ★★

- <a href="https://yukicoder.me/problems/no/2174">No.2174 3 O'clock Easy</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題, difficulty: 939)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)

　
<h2 id="全探索">17. 全探索</h2>

### 難易度統計

「全探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 1.9/1356
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.8/1251
- 2022年のコンテスト平均難易度/difficulty: 2/1689

### 難易度別問題一覧

「全探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2138">No.2138 Add Bacon</a> (Advent Calendar Contest 2022 (2022-12-01) - A問題, difficulty: 1017)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題, difficulty: 569)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題, difficulty: 938)
- <a href="https://yukicoder.me/problems/no/2208">No.2208 Linear Function</a> (yukicoder contest 376 (2023-02-10) - A問題, difficulty: 443)
- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題, difficulty: 331)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題, difficulty: 969)
- <a href="https://yukicoder.me/problems/no/2091">No.2091 Shio Ramen (Easy)</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題, difficulty: 769)
- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題, difficulty: 999)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題, difficulty: 1060)
- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題, difficulty: 744)
- <a href="https://yukicoder.me/problems/no/2315">No.2315 Flying Camera</a> (yukicoder contest 390 (2023-05-26) - B問題, difficulty: 592)

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題, difficulty: 1529)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)
- <a href="https://yukicoder.me/problems/no/2196">No.2196 Pair Bonus</a> (yukicoder contest 374 (2023-01-20) - C問題, difficulty: 1314)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題, difficulty: 1551)
- <a href="https://yukicoder.me/problems/no/2234">No.2234 palindromer</a> (yukicoder contest 379 (2023-03-03) - C問題, difficulty: 1000)
- <a href="https://yukicoder.me/problems/no/2247">No.2247 01 ZigZag</a> (yukicoder contest 381 (2023-03-17) - B問題, difficulty: 1604)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題, difficulty: 2246)
- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題, difficulty: 1331)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題, difficulty: 2471)
- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題, difficulty: 2147)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)

　
<h2 id="サンプルから推測">18. サンプルから推測</h2>

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

　
<h2 id="巡回置換表示">19. 巡回置換表示</h2>

### 難易度統計

「巡回置換表示」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/783
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/783
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「巡回置換表示」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題, difficulty: 849)
- <a href="https://yukicoder.me/problems/no/2316">No.2316 Freight Train</a> (yukicoder contest 390 (2023-05-26) - C問題, difficulty: 718)

　
<h2 id="言及する成分数を最大化する質問">20. 言及する成分数を最大化する質問</h2>

### 難易度統計

「言及する成分数を最大化する質問」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/846
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/846
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「言及する成分数を最大化する質問」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2252">No.2252 Find Zero</a> (yukicoder contest 382 (2023-03-24) - A問題, difficulty: 846)

　
<h2 id="グランディ数">21. グランディ数</h2>

### 難易度統計

「グランディ数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/912
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/912
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「グランディ数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題, difficulty: 912)

　
<h2 id="遷移の収束">22. 遷移の収束</h2>

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

　
<h2 id="ド・モルガンの法則">23. ド・モルガンの法則</h2>

### 難易度統計

「ド・モルガンの法則」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1049
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1049
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「ド・モルガンの法則」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題, difficulty: 1049)

　
<h2 id="検索">24. 検索</h2>

### 難易度統計

「検索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1178
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1768
- 2022年のコンテスト平均難易度/difficulty: 1.5/588

### 難易度別問題一覧

「検索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題, difficulty: 1768)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)

　
<h2 id="頻度表">25. 頻度表</h2>

### 難易度統計

「頻度表」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1183
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1027
- 2022年のコンテスト平均難易度/difficulty: 2/1390

### 難易度別問題一覧

「頻度表」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2153">No.2153 何コーダーが何人？</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - A問題, difficulty: 566)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題, difficulty: 342)

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題, difficulty: 1093)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題, difficulty: 1069)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題, difficulty: 1802)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題, difficulty: 1803)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

　
<h2 id="多項定理">26. 多項定理</h2>

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

　
<h2 id="場合の数">27. 場合の数</h2>

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

　
<h2 id="括弧列判定">28. 括弧列判定</h2>

### 難易度統計

「括弧列判定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1373
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1373
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「括弧列判定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2240">No.2240 WAC</a> (yukicoder contest 380 (2023-03-10) - B問題, difficulty: 1373)

　
<h2 id="操作を数値に翻訳">29. 操作を数値に翻訳</h2>

### 難易度統計

「操作を数値に翻訳」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1379
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1308
- 2022年のコンテスト平均難易度/difficulty: 2/1629

### 難易度別問題一覧

「操作を数値に翻訳」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題, difficulty: 331)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題, difficulty: 1060)

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題, difficulty: 1529)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題, difficulty: 1551)
- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題, difficulty: 831)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題, difficulty: 1331)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)

　
<h2 id="階乗付値">30. 階乗付値</h2>

### 難易度統計

「階乗付値」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2/1605
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1605
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「階乗付値」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題, difficulty: 1605)

　
<h2 id="解の公式">31. 解の公式</h2>

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

　
<h2 id="余事象">32. 余事象</h2>

### 難易度統計

「余事象」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.1/1184
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.1/1184
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「余事象」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題, difficulty: 769)

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題, difficulty: 1049)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題, difficulty: 1257)

　
<h2 id="ギャグ">33. ギャグ</h2>

### 難易度統計

「ギャグ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.1/1310
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.1/1344
- 2022年のコンテスト平均難易度/difficulty: 2/1206

### 難易度別問題一覧

「ギャグ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)
- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題, difficulty: 912)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題, difficulty: 1983)

　
<h2 id="累積和">34. 累積和</h2>

### 難易度統計

「累積和」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.1/1311
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2153
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

##### ★★★

- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題, difficulty: 2153)

　
<h2 id="幅優先探索">35. 幅優先探索</h2>

### 難易度統計

「幅優先探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.1/1321
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.1/1277
- 2022年のコンテスト平均難易度/difficulty: 2/1582

### 難易度別問題一覧

「幅優先探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2064">No.2064 Smallest Sequence on Grid</a> (yukicoder contest 359 (2022-09-02) - B問題, difficulty: 1582)
- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題, difficulty: 849)
- <a href="https://yukicoder.me/problems/no/2316">No.2316 Freight Train</a> (yukicoder contest 390 (2023-05-26) - C問題, difficulty: 718)
- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題, difficulty: 1174)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2178">No.2178 Payable Magic Items</a> (yukicoder contest 372 (2023-01-06) - D問題, difficulty: 1989)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題, difficulty: 1683)

　
<h2 id="貪欲法">36. 貪欲法</h2>

### 難易度統計

「貪欲法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.1/1323
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1098
- 2022年のコンテスト平均難易度/difficulty: 2/1483

### 難易度別問題一覧

「貪欲法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)
- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題, difficulty: 342)

##### ★★

- <a href="https://yukicoder.me/problems/no/2056">No.2056 非力なレッド</a> (yukicoder contest 358 (2022-08-26) - A問題, difficulty: 683)
- <a href="https://yukicoder.me/problems/no/2064">No.2064 Smallest Sequence on Grid</a> (yukicoder contest 359 (2022-09-02) - B問題, difficulty: 1582)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題, difficulty: 849)
- <a href="https://yukicoder.me/problems/no/2307">No.2307 [Cherry 5 th Tune *] Cool 46</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - C問題, difficulty: 1345)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2073">No.2073 Concon Substrings (Swap Version)</a> (yukicoder contest 360 (2022-09-16) - D問題, difficulty: 1802)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題, difficulty: 1200)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題, difficulty: 1758)

　
<h2 id="実験">37. 実験</h2>

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

　
<h2 id="素集合データ構造">38. 素集合データ構造</h2>

### 難易度統計

「素集合データ構造」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1298
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1266
- 2022年のコンテスト平均難易度/difficulty: 2.5/1486

### 難易度別問題一覧

「素集合データ構造」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題, difficulty: 849)
- <a href="https://yukicoder.me/problems/no/2316">No.2316 Freight Train</a> (yukicoder contest 390 (2023-05-26) - C問題, difficulty: 718)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題, difficulty: 1486)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題, difficulty: 1683)
- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題, difficulty: 1302)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題, difficulty: 1795)

　
<h2 id="深さ優先探索">39. 深さ優先探索</h2>

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

　
<h2 id="DAG上のDP">40. DAG上のDP</h2>

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

　
<h2 id="頂点倍加">41. 頂点倍加</h2>

### 難易度統計

「頂点倍加」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1468
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1468
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「頂点倍加」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題, difficulty: 1683)

　
<h2 id="場合分け">42. 場合分け</h2>

### 難易度統計

「場合分け」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1612
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.8/1281
- 2022年のコンテスト平均難易度/difficulty: 2.5/1920

### 難易度別問題一覧

「場合分け」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★

- <a href="https://yukicoder.me/problems/no/2098">No.2098 [Cherry Alpha *] Introduction</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - B問題, difficulty: 862)
- <a href="https://yukicoder.me/problems/no/2175">No.2175 Exciting Combo</a> (yukicoder contest 372 (2023-01-06) - A問題, difficulty: 569)
- <a href="https://yukicoder.me/problems/no/2194">No.2194 兄弟の掛け引き</a> (yukicoder contest 374 (2023-01-20) - A問題, difficulty: 938)
- <a href="https://yukicoder.me/problems/no/2224">No.2224 UFO Game</a> (yukicoder contest 378 (2023-02-24) - A問題, difficulty: 544)
- <a href="https://yukicoder.me/problems/no/2297">No.2297 Best Grouping</a> (yukicoder contest 388 (2023-05-12) - A問題, difficulty: 331)

##### ★☆

- <a href="https://yukicoder.me/problems/no/2063">No.2063 ±2^k operations (easy)</a> (yukicoder contest 359 (2022-09-02) - A問題, difficulty: 969)
- <a href="https://yukicoder.me/problems/no/2110">No.2110 012 Matching</a> (yukicoder contest 366 (2022-10-28) - B問題, difficulty: 1095)
- <a href="https://yukicoder.me/problems/no/2201">No.2201 p@$$w0rd</a> (yukicoder contest 375 (2023-02-03) - A問題, difficulty: 769)
- <a href="https://yukicoder.me/problems/no/2239">No.2239 Friday</a> (yukicoder contest 380 (2023-03-10) - A問題, difficulty: 1060)

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2209">No.2209 Flip and Reverse</a> (yukicoder contest 376 (2023-02-10) - B問題, difficulty: 1008)
- <a href="https://yukicoder.me/problems/no/2247">No.2247 01 ZigZag</a> (yukicoder contest 381 (2023-03-17) - B問題, difficulty: 1604)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)
- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題, difficulty: 1934)
- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題, difficulty: 2039)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題, difficulty: 1803)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)
- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題, difficulty: 2246)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題, difficulty: 1628)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)
- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題, difficulty: 2153)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2151">No.2151 3 on Torus-Lohkous</a> (Advent Calendar Contest 2022 (2022-12-01) - H問題, difficulty: 3257)

　
<h2 id="アルゴリズムのリアクティブ化">43. アルゴリズムのリアクティブ化</h2>

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

　
<h2 id="連長圧縮">44. 連長圧縮</h2>

### 難易度統計

「連長圧縮」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1716
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 1.5/813
- 2022年のコンテスト平均難易度/difficulty: 3/2620

### 難易度別問題一覧

「連長圧縮」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2298">No.2298 yukicounter</a> (yukicoder contest 388 (2023-05-12) - B問題, difficulty: 813)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題, difficulty: 2620)

　
<h2 id="良いケースに帰着">45. 良いケースに帰着</h2>

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

　
<h2 id="ウノ計算">46. ウノ計算</h2>

### 難易度統計

「ウノ計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.2/1795
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1345
- 2022年のコンテスト平均難易度/difficulty: 2.5/2246

### 難易度別問題一覧

「ウノ計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2307">No.2307 [Cherry 5 th Tune *] Cool 46</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - C問題, difficulty: 1345)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2148">No.2148 ひとりUNO</a> (Advent Calendar Contest 2022 (2022-12-01) - E問題, difficulty: 2246)

　
<h2 id="小数誤差解消">47. 小数誤差解消</h2>

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

　
<h2 id="連結成分取得">48. 連結成分取得</h2>

### 難易度統計

「連結成分取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1415
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1405
- 2022年のコンテスト平均難易度/difficulty: 2.5/1486

### 難易度別問題一覧

「連結成分取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)
- <a href="https://yukicoder.me/problems/no/2289">No.2289 順列ソート</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - A問題, difficulty: 849)
- <a href="https://yukicoder.me/problems/no/2316">No.2316 Freight Train</a> (yukicoder contest 390 (2023-05-26) - C問題, difficulty: 718)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題, difficulty: 1486)
- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題, difficulty: 1683)
- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題, difficulty: 1302)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題, difficulty: 1795)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題, difficulty: 2237)

　
<h2 id="同じ値の纏め上げ">49. 同じ値の纏め上げ</h2>

### 難易度統計

「同じ値の纏め上げ」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1573
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.4/1542
- 2022年のコンテスト平均難易度/difficulty: 2.3/1624

### 難易度別問題一覧

「同じ値の纏め上げ」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題, difficulty: 1069)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題, difficulty: 1258)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題, difficulty: 1865)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題, difficulty: 2381)

　
<h2 id="サンプルに帰着">50. サンプルに帰着</h2>

### 難易度統計

「サンプルに帰着」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1591
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1869
- 2022年のコンテスト平均難易度/difficulty: 2/1313

### 難易度別問題一覧

「サンプルに帰着」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2070">No.2070 Icosahedron</a> (yukicoder contest 360 (2022-09-16) - A問題, difficulty: 588)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2112">No.2112 All 2x2 are Equal</a> (yukicoder contest 366 (2022-10-28) - D問題, difficulty: 2039)
- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題, difficulty: 1768)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題, difficulty: 1971)

　
<h2 id="ソート">51. ソート</h2>

### 難易度統計

「ソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1598
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1139
- 2022年のコンテスト平均難易度/difficulty: 2.8/2210

### 難易度別問題一覧

「ソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2334">No.2334 Distinct Cards</a> (yukicoder contest 391 (2023-06-02) - A問題, difficulty: 342)

##### ★★

- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2226">No.2226 Hello, Forgotten World!</a> (yukicoder contest 378 (2023-02-24) - C問題, difficulty: 1551)
- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題, difficulty: 1174)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2210">No.2210 equence Squence Seuence</a> (yukicoder contest 376 (2023-02-10) - C問題, difficulty: 1489)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

　
<h2 id="階乗逆元">52. 階乗逆元</h2>

### 難易度統計

「階乗逆元」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1736
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/2021
- 2022年のコンテスト平均難易度/difficulty: 2.1/1546

### 難易度別問題一覧

「階乗逆元」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題, difficulty: 1356)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題, difficulty: 2121)

　
<h2 id="ニム和">53. ニム和</h2>

### 難易度統計

「ニム和」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1803
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/912
- 2022年のコンテスト平均難易度/difficulty: 2.5/2249

### 難易度別問題一覧

「ニム和」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題, difficulty: 912)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2165">No.2165 Let's Play Nim!</a> (Advent Calendar Contest 2022 (2022-12-01) - P問題, difficulty: 2491)

　
<h2 id="平方根">54. 平方根</h2>

### 難易度統計

「平方根」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.3/1889
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1889
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「平方根」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)
- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題, difficulty: 1768)

　
<h2 id="区間管理">55. 区間管理</h2>

### 難易度統計

「区間管理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.4/1614
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.4/1607
- 2022年のコンテスト平均難易度/difficulty: 2.5/1649

### 難易度別問題一覧

「区間管理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2298">No.2298 yukicounter</a> (yukicoder contest 388 (2023-05-12) - B問題, difficulty: 813)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題, difficulty: 1628)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題, difficulty: 1257)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題, difficulty: 1851)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

　
<h2 id="損をしない変形">56. 損をしない変形</h2>

### 難易度統計

「[損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.4/1745
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.4/1696
- 2022年のコンテスト平均難易度/difficulty: 2.5/1858

### 難易度別問題一覧

「[損をしない変形](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#損をしない変形)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2078">No.2078 魔抜けなパープル</a> (yukicoder contest 361 (2022-09-25) - A問題, difficulty: 1529)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題, difficulty: 1356)
- <a href="https://yukicoder.me/problems/no/2240">No.2240 WAC</a> (yukicoder contest 380 (2023-03-10) - B問題, difficulty: 1373)
- <a href="https://yukicoder.me/problems/no/2247">No.2247 01 ZigZag</a> (yukicoder contest 381 (2023-03-17) - B問題, difficulty: 1604)
- <a href="https://yukicoder.me/problems/no/2307">No.2307 [Cherry 5 th Tune *] Cool 46</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - C問題, difficulty: 1345)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題, difficulty: 1331)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題, difficulty: 2274)
- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題, difficulty: 1758)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2096">No.2096 Rage With Our Friends</a> (yukicoder contest 363 (2022-10-07) - E問題, difficulty: 2690)

　
<h2 id="最終ターン数に注目">57. 最終ターン数に注目</h2>

### 難易度統計

「最終ターン数に注目」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.4/1809
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1666
- 2022年のコンテスト平均難易度/difficulty: 2.3/1951

### 難易度別問題一覧

「最終ターン数に注目」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2209">No.2209 Flip and Reverse</a> (yukicoder contest 376 (2023-02-10) - B問題, difficulty: 1008)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2103">No.2103 ±1s Game</a> (yukicoder contest 365 (2022-10-21) - A問題, difficulty: 1934)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)
- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題, difficulty: 1838)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題, difficulty: 2153)

　
<h2 id="最長歩道取得">58. 最長歩道取得</h2>

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

　
<h2 id="操作回数最小値で判定">59. 操作回数最小値で判定</h2>

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

　
<h2 id="配列を像で管理">60. 配列を像で管理</h2>

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

　
<h2 id="set">61. set</h2>

### 難易度統計

「set」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1302
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1302
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「set」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2290">No.2290 UnUnion Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - B問題, difficulty: 1302)

　
<h2 id="マッチ度ごとに管理">62. マッチ度ごとに管理</h2>

### 難易度統計

「マッチ度ごとに管理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1436
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1625
- 2022年のコンテスト平均難易度/difficulty: 2.5/1247

### 難易度別問題一覧

「マッチ度ごとに管理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題, difficulty: 1628)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題, difficulty: 1220)

　
<h2 id="操作逆順">63. 操作逆順</h2>

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

　
<h2 id="挿入ソート">64. 挿入ソート</h2>

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

　
<h2 id="$\ell^1$距離から$\ell^{\infty}$距離への変換">65. $\ell^1$距離から$\ell^{\infty}$距離への変換</h2>

### 難易度統計

「$\ell^1$距離から$\ell^{\infty}$距離への変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1536
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1536
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「$\ell^1$距離から$\ell^{\infty}$距離への変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2261">No.2261 Coffee</a> (yukicoder contest 383 (2023-04-07) - C問題, difficulty: 1536)

　
<h2 id="最遠点取得">66. 最遠点取得</h2>

### 難易度統計

「最遠点取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1536
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1536
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「最遠点取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2261">No.2261 Coffee</a> (yukicoder contest 383 (2023-04-07) - C問題, difficulty: 1536)

　
<h2 id="符号全探索による絶対値計算">67. 符号全探索による絶対値計算</h2>

### 難易度統計

「符号全探索による絶対値計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1536
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1536
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「符号全探索による絶対値計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2261">No.2261 Coffee</a> (yukicoder contest 383 (2023-04-07) - C問題, difficulty: 1536)

　
<h2 id="差分計算">68. 差分計算</h2>

### 難易度統計

「差分計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1596
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1482
- 2022年のコンテスト平均難易度/difficulty: 3/2049

### 難易度別問題一覧

「差分計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2306">No.2306 [Cherry 5th Tune C] ウソツキタマシイ</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - B問題, difficulty: 812)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題, difficulty: 1331)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)

　
<h2 id="倍数メビウス変換">69. 倍数メビウス変換</h2>

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

　
<h2 id="期待値漸化式">70. 期待値漸化式</h2>

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

　
<h2 id="端から確定">71. 端から確定</h2>

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

　
<h2 id="円環の倍化実装">72. 円環の倍化実装</h2>

### 難易度統計

「円環の倍化実装」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1628
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1628
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「円環の倍化実装」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題, difficulty: 1628)

　
<h2 id="左右から走査">73. 左右から走査</h2>

### 難易度統計

「左右から走査」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1628
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1628
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「左右から走査」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題, difficulty: 1628)

　
<h2 id="区間和の指定された区間計算">74. 区間和の指定された区間計算</h2>

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

　
<h2 id="尺取り法">75. 尺取り法</h2>

### 難易度統計

「尺取り法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1633
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.2/1367
- 2022年のコンテスト平均難易度/difficulty: 3/1988

### 難易度別問題一覧

「尺取り法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2298">No.2298 yukicounter</a> (yukicoder contest 388 (2023-05-12) - B問題, difficulty: 813)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2142">No.2142 Segment Zero</a> (yukicoder contest 370 (2022-12-02) - C問題, difficulty: 1632)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題, difficulty: 1628)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題, difficulty: 1257)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

　
<h2 id="表示可能性DP">76. 表示可能性DP</h2>

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

　
<h2 id="部分回文列挙">77. 部分回文列挙</h2>

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

　
<h2 id="木DP">78. 木DP</h2>

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

　
<h2 id="包除原理">79. 包除原理</h2>

### 難易度統計

「包除原理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1677
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2/1049
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「包除原理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題, difficulty: 1049)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)

　
<h2 id="不変量に注目">80. 不変量に注目</h2>

### 難易度統計

「不変量に注目」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1707
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1363
- 2022年のコンテスト平均難易度/difficulty: 2.8/2052

### 難易度別問題一覧

「不変量に注目」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題, difficulty: 912)
- <a href="https://yukicoder.me/problems/no/2335">No.2335 Jump</a> (yukicoder contest 391 (2023-06-02) - B問題, difficulty: 1025)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題, difficulty: 2153)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題, difficulty: 2500)

　
<h2 id="ミラー戦略">81. ミラー戦略</h2>

### 難易度統計

「ミラー戦略」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1719
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1532
- 2022年のコンテスト平均難易度/difficulty: 2.5/1905

### 難易度別問題一覧

「ミラー戦略」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2282">No.2282 Boxed Nim</a> (yukicoder contest 386 (2023-04-28) - A問題, difficulty: 912)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2059">No.2059 Odd Move Nim</a> (yukicoder contest 358 (2022-08-26) - D問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2126">No.2126 MEX Game</a> (yukicoder contest 368 (2022-11-18) - C問題, difficulty: 1803)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題, difficulty: 2153)

　
<h2 id="ポテンシャル付き素集合データ集合">82. ポテンシャル付き素集合データ集合</h2>

### 難易度統計

「ポテンシャル付き素集合データ集合」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1724
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1724
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「ポテンシャル付き素集合データ集合」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題, difficulty: 1683)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題, difficulty: 2237)

　
<h2 id="充足可能性判定">83. 充足可能性判定</h2>

### 難易度統計

「充足可能性判定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1742
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1742
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「充足可能性判定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2202">No.2202 贅沢てりたまチキン</a> (yukicoder contest 375 (2023-02-03) - B問題, difficulty: 1254)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2277">No.2277 Honest or Dishonest ?</a> (yukicoder contest 385 (2023-04-21) - C問題, difficulty: 1683)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題, difficulty: 1795)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題, difficulty: 2237)

　
<h2 id="周期">84. 周期</h2>

### 難易度統計

「周期」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1755
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1610
- 2022年のコンテスト平均難易度/difficulty: 2.5/2191

### 難易度別問題一覧

「周期」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題, difficulty: 744)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題, difficulty: 1933)
- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題, difficulty: 2153)

　
<h2 id="Vieta Jumping">85. Vieta Jumping</h2>

### 難易度統計

「Vieta Jumping」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1768
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1768
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「Vieta Jumping」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2253">No.2253 Ignore Subtle Differences</a> (yukicoder contest 382 (2023-03-24) - B問題, difficulty: 1768)

　
<h2 id="枝刈り">86. 枝刈り</h2>

### 難易度統計

「枝刈り」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1799
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1560
- 2022年のコンテスト平均難易度/difficulty: 3/2758

### 難易度別問題一覧

「枝刈り」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2259">No.2259 Gas Station</a> (yukicoder contest 383 (2023-04-07) - A問題, difficulty: 744)

##### ★★

- <a href="https://yukicoder.me/problems/no/2233">No.2233 Average</a> (yukicoder contest 379 (2023-03-03) - B問題, difficulty: 939)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題, difficulty: 2758)
- <a href="https://yukicoder.me/problems/no/2213">No.2213 Neq Move</a> (yukicoder contest 376 (2023-02-10) - F問題, difficulty: 2086)
- <a href="https://yukicoder.me/problems/no/2221">No.2221 Set X</a> (yukicoder contest 377 (2023-02-17) - F問題, difficulty: 2471)

　
<h2 id="繰り返し二乗法">87. 繰り返し二乗法</h2>

### 難易度統計

「繰り返し二乗法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1815
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.4/1814
- 2022年のコンテスト平均難易度/difficulty: 2.7/1817

### 難易度別問題一覧

「繰り返し二乗法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題, difficulty: 1261)
- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題, difficulty: 1605)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題, difficulty: 2168)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題, difficulty: 1220)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

　
<h2 id="不変量を保つ戦略">88. 不変量を保つ戦略</h2>

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

　
<h2 id="合成数を法とする逆元計算">89. 合成数を法とする逆元計算</h2>

### 難易度統計

「合成数を法とする逆元計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1838
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1838
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「合成数を法とする逆元計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題, difficulty: 1838)

　
<h2 id="区間代入更新">90. 区間代入更新</h2>

### 難易度統計

「区間代入更新」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1851
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1851
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「区間代入更新」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題, difficulty: 1851)

　
<h2 id="最大・最小要素削除">91. 最大・最小要素削除</h2>

### 難易度統計

「最大・最小要素削除」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1861
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1861
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「最大・最小要素削除」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)

　
<h2 id="優先度付きキュー">92. 優先度付きキュー</h2>

### 難易度統計

「優先度付きキュー」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1861
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1861
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「優先度付きキュー」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)

　
<h2 id="剰余計算">93. 剰余計算</h2>

### 難易度統計

「剰余計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1864
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.4/1689
- 2022年のコンテスト平均難易度/difficulty: 2.6/2059

### 難易度別問題一覧

「剰余計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)
- <a href="https://yukicoder.me/problems/no/2225">No.2225 Treasure Searching Rod (Easy)</a> (yukicoder contest 378 (2023-02-24) - B問題, difficulty: 999)

##### ★★

- <a href="https://yukicoder.me/problems/no/2079">No.2079 aaabbc</a> (yukicoder contest 361 (2022-09-25) - B問題, difficulty: 1261)
- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題, difficulty: 1356)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題, difficulty: 1258)
- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題, difficulty: 831)
- <a href="https://yukicoder.me/problems/no/2299">No.2299 Antitypoglycemia</a> (yukicoder contest 388 (2023-05-12) - C問題, difficulty: 1049)
- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題, difficulty: 1605)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題, difficulty: 2246)
- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)
- <a href="https://yukicoder.me/problems/no/2276">No.2276 I Want AC</a> (yukicoder contest 385 (2023-04-21) - B問題, difficulty: 1331)
- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題, difficulty: 1795)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題, difficulty: 2121)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題, difficulty: 2295)
- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題, difficulty: 2168)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)
- <a href="https://yukicoder.me/problems/no/2134">No.2134 $\sigma$-algebra over Finite Set</a> (yukicoder contest 369 (2022-11-25) - E問題, difficulty: 2245)
- <a href="https://yukicoder.me/problems/no/2156">No.2156 ぞい文字列</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - D問題, difficulty: 1220)
- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題, difficulty: 2673)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題, difficulty: 2758)
- <a href="https://yukicoder.me/problems/no/2172">No.2172 SEARCH in the Text Editor</a> (Advent Calendar Contest 2022 (2022-12-01) - Y問題, difficulty: 2852)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題, difficulty: 1865)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題, difficulty: 2170)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題, difficulty: 2153)
- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題, difficulty: 2237)
- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題, difficulty: 2016)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

　
<h2 id="逆元の再帰計算">94. 逆元の再帰計算</h2>

### 難易度統計

「逆元の再帰計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1909
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.6/1971
- 2022年のコンテスト平均難易度/difficulty: 2.5/1871

### 難易度別問題一覧

「逆元の再帰計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題, difficulty: 1356)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題, difficulty: 2121)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題, difficulty: 2170)

　
<h2 id="最終手番の任意性">95. 最終手番の任意性</h2>

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

　
<h2 id="ダイクストラ法">96. ダイクストラ法</h2>

### 難易度統計

「ダイクストラ法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1979
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1979
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「ダイクストラ法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)
- <a href="https://yukicoder.me/problems/no/2328">No.2328 Build Walls</a> (MMA Contest 015  (2023-05-28) - G問題, difficulty: 1915)

　
<h2 id="最短経路長取得">97. 最短経路長取得</h2>

### 難易度統計

「最短経路長取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1979
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1979
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「最短経路長取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2179">No.2179 Planet Traveler</a> (yukicoder contest 372 (2023-01-06) - E問題, difficulty: 2044)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2328">No.2328 Build Walls</a> (MMA Contest 015  (2023-05-28) - G問題, difficulty: 1915)

　
<h2 id="場合分けによるmin・max計算">98. 場合分けによるmin・max計算</h2>

### 難易度統計

「場合分けによるmin・max計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/1983
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1983
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「場合分けによるmin・max計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)

　
<h2 id="多点BFS">99. 多点BFS</h2>

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

　
<h2 id="高さ奇数ニム和">100. 高さ奇数ニム和</h2>

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

　
<h2 id="変数決め打ち">101. 変数決め打ち</h2>

### 難易度統計

「変数決め打ち」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2028
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.3/1920
- 2022年のコンテスト平均難易度/difficulty: 2.6/2172

### 難易度別問題一覧

「変数決め打ち」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2099">No.2099 [Cherry Alpha B] Time Machine</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - C問題, difficulty: 1730)
- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)
- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2076">No.2076 Concon Substrings (ConVersion)</a> (yukicoder contest 360 (2022-09-16) - G問題, difficulty: 2620)
- <a href="https://yukicoder.me/problems/no/2113">No.2113 Distance Sequence 1.5</a> (yukicoder contest 366 (2022-10-28) - E問題, difficulty: 2168)

　
<h2 id="クラスカル法">102. クラスカル法</h2>

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

　
<h2 id="冪等重みの最短経路長取得">103. 冪等重みの最短経路長取得</h2>

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

　
<h2 id="２変数決め打ち">104. ２変数決め打ち</h2>

### 難易度統計

「２変数決め打ち」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.5/2193
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/2193
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「２変数決め打ち」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)

　
<h2 id="不定方程式の因数分解">105. 不定方程式の因数分解</h2>

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

　
<h2 id="必勝戦略のリアクティブ化">106. 必勝戦略のリアクティブ化</h2>

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

　
<h2 id="分枝限定法">107. 分枝限定法</h2>

### 難易度統計

「分枝限定法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.6/1780
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1596
- 2022年のコンテスト平均難易度/difficulty: 2.7/2037

### 難易度別問題一覧

「分枝限定法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2176">No.2176 LRM Question 1</a> (yukicoder contest 372 (2023-01-06) - B問題, difficulty: 1139)

##### ★★

- <a href="https://yukicoder.me/problems/no/2057">No.2057 Ising Model</a> (yukicoder contest 358 (2022-08-26) - B問題, difficulty: 1728)
- <a href="https://yukicoder.me/problems/no/2094">No.2094 Symmetry</a> (yukicoder contest 363 (2022-10-07) - C問題, difficulty: 1482)
- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)
- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題, difficulty: 1093)
- <a href="https://yukicoder.me/problems/no/2196">No.2196 Pair Bonus</a> (yukicoder contest 374 (2023-01-20) - C問題, difficulty: 1314)
- <a href="https://yukicoder.me/problems/no/2203">No.2203 POWER!!!!!</a> (yukicoder contest 375 (2023-02-03) - C問題, difficulty: 1069)
- <a href="https://yukicoder.me/problems/no/2260">No.2260 Adic Sum</a> (yukicoder contest 383 (2023-04-07) - B問題, difficulty: 1258)
- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題, difficulty: 831)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2200">No.2200 Weird Shortest Path</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題, difficulty: 1257)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題, difficulty: 2295)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2229">No.2229 Treasure Searching Rod (Hard)</a> (yukicoder contest 378 (2023-02-24) - F問題, difficulty: 1865)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題, difficulty: 2170)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題, difficulty: 2153)
- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題, difficulty: 1758)
- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題, difficulty: 2147)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)
- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)
- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題, difficulty: 2381)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
<h2 id="階差数列">108. 階差数列</h2>

### 難易度統計

「階差数列」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.6/1852
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1851
- 2022年のコンテスト平均難易度/difficulty: 2.7/1853

### 難易度別問題一覧

「階差数列」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2111">No.2111 Sum of Diff</a> (yukicoder contest 366 (2022-10-28) - C問題, difficulty: 1206)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題, difficulty: 1851)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2144">No.2144 MM</a> (yukicoder contest 370 (2022-12-02) - E問題, difficulty: 2500)

　
<h2 id="imos法">109. imos法</h2>

### 難易度統計

「imos法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.6/1865
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2237
- 2022年のコンテスト平均難易度/difficulty: 2.5/1680

### 難易度別問題一覧

「imos法」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2154">No.2154 あさかつの参加人数</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - B問題, difficulty: 711)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

　
<h2 id="帰属区間取得">110. 帰属区間取得</h2>

### 難易度統計

「帰属区間取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.6/1996
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2170
- 2022年のコンテスト平均難易度/difficulty: 2.5/1649

### 難易度別問題一覧

「帰属区間取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題, difficulty: 1851)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

　
<h2 id="素数を法とする逆元">111. 素数を法とする逆元</h2>

### 難易度統計

「素数を法とする逆元」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.6/2002
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2040
- 2022年のコンテスト平均難易度/difficulty: 2.5/1964

### 難易度別問題一覧

「素数を法とする逆元」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2131">No.2131 Concon Substrings (COuNt Version)</a> (yukicoder contest 369 (2022-11-25) - B問題, difficulty: 1275)
- <a href="https://yukicoder.me/problems/no/2141">No.2141 Enumeratest</a> (yukicoder contest 370 (2022-12-02) - B問題, difficulty: 1356)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)
- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題, difficulty: 2121)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2105">No.2105 Avoid MeX</a> (yukicoder contest 365 (2022-10-21) - C問題, difficulty: 2327)
- <a href="https://yukicoder.me/problems/no/2127">No.2127 Mod, Sum, Sum, Mod</a> (yukicoder contest 368 (2022-11-18) - D問題, difficulty: 2393)
- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題, difficulty: 2170)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

　
<h2 id="操作の纏め上げ">112. 操作の纏め上げ</h2>

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

　
<h2 id="端から順に確定">113. 端から順に確定</h2>

### 難易度統計

「端から順に確定」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1693
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1693
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「端から順に確定」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題, difficulty: 1628)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2284">No.2284 Assembly</a> (yukicoder contest 386 (2023-04-28) - C問題, difficulty: 1758)

　
<h2 id="押し付け戦略">114. 押し付け戦略</h2>

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

　
<h2 id="オイラー関数">115. オイラー関数</h2>

### 難易度統計

「オイラー関数」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1910
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1910
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「オイラー関数」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2241">No.2241 Reach 1</a> (yukicoder contest 380 (2023-03-10) - C問題, difficulty: 1838)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題, difficulty: 1983)

　
<h2 id="倍数ゼータ変換">116. 倍数ゼータ変換</h2>

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

　
<h2 id="二分探索">117. 二分探索</h2>

### 難易度統計

「二分探索」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/1976
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.4/1831
- 2022年のコンテスト平均難易度/difficulty: 3.5/2364

### 難易度別問題一覧

「二分探索」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2177">No.2177 Recurring ab</a> (yukicoder contest 372 (2023-01-06) - C問題, difficulty: 1856)
- <a href="https://yukicoder.me/problems/no/2325">No.2325 Skill Tree</a> (MMA Contest 015  (2023-05-28) - D問題, difficulty: 1174)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2217">No.2217 Suffix+</a> (yukicoder contest 377 (2023-02-17) - B問題, difficulty: 1200)
- <a href="https://yukicoder.me/problems/no/2227">No.2227 King Kraken's Attack</a> (yukicoder contest 378 (2023-02-24) - D問題, difficulty: 1773)
- <a href="https://yukicoder.me/problems/no/2309">No.2309 [Cherry 5th Tune D] 夏の先取り</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - E問題, difficulty: 2193)
- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題, difficulty: 1774)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題, difficulty: 3018)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)
- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)
- <a href="https://yukicoder.me/problems/no/2085">No.2085 Directed Complete Graph</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

　
<h2 id="距離空間の重み付きグラフ化">118. 距離空間の重み付きグラフ化</h2>

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

　
<h2 id="フェルマーの小定理">119. フェルマーの小定理</h2>

### 難易度統計

「フェルマーの小定理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/2072
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.6/1983
- 2022年のコンテスト平均難易度/difficulty: 3/2430

### 難易度別問題一覧

「フェルマーの小定理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題, difficulty: 1605)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2128">No.2128 Round up!!</a> (yukicoder contest 368 (2022-11-18) - E問題, difficulty: 2430)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

　
<h2 id="積和の和積化">120. 積和の和積化</h2>

### 難易度統計

「積和の和積化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/2079
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2079
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「積和の和積化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

　
<h2 id="超頂点追加">121. 超頂点追加</h2>

### 難易度統計

「超頂点追加」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.7/2107
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2107
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「超頂点追加」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2291">No.2291 Union Find Estimate</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - C問題, difficulty: 1795)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2263">No.2263 Perms</a> (yukicoder contest 383 (2023-04-07) - E問題, difficulty: 2420)

　
<h2 id="最大・最小要素取得">122. 最大・最小要素取得</h2>

### 難易度統計

「最大・最小要素取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/1915
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1894
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「最大・最小要素取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)

　
<h2 id="クエリ先読み">123. クエリ先読み</h2>

### 難易度統計

「クエリ先読み」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/1930
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2489
- 2022年のコンテスト平均難易度/difficulty: 2.8/1743

### 難易度別問題一覧

「クエリ先読み」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2072">No.2072 Anatomy</a> (yukicoder contest 360 (2022-09-16) - C問題, difficulty: 1486)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

　
<h2 id="イベントソート">124. イベントソート</h2>

### 難易度統計

「イベントソート」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/1945
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1894
- 2022年のコンテスト平均難易度/difficulty: 3/2049

### 難易度別問題一覧

「イベントソート」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)

　
<h2 id="動的計画法">125. 動的計画法</h2>

### 難易度統計

「動的計画法」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/1978
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1647
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
- <a href="https://yukicoder.me/problems/no/2275">No.2275 →↑↓</a> (yukicoder contest 385 (2023-04-21) - A問題, difficulty: 831)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2071">No.2071 Shift and OR</a> (yukicoder contest 360 (2022-09-16) - B問題, difficulty: 1641)
- <a href="https://yukicoder.me/problems/no/2132">No.2132 1 or X Game</a> (yukicoder contest 369 (2022-11-25) - C問題, difficulty: 2191)
- <a href="https://yukicoder.me/problems/no/2147">No.2147 ハノイの塔のおもちゃ</a> (Advent Calendar Contest 2022 (2022-12-01) - D問題, difficulty: 2246)
- <a href="https://yukicoder.me/problems/no/2204">No.2204 Palindrome Splitting (No Rearrangement ver.)</a> (yukicoder contest 375 (2023-02-03) - D問題, difficulty: 1661)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)
- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)
- <a href="https://yukicoder.me/problems/no/2283">No.2283 Prohibit Three Consecutive</a> (yukicoder contest 386 (2023-04-28) - B問題, difficulty: 1628)
- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題, difficulty: 875)

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
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題, difficulty: 2153)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)
- <a href="https://yukicoder.me/problems/no/2069">No.2069 み世界数式</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2159">No.2159 Filling 4x4 array</a> (Advent Calendar Contest 2022 (2022-12-01) - J問題, difficulty: 3382)
- <a href="https://yukicoder.me/problems/no/2231">No.2231 Surprising Flash!</a> (yukicoder contest 378 (2023-02-24) - H問題, difficulty: 2690)

　
<h2 id="bitごとに計算">126. bitごとに計算</h2>

### 難易度統計

「bitごとに計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/1980
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.8/1771
- 2022年のコンテスト平均難易度/difficulty: 3/2328

### 難易度別問題一覧

「bitごとに計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2195">No.2195 AND Set</a> (yukicoder contest 374 (2023-01-20) - B問題, difficulty: 1093)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2060">No.2060 AND Sequence</a> (yukicoder contest 358 (2022-08-26) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2300">No.2300 Substring OR Sum</a> (yukicoder contest 388 (2023-05-12) - D問題, difficulty: 1257)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題, difficulty: 2295)
- <a href="https://yukicoder.me/problems/no/2212">No.2212 One XOR Matrix</a> (yukicoder contest 376 (2023-02-10) - E問題, difficulty: 1971)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題, difficulty: 2153)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2083">No.2083 OR Subset</a> (yukicoder contest 361 (2022-09-25) - F問題, difficulty: 2643)
- <a href="https://yukicoder.me/problems/no/2206">No.2206 Popcount Sum 2</a> (yukicoder contest 375 (2023-02-03) - F問題, difficulty: 2381)

　
<h2 id="緩和">127. 緩和</h2>

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

　
<h2 id="平面走査">128. 平面走査</h2>

### 難易度統計

「平面走査」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2019
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.8/1976
- 2022年のコンテスト平均難易度/difficulty: 3/2145

### 難易度別問題一覧

「平面走査」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題, difficulty: 2121)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)
- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題, difficulty: 2274)
- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題, difficulty: 2170)

　
<h2 id="一要素挿入">129. 一要素挿入</h2>

### 難易度統計

「一要素挿入」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2059
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.8/2092
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「一要素挿入」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2248">No.2248 max(C)-min(C)</a> (yukicoder contest 381 (2023-03-17) - C問題, difficulty: 1861)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

　
<h2 id="区間kth取得">130. 区間kth取得</h2>

### 難易度統計

「区間kth取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2069
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1851
- 2022年のコンテスト平均難易度/difficulty: 3/2178

### 難易度別問題一覧

「区間kth取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題, difficulty: 1851)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)

　
<h2 id="一対一対応">131. 一対一対応</h2>

### 難易度統計

「一対一対応」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2180
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2237
- 2022年のコンテスト平均難易度/difficulty: 2.7/2151

### 難易度別問題一覧

「一対一対応」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2058">No.2058 Binary String</a> (yukicoder contest 358 (2022-08-26) - C問題, difficulty: 2008)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題, difficulty: 2295)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

　
<h2 id="半分全列挙">132. 半分全列挙</h2>

### 難易度統計

「半分全列挙」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2181
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/1974
- 2022年のコンテスト平均難易度/difficulty: 3/2595

### 難易度別問題一覧

「半分全列挙」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2329">No.2329 Nafmo、イカサマをする</a> (MMA Contest 015  (2023-05-28) - H問題, difficulty: 1774)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)
- <a href="https://yukicoder.me/problems/no/2236">No.2236 Lights Out On Simple Graph</a> (yukicoder contest 379 (2023-03-03) - E問題, difficulty: 2175)

　
<h2 id="ゼータ変換">133. ゼータ変換</h2>

### 難易度統計

「ゼータ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2310
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2312
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「ゼータ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題, difficulty: 3018)

　
<h2 id="メビウス変換">134. メビウス変換</h2>

### 難易度統計

「メビウス変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.8/2310
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2312
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「メビウス変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2211">No.2211 Frequency Table of GCD</a> (yukicoder contest 376 (2023-02-10) - D問題, difficulty: 1607)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題, difficulty: 3018)

　
<h2 id="フェニック木">135. フェニック木</h2>

### 難易度統計

「フェニック木」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 2.9/2128
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2157
- 2022年のコンテスト平均難易度/difficulty: 3/2109

### 難易度別問題一覧

「フェニック木」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2080">No.2080 Simple Nim Query</a> (yukicoder contest 361 (2022-09-25) - C問題, difficulty: 1649)
- <a href="https://yukicoder.me/problems/no/2308">No.2308 [Cherry 5th Tune B] もしかして、真?</a> (yukicoder contest 389 (Until that day when "Cherry Month" is over.) (2023-05-19) - D問題, difficulty: 1851)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題, difficulty: 2121)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2077">No.2077 Get Minimum Algorithm</a> (yukicoder contest 360 (2022-09-16) - H問題, difficulty: 2707)

　
<h2 id="行列累乗">136. 行列累乗</h2>

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

　
<h2 id="ナップサックDP">137. ナップサックDP</h2>

### 難易度統計

「ナップサックDP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1469
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3.5/1782
- 2022年のコンテスト平均難易度/difficulty: 2/843

### 難易度別問題一覧

「ナップサックDP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2093">No.2093 Shio Ramen</a> (yukicoder contest 363 (2022-10-07) - B問題, difficulty: 843)

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2317">No.2317 Expression Menu</a> (yukicoder contest 390 (2023-05-26) - D問題, difficulty: 875)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2231">No.2231 Surprising Flash!</a> (yukicoder contest 378 (2023-02-24) - H問題, difficulty: 2690)

　
<h2 id="サイクルと非サイクルに分割">138. サイクルと非サイクルに分割</h2>

### 難易度統計

「サイクルと非サイクルに分割」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1499
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1499
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「サイクルと非サイクルに分割」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2301">No.2301 Namorientation</a> (yukicoder contest 388 (2023-05-12) - E問題, difficulty: 1499)

　
<h2 id="クエリソート">139. クエリソート</h2>

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

　
<h2 id="mex取得">140. mex取得</h2>

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

　
<h2 id="スライド最小化">141. スライド最小化</h2>

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

　
<h2 id="オイラー関数前計算">142. オイラー関数前計算</h2>

### 難易度統計

「オイラー関数前計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/1983
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1983
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「オイラー関数前計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2249">No.2249 GCDistance</a> (yukicoder contest 381 (2023-03-17) - D問題, difficulty: 1983)

　
<h2 id="ループ戦略">143. ループ戦略</h2>

### 難易度統計

「ループ戦略」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2043
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2043
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「ループ戦略」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2228">No.2228 Creeping Ghost</a> (yukicoder contest 378 (2023-02-24) - E問題, difficulty: 1933)
- <a href="https://yukicoder.me/problems/no/2278">No.2278 Time Bomb Game 2</a> (yukicoder contest 385 (2023-04-21) - D問題, difficulty: 2153)

　
<h2 id="ポラードの$\rho$">144. ポラードの$\rho$</h2>

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

　
<h2 id="平方剰余">145. 平方剰余</h2>

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

　
<h2 id="付値管理">146. 付値管理</h2>

### 難易度統計

「付値管理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2062
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2062
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「付値管理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★

- <a href="https://yukicoder.me/problems/no/2326">No.2326 Factorial to the Power of Factorial to the...</a> (MMA Contest 015  (2023-05-28) - E問題, difficulty: 1605)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題, difficulty: 2016)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題, difficulty: 2567)

　
<h2 id="区間最大・最小値取得">147. 区間最大・最小値取得</h2>

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

　
<h2 id="素因数分解">148. 素因数分解</h2>

### 難易度統計

「素因数分解」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2076
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3.1/1927
- 2022年のコンテスト平均難易度/difficulty: 2.7/2298

### 難易度別問題一覧

「素因数分解」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2125">No.2125 Inverse Sum</a> (yukicoder contest 368 (2022-11-18) - B問題, difficulty: 2291)
- <a href="https://yukicoder.me/problems/no/2218">No.2218 Multiple LIS</a> (yukicoder contest 377 (2023-02-17) - C問題, difficulty: 1200)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2183">No.2183 LCA on Rational Tree</a> (単発出題)
- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題, difficulty: 2016)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題, difficulty: 2567)

　
<h2 id="総和計算の期待値への帰着">149. 総和計算の期待値への帰着</h2>

### 難易度統計

「[総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2119
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.6/1971
- 2022年のコンテスト平均難易度/difficulty: 4/2566

### 難易度別問題一覧

「[総和計算の期待値への帰着](https://p-adic.github.io/yukicoder-difficulty-statistics-solution-name/#総和計算の期待値への帰着)」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2219">No.2219 Re:010</a> (yukicoder contest 377 (2023-02-17) - D問題, difficulty: 1622)
- <a href="https://yukicoder.me/problems/no/2327">No.2327 Inversion Sum</a> (MMA Contest 015  (2023-05-28) - F問題, difficulty: 2121)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題, difficulty: 2170)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
<h2 id="sorted set">150. sorted set</h2>

### 難易度統計

「sorted set」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2125
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2208
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「sorted set」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

　
<h2 id="一要素削除">151. 一要素削除</h2>

### 難易度統計

「一要素削除」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2125
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2208
- 2022年のコンテスト平均難易度/difficulty: 3/1959

### 難易度別問題一覧

「一要素削除」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2220">No.2220 Range Insert & Point Mex</a> (yukicoder contest 377 (2023-02-17) - E問題, difficulty: 1927)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

　
<h2 id="区間要素数取得">152. 区間要素数取得</h2>

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

　
<h2 id="外積">153. 外積</h2>

### 難易度統計

「外積」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2147
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2147
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「外積」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題, difficulty: 2147)

　
<h2 id="合成による次元削減">154. 合成による次元削減</h2>

### 難易度統計

「合成による次元削減」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2147
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2147
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「合成による次元削減」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2331">No.2331 Maximum Quadrilateral</a> (MMA Contest 015  (2023-05-28) - J問題, difficulty: 2147)

　
<h2 id="区間への分割の右端区間の左端を管理">155. 区間への分割の右端区間の左端を管理</h2>

### 難易度統計

「区間への分割の右端区間の左端を管理」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2153
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2153
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「区間への分割の右端区間の左端を管理」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題, difficulty: 2153)

　
<h2 id="区間の重複度計算">156. 区間の重複度計算</h2>

### 難易度統計

「区間の重複度計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2155
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.5/1661
- 2022年のコンテスト平均難易度/difficulty: 3.5/2649

### 難易度別問題一覧

「区間の重複度計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2197">No.2197 Same Dish</a> (yukicoder contest 374 (2023-01-20) - D問題, difficulty: 1661)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

　
<h2 id="素数列挙">157. 素数列挙</h2>

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

　
<h2 id="グリッド上の価値最大化">158. グリッド上の価値最大化</h2>

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

　
<h2 id="確率漸化式">159. 確率漸化式</h2>

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

　
<h2 id="再帰">160. 再帰</h2>

### 難易度統計

「再帰」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2180
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/1973
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
- <a href="https://yukicoder.me/problems/no/2318">No.2318 Phys Bone Maker</a> (yukicoder contest 390 (2023-05-26) - E問題, difficulty: 2016)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2067">No.2067 ±2^k operations</a> (yukicoder contest 359 (2022-09-02) - E問題, difficulty: 2737)

　
<h2 id="解法場合分け">161. 解法場合分け</h2>

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

　
<h2 id="データ構造初期化">162. データ構造初期化</h2>

### 難易度統計

「データ構造初期化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2237
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2237
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「データ構造初期化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題, difficulty: 2237)

　
<h2 id="一対一対応と乱択の可換性">163. 一対一対応と乱択の可換性</h2>

### 難易度統計

「一対一対応と乱択の可換性」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2237
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2237
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「一対一対応と乱択の可換性」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

　
<h2 id="素集合データ集合">164. 素集合データ集合</h2>

### 難易度統計

「素集合データ集合」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2237
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2237
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「素集合データ集合」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題, difficulty: 2237)

　
<h2 id="頂点倍化">165. 頂点倍化</h2>

### 難易度統計

「頂点倍化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2237
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2237
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「頂点倍化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2293">No.2293 無向辺 2-SAT</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - E問題, difficulty: 2237)

　
<h2 id="bitset高速化">166. bitset高速化</h2>

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

　
<h2 id="基底">167. 基底</h2>

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

　
<h2 id="座標圧縮">168. 座標圧縮</h2>

### 難易度統計

「座標圧縮」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2254
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2363
- 2022年のコンテスト平均難易度/difficulty: 3/2145

### 難易度別問題一覧

「座標圧縮」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2065">No.2065 Sum of Min</a> (yukicoder contest 359 (2022-09-02) - C問題, difficulty: 1696)
- <a href="https://yukicoder.me/problems/no/2161">No.2161 Black Market</a> (Advent Calendar Contest 2022 (2022-12-01) - L問題, difficulty: 2595)
- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)
- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

　
<h2 id="内積の畳み込み計算">169. 内積の畳み込み計算</h2>

### 難易度統計

「内積の畳み込み計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2258
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2258
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「内積の畳み込み計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題, difficulty: 2258)

　
<h2 id="ダブリング">170. ダブリング</h2>

### 難易度統計

「ダブリング」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2274
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2274
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「ダブリング」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2242">No.2242 Cities and Teleporters</a> (yukicoder contest 380 (2023-03-10) - D問題, difficulty: 2274)

　
<h2 id="線形代数">171. 線形代数</h2>

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

　
<h2 id="bitDP">172. bitDP</h2>

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

　
<h2 id="bit全探索">173. bit全探索</h2>

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

　
<h2 id="余因子展開">174. 余因子展開</h2>

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

　
<h2 id="剰余を商に翻訳">175. 剰余を商に翻訳</h2>

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

　
<h2 id="平方分割">176. 平方分割</h2>

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

　
<h2 id="フロー">177. フロー</h2>

### 難易度統計

「フロー」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2420
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2420
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「フロー」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2263">No.2263 Perms</a> (yukicoder contest 383 (2023-04-07) - E問題, difficulty: 2420)

　
<h2 id="完全二部マッチング">178. 完全二部マッチング</h2>

### 難易度統計

「完全二部マッチング」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2420
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2420
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「完全二部マッチング」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2263">No.2263 Perms</a> (yukicoder contest 383 (2023-04-07) - E問題, difficulty: 2420)

　
<h2 id="変数の対称性">179. 変数の対称性</h2>

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

　
<h2 id="単調関数の像計算">180. 単調関数の像計算</h2>

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

　
<h2 id="区間削除更新">181. 区間削除更新</h2>

### 難易度統計

「区間削除更新」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2489
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2489
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「区間削除更新」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

　
<h2 id="区間挿入更新">182. 区間挿入更新</h2>

### 難易度統計

「区間挿入更新」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2489
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2489
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「区間挿入更新」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2292">No.2292 Interval Union Find</a> (yukicoder contest 387 (Union Find Contest) (2023-05-05) - D問題, difficulty: 2489)

　
<h2 id="自己写像に翻訳">183. 自己写像に翻訳</h2>

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

　
<h2 id="準同型">184. 準同型</h2>

### 難易度統計

「準同型」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2656
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/3018
- 2022年のコンテスト平均難易度/difficulty: 3/2295

### 難易度別問題一覧

「準同型」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2123">No.2123 Chalk Breaker</a> (単発出題)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2061">No.2061 XOR Sort</a> (yukicoder contest 358 (2022-08-26) - F問題, difficulty: 2295)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題, difficulty: 3018)

　
<h2 id="約数メビウス変換">185. 約数メビウス変換</h2>

### 難易度統計

「約数メビウス変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/2662
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/3018
- 2022年のコンテスト平均難易度/difficulty: 3/2306

### 難易度別問題一覧

「約数メビウス変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題, difficulty: 3018)

　
<h2 id="指定序数の値の計算を各値未満の数え上げに帰着">186. 指定序数の値の計算を各値未満の数え上げに帰着</h2>

### 難易度統計

「指定序数の値の計算を各値未満の数え上げに帰着」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/3018
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/3018
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「指定序数の値の計算を各値未満の数え上げに帰着」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題, difficulty: 3018)

　
<h2 id="約数ゼータ変換">187. 約数ゼータ変換</h2>

### 難易度統計

「約数ゼータ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3/3018
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/3018
- 2022年のコンテスト平均難易度/difficulty: データなし

### 難易度別問題一覧

「約数ゼータ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2262">No.2262 Fractions</a> (yukicoder contest 383 (2023-04-07) - D問題, difficulty: 3018)

　
<h2 id="区間和取得">188. 区間和取得</h2>

### 難易度統計

「区間和取得」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/1980
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2153
- 2022年のコンテスト平均難易度/difficulty: 3.2/1893

### 難易度別問題一覧

「区間和取得」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2101">No.2101 [Cherry Alpha N] ずっとこの数列だったらいいのに</a> (yukicoder contest 364 (Do you know Cherry Contest?) (2022-10-14) - E問題, difficulty: 2049)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題, difficulty: 2153)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

　
<h2 id="期待値の線形性">189. 期待値の線形性</h2>

### 難易度統計

「期待値の線形性」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2219
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 2.7/2046
- 2022年のコンテスト平均難易度/difficulty: 4/2566

### 難易度別問題一覧

「期待値の線形性」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★☆

- <a href="https://yukicoder.me/problems/no/2235">No.2235 Line Up Colored Balls</a> (yukicoder contest 379 (2023-03-03) - D問題, difficulty: 1922)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2250">No.2250 Split Permutation</a> (yukicoder contest 381 (2023-03-17) - E問題, difficulty: 2170)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2068">No.2068 Restricted Permutation</a> (yukicoder contest 359 (2022-09-02) - F問題, difficulty: 2566)

　
<h2 id="区間加算更新">190. 区間加算更新</h2>

### 難易度統計

「区間加算更新」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.1/2244
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2237
- 2022年のコンテスト平均難易度/difficulty: 3.1/2247

### 難易度別問題一覧

「区間加算更新」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★☆

- <a href="https://yukicoder.me/problems/no/2154">No.2154 あさかつの参加人数</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - B問題, difficulty: 711)

##### ★★★

- <a href="https://yukicoder.me/problems/no/2336">No.2336 Do you like typical problems?</a> (yukicoder contest 391 (2023-06-02) - C問題, difficulty: 2237)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2133">No.2133 Take it easy!</a> (yukicoder contest 369 (2022-11-25) - D問題, difficulty: 2649)

##### ★★★★☆

- <a href="https://yukicoder.me/problems/no/2163">No.2163 LCA Sum Query</a> (Advent Calendar Contest 2022 (2022-12-01) - N問題, difficulty: 3382)

　
<h2 id="ユークリッドの互除法">191. ユークリッドの互除法</h2>

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

　
<h2 id="最大公約数">192. 最大公約数</h2>

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

　
<h2 id="互いに素に帰着">193. 互いに素に帰着</h2>

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

　
<h2 id="DPのデータ構造高速化">194. DPのデータ構造高速化</h2>

### 難易度統計

「DPのデータ構造高速化」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.2/2283
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2161
- 2022年のコンテスト平均難易度/difficulty: 3.3/2332

### 難易度別問題一覧

「DPのデータ構造高速化」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2075">No.2075 GCD Subsequence</a> (yukicoder contest 360 (2022-09-16) - F問題, difficulty: 2306)
- <a href="https://yukicoder.me/problems/no/2139">No.2139 K Consecutive Sushi</a> (Advent Calendar Contest 2022 (2022-12-01) - C問題, difficulty: 1959)
- <a href="https://yukicoder.me/problems/no/2171">No.2171 OR Assignment</a> (Advent Calendar Contest 2022 (2022-12-01) - X問題, difficulty: 2758)
- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)
- <a href="https://yukicoder.me/problems/no/2279">No.2279 OR Insertion</a> (yukicoder contest 385 (2023-04-21) - E問題, difficulty: 2153)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2157">No.2157 崖</a> (yukicoder contest 371 (Asakatsu Presents) (2022-12-09) - E問題, difficulty: 1738)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
<h2 id="調和数列">195. 調和数列</h2>

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

　
<h2 id="ベン図">196. ベン図</h2>

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

　
<h2 id="十分大きな法で計算">197. 十分大きな法で計算</h2>

### 難易度統計

「十分大きな法で計算」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.3/2290
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3.5/2412
- 2022年のコンテスト平均難易度/difficulty: 3/2047

### 難易度別問題一覧

「十分大きな法で計算」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2074">No.2074 Product is Square ?</a> (yukicoder contest 360 (2022-09-16) - E問題, difficulty: 2047)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題, difficulty: 2258)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2207">No.2207 pCr検査</a> (yukicoder contest 375 (2023-02-03) - G問題, difficulty: 2567)

　
<h2 id="B進法">198. B進法</h2>

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

　
<h2 id="小さいケースの構築を拡張">199. 小さいケースの構築を拡張</h2>

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

　
<h2 id="剰余による確率的判定">200. 剰余による確率的判定</h2>

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

　
<h2 id="最小素因数前計算">201. 最小素因数前計算</h2>

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

　
<h2 id="２進法">202. ２進法</h2>

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

　
<h2 id="交代和">203. 交代和</h2>

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

　
<h2 id="inplace DP">204. inplace DP</h2>

### 難易度統計

「inplace DP」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2536
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2169
- 2022年のコンテスト平均難易度/difficulty: 4/2903

### 難易度別問題一覧

「inplace DP」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2230">No.2230 Good Omen of White Lotus</a> (yukicoder contest 378 (2023-02-24) - G問題, difficulty: 2169)

##### ★★★★

- <a href="https://yukicoder.me/problems/no/2162">No.2162 Copy and Paste 2</a> (Advent Calendar Contest 2022 (2022-12-01) - M問題, difficulty: 2903)

　
<h2 id="第二種スターリング数">205. 第二種スターリング数</h2>

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

　
<h2 id="floor sum">206. floor sum</h2>

### 難易度統計

「floor sum」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.5/2648
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: データなし
- 2022年のコンテスト平均難易度/difficulty: 3.5/2648

### 難易度別問題一覧

「floor sum」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2066">No.2066 Simple Math !</a> (yukicoder contest 359 (2022-09-02) - D問題, difficulty: 2648)

　
<h2 id="フロベニウスの硬貨交換問題">207. フロベニウスの硬貨交換問題</h2>

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

　
<h2 id="像決め打ち二分探索">208. 像決め打ち二分探索</h2>

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

　
<h2 id="カタラン数">209. カタラン数</h2>

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

　
<h2 id="01BFS">210. 01BFS</h2>

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

　
<h2 id="ローリングハッシュ">211. ローリングハッシュ</h2>

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

　
<h2 id="最長共通接頭辞">212. 最長共通接頭辞</h2>

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

　
<h2 id="桁DP">213. 桁DP</h2>

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

　
<h2 id="高速フーリエ変換">214. 高速フーリエ変換</h2>

### 難易度統計

「高速フーリエ変換」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.6/2765
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2258
- 2022年のコンテスト平均難易度/difficulty: 3.8/2934

### 難易度別問題一覧

「高速フーリエ変換」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題, difficulty: 2673)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題, difficulty: 2258)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="畳み込み">215. 畳み込み</h2>

### 難易度統計

「畳み込み」を主たる解法に含む問題の難易度統計です。
- コンテスト平均難易度/difficulty: 3.6/2765
- 2024年のコンテスト平均難易度/difficulty: データなし
- 2023年のコンテスト平均難易度/difficulty: 3/2258
- 2022年のコンテスト平均難易度/difficulty: 3.8/2934

### 難易度別問題一覧

「畳み込み」を主たる解法に含む問題の難易度ごとの一覧です。

##### ★★★

- <a href="https://yukicoder.me/problems/no/2164">No.2164 Equal Balls</a> (Advent Calendar Contest 2022 (2022-12-01) - O問題, difficulty: 2673)
- <a href="https://yukicoder.me/problems/no/2330">No.2330 Eat Slime</a> (MMA Contest 015  (2023-05-28) - I問題, difficulty: 2258)

##### ★★★☆

- <a href="https://yukicoder.me/problems/no/2062">No.2062 Sum of Subset mod 999630629</a> (yukicoder contest 358 (2022-08-26) - G問題, difficulty: 2553)

##### ★★★★★

- <a href="https://yukicoder.me/problems/no/2166">No.2166 Paint and Fill</a> (Advent Calendar Contest 2022 (2022-12-01) - S問題, difficulty: 3577)

　
<h2 id="同値関係">216. 同値関係</h2>

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

　
<h2 id="キュー">217. キュー</h2>

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

　
<h2 id="マージ">218. マージ</h2>

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

　
<h2 id="区間を中間で分割してマージ">219. 区間を中間で分割してマージ</h2>

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

　
<h2 id="区間最大・最小値更新">220. 区間最大・最小値更新</h2>

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

　
<h2 id="分割統治畳み込み">221. 分割統治畳み込み</h2>

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

　
<h2 id="遅延セグメント木">222. 遅延セグメント木</h2>

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

　
<h2 id="バケット分割">223. バケット分割</h2>

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

　
<h2 id="区間二次形式取得">224. 区間二次形式取得</h2>

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

　
<h2 id="区間二次式取得">225. 区間二次式取得</h2>

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

　
<h2 id="最近共通祖先">226. 最近共通祖先</h2>

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

　
<h2 id="重軽分解">227. 重軽分解</h2>

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

　
<h2 id="フック長公式">228. フック長公式</h2>

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

　
<h2 id="ヤング図形">229. ヤング図形</h2>

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

　
<h2 id="トポロジカルソート">230. トポロジカルソート</h2>

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

　
<h2 id="強連結成分分解">231. 強連結成分分解</h2>

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

　
<h2 id="残余ネットワーク">232. 残余ネットワーク</h2>

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

　
<h2 id="P-再帰">233. P-再帰</h2>

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

　
<h2 id="多点評価">234. 多点評価</h2>

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

　
<h2 id="評価点シフト">235. 評価点シフト</h2>

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

　
<h2 id="アルゴリズム中に追加処理">236. アルゴリズム中に追加処理</h2>

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

　
<h2 id="ハミルトン路">237. ハミルトン路</h2>

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

　
<h2 id="構文解析">238. 構文解析</h2>

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

