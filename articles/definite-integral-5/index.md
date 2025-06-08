---
title: "定積分 No.5"
date: 2018-08-31
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target.png"
---

# 定積分 No.5

$$ \int_0^1 dx \frac{x^4 (1-x)^4}{1 + x^2} = \frac{22}{7} - \pi $$

## 使用するトリック

被積分関数の分子の次数が分母の次数よりも大きいので，部分分数分解を適用すればよい． 手計算では大変だが，行うことは部分分数分解である．

## 導出

被積分関数を部分分数分解すると次のようなる．

$$ \frac{x^4 (1-x)^4}{1 + x^2} = x^6 - 4 x^5 + 5 x^4 - 4 x^2+4 - \frac{4}{x^2+1} $$

よって定積分は容易にできて所望の結果を直ちに得られる．

## 感想戦

導出は単に地道に事をなしてくものであるが，今回の定積分はとても有名な積分で Dalzell 積分とよぶことにしよう． Donald Percy Dalzell (1898–1988) は 1944 年に [Journal of the London Mathematical Society](https://www.lms.ac.uk/publications/jlms) に次の論文を書いており，ここではじめて今回の定積分が世に出たからである．

[On 22/7](https://londmathsoc.onlinelibrary.wiley.com/doi/pdf/10.1112/jlms/19.75_Part_3.133)

その後に [William Lowell Putnam Mathematical Competition](https://en.wikipedia.org/wiki/William_Lowell_Putnam_Mathematical_Competition) という数学のコンテストに出題された．

[The Twenty-Ninth William Lowell Putnam Mathematical Competition](https://books.google.co.jp/books?id=HNLRgSGZrWMC&pg=PA9&dq=December-7-1968+Putnam+Mathematical-Competition&ei=DZCfR4iRJJu4sgPRu-CwCg&sig=u4-SIYyVtV3rbwN-p56c42BGUKw&redir_esc=y&hl=ja#v=onepage&q=December-7-1968%20Putnam%20Mathematical-Competition&f=false)

この定積分が面白いのは次の有理数が円周率を伴って表れることである．

$$ \frac{22}{7} = 3.\dot{1}4285\dot{7} $$

この有理数は実に紀元前三世紀のアルキメデスにまで遡ることができる円周率の近似値として由緒ある数である． そして今回の定積分で円周率の差として計算されている．被積分関数は明らかに負ではないので，積分した結果もまた負ではない．円周率は無理数であるから等しいこともありえない． よって次の不等式を得る．

$$ \pi < \frac{22}{7} $$

つまり円周率は $\frac{22}{7}$ よりも小さい！

[円周率が22/7より小さいことの証明](https://ja.wikipedia.org/wiki/円周率が22/7より小さいことの証明)

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

[![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir)

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
