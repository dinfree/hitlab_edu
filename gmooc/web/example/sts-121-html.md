
# [STS-121 실습] 웹 프론트엔드 개발 기초::HTML

[![Dinfree][din-badge]][din-url]
[![Subject][html-badge]][din-url]
[![Subject][css-badge]][din-url]
[![Subject][js-badge]][din-url]

## 시작하기 전에
이 페이지는 프론트엔드 웹 프로그래밍의 기본이 되는 [STS-121] HTML 기초 강좌의 예제 학습 페이지 입니다. 동영상이 포함된 강좌는 [STS-121][] 에서 보실수 있습니다. 이곳에서는 각 챕터별 예제들과 간단한 프로젝트형식의 종합예제를 정리해서 제공하고 있습니다. 각각의 예제는 github 리파지토리에서 받아가실수 있으며 첨부된 설명에 따라 학습을 진행하면 됩니다. 실습을 위한 모든 환경설정은 `공통기초->[STS-103]개발도구` 에서 다루었습니다. 따라서 해당학습을 진행하지 않았다면 반드시 먼저 살펴보고 실습을 진행하기 바랍니다.

### 목차
1. 월드와이드웹과 HTML
2. HTML 기본 작성법과 구조
3. 제목, 문단, 형식
4. 목록, 하이퍼링크
5. 이미지, 테이블
6. 입력양식

---

## 1. 월드와이드웹과 HTML
### 예제 1-1) 웹페이지 요청하기와 소스 보기
본 예제에서는 url 을 이용해 원하는 웹페이지를 직접 요청하는 과정을 통해 웹의 기본적인 동작구조인 request -> response 개념을 살펴보게 됩니다. 또한 웹브라우저 화면에 보이는 콘텐츠의 소스 보기를 통해 서버에서 전달된 원본 콘텐츠는 텍스트형식으로 된 html 구조라는 것을 확인해 봅니다.

#### step-1> 웹브라우저 실행하기
```
크롬 웹브라우저를 실행 합니다. 인터넷 익스플로러/엣지 브라우저도 상관없으나 모든 설명은 크롬을 기준으로 합니다.
```
#### step-2> url 입력하기
```
- 웹프라우저 상단의 URL 창에 다음의 주소중 하나를 입력하고 엔터를 칩니다.
- http://www.naver.com
- http://www.apple.com
```

<img alt="1-2결과" src="img/1-2.gif" width="80%">


#### step-3> 소스 보기
```
- 웹브라우저 화면에서 오른쪽 마우스를 눌러 페이지 소스보기를 선택합니다.
- 보이는 텍스트들이 현재 화면을 구성하고 있는 html 소소 입니다.
```

<img alt="1-1결과" src="img/1-1.gif" width="80%">


## 2. HTML 기본 작성법과 구조
### 예제 2-1) HTML 기본문서 작성과 실행하기
본 예제에서는 HTML 파일을 생성하고 HTML 문서의 기본 구조를 작성해 봅니다. 앞으로 진행되는 모든 예제는 별도의 폴더를 생성해 관리할 수 있도로 합니다. github repository 에는 `example/sts-121-html`, `example/sts-122-css`, `example/sts-123-js` 로 구분되어 있습니다. Visual Studio Code 에서는 example 폴더를 오픈해서 사용하면 됩니다.

#### step-1> Visual Studio Code 실행
```
- HTML 문서 작성을 위해 Visual Studio Code 를 실행 합니다. 만일 설치하지 않았다면 공통기초->[STS-103]개발도구 를 참고하기 바랍니다.
- Visual Studio Code 는 공통기초->[STS-103]개발도구 에서 설명한것 처럼 영어 언어 설정으로 사용합니다.
- 미리 생성해둔 예제폴더를 Open Folder 버튼을 이용해 오픈한 다음 New file 버튼을 클릭해 새로운 파일을 생성하고 2-1.html 이라 이름을 입력합니다.
```

