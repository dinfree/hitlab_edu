# [STS-10] 웹프로그래밍 :: 짧고 굵게 배우기

[![Dinfree][din-badge]][din-url]
[![Subject][basic-badge]][din-url]

[STS-10]은 웹프로그래밍의 핵심 개념에서 부터 주요 기술인 html, css, javascript를 비롯해 필수 응용 라이브러리인 bootstrap, jquery까지를 다루는 과정 입니다.

## 월드와이드웹과 HTML
월드와이드웹이 무엇이며 인터넷과의 차이를 이해하고 HTML의 기본적인 학습을 합니다. HyperText와 Markup의 의미를 통해 HTML이 무엇인지 알아보고 HTML에서 태그를 사용하는 방법과 HTML문서의 기본 구조에 대해 학습합니다. 

### 목차
1. [월드와이드웹](#m1)
2. [HTML 소개](#m2)
3. [HTML 기본 작성법](#m3)
4. [HTML 기본 구조](#m4)

---
<a id="m1"></a>

## 1. 월드와이드웹
웹이라고도 불리며 다양한 형태의 데이터와 정보에 접근할 수 있도록 해주는 `인터넷 서비스`입니다. 월드와이드웹은 팀 버너스-리에 의해 개발되어 보편적인 인터넷 서비스로 확대되었습니다.

<img class="img-shadow" alt="html_1-1" src="img/html_1-1.png" width="70%">
<!-- 이미지 주소 : http://techlearninghub.com/difference-bw-internet-web/ -->

- 웹은 인터넷 상의 정보를 `하이퍼텍스트`방식과 멀티미디어 환경에서 검색할 수 있게 해주는 정보 검색 시스템입니다.
- 웹 서비스의 목적은 많은 사람들이 정보를 쉽게 공유하고 접근할 수 있도록 하는 것입니다.
- 웹은 전 세계 컴퓨터를 연결하며 HTTP 프로토콜을 사용하고 HTML로 작성된 문서를 연결하여 멀티미디어 서비스를 제공합니다.
- 인터넷은 `컴퓨터 네트워크 망`을 의미하고, 웹은 `인터넷 서비스`입니다.

### 동영상 강좌
- What is the world wide web? `03:54`
  > http://bit.ly/2zXoOnv
- 웹 서비스? `02:39`
  > http://bit.ly/2mBncGF
- 웹의 개요 `04:46`
  > http://bit.ly/2NAmS6t (00:00~04:46) `04:46`
- 인터넷과 웹의 역사 `08:07`
  > http://bit.ly/2Lg2CKH
- 웹의 의미와 역사 `10:37`
  > http://bit.ly/2NCDvP5

### 참고 자료
- 웹이란 무엇인가
  > http://bit.ly/2zWAYgD
- 웹의 역사
  > http://bit.ly/2uTkcZS
- 인터넷과 웹의 역사
  > http://bit.ly/2mz5fIE

### 퀴즈
#### 1) 월드 와이드 웹이란 무엇인가
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

> 다양한 형태의 데이터와 정보에 접근할 수 있도록 해주는 인터넷 서비스

</div>
</details>

#### 2) 웹과 인터넷에 대해 서술하시오
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

> 인터넷은 컴퓨터 네트워크 망을 의미하고, 웹은 인터넷 서비스 중 하나입니다.

</div>
</details>

<br>

---
<a id="m2"></a>

## 2. HTML 소개
웹 문서를 만들기 위해 사용하는 프로그래밍 언어 중 하나입니다. 하이퍼텍스트 작성을 위해 개발되었으며 대부분의 웹 페이지들은 HTML로 작성됩니다.

<img class="img-shadow" alt="html_1-2-1" src="img/html_1-2-1.jpg" width="50%">
<!-- 이미지 주소 : http://kyd5083.blogspot.com/2013/02/web-html.html -->

- HTML은 `HyperText Markup Language`의 약자로 웹 페이지를 만들기 위한 표준 마크업 언어를 의미합니다.
- `HyperText`는 단순 텍스트 이상의 링크 등의 개념이 포함 된 텍스트를 의미하며 `Markup`은 꺽쇠(< >)로 이루어진 태그를 사용하는 규격을 의미합니다.
- HTML 요소는 HTML 페이지의 구성요소로 태그로 표현됩니다.
- HTML로 작성된 문서를 웹 브라우저가 해석하여 이용자에게 보여줍니다.


### 동영상 강좌
- 웹 프로그래밍이란? 
  > http://bit.ly/2O5bpwC (5:06~15:40) `10:34`
- HTML에서 hyperText Markup 의미
  > http://bit.ly/2NwOSYy `07:14`
- 언어로써의 HTML 의미 알아보기
  > http://bit.ly/2JPbFwI (~3:36) `03:36`
- HTML의 역사 
  > http://bit.ly/2Nzjzwc `10:09`


### 참고 자료
- HTML 입문
  > http://bit.ly/2mBnMUR
- HTML5와 XHTML
  > http://bit.ly/2LDiX8t  
- HTML 기초
  > http://bit.ly/2JLN7V5

### 퀴즈
#### 1) HTML은 무엇의 약자인가
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

- HyperText Markup Language

</div>
</details>

<br>

---
<a id="m3"></a>

## 3. HTML 기본 작성법
HTML에서는 `태그(Tag)`를 사용하며 태그는 `< >`를 사용하여 나타냅니다. 태그는 일반적으로 시작과 끝을 표시하는 `2개의 쌍`으로 이루어져 있으며, 종료태그 앞에는 `/`을 붙여줍니다. 태그의 이름은 규칙으로 정해져 있고 태그마다 역할이 다릅니다.

<img class="img-shadow" alt="샘플이미지" src="img/html_1-3.png" width="60%">
<!--이미지 주소 : https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics-->

- `<h1> hello world </h1>`처럼 쌍으로 태그를 사용해 데이터를 표현합니다.
- 태그 안에 다른 태그가 들어 갈 수 있으나 연 순서대로 닫아야 한다.
- 일부 태그는 닫는 태그가 없는 경우도 있습니다.
- 주석은 `<!--내용-->`의 형식으로 사용합니다.

### 동영상 강좌
- HTML 기본 문법 
  > http://bit.ly/2uViKGB `12:07`
- HTML 태그의 속성과 div태그 
  > http://bit.ly/2JLPjvN `04:53`
- 닫는 태그의 사용규칙 
  > http://bit.ly/2O4LHbP `02:49`
- HTML 주석 달기 
  > http://bit.ly/2Led1GJ `01:41`


### 참고 자료
- 태그, 태그의 속성
  > http://bit.ly/2uWbcmU
- 주석
  > http://bit.ly/2NF5eyz
- 태그, 요소, 속성, 변수
  > http://bit.ly/2JOkQ07


### 퀴즈
#### 1) 옳게 태그를 사용한 것은 무엇인가
1. \<p>안녕하세요.
2. \<strong>\<p>안녕하세요\<strong>\<p>
3. \<p>안녕하세요\</p>
4. 안녕하세요.\</strong>

<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

- 정답 : 3번
> [1번] `<p>안녕하세요.` : 태그는 일반적으로 시작과 끝을 표시하는 `2개의 쌍`으로 이루어져야 합니다.   
> [2번] `<strong><p>안녕하세요<strong><p>` : 태그 안에 다른 태그가 들어 갈 수 있으나 연 순서대로 닫아야 합니다.    
> [4번] `안녕하세요.</strong>` : 태그는 일반적으로 시작과 끝을 표시하는 `2개의 쌍`으로 이루어져야 합니다. 

</div>
</details>

#### 2) HTML에서 주석은 어떻게 사용 하는가
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```html
<!-- 저는 주석입니다. -->
```

</div>
</details>

<br>

---
<a id="m4"></a>

## 4. HTML 기본 구조
HTML 문서는 `<!DOCTYPE html>`, `<HTML>`, `<HEAD>`, `<TITLE>`, `<BODY>`의 기본태그로 이루어져 있습니다. 

<img class="img-shadow" alt="html_1-4-1" src="img/html_1-4-1.png" width="40%">
<!-- 사진 주소 : http://lux.cuenet.kr/93-->

- `<!DOCTYPE html>`- HTML5 문서를 선언하는 구문. 웹브라우저에게 문서가 HTML5로 작성됨을 알려줍니다.
- `<HTML>...</HTML>`- HTML 문서의 시작과 끝을 알려줍니다. 
- `<HEAD>...</HEAD>`- 웹 페이지의 정보를 정의합니다. 문서의 상단 제목을 표시하는 `<TITLE>`태그, 문서의 정보를 설정하는 `<meta>`태그 등이 포함됩니다.
- `<BODY>...</BODY>`- 문서 본문에 해당하는 부분으로 실제 화면에 나타나는 내용을 작성합니다.


### 동영상 강좌
- HTML 기본 구조 
  > http://bit.ly/2LiK5xp `13:24`
- HTML head 
  > http://bit.ly/2A2hozw `02:21`
- Title 태그 
  > http://bit.ly/2uWZicu `00:53`
- meta 태그 
  > http://bit.ly/2Lk5V3q `08:45`
- 기본구조 및 시맨틱 태그 
  > http://bit.ly/2LGlgYm `12:51`
- 시맨틱 태그 
  > http://bit.ly/2Ldy8Jj `08:53`


### 참고 자료
- 인코딩, Head태그, title 태그, meta 태그
  > http://bit.ly/2mA4Fu9
- HTML의 기본구성
  > http://bit.ly/2mDkIHy
- body, footer, header, head, html, meta, title 태그
  > http://bit.ly/2LuGaNa

### 퀴즈
#### 1) HTML의 기본 구조를 서술하시오.
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```html
<!DOCTYPE html>
<html>
    <head>
    <title> </title>
    </head>
    
    <body>

    </body>
</html>
```

</div>
</details>

#### 2) Head에는 어떠한 것이 들어가는가
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

> title 태그, meta 태그, 자바 스크립트 및 스타일시트 정의

</div>
</details>


[din-badge]:https://img.shields.io/badge/dinfree-edu-orange.svg
[din-url]:https://github.com/dinfree
[basic-badge]:https://img.shields.io/badge/core-basic-green.svg