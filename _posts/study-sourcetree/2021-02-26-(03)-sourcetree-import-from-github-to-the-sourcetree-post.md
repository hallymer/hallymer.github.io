---
layout: post
title:  '[Sourcetree(소스트리)] 3. Github에서 Sourcetree로 Clone하기'

categories:
    - git

tags:
    - [sourcetree,소스트리,협업,버전관리,git,github,clone]

toc: true
toc_sticky: true

data: 2021-02-26
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

![이미지19](/assets/img/Blog/git/sourcetree/02. github login-connect/19.png)


<center>
<a href="https://hallymer.github.io/git/2021/02/25/(02)-sourcetree-github-login-connect-post.html">Github 로그인 및 연결</a>까지 완료가 되었습니다.<br>이번에는 <b>Github Repository(저장소)에서 Sourcetree로 Clone(클론)하기</b>에 대해<br>포스팅하겠습니다.<br><br>
</center>

---

## 본론

<center>
<h2><b>[Github Repository에서 Sourcetree로 Clone하기]</b></h2>
</center>
<br>

![이미지1](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/1.png)


<center>
현재 이 모습으로 되어있습니다.<br>
여기서 Github Repository에서 Sourcetree에 불러오겠습니다.<br><br>
우선 아래 주소로 Github에 들어갑니다.<br>
<a href="https://github.com/">https://github.com/</a><br>
들어가서 로그인을 한 다음
</center>
<br>

![이미지2](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/2.png)


​<center>
우측 상단에 빨간색 네모표시를 눌러보면<br>
"Your profile", "Your repositories" 등이 있습니다.<br>
그중에서 <b>"Your repositories"</b>를 클릭합니다.
</center>
<br>

![이미지3](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/3.png)


​<center>
우측 상단에 초록색 NEW 버튼이 있습니다.<br>
그 버튼을 눌러주면
</center>
<br>

![이미지4](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/4.png)


​<center>
Create a new repository(새로운 저장소 만들기)가 뜹니다.<br>
여기서 저장소를 만들면 되는데<br>
<b>간단하게 설명을 하면</b>
</center>

***

​<center>
Repository name : <b>저장소 이름</b><br>
Description : <b>설명</b><br><br>
[권한설정]<br>
Public : <b>공개</b><br>
Private : <b>비공개</b><br><br>
Initialize this repository with a README : <b>(선택)</b><br>
<b>README 파일</b>은 보통 프로젝트에 관해 <b>설명하는 텍스트 파일</b>
<br>
</center>
<br>

***

​<center>
이렇게 설명할 수 있습니다.<br><br>
더 궁금한 점이 있으면<br>
<b><span style="color:red;">구글링</span></b>을 통해 알아보는 것을 추천합니다!
</center>
<br>

![이미지5](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/5.png)


​<center>
요번에 저장소를 만들 때는<br><br>
Repository name : <b>Sourcetree_study</b><br>
Description : <b>Sourcetree 공부용</b><br><br>
[권한설정]<br>
Public : <b>공개</b><br><br>
Initialize this repository with a README : <b>체크</b><br><br>
그러고 나면 아래 이미지처럼 뜹니다.
</center>
<br>

![이미지6](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/6.png)


​<center>
우측 상단에 초록색 Code 버튼이 있습니다.<br>
누르면 <b>"Clone with HTTPS"</b>가 뜨면서 <b>https://~~</b>이런 식으로 주소가 있습니다.<br>
주소 옆에 복사하기 버튼이 있습니다.<br>
그 부분을 클릭하여 주소를 복사합니다.<br>
</center>
<br>

![이미지7](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/7.png)


​<center>
자 이제 Sourcetree로 넘어옵니다.
</center>
<br>

![이미지8](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/8.png)


​<center>
위 이미지처럼 상단 부분에 Clone이 있습니다.<br>
그 부분을 클릭하면 아래 이미지처럼 변합니다.
</center>
<br>

![이미지9](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/9.png)


​<center>
여기서 아까 Github에서 복사한 주소를 소스 경로에 붙여넣기를 합니다.
</center>
<br>

![이미지10](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/10.png)


​<center>
그럼 자동으로 <b>"저장소 종류 : Git 저장소"</b>입니다.라고 뜨고<br>
목적지 경로, 이름이 자동으로 채워집니다.
</center>

***

​<center>
목적지 경로 : <b>로컬 PC 어디에 파일을 저장할 위치를 물어보는 것</b><br>
이름 : <b>파일을 관리할 이름</b>
</center>
<br>

***

​<center>
목적지 경로는 자신이 원하는 대로 변경하면 됩니다.<br>
이름은 목적지 경로를 변경하면 변경됩니다.<br>
이름을 변경하는 것을 추천합니다.<br><br>
저 같은 경우는 목적지 경로를 바탕화면으로 설정하였습니다.<br>
이름은 Sourcetree_study로 변경했습니다.<br><br>
<span style="color:red;"><b>*주의*</b></span><br>
<b>바탕화면에 바로 하려고 하니 안되어서 폴더를 하나 만들어 지정하니 됩니다.</b><br><br>
그리고 난 뒤 파란색 Clone(클론) 버튼을 클릭해주면
</center>
<br>

![이미지11](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/11.png)


​<center>
Github에서 Sourcetree로 Clone이 된 모습입니다.<br>
더 정확한 모습을 보기 위해서는<br>
파일 상태 밑에 있는 History를 클릭합니다.
</center>
<br>

![이미지12](/assets/img/Blog/git/sourcetree/03. import from github to the sourcetree/12.png)


​<center>
이제 Github에서 Sourcetree로 Clone하기를 완료하였습니다😀
</center>

---

<center>
<b>다음번에는 로컬저장소를 Sourcetree로 Add하기에 대해 포스팅하겠습니다.</b><br><br>
<b>또한, 여유로울 때 게시글을 계속 업로드합니다😊<br>
많이 방문해주시고 도움이 되었으면 합니다!!</b><br><br>
감사합니다~~<br><br>
<b>틀린 부분 및 오타/수정할 부분 궁금한 점이 있으면<br>
아래 댓글에 작성 부탁드립니다!</b><br>
</center>