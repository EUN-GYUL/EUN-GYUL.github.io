---
layout: single
title:  "Linear Separation "
categories: Machine Learning
toc : true
use_math : true
---





# Linear Classifier 



## 정의 

$\theta$ 와 $\theta_{0}$ 가 주어졌을 때 linear classifier $h : X \rightarrow \{-1,0,+1\}$인 함수이다. 수식으로 표현하면 , $ h(x) = sing(\theta \cdot x+\theta_0)$ 

$h$는 $\theta \cdot x+\theta_0 = 0$ 을 만족하는 boundary로 정의된다. $i$ 번째 training data는 $(x^{(i)},y^{(i)})$이며 $x^{(i)}$는 vector이고 $y^{(i)}$ 는 scalar 값이다

$\theta$는 $x^{(i)}$와 같은 차원을 가지는 vector이다.

$y^{(i)}$ 은 label $\{-1,1\}$의 값을 가지며 으로 $\ $,  $sing(\theta \cdot x+\theta_0)$ 은 $h$ (classifier)의 결과 값으로 $\{-1,0,1\}$을 갖는다.



 $y^{(i)} ( \theta \cdot x+\theta_0 )>0$  을 만족 하기 위해서는 

$y^{(i)}>0$ and $\theta \cdot x+\theta_0>0$  이거나 $y^{(i)}>0$ and $\theta \cdot x+\theta_0 < 0$일 때 이다. 즉 label 값과 예측 값이 같을 때 이다.

 



