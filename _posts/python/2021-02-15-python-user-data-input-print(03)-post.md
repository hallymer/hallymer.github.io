---
layout: post
title:  '[Python파이썬] 사용자 데이터입출력 (Input&print 03)'

categories:
    - programming

tags:
    - [python, 프로그래밍, 과제, BMI, 총점구하기, 평균구하기]

toc: true
toc_sticky: true

data: 2021-02-15
last_modified_at: 2021-02-15
---

* toc
{:toc}

---

## 문제

    Q1. 키보드로 국어, 영어, 수학 점수를 입력 받아
    세 과목의 총점과 평균을 출력하는 프로그램 작성



    Q2. 키와 몸무게를 입력 받아 체질량지수 "Body Mass Index (BMI)"를
    계산하여 출력하는 프로그램 작성


### 부연설명
**2번 문제**는 **체질량지수(BMI)**를 구해야 합니다.<br>


구하는 방법은 **BMI = 몸무게(kg)/신장(키)(m)^2**로 계산합니다.<br>


또한, 신장(키)은 평소 cm로 측정하기 때문에 cm에서 m로 변환해야 합니다.<br>


cm에서 m로 단위 변환은 **cm*100**을 해주면 **m**로 변경됩니다.<br>

BMI 범위는 검색을 통해 알아보고 조건문(If 문)을 사용해야 합니다.

---

## 풀이

### Q1. 풀이

~~~python
# Q1. Answer
Korean = float(input("국어 점수를 입력하세요 : ")) # 국어 점수 입력 후 Korean 변수에 저장
English = float(input("영어 점수를 입력하세요 : ")) # 영어 점수 입력 후 English 변수에 저장
Math = float(input("수학 점수를 입력하세요 : ")) # 수학 점수 입력 후 Math 변수에 저장

total = Korean + English + Math # 세 과목 총점
average = total/3 # 세 과목 평균 구하는 것

print("세 과목의 총점은 [",total,"]이고, 평균은 [",average,"]입니다.")
~~~

### Q2. 풀이

~~~python
# Q2. Answer
height = float(input("키(cm) : ")) # int는 정수(1,10,50 등) float은 실수 (1.5, 7.5 등)
wegiht = float(input("몸무게(kg) : "))
heightchange = height/100 # cm -> m 단위변환
BMI = wegiht/(heightchange**2) #(height/100)**2도 가능합니다.

if BMI >= 35 :
    print("고도비만")
elif 35 > BMI and 30 <= BMI :
    print("중등도비만")
elif 30 > BMI and 25 <= BMI :
    print("경도비만")
elif 25 > BMI and 23 <= BMI :
    print("과체중")
elif 23 > BMI and 18.5 <= BMI :
    print("정상")
else:
    print("저체중")
~~~

<center>

<b>문제와 답은 여유로울 때 계속 업로드합니다😊<br>
많이 방문해 주시고 도움이 되었으면 합니다!!</b>

</center>
