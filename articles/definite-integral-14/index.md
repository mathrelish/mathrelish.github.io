---
title: "定積分 No.14"
date: 2018-09-02
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-9.png"
---

# 定積分 No.14

$$ \int_0^{\pi} dx \frac{x\sin x}{1 + \cos^2 x} = \frac{\pi^2}{4} $$

## 使用するトリック

積分領域が有限で且つ三角関数と一次式のみなので，積分変数のフリッピングを試行してみる．

$$ J := \int_a^bdx xf(x) = \int_a^bdy (a+b)g(y) - \int_a^bdy yg(y) $$

ここでもし $g(y)=f(y)$ 即ち $f(a+b-y)=f(y)$ ならば次を得る．

$$ J = \frac{a+b}{2}\int_a^bdx f(x) $$

つまり一次式を消去できて，少しは簡単と考えられる式に簡約できるというわけである．

## 導出

積分変数のフリッピングを行うと次を得る．

$$ I := \int_0^{\pi} dx \frac{x\sin x}{1 + \cos^2 x} = \int_0^{\pi} dy \frac{(\pi - y) \sin y}{1 + \cos^2 y} = \pi\int_0^{\pi} dx \frac{\sin x}{1 + \cos^2 x} - I $$

即ち次のように一次式を消去した定積分を得ることができる．

$$ I = \frac{\pi}{2}\int_0^{\pi} dx \frac{\sin x}{1 + \cos^2 x} = -\frac{\pi}{2}\int_0^{\pi} d(\cos x) \frac{1}{1 + \cos^2 x} $$

これを見ると $u=\cos x$ と置けば逆正接関数の積分に近くなるとわかる．よって次を得る．

$$ I = \frac{\pi}{2} \int_{-1}^1 du\frac{1}{1+u^2} = \frac{\pi^2}{4} $$

## 感想戦

$f(a+b-y)=f(y)$ を満たすような関数として三角関数は代表格であるが，定積分という演算と上手く結びついて式変形でもこのように良い性質を満たすこと自体ができすぎている，と思うばかりである．

今回のトリックがいつでも使えるとは限らないが，被積分関数が次の形をしていることは確率統計学との関連を見いだせて面白い．

$$ \int dx xf(x) $$

これは $f$ が確率密度関数であるならば，期待値を表す積分である．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
