---
title: "[Summary][ML/DL] Multinomial(Using Softmax) Classification (lec06)"
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

# Recap
지난 시간에 배웠던 개념을 다시 리뷰하면 아래와 같다.


$$ H_L(x) = Wx $$

$$ Z = H_L(X), g(z) = )\left\{\begin{matrix}
0\\ 

1\end{matrix}\right.  $$

$$ g(z) = \frac{1}{1+e^{-z}} $$

즉, $$ H_R(x) = g(H_L(x)) $$ 이다

# Classification in binary Case (0 or 1)
우선 기존의 Input이 0과 1로 분류가 되는 과정은 다음과 같다.
X -> W ->(Z 함수 사용) -> Activation Funtion(sigmoid...) -> Y(정확히는 Y햇, prediction)

# Multinomial Classification

기존에 특징이 2개일 경우, Logistic Regression을 활용하여 알맞은 구분선을 구어주
우리가 세 개 이상의 특징으로 분류를 하기 위해선 Activation Funtion을 바꿔줄 필요가 있다.
해당하는 Activate Function은 Softmax 함수이다.

# Image about lec
![](https://user-images.githubusercontent.com/68592553/108341491-0a752700-721d-11eb-904a-e931505c8386.jpg)
![](https://user-images.githubusercontent.com/68592553/108341502-0c3eea80-721d-11eb-9b41-23999021d111.jpg)
