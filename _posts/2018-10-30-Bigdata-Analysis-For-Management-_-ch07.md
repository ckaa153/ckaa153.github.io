---
layout: post
title: Bigdata Analysis For Management _ ch07
feature-img: "assets/img/pexels/desk-top.jpeg"
thumbnail: "assets/img/thumbnails/desk-top.jpeg"
tags: [Big Data, Data Analysis, Business Administration, SangMyung University, Republic of Korea]
Data Structure & File IO & Excpetion: <!--more-->
---
## Review

#### 재귀함수

	def factorial(a):
    	if a == 1:
        	return 1
        else :
        	return a * factorial(a-1)
    
    	print factorial(3)


## Data Structure

#### List
- 순서대로 정리된 비정적mutable 자료구조
- List 초기화시 [ ] 사용
- append( ) 와 sort( )
- del = 삭제할 때

		shoplist = ['apple', 'mange', 'carrot', 'banana']

		print 'I have', len(shoplist), 'items to purchase.'

		print 'These items are:',
		for item in shoplist:
			print item,

		print '\nI also have to buy rice.'
		shoplist.appen('rice')
		print 'My shopping list is now', shoplist

		print 'I will sort my list now'
		shoplist.sort( )
		print 'Sorted shopping list is', shoplist

		print 'The first item I will buy is', shoplist[0]
		olditem = shoplist[0]
		del shoplist[0]
		print 'I bought the ', olditem
		print 'My shopping list is now', shoplist
    
    
#### Tuple
- 여러 개의 객체를 모아 담은 정적mutable 자료구조(순서 있음)
- new_zoo[2][2] 인덱싱 연산자
- 튜플을 초기화 할 때 괄호 사용 ( )


		zoo = ('python', 'elephant', 'penguin')
		print 'Number of animals in the zoo is', len(zoo)

		new_zoo = 'monkey', 'camel', zoo
		print 'Number of cage in the new zoo is', len(new_zoo)
		print 'All animals in new zoo ar', new zoo
		print 'Animals brought from old zoo are', new_zoo[2]
		print 'Last animal brought from old zoo is', new_zoo[2][2]
		print 'Number of animals in the new zoo is', /len(new_zoo)-1+len(new_zoo[2])
    
    
#### Dictionary
- Dictionary 초기화에 { }사용
- Key 와 Value 가 쌍으로 이루어짐

		ab = {'Swaroop'   : 'swaroop@swaroopch.com', 'Laryy'     : 'larry@wall.org', 'Matsumoto' : 'matz@ruby-lang.org', 'Spammer'   : 'spammer@hotmail.com'}

		print "Swaroop's address is", ab['Swaroop']

		del ab['Spammer']

		print '\nThere are {} contacts in the address-book\n'.format(len(ab))

		for name, address in ab.items():
			print 'Contact { } at { } '.format(name,address)

		ab['Guido'] = 'guido@python.org'

		if 'Guido' in ab:
		print "\nGuido's address is", ab['Guido']

		print ab

		->

		(result)
		Swaroop's address is swaroop@swaroopch.com

		There are 3 contacts in the address-book

		Contact Swaroop at swaroop@swaroopch.com
		Contact Matsumoto at matz@ruby-lang.org
		Contact Larry at larry@wall.org

		Guido's address is guido@python.org
		{'Swaroop': 'swaroop@swaroopch.com', 'Matsumoto': 'matz@ruby-lang.org', 'Larry': 'larry@wall.org', 'Guido': 'guido@python.org'}
    

#### SET
- 집합은 정렬되지 않은 단순 객체의 묶음
- 중복을 허럭하지 않음
- Membership test 수행 가능
- 한 집합이 다른 집합의 부분 집합인지 알 수 있음
- 교집합 구할 수 있음


		bri = set(['brazil', 'russia', 'india'])

		print bri
		print type(bri)

		print 'india' in bri
		print 'usa' in bri

		bric = bri.copy()
		bric.add('china')
		bric.add('china')
		print bric.issuperset(bri)

		bri. remove('russia')
		print bri
		print bric

		print bri & bric

		->

		(result)
		set(['brazil', 'india', 'russia'])
		<type 'set'>
		True
		False
		True
		set(['brazil', 'india'])
		set(['brazil', 'china', 'india', 'russia'])
		set(['brazil', 'india'])



#### Stack
- Stack은 Data 입/출력이 한쪽으로만 접근할 수 있는 자료 구조
	- 가장 나중에 들어간 Data가 제일 먼저 나옴(LIFO 구조 : Last In First Out)
- Stack을 조작하는 동작은 Data를 넣은 Push 동작과 Data를 빼오는 POP 동작 존재
	- Push는 Stack 최상단 Data 위에 새로운 Data 쌓음
	- POP는 Stack의 최상단에 있는 Data를 빼옴



			def main():
			stack = [ ]
			stack.append(1)
			stack.append(2)
			stack.append(3)
			stack.append(4)
			print stack

			while stack:
				print "POP >", stack.pop( )

			if __name__ == '__main__' :
				main()
		
        
#### Queue
- Queue는 먼저 넣은 Data가 먼저 나오는 구조(FIFO 구조 : First in First Out)
- Queue는 LIFO 구조인 Stack과 반대되는 개념
- Queue는 입/출력 부분이 양쪽에 존재
- 한 쪽은 Data 넣기만 함 -> PUT 동작
- 한 쪽은 Data 빼기만 함 -> GET 동작


#### Mutable(변함) vs Immutable(변하지X)
- 숫자형(Number) = Immutable
- 리스트(List) = Mutable
- 사전(Dictionary) = Mutable
- 문자열(String) = Immutable
- 튜플(Tuple) = Immutable

