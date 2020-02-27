---
layout: blog-child
title: 機能和声の実装 － 音度の接頭辞
subtitle: 音度の接頭辞
date: 2020-02-27
excerpt: "音度の接頭辞のクラスを実装します。"
blog: true
parent: KinouWasei/
prev-child: Pitch/
next-child:
defined-class: [SetTouJiOfOnDo,ZeroIndexedDoSuu,PitchDifferenc]
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
に属する文字列を***音度の接頭辞***と呼びます。流儀によってはこの他にも音度の接頭辞があるかもしれませんが、ここではこれらだけを扱います。ただし音度の接頭辞である$$\textrm{Chou}$$はあくまで文字列としての$$\textrm{Chou}$$であり、調の集合$$\textrm{Chou}$$とは別物であることに注意して下さい。

$$\textrm{ZeroIndexedDoSuu} = \mathbb{N}$$と置き、$$\textrm{PitchDifference} = \mathbb{Z}$$と置き、写像
\\[
\begin{align}
\textrm{Compute} \colon \textrm{ZeroIndexedDoSuu} \times \textrm{PitchDifference} & \to \textrm{SetTouJiOfOnDo} \\\\\
(D,d) & \mapsto \textrm{Compute}(D,d)
\end{align}
\\]
を以下のように定めます：
- $$D$$を$$7$$で割った商を$$q$$、余りを$$r$$と置く。
- $$r = 0$$ならば、$$m = 0$$と置く。
- $$r = 1$$ならば、$$m = 3$$と置く。
- $$r = 2$$ならば、$$m = 7$$と置く。
- $$r = 3$$ならば、$$m = 10$$と置く。
- $$r = 4$$ならば、$$m = 14$$と置く。
- $$r = 5$$ならば、$$m = 17$$と置く。
- $$r = 6$$ならば、$$m = 21$$と置く。
- $$n = 2d-(m+24q)$$と置く。
- $$n = 0$$ならば、$$\textrm{Compute}(D,d) = \textrm{KanZen}$$である。
- $$n = 1$$ならば、$$\textrm{Compute}(D,d) = \textrm{Chou}$$である。
- $$n = -1$$ならば、$$\textrm{Compute}(D,d) = \textrm{Tan}$$である。
- $$n \in \{2,3\}$$ならば、$$\textrm{Compute}(D,d) = \textrm{Zou}$$である。
- $$n \in \{-2,-3\}$$ならば、$$\textrm{Compute}(D,d) = \textrm{Gen}$$である。
- $$n \geq 4$$ならば、$$\textrm{Compute}(D,d) = \textrm{JuuZou}$$である。
- $$n \leq -4$$ならば、$$\textrm{Compute}(D,d) = \textrm{JuuGen}$$である。


<table>
  <tr>
    <th>
      <h2>C++での宣言</h2>
    </th>
  </tr>
</table>

音名のクラス`SetTouJiOfOnDo`および関係する関数たちを以下のように宣言します。

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
- `const SetTouJiOfOnDo& SetTouJiOfOnDo::Compute( const ZeroIndexDoSuu& D , const PitchDifference& d ) noexcept`は`const int q`と`const int r`をそれぞれ`D`を`7`で割った商と余りと定め、`const int m`を`0` , `3` , `7` , `10` , `14` , `17`の`r+1`番目と定め、`const int n`を`d * 2 - ( m + q * 24 )`と定め、`n == 0`ならば`return \textrm{KanZen}()`と定め、`n == 1`ならば`return \textrm{Chou}()`と定め、`n == -1`ならば`return \textrm{Tan}()`と定め、`n == 2 || n == 3`ならば`return \textrm{Zou}()`と定め、`n == -2 || n == -3`ならば、``return \textrm{Gen}`と定め、`n >= 4`ならば、`return \textrm{JuuZou}`と定め、`n <= 4`ならば`return \textrm{JuuGen}`と定める。
- `const SetTouJi& KanZen() noexcept`～`const SetTouJi& JuuGen() noexcept`は`const SetTouJi`型静的局所変数`s`であって`s.Get()`の戻り値が関数名自身とメタに等しいような$$\textrm{SetTouJiOfOnDo}$$の元である文字列であるものへの参照返しである。
- クラス`SetTouJiOfOnDo`に対する等号演算子は自然なものである。
