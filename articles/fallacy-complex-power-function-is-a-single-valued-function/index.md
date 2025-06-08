---
title: "誤謬：複素数冪関数はいつでも一価関数である．"
date: 2020-10-03
categories: 
  - "mathematical-fallacy"
tags: 
  - "complex-function"
coverImage: "fallacy-complex-power-function-is-a-single-valued-function.png"
---

# 誤謬

　

複素数冪関数はいつでも一価関数である．

　

## 判定方法

複素数冪関数 $z^{\alpha}$ があった場合に， 指数 $\alpha$ が整数ならば一価関数であるが， 他はその限りではない．

## 反例

$$ z^{\frac{1}{2}} = e^{\frac{1}{2}\log z} = \{e^{\frac{1}{2}(\ln|z| + i\mathrm{Arg}z)} e^{i\pi n} \mid n\in\mathbb{Z}\} $$

よって $\{e^{i\pi n}\mid n\in\mathbb{Z}\} = \{+1,-1\}$ で二価関数であるから， $z^{1/2}$ は一価関数ではなく二価関数である．

## コメント

複素数の冪関数は次で定義される関数であった．

$$ z^{\alpha} := e^{\alpha \log z} ~~ (z\neq 0) $$

ここで複素対数関数 $\log z$ の中の偏角部分が多価関数になり得る要因になっている．

$$ \log z = \{\ln |z| + i\arg z \mid z\neq 0\} = \{\ln |z| + i(\mathrm{Arg} z + 2\pi n) \mid z\neq 0 \land n\in\mathbb{Z} \} $$

つまり複素数の冪関数は一般に次のようになっている．

$$ z^{\alpha} = \{e^{\alpha(\ln |z| + i\mathrm{Arg} z)} e^{2\pi in \alpha} \mid z\neq 0 \land n\in\mathbb{Z} \} $$

これより多価性の有無は $\{e^{2\pi in \alpha} \mid n\in\mathbb{Z}\}$ に集約されるとわかる． 具体的には次のとおりで，実際にその数を代入すると直ちにわかる．

| $\alpha$ | 価 |
| :-- | :-- |
| $\mathbb{Z}$ | 一価関数 |
| $p/q\in\mathbb{Q}\setminus\mathbb{Z}$ | $q$価関数 |
| $a\in\mathbb{R}\setminus\mathbb{Q}$ | 無限多価関数 |
| $\alpha\in\mathbb{C}\setminus\mathbb{R}$ | 無限多価関数 |

既約分数の場合は分母を相殺する整数値をとった場合に一周すること， 無理数の場合はそれが起こらないということ， そして虚部が存在すると指数関数の指数部が実数となって周期関数でなくなってしまうこと， これらのことが生じて一価関数ではなくなる．

## 参考

[疑義：複素対数関数の実引数](https://mathrelish.com/doubtful/doubtful-complex-logarithm-real-argument)
