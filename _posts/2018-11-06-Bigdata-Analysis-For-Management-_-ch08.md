---
layout: post
title: Bigdata Analysis For Management _ ch08
feature-img: "assets/img/pexels/Grand-Canal-Venice-Italy.jpeg"
thumbnail: "assets/img/thumbnails/Grand-Canal-Venice-Italy.jpeg"
tags: [Big Data, Data Analysis, Business Administration, SangMyung University, Republic of Korea]
OOP: <!--more-->
---
## OOP = Object Oriented Programming (객체 지향 프로그래밍)
- OOP 는 컴퓨터 프로그램을 명령어의 목록으로 보는 시각에서 벗어나 여러 개의 독립된 단위, '객체'들의 모임으로 파악하고자 하는 것
- Class는 선언 시 파스칼 표기법을 따름
- \__init__ 메소드 = 객체가 생성될 때 초기화에 사용


        class Person :
            def say_hi(self):
                print ('Hello, how are you?')

          p = Person()
          p.say_hi()
          -> class 안에 선언된 함수는 Method 라 부름


#### Method
1. 인스턴스 Method : 파라미터로 self를 사용 & 각 개별 객체의 attribute 조작시 사용
2. 클래스 메소드 ; 파라미터로 ds 사용 & @dassmethod 데코레이터와 함께 사용 & 객체 간 공유하는 attribute 조직 시 사용
3. 스태틱 메소드 : 일반 함수와 동일 하나 @staticmethod 데코레이터가 붙어있고 편의를 위해 존재


#### Polymorphism(폴리모피즘)
: 프로그램 언어의 다형성(Polymorphism)은 그 프로그래밍 언어의 자료형 체계의 성질을 나타내는 것으로, 프로그램 언어의 각 요소들이 다양한 type에 속하는 것이 허가되는 성질을 가리킴


#### Overloading & Overriding
1. Overloading : 같은 메소드 네임이나 파라미터의 개수나 타입에 따라 다르게 지정
2. Overridng : 상속관계에서 하위 클래스가 상위 클래스의 같은 이름의 메소드를 재지정


#### Encapsulation (캡슐화)
- Encapsulation(캡슐화)이 되어 있으면, 동시에 여러 군데에서 리소스를 사용할 수 있으나, Encapsulation이 되어 있지 않으면 조각조각 되있어서 제대로 사용할 수 없게 됨


#### 다중상속
: 상속 튜플에 하나 이상의 Class가 등록되어 있을 경우


## Activity

          # -*- coding: utf-8 -*-

          class Car:
              def __init__(self, model_name):
                  self.model_name = model_name

              def stop(self):
                  print "엔진을 정지합니다."

              def start(self):
                  print "엔진을 가동합니다."

              def run(self):
                  print "정속 운행을 합니다."

              def break_pad(self):
                  print "브레이크를 밟습니다."

              def get_car_name(self):
                  print self.model_name + "이(가) 달립니다."

          class ElectricCar :
              def __init__ (self,model_name):
                  self.model_name = model_name

              def stop(self) :
                  print "모터를 정지합니다."

              def start(self) :
                  print "모터를 가동합니다."

              def run(self) :
                  print "운행을 시작합니다."

              def breakpad(self) :
                  print "브레이크를 밟습니다."
                  print "배터리를 충전합니다."

              def get_car_name(self):
                  print self.model_name + "이(가) 달립니다."

          class HybridCar(Car,ElectricCar):
              def __init__ (self,model_name):
                  self.model_name = model_name

              def stop(self):
                  Car.stop(self)

              def start(self):
                  ElectricCar.start(self)
                  Car.start(self)

              def run(self):
                  Car.run(self)

              def breakpad(self):
                  ElectricCar.breakpad(self)

              def get_car_name(self):
                  print self.model_name + "이(가) 달립니다."

          def main():
              print "메인함수입니다."
              oilcar = Car("아반떼")
              oilcar.get_car_name()
              oilcar.stop()
              oilcar.start()
              oilcar.run()
              oilcar.break_pad()
              print "--------------------"
              ELcar = ElectricCar("아이오닉")
              ELcar.get_car_name()
              ELcar.stop()
              ELcar.start()
              ELcar.run()
              ELcar.breakpad()
              print "--------------------"
              HYcar = HybridCar("넥쏘")
              HYcar.get_car_name()
              HYcar.stop()
              HYcar.start()
              HYcar.run()
              HYcar.breakpad()

          if __name__ == '__main__':
              main()

              ->

          메인함수입니다.
          아반떼이(가) 달립니다.
          엔진을 정지합니다.
          엔진을 가동합니다.
          정속 운행을 합니다.
          브레이크를 밟습니다.
          --------------------
          아이오닉이(가) 달립니다.
          모터를 정지합니다.
          모터를 가동합니다.
          운행을 시작합니다.
          브레이크를 밟습니다.
          배터리를 충전합니다.
          --------------------
          넥쏘이(가) 달립니다.
          엔진을 정지합니다.
          모터를 가동합니다.
          엔진을 가동합니다.
          정속 운행을 합니다.
          브레이크를 밟습니다.
          배터리를 충전합니다.
