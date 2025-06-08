---
title: "定積分 No.11"
date: 2018-09-01
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-6.png"
---

# 定積分 No.11

$$ \int_{\sqrt{2}}^{\infty} dx \frac{1}{x + x^{\sqrt{2}}} = (1+\sqrt{2}) \ln \left[ 1 + 2^{\frac{1}{2}(1 - \sqrt{2})} \right] $$

## 使用するトリック

次式を対数関数の微分ということで対数微分といい，これを用いる．

$$ d\ln f(x) = \frac{f^{\prime}(x)}{f(x)}dx $$

## 導出

もっと一般に次の定積分を考える．

$$ I := \int_a^{\infty} dx \frac{1}{x + x^m} ~~ (m\neq 1) $$

そして被積分関数を次のように変形して $f(x)$ と置く．

$$ \frac{1}{x + x^m} = \frac{x^{-m}}{x^{1-m} + 1} =: \frac{x^{-m}}{f(x)} $$

すると被積分関数は更に次のように書き直せる．

$$ \frac{1}{x + x^m} = \frac{1}{1-m}\frac{f^{\prime}(x)}{f(x)} $$

よって一般化した定積分は次の様の書ける．

$$ I = \frac{1}{1-m} \int_a^{\infty} dx \frac{f^{\prime}(x)}{f(x)} = \frac{1}{1-m} \int_a^{\infty} d\ln f(x) = \frac{1}{m-1}\ln(1+a^{1-m}) $$

故に特に $m=a=\sqrt{2}$ をとると求めるべき次の定積分値を得る．

$$ \int_{\sqrt{2}}^{\infty} dx \frac{1}{x + x^{\sqrt{2}}} = (1+\sqrt{2}) \ln\left[1 + 2^{\frac{1}{2}(1 - \sqrt{2})}\right] $$

## 感想戦

対数微分はいろいろなところで表れる．良さは $\frac{f^{\prime}(x)}{f(x)}$ を次元解析をしてわかるように，任意の関数 $f$ が担っているスケールが消えている点である．単純な微分 $f^{\prime}(x)$ であると，$x\in X$ の変化に対する $f\in Y$ の変化量というように，$X,Y$ 二つの異なる世界での変化のスケールは必ずしも同じではなく，それを合わせたい局面で不都合が生じる．対数微分であれば残るのは $X$ の次元のみであるから，$X$ でのスケールを基準とした相対的な考察ができる．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