#### Indextion & Slicing
	
	    shoplist = ['apple', 'mango', 'carrot', 'banana']
	    name = 'swaroop'

	    # Indexting or 'Subscription' operation #
	    print 'Item 0 is', shoplist[0]
	    print 'Item 1 is', shoplist[1]
	    print 'Item 2 is', shoplist[2]
	    print 'Item 3 is', shoplist[3]
	    print 'Item -1 is', shoplist[-1]
	    print 'Item -2 is', shoplist[-2]
		print 'Charactor 0 is', name[0]
	    ->
	    (result)
	    Item 0 is apple
	    Item 1 is mango
	    Item 2 is carrot
	    Item 3 is banana
	    Item -1 is banana
	    Item -2 is carrot
	    Charactor 0 is s



	    # Slicing on a List #
	    print 'Item 1 to 3 is', shoplist[1:3]
	    print 'Item 2 to end is', shoplist[2:]
	    print 'Item 1 to -1 is', shoplist[1:-1]
	    print 'Item start to end is', shoplist[:]
	    ->
	    (result)
	    Item 1 to 3 is ['mango', 'carrot']
	    Item 2 to end is ['carrot', 'banana']
	    Item 1 to -1 is ['mango', 'carrot']
	    Item start to end is ['apple', 'mango', 'carrot', 'banana']



	    # Slicing on a String #
	    print 'Characters 1 to 3 is', name[1:3]
	    print 'Charactors 2 to end is', name[2:]
	    print 'Charactors 1 to -1 is', name[1:-1]
	    print 'Charactors start to end is', name[:]
	    ->
	    (result)
	    Characters 1 to 3 is wa
	    Charactors 2 to end is aroop
	    Charactors 1 to -1 is waroo
	    Charactors start to end is swaroop
    

#### Random

	    import random

	    print random.random()

	    print random.randrange(1,7)

	    # 순서형 자료 섞는 역할
	    abc = ['a', 'b', 'c', 'd', 'e']
	    print abc

	    random.shuffle(abc)
	    print abc

	    # 재정렬
	    abc.sort()
	    print abc

	    ->

	    (result)
	    0.927379293707
	    5
	    ['a', 'b', 'c', 'd', 'e']
	    ['b', 'd', 'e', 'a', 'c']
	    ['a', 'b', 'c', 'd', 'e']

#### Find & Delimiter
- Membership text 'In' 과 'Not In' 연산

	    name = 'Swaroop'

	    if name.startswith('Swa'):
		print 'Yes, the string starts withe "Swa"'

	    if 'a' in name:
		print 'Yes, it contains the string "a"'

	    if name.find('war') != -1:
		print 'Yes, it contains the string "war"'

	    delimiter = '_*_'
	    space_char = ', '
	    myList = ['Brazil', 'Russia', 'Indida', 'China']
	    print delimiter.join(myList)
	    print space_char.join(myList)

	    ->

	    (result)
	    Yes, the string starts withe "Swa"
	    Yes, it contains the string "a"
	    Yes, it contains the string "war"
	    Brazil_*_Russia_*_Indida_*_China
	    Brazil, Russia, Indida, China


#### List Comprehension
- 한 List의 모든 원소 각각에 어떤 함수 적용 후, 그 반환값을 원소로 가지는 다른 List를 쉽게 생성(Mapping)


	    a_list = [1, 9, 8, 4]
	    print ([elem * 2 for elem in a_list])
	    print (a_list)
	    a_list = [elem * 2 for elem in a_list]
	    print (a_list)

	    ->

	    (result)
	    [2, 18, 16, 8]
	    [1, 9, 8, 4]
	    [2, 18, 16, 8]


#### Dictionary & Set Comprehension
- Dictionary Comprehension은 입력 Sequence로부터 지정된 표현식에 따라 새로운 Dictionary 컬렉션을 Build
- {출력표현식 for 요소 in 입력Sequence [if 조건식]}



## File I/O & Exception Handling

#### Exception Handling
- 오류 vs 예외 vs 버그
	1. 버그(Bug)
		- 프로그래머에 의한 에러
	2. 에러(Error)
		- 응용 프로그램의 사용자에 의해서 발생
	3. 예외(Exception)
		- 런타임 오류와 관련된 것 -> 예방 어렵거나 불가능한 것
- 기본 구조
	1. try & except 문
	
			try :
				.....
			except [발생 오류[as 오류 메시지 변수]]
				.....
			
	2. try ... else 문
	
			try :
				f = open('foo.txt', 'r')
			except FileNotFoundError as e :
				print(str(e))
			else :
				data = f.read( )
			f.close()
		
	3. try ... finally 문
	
			f = open('foo.txt', 'w')
			try :
				# 무언가를 수행한다
			finally :
				f.close( )
				
	4. 여러개의 오류 처리하기
	
			try :
				.....
			except 발생 오류 1:
				.....
			except 발생 오류 2:
				.....
	
	5. 오류 회피하기
	
			try :
				f = open("나 없는 파일", 'r')
			except FileNotFoundError :
				pass

	6. 오류 일부러 발생시키기
	
			class Bird :
				def fly(self) :
					raise NotImplementedError


## File I/O

#### Raw_input()
	def reverse(text) :
    	return text[::-1]

   	def is_palindrome(text) :
        	return text == reverse(text)

    	something = raw_input("Enter text: ")
    	if is_palindrome(something) :
        	print "Yes, it is a palindrom"
    	else :
        	print "No, it is not a palindrom"
