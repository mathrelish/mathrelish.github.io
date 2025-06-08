---
title: "定積分 No.23"
date: 2018-09-24
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-18.png"
---

# 定積分 No.23

$$ \int_0^{\infty}dx \frac{\ln(x^2 + 1)}{x^2 + 1} = \pi \ln 2 $$

## 使用するトリック

次の被積分関数があったとする．

$$ \frac{f(x)}{x^2 + 1} $$

これは $x = \tan\theta$ なる置換積分を試みる例であるが，もし $f(x) = \ln(x^2 + 1)$ であったら，今の置換積分を行えば対数関数の中に三角関数が入り込むことになる．つまりオイラーの対数正弦積分が表れる．

よってこのような期待から定積分が求められそうである．

## 導出

求めるべき定積分について $x = \tan\theta$ なる置換積分を行う．

$$ I := \int_0^{\infty}dx \frac{\ln(x^2 + 1)}{x^2 + 1} = \int_0^{\frac{\pi}{2}}dx \ln(\tan^2\theta + 1) $$

ここで次が成り立った．

$$ \tan^2\theta + 1 = \frac{1}{\cos^2\theta} $$

よって次のようにオイラーの対数正弦積分に整理できる．

$$ I = \int_0^{\frac{\pi}{2}}dx \ln\frac{1}{\cos^2\theta} = -2\int_0^{\frac{\pi}{2}}dx \ln\cos\theta = \pi \ln 2 $$

これは所望の結果である．

## 感想戦

オイラーの対数正弦積分でどれだけの多項式を処理できるかの例である． 今回得た定積分は更なる結果を得るための足掛かりとなる．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
