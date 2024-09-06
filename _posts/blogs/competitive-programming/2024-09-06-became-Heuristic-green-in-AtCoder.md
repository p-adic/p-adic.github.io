---
layout: blog
title: AtCoder Heuristic Contest 入緑色記事
date: 2024-09-05
excerpt: "AHCで緑色になった記念の記事です。"
parent: competitive-programming-blog/
prev-child: competitive-programming-problem-solving/
next-child: 
blog: true
image-directory: competitive-programming
tags: [競技プログラミング,数学]
---

## 自己紹介

恐らく多くの人は初めましてだと思いますので簡単な自己紹介から。

$p$進大好きサークルの$p$進大好きbot（以下、筆者）です。絵や漫画を描いたりゲームを作ったりする活動などをしています。

競技プログラミングの勉強をしている目的は、もちろん単純に面白い問題を楽しむために加えて

1. 数学が好きなので、数学をする際にプログラミングで補助できるようになるため。
1. 作問が好きなので、作問をする際に適正な難易度および慣習的な言葉遣い・問題設定を学ぶため。

の$2$つです。特に2のために、上級者じゃなくても気軽に作問できるyukicoderで主に活動しています。競技プログラミング界隈そのものの特色なのかもしれませんがyukicoderには下級者に優しい方々がいっぱいいらっしゃって、いつも懇切丁寧に助けていただいております。

