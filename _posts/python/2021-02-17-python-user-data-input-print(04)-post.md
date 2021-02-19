---
layout: post
title:  '[Python파이썬] 사용자 데이터입출력 (Input&print 04)'

categories:
    - programming

tags:
    - [python, 프로그래밍, 과제, 이스케이프코드, 고양이출력, len함수, 자리수의 합, 자릿수의 합]

toc: true
toc_sticky: true

data: 2021-02-17
last_modified_at: 2021-02-17
---

* toc
{:toc}

---

## 문제

    Q1. 아래 출력예시처럼 출력

    <출력예시>
    고양이가 하고 싶은 말은? 난 널 사랑해
             _______
            <난 널 사랑해>
             -------
            /
      /\_/\ /
     ( o.o )
     >  ^  < 



    Q2. 정수를 입력 받아서 정수의 자리수의 합을 계산
    ex) 235를 입력 받았다면 2+3+5를 계산
    나머지 연산자 %와 정수 나눗셈 // 연산자를 이용


### 부연설명

**2번 문제**는 **정수의 자릿수의 합**을 구해야 합니다.<br>

구하는 방법은 **나머지 연산자 % 와 정수 나눗셈 // 연산자**로 계산한 다음,<br>

최종적으로 다 더하면 됩니다.<br>

위 예시처럼 235라는 숫자를 입력받으면 **235 // 1000**을 한 뒤<br>

그 값을 n이라는 변수에 저장한 뒤 **n % 1000**으로 나머지를 구합니다.<br>

이런 식으로 1의 자리까지 구한 다음 더하면 됩니다!

---

## 풀이

### Q1. 풀이

~~~python
# Q1. Answer
push = input("고양이가 하고 싶은 말은? ")
print("\t ",'_'*len(push))
print("\t","<"+push+">")
print("\t ",'-'*len(push))
print("\t/")
print(" /\_/\ /")
print("( o.o )")
print(">  ^  <")
~~~

### Q2. 풀이 (2가지)

~~~python
# Q2-1. Answer
num = int(input("정수를 입력하세요. : "))

num1000 = num//1000
num %= 1000
num100 = num//100
num %= 100
num10 = num//10
num %= 10
num1 = num//1

add = num1000+num100+num10+num1
print("자릿수의 합은 ",add,"이다.")
~~~

~~~python
# Q2-2. Answer
integer = int(input("정수를 입력하세요. : "))

a = integer//1000
integer = integer%1000
b = integer//100
integer = integer%100
c = integer//10
integer = integer%10
d = integer//1

hap = a+b+c+d
print("자릿수의 합은 ",hap,"이다.")
~~~

<center>

<b>문제와 답은 여유로울 때 계속 업로드합니다😊<br>
많이 방문해 주시고 도움이 되었으면 합니다!!</b>

</center>
