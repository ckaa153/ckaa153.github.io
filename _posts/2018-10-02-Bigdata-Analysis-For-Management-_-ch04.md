---
layout: post
title: Bigdata Analysis For Management _ ch04
tags: [Big Data, Data Analysis, Business Administration, SangMyung University, Republic of Korea]
Version Control: <!--more-->
---
## Version Control
 : 버전 관리 시스템은 파일 변화를 시간에 따라 기록했다가 나중에 특정 시점의 버전을 다시 꺼내올 수 있는 시스템
- SW 형상 관리의 일환으로 소스 코드 관리는 개발에서 필수적
- 중앙 집중형 / 분산형 존재


## Git과 SVN의 차이점
: Git은 분산 저장식 버전관리 시스템
: SVN은 중앙 집중식 버전관리 시스템
- 분산저장식 vs 중앙집중식 (좌측 = git, 우측 = SVN)

![git과svn작동방식차이](/assets/img/pexels/git과svn작동방식차이.jpg)

- 가장 큰 차이 : SVN은 네트워크가 연결되어 있지 않으면 사용 못함
- 논리적 단위의 차이 : SVN = Snapshot , Git = Commit
- Git은 변경되지 않은 파일에 대해서는 파일 자체가 아니라 Link 활용


## Git 동작 원리
 : GIT은 파일을 'Committed - Modified - Staged' 상태로 관리


## Git Flow
 : 일반적으로 SW를 유지보수함에 있어서 아래와 같은 Git Flow 구조 사용
 
![gitflow1](/assets/img/pexels/gitflow1.jpg)

- 특정 타겟에 대한 지능적이고 지속적인 위협인 APT 공격에 제로데이 취약점 공격이 자주 사용됨
	- '무방비 시간대'가 위협이 개시된 시점과 프로그램 제작자가 패치를 내놓는 시점 사이에 존재할 때 발생
	- 새로운 위협/바이러스 출현
	  -> 발생한 위험/바이러스에 대한 보고, 분석
      -> 새로운 솔루션 개발
      -> 새로운 패치/업그레이드 된 시그니처 배포
      -> 유저 시스템에 패치 배포 및 설치 또는 바이러스 DB 업데이트

## Git의 명령어
1. Init : Git의 Repository를 초기화
2. Status : Git의 Repository의 현재 상태를 조회
3. Add : Working Director에 있는 파일들을 Staging Area로 추가
4. Commit : Staging Area에 잇는 파일들을 Repository에 추가
5. Log : 이전에 작성한 Commit이나, 파일의 변경 이력들을 추적
6. Diff : 이전 Commit과 현재 Commit/Directory의 비교
7. Branch : 개발을 병렬적을 진행
8. Tag : 특정 시점에 태킹처리 Release 버전 지정
9. Checkout : Branch를 이동하거나 특정파일을 다운로드
10. Merge : 병렬적으로 진행한 Branch를 하나로 병합


## Pull Request 단계
	1단계 ; Fork - 원작자의 저장소 복제
    2단계 : Clone - 원격저장소를 로컬 저장소로 다운
    3단계 : Branch - Master Branch에서 Develop 또는 다른 작업을 할 Branch 생성
    4단계 : Checkout - 작업할 Branch로 변경
    5단계 : Source Change - 수정이 필요한 부분의 소스 변경
    6단계 : Commit - 변경한 소스를 로컬 저장소에 저장
    7단계 : Push - 로컬 저장소의 작업 Branch를 원격 저장소로 업로드
    8단계 : Pull Request - 변경 사항을 원작자에게 원본 소스에 반영 요쳥 송신
