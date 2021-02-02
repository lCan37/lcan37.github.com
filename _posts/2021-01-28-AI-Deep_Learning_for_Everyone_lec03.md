---
title: "[Summary][ML/DL] How to Minimize Cost (lec03)"
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

# Cost함수를 도출하기

- 계산의 편의를 위해 $$ H(x) = Wx+b $$ 를 다음으로 나타내보자.

$$
H(x) = Wx
$$

우리가 알던 Cost는 아래와 같이 정의할 수 있다.

$$
cost(W) = \frac{1}{m}\sum_{i=1}^n(H(x^i)-y^i)^2
$$

즉, 이는 바뀐 Hypothesis의 정의를 적용하면 아래와 같다.

$$
cost(W) = \frac{1}{m}\sum_{i=1}^n(Wx^i-y^i)^2
$$

위의 cost(W) 함수를 그래프로 표현하면 다음과 같다.
![cost_function](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FMvf8g%2FbtqzyXJ2AX8%2Fmsdrdq1bweK15rKKJ8CxqK%2Fimg.png)

# Cost를 최소화하려면
- Gradient Descent Algorithm을 사용한다.
	- 그래프의 순간변화율(미분)을 구하고, 해당 값(미분 값, 기울기)가 0이 되도록 하는 W의 지점을 찾는 것을 목표로 한다.

## 작동 원리
1. 처음에는 임의의 위치에서 시작한다.
2. 이후 W를 조금씩 변경하여, Cost를 점차 낮춘다.

# Formal Definition of Cost
다시 수식을 바라보자.

$$
cost(W) = \frac{1}{m}\sum_{i=1}^n(Wx^i-y^i)^2
$$

여기에서 계산의 편의를 위해 $$ m := 2m $$ 을 하면 아래와 같이 표현할 수 있다.

$$
cost(W) = \frac{1}{2m}\sum_{i=1}^n(Wx^i-y^i)^2
$$

한편, 우리는 주기마다 Gradient Descent Algorithm을 활용하여  W값을 갱신할 수 있다고 언급했다.
이와 관련된 수식은 다음과 같이 재정의 할 수 있다.

$$
W := W - \alpha \frac{\delta}{\delta W} \cdot cost(W)
$$

이때 $$ \alpha $$ 는 Learning Rate(학습율)로, 학습의 정도를 지정하는 수치이다. 보통 일반적으로 0.1을 선정한다.
위에서 작성한 수식은 아래와 같이 정리하여 나타낼 수 있다.

$$
W := W - \alpha \frac{\delta}{\delta W} \cdot \frac{1}{2m}\sum_{i=1}^n(Wx^i-y^i)^2
$$

이는 아래와 같이 풀어서 작성할 수 있다.

$$
W := W - \alpha \cdot \frac{1}{2m} \cdot 2\sum_{i=1}^n(Wx^i-y^i) \cdot x^i
$$

합성함수의 미분이 완료된 후, 공통 인수로 나누면 아래와 같이 정리가 가능하다.

$$
W := W - \alpha \cdot \frac{1}{m} \sum_{i=1}^n(Wx^i-y^i) \cdot x^i
$$

따라서 **위 공식이 Gradient Descent를 활용한 Cost를 최소화하는 방법의 공식**이다.
단, 이때 한가지 유념해야 할 것은, Local Minimal = Gloabal Minimal이어야 한다는 점이다(local minimal이 여러 개 발생하면 안됨).
