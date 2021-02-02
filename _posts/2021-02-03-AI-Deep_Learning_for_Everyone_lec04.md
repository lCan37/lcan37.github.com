---
title: "[Summary][ML/DL] Multivariable Linear Regression (lec04)"
mathjax: true
toc: true
toc_sticky: true
toc_label: 목차
categories:
- ML
- DL
- AI
- Summary
---

# 지난 강의 요약
지난 강의를 요약하자면 아래와 같은 키워드와 공식으로 정리할 수 있다.
-  **Hypothesis** : $$ H(x) = Wx + b (theory) $$
-  **Cost Function** : $$ cost(W) =  \frac{1}{m}\sum_{i=1}^{n}(H(x^i )-y^i )^2 $$
-  **Gradient Descent**를 활용한 Weight 갱신 : $$ W := W - \alpha \cdot \frac{1}{m} \sum_{i=1}^n(Wx^i-y^i) \cdot x^i $$

# Multivariable이란?
input으로 주어진 feature(변수,특징)가 여러개(2개 이상)일 때를 일컫는다.
- **Hypothesis** : $$ H(x_1, x_2, x_3) = W_{1}x_{1} + W_{2}x_{2} + W_{3}x_{3} +b $$
- **Cost Fuction** : $$ cost(W,b) = \frac{1}{m}\sum_{i=1}^{n}(H(x_{1}^{i}, x_{2}^{i}, x_{3}^{i} )-y^i )^2 $$

즉,  **Hypothesis** : $$ H(x_1,x_2,x_3, \cdots, x_n) = W_1x_1 + W_2x_2 + W_3x_3 + \cdots + W_nx_n+b $$ 이다.

이는 아래와 같은 Matrix로 표현 가능하다.

$$ \begin{pmatrix}
 x1& x2 & x3
\end{pmatrix} \cdot  \begin{pmatrix}
W_1\\ 
W_2\\ 
W_3
\end{pmatrix} = (x_1W_1+x_2W_2+x_3W_3)
$$

이는 Tensorflow 상에서의 Implementation으로 아래와 같이 표기한다.

$$
H(x) = XW
$$
