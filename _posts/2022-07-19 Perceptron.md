---
layout: single
title:  "Perceptron"
categories: Machine Learning
toc : true
use_math : true
---



# Perceptron



퍼셉트론(Perceptron) 알고리즘은 "mistake"( 수식적으론 $y^{(i)}(\theta \cdot x^{(i)}) \le 0$)가 발생 할 때 마다 $\theta$를 업데이트한다.

```
def percetpron(X , y , T):
    n = X.shape[0]
    theta = 0
    theta_0 = 0
    for t in range(T): 
        for i in range(n):
            if y[i] * (np.dot(theta,X[i]) + theta+0) <=0 :
                theta = theta + y[i]*X[i]
                theta_0 = theta_0 + y[i]
    
    return theta, theta_0
```



mistake가 발생 했을 때 , 업데이트된 theta 값들은 더 나은 결과를 낸다고 어떻게 알 수 있는가?

즉 
$$
\theta = \theta + y^{(i)}x^{(i)} \\
\theta_0 = \theta_0 + y^{(i)}
$$
이 업데이트된 theta에 대한 
$$
y^{(i)}( \underbrace {(\theta + y^{(i)}x^{(i)})}_{\text updated \quad \theta} \cdot x^{(i)} + \underbrace {\theta_0 + y^{(i)}}_{\text updated\quad \theta_0})
$$
위의 식의 값이 
$$
y^{(i)}(\theta \cdot x^{(i)})
$$
값보다 항상 크다고 할 수 있는가?