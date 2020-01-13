---
layout: blog-child
title: 機能和声の実装 － 変化記号
date: 2020-01-13
excerpt: "変化記号のクラスを実装します。"
blog: true
parent: kinou-wasei/
prev: kanon/
tags: [音楽,機能和声,C++]
---

<table>
  <tr>
    <th>
      <h2>数式での翻訳</h2>
    </th>
  </tr>
</table>

記号$$\textrm{♭}$$および$$\textrm{♯}$$のみからなる長さ$$1$$の文字列をそれぞれ同じ記号$$\textrm{♭}$$と$$\textrm{♯}$$で表し、空文字列を$$\textrm{□}$$と置きます。記号$$\textrm{♭}$$と$$\textrm{♯}$$のみからなる文字列の集合
\\[
\textrm{HenkaKigou} = \\{\textrm{♭},\textrm{□},\textrm{♯}\\}
\\]
に属する文字列を***変化記号***と呼びます。定義から、変化記号にはちょうど３種類の文字列があります。完全に公理的集合論で定義をしたい場合は、記号を以下の規則で自然数にコードすることで、$$\mathbb{N}$$を記号とする文字列の集合に翻訳して下さい。
\\[
\begin{align}
\textrm{♭} & := 0 \\\\\
\textrm{♯} & := 1
\end{align}
\\]
通常の流儀では空文字列を変化記号と呼ぶことはしないと思いますが、今回は実装の便宜上空文字列を変化記号とみなしています。流儀によってはこの他の記号も変化記号と呼ぶかもしれませんが、今回はこの３種類のみを扱うことにします。


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
  string m_S;
  int m_num;

public:
  inline HenkaKigou( const string& S );
  inline HenkaKigou( const int& num );

  inline const string& Display() const noexcept;
  inline const int& GetNum() const noexcept;

  static int StringToInt( const string& S );
  static const string& IntToString( const int& num );

};

const HenkaKigou& Flat();
const HenkaKigou& Natural();
const HenkaKigou& Sharp();
inline const HenkaKigou& HenkaKigouTable( const string& S );
const HenkaKigou& HenkaKigouTable( const int& num );

~~~


<table>
  <tr>
    <th>
      <h2>C++での定義</h2>
    </th>
  </tr>
</table>

実際の実装例については[こちら](https://github.com/p-adic/cpp/tree/master/Music/OnMei/HenkaKigou)をご覧下さい。実装においては以下の仕様を要請します。
- `inline HenkaKigou::HenkaKigou( const string& S )`はメンバ初期化子リスト`m_S( S )` , `m_num( StringToInt( S ) )`で与える。
- `inline HenkaKigou::HenkaKigou( const int& num )`はメンバ初期化子リスト`m_S( IntToString( num ) )` , `m_num( num )`で与える。
- `inline const string& HenkaKigou::Display() const noexcept`は`HenkaKigou::m_S`への参照返しである。
- `inline const int& HenkaKigou::GetNum() const noexcept`は`HenkaKigou::m_num`への参照返しである。
- `static int HenkaKigou::StringToInt( const string& N )`は`HenkaKigou::IntToString( num )`が`N`と等しい`int num`を返す。
- `static const string& HenkaKigou::IntToString( const uint& num )`は`"♭"` , `""` , `"♯"`のうち`num+1`番目の文字列で定める。
- クラス`HenkaKigou`に対する等号演算子は自然なものである。
- `const HenkaKigou& Flat()`～`const HenkaKigou& Sharp()`は関数名から自然に連想される$$\textrm{HenkaKigou}$$の元である文字列を`HenkaKigou::Display()`で返す静的変数への参照返しである。
- `inline const HenkaKigou& HenkaKigouTable( const string& S )`は`HenkaKigouTable( HenkaKigou::StringToInt( S ) )`で定める。
- `const HenkaKigou& HenkaKigouTable( const uint& num )`は`Flat()`～`Sharp()`のうち`num+1`番目の関数の戻り値で定める。
