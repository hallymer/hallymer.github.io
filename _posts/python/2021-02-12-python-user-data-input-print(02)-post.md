---
layout: post
title:  '[Python파이썬] 사용자 데이터입출력 (Input&print 02)'

categories:
    - programming

tags:
    - [python, 프로그래밍, 과제, format]

toc: true
toc_sticky: true

data: 2021-02-12
last_modified_at: 2021-02-12
---

* toc
{:toc}

---

## 문제
	Q1. 문제 조건
	1) 패딩 : 230000원, 스웨터 140000원
	2) 총 가격 30% 할인
	3) 원하는 패딩과 스웨터의 개수를 입력
	4) 총 가격을 계산하여 출력
	
	Q2. 문제 조건
	* 판매자 관점으로 1번 코드를 변경
	1) 패딩과 스웨터의 가격 및 할인율을 입력
	2) 손님이 사고 싶은 개수입력
	3) 총가격을 소수점 2자리까지 출력

### 부연설명
이 문제는 특별히 부연설명을 할 필요가 없어 안하겠습니다.

---

## 풀이

### Q1. 풀이

~~~python
# Q1. Answer
goods1 = int(input("몇개의 패딩를 살까? : "))
goods2 = int(input("몇개의 스웨터를 살까? : "))
padding = 230000
sweater = 140000

print("{0}개의 패딩과 {1}개의 스웨터를 살래".format(goods1,goods2))
print("총 가격은 : ",((padding*goods1)+(sweater*goods2)*0.7))
~~~

### Q2. 풀이

~~~python
# Q2. Answer
padding = int(input("일단 패딩을 얼마로 할까? : "))
sweater = int(input("일단 스웨터를 얼마로 할까? : "))
discount = int(input("가장 중요한 할인율은 몇%로 할까? : "))
discountrate = 1 - (discount/100)

goods1 = int(input("패딩 몇개를 구매 하시려고 하나요? : "))
goods2 = int(input("스웨터 몇개를 구매 하시려고 하나요? : "))
calculate = ((padding*goods1)+(sweater*goods2))*discountrate

print("{0}개의 패딩과 {1}개의 스웨터를 구매할게요".format(goods1,goods2))
print("총 가격은 : ",format(calculate,".2f"),"입니다.")
~~~

<center>

<b>문제와 답은 여유로울 때 계속 업로드합니다😊<br>
많이 방문해 주시고 도움이 되었으면 합니다!!</b>

</center>
