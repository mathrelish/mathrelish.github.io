---
title: "定積分 No.7"
date: 2018-09-01
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-2.png"
---

# 定積分 No.7

$$ \int_1^{\infty} dx \frac{1}{(x+a)\sqrt{x-1}} = \frac{\pi}{\sqrt{a+1}} $$

## 使用するトリック

平方根がある場合は置換積分によって次数を上げて様子を見るというのが，まずはすべきことであろう．

## 導出

次の変数変換を行う．

$$ t^2 = x-1 $$

これによって定積分は次のように変形される．

$$ \int_1^{\infty} dx \frac{1}{(x+a)\sqrt{x-1}} = 2\int_0^{\infty} dt \frac{1}{t^2 + (a+1)} $$

こうして得られた被積分関数は逆正接関数を原始関数に持つことが容易にわかる．

$$ \int dt \frac{1}{t^2 + c^2} = \frac{1}{c}\arctan\frac{t}{c} $$

よって次のように所望の結果を得る．

$$ \int_1^{\infty} dx \frac{1}{(x+a)\sqrt{x-1}} = 2\left.\frac{1}{\sqrt{a+1}}\arctan\frac{t}{\sqrt{a+1}}\right|_0^{\infty} = \frac{\pi}{\sqrt{a+1}} $$

## 感想戦

$a=-1$ の場合には特異だとわかる．これは元の被積分関数でも積分領域の端点で特異性が表れていることからも予期できる．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
