# [STS-10] 웹프로그래밍 :: 짧고 굵게 배우기

[STS-10]은 웹프로그래밍의 핵심 개념에서 부터 주요 기술인 html, css, javascript를 비롯해 필수 응용 라이브러리인 bootstrap, jquery까지를 다루는 과정 입니다.

 ## JavaScript 함수와 이벤트 처리
컴퓨터 사용이 익숙하지 않은 분들을 위한 기초 학습 입니다. 컴퓨터와 운영체제, 파일관리 및 명령프롬프트 사용, 크롬 웹 브라우저 등 
프로그램 개발 이전에 반드시 알아야 할 컴퓨터 사용법에 대해 다루게 됩니다. 만일 컴퓨터 사용이 익숙하다면 이번 장은 넘어가도 됩니다.

### 목차
1. JavaScript 함수
2. JavaScript 이벤트처리

---
## 1. JavaScript 함수

### 함수 선언 방법

JavaScript에서 함수는 *function*이라는 키워드를 통해 정의됩니다. 함수명은 변수같이 지어질 수 있으며 파라미터를 가지고 있을수 있습니다.
```javascript
function name (one ,two ,three){
    함수 기능
}
```
### 함수 리턴값

함수는 호출되면 리턴값을 내놓습니다.
```javascript
var a= name(2,3);      //2*3=6 리턴
function name(x,y){
    return x*y;
}
```

### 함수를 쓰는 이유
![샘플이미지](https://imgur.com/TgWo9lG.jpg")

코드를 한번 정의하면, 그 코드를 여러번 갖다 쓸 수 있습니다.

### 동영상 강좌
- JavaScript 함수란?
    >https://bit.ly/2zY2xWG 
10분 07초
- 함수 사용하기
    >https://bit.ly/2uXlXW9 
5분 44초
- JavaScript Functions
    >https://bit.ly/2mzrSN0 
6분 28초
- Javascript Functions Tutorial
    >https://bit.ly/2uW6qpn 
13분 49초
- JavaScript 함수 (리턴)
    >https://bit.ly/2Lwu7Pn 
7분 19초


### 참고 자료
- JavaScript Function Definitions
    >  https://www.w3schools.com/js/js_function_definition.asp
    
### 퀴즈

#### 1) JavaScript를 이용하여 두 값을 합하는 함수를 정의하세요
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```javascript
function add(a,b){
    return a+b;
}
```
</div>
</details>

---
#### 2) 위의 정의한 함수를 호출하세요
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```javascript
var x=add(4,3);
```
</div>
</details>

---

## 2. JavaScript 이벤트처리

![샘플이미지](https://imgur.com/YGSKBHH.jpg")

- JavaScript를 이용하면 클릭같은 이벤트가 감지될 때 코드를 실행할 수 있습니다.
- 사용자의 입력값을 가져올 수 있습니다.
- HTML 이벤트 속성은 JavaScript 코드를 직접 실행할 수 있고 함수를 호출할 수 있습니다.
- HTML 요소에 고유한 이벤트 핸들러 함수를 할당할 수 있습니다.
- 이벤트가 막무가내로 보내지거나 처리되는 것을 막을 수 있습니다.

클릭이벤트 예시(버튼을 누르면 날짜 표시)
```javascript
<button onclick="document.getElementById('id').innerHTML = Date()">The time is?</button>
```

### 캡처링 & 버블링
- 캡처링: 이벤트가 부모로부터 발생하여 자식으로 전파되는 방식.
- 버블링: 이벤트가 자식으로부터 발생하여 부모로 전파되는 방식.
### 동영상 강좌
- JavaScript – 이벤트
    >https://bit.ly/2NzNcxG 
4분 24초
- 자바스크립트 이벤트 사용법
    >https://bit.ly/2O9IpnF 
17분 07초
- JavaScript - 이벤트전파 (1/3) : 소개
    >https://bit.ly/2O8OcK5 
5분 08초
- JavaScript - 이벤트전파 (2/3) : 캡처링
    >https://bit.ly/2NCqsNq 
10분 38초
- JavaScript - 이벤트전파 (3/3) : 버블링
    >https://bit.ly/2LyDaPK 
10분 27초
- JavaScript - 마우스 이벤트
    >https://bit.ly/2JKCUbG 
14분 19초
- JavaScript - 폼 이벤트
    >https://bit.ly/2LtfxZ0 
8분 43초
- JavaScript - 문서로드 이벤트
    >https://bit.ly/2Lhg1SR 
10분 19초
    
### 참고 자료
- JavaScript Events
    >  https://www.w3schools.com/js/js_events.asp

### 퀴즈

#### 1) onClick 이벤트를 이용하여 버튼을 누르면 "hello world" 문구가 나오도록 하세요(힌트: style="display:none")
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```javascript
<!DOCTYPE html>
<html>
<body>

<p></p>

<p id="id" style="display:none">Hello World!</p>

<button type="button" onclick="document.getElementById('id').style.display='block'">Click Me!</button>

</body>
</html> 

```
</div>
</details>

---
