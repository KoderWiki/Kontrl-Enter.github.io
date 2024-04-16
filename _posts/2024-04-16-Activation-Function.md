---
layout: post
title: Activation Function, What is it? (한국어)
tags: [ANN, CSE, Data Science, AI, 한국어]
feature-img: "assets/img/0.post/2024-04-16/header.png"
thumbnail: "assets/img/0.post/2024-04-16/header.png"
categories: CSE, AI
---

&emsp;**활성화 함수**(Activation function)란 **퍼셉트론**(Perceptron)의 출력값을 결정하는 함수이다. 많은 종류의 활성화 함수가 존재하고, 활성화 함수의 결정이 결과값에 크게 영향을 준다. 인공신경망 관련 글은 [**이곳**](https://koderwiki.github.io/cse/2024/04/12/ANN.html) 참조

![image](https://github.com/KoderWiki/koderwiki.github.io/assets/153072257/7aed300d-0621-407a-8829-43362d7f0f3a)


## 선형(Linear)과 비선형(Non-Linear)

#### 선형함수 (Linear Function)

**선형함수**(Linear Function)는 말 그래도 직선적인 함수(y=x)이다. 

![image](https://github.com/KoderWiki/koderwiki.github.io/assets/153072257/c96eb0e7-d786-4d6b-8d03-ebd4f72e82b0)

하지만 퍼셉트론에서 값을 받고 다른 계층(Layer)로 전달할 때 연속성 있는 **비선형(non-linear)함수**를 사용한다. 비선형 함수를 사용하는 이유는 선형함수를 활성화 함수로 하게 되면 **심층 신경망**(Deep Neural Network)에 큰 도움이 되지 않기 때문이다. 선형 함수를 사용하게 되면, 여러 계층을 통과하는 결과 값을 단 하나의 계층으로 표현할 수 있게 되면서 **신경망을 깊게 쌓는 의미가 사라진다**. 아래의 그림으로 예를 들어보자.

![image](https://github.com/KoderWiki/koderwiki.github.io/assets/153072257/78748302-97d5-46a0-8566-f05a319ae4d3)

2개의 계층을 쌓아봤지만, X에 곱해지는 항들은 W로 치환 가능하고, 입력과 무관한 상수들은 전체를 B로 치환 가능하기 때문에 WX + B라는 **동일한 결과**를 낸다.



