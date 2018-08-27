---
title: Machine Learning(ML) - ML로 전환하기
date: 2018-08-27 17:20:56
tags: 
    - 머신러닝 단기집중과정
category: 
    - 머신러닝 단기집중과정
---

본 게시물은 {% link 구글 머신러닝 단기집중과정 스터디 [https://developers.google.com/machine-learning/crash-course/?utm_source=DevRel&utm_medium=StudyJam&utm_campaign=q1y2018&utm_term=&utm_content=mlcc] [구글 머신러닝 단기집중과정 스터디] %}을 참고하여 작성되었습니다.

<!-- toc -->

## ML로 전환하기
  * ML로 전환하기? 
    * 주어진 데이터를 통해서 선형 모델을 만들라는 것(=선형회귀!)
    * 어떤 문제를 회귀화 기본적인 Flow(흐름)을 파악하자 - Step by Step!
    
### 선형 회귀
  * 제일 먼저, 데이터를 그래프로 만들어 검토해야한다
  * 왜냐? 데이터가 잘못되면 우리가 원하는 모델을 얻을 수 없기 때문!
  * 예시) 온도별 1분당 귀뚜라미가 우는 횟수 
    * 나는 귀뚜라미가 몇번 우는지를 통해서 온도를 알고 싶다!
    * 데이터를 먼저 좌표로 나타낸다
      <img src="/2018/08/27/machine-learning-2/figure1.JPG" width="400" height="400" alt="Figure 1 : 귀뚜라미가 온도에 따라 1분당 우는 횟수">
      데이터간의 관계를 보면 온도와 1분당 우는 횟수는 서로 비례하는 관계를 가짐
      따라서, 이 관계를 근사치로 표현할 수 있는 단 하나의 직선을 만들어 낼 수 있음
    * 두번째 데이터간의 관계를 근사치로 표현한 직선
      <img src="/2018/08/27/machine-learning-2/figure2.JPG" width="400" height="400" alt="Figure 2 : 근사치 그래프(선형 관계)">
      근사치로 표현한 직선이 모든 점(데이터)를 통과하지 않지만 대략적인 관계를 보여줌
      이 그래프(관계)는 어떤 공식(모델의 방정식)으로 나타낼 수 있다 
    * 직선의 방정식
      <img src="/2018/08/27/machine-learning-2/figure3.JPG" width="200" height="200" alt="Figure 3 : 직선의 방정식">
      위에서 만든 직선을 수학적으로 공식화한 것
      * y : 온도, 예측하려는 값(우리가 알고 싶은 값)
      * m : 선의 기울기
      * x : 1분당 우는 횟수, 입력 특성 값(귀뚜라미가 1분에 100번 울었을때 온도를 알고 싶다면? x=100을 입력)
      * b : y절편(직선이 y축과 만나는 점)
    * 모델의 방정식
      <img src="/2018/08/27/machine-learning-2/figure4.JPG" width="200" height="200" alt="Figure 4 : 모델의 방정식">
      위에서 구한 직선의 방정식을 머신러닝의 관습에 맞게 작성한 방정식
      * y' : 예측된 라벨(얻고자 하는 출력)
      * w₁ : 특성1의 가중치. 가중치는 기울기와 같은 개념
      * x₁ : 특성1(알려진 입력)
      * b : 편향(y절편). w_0\이라고도 표현함
    * 정교한 모델(여러 특성에 의존하는 모델)
      <img src="/2018/08/27/machine-learning-2/figure5.JPG" width="200" height="200" alt="Figure 5 : 3가지 특성에 의존하는 모델의 방정식">
      만약에 귀뚜라미가 우는 시간/횟수, 나이 3가지 특성에 영향을 받는 경우에는 위와 같은 방정식이 나옴  
      

