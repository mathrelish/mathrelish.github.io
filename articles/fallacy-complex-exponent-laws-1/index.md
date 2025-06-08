---
title: "誤謬：複素数冪の指数法則 1"
date: 2020-10-06
categories: 
  - "mathematical-fallacy"
tags: 
  - "complex-function"
coverImage: "fallacy-complex-exponent-laws-1.png"
---

# 誤謬

　

次の指数法則は複素数の冪についていつでも成り立つ．

$$ z^{\alpha}z^{\beta} = z^{\alpha + \beta} $$

　

## 判定方法

指数 $\alpha$ と $\beta$ が共に整数であるか， もしくは「すべて主枝」もしくは「すべて同じ分枝」をとった場合は， 表題の指数法則はいつでも成り立つ． それ以外の場合は特別な場合を除いて保証されない．

## 反例

今回の反例は例のための例という感があるため省略する． その理由は分枝をバラバラに選ぶような偏角を考える場合であり， そのような場合はそうそうない．

## コメント

### 基本事項

複素数の冪関数は次のように定義された．

$$ z^{\alpha} := e^{\alpha\log z} $$

そして複素対数関数は次のように定義された．

\begin{eqnarray} \log z &:=& \{\ln |z| + i\arg z \mid z\neq 0 \}, \\ \arg z &:=& \{\mathrm{Arg} z + 2\pi n \mid z\neq 0 \land n\in\mathbb{Z}\}, \\ \mathrm{Log} z &:=& \ln|z| + i\mathrm{Arg} z \end{eqnarray}

ここで多価性は偏角部分 $\arg z$ に表れている． これらを基礎に丁寧に見ていけば，自ずと誤謬が明らかとなる．

### $z^{\alpha}z^{\beta}$ と $z^{\alpha + \beta}$ について

$z^{\alpha}z^{\beta}$ と $z^{\alpha + \beta}$ を評価すると次のようになる．

\begin{eqnarray} z^{\alpha}z^{\beta} &=& e^{(\alpha + \beta)\mathrm{Log} z + 2\pi i(\alpha n + \beta m)}, \\ z^{\alpha + \beta} &=& e^{(\alpha + \beta)\mathrm{Log} z + 2\pi i(\alpha + \beta)k} \end{eqnarray}

ここに $n,m,k\in\mathbb{Z}$ であり，$z^{\alpha},z^{\beta},z^{\alpha+\beta}$ に対する多価性である． よって次を得る．

$$ z^{\alpha}z^{\beta} = e^{2\pi i[\alpha(n-k) + \beta(m-k)]} z^{\alpha + \beta} $$

つまり単純な指数法則は次の場合を除いて一般には成立しない．

$$ (\delta :=) \alpha(n-k) + \beta(m-k) \in \mathbb{Z} $$

これから普通の指数法則が成立する場合とは次だとわかる．

- 任意の複素数 $\alpha,\beta$ に対して，すべて主枝を取る場合
- 任意の複素数 $\alpha,\beta$ に対して，すべて同じ分枝を取る場合 ($n=m=k$)
- 任意の分枝に対して，指数 $\alpha$ と $\beta$ が共に整数の場合
- この他，$\delta=0$ であるような特別な場合

## 参考

[誤謬：複素数冪関数はいつでも一価関数である．](https://mathrelish.com/mathematical-fallacy/fallacy-complex-power-function-is-a-single-valued-function)
