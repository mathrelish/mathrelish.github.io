---
title: "定積分 No.22"
date: 2018-09-24
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-17.png"
---

# 定積分 No.22

$$ \int_0^{\frac{\pi}{2}}dx \ln(\mathrm{sinc} x) = \frac{\pi}{2}(1 - \ln\pi) $$

## 使用するトリック

[定積分 No.21](https://mathrelish.com/mathematics/definite-integral-21)で導出したオイラーの対数正弦積分を用いる．

なお被積分関数の対数中の関数は $\mathrm{sinc}$ とよばれる関数で次のように定義される．誤植ではない．

$$ \mathrm{sinc} x := \frac{\sin x}{x} $$

[sinc関数](https://ja.wikipedia.org/wiki/Sinc%E9%96%A2%E6%95%B0)

## 導出

示すべき定積分は次のように変形できる．

$$ I := \int_0^{\frac{\pi}{2}}dx \ln(\sin x) - \int_0^{\frac{\pi}{2}}dx \ln x $$

第一項はオイラーの対数正弦積分に他ならない．また第二項は初等的である． つまり次を直ちに得る．

$$ I = \frac{\pi}{2}\ln\frac{1}{2} - \left.\left[ x\ln x - x \right]\right|_0^{\frac{\pi}{2}} = \frac{\pi}{2}(1 - \ln\pi) $$

これは所望の結果である．

## 感想戦

オイラーの対数正弦積分は被積分関数として $\ln f(x)$ のようなものをとるとき，三角関数の恒等式と対数の性質から，$f$ が任意の三角関数であっても，位相が線型ならば対数正弦積分の適当な合成に帰着できるという点で有用である．よって $f$ として三角関数以外の多項式が混じった場合が興味深いとわかる．

今回の定積分はそのような中で自明な場合を扱っているといえる．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
