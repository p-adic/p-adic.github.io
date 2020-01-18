---
layout: blog-child
title: 機能和声の実装 － 変化記号
date: 2020-01-13
excerpt: "変化記号のクラスを実装します。"
blog: true
parent: kinou-wasei/
prev-child: kanon/
next-child: onmei/
tags: [音楽,機能和声,C++]
---

<table>
  <tr>
    <th>
      <h2>数式での翻訳</h2>
    </th>
  </tr>
</table>

$$n \in \mathbb{N} \setminus \{0\}$$に対し、記号$$\textrm{♭}$$および$$\textrm{♯}$$のみからなる長さ$$n$$の文字列をそれぞれ$$\textrm{♭}^n$$と$$\textrm{♯}^n$$で表し、空文字列を$$\textrm{□}$$と置きます。記号$$\textrm{♭}$$と$$\textrm{♯}$$のみからなる文字列の集合
\\[
\textrm{HenkaKigou} = \\{\textrm{♭}^n \mid n \in \mathbb{N} \setminus \\{0\\}\\} \cup \\{\textrm{□}\\} \cup \\{\textrm{♯}^n \mid n \in \mathbb{N} \setminus \\{0\\}\\}
\\]
に属する文字列を***変化記号***と呼びます。定義から、変化記号には可算無限種類の文字列があります。完全に公理的集合論で定義をしたい場合は、記号を以下の規則で自然数にコードすることで、$$\mathbb{N}$$を記号とする文字列の集合に翻訳して下さい。
\\[
\begin{align}
\textrm{♭} & := 0 \\\\\
\textrm{♯} & := 1
\end{align}
\\]
通常の流儀では空文字列を変化記号と呼ぶことはしないと思いますが、今回は実装の便宜上空文字列を変化記号とみなしています。


<table>
  <tr>
    <th>
      <h2>C++での宣言</h2>
    </th>
  </tr>
</table>

変化記号のクラス`HenkaKigou`および関係する関数たちを以下のように宣言します。

~~~c++

class HenkaKigou
{

private:
  int m_num;

public:
  inline HenkaKigou( const int& num ) noexcept;

  inline string Display() const noexcept;
  inline const int& GetNum() const noexcept;

  static string IntToString( const int& num ) noexcept;

};

inline bool operator==( const HenkaKigou& S1 , const HenkaKigou& S2 ) noexcept;
inline bool operator!=( const HenkaKigou& S1 , const HenkaKigou& S2 ) noexcept;

~~~


<table>
  <tr>
    <th>
      <h2>C++での定義</h2>
    </th>
  </tr>
</table>

実際の実装例については[こちら](https://github.com/p-adic/cpp/tree/master/Music/OnMei/HenkaKigou)をご覧下さい。実装においては以下の仕様を要請します。
- `inline HenkaKigou::HenkaKigou( const int& num ) noexcept`はメンバ初期化子リスト`m_S( IntToString( num ) )` , `m_num( num )`で定める。
- `inline string HenkaKigou::Display() const noexcept`は`HenkaKigou::IntToString( m_num )`で定める。
- `inline const int& HenkaKigou::GetNum() const noexcept`は`HenkaKigou::m_num`への参照返しである。
- `static string HenkaKigou::IntToString( const int& num )`は`num == 0`ならば空文字列を、`num > 0`ならば`"♯"`のみからなる長さ`-num`の文字列を、`num < -1`ならば`"♭"`のみからなる長さ`num`の文字列を返す。
- クラス`HenkaKigou`に対する等号演算子は自然なものである。
