---
layout: blog
title: yukicoder score contest 10参加記
date: 2025-02-26
excerpt: "yukicoder score contest 10に参加した記録です。"
parent: competitive-programming-problem-solving/
prev-child: AHC036
next-child: CPCTF2025
blog: true
image-directory: competitive-programming
tags: [競技プログラミング,数学]
---

[yukicoder score contest 10](https://yukicoder.me/contests/532)の参加記です。これまでもyukicoderのスコアコンは全埋めしていましたが、スコアコンのテクニックを乱択しか持っていなかったため多くは自明投げやショートコード投げや、闇雲な乱択投げでした。

しかしAHC036で初めて真面目に（とは言っても11日間ひたすら思いつく限り乱択を投げまくっただけですが）スコアコンに参加してとても楽しかったので、またいつかスコアコンに出てもっと考えて乱択を投げようと思っていました（AHC036の参加記は[こちら]({{ site.ur }}/AHC036/)です）。するとyukicoder score contest 10が開催されると知り、5ヶ月ちょいぶりの挑戦です！

ただし金曜以外は夜空いていないので、残念ながら途中参加確定です。実装が致命的に遅いタイプなので、これではそもそも提出できるかすら怪しいところ。

そこで対策として、予めスコアコンのテクニックを何かしらライブラリー化して時間短縮を図ることにしました。何から勉強すればいいのか分かりませんでしたが、ひとまず乱択と相性の良さそうな焼きなまし法をざっくりと勉強。

細かいパラメータの決め方は分かりませんが、適当に決めてライブラリー化しておきました。ライブラリーと言っても、ラムダ式とかを渡すだけみたいなちゃんとしたものではなくコードのテンプレート的なものを作っただけですが、それでも実装の遅い自分には大きいです。

準備も整った状態で、いざ参加！


## 問題文

問題文そのものは[こちら](https://yukicoder.me/problems/no/5021)からご確認いただけます。

大雑把に言うと、パスカルの三角形を逆向きに（下から）作って、入力で与えられている三角形の数列との誤差を最小化する問題です。ただし誤差は$\ell^{\infty}$誤差を少しいじったもので、絶対値の代わりにmod $10^8$での距離を測る感じです。

それでは挑戦してみましょう。


## 実装の前に

まずAHC036での反省から、gdbデバッグが機能しにくいラムダ式を極力使わないことにしました。もちろん焼きなまし法ライブラリもその前提で、ラムダ式を受け取らないだけでなく中身でもなるべく使わない形式にしています。

またこれもAHC036での経験から、サンプルは即座にダウンロードします。ローカルと提出時で挙動を変え、ローカルではサンプルが走るように設定します。


## 実装方針

焼きなまし法ライブラリがあるので、焼きなまし法決め打ちです。となるとまずはスコア計算を実装するのが良さそうです。何かしらのデータ構造で変更クエリとかが高速に処理できるようにすべきなのかもしれませんが、とにかく時間がありません。愚直を頑張って実装します。

それができたら、色々な乱択を試していくことにします。焼きなまし法ライブラリはmodeという変数があり、時間経過でmodeが変わっていきmodeに従って乱択が切り替わるようになっています。


## 実際の実装

とはいえあまり乱択が思い浮かびません。そこで乱択より先に決定的な前処理で局所最適解を探していきました。例えば二項係数で誤差を割ったりできたら分かりやすいのですが、mod $10^8$では難しいです。そこで、入力で与えられた三角形の底辺そのものを使ってパスカルの三角形を作り、そこから１つの成分の2進法の１つの桁を変更するイメージで2冪を足すことを試みました。

動かしてみるとあら不思議、全くスコアが更新されません。焼きなまし法ライブラリが壊れているのかな？　と思ったけどよく考えたら１つの成分をちょっといじった程度だと$\ell^{\infty}$誤差もその亜種も変わらなさそうなので、もっと劇的に更新する必要がありそう。

そこで思いついたのが、パスカルの三角形の底辺全体を乱択することです。ちまちま周辺分布の最適化をせずに、一気に局所最適解を探していきます。

これは成功で、ちゃんとスコアが更新されました。しかしここでもう時間があまりありません。最初のmodeではこの乱択をして、２個目のmodeではさっきのちまちました2進法で更新、としてみましたが２個目のmodeがまるでスコア改善に繋がらない。

残り時間を見て焦りながら$\ell^{\infty}$誤差の性質を考えて、$\ell^{\infty}$誤差に影響を与える成分を逆算してそこのみから成分を乱択することにしてみました。するとコンパイルエラーいっぱい。どこかしらの閉じ括弧が足りなかったみたいで大変。

残り時間は10分を切っています。まだ１回も提出できていません。頑張ってコンパイルエラーを読み解き、やっとミスを発見。実行すると２個目のmodeでも若干のスコア改善あり。残り6分。WAが出た時のことを考えて、即座に投げました。

実際の提出ページは[こちら](https://yukicoder.me/submissions/1046240)です。

~~~c++
VO Solve()
{
  #ifdef DEBUG
    ifstream ifs( "in/test_001.txt" );
    auto Input = [&](){ int n; ifs >> n; return n; };
  #endif
  CEXPR( double , log_temparature_min , 1e-2 );
  CEXPR( int , updatability_scale , 1e5 );
  RCIN( int , N , Input() );
  assert( N == SimulatedAnnealing::N );
  FOR( i , 0 , N ){
    SimulatedAnnealing::a[i].resize( i + 1 );
    FOREQ( j , 0 , i ){
      RSET( SimulatedAnnealing::a[i][j] , Input() );
    }
  }
  START_WATCH;
  SimulatedAnnealing SA{};

  // pre computation
  
  SA.Execute( log_temparature_min , CURRENT_TIME , 1900 , updatability_scale );
  RETURN( SA );
}
REPEAT_MAIN(1);

/* 省略 */

class SimulatedAnnealing
{

public:
  // static data
  static constexpr double log_temparature_min = 1e-2;
  static constexpr int updatability_scale = 1e5;
  static constexpr double log_updatability_scale = log( updatability_scale );
  static int N;
  static constexpr int B = 1e8;
  using MOD = Mod<B>;
  static vector<vector<MOD>> a;
  
  // mode
  int mode;

  // temporary parameter
  vector<MOD> C;

  // optimal parameter
  vector<MOD> C_opt;

  // update memory
  int sj;
  int sd;
  vector<MOD> sC;
  T2<int> sij;
  int diff_max;

  SimulatedAnnealing() : mode{ 0 } , C( a[N-1] ) , C_opt( C ) , sj() , sd( -1 ) , sC( C ) , sij() , diff_max()
  {
  }

  void SetOptimal()
  {
    C_opt = C;
  }
  
  void OptimiseTemporary()
  {
    // 必要な部分のみ変更してもよい。
    C = C_opt;
  }
  
  void Increment()
  {
    if( ++sd == 26 ){
      sd = 0;
      int down = N - 1 - sij[O];
      sj = GetRand( max( 0 , sij[I] - down ) , min( N - 1 , sij[I] + down ) );
    }
  }

  void Shift1()
  {
    swap( sC , C );
    FOR( j , 0 , N ){
      C[j] = GetRand( 0 , B - 1 );
    }
  }

  void Revert1()
  {
    swap( C , sC );
  }

  void Shift2()
  {
    Increment();
    sC[sj] = C[sj];
    C[sj] += 1 << sd;
  }

  void Revert2()
  {
    C[sj] = sC[sj];
  }

  // void Shift3()
  // {
  //   Increment();
  //   sC[sj] = C[sj];
  //   C[sj] = GetRand( 0 , 1000 );
  // }

  // void Revert3()
  // {
  //   C[sj] = sC[sj];
  // }

  void Shift( const double& current_time )
  {
    int mode_num = 0;
    if( mode == mode_num++ ){
      if( current_time > 1600 ){
        OptimiseTemporary();
        CERR( "" );
        CERR( "Changed mode:" , mode , "->" , mode_num );
        CERR( "Current score:" , ComputeScore() );
        CERR( "" );
        mode = mode_num;
      }
    } else if( mode == mode_num++ ){
      // if( current_time > 1900 ){
      //   OptimiseTemporary();
      //   CERR( "" );
      //   CERR( "Changed mode:" , mode , "->" , mode_num );
      //   CERR( "Current score:" , ComputeScore() );
      //   CERR( "" );
      //   mode = mode_num;
      // }
    } else if( mode == mode_num++ ){


    } else {
      abort();
    }
    mode_num = 0;
    if( mode == mode_num++ ){
      Shift1();
    } else if( mode == mode_num++ ){
      Shift2();
    } else if( mode == mode_num++ ){
      // Shift3();
    } else {
      abort();
    }
    return;
  }

  void Revert()
  {
    int mode_num = 0;
    if( mode == mode_num++ ){
      Revert1();
    } else if( mode == mode_num++ ){
      Revert2();
    } else if( mode == mode_num++ ){
      // Revert3();
    } else {
      abort();
    }
    return;
  }

  using score_type = ll;
  
  score_type ComputeScore()
  {
    score_type score = 0;
    diff_max = 0;
    vector<MOD> A = C;
    FOREQINV( i , N - 1 , 0 ){
      if( i < N - 1 ){
        FOREQ( j , 0 , i ){
          A[j] += A[j+1];
        }
        pop( A );
      }
      auto& a_i = a[i];
      FOREQ( j , 0 , i ){
        int diff = ( A[j] - a_i[j] ).Represent();
        diff = min( diff , B - diff );
        if( diff_max < diff ){
          diff_max = diff;
          sij = {i,j};
          #ifdef DEBUG
            score = -( ll( diff_max ) * 10000 );
          #else
            score = -( ll( diff_max ) << 12 );
          #endif
        } else if ( diff_max == diff ){
          score--;
        }
      }
    }
    return score;
  }

  double Temparature( const double& log_temparature_min , const double& time , const int& time_lim )
  {
    return exp( ( log_temparature_min * time ) / time_lim );
  }
  
  bool Updatable( const int& updatability_scale , const score_type& score , const score_type& score_local_opt , const double& log_temparature_min , const double& time , const int& time_lim )
  {
    return score > score_local_opt || GetRand( 0 , updatability_scale ) < exp( ( score - score_local_opt ) / Temparature( log_temparature_min , time , time_lim ) + log_updatability_scale );
  }

  void Execute( const double& log_temparature_min , const double& start_time , const double& final_time , const int& updatability_scale )
  {
    START_WATCH;
    const double time_lim = final_time - start_time;
    score_type score_opt = ComputeScore() , score_local_opt = score_opt;
    while( CHECK_WATCH( time_lim ) ){
      Shift( current_time );
      const score_type score = ComputeScore();
      if( Updatable( updatability_scale , score , score_local_opt , log_temparature_min , current_time , time_lim ) ){
        if( score > score_opt ){
          CERR( "Updated the optimal score:" , score_opt , "->" , score );
          SetOptimal();
          score_opt = score_local_opt = score;
        } else {
          if( score > score_local_opt ){
            CERR( "Updated the local optimal score:" , score_local_opt , "->" , score );
          } else if( score < score_local_opt ){
            CERR( "Changed the local optimal score:" , score_local_opt , "->" , score );
          } else {
            CERR( "Kept the local optimal score:" , score_local_opt );
          }
          score_local_opt = score;
        }
      } else {
        CERR( "Declined the last score:" , score );
        Revert();
      }
    }
    OptimiseTemporary();
    #ifdef DEBUG
      CERR( "The last score is:" , score_opt );
      assert( score_opt == ComputeScore() );
    #endif
    return;
  }
};

int SimulatedAnnealing::N = 50;
vector<vector<SimulatedAnnealing::MOD>> SimulatedAnnealing::a = vector( SimulatedAnnealing::N , vector<MOD>() );

template <class Traits> inline basic_ostream<char,Traits>& operator<<( basic_ostream<char,Traits>& os , const SimulatedAnnealing& SA ) { return os << SA.C; }

~~~

## 提出結果

無事AC！　スコアは35,006,920点で、19位に入っていました。ヒューリスティックでこんなにいい順位取れるなんてびっくり。焼きなまし法、一番好きな法律です！

そして時間切れ。この短い時間で20位に落ちてしまいましたが満足です。


## 感想戦

初めての焼きなまし法、とても楽しかったです。次はフル参加したいな。金曜のレギュラーコンテスト枠にスコアコン欲しい。

あと局所的な遷移でない全体の乱択でも焼きなまし法を使っていたのが意味なかったので、そういう初期化っぽい部分の処理を別にするようにライブラリを改修しなきゃ。
