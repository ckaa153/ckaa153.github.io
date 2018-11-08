---
layout: post
title: Bigdata Analysis For Management _ ch02
tags: [Big Data, Data Analysis, Business Administration, SangMyung University, Republic of Korea]
comments : true
Hello Python!: <!--more-->
---
## Anaconda
- Jupyter 라는 Web 기반 Notebook Interface를 지닌 커널 변경이 가능한 개발 환경 함께 제공
- 문서에 코드를 바로 넣어 실행해 볼 수 있음
- 리눅스 기반 서버에 설치하여 다른 컴퓨터에서도 사용 가능 (Jupyter Hub)
- Spyder 라는 통합 개발환경(IDE) 지원

## SublimeText 2
- 대부분의 프로그래밍 언어의 문법 강조 기능 지원
- 가벼운 코드 Editor를 급하게 사용할 때 편리

## What is Python?
- 배우기 쉽고, 강력한 프로그래밍 언어
- 효율적인 고수준 데이터 구조
- 간단하지만 효과적인 객체 지향 프로그래밍 접근법
- 우아한 문법과 동적 타이핑, 그리고 인터프리팅 환경
- 다양한 플랫폼에서 사용될 수 있는 최적의 스크립팅 언어

1. 인터프리터 언어
	- 인터프리터가 Line By Line 으로 실행되는 타이밍에 코드를 실행하는 방식
	- Python에서는 바이트코드라는 중간 형태로 변환 뒤 인터프리터에서 실행
	- 컴파일 언어에 비해 속도가 느림

2. 동적타이핑 (Dynamic Typing)
	- Python은 실행시간에 자료형을 검사하여, 동적으로 타입이 지정
	- 변수선언 시점에 해당 자료형을 명시할 필요 없음

3. 우아한 문법위한 Codeing Convertion
	- Coding Convertion은 프로그램을 작성할 때 특정 스타일을 지칭
		- 협업과 가독성을 위해 하나의 일관성 있는 스타일 사용을 지칭
	- Python은 Coding Block 구분을 들여쓰기로 함(필수)
	- 들여쓰기는 Space Bar 4개로 하는 것을 권장
	
4. Naming
	- 스테이크 형식 : module_name, package_name etc.
	- 카멜 형식 : ClassName, ExceptionName etc.
	- 그 외 : GLOBAL_CONSTANT_NAME etc.

5. 피해야 할 사항
	- 카운터나 interator의 예외에 하나의 Character 사용
	- Package나 Module 명에 dash(-) 쓰는 것
	- Python 예약어를 따로 선언하는 것 ex)_self_


### The Zen of Python
	- Beautiful is better than ugly (아름다운 것이 추한 것보다 낫다)
	- Explicit is better than implicit (명시적인 것이 암시적인 것보다 낫다)
	- Simple is better than complex (단순한 것이 복잡한 것보다 낫다)
	- Complex is better than complicated (내부적으로 복잡한 것이 외부적으로 복잡한 것보다 낫다)

## Docker
1. 개발자가 MAC을 쓰는 이유
	- MacOS와 Linux는 같은 BSD Unix 계열

2. 항상 Guest OS 띄우는 가상머신과 달리 Docker Engine으로 통합하여 성능 향상
	- host OS에서 개발 환경 등을 통째로 변경하지 않고 Container화 시켜서 다른 컴퓨터로 배포 가능
	- 기존에 개발환경에 영향 주지 않으면서 개발 환경 구축 가능
	- Backend 환경에서만 가능한 작업들이 상당 수 Docker에서 작업 가능

3. Window에서 구동되는 Docker는 VirtualBox 기반의 Linux VM에서 작동
