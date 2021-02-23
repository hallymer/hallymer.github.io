---
layout: post
title: 듀얼부팅 환경에서 블루투스 키보드 사용하기

categories:
    - etc

tags:
    - [ubuntu, windows 10, logitech, k380, keychron, k2, 멀티부팅, 듀얼부팅]

toc: true
toc_sticky: true

data: 2021-02-23
last_modified_at: 2021-02-24
---

* toc
{:toc}

---

## 포스팅하게 된 이유

평소 집 또는 기숙사에서 무선(블루투스) 키보드를 애용한다. 처음에는 Windows만 사용하다가 어느 순간 Ubuntu를 사용하기 시작하여 현재 2개의 운영체제를 번갈아 사용하게 되었다. 그 당시에는 불편함을 느끼지 못하였다.<br>

<br>

하지만, 노트북을 모니터에 연결하고 여러 장치를 연결하다 보니 무선(블루투스) 키보드를 많이 사용하기 시작하게 되었고 두 운영체제에서 사용하려고 하다 보니 부팅할 때마다 블루투스 인식이 안 되어 직접 페어링을 시켜주는 귀찮은 상황이 계속 발생하였다.

결국, 너무 불편해서 직접 찾아서 해결하였다.<br>
어떻게 해결하였는지 해결한 부분에 대해 포스팅을 남겨두려고 한다. 그래야 나중에 나와 같은 상황이 발생한 사람이 들어와서 도움을 받고 해결했으면 좋겠다.

