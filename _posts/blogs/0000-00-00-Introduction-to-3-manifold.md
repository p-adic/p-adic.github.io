---
layout: blog
title: 「３次元多様体入門」を読む
date: 2020-07-23
excerpt: "「３次元多様体入門」を読み進めながら雑感を書いていきます。"
blog: true
tags: [数学]
---

[p進大好きbot](https://twitter.com/non_archimedean)が森元勘治先生著の「３次元多様体入門」（電子版）を読み進めながら雑感を書いていきます。この記事が書籍への間接的フィードバックおよび同書籍を勉強する方の参考になれば幸いです。特に誤植や曖昧なところをどう推測したかも記録しましたので、知らない分野の教科書を読む際にどのように誤植や曖昧なところを埋めていくかの参考にして下さい。

一般論として誤植や曖昧なところをどう修正していくかは初学者が一人で考えてもしょうがないので、人に聞いたり他の文献を当たったり、複数の可能性を保持しておいて後の記述と照らし合わせて特定していくことが多いと思います。ただし人に聞いたり他の文献を当たったりした場合も、用語の流儀が文脈によって違いうる場合には注意が必要です。それを初学者が推測することは困難ですので、人から聞いたり他の文献を当たったりした場合でも過信せず、基本的には後の記述と照らし合わせておかしいなと思ったら別の可能性も探っていきましょう。

なおこの書籍は[著者のページ](http://tunnel-knot.sakura.ne.jp/3-manifolds.html)にて一般公開されているもので、今回読み進めているのは2020年7月22日にダウンロードさせていただいた版です。[p進大好きbot](https://twitter.com/non_archimedean)は３次元多様体論についてほとんど知りませんが、予備知識なく読めるものとしてお勧めしていただきました。そのため証明が省略されている部分や明らか誤植がある部分は他の文献に当たるのではなくなるべくこの書籍だけを参考にして考えていこうと思いますが、それでも分からないところは飛ばし、どこを飛ばしたかをここに明確に残すことでうっかり循環論法等に陥らないように気を付けます。今のところとても丁寧に書かれていて読み心地の良い書籍だと思います。


## p. vii

{% assign i = 0 %}
### {{i}}：コメント
この書籍では自然数に$$0$$を含めず、$$\mathbb{N}$$を正整数全体の集合としています。そのためこの記事では非負整数全体を表す記号として$$\omega$$を採用します。


## p. 1

{% assign i = i | plus: 1 %}
### {{i}}：コメント
「いくつかの基本命題は証明を省略するので参考文献を参照する」という旨の指示がありましたが、上述した通りここはなるべく考えていこうと思います。

{% assign i = i | plus: 1 %}
### {{i}}：曖昧
「全ての図形はユークリッド空間に含まれる」という旨の注意書きがありましたが、「図形」が「空間的な構造を持つ集合」（例えば写像とかは該当しない）をざっくり表すことは良いとして、例えばユークリッド空間やカントール集合なども図形として扱われているのかどうかが曖昧です。また図形を含むという「ユークリッド空間」が、図形によらない１つの有限次元ユークリッド空間を指すのか、図形ごとに異なってもいいユークリッド空間を指すのか曖昧です。曖昧さを解消するためにいくつかの可能性を検討します。

まずユークリッド空間を図形とみなすとします。この場合、この直後に一般の非負整数$$n$$に対し$$n$$次元ユークリッド空間を考えており、全ての$$n$$次元ユークリッド空間を含むユークリッド空間は存在しないことから、図形を含むとされるユークリッド空間は図形ごとに異なってもよいということになります。

次にユークリッド空間を図形とみなさないとします。この場合も、一般の非負整数$$n$$と$$k$$であって$$k+1 \leq n$$を満たすものに対し$$k$$次元単体を$$\mathbb{R}^n$$の部分集合として考えています。直前に単体と図形の関連が示唆されていることから、単体は図形であると推測します。一方で、全ての$$k$$次元単体を含むユークリッド空間は存在しないことから、この場合もやはり図形を含むとされるユークリッド空間は図形ごとに異なってもよいということになります。

以上より、いずれにしても図形を含むとされるユークリッド空間は図形ごとに異なってもよいことが推測されました。ただしユークリッド空間やカントール集合が図形とみなされているかどうかはこの時点では推測できていないので、両方の可能性を保持して読み進めていきます。


## p. 2

{% assign i = i | plus: 1 %}
### {{i}}：誤植
単体の「内部」という概念が定義されました。しかし$$k$$次元単体の内部の定義に、$$k-1$$次元単体という概念が出てきます。$$k > 0$$の時は何の問題もありませんが、$$k = 0$$の時に$$-1$$次元単体という未定義な概念が参照されてしまうため、$$0$$次元単体の内部はill-definedとなります。

修正方法を検討します。まず思いつくのは「$$k > 0$$という条件を課し忘れた」という可能性ですが、p. 5で導入される開星状体という概念の定義は次元に制約のない単体の内部を参照しているため、この推測は誤りとなります。となると$$0$$次元単体の内部を別個に定義する必要がありますが、内部ということは恐らく元の単体の多面体の部分集合、つまり空集合またはその単体の多面体そのものであることが推測できます。両方の可能性を保持して読み進めていきましょう。

なお後述するように、命題1.3を踏まえると$$0$$次元単体の内部は空集合ではないことが推測されるので、恐らく$$0$$次元単体の内部はその単体の多面体そのものであると推測します。

{% assign i = i | plus: 1 %}
### {{i}}：誤植
「単体的複体」という概念が定義されました。単体的複体の定義の条件(2)に現れる「$$\sigma \cap \tau \neq$$」は「$$\sigma \cap \tau \neq \emptyset$$」の誤植だと推測されます。

この修正を踏まえて、この本の流儀における単体的複体の定義を要約します。単体の集合$$K$$が単体的複体であるとは、以下の$$3$$条件を満たすもののことです：

(1) 任意の$$\sigma \in K$$と$$\tau \subset \sigma$$に対し、$$\tau$$が$$\sigma$$の面であるならば$$\tau \in K$$である。

(2) 任意の$$\tau_1, \tau_2 \in K$$に対し、$$\tau_1 \cap \tau_2 \neq \emptyset$$であるならば、$$\tau_1 \cap \tau_2$$は$$\tau_1$$と$$\tau_2$$の面である。

(3) 任意の$$\sigma \in K$$に対し、$$\{\tau \in K \mid \sigma \cap \tau \neq \emptyset\}$$は有限集合である。

単体的複体の絵が描いてあるだけで具体例は与えられていませんが、例えばカントール集合$$C \subset \mathbb{R}$$を用いて$$K_C := \{U \in \mathcal{P}(C) \mid \exists x \in C, U = \{x\}\}$$と表される集合は$$0$$単体のみからなる単体的複体ですね。この例を念頭に置いて読み進めていきます。

{% assign i = i | plus: 1 %}
### {{i}}：曖昧
単体的複体$$K$$に対しその幾何的実現のような「多面体」$$\lvert K \rvert$$という概念が定義されました。例えば$$K_C$$の多面体$$\lvert K_C \rvert$$はカントール集合$$C$$の下部集合と一致します。

しかし$$\mathbb{R}^n$$を$$\mathbb{R}^{n+1}$$の部分空間とみなしている流儀なのかどうかがはっきり明言されていないことに注意します。またこの時点で多面体を図形とみなしているかどうかが不明確であるため、多面体がユークリッド空間に含まれるかどうかは両方の可能性を保持していきます。

$$\mathbb{R}^n$$を$$\mathbb{R}^{n+1}$$の部分空間とみなす流儀の場合、例えば$$n$$次元標準単体の面全体のなす単体的複体を$$K_n$$と置くと$$\bigcup_{n \in \omega} K_n$$もまた単体的複体となります。この単体的複体は包含関係に関するグラフ構造が連結であり、かつ１つの有限次元ユークリッド空間の単体の集合にはなりません。特にその多面体は１つの有限次元ユークリッド空間に含まれないことから、多面体は図形でないということが推測されます。

一方で$$\mathbb{R}^n$$を$$\mathbb{R}^{n+1}$$の部分空間とみなさない流儀の場合、共通部分が空でない単体同士は必ず同じ次元のユークリッド空間に属すことになるため、包含関係に関するグラフ構造が連結である単体的複体は１つの有限次元ユークリッド空間の単体の集合となります。従ってどちらの流儀を採用しているかによって、単体的複体という概念の定義が変わります。

なお後述するように、p. 5の単体写像の定義を踏まえると単体的複体が１つの有限次元ユークリッド空間の単体の集合であることが推測されるので、$$\mathbb{R}^n$$を$$\mathbb{R}^{n+1}$$の部分空間とみなしていると推測します。

更に後述するように、p. 6で実は単体的複体にはその多面体が１つの有限次元ユークリッド空間内にあることが暗黙に仮定されているということが明かされます。これにより、$$\mathbb{R}^n$$を$$\mathbb{R}^{n+1}$$の部分空間とみなしているかどうかはあまり重要ではなくなります。

{% assign i = i | plus: 1 %}
### {{i}}：誤植？
単体的複体の「次元」という概念が定義されました。単体の次元の$$\max$$が存在する場合は$$\max$$、存在しない場合は$$\infty$$と定義されています。直感的には$$\max$$より非負整数全体における$$\sup$$の方が次元っぽいと思うのですが、何か意図があるのかもしれません。例えば$$\emptyset$$は単体的複体となりますが、$$\max$$の流儀だと$$\infty$$次元、非負整数全体における$$\sup$$の流儀だと$$0$$次元となります。


## p. 3

{% assign i = i | plus: 1 %}
### {{i}}：コメント
単体的複体の多面体の点の「絡み近傍」という概念が定義されました。絡み近傍という名に反して近傍っぽくないことに注意が必要ですね。（この時点で多面体の位相が定義されていないので重要なことではありませんが）


## p. 4

{% assign i = i | plus: 1 %}
### {{i}}：誤植
単体の「直径」という概念が定義されました。直径は$$1$$次元面の長さの最大値と一致すると主張されています。しかし$$0$$次元単体$$\{0\} \subset \mathbb{R}$$は直径が$$0$$ですが、$$1$$次元面を１つも持たないため$$1$$次元面の長さの最大値は存在しませんので、これは主張の反例となります。恐らく「$$0$$次元でない」という条件を書き忘れたものと推測されます。

{% assign i = i | plus: 1 %}
### {{i}}：誤植？
単体的複体の「mesh」という概念が定義されました。meshは単体の直径の$$\max$$が存在する場合は$$\max$$、存在しない場合は$$\infty$$と定義されています。直感的には$$\max$$より非負実数全体における$$\sup$$の方が自然な概念っぽいと思うのですが、何か意図があるのかもしれません。例えば$$\bigcup_{n \in \omega \setminus \{0\}} \{\{n\},\{n+1-\frac{1}{n}\},[n,n+1-\frac{1}{n}]\}$$は$$1$$次元単体的複体となりますが、$$\max$$の流儀だとmesh $$\infty$$、非負実数全体における$$\sup$$の流儀だとmesh $$1$$となります。


## p. 5

{% assign i = i | plus: 1 %}
### {{i}}：保留→解決
定理1.2（共通細分定理：多面体の等しい２つの単体的複体には共通の細分が存在する的な主張）が証明できませんでした。一般に「位相空間の単体分割は細分を除いて一意であるか」という問題はHauptvermutungと呼ばれる重要な問題ですが、そちらには反例が知られているそうです。今回は一般の（ユークリッド空間に埋め込めるとは限らない）位相空間の単体分割を考えているのではなくユークリッド空間内の単体の貼り合わせを考えているだけなので、Hauptvermutungの反例は適用できないということなのでしょうね。

後日他の方に教えていただきましたところ、Hauptvermutungにおいては多面体が一致するのではなく単に同相なだけの状況を考えていることになるので、全く違う設定となっているとのことです。確かに多面体同士が同相であっても、その同相がアフィン変換等のきれいな同相で与えられている保証はなく、片方の多面体内の単体が同相で写った結果もう片方の多面体内の単体になる保証すらないので、かなり自由度の高い設定を考えているわけですね。さて、Hauptvermutungとの設定の違いが分かったところで定理1.2を示していきます。

> **定理1.2の証明：**
>
> $$K_1$$と$$K_2$$を単体的複体とし、$$\lvert K_1 \rvert = \lvert K_2 \rvert$$と仮定する。$$K := \{U \in \mathcal{P}(\lvert K_1 \rvert) \mid \exists x \in \lvert K_1 \rvert, U = \{x\}\}$$と置くと、$$K$$は単体的複体である。実際、$$K$$の各元は点なので単体であり、$$\tau_1,\tau_2 \in K$$が交わる時$$\tau_1 = \tau_2$$となるので局所有限であり、$$\tau_1 \cap \tau_2 = \tau_1 = \tau_2$$となるので共通部分は$$\tau_1$$と$$\tau_2$$の面である。
> 
> $$K$$が$$K_1$$と$$K_2$$の共通細分であることを示す。$$\tau \in K$$とする。$$K$$の定義から$$\tau = \{x\}$$を満たす$$x \in \lvert K_1 \rvert$$が存在する。$$x \in \lvert K_1 \rvert = \lvert K_2 \rvert$$であることから、ある$$\tau_1 \in K_1$$と$$\tau_2 \in K_2$$が存在して$$x \in \tau_1$$かつ$$x \in \tau_2$$である。従って$$\tau \subset \tau_1$$かつ$$\tau \subset \tau_2$$である。以上より、$$K$$は$$K_1$$と$$K_2$$の共通細分である。$$\Box$$

{% assign i = i | plus: 1 %}
### {{i}}：曖昧
単体の多面体間の「単体写像」という概念が定義されました。しかしその定義には写像の連続性が要請され、従って多面体の位相が参照されますが、多面体は点集合であるとp. 2で明言されており多面体の位相はこの時点で定義されていません。

位相の定義案を検討します。単純に考えるとユークリッド空間の部分位相ですが、それが適用できるのは単体的複体が１つのユークリッド空間の単体の集合である場合に限ります。単体の定義において、$$\mathbb{R}^n$$を$$\mathbb{R}^{n+1}$$の部分集合とみなしているかどうかの曖昧性の問題がここで再燃します。もし相対位相と考えるならば、$$\mathbb{R}^n$$を$$\mathbb{R}^{n+1}$$の部分集合とみなす必要があるわけです。

もう１つの位相の候補は、単体のユークリッド位相に関する順極限位相です。例えば$$K_C$$の多面体$$\lvert K_C \rvert$$に順極限位相を入れたものは、$$C$$の下部集合に離散位相を入れたものとなります。重要な例である$$C$$には離散位相を入れて欲しくないと思いますので、この案は誤りであると推測します。

以上より、位相の定義は１つ目の案が正しいものと推測します。これにより、$$\mathbb{R}^n$$を$$\mathbb{R}^{n+1}$$の部分集合とみなしているということが推測されます。ただし２つ目の案を棄却する根拠は少し薄いので、こちらの案も完全には捨てないことにします。

{% assign i = i | plus: 1 %}
### {{i}}：誤植
単体的複体の多面体の点の「開星状体」という概念が定義され、それを用いて多面体間の連続写像の「単体近似」という概念が定義されました。単体的複体$$K$$の多面体の点$$x \in \lvert K \rvert$$の開星状体$$\textrm{Os}(x;K)$$とは「$$x$$を含む単体$$\tau \in K$$の内部全体の集合」となっています。一方で単体的複体$$K_1$$と$$K_2$$と多面体の間の連続写像$$f \colon \lvert K_1 \rvert \to \lvert K_2 \rvert$$に対し、$$f$$の単体近似の定義中で任意の$$x \in \lvert K_1 \rvert$$に対する$$f(\textrm{Os}(x;K_1))$$という概念が断りなく使われています。
例えば定義域$$\lvert K_1 \rvert$$の部分集合$$U \subset \lvert K_1 \rvert$$に対しては$$f(U)$$で$$f$$による$$U$$の像$$\{y \in \lvert K_2 \rvert \mid \exists x \in \lvert K_1 \rvert, f(x) = y\}$$を表す慣習がありますが、開星状体$$\textrm{Os}(x;K_1)$$は$$f$$の定義域$$\lvert K_1 \rvert$$の部分集合ではなく、$$f$$の定義域$$\lvert K_1 \rvert$$の部分集合の集合です。$$f$$の定義域$$\lvert K_1 \rvert$$の部分集合の集合$$\mathcal{U}$$に対する$$f(\mathcal{U})$$という記法は標準的な定義を持たないと思いますので、単体近似という概念がill-definedとなってしまいます。従って開星状体の定義または単体近似の定義に誤植があると考えられます。

修正案を検討します。恐らく開星状体の定義が実際は「単体の内部全体の集合」ではなく「単体の内部全体の和集合」であると推測します。しかし前述したように、内部の定義にも誤植があり$$0$$次元単体の内部がill-definedとなっているのですが、$$0$$次元単体の内部の定義次第でこの修正案で得られるものが変わってしまうので、現時点では開星状体の定義を完全には推測できませんでした。

{% assign i = i | plus: 1 %}
### {{i}}：保留
命題1.3（単体的複体の多面体の間の任意の連続写像$$f$$とその単体近似$$g$$に対し、$$f$$と$$g$$はホモトピック的な主張）が証明できませんでした。まず上述の誤植により内部という概念と単体近似という概念がill-definedとなっていますし、仮に内部という概念を２通りの方法で修正してそれぞれの場合で開星状体という概念を上述したように修正してみることにします。

具体例として$$K_C$$を考えましょう。$$0$$次元単体の内部の定義を空集合として開星状体の定義を上述したように修正したとすると、任意の連続写像$$f \colon \lvert K_C \rvert \to \lvert K_C \rvert$$と$$g \colon \lvert K_C \rvert \to \lvert K_C \rvert$$が単体写像となり、かつ$$f$$が$$g$$の単体近似となります。一方で、定数写像$$\lvert K_C \rvert \to \lvert K_C \rvert, \ x \mapsto 0$$と$$\lvert K_C \rvert \to \lvert K_C \rvert, \ x \mapsto 1$$はホモトピックではありません。従って、この修正による命題1.3は成り立たないことが分かります。以上より、上述した開星状体の定義の修正案を採用する上では$$0$$次元単体の内部の定義は空集合でないということが分かります。ちなみにこの議論において$$\lvert K_C \rvert$$の位相は$$C$$の位相でも離散位相でもどちらでも構いませんので、多面体の位相の定義の推測が誤っていてもここには影響を与えません。

というわけで残る妥当な修正案は、$$0$$次元単体の内部がその単体の多面体であると修正し、開星状体の定義を上述した方法で修正する案です。この場合、やはり任意の連続写像$$\lvert K_C \rvert \to \lvert K_C \rvert$$が単体写像となり、一方で２つの連続写像$$f \colon \lvert K_C \rvert \to \lvert K_C \rvert$$と$$g \colon \lvert K_C \rvert \to \lvert K_C \rvert$$に対し$$g$$が$$f$$の単体近似となるのは$$f = g$$である時に限られますので、その場合は確かに$$f$$と$$g$$がホモトピックとなります。従ってこの修正案は妥当である可能性が高いです。しかしながら、このように修正したとしても命題1.3の証明は思いつきませんでした。

後日他の方に教えていただきましたところ、$$g$$が$$f$$の単体近似であるという仮定から、「任意の$$x \in \lvert K \rvert$$に対しある$$\tau \in L$$が存在して$$f(x) \in \tau $$かつ$$g(x) \in \tau$$を満たす」ということが示せ、これにより「$$f_t(x) = (1-t)f(x)+tg(x)$$が$$f$$と$$g$$の間のホモトピーとなる」ということが示せるそうです。これをヒントに、再度挑戦してみます。

{% assign i = i | plus: 1 %}
### {{i}}：コメント
定理1.4（単体近似定理：有限単体的複体の多面体から単体的複体の多面体への連続写像は、定義域側の有限単体的複体を十分重心細分しておけば単体近似することができる的な主張）は、多面体の代わりに単体分割された空間を考える場合、僕の知っているものだとルベーグの被覆補題を使います。これはコンパクト距離空間に対し適用可能なものなので、同様の議論をしようと思ったら多面体に入る位相もコンパクト距離空間をなすことを期待します。また定理1.1との兼ね合いを考えると、単に距離化可能なだけでなく、直径やmeshと整合的な距離を考えているのではないかと推測します。従って、多面体には性質の分かりにくい順極限位相ではなくやはりユークリッド空間の相対位相を考えているのではないかと推測します。その場合は定理1.1とルベーグの被覆補題を使うことで定理1.4をすんなり示すことができます。

余談ですが、英語版wikipediaで[単体近似定理](https://en.wikipedia.org/wiki/Simplicial_approximation_theorem)を調べると、証明には「[ルベーグの被覆定理](https://en.wikipedia.org/wiki/Lebesgue_covering_dimension#Properties)を用いる」という解説がついています。これは[ルベーグの被覆補題](https://en.wikipedia.org/wiki/Lebesgue%27s_number_lemma)と別物の「有限単体的複体の多面体のチェック次元がアフィン次元と等しい」という定理らしいのですが、そういう証明もあるのでしょうか？

{% assign i = i | plus: 1 %}
### {{i}}：保留
「命題1.3と定理1.4によりコンパクトな多面体から多面体への連続写像は単体近似を持つ」的な旨の演繹が述べられていますが、定理1.4は有限単体的複体にしか適用できず、多面体がコンパクトであったとしても有限単体的複体であるとは限らないことは既に$$K_C$$を例に確認しましたので、定理1.4をどう適用するのかよく分かりませんでした。もしかして多面体のコンパクト性を課しているのは誤植で、実際は単体的複体の有限性が課されているか、または多面体の連結性も課されているのではないかと推測しました。もしくは多面体の位相の推測が誤っている可能性があります。


## p. 6

{% assign i = i | plus: 1 %}
### {{i}}：コメント
「全ての図形が１つの有限次元ユークリッド空間に含まれる」的な旨の説明が再度明言されました。相変わらず図形とは何かが明言されていないためこれだけでは新たな情報とならないのですが、直後に対比的に（多面体とは限らない）一般の位相空間の話が始まったことから、恐らく多面体もまた図形とみなされていることが分かります。

一方で、単体的複体$$K$$に対し、多面体$$\lvert K \rvert$$は必ずしも１つの有限次元ユークリッド空間に含まれないので、この「全ての図形が１つのユークリッド空間に含まれる」という設定は恐らく「$$\lvert K \rvert$$が１つの有限次元ユークリッド空間に含まれる場合しか考えていない」という意図であろうと推測します。

これにより$$\mathbb{R}^n$$が$$\mathbb{R}^{n+1}$$の部分集合とみなされているかどうかはあまり重要ではなくなりました。何故なら、みなそうがみなすまいが、多面体が１つの有限次元ユークリッド空間に含まれていることを課しているからです。これだけの情報では多面体にユークリッド空間の相対位相を入れられるというだけで相対位相を入れた保証にはなりません。しかしながら順極限位相を断りなく用いることは考えにくく、また順極限位相だと単体的複体の取り方によって多面体の位相が変わってしまうかもしれないような気がするため、多面体にはユークリッド位相の相対位相を入れていると推測されます。やはりカントール集合には離散位相を入れたくないということですね。


{% assign i = i | plus: 1 %}
### {{i}}：コメント
位相空間の「三角形分割」という概念が定義されました。この用語は単体分割と同じ意味で使われるものだと思いますが、今回は多面体が１つの有限次元ユークリッド空間に含まれるように定式化していることから、一般の（ユークリッド空間に埋め込めるとは限らない）位相空間に対する単体分割より狭い流儀の単体分割に対応する用語として定義されていることに注意して読み進めていきます。


----


ここまで来て他の方にこの記事を読んでもらい、僕が気付いていなかった***致命的な誤植***を教えていただきました。どうも単体的複体の定義の条件(3)（任意の$$\sigma \in K$$に対し、$$\{\tau \in K \mid \sigma \cap \tau \neq \emptyset\}$$は有限集合である的なもの）が本当は「任意の$$x \in \bigcup_{\sigma \in K} \sigma$$に対し、$$x$$のある近傍$$U \subset \mathbb{R}^n$$が存在して、$$\{\sigma \in K \mid \sigma \cap U \neq \emptyset\}$$が有限集合である」（ただし$$n$$は$$K \subset \mathcal{P}(\mathbb{R}^n)$$を満たす非負整数）の誤植だそうです。これは普通に読むだけでは気付けない誤植ですね。

この修正により、散々単体的複体の具体例として用いてきた$$K_C$$はもはや単体的複体でないことになります。従って、上記の議論の大半は意味がなくなります。また、上記した定理1.2の証明も元の定義に基づいて書かれているため、定義の修正により完全に破綻します。

このように数学書にはしばしば重大な誤植があり、自力でそれに気付くことが困難なこともあります。そのため可能なら独学ではなく専門的知識を持った指導者の下で学習することが望ましいですね。この本は誤植を無視すれば丁寧に書かれていて読みやすくもっと先も読みたいのですが、自力で読んでも今回のような誤植は他に何冊か教科書を用意して本格的に読み進めるのでない限り気付きにくく、専門家の方に逐一今回のような誤植をチェックしてもらうのは心苦しいので、残念ながらここで次の本に移行させていただきます。（普通の学習ではもっと根気強く読むことが多いと思いますが、この企画の趣旨で次に移らせていただきます）

なお、他の方のお勧めによりますとHempelの本というもの併用すれば問題なく読み進められそうとのことです。僕は読んだことがないのでお勧めできるかどうかはわかりませんが、この書籍で勉強なさる方は参考にすると良いかもしれません。
