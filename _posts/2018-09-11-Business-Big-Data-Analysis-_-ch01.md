---
layout: post
title: Business Big Data Analysis _ ch01
tags: [Big Data, Data Analysis, Business Administration, SangMyung University, Republic of Korea]
Definition of BigData: <!--more-->
---
## What is BigData?
	기존 방식으로 저장/관리/분석하기 어려울만큼 큰 규모의 자료

1. 기존의 방식이란 특정 용량을 의미하는 것은 아니다.
2. 데이터에 결합된 정보의 복잡성과 분석과정에서 요구되는 속도도 기존의 의미와 구별된다.
3. "BigData"의 의미는 "특정용량"이상의 데이터가 아니라 "데이터의 크기 자체가 문제가 될 때"를 의미한다.
>오늘의 Big이 다음주엔 Small이 될 수 있음
    
## Waht is Big Data?
	1. DB의 규모에 초점을 맞춘 정의 (McKinsey, 2011)
	2. DB가 아니라 업무 수행에 초점을 맞춘 정의 (IDC, 2011)

## Big Data's 3Vs & 6Vs
	1. 3Vs : Velocity(속도), Volume(규모), Variety(다양성)
	2. 6Vs : 3Vs + Veracity(진실성), Variability(가변성), Visualization(시각화)

## BigData Analysis Process
	1단계 : 데이터 창출 (생산자)
	2단계 : 데이터 획득 (설계가, 엔지니어)
	3단계 : 정보 처리 (분석가, 과학자)
	4단계 : 비즈니스 프로세스 (최종 사용자)
    
![빅데이터분석과정](/assets/img/pexels/빅데이터분석과정.jpeg)
    
# 3Vs of Big Data

## Variety(다양성)
	기존 내부 데이터 + 외부 데이터의 폭증 & Iot서비스 데이터
    
* 최근 개인이 생산해내는 데이터의 양과 종류가 증가 (개인 데이터 증가)
* 기존 분석 어려운 비정형 데이터 분석 기법까지 등장 -> 분석가능 데이터 종류 다양해짐
* Big Data 이용 시스템이 오픈 소스로 공개
* GPGPU 기술 도입 -> 연신속도 비약적으로 향상

![gpgpu1](/assets/img/pexels/gpgpu1.jpeg)


## Volume

##### Google File System
: 다수의 저사양 PC를 하나의 슈퍼컴퓨터처럼 사용하는 분산컴퓨팅 기술
##### Hadoop Distributed File System
: 야후와 아파치 재단이 구글의 GFS을 참조하여 만들어 오픈소스화 한 것

	하둡 도입 이후
    	1. 분석시간이 3일에서 3시간으로 단축
    	2. 데이터 활용 규모 2TB에서 15TB로 증가

##### Spark
- 기존 HDFS에서 발생한 I/O속도 저하를 Imutable In-Memory 활용하여 획기적인 속도 향상 구현
		1. RAM을 ROM처럼 활용
- 기존 HDFS에 비해 시스템 구성이 간결하고 Interface가 뛰어나 리소스 도입비용 측면에서 강점
		1. Java, Python 등을 SDK에 제공하여 기존 개발자 학습비용 낮춤
		2. Spark는 Spark만으로도 많은 것을 할 수 있음
		3. SSD와 마찬가지로 RAM의 전반적인 가격 하락

#### CAP 이론
1. AP에 해당하는 Cassandra DB와 주로 사용되어 현재 빅데이터 분석의 메인스트림으로 자리잡음
2. Databases and CAP Theorem
	- Consistency (일관성) : 모든 사용자는 항상 동시에 같은 데이터 조회
	- Availability (가용성) : 모든 사용자는 항상 Read/Write 할 수 있으며 몇몇 노드 장애시에도 다른 노드들의 작동을 보장
	- Partition Tolerance (파티션 내용성) : 물리적으로 분산된 네트워크상에서 메시지 손실로 인한 부분적 결합이 있어도 자동복구되어 정상적으로 작동


## Velocity

- 뇌 스캐너가 정밀하게 발달하면서 암진단을 위한 분석시스템의 필요에 의하여 GPGPU 개념 등장

##### GPGPU
- CUDA는 오픈소스지만 NVIDA 그래픽 카드에서만 작동하여 하나의 Ecosystem 형성
- Google 알파고에도 GPGPU 기술 활용

###### 알파고
1. 승률과 기보를 사용하면서 강화학습(딥러닝) 기반의 Monte Carlo Tree Search 알고리즘 활용
2. Tic-Tac-Toc 빙고 게임의 원리를 이용


## Big Data Business Model

#### Big Data Business Opportunity
: 디지털 고객 가치 추구에 빅데이터 경쟁력 활용하면 새로운 비즈니스 기회 모색 가능

1. 빅데이터의 문제 해결 방법과 새로운 비즈니스
2. 독점기업의 이윤
	- 빅데이터 비즈니스 모델의 경쟁력은 차별화된 특징, 독점성, 저비용 측면 존재
	- 저렴한 비용으로 자신만이 보유한 데이터를 차별화된 방법으로 분석하여 경쟁력 확보하는 것
	
![독점기업이윤](/assets/img/pexels/독점기업이윤.jpeg)

#### Feature of Data
: 데이터의 깊이, 길이, 폭, 시점
- 데이터는 필요에 따라 매우 상세
- 과거로부터 현재까지 어떤 변화가 있었는지 자세히 보여줌
- 관심 주제 혹은 의사결정 사안에 대한 모든 이슈 다뤄야 됨
- 이용자가 필요로 하는 특정 시점의 데이터가 있어야 함

#### 5 Type of Big Data Business Model
1. 빅데이터 비즈니스맨
	: 상업적 활용이 가능한 데이터가 많은 기업에서 데이터를 활용 방안 모색
    
2. 빅데이터 창줄자
	: 데이터 창출, 가공, 분석해서 새로운 정보와 지식을 만들어내는 기술 전문가
    
3. 빅데이터 대리인
	: 데이터 관리를 전문적으로 하는 사람
    
4. 빅데이터 연구가
	: 특정 분야, 산업의 지식에 정통하여 자신의 전문 분야에 데이터를 활용하는 사람
    
5. 빅데이터 응용가
	: 기존 서비스에 빅데이터를 이용하여 차별적인 스마트 서비스로 변모시키는 사람
