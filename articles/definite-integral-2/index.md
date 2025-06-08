---
title: "定積分 No.2"
date: 2018-08-31
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-1.png"
---

# 定積分 No.2

$$ \int_0^{\infty} dx \frac{\ln x}{1 + x^2} = 0 $$

## 使用するトリック

積分領域の分割を考える．

$$ \int_0^{\infty} dx f(x) = \int_0^1 dx f(x) + \int_1^{\infty} dx f(x) $$

このとき次が成り立つ．

$$ \int_0^a dx f(x) = - \int_a^{\infty} dx f(x) \Leftrightarrow \int_0^{\infty} dx f(x) = 0 $$

## 導出

変数変換 $t=\frac{1}{x}$ を行って，次のように定積分を評価する．

$$ \int_0^1 dx \frac{\ln x}{1 + x^2} = \int_{\infty}^1 \left(-\frac{dt}{t^2}\right) \frac{\ln \frac{1}{t}}{1 + \frac{1}{t^2}} = -\int_1^{\infty} dt \frac{\ln t}{1 + t^2} $$

よって右辺を左辺に移項して，積分領域を統合すれば次を得る．

$$ \int_0^{\infty} dx \frac{\ln x}{1 + x^2} = 0 $$

## 感想戦

対数関数があることも考慮して，負符号を出したいために変数変換として逆数をとっている．また逆数が自身に等しい数は $1$ のみであるから $1$ を堺に積分領域を分割できる． 被積分関数が積分領域の内部に特異点がないことも助かった．

さてより一般的に次の定積分を考えてみる．

$$ I := \int_0^{\infty} dx \frac{\ln x}{b^2 + x^2} $$

これは最早 $0$ にはならない．つまり積分領域の分割を意図した計算は途中で止まる． ほんの少しの根気と異なるアプローチが必要だが，ここで得た結果は無駄にはならない．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
