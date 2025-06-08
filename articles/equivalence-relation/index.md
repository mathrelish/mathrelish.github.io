---
title: "同値関係とは"
date: 2018-07-08
categories: 
  - "mathematics"
tags: 
  - "set"
coverImage: "equivalence.png"
---

# 同値関係

同値関係とは「関係」という数学的な概念のうちで特別なものの一つで， 相等関係「$=$」の抽象化でもある．

ある二つのものが同じであるという事柄を記述するのに用いられ， 対象の分類であったり，商空間による例の生成などに用いられる．

以下では同値関係でない二項関係についても具体例を挙げる．

[The Math Relish Journal Volume 1S](https://mathrelish.booth.pm/items/1123647/)

## 着想と背景

「関係」という語を集合の中で見出すことで， 「$=$」「$\leq$」などを集合論として捉えることができる．

例えば与えられた集合 $S$ の中で，ある元 $a$ に「等しい」という「関係」にある元は $b$ だったとしよう．すると普通は $a=b$ とか書いて表す． ここの「$=$」が「関係」である．

集合 $S$ の中にはそういった「$=$」で表される「関係」が他にもたくさんあるだろう． 何れにしてもこういった「関係」というのは他にいくらでも導入できる． するとそれだけ多くの記号が各関係を表すのに必要になる． それらのために集合論に特別な地位を持った独立な記号を用意する必要があるのだろうか．

その必要はない．

互いに「関係」する元を組として表現し，その組が属すべき条件を書いた集合で，その「関係」を表現できる．

このような約束の下で，便宜のために慣習的な記号や専用の記号を用いればよい．

## 定義

集合 $S$ 上の二項関係 $R$ とは次の集合のことをいう．

$$ R := \{(x,y)\in S\times S ~|~ R(x,y) = \top \} $$

$R(x,y)$ を $xRy$ などのように中置記法でしばしば記す．

$\top$ は真であることを示す記号である．

二項関係のうち同値関係を定める基本的な関係は次の三つの関係である．

集合 $S$ 上の任意の元について，二項関係 $R$ が次を満たすならば，$R$ を反射関係といい， また二項関係 $R$ は反射律を満たすという．

$$ (\forall x\in S)(xRx=\top) $$

　

集合 $S$ 上の任意の元について，二項関係 $R$ が次を満たすならば，$R$ を対称関係といい， また二項関係 $R$ は対称律を満たすという．

$$ (\forall x\in S)(\forall y\in S)(xRy=\top\Rightarrow yRx=\top) $$

　

集合 $S$ 上の任意の元について，二項関係 $R$ が次を満たすならば，$R$ を推移関係といい， また二項関係 $R$ は推移律を満たすという．

$$ (\forall x\in S)(\forall y\in S)(\forall z\in S)(xRy\land yRz=\top\Rightarrow xRz=\top) $$

以上を持ってして同値関係を次で定義できる．

二項関係 $R$ が次のすべての関係を満たすならば，$R$ を同値関係といい， また二項関係 $R$ は同値律を満たすという．

\- 反射関係 - 対称関係 - 推移関係

同値関係 $R$ を度々 $\sim$ と書く．但し専用の記号がある場合にはその限りではない．

## コメント

### 同値関係に反射律は不必要か？

関係 $R$ について対称律と推移律が成り立ったとする．すると次の推論をしたくなる．

> 対称律から $xRy$ なるとき $yRx$であり，更に推移律に従えば $xRx$ を得る． 故に同値関係の定義には反射律は不要である．

この推論は誤っているのだが，どこが誤っているのだろうか． もし正しいとすると，対称律と推移律が真であるならば，反射律はいつでも真ということになる． よって対称律と推移律が真であるにもかかわらず，反射律が偽であるような場合が重要となる． そのような例は後で与えるわけだが，ここでは上記の推論がどこで誤っているか指摘をしておく．

それは $xRy$ を満たす $y$ が暗黙にいつでも存在するということを仮定しているところが誤っている． 対称律や推移律はあくまでも，もし $xRy$ を満たす $y$ があったら，これこれだ，と述べているだけで，存在しなかったらこの推論は成り立たない．

## 例

同値関係と同値関係でない具体例を以下に示す．

### 同値関係である例

#### 相等関係

相等関係とはいわゆる等号 $=$ による関係のことである． これが同値関係であることは明らかである． 相等関係は自分自身しか等しいものはいないという，最も狭い同値性を与える．

#### 合同関係，相似関係

ユークリッド空間で二点間の距離を変えない変換を合同変換という． 二つの図形 $X,Y$ が合同変換によって結びつくとき，$X,Y$ は合同な関係にあるという．

明らかに合同な関係は同値関係である． 同様に二つの図形が相似変換で結びつく際の相似な関係もまた同値関係である．

#### 合同式

整数集合に対して合同式による次の二項関係を考える．

$$ x\sim y \Leftrightarrow x\equiv y \pmod{n} \Leftrightarrow (\exists q\in\mathbb{Z}) (x-y = qn) $$

この二項関係が同値関係であることは次のとおり．

- $x\sim x$ は法 $n=0$ の場合であり真であるから，反射律を満たす．
- $x\sim y\Leftrightarrow (\exists q) (x-y = qn)\Leftrightarrow (\exists q) (y-x = (-q)n)$ であるから，$y\sim x$ が従うので，対称律を満たす．
- $x\sim y\land y\sim z$ ならば $x-z=x-y+y-z=qn+q^{\prime}n=(q+q^{\prime})n\Leftrightarrow x\sim z$ が従うから，推移律を満たす．

#### 偶数和の関係

整数集合に対して，和が偶数となる二項関係 $R$ を考える．

$$ xRy \Leftrightarrow x + y \in 2\mathbb{Z} $$

この二項関係が同値関係であることは次のとおり．

- $xRx\Leftrightarrow x+x=2x$ で偶数であるから，反射律を満たす．
- 加法は可換な演算であるから，対称律を満たす．
- $xRy\Leftrightarrow x+y\in 2\mathbb{Z}$ 且つ $yRz\Leftrightarrow y+z\in 2\mathbb{Z}$ に対して，$xRz\Leftrightarrow x+z=x+y+y+z-2y\in 2\mathbb{Z}$ で偶数となり，推移律を満たす．

#### 行列の相似関係

$n$ 次の正方行列全体からなる集合に対して次の二項関係 $R$ を考える． ここに $P$ は正則行列である．

$$ XRY \Leftrightarrow (\exists P)(P^{-1}XP = Y) $$

この二項関係が同値関係であることは次のとおり．

- 単位行列 $I$ は正則行列であり，$XRX\Leftrightarrow I^{-1}XI=X$ を保証するから，反射律を満たす．
- $XRY \Leftrightarrow (\exists P)(P^{-1}XP = Y)$ が真であるとき，$Q:=P^{-1}$ とすると $Q^{-1}YQ = X\Leftrightarrow YRX$ が従うから，対称律を満たす．
- $XRY\Leftrightarrow (\exists P)(P^{-1}XP = Y)$ 且つ $YRZ\Leftrightarrow (\exists Q)(Q^{-1}YQ = Z)$ に対して，$(PQ)^{-1}=Q^{-1}P^{-1}$ を用いれば $XRZ\Leftrightarrow (PQ)^{-1}X(PQ) = Z$ が従うから，推移律を満たす．

### 同値関係でない例

$(\textrm{R},\textrm{S},\textrm{T})$ と書いて二項関係の「反射律」「対称律」「推移律」に対する真偽値の三組を表すことにする．また真偽値を $T,F$ と書くことにする．

同値関係でない例を作ること自体は難しくはないが，例のための例になりがちである． なるべくそうでないような例を以下に挙げる．

#### $(\textrm{R},\textrm{S},\textrm{T})=(T,T,F)$

##### 可換行列の関係

$n$ 次の正方行列全体からなる集合を考えて，正方行列 $X,Y$ が可換であるという二項関係 $R$ を考える．

$$ XRY \Leftrightarrow [X,Y] = 0 $$

以下，$[\cdot,\cdot]$ を交換子，$0$ は零行列の意味で用いる．

- 任意の正方行列は自分自身と可換であるから，反射律を満たす．
- $XRY \Leftrightarrow [X,Y]=0$ ならば $YRX \Leftrightarrow [Y,X]=-[X,Y]=0$ であるから，対称律を満たす．
- 単位行列 $I$ (に比例する行列) とそれ以外の行列 $X,Y$ について，$XRI \Leftrightarrow [X,I]=0$ 且つ $IRY \Leftrightarrow [I,Y]=0$ であるが，一般には $XRY \Leftrightarrow [X,Y]\neq 0$ である．よって推移律を満たさない．

なお $[\cdot,\cdot]$ をより一般に Lie 括弧積としてみると，反射律と対称律は Lie 括弧積の定義から従う．

#### $(\textrm{R},\textrm{S},\textrm{T})=(T,F,T)$

##### 等号付き大小関係 $\leq$

実数集合に対して，二項関係 $\leq$ を考える．

- $x\leq x$ は常に真であるから，反射律を満たす．
- $0\leq 1$ は真であるが，$1\leq 0$ は偽であるから，対称律を満たさない．
- $x\leq y$ 且つ $y\leq z$ ならば，$x\leq z$ が常に真であるから，推移律を満たす．

#### $(\textrm{R},\textrm{S},\textrm{T})=(T,F,F)$

実数集合に対して，次の二項関係 $R$ を考える．

$$ xRy \Leftrightarrow x\neq y + 1 $$

- $xRx\Leftrightarrow x\neq x+1$ は常に真であるから，反射律を満たす．
- $0R1\Leftrightarrow 0\neq 1+1$ で真であるが，$1R0\Leftrightarrow 1\neq 0+1$ は偽である．よって対称律を満たさない．
- $2R0$ と $0R1$ は何れも真であるが，$2R1$ は偽である．よって推移律を満たさない．

#### $(\textrm{R},\textrm{S},\textrm{T})=(F,T,T)$

##### 平行関係 $\parallel$

位置ベクトルの集合に対して，二項関係 $\parallel$ を考える． 但し内積の絶対値が $1$ として定義する．

$$ \vec{x}\parallel\vec{y} \Leftrightarrow |\vec{x}\cdot\vec{y}| = 1 $$

- $\vec{x}\parallel\vec{x}$ は零ベクトルについて偽であるから，反射律を満たさない．
- $\vec{x}\parallel\vec{y}$ ならば $\vec{y}\parallel\vec{x}$ は常に真であるから，対称律を満たす．
- $\vec{x}\parallel\vec{y}$ 且つ $\vec{y}\parallel\vec{z}$ ならば $\vec{x}\parallel\vec{z}$ を満たすから，推移律を満たす．

対称律と推移律が真であるからといって，反射律は自動的に真とはならない． $\vec{x}\parallel\vec{y}$ について，$\vec{x}=\vec{0}$ ならば $\vec{x}\parallel\vec{y}$ を満たす $\vec{y}$ が存在しないからである．

#### $(\textrm{R},\textrm{S},\textrm{T})=(F,T,F)$

##### 奇数和の関係

整数集合に対して，和が奇数となる二項関係 $R$ を考える．

$$ xRy \Leftrightarrow x + y \in 2\mathbb{Z} + 1 $$

- $xRx=x+x=2x$ で偶数であるから，反射律を満たさない．
- 加法は可換な演算であるから，対称律を満たす．
- $0R1=0+1=1$ 且つ $1R2=1+2=3$ であるが，$0R2=0+2=2$ で偶数となり，推移律を満たさない．

##### 直交関係 $\perp$

位置ベクトルの集合に対して，二項関係 $\perp$ を考える． 但し内積が $0$ として定義する．

$$ \vec{x}\perp\vec{y} \Leftrightarrow \vec{x}\cdot\vec{y} = 0 $$

- $\vec{x}\perp\vec{x}$ は零ベクトルを除いて常に偽であるから，反射律を満たさない．
- $\vec{x}\perp\vec{y}$ ならば $\vec{y}\perp\vec{x}$ は常に真であるから，対称律を満たす．
- 同一平面上にある $\vec{x}\perp\vec{y}$ 且つ $\vec{y}\perp\vec{z}$ を満たす互いに異なる位置ベクトルを考える．すると $\vec{x},\vec{z}$ は逆向きに平行になって $\vec{x}\perp\vec{z}$ を満たさないから，推移律を満たさない．

##### 反可換行列の関係

$n$ 次の正方行列全体からなる集合を考えて，正方行列 $X,Y$ が反可換であるという二項関係 $R$ を考える．

$$ XRY \Leftrightarrow \{X,Y\} = 0 $$

以下，$\{\cdot,\cdot\}$ を反交換子，$0$ は零行列の意味で用いる．

- 冪零行列を除いて任意の正方行列は自分自身と反可換ではないから，反射律を満たさない．
- $XRY \Leftrightarrow \{X,Y\}=0$ ならば $YRX \Leftrightarrow \{Y,X\}=\{X,Y\}=0$ であるから，対称律を満たす．
- 零行列 $0$ とそれ以外の行列 $X,Y$ について，$XR0 \Leftrightarrow \{X,0\}=0$ 且つ $0RY \Leftrightarrow \{0,Y\}=0$ であるが，一般には $XRY \Leftrightarrow \{X,Y\}\neq 0$ である．よって推移律を満たさない．

##### JavaScript の等値演算子 `==`

二項関係として JavaScript の等値演算子 `==` を考える． 等値演算子の評価は非常に奇異な振る舞いを我々に見せてくれる． その仕様は次に述べられている．

- [Abstract Equality Comparison](https://www.ecma-international.org/ecma-262/#sec-abstract-equality-comparison)

これに従うと次の事柄が得られる．

- `[] == []` は偽である．よって反射律を満たさない．
- 左辺と右辺を対等に扱うという点では真であるため，対称律を満たす．
- `[] == 0` は真であり，且つ `0 == "0"` も真である．しかし `[] == "0"` は偽である．よって推移律を満たさない．

このふざけた関係演算子は次のリンクにあるスポンジ・ボブのパトリックに実によくあてはまる．

- [Old meme format, timeless JavaScript quirks](https://www.reddit.com/r/ProgrammerHumor/comments/88gniv/old_meme_format_timeless_javascript_quirks/)

F12 キーを押してみてほしい．Console が開かれることだろう． 上記のことが本当かどうか是非体験してほしい．

#### $(\textrm{R},\textrm{S},\textrm{T})=(F,F,T)$

##### 大小関係 $<$

実数集合に対して，二項関係 $<$ を考える．

- $x< x$ は常に偽であるから，反射律を満たさない．
- $0< 1$ は真であるが，$1< 0$ は偽であるから，対称律を満たさない．
- $x< y$ 且つ $y< z$ ならば，$x< z$ が常に真であるから，推移律を満たす．

##### 整除関係 $\mid$

整数集合に対して，二項関係 $\mid$ を考える． $b\mid a$ は $a=bq$ なる整数 $q$ が存在することを表す記号である．

- $0\mid 0$ は常に偽であるから，反射律を満たさない．
- $1\mid 2$ は真であるが，$1\mid 2$ は偽であるから，対称律を満たさない．
- $y\mid x$ 且つ $z\mid y$ ならば，$x=yq_1\land y=zq_2$ である．よって $x=(q_1q_2)z\mid$ を得る．$q_1q_2$ は再び整数となるから，$z\mid x$ は常に真とわかる．よって推移律を満たす．

#### $(\textrm{R},\textrm{S},\textrm{T})=(F,F,F)$

実数集合に対して，次の二項関係 $R$ を考える．

$$ xRy \Leftrightarrow x = y + 1 $$

- $xRx\Leftrightarrow x= x+1$ は常に偽であるから，反射律を満たさない．
- $xRy\Leftrightarrow x= y+1$ が真であるとき，$yRx\Leftrightarrow y=x+1=y+2$ となって偽である．よって対称律を満たさない．
- $xRy$ と $yRz$ が真であることから $x=z+2$ を得る．一方で，$xRz\Leftrightarrow x=z+1$ であるから，$xRz$ は偽である．よって推移律を満たさない．

## 参考

- [はじめての集合と位相](https://amzn.to/2MVwJTX)
- [例題で学ぶ集合と論理](https://amzn.to/2MXBYTf)
- [幾何学への新しい視点―不確定性と非可換時空 (幾何学をみる)](https://amzn.to/2KYIh8C)
- [数の生ひ立ち](https://amzn.to/2zlX9fS)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="同値関係";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
