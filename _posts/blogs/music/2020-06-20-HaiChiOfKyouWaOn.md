---
layout: blog-child
title: 機能和声の実装 － 協和音の配置
subtitle: 配置
date: 2020-06-20
excerpt: "協和音の配置のクラスを実装します。"
blog: true
parent: KinouWasei/
prev-child: HaiChi/
next-child: 
defined-class: [HaiChiOfKyouWaOn]
tags: [音楽,機能和声,C++]
---

<table>
  <tr>
    <th>
      <h2>数式での翻訳</h2>
    </th>
  </tr>
</table>


$$P$$を配置とします。調$$N$$に対し、$$P$$が***調$$N$$の協和音の配置***であるとは、$$P$$が非交叉で自然な音域に属し自然な音度域に属し、かつ以下の条件を満たす$$3$$和音$$H$$が存在するということです：
1. $$P$$は$$H$$の配置である。
1. $$H$$は調$$N$$の協和音である。
1. $$\textrm{GetOnKai}(N)$$が$$\textrm{ChouOnKai}$$でありかつ調$$N$$における$$H$$の階名が$$V$$であるならば、$$\textrm{GetOnMei}(\textrm{GetPitch}(P,i))$$が$$H$$の第$$3$$音と一致するような$$i \in \{0,1,2,3\}$$は一意である。
1. $$P$$のバスは$$H$$の第$$5$$音でない。

ここで「$$H$$の階名」という概念はill-definedであったことに対し「調$$N$$における$$H$$の階名」という概念はwell-definedであったことに注意しましょう。忘れてしまった人は[協和音の記事]({{ site.url }}/KyouWaOn/)を読み返しておいて下さい。第$$3$$音の一意性は$$\textrm{GetOnKai}(N)$$が$$\textrm{ChouOnKai}$$でありかつ調$$N$$における$$H$$の階名が$$V$$である場合にしか課されていませんが、そうでない場合にも協和音の配置の「良さ」を考える際にはなるべく第$$3$$音を一意にした方がよい状況があるようです。それを踏まえて、調$$N$$の協和音の配置$$P$$に対して「良さ」を形式化した指標として***評価値***という概念を以下のように導入します：
- $$\textrm{GetOnMei}(\textrm{GetPitch}(P,i))$$が$$H$$の第$$3$$音と一致するような$$i \in \{0,1,2,3\}$$が一意であるならば、$$P$$の調$$N$$における評価値を$$4$$と定める。
- $$\textrm{GetOnMei}(\textrm{GetPitch}(P,i))$$が$$H$$の第$$3$$音と一致するような$$i \in \{0,1,2,3\}$$が一意でないとする。
    - $$\textrm{GetOnKai}(N)$$が$$\textrm{ChouOnKai}$$であるならば、$$P$$の調$$N$$における評価値を$$1$$と定める。
    - $$\textrm{GetOnKai}(N)$$が$$\textrm{ChouOnKai}$$でないならば、$$P$$の調$$N$$における評価値を$$2$$と定める。

ちなみに$$H$$は$$P$$の和音であるため一意ですので、$$P$$の調$$N$$における評価値という概念は$$H$$の選び方に依存しません。その意味で、$$P$$の調$$N$$における評価値はwell-definedです。


<table>
  <tr>
    <th>
      <h2>C++での宣言</h2>
    </th>
  </tr>
</table>

{{ page.subtitle }}のクラスおよび関係する関数たちを以下のように宣言します。

~~~c++

class HaiChiOfKyouWaOn :
  public KyouWaOn , public HaiChi
{

private:
  bool m_valid;
  uint m_goodness;

public:
  inline HaiChiOfKyouWaOn( const Chou& N , const KaiMei& n , const uint& bas_num , const uint& bas_octave , const uint& ten_num , const uint& ten_octave , const uint& alt_num , const uint& alt_octave , const uint& sop_num , const uint& sop_octave ) noexcept;

  void SetValidity( const Chou& N , const KaiMei& n , const uint& bas_num , const uint& bas_octave , const uint& ten_num , const uint& ten_octave , const uint& alt_num , const uint& alt_octave , const uint& sop_num , const uint& sop_octave ) noexcept;

  inline const OnMei& GetOnMei( const uint& i ) const noexcept;

};

~~~


<table>
  <tr>
    <th>
      <h2>C++での定義</h2>
    </th>
  </tr>
</table>

実際の実装例については[こちら](https://github.com/p-adic/cpp/tree/master/Music/HaiChi/KyouWaOn)をご覧下さい。実装においては以下の仕様を要請します。
- `inline HaiChiOfKyouWaOn::HaiChiOfKyouWaOn( const Chou& N , const KaiMei& n , const uint& bas_num , const uint& bas_octave , const uint& ten_num , const uint& ten_octave , const uint& alt_num , const uint& alt_octave , const uint& sop_num , const uint& sop_octave ) noexcept`はメンバ初期化子`KyouWaOn( N , n )` ,
`HaiChi( GetOnMei( bas_num ) , bas_octave , GetOnMei( ten_num ) , ten_octave , GetOnMei( alt_num ) , alt_octave , GetOnMei( sop_num ) , sop_octave )` ,
`m_valid( false )` , `m_goodness( 0 )`および実装部`SetValidity( N , n , bas_num , bas_octave , ten_num , ten_octave , alt_num , alt_octave , sop_num , sop_octave );`で定める。
- `void HaiChiOfKyouWaOn::SetValidity( const Chou& N , const KaiMei& n , const uint& bas_num , const uint& bas_octave , const uint& ten_num , const uint& ten_octave , const uint& alt_num , const uint& alt_octave , const uint& sop_num , const uint& sop_octave ) noexcept`は以下のように定める：
1. `bas_num == 5`または`! IsNaturallyOrdered()`または`GetNumberOfOnMei() != 3`または`CheckValidKaiMei( N , n )`の時は`return;`と定める。
1. そうでない時、`CheckHasDoubleDaiSanOn( bas_num , ten_num , alt_num , sop_num )`であるとする：
  1. `N.GetOnKai() == ChouOnKai()`であるとする。
    1. `n == KaiMei::V()`である時は`return;`と定める。
    1. そうでない時は`m_goodness = 1;`と`m_valid = true;`としてから`return;``と定める。
    1. `N.GetOnKai() == ChouOnKai()`である時は`return;`と定め、そうでない時は`m_goodness = 1;` , `m_valid = true;`としてから`return;``と定める。
  1. そうでない時、`m_goodness = 2;` , `m_valid = true;`としてから、`return;`と定める。
1. そうでない時、`m_goodness = 4;` , `m_valid = true;`としてから`return;`と定める。
- `inline const OnMei& HaiChiOfKyouWaOn::GetOnMei( const uint& i ) const noexcept`は`KyouWaOn::GetNeOn()` , `KyouWaOn::GetDaiSanOn()` , `KyouWaOn::GetDaiGoOn()`のうち$$i$$番目の戻り値で定める。
