---
layout: post
title:  "Quick DBD 간단 사용 review"
date:   2023-11-09 09:54:53 +0900
---

<h3 id="quickdbd에-대해">QuickDBD에 대해</h3>
<p>QuickDBD는 간편한 ER 다이어그램 툴이다. 시중에 여러 가지의 데이터베이스 다이어그램 관련 툴이 존재하는데, 그 중에서도 QuickDBD를 사용하는 이유에 대하여 정리해 보겠다.</p>
<p>ER 다이어그램을 만들 때 작업에 집중하기 위해 키보드 사용을 선호하는 경우 QuickDB가 가장 적합한 프로그램이 될 수 있다. 그뿐만 아니라 온라인으로 다이어그램을 공유하여 공동으로 작업하고 양질의 데이터베이스 구조를 생성할 수 있다. 이 ER 다이어그램 툴에서는 MySQL, Oracle 및 SQL Server로부터 스키마를 불러올 수 있어 ERD를 보다 쉽고 빠르게 생성할 수 있다. 추가적으로 나는 QuickDBD가 특히 GUI가 좋고, 코드로 작성하여 설계가 가능하다는 점이 마음에 들었다.</p>
<p>주요 특징:</p>
<ul>
<li>공개적으로 프로젝트를 저장하고 공유할 수 있다.</li>
<li>스키마를 입력하여 ERD를 생성한다.</li>
<li>MySQL, SQL Server 및 Oracle 지원을 해 준다.</li>
</ul>
<h3 id="erd란">ERD란?</h3>
<p>QuickDBD가 유용한 ERD 툴이라는 것은 알게 되었는데, 그렇다면 ERD란 무엇인가?<br />
ERD는 Entity Relationship Diagram 의 약자이고, E-R 다이어그램이라고 부르기도 한다.<br />
'존재하고 있는 것(Entity)들의 관계(Relationship)을 나타낸 도표(Diagram)' 이라는 뜻이다.<br />
여기서 말하는 존재하고 있는 것이란 데이터를 뜻하니 데이터들의 관계를 나타낸 도표인 셈이다.<br />
<img src="https://velog.velcdn.com/images/kijrary/post/9ecdd9fd-b252-4015-b57c-9f75bf666329/image.png" /><br />
데이터 간의 관계들을 도표로 나타내는 규칙이다. 1:1, 1:N, N:M 등의 관계를 표현한 것이다. 또한 실선은 부모 테이블의 기본키를 자식 테이블이 가지고 있으며 이를 기본키로 사용하는 경우이고 점선은 부모 테이블의 기본키를 자식테이블이 가지고 있지만 이를 기본키로 사용하지 않을 때 사용한다.<br />
<img src="https://velog.velcdn.com/images/kijrary/post/f9f888d4-b4a6-47cd-bb86-9d9a48f68a52/image.png" /><br />
<img src="https://velog.velcdn.com/images/kijrary/post/36b2ac20-6dc4-4ddb-9d65-071fa5b8c53d/image.png" /><br />
점선/실선과 관계를 나타낸 것을 볼 수 있다.<br />
<img src="https://velog.velcdn.com/images/kijrary/post/f79e3fbc-a3ee-4265-a16b-aa6cdec7a0e8/image.png" /><br />
논리적 데이터 모델링을 통해, ERD를 설계한 모습이다.</p>
<h3 id="quickdbd-사용-방법">QuickDBD 사용 방법</h3>
<p>아래의 사이트에 접속하여 try the app 버튼을 통해 페이지로 들어간다.<br />
<a href="https://www.quickdatabasediagrams.com/">QuickDBD 사이트 바로가기</a><br />
<img src="https://velog.velcdn.com/images/kijrary/post/4cb3c567-c70a-465c-bb78-ecee1bc13354/image.png" /><br />
초기 기본 페이지가 생성된 것을 볼 수 있다. 화면의 왼쪽에는 스키마를 정의할 수 있는 곳이 있고, 오른쪽에는 왼쪽에서 정의한 스키마들을 테이블로 한눈에 볼 수 있는 테이블 다이어그램 화면이 있다. 위쪽 메뉴에서는 여기서 만든 스키마를 추출할 수 있는 기능, 불러올 수 있는 기능 등이 있고, 회원 로그인과 공유 기능도 있다.</p>
<p><img src="https://velog.velcdn.com/images/kijrary/post/b0b645a2-b454-4a78-ba08-a19f932b1bd9/image.png" /><br />
우선 간단하게 ERD를 작성해 보았다. 오늘 처음 사용한 툴인데도 쉽게 익숙해져 편하게 만들 수 있었다. 테이블 이름을 입력한 후 as ~~ 를 통해 실사용 테이블명을 설정할 수 있고, FK를 입력한 후 &gt;- 참조할_테이블.키 를 입력하면 쉽게 화살표를 통해 테이블 관계를 나타낼 수 있다. 오른쪽의 테이블에서는 편하게 내가 설계한 것들을 파악할 수 있게 되어 있다. 기본 ERD를 조금만 들여다봐도 쉽게 응용할 수 있고, 테이블도 자유롭게 이동하면서 작성할 수 있다.<br />
깔끔하고 눈에 잘 들어오는 디자인도 마음에 들었다!</p>
<p><img src="https://velog.velcdn.com/images/kijrary/post/bbb21cfd-ce19-4768-a4d1-89aabcfac223/image.png" /><br />
작성한 파일을 추출해 보았다. 상단의 EXPORT 메뉴를 통해 원하는 형식으로 추출할 수 있다. 나는 MySQL을 사용하므로 해당 메뉴를 클릭해 보았다.<br />
<img src="https://velog.velcdn.com/images/kijrary/post/5b0691cf-7040-47d7-a686-895a7b42ef83/image.png" /><br />
파일이 자동으로 다운받아지고, 이런 식으로 만들어진 sql 파일을 볼 수 있게 된다.</p>
<p><img src="https://velog.velcdn.com/images/kijrary/post/7d8eb35f-d2af-48bc-bf56-40ae50f9e592/image.png" /><br />
Share 버튼을 통해 만들어진 다이어그램을 링크 공유 형태로 공유할 수도 있고,<br />
<img src="https://velog.velcdn.com/images/kijrary/post/cf8dee55-ded6-4f0e-aca1-63efd746b0e1/image.png" /><br />
File &gt; Collaborate 기능을 통해 팀원과 협업할 수 있다. <img src="https://velog.velcdn.com/images/kijrary/post/f5f11f94-d82f-4d8c-897a-09bf034b2c0d/image.png" /><br />
해당 메뉴를 누르면 협업할 팀원을 초대할 수 있는 기능이 나온다.</p>
<p>이전에 데이터베이스와 SQL을 공부할 때에는 이러한 툴이 있다는 것을 알지 못했는데, 좋은 기회로 다양한 툴이 있다는 것을 알게 되어서 앞으로 유용하게 사용할 수 있을 것이라고 생각했다. 또한 서버 공부를 하기 위해서 필수적으로 필요한 도구라고 생각한다. 공개적으로 프로젝트가 공유된다는 점에서, 팀 단위로 협업할 때 제일 쓰기 편한 툴이라고 생각된다. 그래서 앞으로 동아리를 통해 서버 공부를 하고 프로젝트를 진행하는 동안 꾸준하게 사용하게 될 것 같다! 그리고 앞으로 서버 개발자가 된다면... 더더욱 사용할 것이다. 앞으로 QuickDBD와 함께 재미있고 효율적으로 공부를 해보고 싶다!</p>
<h3 id="1년-무료-권한-받는-방법">1년 무료 권한 받는 방법</h3>
<ol>
<li>Quick DBD free trial을 간단히 사용해 본 후 블로그에 리뷰 글을 작성한다. 특별히 주의해야 할 점이 있는데, 단어 수가 500자 이상이어야 한다는 것이다!</li>
<li>promo@quickdbd.com으로 리뷰를 작성한 블로그의 링크를 담아 권한 신청에 대한 메일을 보낸다.</li>
<li>확인 메일을 받으면 메일의 안내 내용대로 해당 이메일로 QuickDBD에 로그인하고, 등록한다.</li>
<li>Quick DBD 오른쪽 상단의 Account에 들어가 Pro plan expires on - email confirmed를 확인하고, 사용하면 된다!</li>
</ol>
<p><img src="https://velog.velcdn.com/images/kijrary/post/8b3b47e9-8f7e-4b1d-aacf-9bd691c12bb9/image.png" /><br />
