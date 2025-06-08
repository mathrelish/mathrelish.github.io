---
title: "定積分 No.15"
date: 2018-09-02
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-10.png"
---

# 定積分 No.15

$$ \int_0^{\frac{\pi}{2}} dx \frac{\sin^2 x}{\sin x + \cos x} = \frac{1}{2\sqrt{2}}\ln(3 + 2\sqrt{2}) $$

## 使用するトリック

分母が対称式で分子が正弦関数の二次であることから，積分変数のフリッピングを行えば，少なくとも分子は $\sin^2 x + \cos^2 x = 1$ となって，分母だけに三角関数が残るようなに簡約できると見通せる．

三角関数だけの有理式となったとき，分母の次数が二次ならば逆正接関数への帰着を検討して，その他の場合は次の変数変換によって代数関数に直して三角関数の議論から脱することを狙う．

$$ t = \tan\frac{x}{2} $$

このとき計算に必要な諸量は次のとおり．

$$ \begin{eqnarray} \sin x &=& \frac{2t}{1+t^2}, \\ \cos x &=& \frac{1-t^2}{1+t^2}, \\ \tan x &=& \frac{2t}{1-t^2}, \\ dx &=& \frac{2}{1+t^2}dt \end{eqnarray} $$

## 導出

積分変数のフリッピングを行って，加法定理によって整理すれば次を得る．

$$ I := \int_0^{\frac{\pi}{2}} dx \frac{\sin^2 x}{\sin x + \cos x} = \int_0^{\frac{\pi}{2}} dx \frac{\cos^2 x}{\sin x + \cos x} $$

よって二つの同じ値をもっている異なる表現を足し合わせて次を得る．

$$ 2I = \int_0^{\frac{\pi}{2}} dx \frac{\sin^2 x + \cos^2 x}{\sin x + \cos x} = \int_0^{\frac{\pi}{2}} dx \frac{1}{\sin x + \cos x} $$

次に $t = \tan\frac{x}{2}$ によって置換積分を行って次を得る．

$$ I = \int_0^1 dt \frac{1}{1 + 2z - z^2} $$

分母を平方完成して一次の項を消去すると，更に因数分解ができる．

$$ 1 + 2z - z^2 = 2 - (z - 1)^2 = (\sqrt{2} + z-1)(\sqrt{2} - z+1) $$

従って部分分数分解を実行して次のように整理ができる．

$$ I = \frac{1}{2\sqrt{2}}\int_0^1 dz \left[\frac{1}{\sqrt{2} + z-1} + \frac{1}{\sqrt{2} - z+1}\right] = \frac{1}{2\sqrt{2}}\left[\int_{\sqrt{2}-1}^{\sqrt{2}} du \frac{1}{u} - \int_{-\sqrt{2}+1}^{-\sqrt{2}} du \frac{1}{u} \right] $$

故に所望の結果を得る．

$$ I = \frac{1}{2\sqrt{2}}\left[\ln\left(\frac{\sqrt{2}}{\sqrt{2} - 1}\right) - \ln\left(\frac{\sqrt{2}}{\sqrt{2} + 1}\right) \right] = \frac{1}{2\sqrt{2}}\ln(3 + 2\sqrt{2}) $$

## 感想戦

もしはじめに積分変数のフリッピングが思いつかなったら苦労するのではないかと思う． それ以降は比較的わかりやすい，もしくは気付きやすい前提条件の下で，とりあえず最終手段として試せることばかりである．

なお途中用いた次の置換法を Weierstrass 置換という．

$$ t = \tan\frac{x}{2} $$

[Weierstrass 置換](https://en.wikipedia.org/wiki/Weierstrass_substitution)

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
