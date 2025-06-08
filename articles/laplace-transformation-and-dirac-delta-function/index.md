---
title: "ラプラス変換とディラックのデルタ関数"
date: 2020-09-27
categories: 
  - "mathematics"
tags: 
  - "complex-function"
  - "generalized-function"
coverImage: "laplace-transformation-and-dirac-delta-function.png"
---

# ラプラス変換とディラックのデルタ関数

ラプラス変換とは次のように定義される積分変換だった．

$$ \mathcal{L}[f(t)](s) := \int_{0}^{\infty} dt e^{-st} f(t) $$

ここで $f$ が通常の関数である場合と， そうではなくディラックのデルタ関数のように超関数の場合とで， 何れも同じ記法を用いてしまうことが多い．

これは多くの文献でそうなので，その慣例に従わないことは普通はためらわれる． しかしこれらは厳然として別物である場合が一般にはあることを述べたい．

## 背景

何を話題にしようとしているのかというと次のようなことである．

### よくみるラプラス変換表

ラプラス変換といえば，複雑な微分方程式の計算を多項式の計算に還元できてしまうところにある． そのためにしばしば以下のような変換表を目にすることだろう．

\begin{eqnarray} \mathcal{L}[1\cdot u(t)](s) &=& \frac{1}{s} ~~ (\Re[s]>0), \\ \mathcal{L}[t^nu(t)](s) &=& \frac{n!}{s^{n+1}} ~~ (\Re[s]>0 \land n\in\mathbb{N}), \\ \mathcal{L}[e^{-at}u(t)]](s) &=& \frac{1}{s+a} ~~ (\Re[s]>-a), \\ \mathcal{L}[\sin\omega t \cdot u(t)](s) &=& \frac{\omega}{s^2 + \omega^2} ~~ (\Re[s]>0), \\ \mathcal{L}[\cos\omega t \cdot u(t)](s) &=& \frac{s}{s^2 + \omega^2} ~~ (\Re[s]>0), \\ \mathcal{L}_-[\delta(t)](s) &=& 1 ~~ (\forall s\in\mathbb{C}) \end{eqnarray}

ここでデルタ関数のラプラス変換を $\mathcal{L}_-$ と書いているのは誤植ではない． それを整理することが今回の主題である．

### 期待したい計算

まず期待としてデルタ関数 のフーリエ変換は $1$ だったから， それと同じように冒頭で定義を述べた意味でのラプラス変換について $1$ になって欲しい．

\begin{equation} \mathcal{L}[\delta(t)](s) = 1 ~~ (??) \end{equation}

これがすべての始まりである．

### 暗雲

ラプラス変換後に $1$ になるために， 原点 $t=0$ を積分変換の定積分が含んでいるか否かが問題になる． つまりラプラス変換にはフーリエ変換にはなかった以下の特有の難しさがある．

- ラプラス変換の積分の下端である $t=0$ の取り扱いが厳密にやろうとすると思った以上に場合分けを要する．

フーリエ変換の積分の両端は無限遠方であって，例えば $\pm\infty$ の微小な両隣という概念がなく， 無限遠方への極限だけを考えれば良い．

一方でラプラス変換は何気なく使っている単位ステップ関数 $u$ が時刻 $0$ で $1$ であるということや， ラプラス変換の定義式がまるで一つしかないように感じてしまう．

### 期待しない計算

もし $\delta(t) = \tilde{\partial}_t u(t)$ なる超関数の意味での微分を採用して，単位ステップ関数からデルタ関数を紐付けるとき，微分に関するラプラス変換の公式を愚直に利用すると次の期待していない結果が得られる．

\begin{equation} \mathcal{L}[\delta(t)](s) = \mathcal{L}[\tilde{\partial}_t u(t)](s) = s\mathcal{L}[u(t)](s) - u(0) = 1 - 1 = 0 \end{equation}

この辺りについて，実際，正しく触れている文献は大変少なく， 超関数を利用する場合にはしれっと定義を変えて計算をするものである．

## 定義

ラプラス変換の変換対象 $f(t)$ やその導関数が原点で特異性を持っている場合には， 定積分 $\int_0^{\infty}$ はそのままでは実行できない． そこで積分変換を次のように広義積分に拡張する必要がある．

次の広義積分で定義する積分変換$\mathcal{L}_{\pm}$を広義の片側Lapalce変換とよぶ．

\begin{equation} \mathcal{L}_{\pm}[f(t)](s) := \int_{\pm0}^{\infty} dt e^{-st} f(t) := \lim_{\varepsilon\to\pm0}\int_{0+\varepsilon}^{\infty} dt e^{-st} f(t) \end{equation}