#### step-2> html 소스코드 작성(2-1.html)
다음과 같이 html 코드를 작성합니다. 들여쓰기는 프로그램 소스 작성시 가독성 향상을 위해 중요한 요소 이므로 탭 키를 이용해 반드시 들여쓰기를 하 수 있도록 합니다.
```html
<!doctype html>
<html>
    <head>
        <title>2-1.html</title>
    </head>
    <body>
        <H2>2-1.html</H2>
        <HR>
        example 2-1.html
    </body>
</html>
```

#### step-3> 실행 및 결과 확인
파일을 선택후 오른쪽 마우스를 눌러 open in browser 메뉴를 선택해 브라우저에서 실행결과를 확인 합니다. 메뉴가 보이지 않을 경우 `공통기초->[STS-103]개발도구` 를 다시 참조해 해당 플러그인을 설치후 진행하기 바랍니다.

<img alt="2-1결과" src="img/2-1.gif" width="80%">


## 3. 제목, 문단, 형식
### 예제 3-1) 제목과 문단으로 웹 문서 작성
본 예제에서는 `<h1>`부터 `<h6>`까지 있는 다양한 h태그들과 문단을 나타내는 `<p>`태그 및 개행을 하는 `<br>`태그를 이용하여 웹 문서를 작성해봅니다.




#### step-1> html 소스코드 작성 (3-1.html)
New file 버튼을 클릭해 새로운 파일을 생성해 3-1.html 이라 이름을 입력하고 다음과 같이 html 코드를 작성합니다. 본문 내의 연속된 공백 및 줄바꿈을 HTML에서 어떻게 처리하는지 확인하기 위해 아래와 같이 코드를 작성합니다.


```html
<!doctype html>
<html> 
    <head>
        <title>3-1.html</title>
    </head>
    <body>
        <h1>3-1.html</h1>
        <h3>html example</h2>
        
        <p>hello world</p>
        <p>hello

                     world
        </p>
        <p>hello<br>world</p>
        
    </body>
</html>
```
#### step-2> 실행 및 결과 확인
파일을 선택후 오른쪽 마우스를 눌러 open in browser 메뉴를 선택해 브라우저에서 실행결과를 확인 합니다.<br>아래 결과와 같이 HTML에서는 본문 내에서 연속된 공백이나 줄 바꿈은 하나의 공백으로 처리합니다.

<img alt="3-1결과" src="img/3-1.png" width="80%">


### 예제 3-2) 텍스트 관련 태그들
본 예제에서는 텍스트 관련 태그들에는 무엇이 있는지 살펴보고, 각 태그들에 의해 텍스트가 어떻게 변하는지를 살펴봅니다.

#### step-1> html 소스코드 작성 (3-2.html)
New file 버튼을 클릭해 새로운 파일을 생성해 3-2.html 이라 이름을 입력하고 다음과 같이 html 코드를 작성합니다.


```html
<!doctype html>
<html> 
    <head>
        <title>3-2.html</title>
    </head>
    <body>
        <b>bold text</b><br>
        <strong>strong text</strong><br>
        <i>italic text</i><br>
        <em>emphasized text</em><br>
        <mark>mark text</mark><br>
        <small>small text</small><br>
        <del>deleted text</del><br>
        <ins>inserted text</ins><br>
        <sub>subscript text</sub><br>
        <sup>superscript text</sup>
    </body>
</html>
```
#### step-2> 실행 및 결과 확인
파일을 선택후 오른쪽 마우스를 눌러 open in browser 메뉴를 선택해 브라우저에서 실행결과를 확인 합니다.

<img alt="3-2결과" src="img/3-2.png" width="80%">

## 4. 목록, 하이퍼링크
### 예제 4-1) 목록 만들기
본 예제에서는 순서가 있는 목록과 순서가 없는 목록, 두 가지를 작성해봅니다. 또한 `type`속성을 이용하면 리스트가 어떻게 바뀌는지 확인해봅니다. 



#### step-1> html 소스코드 작성 (4-1.html)
예제 4-1은 여러가지 음료를 리스트를 통해 보여주는 코드입니다. 4-1.html 파일을 생성하고 순서 있는 목록과 순서 없는 목록, 두 가지로 표현해보기 위해 다음과 같이 코드를 작성합니다.

