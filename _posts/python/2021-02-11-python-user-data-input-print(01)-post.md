---
layout: post
title:  '[Python파이썬] 사용자 데이터입출력 (Input&print 01)'

categories:
    - programming

tags:
    - [python, 프로그래밍, 과제, 최대공약수, 유클리드]

toc: true
toc_sticky: true

data: 2021-02-11
last_modified_at: 2021-02-11
---

* toc
{:toc}

---

## 문제
    Q1. 두 수를 입력받아 최대 공약수를 구하는 프로그램을 작성
    프로그램 순서 : (2에서 5단계까지가 반복문)

    1. 두 수 가운데 큰 수를 x 작은 수를 y 로 한다
    2. y가 0일 때 까지 반복하며 결과 공약수는 x이다.
    3. r = x%y //x를 y로 나눈 나머지가 새로운 x가 된다.
    4. x = y; // 기본의 y값은 새로운 x가 된다.
    5. y = r;
    6. 2단계로 돌아간다.

### 부연설명
이 문제는 **유클리드 호제법을 사용하는 문제**입니다.
<br>

여기서 **유클리드 호제법**이란


**2개의 자연수 또는 정식의 최대공약수를 구하는 알고리즘의 하나**입니다.


자세한 내용은 [위키백과 예시](https://ko.wikipedia.org/wiki/%EC%9C%A0%ED%81%B4%EB%A6%AC%EB%93%9C_%ED%98%B8%EC%A0%9C%EB%B2%95)를 참고하면 이해에 도움이 되실 겁니다.

---

## 풀이
푸는 방법은 2가지가 있습니다.
### 첫번째 방법입니다.

~~~python
# first Answer
num1 = int(input("정수를 입력해주세요 : "))
num2 = int(input("정수를 입력해주세요 : "))

if num1 > num2:
    x = num1;    y = num2
else:
    x = num2;    y = num1
while True:
    r = x%y
    x = y
    y = r

    if r !=0:
        continue #유클리드 호제법 최대공약수를 구하는 두번째 정리를 이용

    else:
        break
print("최대 공약수(" ,num1, "," ,num2, ")는",x,"입니다.")
~~~


### 두번째 방법입니다.

~~~python
# second Answer
num1 = int(input("정수를 입력해주세요 : "))
num2 = int(input("정수를 입력해주세요 : "))

if num1 > num2:
    x = num1;    y = num2
else:
    x = num2;    y = num1
while(y>0):
    r =x%y
    x = y
    y = r
print("최대 공약수(" ,num1, "," ,num2, ")는",x,"입니다.")
~~~

<center>

<b>문제와 답은 여유로울 때 계속 업로드합니다😊<br>
많이 방문해 주시고 도움이 되었으면 합니다!!</b>

</center>
