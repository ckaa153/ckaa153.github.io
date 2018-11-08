---
layout: post
title: Bigdata Analysis For Management _ ch05
tags: [Big Data, Data Analysis, Business Administration, SangMyung University, Republic of Korea]
comments : true
Data Visualization & AWS: <!--more-->
---
## Data Analysis Process
 : Server에 누적된 데이터와 실시간으로 발생되는 데이터를 병합하여 처리
 
- Python을 통해 데이터를 수집하고, String 연산, 정규표현식 등을 활용하여 CSV 파일로 정제
- 일반 Desktop에서 다루기 어려운 규모의 Data는 Linux Server 통해 Data Handling
- Python의 ggplot 또는 Tableau 등으로 Data Visualization

![dp1](/assets/img/pexels/dp1.jpeg)


## Confusion Matrix & F1-Measure
Q. 정상이 99.95%이고 0.05%만 암에 걸린다 했을 때, 모두 정상인으로 판단할 때 정확도는?

- 단순히 정확도 만으로는 데이터 분석의 성능을 올바로 측정하기 어렵다
- Data Balancing을 맞추어야 통계학적으로 설명력(Power)이 세진다

![cf1](/assets/img/pexels/cf1.jpeg)


## K-fold Test & Overfitting(과적합)
 : Training / Test set / Validation Set 을 나누어 훈련,테스트,검증 과정을 K회 진행하여 성능을 도출

![kf1](/assets/img/pexels/kf1.jpeg)

- Sample의 분화
	1. Training Set 모델 만들 때 사용
	2. Validation Set 모델 조정 위해 사용
	3. Test Set 모델의 최종 평가 위해 사용

![kf2](/assets/img/pexels/kf2.jpeg)

> 교차검증시 2차 데이터(외부 데이터)를 사용하는 것이 제일 좋음

![kf3](/assets/img/pexels/kf3.jpeg)

- 3번은 너무 최적화 되어 있어서 학습효과가 발생할 수 없음 => Overfitting 발생
- Overfitting 을 막기 위해 Training Set, Test Set, Validation Set으로 분할

> 충분한 교차 검증을 거치지 않을 경우, Training Set에만 최적화 되는 Overfitting 발생


## Tableau
 : BI(Business Intelligence) Tool 로써 시각화 통해 Insight 발굴
- BI : Fact와 Fact 기반 시스템을 통해 비즈니스 의사결정을 향상시킬 수 있는 개념과 방법론의 집합
- 여러 곳에 산재되어 있는 데이터를 수집하여 체계적이고 일목요연하게 정리
- 사용자가 필요로 하는 정보를 정확한 시간에 제공할 수 있는 환경