## コメント

物理的には時刻 $0$ の他にこれと無限小だけ異なる二つの時刻に対して注意を払う必要が生じる． それは事前初期値と事後初期値である．

[事前初期値と事後初期値とは](https://mathrelish.com/physics/pre-initial-value-post-initial-value)

微分に関する次の関係式は事前初期値と事後初期値の違いに関して著しい．

\begin{equation} \mathcal{L}_{\pm}[\partial_t f(t)](s) = s\mathcal{L}[f(t)](s) - f(\pm0) \end{equation}

ここで $\pm0$ は $f$ の $t=0$ での左極限と右極限であるから， 連続関数であればその区別はなく一致する． しかし次の場合には一致しないかもしくは存在しない．

- $f$ 自体が $t>0$ の領域でしか定義されていない場合
- 不連続関数の場合

一つ目については必然と左極限を考える他なくなる． 二つ目については超関数がラプラス変換の定義に入ってくることになる．

例えば単位ステップ関数$u(t)$は超関数ではないが，不連続なので， その微分とよぶべき演算は，超関数の意味で微分をとることになる．

このとき微分に関するラプラス変換の関係式をデルタ関数について引用すると次のようになる．

\begin{equation} \mathcal{L}_{\pm}[\delta(t)](s) = 1 - u(\pm0) = \begin{cases} 0 & (t\rightarrow +0), \\ 1 & (t\rightarrow -0) \end{cases} \end{equation}

これからわかるようにデルタ関数のラプラス変換に期待する性質 $\delta(t)\mapsto 1$ を満たすためには， ラプラス変換は左極限でなければならないことがわかる．

更に $u(0)=1$ という $t=0$ での値は用いていないことに忘れずに着目すべきである． つまり $u(0)$ の値は $1$ でも $0$ でも，はたまた $1/2$ でも構わない． 必要以上の要求をしない立場を貫こうと思えば，未定義とすべきことがわかる． それはヘビサイドの階段関数 $\theta$ に他ならない．

## 例

### Mathematica の処理

Wolfram 言語での `LaplaceTransform` はディラックのデルタ関数を与えると， 特にオプション引数を指定することなく，`1` を返すようになっている．

```
In[1]:= LaplaceTransform[DiracDelta[t], t, s]
Out[1]:= 1
```

これまでの議論から積分領域の下限は事前初期値になっていなければ， `1` を返すのはおかしい．

この点に関して，Wolfram 言語は以下のドキュメントにあるように， 確かに積分領域の下限を事前初期値とすることを「詳細とオプション」の項で言明している．

[LaplaceTransform](https://reference.wolfram.com/language/ref/LaplaceTransform.html)

しかもサンプルも例示されている． このようなところを見るたび，Mathematica が非常に信頼できるソフトウェアだという 印象を抱かざるを得ない．

### $\theta(0)=1$とする必然性が感じられる例

ディラックのデルタ関数について，引数を動径座標 $r$ のように， 定義域が負になりえないような変数を扱う場合には次の定積分が問題になる．

\begin{equation} \int_0^{\infty}dr \delta(r) = \theta(0) ~~ (\mathrm{undefined}) \end{equation}

この未定義量を $1$ とするか，$1/2$ とするか，はたまた他の値とするかどうかは， 扱う問題に応じて決める他ない．

もし $1$ とするなら，単位ステップ関数 $u$ の原点での値を持って，$\theta(0)$ の値を定義することになる． またそのような設定はこの場合には必然性が感じられる例であろう．

ところで何かしらヘビサイド関数の未定義部分を定義したらば，その定義した値の違いによって， 各々異なるヘビサイド関数が定義されたことになり， これらは区別しなければならない． そして，このことに紐付いて，ディラックのデルタ関数もまた定義を区別して扱う必要がある．

普通，この煩雑さを避けるために，同じ記号を用いてあたかも区別しないように書いて， なるべく混在するような式変形を伴わないようにするが， そうでない場合に首尾一貫性を明示的に保つには，本来は書き分けて記述した方がよいだろう．

## 参考

- [基礎ラプラス変換](https://amzn.to/3kRmYak)
- [デルタ関数とラプラス変換](https://onsen-mula.org/wp-content/uploads/2017/04/laptran_delta.pdf)
- [デルタ関数と微分方程式【応用数学叢書】 (岩波オンデマンドブックス)](https://amzn.to/2NaLYx6)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="Laplace-Transform";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
