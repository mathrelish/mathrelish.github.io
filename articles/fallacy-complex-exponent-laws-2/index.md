---
title: "誤謬：複素数冪の指数法則 2"
date: 2020-10-07
categories: 
  - "mathematical-fallacy"
tags: 
  - "complex-function"
coverImage: "fallacy-complex-exponent-laws-2.png"
---

# 誤謬

　

次の指数法則は複素数の冪についていつでも成り立つ．

$$ (z^{\alpha})^{\beta} = (z^{\beta})^{\alpha} = z^{\alpha\beta} $$

　

## 判定方法

指数 $\alpha$ と $\beta$ が共に整数であるか， もしくは主枝をとった場合は，表題の指数法則はいつでも成り立つ． それ以外の場合は特別な場合を除いて保証されない．

その特別な場合の中には注目すべき場合があり，コメントで詳しく述べる．

## 反例

後で述べるように，$k\in\mathbb{Z}$ で，$\alpha\in\mathbb{C}\setminus\mathbb{Q}$ について，以下の計算となる．

$$ (z^{\alpha})^k = z^{k\alpha} $$

一方で次が得られる．

$$ (z^k)^{\alpha} = e^{2\pi i\alpha m} z^{\alpha k} $$

つまり主枝 $m=0$ でない場合には一致しない． またもし $\alpha\in\mathbb{Q}$ である場合には， 主枝の他にも，既約分数の分母を相殺する分枝を選んでいれば一致するが，それ以外は一致しない．

## コメント

### 基本事項

複素数の冪関数は次のように定義された．

$$ z^{\alpha} := e^{\alpha\log z} $$

そして複素対数関数は次のように定義された．

\begin{eqnarray} \log z &:=& \{\ln |z| + i\arg z \mid z\neq 0 \}, \\ \arg z &:=& \{\mathrm{Arg} z + 2\pi n \mid z\neq 0 \land n\in\mathbb{Z}\}, \\ \mathrm{Log} z &:=& \ln|z| + i\mathrm{Arg} z \end{eqnarray}

ここで多価性は偏角部分 $\arg z$ に表れている． これらを基礎に丁寧に見ていけば，自ずと誤謬が明らかとなる．

今回は更に以下の等式が重要になる．

\begin{eqnarray} \log z^{\alpha} &=& \{\alpha \log z + 2\pi i n \mid z\neq 0 \land n\in\mathbb{Z}\}, \\ \log z^{\frac{1}{k}} &=& \frac{1}{k}\log z ~~ (k\in\mathbb{Z}) \end{eqnarray}

[誤謬：複素対数関数の対数法則１](https://mathrelish.com/mathematical-fallacy/fallacy-complex-logarithm-laws-1)

### $(z^{\alpha})^{\beta}$ と $(z^{\beta})^{\alpha}$ そして $z^{\alpha\beta}$ について

$(z^{\alpha})^{\beta}$ と $z^{\alpha\beta}$ を評価すると次のようになる．

\begin{eqnarray} (z^{\alpha})^{\beta} &=& e^{\alpha\beta\log z + 2\pi i\beta n}, \\ (z^{\beta})^{\alpha} &=& e^{\alpha\beta\log z + 2\pi i\alpha m}, \\ z^{\alpha\beta} &=& e^{\alpha\beta\log z} \end{eqnarray}

こうして次を得る．つまり何れも一般には一致しない．

\begin{eqnarray} (z^{\alpha})^{\beta} &=& e^{2\pi i\beta n}z^{\alpha\beta}, \\ (z^{\beta})^{\alpha} &=& e^{2\pi i\alpha m}z^{\alpha\beta} \end{eqnarray}

この結果から特に次が成り立つとわかる．

いかなる分枝についても次が成り立つ．

$$ (z^{\alpha})^k = z^{k\alpha} ~~ (k\in\mathbb{Z},\alpha\in\mathbb{C}) $$

しかし次が成立することはその限りでなく，指数の順序を安易に変更できない．

$$ (z^{\alpha})^k = (z^k)^{\alpha} ~~ (k\in\mathbb{Z},\alpha\in\mathbb{C}) $$

証明略■

### 注目すべき特別な場合

いかなる分枝についても次が成り立つ．

$$ (z^{\frac{1}{k}})^{\alpha} = z^{\frac{\alpha}{k}} ~~ (k\in\mathbb{Z},\alpha\in\mathbb{C}) $$

複素数冪関数の定義から次を得る．

$$ (z^{\frac{1}{k}})^{\alpha} = e^{\alpha\log z^{\frac{1}{k}}} $$

ここで $k\in\mathbb{Z}$ より，分枝の選択に関わらず，$\log z^{\frac{1}{k}} = \frac{1}{k}\log z $ が成り立つから次が得られる．

$$ e^{\alpha\log z^{\frac{1}{k}}} = e^{\frac{\alpha}{k}\log z} = z^{\frac{\alpha}{k}} $$

これは示したいことだった．■

いかなる分枝についても次が成り立つ．

$$ \frac{1}{z^{\alpha}} = \left(\frac{1}{z}\right)^{\alpha} $$

いかなる分枝についても次が成り立つことが既に示されている．

\begin{eqnarray} (z^{\alpha})^k &=& z^{k\alpha} ~~ (k\in\mathbb{Z},\alpha\in\mathbb{C}), \\ (z^{\frac{1}{l}})^{\alpha} &=& z^{\frac{\alpha}{l}} ~~ (l\in\mathbb{Z},\alpha\in\mathbb{C}) \end{eqnarray}

これらの右辺が一致するのは $k=1/l=\pm 1$ の場合である． 非自明な場合は $-1$ の場合であり，それは題意の主張に他ならない．■

## 参考

[誤謬：複素数冪の指数法則 1](https://mathrelish.com/mathematical-fallacy/fallacy-complex-exponent-laws-1)
