

---

layout: single
title:  "Variance, covariance, correlation coefficient"
categories: probabilty
tags : probabilty
toc : true
use_math : true

---



# Variance, covariance, correlation coefficient

## Variance

$$
Var(X) = \mathbb {E}(X-\mathbb {E}X)^2 = EX^2-(\mathbb{E}X)^2
$$

## Covariance

$$
Cov(X,Y) = \mathbb{E}[(X-\mathbb{E}X)(Y-\mathbb{E}Y)]=\mathbb{E}(XY)-(\mathbb{E}X)(\mathbb{E}Y)
$$

## Correlation coefficient

$$
-1 \le \rho=\frac{Cov(X,Y)}{\sqrt{Var(X)}\sqrt{Var(Y)}} \le1
$$

# Mean and variance of the sum of random variables

#### In general

$$
\begin {align}
\displaystyle \mathbb {E}\left(\sum_{i=1}^nX_i\right) &= \sum_{i=1}^n \mathbb{E}(X_i) \\
\displaystyle Var\left(\sum_{i=1}^nX_i\right) &= \sum_{i=1}^n Var(X_i) + \sum_{i\neq j} cov(X_i,X_j) \\
&=  \sum_{i=1}^n Var(X_i) + 2\sum_{i\le j} cov(X_i,X_j)
\end {align}
$$

---

##### proof.

$$
\begin {array} 
&& Var\left(\sum_{i=1}^nX_i\right) &= Cov\left(\sum_{i=1}^nX_i,\sum_{i=1}^nX_i \right) \\
&&=Cov(X_1,X_1) &+ Cov(X_1,X_2) &+ \cdots &+ Cov(X_1,X_n )\\
&&+Cov(X_2,X_1) &+ Cov(X_2,X_2) &+ \cdots &+ Cov(X_2,X_n )\\
&&\vdots&\vdots&\ddots&\vdots\\
&&+Cov(X_n,X_1) + &+ Cov(X_n,X_2) &+ \cdots &+ Cov(X_n,X_n )
\end {array}
$$

---





#### If $X_i$ are independent

$$
\displaystyle \mathbb {E}\left(\sum_{i=1}^nX_i\right) = \sum_{i=1}^n \mathbb{E}(X_i)\\
\displaystyle Var\left(\sum_{i=1}^nX_i\right) = \sum_{i=1}^n Var(X_i)
$$

#### If $X_i$ are iid

$$
\displaystyle \mathbb {E}\left(\sum_{i=1}^nX_i\right) = \sum_{i=1}^n \mathbb{E}(X_i) = n\mathbb{E}(X_1) \\
\displaystyle \mathbb Var\left(\sum_{i=1}^nX_i\right) = \sum_{i=1}^n Var(X_i) = nVar(X_1)
$$



