# [STS-10] 웹프로그래밍 :: 짧고 굵게 배우기


[STS-10]은 웹프로그래밍의 핵심 개념에서 부터 주요 기술인 html, css, javascript를 비롯해 필수 응용 라이브러리인 bootstrap, jquery까지를 다루는 과정 입니다.

 ## JavaScript 문서 객체 모델(DOM)
 JavaScript에서 사용하는 문서객체 모델(DOM)이 무엇이며, 어떻게 사용하고, 어느 때에 어떤 메서드를 사용하는지에 대해 알아봅니다. 

### 목차
1. DOM의 개념
2. Document 객체

---
## 1. DOM(Document Object Model)의 개념

- DOM이란 XML이나 HTML 문서에 접근하기 위한 일종의 인터페이스입니다.<br>
- DOM은 문서 내의 모든 요소를 정의하고, 각각의 요소에 접근하는 방법을 제공합니다.
- 웹페이지가 열리면 브라우저는 페이지의 문서 객체 모델을 만듭니다.
![샘플이미지](https://imgur.com/RqsKzMb.jpg")

JavaScript는 이러한 DOM을 이용하여 HTML의 요소, 속성, 스타일 등을 변경할 수 있습니다.


### 동영상 강좌
- DOM이란
    >https://bit.ly/2M0PaLa  5분 19초
- What is the DOM in JavaScript?
    >https://bit.ly/2niZ0ZQ 
4분31초

### 참고자료
- DOM Intro
    >https://bit.ly/2riNpxI 


### 퀴즈
#### 1) DOM은 왜 사용하는가?
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```
HTML의 요소, 속성, 스타일 등을 변경할 수 있습니다.
```
</div>
</details> 

---

## 2. document 객체

document 객체는 웹 페이지 그 자체를 의미합니다. <br>
웹페이지에 존재하는 HTML 요소에 접근 할 때는 반드시 **document**객체부터 시작해야합니다.
### Document 메소드

1) HTML 요소의 선택
```javascript
document.getElementsByTagName("태그이름") //해당 태그 이름의 요소를 모두 선택

document.getElementById("아이디")//해당 아이디의 요소를 선택함.

document.getElementsByClassName("클래스이름")//해당 클래스에 속한 요소를 모두 선택함.

document.getElementByName("name속성값")//해당 name 속성값을 가지는 요소를 모두 선택함.

document.querySelectorAll("선택자")//해당 선택자로 선택되는 요소를 모두 선택함.
```
2) HTML 요소의 생성
```javascript
document.createElement("HTML요소")//지정된 HTML 요소를 생성함.

document.write("텍스트")//HTML 출력 스트림을 통해 텍스트를 출력함.
```
3) HTML 이벤트 핸들러 추가
```javascript
document.getElementById("아이디").onclick = function(){ 실행할 코드 }//마우스 클릭 이벤트와 연결될 이벤트 핸들러 코드를 추가함.
```

#### DOM 요소의 변경

- HTML DOM을 이용하면 HTML 요소의 내용(content)이나 속성값이나 스타일 등을 손쉽게 변경할 수 있습니다.
- HTML 요소의 내용을 변경하는 가장 쉬운 방법은 innerHTML 프로퍼티를 이용하는 것입니다.

```javascript
var str = document.getElementById("text");
str.innerHTML = "문장바껴라";
```
HTML 요소의 변경, 추가, 제거
```javascript
element.attribute = new value          //HTML 요소의 속성값 변경
element.setAttribute(attribute, value) //HTML 요소의 속성값 변경
element.style.property = new style     //HTML 요소의 스타일 변경

document.createElement(element)        //HTML 요소의 생성
document.removeChild(element)          //HTML 요소 제거
document.appendChild(element)          //HTML 요소 추가
document.replaceChild(element)         //HTML 요소 대체
document.write(text)                   //HTML로 출력
```

DOM의 사용 예시
```html
<!DOCTYPE html>
<html>
<body>

<p id="intro">Hello World!</p>   //id가 intro 인 p태그

<p>This example demonstrates the <b>getElementById</b> method!</p>

<p id="demo"></p>               //id가 demo인 p태그

<script>
var myElement = document.getElementById("intro");  //intro 아이디의 요소를 선택함.
document.getElementById("demo").innerHTML =         //demo 아이디의 요소를 선택 후 innerHTML 로 내용 변경.
"The text from the intro paragraph is " + myElement.innerHTML;
</script>

</body>
</html>

```
결과<br>
Hello World!

This example demonstrates the **getElementById** method!

The text from the intro paragraph is Hello World!


### 동영상 강좌
- DOM 객체
    >https://bit.ly/2LYf169 
10분 33초
- DOCUMENT 객체
    >https://bit.ly/2vGRQCA 
7분 52초
- 자바스크립트(javascript)와 DOM 프로그래밍
    >https://bit.ly/2nk8nJ0 
7분48초
- DOM 메소드와 속성
    >https://bit.ly/2vpvrdH 
12분 11초

### 참고자료
- DOM 메소드
    >https://bit.ly/2qW7t9n 
- DOM 요소
    >https://bit.ly/2OjjRHR 

### 퀴즈
#### 1) document 메소드를 이용하여 HTML 클래스이름이 “happy”에 속한 요소들을 모두 선택하시오.
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```javascript
document.getElementsByClassName("happy")
```
</div>
</details> 

#### 2) HTML 요소의 내용을 바꾸는 가장 쉬운 방법은 무엇인가?
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```
innerHTML 메소드를 사용하여 바꾼다. 
ex) str.innerHTML="바꾸기";
```
</div>
</details> 

---



