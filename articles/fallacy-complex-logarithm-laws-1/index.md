---
title: "誤謬：複素対数関数の対数法則１"
date: 2020-10-07
categories: 
  - "mathematical-fallacy"
tags: 
  - "complex-function"
coverImage: "fallacy-complex-logarithm-laws-1.png"
---

# 誤謬

　

次の対数法則は複素数の冪についていつでも成り立つ．

$$ \log z^{\alpha} = \alpha \log z ~~ (z\neq 0 \land \alpha\in\mathbb{C}) $$

　

## 判定方法

$$ \log z^{\alpha} = \{\alpha \log z + 2\pi i n \mid z\neq 0 \land n\in\mathbb{Z}\} $$

上記が正しい評価式であるが，これから $\log z^{\alpha} = \alpha \log z$ となるためには主枝 ($n=0$) をとっているかいないかで判定すればよいとわかる．

しかし主枝でない場合も以下の特別な場合に限っては複素数冪関数からの多価性が消えて， 実対数関数と同じ対数法則を満たす．

$$ \log z^{\frac{1}{k}} = \frac{1}{k}\log z ~~ (k\in\mathbb{Z}\land z\neq 0) $$

これは注目すべき特別な場合であって，コメントで詳しく述べる．

## 反例

「反例は主枝を取らない場合である．」と言い切りたいところだが， 次は主枝を選択しない場合でも成り立つため，反例にはならない．

$$ \log \frac{1}{z} = \log z^{-1} = -\log z $$

## コメント

### 基本事項

複素数の冪関数は次のように定義された．

$$ z^{\alpha} := e^{\alpha\log z} $$

そして複素対数関数は次のように定義された．

\begin{eqnarray} \log z &:=& \{\ln |z| + i\arg z \mid z\neq 0 \}, \\ \arg z &:=& \{\mathrm{Arg} z + 2\pi n \mid z\neq 0 \land n\in\mathbb{Z}\}, \\ \mathrm{Log} z &:=& \ln|z| + i\mathrm{Arg} z \end{eqnarray}

ここで多価性は偏角部分 $\arg z$ に表れている． これらを基礎に丁寧に見ていけば，自ずと誤謬が明らかとなる．

### 正しい評価

$\log f(z)$ について複素対数関数は絶対値と偏角部分の分解からまず行う．

$$ \log f(z) = \ln |f(z)| + i\arg(f(z)) $$

今回は $\log z^{\alpha}$ なので，次のようになる．

$$ \log z^{\alpha} = \ln |z^{\alpha}| + i\arg(z^{\alpha}) $$

つまり $z^{\alpha}$ の絶対値と偏角部分を求めればよい． このために次の計算を行う．

$$ z^{\alpha} = e^{\alpha \log z} $$

ここで指数部分を実部と虚部の和に分ければ，絶対値と偏角部分が確定する． そこで $\alpha=\xi+i\eta$ と $\alpha$ の実部と虚部を考える． すると直ちに次が得られる．

$$ z^{\alpha} = [|z|^{\xi}e^{-\eta\arg z}] e^{i(\eta\ln|z| + \xi\arg z)} $$

よって次を得る．

\begin{eqnarray} |z^{\alpha}| &=& |z|^{\xi}e^{-\eta\arg z}, \\ \arg(z^{\alpha}) &=& \{\eta\ln|z| + \xi\arg z + 2\pi n \mid n\in\mathbb{Z}\} \end{eqnarray}

これを $\log z^{\alpha} = \ln |z^{\alpha}| + i\arg(z^{\alpha})$ 代入すれば，次の計算ができる． 但し集合記法をここでは省略し，あたかも一つの分枝を選んだような略記を行う．

$$ \log z^{\alpha} = \xi\ln |z| - \eta\arg z + i[\eta\ln|z| + \xi\arg z + 2\pi n] = \alpha\log z + 2\pi i n $$

上手く元の $\alpha$ や $\log z$ に戻ってくれる点がありがたいところである． というわけで，こうして正しい評価を得ることができた．

### 注目すべき特別な場合

複素対数関数の対数法則は主枝以外では複素数冪関数の多価性を被るようにみえるが， 実は以下のように特別な場合に限ってはそれが消えることになる．

$$ \log z^{\frac{1}{k}} = \frac{1}{k}\log z ~~ (k\in\mathbb{Z}\land z\neq 0) $$

$$ \log z = \{\ln |z| + i(\mathrm{Arg} z + 2\pi m) \mid m\in\mathbb{Z}\land z\neq 0 \} $$

上記を用いて，一般の $\alpha\in\mathbb{C}$ に対して，まず次を得ておく．

$$ \log z^{\alpha} = \left\{\alpha \left[\log z + i\mathrm{Arg} z + 2\pi i \left(m + \frac{n}{\alpha}\right)\right] \mid n,m\in\mathbb{Z}\land z\neq 0\right\} $$

すると題意にある $\alpha=1/k$ なる冪を考えると，$l:=m+n/\alpha = m+kn \in\mathbb{Z}$ である． よって次を得る．

$$ \log z^{\alpha} = \left\{\frac{1}{k} \left[\log z + i(\mathrm{Arg} z + 2\pi l) \right] \mid l\in\mathbb{Z}\land z\neq 0\right\} $$

これは即ち次を得たことに他ならない．

$$ \log z^{\alpha} = \frac{1}{k} \log z $$

故に示された．■

以上から次もまた得られた．

$$ \log\frac{1}{z} = -\log z $$

これはよく出てきてもおかしくない計算だが， 主枝を選ぶこととは無関係に成立する計算になっている．

よってその事情を知っていないと，この式変形を仮定するために， 「意図せず」主枝を選ぶという必要以上の仮定を置いてしまうことになりかねない．

## 参考

[誤謬：複素数冪の指数法則 1](https://mathrelish.com/mathematical-fallacy/fallacy-complex-exponent-laws-1)
