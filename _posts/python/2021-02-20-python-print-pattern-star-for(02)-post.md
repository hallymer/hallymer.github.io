---
layout: post
title:  '[Python파이썬] for문을 사용하여 별찍기+숫자찍기 (for문 02)'

categories:
    - programming

tags:
    - [python, 프로그래밍, 과제,for문, 별, 별찍기, 숫자찍기, 숫자탑]

toc: true
toc_sticky: true

data: 2021-02-20
last_modified_at: 2021-02-20
---

* toc
{:toc}

---

## 문제

    Q1. 바깥쪽 한 개의 for 문과 안쪽 세 개의 for문을 중첩하여 반복하면서 별모양 출력
    (바깥쪽 for문은 range(1,6)으로,
     안쪽의 세 for 문은 각각 range(1, 6-i), range(1, i+1), range(1,i)로 반복)

    <출력예시>
        *
       ***
      *****
     *******
    *********

    Q2. for문 1개를 이용하여 숫자탑 출력

    <출력예시>
    1
    22
    333
    4444
    55555
    666666
    7777777
    88888888
    999999999





### 부연설명

문제마다 힌트가 있지만, 조금 더 설명하겠습니다.<br>

**1번 문제**는 사중 for 문으로 작성해야 합니다.<br>

처음 문제를 읽다 보면 이해를 못 하실 수 있습니다.<br>

쉽게 설명해 드리면,<br>

~~~python
for i in range()
    for j in range()
    for k in range()
    for m in range()
~~~

위 코드처럼 작성해야 한다는 의미입니다.<br>

**2번 문제**는 출력하기 위해서 str() 형변환을 해주어야 합니다.<br>

또한, 아래 사이트에 더 많은 별탑과 숫자탑 등 여러가지가 있습니다.<br>
[https://pynative.com/print-pattern-python-examples/](https://pynative.com/print-pattern-python-examples/)

---

## 풀이

### Q1. 풀이

~~~python
# Q1. Answer
for i in range(1,6):
    for j in range(1,6-i):
        print(" ",end="")
    for k in range(1,i+1):
        print("*", end="")
    for m in range(1, i):
        print("*", end="")
    print()
    
# 번외 (한 줄로 트리만들기)
# Q1. Extra_Answer(01)
for i in range(1,6):
    print(' '*(6-i) + '*'*(2*i-1))

# Q1. Extra_Answer(02)
for i in range(1,11,2):
    print('{:^9}'.format('*'*i))
~~~

### Q2. 풀이

~~~python
# Q2. Answer
for i in range(1,10):
  print(str(i)*i)
~~~

<center>

<b>문제와 답은 여유로울 때 계속 업로드합니다😊<br>
많이 방문해 주시고 도움이 되었으면 합니다!!</b>

</center>
