---
layout: blog-child
title: 機能和声の実装 － 変化記号
subtitle: 変化記号
date: 2020-01-13
excerpt: "変化記号のクラスを実装します。"
blog: true
parent: KinouWasei
prev-child: KanOn
next-child: OnMei
defined-class: [HenKaKiGou]
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
\textrm{HenKaKiGou} = \\{\textrm{♭}^n \mid n \in \mathbb{N} \setminus \\{0\\}\\} \cup \\{\textrm{□}\\} \cup \\{\textrm{♯}^n \mid n \in \mathbb{N} \setminus \\{0\\}\\}
\\]
に属する文字列を***変化記号***と呼びます。定義から、変化記号には可算無限種類の文字列があります。例えば$$\textrm{♭}\textrm{♭}$$や$$\textrm{♯}\textrm{♯}\textrm{♯}$$は変化記号ですが、$$\textrm{♭}\textrm{♯}$$や$$\textrm{♯}\textrm{♭}$$は変化記号ではありません。完全に公理的集合論で定義をしたい場合は、記号を以下の規則で自然数にコードすることで、$$\mathbb{N}$$を記号の集合とする文字列の集合に翻訳して下さい。
\\[
\begin{align}
\textrm{♭} & := 0 \\\\\
\textrm{♯} & := 1
\end{align}
\\]
通常の流儀では空文字列を変化記号と呼ぶことはしないと思いますが、今回は実装の便宜上空文字列を変化記号とみなしています。また流儀によっては$$\textrm{??}$$（環境によっては正しく表示できません）や$$\textrm{?}$$や$$\textrm{??}$$（環境によっては正しく表示できません）を変化記号として用いますが、ここではそれらを用いません。

また写像
\\[
\begin{align}
\textrm{GetNum} \colon \textrm{HenKaKiGou} & \to \mathbb{Z} \\\\\
S & \mapsto \textrm{GetNum}(S)
\end{align}
\\]
を以下のように定めます：
1. $$S = \textrm{♭}^n$$を満たす$$n \in \mathbb{N} \setminus \{0\}$$が存在するならば、$$\textrm{GetNum}(S) = -n$$である。
1. $$S = \textrm{□}$$ならば、$$\textrm{GetNum}(S) = 0$$である。
1. $$S = \textrm{♯}^n$$を満たす$$n \in \mathbb{N} \setminus \{0\}$$が存在するならば、$$\textrm{GetNum}(S) = n$$である。

この写像$$\textrm{GetNum} \colon \textrm{HenKaKiGou} \to \mathbb{Z}$$は全単射であるので、これを通じて$$\textrm{HenKaKiGou}$$に環構造を誘導します。ちなみに[幹音の記事]({{ site.url }}/KanOn/)において定義した写像$$\textrm{KanOn} \to \mathbb{Z}/7 \mathbb{Z}$$もまた$$\textrm{GetNum}$$と表していましたが、$$\textrm{KanOn} \cap \textrm{HenKaKiGou} = \emptyset$$であるため、このような記法の重複による曖昧さはあまり問題を起こしません。このように記法を重複させることを***オーバーロード***と言い、数学において曖昧さが致命的でない範囲で断りなく多用されるものですので、今後も断りなく使っていきます。


<table>
  <tr>
    <th>
      <h2>C++での宣言</h2>
    </th>
  </tr>
</table>

{{ page.subtitle }}のクラスおよび関係する関数たちを以下のように宣言します。

~~~c++

class HenKaKiGou
{

private:
  int m_num;

public:
  inline HenKaKiGou( const int& num ) noexcept;

  HenKaKiGou& operator++() noexcept;
  HenKaKiGou& operator--() noexcept;
  
  inline string Display() const noexcept;
  inline const int& GetNum() const noexcept;

  static string IntToString( const int& num ) noexcept;

};

inline bool operator==( const HenKaKiGou& S1 , const HenKaKiGou& S2 ) noexcept;
inline bool operator!=( const HenKaKiGou& S1 , const HenKaKiGou& S2 ) noexcept;

inline HenKaKiGou operator+( const HenKaKiGou& S1 , const HenKaKiGou& S2 ) noexcept;
inline HenKaKiGou operator-( const HenKaKiGou& S1 , const HenKaKiGou& S2 ) noexcept;

~~~


<table>
  <tr>
    <th>
      <h2>C++での定義</h2>
    </th>
  </tr>
</table>

実際の実装例については[こちら](https://github.com/p-adic/cpp/tree/master/Music/OnMei/HenKaKiGou)をご覧下さい。実装においては以下の仕様を要請します。
- `inline HenKaKiGou::HenKaKiGou( const int& num ) noexcept`はメンバ初期化子リスト`m_S( IntToString( num ) )` , `m_num( num )`で定める。
- `HenKaKiGou& HenKaKiGou::operator++() noexcept`と`HenKaKiGou& HenKaKiGou::operator--() noexcept`はそれぞれ`m_num += 1`と`m_num -= 1`を実行し、`return *this`と定める。
- `inline string HenKaKiGou::Display() const noexcept`は`return IntToString( m_num )`と定める。
- `inline const int& HenKaKiGou::GetNum() const noexcept`は`return m_num`と定める。
- `static string HenKaKiGou::IntToString( const int& num )`は`num == 0`ならば空文字列を、`num > 0`ならば`"♯"`のみからなる長さ`-num`の文字列を、`num < -1`ならば`"♭"`のみからなる長さ`num`の文字列を返す。
- クラス`HenKaKiGou`に対する等号演算子は自然なものである。
- クラス`HenKaKiGou`に対する加法演算子と減法演算子は、`HenKaKiGou::GetNum()`が加法演算子と減法演算子と可換になるように定める。
