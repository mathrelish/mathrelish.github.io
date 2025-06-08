---
title: "定積分 No.17"
date: 2018-09-21
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-12.png"
---

# 定積分 No.17

$$ \int_0^{\infty} dx \prod_{k=1}^n \frac{1}{x^2 + a_k^2} = \frac{\pi}{2}\sum_{k=1}^n\frac{c_k}{a_k} ~~ ((\forall k)(a_k\neq 0) \land (i\neq j \Rightarrow a_i \neq a_j)) $$

但しここで $c_k$ は次のように与えられる．

$$ c_k := \prod_{j=1}^n\gamma_{j,k} ~~\mathrm{where}~ \gamma_{j,k} := \begin{cases} \frac{1}{a_j^2 - a_k^2} & (j\neq k) \\ 1 & (j=k) \end{cases} $$

## 使用するトリック

部分分数分解を頑なに行うだけになる． 非常に対称な形をした被積分関数なので，鮮やかに部分分数分解の展開係数が求められる． その過程は留数を求めるような片鱗を見せてくれる．

## 導出

被積分関数を次のように部分分数分解する．

$$ f(x) := \prod_{k=1}^n \frac{1}{x^2 + a_k^2} = \sum_{k=1}^n \frac{c_k}{x^2 + a_k^2} $$

両辺に $(x^2 + a_k^2)$ を乗じ，$\lim_{x\rightarrow ia_k}$ をとって次を得る．

$$ \lim_{x\rightarrow ia_k} f(x) = c_k $$

そこでこの左辺を評価すれば部分分数分解の展開係数 $c_k$ がわかるから，これを行うと次のとおり．

$$ c_k = \lim_{x\rightarrow ia_k} f(x) = \prod_{j=1}^n\gamma_{j,k} $$

よって求める定積分は次のように評価できる．

$$ I := \int_0^{\infty} dx \prod_{k=1}^n \frac{1}{x^2 + a_k^2} = \sum_{k=1}^n c_k \int_0^{\infty} dx \frac{1}{x^2 + a_k^2} $$

最右辺の定積分は逆正接関数であるから，もう求められたとわかる． それを実行すると次のとおり．

$$ I = \sum_{k=1}^n \frac{c_k}{a_k} \left.\arctan \frac{x}{a_k} \right|_0^{\infty} = \frac{\pi}{2} \sum_{k=1}^n \frac{c_k}{a_k} $$

## 感想戦

今回の定積分は場の量子論での伝播関数とよく似た式になっている． そこでの計算では複素関数論が必須で，今回のように虚数を用いた極限というものが ad hoc なものではなくなる． ひとまずは今得られた結果の応用を次のとおり考えてみる．

$n=2$ の場合を特に考えると $c_2=-c_1$ および $c_1=\frac{1}{a_2^2 - a_1^2}$ より，次のように整理できる．

$$ \int_0^{\infty} dx \prod_{k=1}^2 \frac{1}{x^2 + a_k^2} = \frac{\pi}{2} \frac{1}{a_1a_2(a_1+a_2)} $$

これから次の定積分を直ちに求められる．

$$ \int_0^{\infty} dx \frac{1}{x^4 + 2x^2\cosh(2\alpha) + 1} = \int_0^{\infty} dx \frac{1}{(x^2 + e^{2\alpha})(x^2 + e^{-2\alpha})} = \frac{\pi}{4\cosh\alpha} ~~ (\forall\alpha\in\mathbb{C}) $$

すると次の定積分も求められる．

$$ \int_0^{\infty} dx \frac{1}{x^4 + 2x^2\cos(2\alpha) + 1} = \frac{\pi}{4\cos\alpha} $$

但しここで次を用いた．

$$ \cosh (i\alpha) = \cos\alpha $$

複素関数として拡張された三角関数や双曲線関数を用いることなしに，実積分の範疇で示すには少し大変である． この導出は次回の定積分で行う．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
