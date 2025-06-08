---
title: "定積分 No.19"
date: 2018-09-21
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-14.png"
---

# 定積分 No.19

$$ I_n(\alpha) := \int_0^{\pi} dx \frac{\cos(nx) - \cos(n\alpha)}{\cos x - \cos\alpha} = \pi\frac{\sin(n\alpha)}{\sin\alpha} ~~ (n=0,1,2,3,\cdots) $$

## 使用するトリック

今回のように $n$ でラベルされた数式は，まず $n$ について素直に場合分けなく連番された結果を得ると予想して漸化式を立式できないかを考えてみるのも手である． ここに素直でない場合分けのある結果とは，例えば $n$ が偶数と奇数で違った一般解を持つようなものである．

今回の定積分は漸化式を立式することによって求められる例である．

漸化式の立式は異なる $n$ についての何らかの恒等式を手がかりに見出すことになる． 今回の場合は次のよう[三角関数の和積の公式](https://mathrelish.com/mathematics/trigonometric-addition-formulas)から連続する三つの $n$ についての漸化式を見出すことになる．

$$ \cos[(n+1)\phi] + \cos[(n-1)\phi] = 2 \cos(n\phi) \cos\phi $$

これから次の線型な漸化式が得られそうだと期待できる．

$$ A I_{n+1}(\alpha) + B I_n(\alpha) + C I_{n-1}(\alpha) = Q $$

ここで「線型」というのは漸化式を満たす解の任意の線型結合もまた漸化式を満たす解となることをいい，従って一般解は線型結合で与えられる．このとき線型結合の係数は初期条件から決められる．

$A,B,C,Q$ を見出すことで，上記の線型な漸化式を手にすることができたら，後は漸化式を解きさえすれば，定積分が求められたことになる．

## 導出

まず明らかに次のことが直ちにわかる．

$$ I_0(\alpha) = 0,~ I_1(\alpha) = \pi $$

これらはこれから導出する漸化式の初期条件となる．

我々は次の恒等式に基づいて漸化式の立式を試みる．

$$ \cos[(n+1)\phi] + \cos[(n-1)\phi] = 2 \cos(n\phi) \cos\phi $$

被積分関数は対称な形をしており，この恒等式から次の漸化式を見出すことができる．

$$ I_{n+1}(\alpha) - 2\cos\alpha I_n(\alpha) + I_{n-1}(\alpha) = 0 $$

この漸化式の解として次を仮定する．

$$ I_n(\alpha) = Ce^{sn} $$

ここに $C,s$ は $\alpha$ に依存するところの何らかの定数である． 漸化式に上記の解を代入して，二次方程式 (特性方程式) を解くこととなり，整理すると次を得る．

$$ e^s = e^{\pm i\alpha} $$

よって一般解は次の線型結合だとわかる．

$$ I_n(\alpha) = C_+ e^{+i\alpha n} + C_- e^{-i\alpha n} $$

冒頭の初期条件にこれは従うべきであるから，係数は次のように直ちに求められる．

$$ C_- = -C_+,~ C_+ = \frac{\pi}{2i\sin\alpha} $$

これを代入して整理すると所望の結果に至る．

## 感想戦

定積分を求めるのに，置換積分や部分積分などの単純な式変形以外の方法を用いている点が特色である． 今回は与えられた定積分について解く形で，漸化式を利用したが，何らかの定積分を一般化する技法としても利用できる．

また導出の過程で解いた特性方程式の解が大変綺麗な形で表れており，美しいといえるだろう．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
