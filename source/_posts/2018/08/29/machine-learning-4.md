---
title: Machine Learning(ML) - 텐서플로우 첫걸음
date: 2018-08-29 20:24:13
tags: 
    - 머신러닝 단기집중과정
category: 
    - 머신러닝 단기집중과정
---

본 게시물은 {% link 구글 머신러닝 단기집중과정 스터디 [https://developers.google.com/machine-learning/crash-course/?utm_source=DevRel&utm_medium=StudyJam&utm_campaign=q1y2018&utm_term=&utm_content=mlcc] [구글 머신러닝 단기집중과정 스터디] %}을 참고하여 작성되었습니다.

<!-- toc -->

## 텐서플로우 첫걸음
  드디어 머신러닝의 꽃, 텐서플로우!
  간단하게 살펴보자

### 텐서플로우 계층구조
  <img src="/2018/08/29/machine-learning-4/figure1.JPG" width="400" height="400" alt="Figure 1 : 계층 구조">
  
  * 에스티메이터(tf.estimator)
    * 간단히 텐서플로우에서 제공하는 함수를 사용 
  * tf.layers/tf.losses/tf.metrics
    * 커스텀할 수 있도록 라이브러리를 재사용할 수 있게 제공(함수가 동작하면서 로그를 찍을 수 있도록 수정하는 등)
  * 텐서플로우
    * 특정 플랫폼에서 좀 더 효율적이게 할 수 있도록 커널까지 접근할 수 있는 구조.(학습을 인텔 CPU에 맞게 GPU에 맞게 설정)
    * 요소
      * 자바 컴파일러 및 JVM과 유사함
      * JVM이 여러 하드웨어 플랫폼에서 구현되는 것처럼 텐서플로우도 여러 CPU, GPU에서 구현 가능
      * 종류
        * 그래프 프로토콜 버퍼
        * 분산된 그래프를 실행하는 런타임

## 실습
### 자주 사용하는 변수
  * 초매개변수
    * steps : 총 학습 반복 횟수. 한 단계에서 한 배치의 손실을 계산 후, 이 값을 사용하여 모델의 가중치를 한번 수정함
    * batch size : 하나의 단계와 관련된 예시의 수.(랜덤 선택) 확률적 경사하강법의 batch size는 1.
    {% codeblock %}
    학습된 예시의 전체 수 = batch size * steps
    {% endcodeblock %}
  * 변수
    * periods : 보고의 세부사항을 제어. 학습에 영향을 주지 않는 값.
      * steps = 70, periods = 7 : 실습에서 10단계 or 7번마다 손실 값을 출력함
    
### 판다스(Pandas)
  
  
### 텐서플로우(TensorFlow)