```html
<!doctype html>
<html> 
    <head>
        <title>4-1.html</title>
    </head>
    <body>
        <h2>Unordered List</h2>
        <ul>
        <li>Coffee</li>
        <li>Tea</li>
        <li>Milk</li>
        </ul>  

        <h2>Ordered List</h2>
        <ol>
        <li>Coffee</li>
        <li>Tea</li>
        <li>Milk</li>
        </ol> 
    </body>
</html>
```
#### step-2> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 아래와 같이 `<ul>`은 순서가 없는 리스트가 만들어지고, `<ol>`은 순서가 있는 리스트가 만들어지는 것을 확인할 수 있습니다.

<img alt="4-1-1결과" src="img/4-1.png" width="80%">

#### step-3> type 속성 추가
순서 있는 목록의 순서 표기법을 변경해보기 위해, 위에서 작성한 4-1.html의 코드를 아래처럼 수정합니다.

```html
<h2>Ordered List</h2>
<ol type="A">
<li>Coffee</li>
<li>Tea</li>
<li>Milk</li>
</ol> 
```

#### step-4> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 아래 그림처럼 1,2,3이였던 순서가 A,B,C로 바뀐 것을 확인 할 수 있습니다. 

<img alt="4-1-3결과" src="img/4-2.png" width="80%">


### 예제 4-2) 하이퍼링크 사용하기
본 예제에서는 `<a>`태그를 통해 하이퍼링크를 사용해봅니다. `<a>`태그의 기본적인 사용법을 살표보고 `target`속성에 대해 알아봅니다.



#### step-1> html 소스코드 작성 (4-2.html)
예제 4-2는 가천대학교로 연결하는 하이퍼링크를 만들어보는 코드입니다. 4-2.html 파일을 생성하고 하이퍼링크를 만들기 위해 다음과 같이 html 코드를 작성합니다.

```html
<!doctype html>
<html> 
    <head>
        <title>4-2.html</title>
    </head>
    <body>
        <a href="http://www.gachon.ac.kr">Gachon</a>
    </body>
</html>
```
#### step-2> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="4-2결과" src="img/4-2.gif" width="80%">

#### step-3> target 속성 추가
target 속성을 추가하여 링크가 열리는 위치를 변경하고자 합니다. 새로운 탭에서 열리게 하기위해, 위에서 작성한 4-2.html의 코드를 아래처럼 수정합니다.

```html
<a href="http://www.gachon.ac.kr" target="_blank">Gachon</a>
```

#### step-4> 실행 및 결과 확인
파일을 선택후 오른쪽 마우스를 눌러 open in browser 메뉴를 선택해 브라우저에서 실행결과를 확인 합니다. `target`속성은 연결된 문서를 열 위치를 지정합니다. `_blank`로 지정을 해둘 경우, 새로운 탭에서 열리게 됩니다..

<img alt="4-3결과" src="img/4-3.gif" width="80%">

### 예제 4-3) 책갈피
본 예제에서는 `<a>`태그를 통해 본문 내에서 특정한 위치로 이동하는 책갈피 기능을 사용해봅니다.



#### step-1> html 소스코드 작성 (4-3.html)
예제 4-3은 커피숍 메뉴판에서 원하는 항목으로 이동시켜주는 책갈피 기능을 만들어보는 코드입니다. 4-3.html 파일을 생성하고 `<ul>`을 통해 메뉴판을 만들고 `<a>`태그를 이용하여 책갈피 기능을 만들기 위해 다음과 같이 html 코드를 작성합니다.

