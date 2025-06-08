---
title: "定積分 No.18"
date: 2018-09-21
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-13.png"
---

# 定積分 No.18

$$ \int_0^{\infty} dx \frac{1}{x^4 + 2x^2\cos(2\alpha) + 1} = \frac{\pi}{4\cos\alpha} $$

## 使用するトリック

実積分の範疇でこの定積分を求めるのは労を要する． ここまで培った次のトリックを適宜用いる．

- 積分変数のフリッピング
- 偶関数・奇関数
- 置換積分

求める定積分の積分範囲は有限ではないが，例えば次の置換積分によって積分変数のフリッピングを行うことができる．

$$ y = \frac{1}{x} $$

これで似たような関数を得るわけであるが，この置換積分は関数の偶奇性を保つので，もし被積分関数の分母が同じであれば (事実，同じになるのであるが) 冪乗が分子に出てくるはずである．

このこととは別に被積分関数の分母は次のように因数分解できる．

$$ x^4 + 2x^2\cos(2\alpha) + 1 = (x^2 - 2x\sin\alpha + 1)(x^2 + 2x\sin\alpha + 1) $$

この因数をみると偶関数二つと奇関数一つの和になっている． そこで積分変数のフリッピングによって $x^2$ なる偶関数が分子にさえ出てくれば，分母分子を約せそうである．というのも奇関数の部分については $0$ を足すということで補えるからである．

もしこれが上手くいけば (事実，上手くいくのだが) 二次式に落ちるので，後は平方完成して，適当に定数分だけの違いを置換積分すれば，逆正接関数がでてきそうである．

上記のような計画の下で，定積分を求めるということを行う．

## 導出

積分変数のフリッピングを行って次を得る．

$$ I(\alpha) := \int_0^{\infty} dx \frac{1}{x^4 + 2x^2\cos(2\alpha) + 1} = \int_0^{\infty} dy \frac{y^2}{y^4 + 2y^2\cos(2\alpha) + 1} $$

二つの異なる表式を足し合わせて，偶関数の性質によって積分範囲を広げて，次を得る．

$$ I(\alpha) = \frac{1}{2}\int_0^{\infty} dx \frac{x^2 + 1}{x^4 + 2x^2\cos(2\alpha) + 1} = \frac{1}{4}\int_{-\infty}^{\infty} dx \frac{x^2 + 1}{x^4 + 2x^2\cos(2\alpha) + 1} $$

ここで次の奇関数の定積分を考える．

$$ 0 = \int_{-\infty}^{\infty} dx \frac{x}{x^4 + 2x^2\cos(2\alpha) + 1} $$

求めるべき定積分の被積分関数の分母を因数分解して，この奇関数の定積分を加えることで，分母分子を約せるので，これを実行すると次を得る．

$$ I(\alpha) = \frac{1}{4}\int_{-\infty}^{\infty} dx \frac{x^2 \mp 2x\sin\alpha + 1}{(x^2 - 2x\sin\alpha + 1)(x^2 + 2x\sin\alpha + 1)} = \frac{1}{4}\int_{-\infty}^{\infty} dx \frac{1}{x^2 \pm 2x\sin\alpha + 1} $$

得られた定積分の被積分関数の分母を平方完成する．

$$ I(\alpha) = \frac{1}{4}\int_{-\infty}^{\infty} dx \frac{1}{(x \pm \sin\alpha)^2 + \cos^2\alpha} $$

ここで $u_{\pm} := x\pm \sin\alpha$ なる変数変換による置換積分を行って，所望の結果を得る．

$$ I(\alpha) = \frac{1}{4}\int_{-\infty}^{\infty} du_{\pm} \frac{1}{u_{\pm}^2 + \cos^2\alpha} = \frac{1}{4}\frac{1}{\cos\alpha}\left. \arctan\frac{u_{\pm}}{\cos\alpha} \right|_{-\infty}^{\infty} = \frac{\pi}{4\cos\alpha} $$

## 感想戦

トントン拍子に上手くいくような定積分の面白みが程よく詰まったような計算だった．

得られた結果について $\alpha$ を様々に変えることで，いろいろな対称な定積分を特殊な場合として得ることができる．労に対して少しは報われることだろう．

$$ I\left(\frac{\pi}{4}\right) = \int_0^{\infty} dx \frac{1}{x^4 + 1} = \int_0^{\infty} dx \frac{x^2}{x^4 + 1} = \frac{\pi}{2\sqrt{2}} $$

$$ I\left(\frac{\pi}{6}\right) = \int_0^{\infty} dx \frac{1}{x^4 + x^2 + 1} = \int_0^{\infty} dx \frac{x^2}{x^4 + x^2 + 1} = \frac{\pi}{2\sqrt{3}} $$

$$ I\left(\frac{\pi}{3}\right) = \int_0^{\infty} dx \frac{1}{x^4 - x^2 + 1} = \int_0^{\infty} dx \frac{x^2}{x^4 - x^2 + 1} = \frac{\pi}{2} $$

$$ I\left(0\right) = \int_0^{\infty} dx \frac{1}{x^4 + 2x^2 + 1} = \int_0^{\infty} dx \frac{x^2}{x^4 + 2x^2 + 1} = \frac{\pi}{4} $$

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
