---
title: "定積分 No.10"
date: 2018-09-01
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-5.png"
---

# 定積分 No.10

$$ \int_0^{\infty} dx \frac{1}{1 + e^{ax}} = \frac{\ln 2}{a} $$

## 使用するトリック

指数関数だけの積分は次のように $t=e^x$ (指数置換) による置換積分で $t$ だけの積分にできる．

$$ \int dx f(e^x) = \int dt \frac{f(t)}{t} $$

## 導出

$t=e^{ax}$ による置換積分を行って次の評価を得る．

$$ I := \int_0^{\infty} dx \frac{1}{1 + e^{ax}} = \frac{1}{a}\int_1^{\infty} dt \frac{1}{t(1+t)} $$

これで後は部分分数分解を行って簡約していけばよい．

$$ I = \frac{1}{a}\int_1^{\infty} dt \left(\frac{1}{t} - \frac{1}{1+t}\right) = \frac{\ln 2}{a} $$

## 感想戦

双曲線関数は定義に立ち返れば指数関数だけの積分であるから，これもまた同様に易しいものだと確かに推論できる．加えて指数関数だけの関数を偶関数と奇関数に分けるということは，双曲線関数で表すと同義であるから，今回のような話は双曲線関数が計算の基底のような役目を果たしているという理解ができる．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
