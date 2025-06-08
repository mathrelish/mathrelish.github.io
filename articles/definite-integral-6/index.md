---
title: "定積分 No.6"
date: 2018-09-01
categories: 
  - "calculation"
tags: 
  - "integration"
coverImage: "target-1.png"
---

# 定積分 No.6

$$ \int_1^{\infty} dx \frac{\{x\} - \frac{1}{2}}{x} = -1 + \ln\sqrt{2\pi} $$

但し $\{x\}$ は $x$ の小数部分を表す記号である．

[Fractional Part](http://mathworld.wolfram.com/FractionalPart.html)

## 使用するトリック

$\sqrt{2\pi}$ というところが階乗に関わる定積分の結果としてよく表れる定数であるため，そこでピンとくる人はピンとくる．ただの円周率であれば逆正接関数を想起するが，円周率の平方根というところが普通ではない．この数学定数と階乗を結びつけるのが，$n!$ についてのスターリングの漸近公式である．

$$ n! \sim \sqrt{2\pi} n^{n+\frac{1}{2}} e^{-n} $$

## 導出

$n!$ についてのスターリングの漸近公式は次のようにも書くことができる．

$$ \lim_{n\rightarrow \infty} \frac{n!}{n^{n+\frac{1}{2}} e^{-n}} = \sqrt{2\pi} $$

これを最後に用いる．

さてまず次を導出する．

$$ \ln n! = \int_1^n dx \frac{n - \lfloor x\rfloor}{x} $$

それは次のとおり．

$$ \ln n! = \sum_{k=2}^n \ln k = \sum_{k=2}^n \int_1^k dx \frac{1}{x} = \sum_{k=2}^n \sum_{j=1}^k \int_j^{j+1} dx \frac{1}{x} $$

ここで $\sum_{k=2}^n \sum_{j=1}^k \int_j^{j+1}$ を上手く次のようにして和の順序を組み直す．

$$ \sum_{k=2}^n \sum_{j=1}^k \int_j^{j+1} = \begin{matrix} \int_1^2 & & & & & & & & \\ \int_1^2 & + & \int_2^3 & & & & & & \\ \int_1^2 & + & \int_2^3 & + & \int_3^4 & & & & \\ \vdots & + & \vdots & + & \vdots & + & \ddots & & \\ \int_1^2 & + & \int_2^3 & + & \int_3^4 & + & \cdots & + & \int_{n-1}^n \end{matrix} = \sum_{j=1}^{n-1} (n-j)\int_j^{j+1} $$

よって次を得る．

$$ \ln n! = \sum_{j=1}^{n-1} \int_j^{j+1}dx\frac{n-j}{x} $$

今，積分変数は $j\leq x< j+1$ の間を動くので，このような $x$ は $\lfloor x\rfloor = j$ を満たす．これから次のように書き直せる．

$$ \ln n! = \sum_{j=1}^{n-1} \int_j^{j+1}dx\frac{n - \lfloor x \rfloor}{x} = \int_1^n dx\frac{n - \lfloor x \rfloor}{x} $$

これは導出したかった最初の式である． 我々はここから床関数を小数部分を与える関数へと次を用いて書き直す．

$$ \lfloor x\rfloor = x - \{x\} $$

書き換えを実行すると小数部分を与える関数についての定積分を除いて初等的に実行できるから，次の計算ができる．

$$ \ln n! = \ln\left[n^{n+\frac{1}{2}}e^{-n}\exp\left(1 + \int_1^n dx \frac{\{x\} - \frac{1}{2}}{x} \right)\right] $$

よって両辺の対数を外して次を得る．

$$ \exp\left(1 + \int_1^n dx \frac{\{x\} - \frac{1}{2}}{x} \right) = \frac{n!}{n^{n+\frac{1}{2}}e^{-n}} $$

右辺はスターリングの漸近公式の形そのままであるから，$\lim_{n\rightarrow \infty}$ をとって，両辺自然対数をとれば，所望の結果を得る．

## 感想戦

問題となった定積分はスターリングの漸近公式と同値といえるものであることが導出を追うとわかる． スターリングの漸近公式はスターリングよりも前にド・モアブルが先に導いていたが，$\sqrt{2\pi}$ がわからなかった．この数学定数を導出したのがスターリングの功績である．今回の定積分の計算を通して改めて数学定数 $\sqrt{2\pi}$ に敬意を表することができるだろう．

導出中に行った和の組み換えと $\lfloor x\rfloor = j$ によって一つに集約するところは実に技巧的で思い出深いだろう． 実数を整数部分と小数部分に分けるという話題はいろいろと面白い話があるが，わざわざ連続量を解析的には扱いにくい離散量に置き換えるということは勇気がいるものなので，今回のようなトリックがあるということ自体は記憶に値するといえるだろう．

なお今回は小数部分について正実数について扱ったという点も地味に面倒な問題を回避している． この件については下記に数学英語と絡めて解説されており参考になる．

[Fractional Part](http://math-eng.blogspot.com/2018/03/fractional-part.html)

## 参考

- [積分計算 – オススメの参考書・問題集](https://mathrelish.com/calculation/recommended-books-in-integral-calculus)

| [![](images/q)](https://www.amazon.co.jp/gp/product/1493912763/ref=as_li_ss_il?ie=UTF8&linkCode=li3&tag=alexandritefi-22&linkId=a5286db3f4f2b51f66db8f1437793841&language=ja_JP)![](images/ir) | [![](images/q)](https://www.amazon.co.jp/Irresistible-Integrals-Symbolics-Experiments-Evaluation/dp/0521796369/ref=as_li_ss_il?_encoding=UTF8&qid=&sr=&linkCode=li3&tag=alexandritefi-22&linkId=127b41d8f664d6dad21fbca1f6d0e0eb&language=ja_JP)![](images/ir) |
| --- | --- |

<script type="text/javascript">amzn_assoc_ad_type ="responsive_search_widget"; amzn_assoc_tracking_id ="alexandritefi-22"; amzn_assoc_marketplace ="amazon"; amzn_assoc_region ="JP"; amzn_assoc_placement =""; amzn_assoc_search_type = "search_widget";amzn_assoc_width ="auto"; amzn_assoc_height ="auto"; amzn_assoc_default_search_category =""; amzn_assoc_default_search_key ="積分";amzn_assoc_theme ="light"; amzn_assoc_bg_color ="FFFFFF";</script>

<script src="//z-fe.amazon-adsystem.com/widgets/q?ServiceVersion=20070822&amp;Operation=GetScript&amp;ID=OneJS&amp;WS=1&amp;Marketplace=JP"></script>
