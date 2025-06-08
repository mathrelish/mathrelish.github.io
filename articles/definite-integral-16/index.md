---
title: "定積分 No.16"
date: 2018-09-09
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-11.png"
---

# 定積分 No.16

$$ \int_0^1 dx \frac{\ln (x+1)}{x^2 + 1} = \frac{\pi}{8}\ln 2 $$

## 使用するトリック

まず被積分関数が $\frac{1}{x^2 + 1}$ を含んでいるので次の置換積分によって分母を約せる．

$$ x = \tan\theta $$

すると対数関数に三角関数が入り込んだ被積分関数となるが，積分領域が有限であることと三角関数を含んでいることから，積分変数のフリッピングを試行してみる．

## 導出

被積分関数を $x = \tan\theta$ で置換積分して整理すると次を得る．

$$ I := \int_0^1 dx \frac{\ln (x+1)}{x^2 + 1} = \int_0^{\frac{\pi}{4}} d\theta \ln (\tan\theta + 1) $$

次に積分変数のフリッピングを行って，三角関数の加法定理を用いて整理すれば次を得る．

$$ I = \int_0^{\frac{\pi}{4}} d\theta \ln\left[ \tan\left(\frac{\pi}{4} - \theta\right) + 1\right] = \int_0^{\frac{\pi}{4}} d\theta \ln\left[ \frac{1 - \tan\theta}{1 + \tan\theta} + 1\right] = \frac{\pi}{4}\ln 2 - I $$

よって $I$ について整理すれば所望の結果を得る．

## 感想戦

今回の定積分はかつて 1844 年に Joseph Alfred Serret (1819-1885) により解かれたことから，Serre の積分とよばれる定積分である．

[Joseph Alfred Serret](https://en.wikipedia.org/wiki/Joseph_Alfred_Serret)

Serre の積分は次のように一般化できる．

$$ I_a := \int_0^a dx \frac{\ln (x+a)}{x^2 + a^2} = \frac{\pi}{8a}\ln(2a^2) ~~ (a>0) $$

導出は $I_1$ に対して，$x=\frac{t}{a}$ なる置換積分を行って整理する．それは次のとおり．

$$ I_1 = \int_0^a \frac{dt}{a} \frac{\ln\left(\frac{t}{a} + 1\right)}{\frac{t^2}{a^2} + 1} = aI_a - \frac{\pi}{4}\ln a $$

これから $I_a$ について整理すればよい．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
