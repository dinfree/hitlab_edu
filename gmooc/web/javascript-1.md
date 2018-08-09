# [STS-10] 웹프로그래밍 :: 짧고 굵게 배우기


[STS-10]은 웹프로그래밍의 핵심 개념에서 부터 주요 기술인 html, css, javascript를 비롯해 필수 응용 라이브러리인 bootstrap, jquery까지를 다루는 과정 입니다.

 ## JavaScript
이부분은 해당 챕터에 대한 설명과 안내가 나와야 하는데 우선 이부분은 비워 두도록 한다.

### 목차
1. JavaScript 소개
2. JavaScript 기본문법
---
## 1. JavaScript 소개
### JavaScript란 & 배우는 이유?
> JavaScript는 HTML과 웹에서 사용하는 쉽게 배울 수 있는 프로그래밍 언어입니다.

> JavaScript는 웹개발자가 반드시 배워야하는 3가지 언어 중 하나입니다.<br>
웹페이지에서 JavaScript가 안 쓰인것은 없습니다. 


### JavaScript의 특징
- 브라우저 해석기에서 실행되므로 별도의 실행 프로그램이 필요 없습니다.<br>
- 사용자가 배우기 쉽고, 동적인 페이지를 작성할 수 있습니다.<br>
- 클라이언트와 서버 간에 대화 기능이 없습니다.<br>
- 빠르고 쉽게 배울 수 있습니다.<br><br><br>
![샘플이미지](https://imgur.com/X39ar6b.jpg")
<br><br>
- JavaScript는 HTML 내용과 value를 바꿀 수 있습니다.
- JavaScript는 CSS의 스타일을 바꿀 수 있습니다.

### 동영상 강좌
- JavaScript 개요(3분 18초)
    > https://bit.ly/2LIT1YP  
- JavaScript 기본구조(13분 05초)
    >https://bit.ly/2JKOZh3 
- JavaScript  오리엔테이션(23분 51초)
    >https://bit.ly/2LdYPxr 
- What is JavaScript?(2분 16초)
    >https://bit.ly/2LwOuMc 
- How Javascript works(3분 42초)
    >https://youtu.be/b1ieJtIx1NY 
- What Is JavaScript? What Does It Do?(5분 23초)
    >https://bit.ly/2Lgcdkt 

### 참고 자료
- JavaScript Introduction
    >  https://bit.ly/2o4KTKt 
- JavaScript 입문
    >  https://bit.ly/2uI2GbP 

### 퀴즈
#### 1) JavaScript는 클라이언트와 서버간의 대화를 주고받는다 (O/X)
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```
정답: X JavaScript는 클라이언트와 서버간의 대화를 주고받지 않습니다.
```
</div>
</details>

---
#### 2) JavaScript는 HTML으로 작성한 내용을 숨기거나 바꿀 수 있다.(O/X)
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```
정답: O
```
![샘플이미지](https://imgur.com/SVJrECL.jpg")
</div>
</details>

## 2. JavaScript 기본 문법

### 어디에다 작성해야하는지..
- HTML에서는 JavaScript 코드는 반드시 *script* 태그 사이에 작성해야합니다.
- *script* 태그는 *head* 또는 *body* 태그 둘 다 있을 수 있으며, 외부에서도 참조할 수 있습니다.

### 변수 선언 
> 기본적으로 var 이라는 키워드로 변수를 선언할 수 있습니다.<br>
> 변수이름은 대소문자를 구별합니다.
> 변수는 한번에 여러개 선언할 수 있습니다.
> 변수는 지역변수와 전역변수가 있습니다.
```javascript
var a,A;
a=10;
```
### string 변수
> string 변수는 큰따옴표("") 또는 작은따옴표('')로 표현할 수 있습니다.
```javascript
var a;
a="Java Script";
```

### 출력 방법
> innerHTML을 사용하여 HTML 요소에 작성하기 .
><details>
><summary>예시 보기</summary>
><p></p>
><div markdown="1">
>
>```JavaScript
><script>
>document.getElementById("id").innerHTML = 5 + 6;
></script>
>```
></div>
></details>


> document.write ()를 사용하여 HTML 출력에 쓰기 .
><details>
><summary>예시 보기</summary>
><p></p>
><div markdown="1">
>
>```JavaScript
><script>
>document.write(5 + 6);
></script>
>```
></div>
></details>

> window.alert ()를 사용하여 알림창에 쓰기 .
><details>
><summary>예시 보기</summary>
><p></p>
><div markdown="1">
>
>```JavaScript
><script>
>window.alert(5 + 6);
></script>
>```
></div>
></details>

> console.log ()를 사용하여 브라우저 콘솔에 기록하기 . 
><details>
><summary>예시 보기</summary>
><p></p>
><div markdown="1">
>
>```JavaScript
><script>
>console.log(5 + 6);
></script>
>```
></div>
></details>
### 연산자
> 변수 값은 사칙연산으로 계산될 수 있습니다.
```javascript
var a, b, c;
a=10;
b=5;
c = a * b;
```
 사칙연산 외에도 여러 연산자(논리, 비교연산자)가 있습니다.<br><br>
>비교연산자<br>
![샘플이미지](https://imgur.com/uWLTGgu.jpg")<br><br>

> 논리연산자<br>
![샘플이미지](https://imgur.com/uahGXcq.jpg")



### 주석달기
> 주석은 // 와 /* example */ 형식으로 처리할 수 있습니다.
```javascript
var a, b, c;    //a,b,c 변수 선언
a=10;
b=5;
c = a * b;
/* c=50이다 */
```

### 동영상 강좌

- 자바스크립트의 기본적인 문법 
    >https://bit.ly/2JLD2r7 
17분 24초
- 자바스크립트의 기본 구문
    >https://bit.ly/2uTsIbt 
14분 58초
- 자바스크립트 기초 
    >https://bit.ly/2NETqMr 
10분 43초
- 자바스크립트 기초 문법
    >https://bit.ly/2A1SHD5 
34분 13초
- JavaScript 변수 사용법
    >https://bit.ly/2mABwiH 
6분 41초
- JavaScript 반복문
    >https://bit.ly/2JQyyQ6 
11분 08초
- JavaScript_반복문
    >https://bit.ly/2mHdR09 
8분 07초
- JavaScript -조건문
    >https://bit.ly/2uJDscV 
6분 07초
- JavaScript 제어문
    >https://bit.ly/2mDd14p 
19분 50초
- JavaScript –조건문의 응용 (비교 연산자)
    >https://bit.ly/2Lxtrt5 
12분 57초
- JavaScript -배열의 문법
    >https://bit.ly/2LGMZYP 
9분 15초

    
### 참고 자료
- 기본문법
    >  https://brunch.co.kr/@hee072794/27
- 변수 
    >  https://www.w3schools.com/js/js_intro.asp
- 반복문
    >  https://www.w3schools.com/js/js_loop_for.asp
- 조건문
    >  https://www.w3schools.com/js/js_if_else.asp

### 퀴즈
#### 1) JavaScript에서 변수를 선언하는 키워드는?
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```
정답: var
```
</div>
</details>

---
#### 2) JavaScript 코드를 작성하기 위한 태그는?
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```
정답: **script**
```
</div>
</details>

---

#### 3) JavaScript에서 변수의 값을 출력하기 위한 코드 한줄 
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```javascript
<!DOCTYPE html>
<html>
<body>
<script>
var a="JavaScript";
document.write(a);          //정답
</script>

</body>
</html>
```
</div>
</details>
