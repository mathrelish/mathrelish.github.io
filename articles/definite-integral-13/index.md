---
title: "定積分 No.13"
date: 2018-09-02
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-8.png"
---

# 定積分 No.13

$$ \int_0^{\frac{\pi}{2}} dx \frac{\sqrt{\sin x}}{\sqrt{\sin x } + \sqrt{\cos x}} = \frac{\pi}{4} $$

## 使用するトリック

積分変数のフリッピングを用いる．積分変数のフリッピングとは向きを変える変数変換のことで，例えば積分領域が $[a,b]$ であったなら，$y = a + b - x$ と変数変換することをいう．このようにすれば積分は $\int_a^b dx f(x) = \int_a^b dy g(y)$ となり二つの同じ値を取る異なった表現を得ることができる．これを上手く用いる．

どのようなときに功を奏するかであるが，フリッピングに対してまた似たような関数に戻る場合に有効である． また必然的に積分領域に無限大を含んでいないことが使用条件となる．

## 導出

$y= \frac{\pi}{2} - x$ と変数変換する置換積分を行うと次を得る．

$$ I := \int_0^{\frac{\pi}{2}} dx \frac{\sqrt{\sin x}}{\sqrt{\sin x } + \sqrt{\cos x}} = \int_0^{\frac{\pi}{2}} dy \frac{\sqrt{\sin \left(\frac{\pi}{2} - y\right)}}{\sqrt{\sin \left(\frac{\pi}{2} - y\right) } + \sqrt{\cos \left(\frac{\pi}{2} - y\right)}} = \int_0^{\frac{\pi}{2}} dy \frac{\sqrt{\cos y}}{\sqrt{\sin y} + \sqrt{\cos y}} $$

よって元の式と足し合わせて次を得る．

$$ 2I = \int_0^{\frac{\pi}{2}} dx \frac{\sqrt{\sin x } + \sqrt{\cos x}}{\sqrt{\sin x } + \sqrt{\cos x}} = \frac{\pi}{2} $$

故に所望の結果に至る．

## 感想戦

今回の式変形からわかるように根号はブラフだとわかる．これから $\frac{\pi}{4}$ の値を取る同一の定積分をいくつか考えることができる．一例を示すと次のとおり．

$$ J := \int_0^{\frac{\pi}{2}} dx \frac{g(\sin x)}{f(\sin x,\cos x)} $$

積分変数のフリッピングを行って次を得る．

$$ 2J = \int_0^{\frac{\pi}{2}} dx \left[\frac{g(\sin x)}{f(\sin x,\cos x)} + \frac{g(\cos x)}{f(\cos x,\sin x)} \right] $$

この被積分関数が $1$ である場合を特に考えたい．

ここで例えば $f(\cos x,\sin x) = f(\sin x, \cos x)$ だとすると，通分した分子は分母に等しくならねばならない．ところが分子 $g(\sin x) + g(\cos x)$ は交叉項を作れないから，$f(\sin x, \cos x) = g(\sin x) + g(\cos x)$ が満たされさえすれば，特異にならない限りなんでもよいとわかる．

### King's Property (Rule)

ところで我々は次の置換積分のことをフリッピングと称した．

$$ \int_a^b dx f(x) = \int_a^b dx f(a+b-x) $$

これには幾つか別称があって，King's Property とか King's Rule などとよばれることがある． 何故そのような名称なのか，一節によればインドの教育会社がこのように呼称したらしく， King とは Rajasthan 州でかつて栄えた王朝を意識してのことのようだが，由来は定かではない．

[Why is it called 'King's Property of Integration'?](https://math.stackexchange.com/questions/3952365/why-is-it-called-kings-property-of-integration)

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
