# [STS-10] 웹프로그래밍 :: 짧고 굵게 배우기

[![Dinfree][din-badge]][din-url]
[![Subject][basic-badge]][din-url]

[STS-10]은 웹프로그래밍의 핵심 개념에서 부터 주요 기술인 html, css, javascript를 비롯해 필수 응용 라이브러리인 bootstrap, jquery까지를 다루는 과정 입니다.

 ## JavaScript - DOM(문서 객체 모델)
 JavaScript에서 사용하는 문서객체 모델(DOM)이 무엇이며, 어떻게 사용하고, 어느 때에 어떤 메서드를 사용하는지에 대해 알아봅니다. 

### 목차
1. [DOM의 개념](#m1)
2. [Document 객체](#m2)

---
<a id="m1"></a>

## 1. DOM의 개념
JavaScript는 DOM을 이용하여 HTML의 요소, 속성, 스타일 등을 변경할 수 있습니다.

<img class="img-shadow" alt="js_3-1" src="img/js_3-1.jpg" width="70%" >

- DOM이란 `XML이나 HTML문서에 접근하기 위한 일종의 인터페이스`입니다.
- DOM은 문서 내의 모든 요소를 정의하고 각각의 요소에 `접근하는 방법을 제공`합니다.
- 웹페이지가 열리면 브라우저는 페이지의 문서 객체 모델을 만듭니다.

### 동영상 강좌
- DOM이란
  > https://bit.ly/2M0PaLa  `05:19`
- What is the DOM in JavaScript?
  > https://bit.ly/2niZ0ZQ `04:31`


### 참고자료
- DOM Intro
  > https://bit.ly/2riNpxI 


### 퀴즈
#### 1) DOM은 왜 사용하는가?
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

> HTML의 요소, 속성, 스타일 등을 변경할 수 있습니다.

</div>
</details> 

---
<a id="m2"></a>

## 2. document 객체

document객체는 `웹 페이지`를 의미합니다. 웹페이지에 존재하는 HTML요소에 접근할 때는 반드시 `document객체`부터 시작해야 합니다.

#### 1) Document 메소드

- HTML 요소선택
```javascript
document.getElementsByTagName("tag_name")
document.getElementById("id_name")
document.getElementsByClassName("class_name")
document.getElementByName("name_attribute")
document.querySelectorAll("selector")
```

- HTML 요소생성
```javascript
document.createElement("HTML_element")
document.write("text")
```

- HTML 이벤트핸들러 추가
```javascript
document.getElementById("id_name").onclick = function(){ code };
```

#### 2) DOM 요소의 변경

- innerHTML 이용.
```js
var str = document.getElementById("text");
str.innerHTML = "changed text";
```

- HTML 요소의 속성값 변경
```js
element.setAttribute(attribute, value)
```

- HTML 요소 생성, 제거, 추가
```js
document.createElement(element)        
document.removeChild(element)          
document.appendChild(element)          
document.replaceChild(element)                    
```

- DOM의 사용 예시
```html
<html>
  <body>
    <p id="intro">Hello World!</p>
    <p>This example demonstrates the <b>getElementById</b> method!</p>
    <p id="demo"></p>             
    
    <script>
      var myElement = document.getElementById("intro");  
      document.getElementById("demo").innerHTML = "The text from the intro paragraph is " + myElement.innerHTML;
    </script>
  </body>
</html>
```

##### 실행 결과
<p id="intro">Hello World!</p>
<p>This example demonstrates the <b>getElementById</b> method!</p>
<p id="demo"></p>             
<script>
  var myElement = document.getElementById("intro");
  document.getElementById("demo").innerHTML = "The text from the intro paragraph is " + myElement.innerHTML;
</script>


### 동영상 강좌
- DOM 객체
  > https://bit.ly/2LYf169 `10:33`
- DOCUMENT 객체
  > https://bit.ly/2vGRQCA `07:52`
- 자바스크립트(javascript)와 DOM 프로그래밍
  > https://bit.ly/2nk8nJ0 `07:48`
- DOM 메소드와 속성
  > https://bit.ly/2vpvrdH `12:11`


### 참고자료
- DOM 메소드
  > https://bit.ly/2qW7t9n 
- DOM 요소
  > https://bit.ly/2OjjRHR 


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

> innerHTML 메소드를 사용하여 바꾼다.   
```js
str.innerHTML="changed text";
```

</div>
</details> 



[din-badge]:https://img.shields.io/badge/dinfree-edu-orange.svg
[din-url]:https://github.com/dinfree
[basic-badge]:https://img.shields.io/badge/core-basic-green.svg