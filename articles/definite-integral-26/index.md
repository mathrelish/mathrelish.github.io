---
title: "定積分 No.26"
date: 2018-09-25
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-21.png"
---

# 定積分 No.26

$$ \int_0^1 dx \frac{1 - x}{1 + x + x^2} = \frac{1}{2}\left( \frac{\pi}{\sqrt{3}} - \ln 3 \right) $$

## 使用するトリック

基本に忠実に計算するのみで，目立ったトリックはない．

## 導出

まず求めるべき定積分の被積分関数について分母を平方完成する．

$$ I := \int_0^1 dx \frac{1 - x}{1 + x + x^2} = \int_0^1 dx \frac{1 - x}{\left( x + \frac{1}{2} \right)^2 + \frac{3}{4}} $$

次に平方完成で定数だけずれた分を置換積分によって吸収して整える．

$$ I = \int_{\frac{1}{2}}^{\frac{3}{2}} dx \frac{\frac{3}{2} - x}{x^2 + \frac{3}{4}} = \frac{3}{2}\int_{\frac{1}{2}}^{\frac{3}{2}} dx \frac{1}{x^2 + \frac{3}{4}} - \int_{\frac{1}{2}}^{\frac{3}{2}} dx \frac{x}{x^2 + \frac{3}{4}} =: I_1 + I_2 $$

ここで最右辺で定めた各定積分を順に求めると次のとおり．

$$ I_1 = \frac{3}{2}\frac{1}{\frac{\sqrt{3}}{2}} \left. \arctan \frac{x}{\frac{\sqrt{3}}{2}} \right|_{\frac{1}{2}}^{\frac{3}{2}} = \frac{\pi}{2\sqrt{3}} $$

$$ I_2 = - \int_1^3\frac{dt}{2}\frac{1}{t} = -\frac{1}{2}\left.\ln t\right|_1^3 = -\frac{1}{2}\ln3 $$

$I_2$ の計算では $t = x^2 + \frac{3}{4}$ なる置換積分を行った．

以上の各結果を合わせれば所望の結果に至る．

## 感想戦

基本に忠実に．慌てず一つずつ．着実に計算していく．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
