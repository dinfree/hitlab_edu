# [STS-10] 웹프로그래밍 :: 짧고 굵게 배우기

[![Dinfree][din-badge]][din-url]
[![Subject][basic-badge]][din-url]

[STS-10]은 웹프로그래밍의 핵심 개념에서 부터 주요 기술인 html, css, javascript를 비롯해 필수 응용 라이브러리인 bootstrap, jquery까지를 다루는 과정 입니다.

## HTML - 입력양식
여러가지 입력양식 태그들에 대해 학습합니다. 입력 양식을 만드는 방법을 학습한 후 여러가지 입력 양식들을 만들어봅니다. 또한 입력된 값들이 전달되는 방식을 알아보고 각 방식의 차이를 이해합니다. 

### 목차
1. [입력 양식](#m1)
2. [입력 양식 태그](#m2)
3. [다양한 입력 양식 태그](#m3)

---
<a id="m1"></a>

## 1. 입력 양식
입력 양식은 사용자에게 정보를 입력 받을 때 사용됩니다. 기본적으로 `<form>`태그가 사용되나 \<form>태그 내부에 다양한 form 요소들을 위치시켜줘야 합니다. \<form>태그에서 사용할 수 있는 속성은 `method`와 `action`이 있습니다. `method`는 웹 서버와의 통신 방법을 지정하며 `get`과 `post` 방식이 존재합니다. `action`은 입력 받은 값을 저장할 페이지를 지정합니다. 

```html
<form action="#" method="get">
  <fieldset>
    <legend>Shipping Address</legend>
    <p>name: <input type="text" name="Name" /></p>
    <p>Address: <input type="text" name="Address" /></p>
    <p>City: <input type="text" name="City" /></p>
    <p>State: <input type="text" name="State" /></p>
    <p>zip: <input type="text" name="Zip" /></p>
  </fieldset>
</form>
```
<details>
<summary>실행 결과 보기</summary>
<p></p>
<div markdown="1">

<form action="#" method="get">
  <fieldset>
    <legend>Shipping Address</legend>
    <p>name: <input type="text" name="Name" /></p>
    <p>Address: <input type="text" name="Address" /></p>
    <p>City: <input type="text" name="City" /></p>
    <p>State: <input type="text" name="State" /></p>
    <p>zip: <input type="text" name="Zip" /></p>
  </fieldset>
</form>

</div>
</details>
<br>

<img alt="html_4-2-1" src="img/html_4-2-1.jpg" width="90%"><br>
<!--이미지 주소 : https://opentechlabs.blogspot.com/2014/10/difference-between-post-get.html -->

- `<form>`은 입력양식의 최상위 요소로 입력양식의 범위를 지정합니다. 
- `get`방식은 URL뒤에 파라미터를 붙여서 데이터를 전달합니다. 
- `post`방식은 HTTP Request 헤더에 파라미터를 붙여서 전송하며 get방식에 비해 보안이 더 뛰어납니다. 

### 동영상 강좌
- form 기본 : [http://bit.ly/2uHYadt](http://bit.ly/2uHYadt){:target="_blank"} `12:19`
- GET과 POST의차이 : [http://bit.ly/2A9oa6m](http://bit.ly/2A9oa6m){:target="_blank"} `10:03`


### 참고 자료
- form 태그 : [http://bit.ly/2uJ2cSO](http://bit.ly/2uJ2cSO){:target="_blank"}
- HTML Forms : [http://bit.ly/2uRY2XY](http://bit.ly/2uRY2XY){:target="_blank"}


### 퀴즈
#### 1) \<form>태그의 action에 들어가야 되는 내용은 무엇입니까?

<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

> 입력 받은 값을 저장할 페이지를 지정해줍니다.

</div>
</details>

#### 2) get방식과 post 방식의 차이에 대해 서술하시오.
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

- get방식은 URL 뒤에 파라미터를 붙여서 데이터를 전달하는 방식입니다. 
- post 방식은 HTTP Request 헤더에 파라미터를 붙여서 전송하여 보안에 좋습니다. 

</div>
</details>
<br>

---
<a id="m2"></a>

## 2. 입력 양식 태그
실제로 사용자가 양식을 입력하기 위한 태그는 `<input>`을 사용합니다. `type`속성으로 입력 양식의 종류를 나타내고 `name`속성으로 데이터 이름을, `value`속성으로 기본 값을 지정합니다. 

| Tag | Description | 
|:----:|-----| 
|\<form> | Defines a form for user input |
|\<input> | Defines am input field |
|\<textarea> | Defines a text-area (a multi-line text input control) |
|\<label> | Defines a label to a control |
|\<fieldset> | Defines a fieldset |
|\<legend> | Defines a caption for a fieldset |
|\<select> | Defines a selectable list (a drop-down box) |
|\<optgroup> | Defines an option group |
|\<option> | Defines an option in the drop-down box |
|\<button> | Defines a push button |
|\<isindex> | Deprecated. use \<input> instead |   


<!--이미지 주소 : https://poiemaweb.com/html5-tag-list-table-->


- `type`는 필수 속성이며 사용할 수 있는 값은 다음과 같습니다.
  - text - 텍스트 입력 필드
  - password - 비밀번호 입력필드
  - checkbox - 복수 선택 가능한 체크 박스
  - radio - 복수 선택 불가능한 라디오 버튼 생성
  - submit - 송신 버튼
  - reset - 리셋 버튼
  - button - 범용 버튼 
- `name`속성에 폼의 이름을 설정해줍니다. name속성 값은 변수처럼 사용됩니다. 
- `fieldset`은 연관성 있는 입력 양식들을 하나로 묶을 수 있게 도와주며 `legend`는 제목을 붙이는 역할을 합니다. 


### 동영상 강좌
- 폼 관련 태그들 : [http://bit.ly/2mAvZIN](http://bit.ly/2mAvZIN){:target="_blank"} `12:11`
- input type : [http://bit.ly/2JNfdPJ](http://bit.ly/2JNfdPJ){:target="_blank"} `10:11`
- input 태그 color 속성 : [http://bit.ly/2uXDg9s](http://bit.ly/2uXDg9s){:target="_blank"} `01:03`
- input 태그 date, month, week 속성 : [http://bit.ly/2JNfYs3](http://bit.ly/2JNfYs3){:target="_blank"} `02:24`
- fildset : [http://bit.ly/2mAVlWU](http://bit.ly/2mAVlWU){:target="_blank"} `06:52`
- 회원가입 폼 태그 예제 : [http://bit.ly/2uWddPS](http://bit.ly/2uWddPS){:target="_blank"} (~23:00) `23:00`


### 참고 자료
- button, form, input 태그 : [http://bit.ly/2uVyY2b](http://bit.ly/2uVyY2b){:target="_blank"}


### 퀴즈
#### 1) 텍스트 입력란을 만들어보세요.
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

```html
<form>
    <input type="text">
</form>
```

</div>
</details>

#### 2) 제출 버튼을 만들기 위해 사용하는 \<input>태그의 속성은 무엇입니까?
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

- submit

</div>

</details>

#### 3) 다음 중 \<input>태그의 속성이 아닌 것은 무엇입니까?
1. type
2. action
3. name
4. value
<details>
<summary>해답보기</summary>
<p></p>
<div markdown="1">

- [2번] - action은 \<form>의 속성입니다.
</div>
</details>


[din-badge]:https://img.shields.io/badge/dinfree-edu-orange.svg
[din-url]:https://github.com/dinfree
[basic-badge]:https://img.shields.io/badge/core-basic-green.svg