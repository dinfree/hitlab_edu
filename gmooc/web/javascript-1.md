# [STS-10] 웹프로그래밍 :: 짧고 굵게 배우기


[STS-10]은 웹프로그래밍의 핵심 개념에서 부터 주요 기술인 html, css, javascript를 비롯해 필수 응용 라이브러리인 bootstrap, jquery까지를 다루는 과정 입니다.

 ## JavaScript
이부분은 해당 챕터에 대한 설명과 안내가 나와야 하는데 우선 이부분은 비워 두도록 한다.

### 목차
1. JavaScript 소개
2. JavaScript 기본문법
---
## 1. JavaScript 소개
### JavaScript란
- JavaScript는 객체(object) 기반의 스크립트 언어입니다.
- JavaScript는 웹의 동작을 구현할 수 있습니다.
- JavaScript는 주로 웹 브라우저에서 사용되나, Node.js와 같은 프레임워크를 사용하면 서버 측 프로그래밍에서도 사용할 수 있습니다.
- 현재 컴퓨터나 스마트폰 등에 포함된 대부분의 웹 브라우저에는 JavaScript 인터프리터가 내장되어 있습니다.


### JavaScript의 특징
![샘플이미지](https://imgur.com/X39ar6b.jpg")
1. JavaScript는 객체 기반의 스크립트 언어입니다.
2. JavaScript는 동적이며, 타입을 명시할 필요가 없는 *인터프리터* 언어입니다.
3. JavaScript는 객체 지향형 프로그래밍과 함수형 프로그래밍을 모두 표현할 수 있습니다.
4. JacaScript는 HTML의 '내용','속성','스타일'을 변경 할 수 있습니다.

 *인터프리터* 언어란 컴파일 작업을 거치지 않고, 소스 코드를 바로 실행할 수 있는 언어를 의미합니다.
JavaScript는 웹 브라우저에 포함된 JavaScript 인터프리터가 소스 코드를 직접 해석하여 바로 실행해 줍니다.

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
#### 1) 인터프리터 언어란 무엇인가요?
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```
정답: 컴파일 작업을 거치지 않고, 소스 코드를 바로 실행할 수 있는 언어입니다 
```
</div>
</details>


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

- HTML에서는 JavaScript 코드는 반드시 *script* 태그 사이에 작성해야합니다.
-JavaScript의 실행문은 세미콜론(;)으로 구분됩니다.

### 변수 선언 
- 기본적으로 **var** 이라는 키워드로 변수를 선언할 수 있습니다.<br>
- 변수이름은 대소문자를 구별합니다.
- 변수는 한번에 여러개 선언할 수 있습니다.
- 변수는 지역변수와 전역변수가 있습니다.
```javascript
var a,A;
a=10;
```
### string 변수
- string 변수는 큰따옴표("") 또는 작은따옴표('')로 표현할 수 있습니다.
```javascript
var a;
a="Java Script";
```
### 배열 선언
- 배열(array)은 이름과 인덱스로 참조되는 정렬된 값의 집합으로 정의됩니다.
- 배열을 구성하는 각각의 값을 배열 요소(element)라고 하며, 배열에서의 위치를 가리키는 숫자를 인덱스(index)라고 합니다.

```javascript
var korea=['seoul','busan','incheon'];
```
### 출력 방법
 innerHTML을 사용하여 HTML 요소에 작성하기 .>
```JavaScript
<script>
document.getElementById("id").innerHTML = 5 + 6;
</script>
```

document.write ()를 사용하여 HTML 출력에 쓰기 .
```JavaScript
<script>
document.write(5 + 6);
</script>
```
 window.alert ()를 사용하여 알림창에 쓰기 .
```JavaScript
<script>
window.alert(5 + 6);
</script>
```
console.log ()를 사용하여 브라우저 콘솔에 기록하기 . 
```JavaScript
<script>
console.log(5 + 6);
</script>
```
### 연산자
> 변수 값은 사칙연산으로 계산될 수 있습니다.
```javascript
var a, b, c;
a=10;
b=5;
c = a * b;
```
 사칙연산 외에도 여러 연산자(논리, 비교연산자)가 있습니다.<br><br>
비교연산자


| **Operator** | Description                       |
|----------|-----------------------------------|
| **==**       | equal to                          |
| **===**      | equal value and equal type        |
| **!=**       | not equal                         |
| **!==**      | not equal value or not equal type |
| **>**        | greater than                      |
| **<**        | less than                         |
| **>=**       | greater than or equal to          |
| **<=**       | less than or equal to             |
| **?**        | ternary operator                  |

논리연산자


| **Operator** | Description |
|----------|-------------|
| **&&**       | logical and |
| &#124;	&#124;	       | logical or  |
| **!**        | logical not |


### 주석달기
주석은 // 와 /* example */ 형식으로 처리할 수 있습니다.
```javascript
var a, b, c;    //a,b,c 변수 선언
a=10;
b=5;
c = a * b;
/* c=50이다 */
```

### JavaScript 적용방법

**1. 내부 JavaScript 코드로 적용**<br>
JavaScript 코드는 *script*태그를 사용하여 HTML 문서 안에 삽입할 수 있습니다.
```javascript
<script>
    document.getElementById("text").innerHTML = "여러분을 환영합니다!";
</script>
```
이렇게 삽입된 JavaScript 코드는 HTML 문서의 *head*태그나 *body*태그, 또는 양쪽 모두에 위치할 수 있습니다.
```javascript
<head>

    <meta charset="UTF-8">

    <title>JavaScript Apply</title>

    <script>

        function printDate() {

            document.getElementById("date").innerHTML = Date();

        }

    </script>

</head>
```
*head* 태그에 JavaScript 코드 적용

**2. 외부 JavaScript 파일로 적용**

- JavaScript 코드는 HTML 문서의 내부뿐만 아니라 외부 파일로 생성하여 삽입할 수도 있습니다.
- 외부에 작성된 JavaScript 파일은 .js 확장자를 사용하여 저장합니다.
- 해당 JavaScript 파일을 적용하고 싶은 모든 웹 페이지에 *script* 태그를 사용해 외부 JavaScript 파일을 포함하면 됩니다.

```javascript
//example.js 파일
function printDate() {

    document.getElementById("date").innerHTML = Date();

}
```

```javascript
//외부 JavaScript 파일 포함 방법
<head>

    <meta charset="UTF-8">

    <title>JavaScript Apply</title>

    <script src="/examples/media/example.js"></script>

</head>
```

- 외부 JavaScript 파일을 사용하면 웹의 내용을 담당하는 HTML 코드로부터 웹의 동작을 구현하는 JavaScript 코드를 분리할 수 있습니다.
- 이렇게 하면 HTML 코드와 JavaScript 코드를 각각 읽기도 편해지고, 유지 보수도 쉬워집니다.
- 외부 JavaScript 파일은 웹 브라우저가 미리 읽어 올 수 있어 웹 페이지의 로딩 속도 또한 빨라집니다.

### 동영상 강좌

- JavaScript의 기본적인 문법 
    >https://bit.ly/2JLD2r7 
17분 24초
- JavaScript의 기본 구문
    >https://bit.ly/2uTsIbt 
14분 58초
- JavaScript 기초 
    >https://bit.ly/2NETqMr 
10분 43초
- JavaScript 기초 문법
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
정답: script
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
