---
layout: single
title:  "Expectation"
categories: probabilty
tags : probabilty
toc : true
use_math : true
---

---

# Expectation

## Definition

$$
\begin{array}{lllllllll}
\mbox{Discrete}&EX&=&\displaystyle\sum_x xP(X=x) \nonumber\\
\mbox{Continuous}&EX&=&\displaystyle\int_{-\infty}^{\infty} x f(x)dx \nonumber\\
\end{array}
$$


### Properties of Expectation

#### Expectation as a linear operator

$$
\begin{eqnarray}
(1) &&\quad\displaystyle \mathbb{E}(X+Y) =\mathbb{E}(X) + \mathbb{E}(Y) \nonumber\\
(2) &&\quad\displaystyle \mathbb{E}(aX) = a\mathbb{E}(X) \nonumber\\
(3) &&\quad\displaystyle \mathbb{E}(a) = a \nonumber
\end{eqnarray}
$$

#### Change of variable

$$
\begin{eqnarray}
(4) &&\quad\displaystyle \mathbb{E}[g(X)] =\sum_{x_i}g(x_i)p_{x_i} \nonumber\\
(5) &&\quad\displaystyle \mathbb{E}[g(X, Y)] =\sum_{x_i}\sum_{y_j}g(x_i,y_j)p_{x_i},_{y_j} \nonumber
\end{eqnarray}
$$

#### Product of independent random variables

$$
\begin{array} {llllllll}
(6) &&\quad\displaystyle \mathbb{E}[XY] =\mathbb{E}[X]\mathbb{E}[Y] &&\mbox{if $X$ and $Y$ are independent} \nonumber\\
(7) &&\quad\displaystyle \mathbb{E}g[X]h[Y] =\mathbb{E}[g(X)]\mathbb{E}[h(Y)] &&\mbox{if $X$ and $Y$ are independent} \nonumber\\
\end{array}
$$

#### Cauchy-Schwartz inequality

$$
\begin{eqnarray}
(8)&&\quad\displaystyle \mathbb{E}|XY|\le (\mathbb{E}X^2)^{1/2}(\mathbb{E}Y^2)^{1/2}\nonumber
\end{eqnarray}
$$











