---
title: "定積分 No.24"
date: 2018-09-24
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-19.png"
---

# 定積分 No.24

$$ \int_0^1 dx \frac{\ln(x + \frac{1}{x})}{x^2 + 1} = \frac{\pi}{2} \ln 2 $$

## 使用するトリック

示すべき定積分の被積分関数は次の双対な変数変換に対して積分領域は移り変わるが被積分関数自体は不変である．

$$ y = \frac{1}{x} $$

この事実と以下で得た結果を合わせることで示す．

- [定積分 No.2](https://mathrelish.com/calculation/definite-integral-2)
- [定積分 No.23](https://mathrelish.com/calculation/definite-integral-23)

具体的には 分割された二つの積分領域は次の変数変換で対応づく双対な関係にある．

これを用いて上手く題意の定積分を引きずり出す．

## 導出

示すべき定積分について，$y=\frac{1}{x}$ なる置換積分を行って次を得る．

$$ I := \int_0^1 dx \frac{\ln(x + \frac{1}{x})}{x^2 + 1} = \int_1^{\infty} dx \frac{\ln(x + \frac{1}{x})}{x^2 + 1} $$

さて[定積分 No.23](https://mathrelish.com/calculation/definite-integral-23)で示したように次が成立した．

$$ \int_0^{\infty}dx \frac{\ln(x^2 + 1)}{x^2 + 1} = \pi \ln 2 $$

この定積分についても，$y=\frac{1}{x}$ なる置換積分を行って次を得る．

$$ \int_0^{\infty}dx \frac{\ln(x^2 + 1)}{x^2 + 1} = \int_0^{\infty} dx \frac{\ln\left(\frac{1}{x^2} + 1\right)}{x^2 + 1} = \int_0^{\infty} dx \frac{\ln(x + \frac{1}{x})}{x^2 + 1} - \int_0^{\infty} dx \frac{\ln x}{x^2 + 1} $$

ここで第二項は[定積分 No.2](https://mathrelish.com/calculation/definite-integral-2)で示したように $0$ となるから落ちる． 一方で第一項は冒頭で述べたことを合わせて次のようになる．

$$ \int_0^{\infty} dx \frac{\ln(x + \frac{1}{x})}{x^2 + 1} = 2I $$

よって我々は次を得る．

$$ I = \frac{1}{2}\int_0^{\infty}dx \frac{\ln(x^2 + 1)}{x^2 + 1} = \frac{\pi}{2} \ln 2 $$

これは所望の結果である．

## 感想戦

今回得た定積分は双対な変数変換を見事に用いて解かれた結果だった． 実は暗にカタラン定数 $G$ が相殺している．

$$ \int_0^{\infty} dx \frac{\ln x}{x^2 + 1} = \int_0^1 dx \frac{\ln x}{x^2 + 1} + \int_1^{\infty} dx \frac{\ln x}{x^2 + 1} = -G + G = 0 $$

[Catalan's constant](https://en.wikipedia.org/wiki/Catalan%27s_constant)

このように上手くカタラン定数がでないように定積分を求めているところが繊細である．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