```html
<!doctype html>
<html> 
    <head>
        <title>4-3.html</title>
    </head>
    <body>
        <h1>Menu</h1>
        <a href="#index1">Coffee</a><br>
        <a href="#index2">Cake</a><br>
        <a href="#index3">Juice</a><br>

        
        <h2 id="index1">Menu01::Coffee</h2>
        <ul>
            <li>Americano</li>
            <li>Cappuccino</li>
            <li>Cafe latte</li>
        </ul>
        
        <h2 id="index2">Menu02::Cake</h2>
        <ul>
            <li>Carrot cake</li>
            <li>black tea cake</li>
            <li>Strawberry shortcake</li>
        </ul>
        
        <h2 id="index3">Menu03::Juice</h2>
        <ul>
            <li>orange</li>
            <li>grape</li>
            <li>watermelon</li>
        </ul>

    </body>
</html>
```
#### step-2> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 화면이 클 경우, 특정 위치로 이동하는 것이 보이지 않을 수 있습니다. 창을 작게 줄여서 확인하도록 합니다.

<img alt="4-2결과" src="img/4-4.gif" width="80%">



## 5. 이미지, 테이블
### 예제 5-1) 이미지 추가 및 속성
본 예제에서는 `<img>`태그를 통해 이미지를 삽입합니다. 인터넷에 있는 이미지를 이미지 주소를 통해 본문에 추가해보고 크기를 조정해봅니다. 또한 alt 속성을 직접 사용해보고 어떻게 나타나는지 확인합니다.


#### step-1> 이미지 준비
웹 사이트에서 원하는 이미지를 찾습니다. 원하는 이미지를 좌클릭하고 이미지 주소 복사를 클릭해 이미지의 주소를 복사합니다.

<img alt="5-1결과" src="img/5-1.gif" width="80%">


#### step-2> html 소스코드 작성 (5-1.html)
5-1.html 파일을 생성하고 이미지를 본문에 추가하기 위해 다음과 같이 코드를 작성합니다. `img`태그의 `src`속성에는 복사해두었던 이미지의 주소를 넣어줍니다.


```html
<!doctype html>
<html> 
    <head>
        <title>5-1.html</title>
    </head>
    <body>
        <img src="https://t1.daumcdn.net/cfile/tistory/17441F41509D287F03">
    </body>
</html>
```
#### step-3> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다.

<img alt="3-1결과" src="img/5-2.png" width="80%">

#### step-4> 이미지 크기 조절
이미지의 크기를 임의적으로 조절해봅니다. 높이와 너비의 조절을 위해 위에서 작성한 4-2.html의 코드를 아래처럼 수정합니다.

```html
<img src="https://t1.daumcdn.net/cfile/tistory/17441F41509D287F03" width="100px" height="100px">
```

#### step-5> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 아래와 같이 이미지의 크기가 줄어든 것을 확인 할 수 있습니다.

<img alt="3-1결과" src="img/5-3.png" width="80%">

#### step-6> alt 속성 적용
위에서 작성한 4-2.html의 코드를 아래처럼 수정합니다. `alt`속성의 적용 여부를 확인하기 위해 이미지의 주소를 일부로 틀리게 설정해봅시다.

```html
<img src="https://XXX" alt="가천대 로고">
```

#### step-7> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 이미지가 오류 등으로 인해 보여지지 않을 경우, `alt`속성의 값이 이미지 대신 표시됩니다.

<img alt="3-1결과" src="img/5-4.png" width="80%">

### 예제 5-2) 로컬 이미지 추가
본 예제에서는 컴퓨터에 저장되어있는 로컬이미지를 본문에 추가해봅니다.

#### step-1> img 폴더 생성하기
```
예제 폴더 안에 이름이 img 인 폴더를 하나 생성합니다.
```
#### step-2> img 폴더안에 이미지 저장하기
```
원하는 이미지를 img 폴더 안에 저장합니다.
```
#### step-3> html 소스코드 작성 (5-2.html)
5-2.html 파일을 생성하고 이미지를 본문에 추가하기 위해 다음과 같이 코드를 작성합니다. `img`태그의 `src`속성에는 저장한 이미지의 상대 경로를 입력합니다. 아래 코드의 경로는 현재 작업중인 5-2.html 파일을 기준으로 img폴더 안에 있는 sample.png 파일을 의미합니다.


```html
<!doctype html>
<html> 
    <head>
        <title>5-2.html</title>
    </head>
    <body>
        <img src="img/sample.png">
    </body>
</html>
```
#### step-4> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다.

