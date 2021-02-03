---
title: "[Summary][ML/DL] Logistic Classification(Regression) (lec05)"
mathjax: true
toc: true
toc_sticky: true
toc_label: 목차
categories:
- AI
- ML
- DL
- Summary
---

# Recap

- **Hypothesis :**

$$
H(x) = Wx + b
$$

- **cost funtion :**

$$
cost(W,b) = \frac{1}{m}\sum^n _{i=1}(H(x)^i)-y^i)^2
$$

$$
cost(W) = \frac{1}{m}\sum^n _{i=1}(Wx^i)-y^i)^2
$$

- **Gradient Descent :**

$$
W := W - \alpha\frac{\delta}{\delta W}cost(W)
$$

---
# What is Classification?
만약, 학생의 성적을 토대로 Pass와 Fail의 구분선을 긋는다(분류한다)고 생각해보자.
![](https://user-images.githubusercontent.com/68592553/106772005-ecd38980-6682-11eb-88b5-08ef3db5c1c2.PNG)

그렇다면 위처럼 범주에 따라 Pass와 Fail의 경계를 직선으로 구분짓기 어렵다.

따라서 우리는 **분류를 잘 할 수 있는 새로운 funtion 모델**이 필요하며, 그것이 바로**Sigmoid함수**를 활용한 **Logistic Regression**이다.

# In Classification
## Logistic
기존의 $$ H(x) = Wx+b $$에서 $$ H(x) $$ 를 우리는 $$ Z $$ 라고 설정할 것이다.
또한 $$ Z = Wx+b $$ 로 정의하여, 새로운 $$ g(Z) $$ 가  $$ \rightarrow 0 \cdots 1 $$ 를 반환하도록 설정한다.
## Hypothesis
기존의 Hypothesis는 $$ Z $$ 로 변경됐으므로, 새로운 $$ H(x) $$를 다음과 같이 설정한다.
$$ H(x) = \frac{1}{1+e^{-W^{T}X}} $$

## Cost funtion, Gradeint Descent Algorithm in Logistic
기존의 Linear Regression에서의 cost 함수는 아래와 같다.

$$ cost(W,b) = \frac{1}{m}\sum^n _{i=1}(H(x)^i)-y^i)^2 $$   $$ when $$   $$ H(x) = Wx+b $$
![](https://user-images.githubusercontent.com/68592553/106774453-784e1a00-6685-11eb-8a12-67abc905ee2b.PNG)

위는 Gradient Descent Algorithm을 잘 적용할 수 있고, 따라서 cost 함수의 미분 값이 최소가 되는 지점에서의 W값을 구할 수 있다.

허나 Logistic 모델에서는 cost 함수를 만들 때 아래와 같은 모습을 띤다.

$$ cost(W,b) = \frac{1}{m}\sum^n _{i=1}(H(x)^i)-y^i)^2 $$   $$ when $$   $$ H(x) = \frac{1}{1+e^{-W^{T}X}} $$
![](https://user-images.githubusercontent.com/68592553/106774460-797f4700-6685-11eb-93fd-7a705af1877a.PNG)

위는 Local Minimal != Global Minimal이다. 즉, Gradient Descent를 적용하면, 최소가 아닌 지점임에도 최소라고 판단하여 해당 W값을 반환할 것이다. 따라서 우리는 분류 환경(이하 로지스틱 회귀)에 걸맞는 cost 함수를 재정의해줄 필요가 있다.

## New cost function for Logistic
이하 부분은 21년 02월 5일 업로드 예정입니다.
