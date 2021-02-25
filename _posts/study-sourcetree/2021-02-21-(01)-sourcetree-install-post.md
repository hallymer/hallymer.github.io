---
layout: post
title:  '[Sourcetree(소스트리)] 1. 설치하기'

categories:
    - git

tags:
    - [sourcetree,sourcetreet설치,소스트리,소스트리설치,협업,버전관리,git,github,설치]

toc: true
toc_sticky: true

data: 2021-02-21
last_modified_at: 2021-02-26
---

![소스트리 이미지](/assets/img/Blog/git/sourcetree/sourcetree.png)

* toc
{:toc}

---

## 도입

<center>
<b>[ 본 포스팅은 <span style="color:red;">PC화면에 최적화</span> 되어있습니다. ]</b>
</center>


![이미지1](/assets/img/Blog/git/sourcetree/01.install-sourcetree/1.jpg)


<center>
Git, GitHub, Sourcetree, Opensource 등 요즘 이야기가 많이 나온다.<br>
위키 백과를 참고하여 설명하면<br><br>
</center>

**Git(깃)**<br>
**-->** 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템

**GitHub(깃허브)**<br>
**-->** 분산 버전 관리 툴인 깃(Git)을 사용하는 프로젝트를 지원하는 웹호스팅 서비스

**Sourcetree(소스트리)**<br>
**-->** Git 사용을 도와주는 **GUI**(**G**raphical **U**ser **I**nterface)프로그램

**Opensource(오픈소스)**<br>
**-->** 원래는 Open Source Software(OSS)라고 부르지만 간략하게 OpenSource라고 말한다.<br>
소스 코드를 공개해 누구나 특별한 제한 없이 그 코드를 보고 사용할 수 있는 오픈 소스 라이선스를 만족하는 소프트웨어

​
<center>
요약하면 <b>"효율적인 프로젝트 관리 및 협업"</b>에 사용하는 <b>분산 버전 관리 시스템</b><br>
거기에 <b>SourceTree(소스트리)를 사용</b>하여 직접 git 명령어 입력 대신<br>
<b>클릭으로 git을 더 쉽게 사용할 수 있도록 도와준다.</b><br><br>
<b>[더 자세한 내용은 <span style="color:red;">구글링</span>을 통해 알아보는 것을 추천합니다]</b>
</center>

---

## 본론
<center>
자 이제 소스트리 설치하는 방법에 대해 알아보겠습니다.<br>
( Github에 가입했다는 가정하에 진행합니다.)<br>
(Github에 가입을 안 하신 분은 가입 후 진행하시길 바랍니다.)<br><br>
<b>Sourcetree(소스트리) 홈페이지에 접속합니다.<br>
아래링크로 접속하시면 됩니다.<br></b>
<a href="https://www.sourcetreeapp.com/"> https://www.sourcetreeapp.com/ </a>
</center>
<br>

![이미지2](/assets/img/Blog/git/sourcetree/01.install-sourcetree/2.png)

<br>
<center>
위 링크를 통해 홈페이지에 접속하면 바로 다운로드 받을수 있는 버튼이 보입니다.<br>
다운로드 버튼을 눌러 설치파일을 실행시킵니다.
</center>
<br>

![이미지3](/assets/img/Blog/git/sourcetree/01.install-sourcetree/3.png)

<br>
<center>
실행을 시키면 위 이미지처럼 Sourcetree 계정 등록하는 화면이 나옵니다.<br>
<b>(참고)</b><i>Sourcetree에 회원가입을 하고 로그인을 해야 설치 진행을 할 수 있습니다!</i><br>
Bitbucket Server 옆에 있는 Bitbucket을 눌러주면 아래처럼 뜹니다.<br>
</center>
<br>

![이미지4](/assets/img/Blog/git/sourcetree/01.install-sourcetree/4.png)

<br>
<center>
저 같은 경우는 구글계정으로 진행하였습니다.<br>
회원가입을 다 진행하고 로그인을 하면<br>
</center>
<br>

![이미지5](/assets/img/Blog/git/sourcetree/01.install-sourcetree/5.png)

<br>
<center>
위 이미지처럼 다음을 진행 할 수 있도록 나옵니다.<br>
</center>
<br>

![이미지6](/assets/img/Blog/git/sourcetree/01.install-sourcetree/6.png)

<br>
<center>
설치화면이 나옵니다<br>
여기서 Git, Mercurial 이렇게 나오는데 Git에 체크하고 다음을 눌러줍니다.<br>
Mercurial이란 Git과 비슷한 버전관리 툴입니다.<br>
Mercurial을 설치할지 말지를 선택합니다.<br>
저 같은 경우는 같이 설치를 했지만, 설치를 안 하셔도 상관없습니다~<br>
</center>
<br>

![이미지7](/assets/img/Blog/git/sourcetree/01.install-sourcetree/7.png)

<br>
<center>
소스트리에서 Git을 사용할 때 기본 계정으로 사용할 Git 계정을 설정하는 화면입니다.<br>
Github에 가입했던 계정 정보를 입력하면 됩니다.<br><br>
첫 번째 빈칸은 Git에서 사용하는 Username, <br>
두 번째 빈칸은 Github에 가입할 때 적었던 이메일을 입력한 뒤<br>
다음을 눌러주시면 됩니다.<br>
</center>
<br>

![이미지8](/assets/img/Blog/git/sourcetree/01.install-sourcetree/8.png)

<br>
<center>
SSH키를 불러올지를 선택합니다.<br>
저 같은 경우는 "아니요"로 선택하였습니다.<br>
</center>
<br>

![이미지9](/assets/img/Blog/git/sourcetree/01.install-sourcetree/9.png)

<br>
<center>
이제 설치가 완료되었습니다 :0<br><br>
</center>

---

<center>
<b>다음번에는 Sourcetree에서 Github 로그인 및 연결에 대해 포스팅하겠습니다.</b><br><br>
<b>또한, 여유로울 때 게시글을 계속 업로드합니다😊<br>
많이 방문해주시고 도움이 되었으면 합니다!!</b><br><br>
감사합니다~~<br><br>
<b>틀린 부분 및 오타/수정할 부분 궁금한 점이 있으면<br>
아래 댓글에 작성 부탁드립니다!</b><br>
</center>