<img alt="3-1결과" src="img/5-5.png" width="80%">


### 예제 5-3) 테이블 만들기
본 예제에서는 `<table>`태그 및 `<td>`, `<tr>`, `<th>` 태그들을 이용하여 테이블을 만들어봅니다.

#### step-1> html 소스코드 작성 (5-3.html)
예제 5-3은 인적사항이 정리되어 있는 테이블을 작성하는 코드입니다. 5-3.html 파일을 생성하고 `<table>`을 통해 테이블을 만들고 `<tr>`태그를 이용하여 테이블의 행을, `<td>`태그를 이용하여 각 행의 요소를 생성하기 위해 다음과 같이 html 코드를 작성합니다.

```html
<!doctype html>
<html>
    <head>
        <title>5-3.html</title>
    </head>
    <body>
        <table>
            <tr>
                <th>no.</th>
                <th>name</th>
                <th>email</th>
                <th>tel</th>
            </tr>
            <tr>
                <td>1</td>
                <td>James Kang</td>
                <td>james@gachon.ac.kr</td>
                <td>010-1234-1234</td>
            </tr>
            <tr>
                <td>2</td>
                <td>Justin Born</td>
                <td>justin@google.com</td>
                <td>010-9876-1234</td>
            </tr>
            <tr>
                <td>3</td>
                <td>Mariata Kumba</td>
                <td>kumba@amazon.com</td>
                <td>010-2222-3333</td>
            </tr>
            <tr>
                <td>4</td>
                <td>Mola Landa</td>
                <td>mola@naver.com</td>
                <td>010-4444-5555</td>
            </tr>
        </table>
    </body>
</html>
```

#### step-2> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="5-3결과" src="img/5-6.png" width="80%">

#### step-3> 테두리 만들기
테이블을 더 보기 좋게 하기 위해서 테두리를 추가해봅시다. 테두리를 만들기위해 작성한 5-3.html의 코드를 아래처럼 수정합니다.

```html
<table border="1">
```

#### step-4> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="5-3결과" src="img/5-7.png" width="80%">

#### step-5> 테이블 병합하기
1번의 email과 tel을 하나의 칸으로, no.의 2번과 3번을 하나의 칸으로 합쳐보려고 합니다. 
작성한 5-3.html의 코드를 아래처럼 수정합니다.

```html
<tr>
    <td>1</td>
    <td>James Kang</td>
    <td colspan="2">james@gachon.ac.kr,010-1234-1234</td>
</tr>
<tr>
    <td rowspan="2">2</td>
    <td>Justin Born</td>
    <td>justin@google.com</td>
    <td>010-9876-1234</td>
</tr>
<tr>
    <td>Mariata Kumba</td>
    <td>kumba@amazon.com</td>
    <td>010-2222-3333</td>
</tr>        
```

#### step-6> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="5-3결과" src="img/5-8.png" width="80%">

### 예제 5-4) 테이블 병합 연습
본 예제에서는 `colspan`과 `rowspan`을 사용해 테이블을 병합하는 것을 중점적으로 연습해봅니다.

#### step-1> html 소스코드 작성 (5-4.html)
예제 5-4는 테이블을 병합하는 코드입니다. 5-4.html 파일을 생성하고 병합을 하기 전 기본적인 테이블 구조를 잡아주기 위해 다음과 같이 html 코드를 작성합니다.

```html
<!doctype html>
<html>
    <head>
        <title>5-4.html</title>
    </head>
    <body>
        <table border=1 width=300 height=300>
            <tr>
                <td>1</td>
                <td>2</td>
                <td>3</td>
                <td>4</td>
            </tr>
            <tr>
                <td>5</td>
                <td>6</td>
                <td>7</td>
                <td>8</td>
            </tr>
            <tr>
                <td>9</td>
                <td>10</td>
                <td>11</td>
                <td>12</td>
            </tr>
        </table>
    </body>
</html>
```


#### step-2> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="5-4결과" src="img/5-9.png" width="80%">


