---
title: "定積分 No.12"
date: 2018-09-01
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-7.png"
---

# 定積分 No.12

$$ \int_{-\infty}^{\infty} dx \frac{1}{\cosh x} = \pi $$

## 使用するトリック

双曲線関数は指数関数を偶関数や奇関数に分解した関数であるから，[定積分 No.10](https://mathrelish.com/mathematics/definite-integral-10) で述べたとおり，$t=e^x$ と置換積分すれば，それで事足りることが保証されている．

## 導出

直ちに次を得る．

$$ \int_{-\infty}^{\infty} dx \frac{1}{\cosh x} = \int_{-\infty}^{\infty} dx \frac{1}{\frac{1}{2}(e^x + e^{-x})} = 2\int_0^{\infty} dt \frac{1}{t^2 + 1} = 2\arctan\infty = \pi $$

## 感想戦

計算自体については特に感慨深いものがない．敢えて言えば被積分関数は $\mathrm{sech}$ であるから，その他の双曲線関数に変えたときにどうなるかが興味を持つ．答えとしては次のとおり．

$$ \begin{eqnarray} \mathrm{p.v.}\int_{-\infty}^{\infty} dx \sinh x &=& 0 \\ \int_{-\infty}^{\infty} dx \cosh x &=& \infty \\ \mathrm{p.v.}\int_{-\infty}^{\infty} dx \tanh x &=& 0 \\ \mathrm{p.v.}\int_{-\infty}^{\infty} dx \mathrm{csch} x &=& 0 \\ \int_{-\infty}^{\infty} dx \mathrm{sech} x &=& \pi \\ \mathrm{p.v.}\int_{-\infty}^{\infty} dx \coth x &=& 0 \end{eqnarray} $$

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