時間と体力的にyukicoderだけで手一杯な身ですが、長期コンならば参加しやすいのでAtCoderで長期コンがあればいつか参加したいと思っていたところにちょうど[RECRUIT 日本橋ハーフマラソン 2024夏（AtCoder HeuristicContest 036）](https://atcoder.jp/contests/ahc036)が開催されることを知って参加させていただき（[参加記]({{ site.url }}/AHC036)）、晴れて緑色になることができました。色が変わったら記事を書くのがAtCoderユーザーの文化のようです。

ただ参加記を見ていただければ分かるように正直今回緑色になれたのはただの幸運な（スコアの推定できていない色々な乱択を試していたらたまたまいい感じのスコアが出る乱択が見つかった）だけなので色変記事を書くのにやや後ろめたさがありますが、今回が最初で最後の執筆機会かもしれないと思って書かせていただきました。


## 競技プログラマーとしてのプロフィール

AtCoderのレートはAlgorithmが$21$で灰色、Heuristicが$877$で緑色です。

- [AtCoderのユーザーページ](https://atcoder.jp/users/padic)

yukicoderにはレーティングシステムの代わりにサイトへの貢献度的なものを表すゆるふわポイントというシステムがあり、それは$24640$で$5$位です。一方でコンテストの成績は、全体の真ん中よりちょっと下くらいだと思います。

現時点での作問数は公開済みが$63$問、公開予定も合わせると$128$問です。tester経験数は公開済みが$94$（$88+0+1+5$）問、公開予定も合わせると$117$（$110+1+1+5$）問です。ゆるふわポイントは主に作問とtesterで稼いでいます。

- [yukicoderのユーザーページ](https://yukicoder.me/users/5376)

使用言語はC++とcLayとPythonで、yukicoderの★2以上をC++、★1.5以下をcLayかPythonで解くことが多いです。ライブラリーは主にC++で作っていますが、作問のために少しずつPythonも増やしています。


## 好きなアルゴリズム

人から伝授していただいたアルゴリズムには愛着が湧きます。okkuuさんから教わった[BIT](https://github.com/p-adic/cpp/tree/master/Mathematics/SetTheory/DirectProduct/AffineSpace/BIT)と、えこってさんやチルノさんから教わった[平方分割](https://github.com/p-adic/cpp/tree/master/Mathematics/SetTheory/DirectProduct/AffineSpace/SqrtDecomposition)を、これでもかというほどに使い倒しています。

hotmanさんやNyaanさんやTKOさんや（多すぎて全員挙げられない）から教わった[多項式・形式冪級数周りのアルゴリズム](https://github.com/p-adic/cpp/tree/master/Mathematics/Polynomial)も深い思い入れがありますが、残念ながら★3以下で使う機会がほとんどないので全然応用力を培えていません。

<details>
<summary>
※ちなみに思い入れがあるのは以下の問題での苦戦からです。（ネタバレ防止用にクリックで開く）
</summary>
<ul>
<li><a href="https://yukicoder.me/problems/no/2062">Sum of Subset mod 999630629</a>（初めての高速フーリエ変換実装）</li>
<li><a href="https://yukicoder.me/problems/no/2166">Paint and Fill</a>（解説を読んで理解してからも更に$1$ヶ月のデバッグ）</li>
</ul>
</details>

また代入を体現したようなアルゴリズムである[UnionFind](https://github.com/p-adic/cpp/tree/master/Mathematics/Geometry/Graph/Algorithm/UnionFindForest)と、単射を抽象化したような問題設定である[最大二部マッチングの求解アルゴリズム](https://github.com/p-adic/cpp/tree/master/Mathematics/Geometry/Graph/Algorithm/HopcroftKarp)は、代入や単射の数学における重要性から一目置いています。

あと競技プログラミングとは違う文脈で知っていた[マーラー変換](https://github.com/p-adic/cpp/tree/master/Mathematics/Combinatorial/ZetaTransform/MahlerTransform)や[順序数表記](https://googology.fandom.com/wiki/User_blog:P%E9%80%B2%E5%A4%A7%E5%A5%BD%E3%81%8Dbot/Relation_between_an_OCF_and_an_Ordinal_Notation#Ordinal_Notation)も好きなのですが、競技プログラミングでの出題頻度は低いので自分で作問しています。

他にも[グレブナー基底](https://github.com/p-adic/cpp/tree/master/Mathematics/Polynomial/GroebnerBasis)の同人誌やゲームを制作しています。グレブナー基底大好きbotさんの書籍「[妹がグレブナー基底に興味を持ち始めたのだが。](https://shosen.tokyo/?pid=171797363)」のシリーズのどこかにも何箇所か絵を載せていただいているのでぜひ探してみてください。


## 苦手なアルゴリズム

BITに親しみを覚えすぎているので、[累積和](https://github.com/p-adic/cpp/tree/master/Mathematics/SetTheory/DirectProduct/AffineSpace/CumulativeProduct)と[imos法](https://github.com/p-adic/cpp/tree/master/Mathematics/SetTheory/DirectProduct/AffineSpace/DifferenceSequence)のことをよく考察から漏らします。あと[再帰](https://github.com/p-adic/cpp/tree/master/Mathematics/Function/Recursion)はyukicoderでの出題頻度が低いのでよく失念しています。[イベントソート](https://github.com/p-adic/cpp/tree/master/Mathematics/SetTheory/DirectProduct/AffineSpace/BIT/TimeSeriesSetMax)には強い苦手意識があり、考察できても実装で失敗することが多いです。

なお好きなアルゴリズムで挙げた[多項式・形式冪級数周りのアルゴリズム](https://github.com/p-adic/cpp/tree/master/Mathematics/Polynomial)も、その苦い思い出の数々から同時に苦手意識を持っています。特に[多点評価](https://github.com/p-adic/cpp/tree/master/Mathematics/Polynomial/MultipointEvaluation)と[評価点シフト](https://github.com/p-adic/cpp/tree/master/Mathematics/Polynomial/IntervalEvaluation)。$1$ヶ月もデバッグしてました……。


## 競技プログラミングを始めたきっかけ

まずAtCoderというものがあることを$2018$年に知り、どういう問題を扱う競技なのか気になって[practice contest](https://atcoder.jp/contests/practice)というものに挑戦してみました。

当時はプログラミングも全然分かっておらず、B問題のInteractive Sortingが半日以上掛けても正解できず、答えを調べてやっとACとなった経験があります。A問題がWelcome to AtCoderといういかにも一番簡単そうな名前だったので$2$番目に簡単な問題がこのレベルなんだろうなと思い、筆者には到底無理な競技だと悟ったのが良い思い出です。

とはいえすぐに諦めるのはよくないと思い、その後も[AtCoder Beginners Selection](https://atcoder.jp/contests/abs)を練習してみた上で、頃合いを見て[AtCoder Beginner Contest 103](https://atcoder.jp/contests/abc103)にも挑戦してみましたが結果はABの$2$完でした。

コンテスト中、ABを解き終わってからは何も分からない空虚な時間が過ぎていき、夜に考えごとをするのが苦手で起きているのすらやっとだったので当時の経験はかなり辛いものでした。初心者向けのコンテストでこんな状況ではさすがに向いていないかなと思い、ここで競技プログラミングのことは忘れてしまいました。

$4$年後の$2022$年、知り合いのokkuuさんがyukicoderで作問をなさったけれどまだあまり解かれていらっしゃらないという話を聞き、久しぶりに競技プログラミングの問題に挑戦してみようと思いました。思い出深い[K色問題](https://yukicoder.me/problems/no/1815)です。

<details>
<summary>
自力で解くことを目標に、$1$ヶ月近くかけてようやくACを取れた時の爽快感は今でも忘れません。（ネタバレあり。クリックで開く）
</summary>
当時は競技プログラミングの知識が全くありませんでしたが、たまたま問題が繰り返し二乗法と行列累乗以外の高度な知識を要求しない定数倍高速化を問うものだったこと、繰り返し二乗法と行列累乗は数学の文脈で最初から知っていたこと、がとても幸運でした。運が悪ければ手も足も出ずまた競技プログラミングを諦めるところでした。
</details>

結果的に解けたおかげで大きな励みになり、これが競技プログラミングを始めたきっかけとなりました。

## 競技プログラミングの勉強

そこからはきちんと競技プログラミングの勉強をしようと思い、yukicoderで★1の通常問題を埋め、★1.5と★2をいくつか挑戦し、yukicoderのコンテストに出るようになりました。初めて参加したのは[yukicoder contest 358](https://yukicoder.me/contests/399)で、何故かA（★2）B（★2）C（★2.5）の3完できてしまいびっくりしました。いわゆるbeginner's luckで、後述するように★2.5は今でも苦戦する難易度です。

その成功体験をバネに、★2の練習を続けました。★2で解けずに解説を読んだ問題は自力で実装するようにしていたのですが、その際には解説に現れないswapが何故かよく出てきたので「★2で分からなければswap！」と意識して解くようにしたら★2の正答率がぐんぐん上がっていきました。今年に入って初めて知ったのですが、★2の解法のswapを使った実装は[Next DP](https://qiita.com/H20/items/922cc0a17ba5817f26d7)と呼ぶらしいです。

そしてすぐに★2.5の壁にぶつかりました。それから$2$年、今に至ります。★2.5が難しすぎて、たいていコンテスト時間中に解き終わりません。初参加だったyukicoder contest 358以降の全ての通常コンテストで★3以下をupsolveするようにして、苦手な実装を克服するために★3以下の典型アルゴリズムを勉強して自力で一から[ライブラリー](https://p-adic.github.io/cpp/)化して、実装が軽くなるように[tailsさんのコード](https://yukicoder.me/users/385/submissions)を研究して、苦手な考察を克服するために★3以下の典型考察も自動で提供してくれる[ライブラリー](https://github.com/p-adic/cpp/tree/master/Contest/AutoCheck/LibrarySearch)を構築して、考察失敗しやすい数え上げ問題などでサンプルや愚直解から正答を推定するための[サンプル解析器](https://github.com/p-adic/cpp/tree/master/Contest/AutoCheck/SampleAnalyser)を作成して、夜に$20$分以上連続して考えると高確率で寝落ちしてしまうことを克服するために★2.5を最初に解くようにしても、いまだに★2.5の壁を乗り越えられていません。

yukicoderの問題の難易度はwriterさんが自由につけるのですが、多くはyukicoderの過去問の解かれ具合と照らし合わせての難易度設定だと思います。恐らくyukicoderの現状は新規参入者の流入より競技プログラマーの平均的成長の寄与が大きく、絶対的に同難易度な問題の解かれやすさが上がっていく傾向にあるようです。そのため、★2.5に割り振られる問題の難易度が時々刻々と上昇していき、その上昇率に追いついて行けていないのが筆者の現状だと考えています。何故なら、考察系でない古い★2.5は比較的解けようになってきたからです。

また考察系の★2.5は古い過去問であってもなかなか解けません。★2.5の考察の練習にはAtCoderの水色の考察問を解くことをhiro1729さんにおすすめしていただいたのでそれもたまに挑戦していますが、なかなか解けるようになりません。実装と考察の両方が苦手なのが致命的です。まさに苦手の二刀流。

たまに「数学が得意ならば競技プログラミングに向いている」という言説を聞きますが、どうやらその反例が筆者のようです（数学が得意であることに疑義がありましたらすみません）。強い競技プログラマーを見てると数学に長けている人が多い一方で、逆は必ずしも成り立たないようです。というか強い競技プログラマーは数学に限らず色々なことに長けているように見えるのでひたすら脱帽です。学科選択や大学院進学の話題になるたび、「え？　数学専攻じゃないの？」という驚きと寂しさ（数学を専攻してほしかったなぁ）を覚えます。SSRSさんとか。

一応★2までの練習はしやすく感じたので、そこに数学の恩恵があるかもしれません。また作問に慣れている人の解説は★4でも読解しやすく感じるので、そこにも数学の恩恵がありそうです。でも★2.5を解けるようにはならないんですよねぇ。単に練習量が相対的に足りていなさそうで、数学が得意であるだけでは練習量の不足を補えなさそうです。競技プログラマーの練習量がすごい！　更に時間を捻出する方法を考えるか、練習内の非効率部分を探して削っていくか、どうにかする必要があります。

そんなこんなで、競技プログラミングを始めてからずっと★2.5の壁に悩まされ続けている現状です。いつか乗り越えられると良いな。こんな成長の乏しい筆者でも師事させていただける競技プログラマーを募集中です。


## 競技プログラミングの作問

冒頭に述べたように、競技プログラミングの勉強をしている最も大きな目的の１つが作問です。yukicoderは初心者から作問をすることができるので筆者にぴったりで、ちょくちょくコンテストを開かせていただいております。はちじさんみたいに面白い問題が作れるようになることを目指しています。

また作問は１問１問時間をかけて行います。普段のupsolveや復習より遥かに長い時間１つの問題に向き合うため、それらとはまた違った恩恵があることを期待しています。作問をして解法の正当性を確認する際は各種アルゴリズムの理解を深められますし、testerさんに様々なフィードバックをもらう過程で知らなかった知識やテクニックを次々と身につけることができます。

筆者の主観的体感としては現状、作問によって得られている成長が筆者の上達の中で一番大きな割合を占めていると思っています。しかし競技プログラミングを始めてから現在に至るまでずっと★2.5の壁に悩まされ続けているので、客観的には成長が$0$だと思います。$0$の中で割合を語っても見向きもされないと思いますので、何らかの方法で現状を改善して★2.5の壁を破ってきちんと成長を客観的に示し、作問が勉強の役に立つということを胸を張って主張できる日が来るように頑張ります。


## 終わりに

またいつか長期コンに参加するかもしれません。今回は繁忙期だったのでくたくたになってしまったので、次回は時間に余裕のあるタイミングでの参加を目指します。その際はよろしくお願いいたします。

以上です。お読みいただきありがとうございました。
