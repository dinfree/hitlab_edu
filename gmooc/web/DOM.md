# [STS-10] 웹프로그래밍 :: 짧고 굵게 배우기


[STS-10]은 웹프로그래밍의 핵심 개념에서 부터 주요 기술인 html, css, javascript를 비롯해 필수 응용 라이브러리인 bootstrap, jquery까지를 다루는 과정 입니다.

 ## JavaScript 문서 객체 모델(DOM)
컴퓨터 사용이 익숙하지 않은 분들을 위한 기초 학습 입니다. 컴퓨터와 운영체제, 파일관리 및 명령프롬프트 사용, 크롬 웹 브라우저 등 
프로그램 개발 이전에 반드시 알아야 할 컴퓨터 사용법에 대해 다루게 됩니다. 만일 컴퓨터 사용이 익숙하다면 이번 장은 넘어가도 됩니다.

### 목차
1. DOM의 개념
2. document 객체
3. DOM 요소
4. 노드

---
## 1. DOM의 개념

DOM이란 XML이나 HTML 문서에 접근하기 위한 일종의 인터페이스입니다.

DOM은 문서 내의 모든 요소를 정의하고, 각각의 요소에 접근하는 방법을 제공합니다.
![샘플이미지](https://imgur.com/RqsKzMb.jpg")

JavaScript는 이러한 DOM을 이용하여 HTML의 요소, 속성, 스타일 등을 변경할 수 있습니다.
#### DOM의 종류
1. Core DOM : 모든 문서 타입을 위한 DOM 모델

2. HTML DOM : HTML 문서를 위한 DOM 모델<br>
모든 HTML 요소는 HTML DOM를 통해 접근할 수 있습니다.

3. XML DOM : XML 문서를 위한 DOM 모델<br>
모든 XML 요소는 XML DOM를 통해 접근할 수 있습니다.

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




### 참고자료
- DOM 메소드
    >https://bit.ly/2qW7t9n 

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

---

## 3. DOM 요소

HTML 요소를 다루기 위해서는 우선 해당 요소를 선택해야만 합니다.<br>
자바스크립트에서 특정 HTML 요소를 선택하는 방법은 다음과 같습니다.
1. HTML 태그 이름(tag name)을 이용한 선택
```javascript
var selectedItem = document.getElementsByTagName("li"); 
// 모든 <li> 요소를 선택함.
```
2. 아이디(id)를 이용한 선택
```javascript
var selectedItem = document.getElementById("even"); 
// 아이디가 "even"인 요소를 선택함.
```
3. 클래스(class)를 이용한 선택
```javascript
var selectedItem = document.getElementsByClassName("odd"); 
// 클래스가 "odd"인 모든 요소를 선택함.
```
4. name 속성(attribute)을 이용한 
선택
```javascript
var selectedItem = document.getElementsByName("first"); 
// name 속성값이 "first"인 모든 요소를 선택함.
```
5. CSS 선택자(selector)를 이용한 선택
```javascript
var selectedItem = document.querySelectorAll("li.odd"); 
// 클래스가 "odd"인 요소 중에서 <li> 요소만을 선택함.
```
6. HTML 객체 집합(object collection)을 이용한 선택
```javascript
var title = document.title; 
// <title> 요소를 선택함.
```
#### DOM 요소의 변경

HTML DOM을 이용하면 HTML 요소의 내용(content)이나 속성값이나 스타일 등을 손쉽게 변경할 수 있습니다.

HTML 요소의 내용을 변경하는 가장 쉬운 방법은 innerHTML 프로퍼티를 이용하는 것입니다.

```javascript
var str = document.getElementById("text");
str.innerHTML = "문장바껴라";
```

### 동영상 강좌
- DOM 메소드와 속성
    >https://bit.ly/2vpvrdH 
12분 11초


### 참고자료
- DOM 요소
    >https://bit.ly/2OjjRHR 


### 퀴즈
#### 1) HTML 요소의 내용을 바꾸는 가장 쉬운 방법은 무엇인가?
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

## 4. 노드

#### 노드란?
- HTML DOM은 노드(node)라고 불리는 계층적 단위에 정보를 저장하고 있습니다.
- HTML DOM은 이러한 노드들을 정의하고, 그들 사이의 관계를 설명해 주는 역할을 합니다.
- HTML 문서의 정보는 노드 트리(node tree)라고 불리는 계층적 구조에 저장됩니다.
- 이러한 노드 트리는 노드들의 집합이며, 노드 간의 관계를 보여줍니다.
- 노드 트리는 최상위 레벨인 루트 노드(root node)로부터 시작하여, 가장 낮은 레벨인 텍스트 노드까지 뻗어 내려갑니다.
- 자바스크립트에서는 HTML DOM을 이용하여 노드 트리에 포함된 모든 노드에 접근할 수 있습니다.

#### 노드의 종류

- **문서 노드(document node)**: HTML 문서 전체를 나타내는 노드
- **요소 노드(element node)**: 모든 HTML 요소는 요소 노드이며, 속성 노드를 가질 수 있는 유일한 노드
- **속성 노드(attribute node)**: 모든 HTML 요소의 속성은 속성 노드이며, 요소 노드에 관한 정보를 가지고 있음.<br>
하지만 해당 요소 노드의 자식 노드(child node)에는 포함되지 않음.
- **텍스트 노드(text node)**: HTML 문서의 모든 텍스트는 텍스트 노드
- **주석 노드(comment node)**: HTML 문서의 모든 주석은 주석 노드

#### 노드간의 관계

![샘플이미지](https://imgur.com/AMF0f1q.jpg")

*루트 노드를 제외한 모든 노드는 단 하나의 부모 노드만 가집니다.<br> 모든 요소 노드는 자식 노드를 가질 수 있습니다.*
- **루트노드**: 노드 트리의 가장 상위에 있는 단 하나의 노드. 
- **형제노드**: 같은 부모 노드를 가지는 모든 노드.
- **조상노드**: 부모 노드를 포함해 계층적으로 현재 노드보다 상위에 존재하는 모든 노드.
- **자손노드**: 자식노드를 포함해 계층적으로 현재 노드보다 하위에 있는 모든 노드.

### 참고자료
- 노드
    >https://bit.ly/2LZpb6O 

---
