---
layout: post
title: Bigdata Analysis For Management _ ch03
tags: [Big Data, Data Analysis, Business Administration, SangMyung University, Republic of Korea]
Variables and Operators: <!--more-->
---
## LR : Language Rule
 : 문법적인 사항으로 필수적으로 지켜야 할 부분
	- Default iterators and Operators : 기본 iterator와 연산자 쓸 것 / 연산자 오버로딩 하지말 것
	- Imports : 모듈과 패키지에만 사용할 것 / 상대적 경로 아닌 Full Path 쓸 것
	- Packages : 각 모듈과 패키지를 Full Pathname을 사용할 것

## SR : Style Rule
 : 컨벤션에 가까움
	- Imports Formatting : Import 할 때는 라인을 분리한다.
	- Indentation : 탭을 사용하지말고 띄어쓰기 4개로 사용할 것 / 들여쓰기는 수직열이 맞아야 함
	- Whitespace : 괄호사이, 파라미터 리스트, 인덱스, 슬라이싱에 공백 X

## Format String
	: raw_input()

- 파라미터 (변수형식)
	- %d (정수형 10진수 상수/integer)
	- %f (실수형 싱수/float)
	- %lf (실수형 상수/double)
	- %c (문자 값/char)
	- %s (문자 스트링/(const)(unsigned) char *)
	- %u (양의 정수/10진수)
	- %o (양의 정수/8진수)
	- %x (양의 정수/16진수)
	- %s (a문자열)
	- %n (쓰인 총 바이트 수/* int)
	- %hn (%n의 반인 2바이트 단위)

## Parameter vs Argument
1. 전역변수
	- 프로그램 시작 시 초기화되어 종료 시까지 할당된 메모리를 유지하는 변수
    - 모든 함수가 함께 사용 가능
    - 같은 이름의 전역 변수는 하나 이상 사용할 수 없음

2. 지역변수
	- 함수 또는 어떤 블록 안에 정의된 변수
	- 사용 범위가 함수 내부로 제한
	- 함수가 호출되면 생성되었다가 리턴하면서 소멸
	- 서로 다른 함수에 같은 변수명 사용 가능

3. 매개변수
	- 두 개 이상의 변수 사이의 함수 관계를 보조 변수 사용하여 간접적으로 표시할 때, 그 보조 변수를 칭함


## 변수의 타입
1. 정수형(integer) : 정수를 뜻하는 자료형
2. 실수형(Floating-point) : 소수점이 포함된 숫자
3. 8진수(Octal) : 8진수 만들기 위해서는 숫자가 0o 또는 0O로 시작
4. 16진수(Hexadecimal) : 16진수 만들기 위해서는 숫자가 0x로 시작


## Type Casting
- C의 ++,-- 연산은 Python에서는 + = 1, - = 1 로 고쳐 사용
- Python은 일관성과 가독성을 중시하는 언어
- Operator의 종류
	: -**,-,+,*,/,%,//,+=,>>,<<,&,^,|,<=,<,>,>=,!=,==
    
    
## 비트연산자
- 활용도 : 다중 선택 옵션 등에 활용
- 시간 복잡도 & 공간 복잡도
- Operator
	1. & : AND 연산, 둘 다 참일 때만 만족
	2. | : OR 연산, 둘 중 하나만 참이어도 만족
	3. ^ : XOR 연산, 둘 중 하나만 참일 때 만족
	4. ~ : 보수 연산
	5. << : 왼쪽 시프트 연산, 변수의 값을 왼쪽으로 지정된 비트 수 만큼 이동
	6. >> : 오른쪽 시프트 연산, 변수의 값을 오른쪽으로 지정된 비트 수 만큼 이동



# Markdown & Jekyll

## Jekyll
- 정적인 웹페이지 만들어주는 유틸리티 (MAC만 공식 지원)
