---
title: "定積分 No.4"
date: 2018-08-31
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-3.png"
---

# 定積分 No.4

$$ \mathrm{p.v.}\int_0^{\infty} dx \frac{1}{x^3 - 1} = -\frac{\pi\sqrt{3}}{9} $$

## 使用するトリック

積分領域に被積分関数は特異点 $x=1$ を含んでいるので，一般に積分値は極限の取り方に依存する．そのような極限の取り方の一つがコーシーの主値積分である．主題の定積分がコーシーの主値積分を表している．特異点を $x=c\in[a,b]$ とするとき定義は次のとおり．

$$ \mathrm{p.v.} \int_a^b dx f(x) := \lim_{\varepsilon\rightarrow +0} \left( \int_{a}^{c-\varepsilon}dx f(x) + \int_{c+\varepsilon}^{b}dx f(x) \right) $$

注意すべきはコーシーの主値積分は極限の取り方を与えるものであって，収束までは保証しない． 発散する場合もあるし，不定な場合もある．

以上は計算に意味を持たせる定義に過ぎない．今回のトリックは部分分数分解である． $x^3 - 1$を因数分解すると次のとおり．

$$ x^3 - 1 = (-x + 1) (x^2 + x + 1) $$

一般に次の部分分数分解が成り立つ．

$$ \frac{px^2+qx+r}{(ax+b)(cx^2+dx+e)} = \frac{A}{ax+b} + \frac{Bx}{cx^2+dx+e} + \frac{C}{cx^2+dx+e} $$

我々はこれを用いる．

## 導出

被積分関数を部分分数分解すると次のとおり．

$$ \frac{1}{x^3 - 1} = \frac{1/3}{x-1} + \frac{-x/3}{x^2+x+1} + \frac{-2/3}{x^2+x+1} $$

右辺第二項の分子を分母の微分となるようにしつつ，右辺第三項は平方完成しておく． つまり前者および第一項は対数関数を得る積分，後者は逆正接関数を得る積分であることを見抜く．

$$ \frac{1}{x^3 - 1} = \frac{1}{3(x-1)} - \frac{2x+1}{6(x^2+x+1)} - \frac{1}{2\left[(x+\frac{1}{2})^2+\frac{3}{4}\right]} $$

よってこれを不定積分すると次を得る．

$$ \int dx \frac{1}{x^3 - 1} = \frac{1}{6}\ln\left(\frac{x^2-x+1}{x^2+x+1}\right) - \frac{1}{\sqrt{3}}\arctan\left(\frac{2x+1}{\sqrt{3}}\right) $$

これを基にコーシーの主値積分を行い雑多な計算を行うと次のとおりである．

$$ \mathrm{p.v.}\int_0^{\infty} dx \frac{1}{x^3 - 1} = \frac{1}{\sqrt{3}} \lim_{\varepsilon\rightarrow +0} \left[ -\arctan\left(\frac{3 - 2\varepsilon}{\sqrt{3}}\right) + \arctan\frac{1}{\sqrt{3}} - \frac{\pi}{2} + \arctan\left(\frac{3 + 2\varepsilon}{\sqrt{3}}\right) \right] $$

この極限は存在して所望の実数値を与える．

## 感想戦

部分分数分解は不定積分の一般論を展開する上でも基礎となるが，分数である以上は特異点の問題が避けられない． 従ってコーシーの主値積分の話題が必然的に表れることになる． 後は部分分数分解する以上は項別の積分が増えるので，やや退屈な計算が続くことになりやすい．

部分分数分解した不定積分結果が逆正接関数を含むと，定積分することで円周率 $\pi$ もまたよく表れる．今回の計算では $\arctan\infty=\frac{\pi}{2}$ 由来の円周率 $\pi$ が最後に残っている．この他，円周率 $\pi$ と $3$ の冪との積であることも面白い．つまり意識的に書けば次のようになる．

$$ \mathrm{p.v.}\int_0^{\infty} dx \frac{1}{x^3 - 1} = -\pi 3^{\frac{1}{2} - \frac{2}{1}} $$

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
