---
layout: blog-child
title: 機能和声の実装 － 音度の接頭辞
subtitle: 音度の接頭辞
date: 2020-02-27
excerpt: "音度の接頭辞のクラスを実装します。"
blog: true
parent: KinouWasei/
prev-child: Pitch/
next-child: OnDo/
defined-class: [SetTouJiOfOnDo,ZeroIndexedDoSuu,PitchDifference]
tags: [音楽,機能和声,C++]
---

<table>
  <tr>
    <th>
      <h2>数式での翻訳</h2>
    </th>
  </tr>
</table>

文字列の集合
\\[
\textrm{SetTouJiOfOnDo} = \\{\textrm{KanZen},\textrm{Chou},\textrm{Tan},\textrm{Zou},\textrm{Gen},\textrm{JuuZou},\textrm{JuuGen}\\}
\\]
に属する文字列を***音度の接頭辞***と呼びます。流儀によってはこの他にも音度の接頭辞があるかもしれませんが、ここではこれらだけを扱います。ただし音度の接頭辞である$$\textrm{Chou}$$はあくまで文字列としての$$\textrm{Chou}$$であり、調の集合をメタに表す記号$$\textrm{Chou}$$とは別物であることに注意して下さい。

$$\textrm{ZeroIndexedDoSuu} = \mathbb{N}$$と置き、$$\textrm{PitchDifference} = \mathbb{Z}$$と置きます。$$\textrm{ZeroIndexedDoSuu}$$は次の[音度の記事]({{ site.url }}/OnDo/)で導入する$$\textrm{DoSuu}$$という集合の亜種で、実装のために便宜上導入するものです。大雑把に言うと、$$\textrm{DoSuu}$$は$$2$$つのピッチの関係を表す$$1$$以上の整数の集合で、$$\textrm{ZeroIndexedDoSuu}$$は単に$$\textrm{DoSuu}$$の各要素を$$1$$ずらしただけのものです。従って$$0$$は$$\textrm{DoSuu}$$の要素ではないですが、$$\textrm{ZeroIndexedDoSuu}$$の要素となります。

写像$$D \in \textrm{ZeroIndexedDoSuu}$$と$$d \in \textrm{PitchDifference}$$に対し、音度の接頭辞$$S_{D,d}$$を以下のように定めます：
1. $$r = \textrm{Represent}(D + 7\mathbb{Z}) \in \{0,1,2,3,4,5,6\}$$と置き、$$q = \frac{D - r}{7}\in \mathbb{N}$$と置く。
1. $$r = 0$$ならば、$$m = 0 \in \mathbb{N}$$と置く。
1. $$r = 1$$ならば、$$m = 3 \in \mathbb{N}$$と置く。
1. $$r = 2$$ならば、$$m = 7 \in \mathbb{N}$$と置く。
1. $$r = 3$$ならば、$$m = 10 \in \mathbb{N}$$と置く。
1. $$r = 4$$ならば、$$m = 14 \in \mathbb{N}$$と置く。
1. $$r = 5$$ならば、$$m = 17 \in \mathbb{N}$$と置く。
1. $$r = 6$$ならば、$$m = 21 \in \mathbb{N}$$と置く。
1. $$n = 2d-(m+24q) \in \mathbb{Z}$$と置く。
1. $$n = 0$$ならば、$$S_{D,d} = \textrm{KanZen}$$である。
1. $$n = 1$$ならば、$$S_{D,d} = \textrm{Chou}$$である。
1. $$n = -1$$ならば、$$S_{D,d} = \textrm{Tan}$$である。
1. $$n \in \{2,3\}$$ならば、$$S_{D,d} = \textrm{Zou}$$である。
1. $$n \in \{-2,-3\}$$ならば、$$S_{D,d} = \textrm{Gen}$$である。
1. $$n \geq 4$$ならば、$$S_{D,d} = \textrm{JuuZou}$$である。
1. $$n \leq -4$$ならば、$$S_{D,d} = \textrm{JuuGen}$$である。

この$$S_{D,d}$$を***$$(D,d)$$に対応する音度の接頭辞***と呼びます。

<table>
  <tr>
    <th>
      <h2>C++での宣言</h2>
    </th>
  </tr>
</table>

{{ subtitle }}のクラスおよび関係する関数たちを以下のように宣言します。

~~~c++

using ZeroIndexedDoSuu = uint;
using PitchDifference = int;

class SetTouJiOfOnDo
{

private:
  string m_s;

public:
  inline SetTouJiOfOnDo( const string& s ) noexcept;

  inline const string& Get() const noexcept;

  static const SetTouJiOfOnDo& Compute( const ZeroIndexDoSuu& D , const PitchDifference& d ) noexcept;

  static const SetTouJiOfOnDo& KanZen() noexcept;
  static const SetTouJiOfOnDo& Chou() noexcept;
  static const SetTouJiOfOnDo& Tan() noexcept;
  static const SetTouJiOfOnDo& Zou() noexcept;
  static const SetTouJiOfOnDo& Gen() noexcept;
  static const SetTouJiOfOnDo& JuuZou() noexcept;
  static const SetTouJiOfOnDo& JuuGen() noexcept;

};

inline operator==( const SetTouJiOfOnDo& s1 , const SetTouJiOfOnDo& s2 ) noexcept;
inline operator!=( const SetTouJiOfOnDo& s1 , const SetTouJiOfOnDo& s2 ) noexcept;


~~~


<table>
  <tr>
    <th>
      <h2>C++での定義</h2>
    </th>
  </tr>
</table>

実際の実装例については[こちら](https://github.com/p-adic/cpp/tree/master/Music/OnMei/Pitch/OnDo/SetTouJi)をご覧下さい。実装においては以下の仕様を要請します。
- `inline SetTouJiOfOnDo::SetTouJiOfOnDo( const string& s ) noexcept`はメンバ初期化子リスト`m_s( s )`で定める。
- `inline const string& SetTouJiOfOnDo::Get() const noexcept`は`return m_s`と定める。
- `const SetTouJiOfOnDo& SetTouJiOfOnDo::Compute( const ZeroIndexDoSuu& D , const PitchDifference& d ) noexcept`は`const int q`と`const int r`をそれぞれ`D`を`7`で割った商と余りと定め、`const int m`を`0` , `3` , `7` , `10` , `14` , `17`の`r+1`番目と定め、`const int n`を`d * 2 - ( m + q * 24 )`と定め、`n == 0`ならば`return KanZen()`と定め、`n == 1`ならば`return Chou()`と定め、`n == -1`ならば`return Tan()`と定め、`n == 2 || n == 3`ならば`return Zou()`と定め、`n == -2 || n == -3`ならば、`return Gen()`と定め、`n >= 4`ならば、`return JuuZou()`と定め、`n <= -4`ならば`return JuuGen()`と定める。
- `const SetTouJi& KanZen() noexcept`～`const SetTouJi& JuuGen() noexcept`は`const SetTouJi`型静的局所変数`s`であって`s.Get()`の戻り値が関数名自身とメタに等しいような$$\textrm{SetTouJiOfOnDo}$$の元である文字列であるものへの参照返しである。
- クラス`SetTouJiOfOnDo`に対する等号演算子は自然なものである。