또한, 이 포스팅은 <b>NoUnique님이 작성한 내용을 바탕으로 작성한 글</b>이다.<br>
[https://nounique.github.io/development/multiboot-sharing-bluetooth/](https://nounique.github.io/development/multiboot-sharing-bluetooth/)<br>
Disqus로 댓글 남기기를 하려고 했지만, 무슨 이유인지 댓글이 달리지 않아 직접 인스타 DM으로 **"멀티부팅 환경에서 블루투스장치 공유하기"** 게시글을 참고하여 게시글을 작성해도 되는지를 연락드렸고 **출처만 남겨주면 된다**고 흔쾌히 **수락하셨다.**

---

## 순서

**1.** Ubuntu에 키보드를 블루투스 장치에 페어링<br>
**2.** 윈도우에서 동일 키보드를 블루투스 장치에 다시 페어링<br>
**3.** 윈도우에서 [psexec](http://live.sysinternals.com/psexec.exe)를 이용하여 블루투스 페어링 정보 획득<br>
**4.** 윈도우의 페어링 정보를 우분투의 블루투스 장치 정보에 입력 (<b>⚠이 부분이 중요⚠</b>)<br>
**5.** 우분투 터미널에서 블루투스 서비스 재시작 (sudo service bluetooth restart)

---

## 적용방법
### 원리

우분투에 페어링 된 상태에서 다시 윈도우로 페어링을 하게 되면, 블루투스 장치는 이전 연결정보(우분투와의 페어링 정보)를 잃고 새로운 정보(윈도우와의 페어링 정보)를 저장하게 되는데 윈도우에 저장된 페어링 키들을 [psexec.exe](http://live.sysinternals.com/psexec.exe)로 접근하여 키들을 Ubuntu로 옮겨주면 멀티 부팅 환경에서 다른 OS를 쓰더라도 블루투스 장치를 공유해서 사용할 수 있게 된다.

자세한 내용은 아래 2개 링크를 참고하면 된다.<br>
1. [https://nounique.github.io/development/multiboot-sharing-bluetooth/](https://nounique.github.io/development/multiboot-sharing-bluetooth/)<br>
2. [https://console.systems/2014/09/how-to-pair-low-energy-le-bluetooth.html](https://console.systems/2014/09/how-to-pair-low-energy-le-bluetooth.html)<br>

몇 번 읽어보면 이해가 될 것이다. \\(●'◡'●)/

<br>

이 포스팅은 간단하게 <b>누구든 최대한 쉽게 보고 적용할 수 있도록</b> 포스팅하려고 한다.

<br>

무선(블루투스) 키보드는 총 두 가지이다.

1. Logitech K380
2. Keychron K2

이 2개의 무선(블루투스) 키보드는 BLE 제품이 아닌 **BR/EDR 제품**이다.

> * BLE : Bluetooth Low Energy
> * BR : Bluetooth Basic Rate
> * EDR : Enhanced Data Rate

---

우선 우분투에다가 블루투스 키보드를 페어링한다.<br>
페어링이 완료되면 윈도우로 부팅하여 다시 페어링한다.<br><br>
**먼저 우분투에 페어링하는 이유**<br>
--> 키보드 연결정보 생성한 뒤 추후 내용 수정만으로 장치와 연결할 수 있도록 하기 위함

---

먼저 [psexec.exe](http://live.sysinternals.com/psexec.exe)를 다운받고,<br>
psexec.exe를 이용하여 감춰져있는 레지스트리에서 블루투스 키들을 추출한다.<br>

<br>

여기서, cmd(명령어 프롬프트) OR powershell(파워쉘)은 **관리자 권한**으로 실행해야 한다.

<br>

~~~cmd
> psexec.exe -s -i regedit /e C:\BTKeys.reg HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\BTHPORT\Parameters\Keys
~~~

---

만약 바탕화면에 psexec.exe파일이 있다면,<br>
명령어로 psexec.exe가 있는 바탕화면(Desktop) 위치까지 가줘야 한다.<br><br>
관리자 권한으로 실행시키면 **C:\WINDOWS\system32>**로 나온다.<br>
**cd /**를 작성하고 엔터를 누르면 **C:\\>**나온다.<br>
그 상태에서 **cd Users --> cd 사용자 계정명 --> cd Desktop** 이 순으로 작성하면<br>
최종적으로 아래처럼 나온다.<br>
**C:\Users\사용자 계정명\Desktop>**<br><br>
이 상태에서 입력해야 한다. 안 그러면 Error가 발생한다.

---

또한, 레지스트리 내용을 스크린샷으로 찍어 놓으면 더 편리하게 작업을 할 수 있다. 페어링 키를 파일로 추출할 때처럼 관리자 권한으로 psexec를 통해 레지스트리 편집기를 실행시킨다.


~~~cmd
> psexec.exe -s -i regedit
~~~

**HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\BTHPORT\Parameters\Keys**<br>
위 경로로 들어가면 블루투스 수신기 아래에서 필요한 정보가 나온다. 그걸 캡처한다.<br>
캡처한 걸 카톡에 보낸다.


![이미지1](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/1.png)


아래 이미지를 보면 노란 형광으로 표시한 부분 **블루투스 수신기의 MAC 주소**이고,<br>
그 아래에 초록 형광으로 표시한 부분은 블루투스 장치 즉, **키보드의 MAC 주소**다.


![이미지2](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/2.png)


내 블루투스 수신기와 키보드의 MAC 주소를 요약하면,<br>

**블루투스 수신기의 MAC 주소** : 283a4d158334<br>
**키보드의 MAC 주소** : 34885df70026 ~ dc2c26ee9409

---

NoUnique님이 작성한 글에서는 **Keys / 블루투스 수신기 MAC / 키보드 MAC** 이런 식으로 폴더로 나오는 것에 반해, 나 같은 경우는 **블루투스 수신기 MAC**에 대한 폴더가 있고 **키보드 MAC**이 이름으로 쫙 나와 있었다.<br><br>
이 부분 때문에 고생하였다.

---

아까 C드라이브에 저장된 BTKeys.reg의 출력 내용은 아래와 같다.<br>

~~~txt
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\BTHPORT\Parameters\Keys]

[HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Services\BTHPORT\Parameters\Keys\283a4d158334]
"b8d50bc63b3c"=hex:3e,17,eb,2e,83,58,d1,5d,c8,cf,aa,b2,30,23,57,b0
"MasterIRK"=hex:5d,c8,3d,69,8a,86,25,65,8c,fc,aa,9e,db,a7,e4,4a
"a8be271e7ef6"=hex:5f,1e,d2,a8,d4,67,c9,ad,a5,e9,30,df,2f,c6,1f,00
"a82bb9d88ad1"=hex:71,6b,d0,2c,0a,9b,e7,f0,03,18,41,08,98,e3,e0,fb
"34885df70026"=hex:f4,3b,ca,a9,10,d0,25,06,0d,1f,30,b2,9b,87,9c,32
"dc2c26ee9409"=hex:ee,56,10,23,1c,b7,8a,ec,41,7d,5a,de,1b,e2,1b,55
~~~
이때 필요한 정보는 **블루투스 수신기의 MAC주소**, **키보드의 MAC주소**, **이름**, **데이터**<br>
이렇게 **4가지**가 필요하다.<br>

**캡처한 이미지와 BTKeys.reg** 이 두 개를 다 준비가 되었다면,<br>
우분투로 넘어가서 블루투스 정보(BTKeys.reg)를 **/var/lib/bluetooth/{블루투스 수신기 MAC}**에 복붙해주고 난 뒤, 
각각의 키보드의 MAC 주소의 폴더가 있을 것이다. 폴더에 들어가서 info 파일을 클릭하면 정보가 뜨게 되고,<br>
[General] 부분에 키보드 이름이 적혀있다. 그걸 참고하고 클릭한 폴더에 키보드 MAC 주소로 폴더명이 적혀있으니 그걸 참고하여<br>
캡처한 이미지 혹은 BTKeys.reg를 열어서 키보드의 MAC을 찾은 후 HEX 부분을 콤마(,) 구분자 없이 싹 대문자로 입력한다.<br>

---

글로만 작성하면 이해를 못 할 가능성이 크다. 아래 이미지를 추가하면서 설명을 하겠다.

---

* 이미지가 안 보이면 우측 클릭 **"새 탭에서 이미지 열기"**를 하면 잘 보인다.

![이미지3](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/3.png)


위 이미지는 **/var/lib/bluetooth**까지 들어온 모습이다.<br>폴더명을 보면 28:3A:4D:15:83:34로 나와 있다.<br><br>
즉, **블루투스 수신기의 MAC 주소**가 폴더명이라는 것을 알 수 있다. 블루투스 수신기의 MAC 주소로 나와 있는 폴더를 클릭해서 들어가면 아래 이미지처럼 나온다.


![이미지4](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/4.png)


아래 빨간 사각형으로 표시해둔 2개가 있다. 표시한 것이 **키보드의 MAC 주소**로 폴더명이 만들어진걸 알 수 있다.
어떤 키보드의 MAC 주소인지 알기 위해 각각의 폴더에 들어가서 **info 파일**을 확인하면 된다.


![이미지4-1](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/4-1.png)

![이미지5](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/5.png)


psexec.exe를 이용하여 감춰져 있는 블루투스 키들을 추출한 것을<br>블루투스 수신기의 MAC 주소 폴더명에 복붙한 모습이다.


![이미지6](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/6.png)


키보드의 MAC 주소로 저장되어있는 폴더명에 들어가니 info 파일이 있다.<br>
info 파일을 클릭하면 아래 이미지처럼 나온다.


![이미지7](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/7.png)

![이미지7-1](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/7-1.png)


위 이미지를 보면 [LinkKey] 부분에 빨간 직사각형으로 표시해놨다.<br>
여기서 **Key 부분**을 **BTKeys.reg 혹은 캡처한 내용을 바탕으로 변경**하면 된다.<br>
**Key 부분을 변경**할 때 HEX 부분을 콤마(,) **구분자 없이 싹 대문자로 입력**해야 한다.<br>
현재 위 이미지는 이미 변경한 내용이라 모르겠으면 아래 이미지와 대조하면 금방 이해할 거로 생각한다.
**아래 이미지는 BTKeys.reg 내용**이다.


![이미지8](/assets/img/Blog/etc/Multiboot-bluetooth-keyboard-connecting/8.png)

---

설정이 다 완료되었다면,

~~~Terminal
sudo service bluetooth restart
~~~

위 명령어를 꼭 입력하고 Enter를 해주어야 한다.<br>블루투스 서비스를 재시작을 안 해주면 새 설정이 적용이 안 된다.<br>
이제 듀얼환경 혹은 멀티환경에서 윈도우와 우분투 환경을 바꿔가며 키보드를 사용해도<br>지속해서 페어링이 되어있을 것이다.<br>

나 같은 경우는 간단하게 한 편이고 추가로 궁금한 내용이 있으면,<br>
[NoUnique님이 작성한 글](https://nounique.github.io/development/multiboot-sharing-bluetooth/)을 보면 될 것 같다.<br>
