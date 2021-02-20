---
layout: post
title:  '[Python파이썬] for문을 사용하여 별찍기+숫자찍기 (for문 01)'

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

    Q1. 바깥쪽 한 개의 for문과 안쪽 두개의 for문을 중첩하여 반복하면서 별모양 출력
    (바깥쪽 for 문은 range(1, 6)으로, 안쪽 for문은 range(1, i+1)로 반복)

    <출력예시>
    *
    * *
    * * *
    * * * *
    * * * * *




    Q2. 두개의 for문을 중첩하여 반복하면서 별모양 출력
    (바깥쪽 for문은 range(1,6)으로, 안쪽 for문은 range(i, 6)로 반복)

    <출력예시>
    * * * * *  
    * * * *  
    * * *  
    * *  
    * 




    Q3. 두개의 for문을 중첩하여 반복하면서 별모양 출력
    (바깥쪽 for문은 range(1,6)으로, 안쪽의 두 for문은 각각 range(1,6-i)와 range(1,i+1)로 반복)

    <출력예시>
            *
          * *
        * * *
      * * * *
    * * * * *




### 부연설명

문제마다 힌트가 있지만, 조금 더 설명하겠습니다.<br>

**1번 문제**는 삼중 for 문으로 작성해야 합니다.<br>

처음 문제를 읽다 보면 이해를 못 하실 수 있습니다.<br>

쉽게 설명해 드리면,<br>

~~~python
for i in range()
    for j in range()
    for k in range()
~~~

위 코드처럼 작성해야 한다는 의미입니다.<br>

**2번 문제, 3번 문제**는 이중 for 문으로 작성해야 합니다.<br>


---

## 풀이

### Q1. 풀이

~~~python
# Q1. Answer
for i in range(1, 6):
    for j in range(1, i+1):
        print('*', end=" ")
    for k in range(1, i+1):
        print(end='')
    print()
~~~

### Q2. 풀이

~~~python
# Q2. Answer
for i in range(1,6):
      for j in range(i,6):
          print("*",end=" ")
      print(" ")
~~~

### Q3. 풀이

~~~python
# Q3. Answer
for i in range(1,6):
    for j in range(1,6-i):
        print(" ",end=" ")
    for j in range(1,i+1):
        print('*', end=" ")
    print()
~~~

<center>

<b>문제와 답은 여유로울 때 계속 업로드합니다😊<br>
많이 방문해 주시고 도움이 되었으면 합니다!!</b>

</center>
