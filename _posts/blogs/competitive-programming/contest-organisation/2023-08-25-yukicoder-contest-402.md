---
layout: competitive-programming-contest
title: yukicoder contest 402（線形代数コンテスト）開催記
subtitle: yukicoder contest 402（線形代数コンテスト）
suburl: yukicoder-contest-402
excerpt: "yukicoder contest 402（線形代数コンテスト）の開催記です。"
date: 2023-08-25
num: 454
parent: competitive-programming-contest
prev-child: yukicoder-contest-399
next-child: yukicoder-contest-412
own: 単著
blog: true
tags: [競技プログラミング,数学]
---

まずはお詫びから入らせていただきます。実は前回のコンテスト後に色々ありまして、尊敬する熟練のwriterさんから強い不快感のご表明を受け、具体的には非教育的であるというご批難に加えてyukicoderから他サイトに移住するようご提案をいただくという事態になりました。同じような不快感をお抱いきになった参加者の方々にはこの場で改めてお詫び申し上げます。


そういった事情もあり前回のコンテストから日が浅いうちにまたコンテストを開かせていただくと更なる不快感のもととなるのではないかと心配になり一旦コンテストに関わるのはやめた方が良いのではないかとも思いましたが、せっかくコンテスト予定が空いているので恥を忍んで再挑戦させていただきました。

もちろんただ開催するだけでなくいただいたご諫言をもとに色々と悩んで、どうすればより教育的になるかやどうすれば他サイトへの移住を促されずに済むかを考えました。例えば現状では典型を全く学べないという厳しいご批評をいただいたので、これまでより遥かに典型色の強い問題を混ぜていく試みを検討しました。コンテスト参加者にとって逆に新鮮さや面白みが減ってしまう危険性もありますが、その際はまたご意見をいただければちょうどいい塩梅を模索していきます。

加えて何名かの上級者の方々にご意見や改善すべき点を頂戴したので、それらを踏まえて自分なりにできることを行動に移していくつもりです。具体的には★4以下の解説は用語の大雑把な説明も追加するなどの改善を行い、更にアウトリーチ色の強い問題はできる限り以前より短い問題文を心掛けるようにいたします。ただし後者についてはあまりイメージができておらず、例えば同値な定義の中でより短いものを吟味して差し替えたり一般的な数学用語の定義を非表示（クリックして初めて開く）にしたりといった工夫であれば元々しているので、他に「こうしたらもっと簡潔になる」というアイデアをお持ちの方はぜひご教示いただけますと幸いです。

なお教育的か否かの基準は人それぞれであるなどの事情で教育的であることを諦めるべきというご提案も何人かにいただきましたが、競技プログラミングの勉強をしている一番の動機がその教育的側面であるという事情がございます。教育従事者であるため教育的であることに起因する動機が他の動機より著しく大きいため、そこを諦めてしまうとそもそも競技プログラミングの勉強を続けていく自信もなく、とりあえず教育的であることを目指すのは第一前提とさせていただきました。

もちろんこちらの動機は皆様には関係のないことだとは承知しておりますが、仮に教育的であることが様々な要因で積極的には到達不可能な目標であり諦めるべきであるという結論が共有される文脈ではそもそも非教育的であるというご批判を受けることもございませんので、少なくとも苦言を呈していただいたwriterさんの見解では改善のしようがあるものと考え、ひとまずは諦める必要がないものとして前提をご共有いただきますよう心からお願い申し上げます。

まだまだ勉強不足であり至らない点も多いかと思いますが、いただいたご意見を真摯に受け止めて改善していくつもりですのでよろしくお願いいたします。実際、ご意見をいただいてから今日に至るまで、競技プログラミングの勉強時間を大幅に削って入念に解説の見直しを行いました。口だけではなく実際に行動に移してまいりますので、ご指導ご鞭撻をいただけますと嬉しいです。

謝罪と今後のあり方ご説明は以上です。皆さんにとってはあまり面白くないだろう話を長々としてしまい申し訳ございません。


それではコンテスト内容に話題を移します。当初予定していた問題のうち２問に難易度の上方修正が必要でうち１問（F問題）は★2から★3.5への修正があったのですが、今回は事故（近いコンテストとの問題被りやtester作業中の難易度の急勾配発覚）をケアして予備問題を作成していたので１問をそれに差し替えてC問題としました。

全てのtester作業が終わって開催が決まったのもコンテスト開催2日前なのでタイミング的に全体testerを見つけるのは困難だと思ったので、１問１問丁寧にチェックをして本番に臨みます。特にいつも気がかりなのが★2.5周りの難易度勾配ですが、今回の★2.5であるC・D問題のうちC問題は上述の一件以降に一から細心の注意を払って練り上げたものでひときわ典型色が強いので、D問題との難易度反転はまず起こらないだろうと信じています。（※コンテスト本番での参加者の解き具合を参考にしてB問題の難易度を★2から★2.5に、D問題の難易度を★2.5から★3に上方修正しました。これにより最新の★2.5はB・C問題に変更となっています）


そして迎えたコンテスト当日です。問題のチェックを繰り返し、根を詰めすぎないように別の作問を進めたりして過ごしました。それでもついつい気になってしまい、結局開始直前にも再度問題のチェックをしていました。

今回も大きな事故はなく済んで良かったです。質問が１件もなかったのは大きな進歩かもしれません。参加者の皆様、testerの皆様、そして色々とご相談に乗ってくださった方々にこの場でお礼申し上げます。

今回は線形代数コンテストという趣旨でセットを組ませていただきました。線形代数の標準的なカリキュラムに沿った問題構成となっているので、線形代数に苦手意識がある人はぜひ難易度の低い問題から順に解いていって理解の確認をしてみてください。線形代数が得意な人でも満足していただけるように、背景や解説もかなり丁寧に書かせていただきました。
- A問題 行列累乗：行列の掛け算
- B問題 線形写像：行列表示
- C問題 特殊線形群の標準表現：逆行列計算
- D問題 一次変換と体積：行列式の幾何的意味づけ
- E問題 奇行列式：行列式の余因子展開
- F問題 完全列：掃き出し法と階数計算
- G問題 行列累乗根：対称行列の対角化
- H問題 一次変換と面積：総まとめ

次回は基礎論コンテストを予定しています。そちらも丁寧な解説を心がけておりますので、開催の際はぜひよろしくお願いいたします。
