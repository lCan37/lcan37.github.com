---
title: "[Summary][ML/DL] Linear Regression, Hypothesis, Cost Function (lec02)"
categories:
- ML
- DL
- AI
- Summary
---

## Linear Regression
### 1. What is Linear Regression
![Data](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbcCKJw%2FbtqzANTLldb%2FWJcNgXZhwAkaoOMVoJMmGk%2Fimg.png)

![LR1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Flrmyd%2FbtqzAOd3AR5%2FvB3S1jCw4qTnsIGUBjeUKk%2Fimg.png)

- Linear Regression이란, 데이터의 특징을 잘 나타내는 선형식을 긋는 걸 말한다.
- 파란색의 선은 위 세 직선 중 가장 데이터의 특징을 잘 나타내며, 우리는 다른 두 개의 선도 W(기울기)와 b(y절편)의 값을 잘 조절하여 파란색 선에 가깝게 해야한다.

### 2. 최적의 선형식을 찾기
![Cost1](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fbw89Vv%2FbtqzAjrQA8e%2FVK8wVqdNa0Fk22qbZGOzGk%2Fimg.png)

 - 위처럼 실제 데이터의 값과 선형식의 값의 차이를 최소화 함으로써 최적의 선형식을 찾을 수 있다.
 - 이때 실측값과 예측값(선형식으로 추정한 것)의 차이를 Cost라고 한다.

### 정리 (결론)
![Cost2](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FNn3Tf%2Fbtqzzl4JLJX%2FiKo0R0UcpR0IaoyKq8De5K%2Fimg.png)
![Cost3](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FmNHtj%2FbtqzAi0ITih%2F6MGnS8nAKUSipMYKrWgdYK%2Fimg.png)
- 위 수식을 만족하는, 즉, cost가 최소인 W와 b를 찾는 것이 Linear Regression에서의 목표다.
