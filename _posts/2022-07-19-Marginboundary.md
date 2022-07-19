---
layout: single
title:  "Margin boundary"
categories: MachineLearning
toc : true
use_math : true
---



# Desicion boundary 와 Margin boundary의 거리

**Machine Learning with Python-From Linear Models to Deep Learning** 에서 

Unit1.Linear Classifiers and Generaliztions 중 Lecture 3 부분을 정리한 것 입니다.





$\mathbb R^2$ 공간에 있는 직선 $L$은


$$
L:\theta \cdot x + \theta_0 = 0
$$


$\theta$는 직선 $L$ 에 수직(Normal to the line L)인 벡터이다. 

점 $P$를 벡터 $x_0$의 종점이라 하자. 



점$P$ 와 직선 $L$ 사이의 거리는 


$$
d = \frac {|\theta \cdot x_0 + \theta_0|}{\lVert \theta \rVert}
$$
이다.





**decision boundary**  는
$$
\theta \cdot x + \theta_0 = 0
$$
을 만족하는 점$x$의 집합이며

**margin boundary** 는 
$$
\theta \cdot x + \theta_0 = \pm 1
$$
을 만족하는 점 $x$ 의 집합이다.



두 경계는 평행하므로 $x$를 margin boundary 위의 점이라 하고

decision boundary 까지의 거리를 구하면  두 경계의 거리가 된다.
$$
\frac {|\theta \cdot x + \theta_0|}{\lVert \theta \rVert} = \frac {1}{\lVert \theta \rVert}
$$
즉 **decision boundary** 에서 **margin boundary** 까지의 거리는 $\frac {1}{ \lVert\theta\rVert}$가 된다. 



$\theta$ 를 증가시키면 두 경계의 더 가까워지면 $\theta$ 를 감소시키면 두 경계의 거리는 멀어진다.



Margin을 최대화 하기 위해서는 $\theta$ 를 최소화 시켜야한다.



# Hinge Loss



$z$ 를 
$$
z = y^{(i)}(\theta \cdot x^{(i)} + \theta_0)
$$
이라 하자.

Hinge Loss는 다음과 같이 정의 할 수 있다.
$$
\begin {eqnarray}
Loss_h (z) &= max(0,1-z)
\end {eqnarray}
$$






# Objective 



**Objective** 함수를 다음과 같이 정의하자.
$$
J(\theta,\theta_0 )= \frac{1}{n} \sum_{i=1}^n Loss_h (y^{(i)}(\theta \cdot x^{(i)} + \theta_0)) + \frac{\lambda}{n} \lVert\theta\lVert^2
$$


우리의 목표는 $J$ 함수를 최소화 시키는 것이다.

$\lambda$ 항이 $Loss$항 보다 상대적으로 더 크다고 한다면 $\theta$ 값을 최소화 시켜야 하며 그 결과 Error 최소화 하기보다는  **Margin**을 최대화하게 된다. 더 일반화 된다.

$\lambda$ 항이 $Loss$항 보다 상대적으로 더 작다고 한다면 Loss항을 최소화 해야 하므로 Margin을 크게 하기보다 **Error** 를 최소화하게 된다. train_data에 더 맞추게 된다. 









