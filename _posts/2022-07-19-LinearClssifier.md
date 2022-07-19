---
layout: single
title:  "Linear Separation and Perceptron"
categories: MachineLearning
tag : 정리
toc : true
use_math : true
---







# Linear Classifier 



**Machine Learning with Python-From Linear Models to Deep Learning** 에서 

Unit1.Linear Classifiers and Generaliztions 중 Lecture 2 부분을 정리한 것 입니다.



## 정의 

$\theta$ 와 $\theta_{0}$ 가 주어졌을 때 linear classifier $h : X \rightarrow \{-1,0,+1\}$인 함수이다. 수식으로 표현하면 
$$
h(x) = sing(\theta \cdot x+\theta_0)
$$
$h$는 $\theta \cdot x+\theta_0 = 0$ 을 만족하는 boundary로 정의된다. 



$i$ 번째 training data는 $(x^{(i)},y^{(i)})$이며 $x^{(i)}$는 vector이고 $y^{(i)}$ 는 scalar 값이고 $\theta$는 $x^{(i)}$와 같은 차원을 가지는 vector이다.

$y^{(i)}$ 은 label $\{-1,1\}$의 값을 가지며  $sing(\theta \cdot x+\theta_0)$ 은 $h$ (classifier)의 결과 값으로 $\{-1,0,1\}$을 갖는다.



 $y^{(i)} ( \theta \cdot x+\theta_0 )>0$  을 만족 하기 위해서는 

$y^{(i)}>0$ and $\theta \cdot x+\theta_0>0$  이거나 $y^{(i)}>0$ and $\theta \cdot x+\theta_0 < 0$일 때 이다. 즉 label 값과  분류한 값이 같을 때 이다.



 $y^{(i)} ( \theta \cdot x+\theta_0 ) \le 0$ 이면

label 값과  분류한 값이 일치하지 않을 때를 의미한다.



즉  $y^{(i)} ( \theta \cdot x+\theta_0 ) \le 0$  값이 커지면 더 나은 분류를 하고 있다고 볼 수 있다.





# Perceptron



퍼셉트론(Perceptron) 알고리즘은 "mistake" (  $y^{(i)}(\theta \cdot x^{(i)}) \le 0$ )가 발생 할 때 마다 $\theta$를 업데이트한다.

```
def percetpron(X , y , T):
    n = X.shape[0]
    theta = 0
    theta_0 = 0
    for t in range(T): 
        for i in range(n):
            if y[i] * (np.dot(theta,X[i]) + theta_0) <=0 :
                theta = theta + y[i]*X[i]
                theta_0 = theta_0 + y[i]
    
    return theta, theta_0
```



mistake가 발생 했을 때 , 업데이트된 theta 값들은 더 나은 결과를 낸다고 어떻게 알 수 있는가?

$$
\begin {align}
\theta = \theta + y^{(i)}x^{(i)} \\
\theta_0 = \theta_0 + y^{(i)}
\end {align}
$$


이 업데이트된 theta에 대한 




$$
\begin {align}
y^{(i)}( \underbrace {(\theta + y^{(i)}x^{(i)})}_{\text updated \quad \theta} \cdot x^{(i)} + \underbrace {\theta_0 + y^{(i)}}_{\text updated\quad \theta_0})
\end {align}
$$
위의 식의 값이 


$$
\begin {align}
y^{(i)}(\theta \cdot x^{(i)} + \theta_0)
\end {align}
$$
값보다 항상 크다고 할 수 있는가? 

위의 두 식을 빼면 
$$
\begin {align}
y^{(i)}y^{(i)}x^{(i)}\cdot x^{(i)} = (y^{(i)})^2\ {\lVert x^{(i)} \rVert}^2 \ge 0
\end {align}
$$
 그러므로 업데이트 된 값이 더 나은 분류 값이라고 할 수 있다.