#### step-3> 행 병합
위 테이블의 3번과 7번을 하나의 칸으로 합치고 그 안에 3이라 적어넣고, 8번과 12번을 합치고 그 안에 6을 적어 넣어봅시다. 
작성한 5-3.html의 코드를 아래처럼 수정합니다.

```html
<tr>
    <td>1</td>
    <td>2</td>
    <td rowspan=2>3</td>
    <td>4</td>
</tr>
<tr>
    <td>5</td>
    <td>5</td>
    <td rowspan=2>6</td>
</tr>
<tr>
    <td>7</td>
    <td>8</td>
    <td>9</td>
</tr>
```

#### step-4> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="5-4결과" src="img/5-10.png" width="80%">

#### step-5> 열 병합
위 테이블의 2개의 5번을 하나의 칸으로 합쳐 그 안에 5라 적어넣고, 8번과 9번을 합쳐 그 안에 8이라 적어넣어봅니다.
작성한 5-3.html의 코드를 아래처럼 수정합니다.

```html
<tr>
    <td colspan=2>5</td>
    <td rowspan=2>6</td>
</tr>
<tr>
    <td>7</td>
    <td colspan=2>8</td>
</tr>
```

#### step-6> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="5-4결과" src="img/5-11.png" width="80%">


## 6. 입력양식
### 예제 6-1) 검색창 만들기
본 예제에서는 `form`을 이용하여 text입력창과 제출버튼으로 이루어진 검색창을 만들어봅니다.

#### step-1> html 소스코드 작성 (6-1.html)
예제 6-1은 검색창을 만드는 코드입니다. 6-1.html 파일을 생성하고 `form`태그 안에 `<input type="text">`로 텍스트 입력란을, `<input type="submit">`로 전송 버튼을 만들기위해 다음과 같이 html 코드를 작성합니다.

```html
<!doctype html>
<html>
    <head>
        <title>6-1.html</title>
    </head>
    <body>
        <form action=""> 
        search: <input type="text">
        <input type="submit" value="search">
        </form>
    </body>
</html>
```


#### step-2> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="6-1결과" src="img/6-1.png" width="80%">


### 예제 6-2) 신청서 만들기
본 예제에서는 테이블 및 입력양식을 이용하여 신청서를 만들어봅니다.

#### step-1> html 소스코드 작성 (6-2.html)
예제 6-2은 신청서를 만드는 코드입니다. 6-2.html 파일을 생성하고 테이블로 레이아웃을 잡고 다양한 input 태그를 이용하여 신청서를 만들기위해 다음과 같이 html 코드를 작성합니다.

```html
<!doctype html>
<html>
    <head>
        <title>6-2.html</title>
    </head>
    <body>
        <table border=0>
            <tr>
                <td>
                    <form>
                    First name:<br>  
                    <input type="text" name="fname"><br>  
                    Last name:<br>  
                    <input type="text" name="lname"><br>
                    Email:<br>
                    <input type="email" name="email"><br>
                    Gender: <input type="radio" name="gender">Male, <input type="radio" name="gender">Female <br>
                    Favorite : <input type="checkbox" name="fav">HTML, <input type="checkbox" name="fav">Java, <input type="checkbox" name="fav">PHP<br>
                    University : <select>
                        <option>Gachon University</option>
                        <option>Korea University</option>
                        <option>Yeonsei University</option>
                        <option>Seoul University</option>
                    </select>
                    <br>
                    Color: <input type="color"> <br>
                    Date: <input type="date"> <br>
                    <br><br>
                    <input type="submit" value="Registration">
                    </form>
                </td>
            </tr>
        </table>
    </body>
</html>
```


#### step-2> 실행 및 결과 확인
브라우저에서 실행결과를 확인 합니다. 

<img alt="6-2결과" src="img/6-2.png" width="80%">


[din-badge]:https://img.shields.io/badge/dinfree-edu-orange.svg
[din-url]:https://github.com/dinfree
[css-badge]:https://img.shields.io/badge/frontend-css-ff69b4.svg
[html-badge]:https://img.shields.io/badge/frontend-html-brightgreen.svg
[js-badge]:https://img.shields.io/badge/frontend-javascript-red.svg
