---
layout: post
title:  '[Sourcetree(소스트리)] 2. Github 로그인 및 연결'

categories:
    - git

tags:
    - [sourcetree,소스트리,협업,버전관리,git,github,로그인,연결]

toc: true
toc_sticky: true

data: 2021-02-25
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
<br>

![이미지1](/assets/img/Blog/git/sourcetree/02. github login-connect/1.png)


<center>
앞에서 <a href="https://hallymer.github.io/git/2021/02/21/(01)-sourcetree-install-post.html">포스팅</a>한 Sourcetree 설치 이후<br>이번에는 Sourcetree에서 <b>Github 로그인 및 연결</b>에 대해 포스팅하겠습니다.<br><br>
</center>

---

## 본론

<center>
<h2><b>[첫 번째 방법]</b></h2>
</center>
<br>

![이미지2](/assets/img/Blog/git/sourcetree/02. github login-connect/2.png)

![이미지3](/assets/img/Blog/git/sourcetree/02. github login-connect/3.png)

<br>
<center>
맨 위에 상단 바를 보면 <b>"도구 - 옵션"</b>이 있습니다.<br>
클릭하면 밑에 이미지처럼 나옵니다.
</center>
<br>

![이미지4](/assets/img/Blog/git/sourcetree/02. github login-connect/4.png)


​<center>
옵션 창에서 <b>인증</b>을 클릭해줍니다.
</center>
<br>

![이미지5](/assets/img/Blog/git/sourcetree/02. github login-connect/5.png)


​<center>
인증을 클릭하면 아래와 같은 이미지로 뜹니다.<br>
(계정은 뜰 수도 있고 안뜰 수도 있습니다)
</center>
<br>

![이미지6](/assets/img/Blog/git/sourcetree/02. github login-connect/6.png)


​<center>
여기서 우측에 파란색 글씨로 <b>"추가"</b>라는 부분이 있습니다<br>
"추가" 부분을 클릭해줍니다.
</center>
<br>

![이미지7](/assets/img/Blog/git/sourcetree/02. github login-connect/7.png)


​<center>
위 이미지처럼 이렇게 뜰 겁니다.<br><br>
Bitbucket 호스팅 서비스 대신 <b>Github 호스팅 서비스</b>를 이용하기 위해 <b>변경</b>해줍니다.<br>
그러고 난 뒤 인증을 OAuth에서 <b>Basic으로 변경</b>합니다.<br>
<b>Basic으로 변경 후, 사용자명</b>에 <b>자신의 Github 영문 이름</b>을 <b>입력</b>합니다.
</center>
<br>

![이미지8](/assets/img/Blog/git/sourcetree/02. github login-connect/8.png)


​<center>
<b>호스팅 서비스 :</b> Github<br><b>인증 :</b> Basic<br><b>사용자명 :</b> Github 닉네임<br><br>
그다음 비밀번호 새로 고침 클릭을 합니다.<br>
그럼 아래 이미지처럼 Github에 로그인하라고 뜹니다.
</center>
<br>

![이미지9](/assets/img/Blog/git/sourcetree/02. github login-connect/9.png)


​<center>
로그인하게 되면 밑에 이미지처럼 <b>초록색 체크 표시와 함께 인증 성공</b>이 뜹니다.<br>
그리고서 확인을 눌러주면
</center>
<br>

![이미지10](/assets/img/Blog/git/sourcetree/02. github login-connect/10.png)

![이미지11](/assets/img/Blog/git/sourcetree/02. github login-connect/11.png)

​<center>
위 이미지처럼 계정이 추가된 것이 보입니다!
</center>

---

<center>
<h2><b>[두 번째 방법]</b></h2>
Remote를 누르면 <b>"원격 저장소"</b>가 보입니다.
</center>
<br>

![이미지12](/assets/img/Blog/git/sourcetree/02. github login-connect/12.png)


​<center>
원격 저장소 밑에 Bitbucket 계정이 있습니다.<br>우측클릭을 하면 <b>"계정편집"</b>이 나오는데 클릭하면<br>
방법 1에서 나온 것처럼
</center>
<br>

![이미지13](/assets/img/Blog/git/sourcetree/02. github login-connect/13.png)


​<center>
이런 식으로 나옵니다.<br>
그런 다음 방법 1과 같이 <b>호스팅 서비스 : Github</b>으로 변경해 준 다음<br>
인증을 Basic 대신 <b>OAuth 그대로</b> 합니다.
</center>
<br>

![이미지14](/assets/img/Blog/git/sourcetree/02. github login-connect/14.png)


​<center>
그다음에 OAuth 토큰 새로 고침을 눌러주시면 됩니다!<br>
누르면 아래 이미지처럼 웹사이트가 뜹니다.
</center>
<br>

![이미지15](/assets/img/Blog/git/sourcetree/02. github login-connect/15.png)


​<center>
아래로 내려보면
</center>​
<br>

![이미지16](/assets/img/Blog/git/sourcetree/02. github login-connect/16.png)


​<center>
Authorize atlassian<br>
[아틀라시안에 권한을 부여하다]<br>
눌러주면 Github에 로그인하라고 합니다.<br>
로그인한 뒤 Sourcetree를 보면
</center>
<br>

![이미지17](/assets/img/Blog/git/sourcetree/02. github login-connect/17.png)

![이미지18](/assets/img/Blog/git/sourcetree/02. github login-connect/18.png)

​<center>
초록색 체크 표시와 함께 인증 성공이 뜹니다.<br>
확인을 누르면
</center>
<br>

![이미지19](/assets/img/Blog/git/sourcetree/02. github login-connect/19.png)


​<center>
위 이미지처럼 Bitbucket 계정이 Github 계정으로 변경된 것이 보입니다~!<br>
우측에 새로 고침을 누르면 Github에 올라가 있는 원격저장소 목록을 보여줍니다.<br><br>
그리고<br>
OAuth 무엇인지 검색을 해봤습니다.<br><br>
<a href="https://interconnection.tistory.com/76">https://interconnection.tistory.com/76</a><br><br>
한번 궁금하신 분은 위 링크를 참고하세요.<br><br>
이제 Sourcetree에 Github 로그인 및 연결을 완료하였습니다😀
</center>

---

<center>
<b>다음번에는 Github에서 Sourcetree로 Clone하기에 대해 포스팅하겠습니다.</b><br><br>
<b>또한, 여유로울 때 게시글을 계속 업로드합니다😊<br>
많이 방문해주시고 도움이 되었으면 합니다!!</b><br><br>
감사합니다~~<br><br>
<b>틀린 부분 및 오타/수정할 부분 궁금한 점이 있으면<br>
아래 댓글에 작성 부탁드립니다!</b><br>
</center>