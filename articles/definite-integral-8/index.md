---
title: "定積分 No.8"
date: 2018-09-01
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-3.png"
---

# 定積分 No.8

$$ \int_0^{\infty} dx \ln\left(1 + \frac{a^2}{x^2}\right) = a\pi $$

## 使用するトリック

対数関数は微分すると有理関数となる．そこで対数関数が被積分関数にあるときは部分積分を用いて，対数関数を追い出すということを行う．ここに部分積分とは次のように積の微分を積分して得られる恒等式のことをいう．

$$ d(uv) = udv + vdu $$

$$ \int_a^b udv = \left.uv\right|_a^b - \int_a^b dx vdu $$

必然的に対数関数が絡んだ極限値の計算が必要となる． よくあるのは次の極限値計算であり，ロピタルの定理を用いる．

$$ \lim_{x\rightarrow +0}x\ln x = \lim_{x\rightarrow +0}\frac{\ln x}{\frac{1}{x}} = \lim_{x\rightarrow +0}\frac{\frac{1}{x}}{-\frac{1}{x^2}} = -\lim_{x\rightarrow +0}x = 0 $$

## 導出

$$ (u,v) := \left( \ln\left(1 + \frac{a^2}{x^2}\right), x \right) $$

上記のように置いて部分積分を行って次を得る．

$$ \int_0^{\infty} dx \ln\left(1 + \frac{a^2}{x^2}\right) = \left.x\ln\left(1 + \frac{a^2}{x^2}\right)\right|_0^{\infty} + 2a^2 \int_0^{\infty}dx \frac{1}{x^2 + a^2} $$

ここで第一項は次のとおり $0$ となる．

$$ \lim_{x\rightarrow +0}x\ln\left(1 + \frac{a^2}{x^2}\right) = \lim_{x\rightarrow \infty}x\ln\left(1 + \frac{a^2}{x^2}\right) = 0 $$

何故ならばそれぞれ次のとおり．

$\lim_{x\rightarrow +0}$ 側については次のとおり．

$$ \lim_{x\rightarrow +0}x\ln\left(1 + \frac{a^2}{x^2}\right) = \lim_{x\rightarrow +0}x\ln\frac{a^2}{x^2} = \lim_{x\rightarrow +0}[x\ln a^2 - 2x\ln x] = -2\lim_{x\rightarrow +0}x\ln x = 0 $$

$\lim_{x\rightarrow \infty}$ 側については次のとおり．

$$ \lim_{x\rightarrow \infty}x\ln\left(1 + \frac{a^2}{x^2}\right) = \lim_{x\rightarrow \infty}x\sum_{k=1}^{\infty}\frac{(-)^{k+1}}{k}\left(\frac{a^2}{x^2}\right)^k = \lim_{x\rightarrow \infty} \left(\frac{a^2}{x} - \frac{1}{2}\frac{a^4}{x^3} + \cdots\right) = 0 $$

以上より求める定積分は次のようになる．

$$ \int_0^{\infty} dx \ln\left(1 + \frac{a^2}{x^2}\right) = 2a^2 \int_0^{\infty}dx \frac{1}{x^2 + a^2} = 2a^2 \frac{1}{a}\arctan\infty = a\pi $$

## 感想戦

無限小量 $\varepsilon$ について次が成り立つことを途中で用いた．

$$ \ln(1 + \varepsilon) = \sum_{k=1}^{\infty}\frac{(-)^{k+1}}{k}\varepsilon^k $$

部分積分は境界値問題を必然的に内包しており，応用上，興味深い事柄が様々にある． 物理では表面項と言ったりするが，これが $0$ でないときは適切な境界条件を設定したりなど，物理的描像のヒントになったりする．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
