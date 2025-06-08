---
title: "定積分 No.20"
date: 2018-09-22
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-15.png"
---

# 定積分 No.20

$$ I_n := \int_0^{\infty} dx x^{2n}e^{-x^2} = \frac{(2n)!}{4^n n!}\frac{\sqrt{\pi}}{2} ~~ (n=0,1,2,3,\cdots) $$

## 使用するトリック

$n$ についての漸化式を立式することで積分を求める． 今回の場合は部分積分を手がかりに漸化式を見出すことになる． 被積分関数は指数関数を含んでおり，形を変えずに冪関数の次数だけ変化させられると期待できるからである．

なお漸化式の初期条件である次の定積分 (ガウス積分) の導出はここでは既知だとする．

$$ I_0 = \int_0^{\infty} dx e^{-x^2} = \frac{1}{2} \int_{-\infty}^{\infty} dx e^{-x^2} = \frac{\sqrt{\pi}}{2} $$

## 導出

与えられた定積分について部分積分を行うと次を得る．

$$ \int_0^{\infty} dx \frac{d}{dx}[x^{2n}e^{-x^2}] = (2n-1)I_{n-1} - 2I_n $$

ここで左辺は次のように評価できる．

$$ \int_0^{\infty} dx \frac{d}{dx}[x^{2n}e^{-x^2}] = \left.x^{2n}e^{-x^2}\right|_0^{\infty} = 0 ~~ \left(n > \frac{1}{2}\right) $$

よって次の漸化式を得る．

$$ I_n = \frac{2n-1}{2}I_{n-1} ~~ (n=1,2,3,\cdots) $$

これは容易に次のように直接に解ける．

$$ I_n = \frac{2n-1}{2}\frac{2n-3}{2}\frac{2n-5}{2}\cdots\frac{2n-(2n-1)}{2}I_0 =: c_n I_0 $$

ここで $c_n$ は次のように求められる．

$$ \begin{aligned} c_n &= \frac{2n}{2n}\frac{2n-1}{2}\frac{2n-2}{2n-2}\frac{2n-3}{2}\frac{2n-4}{2n-4}\frac{2n-5}{2}\cdots\frac{2}{2}\frac{1}{2} \\ &= \frac{(2n)!}{2^n}\frac{1}{2n(2n-2)(2n-4)\cdots 2} \\ &= \frac{(2n)!}{2^n}\frac{1}{2^n n!} \\ &= \frac{(2n)!}{4^n n!} \end{aligned} $$

これと $I_0$ についてガウス積分の結果を援用すれば所望の結果に至る．

## 感想戦

今回の定積分はエルミート多項式の直交性を表す次の評価に表れる．

$$ \int_{-\infty}^{\infty}dx H_m(x)H_n(x) e^{-x^2} = \sqrt{\pi}2^n n!\delta_{n,m} $$

エルミート多項式 $H_n(x)$ は $n$ の偶奇に応じて偶数冪・奇数冪関数となる． このため直交関係で $0$ とならない $[H_n(x)]^2$ は偶数冪関数となる． よって今回の定積分が表れることになる．

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
