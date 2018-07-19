# [스터디] 파이썬 :: 3.1 자료구조
> 작성일: 2018.07.16 | 작성자: 유현지

자료형이란 프로그래밍을 할 때 쓰이는 숫자, 문자열 등 자료 형태로 사용하는 모든 것을 뜻한다. 프로그램의 기본이자 핵심 단위가 바로 자료형이다. 계산 프로그램을 만들려면 어떤 것을 계산할지부터 알아야 하고, 데이터베이스 프로그램을 만들려면 어떤 자료를 저장할지부터 알아야하는 것처럼 기본 중의 기본이라고 할 수 있다. 

### 목차
1. [숫자형](#m1)
2. [문자열](#m2)


---
<a id="m1"></a> 
## 1. 숫자형
숫자형(Number)이란 숫자 형태로 이루어진 자료형.

### 1) 숫자형의 종류

- **정수형**
```python
 a = 123   
 a = -173   
 a = 0 
```

- **실수형**
```python
 a = 1.2  
 a = -3.45  
```
```python
 # 컴퓨터식 지수 표현 방식
 a = 4.24E3  # 4.24 * 10³
 a = 4.24e-3  # 4.24 * 10－³
```

- **8진수**
```python
a = 0o177
a = 0O177
```

- **16진수**
```python
a = 0x8ff
a = 0xABC
```

### 2) 연산자
- **사칙연산**  
```
+ - * /
```

- `**`**연산자 (=제곱연산자)**
```python
a = 3
b = 4
a ** b = 81
```

- `%`**연산자 (=나머지연산자)**
```python
7 % 3 = 1
3 % 7 = 3
```

- `//`**연산자 (=나눗셈 후 소숫점아래 버림)**
```python
7 / 4 = 1.75
7 // 4 = 1
```

> **무조건 소수점을 버리는 것이 아니라,  
 나눗셈의 결과값보다 작은 정수 중 가장 큰 수 리턴**
```python
-7 / 4 = -1.75
-7 // 4 = -2
```

---
<a id="m2"></a> 
## 2. 문자형
문자열(String)이란 문자, 단어 등으로 구성된 문자들의 집합.

### 1) 문자열 표현방식

1. 큰따옴표로 둘러싸기 `"Hello"`
2. 작은따옴표로 둘러싸기 `'Hello'`
3. 큰따옴표 **3개**로 둘러싸기 `"""Hello"""`
4. 작은따옴표 **3개**로 둘러싸기 `'''Hello'''`

- **문자열에 큰따옴표(")와 작은따옴표(') 포함 방법**
```python
'"Python is very easy." he says.'

"Hyunji's favorite food is pasta. (o)
'Hyunji's favorite food is pasta. (x)
```
```python
# \(백슬래시) 이용
'Hyunji\'s favorite food is pasta.
"\"Python is very easy.\" he says." 
```

- **줄 바꾸기**
1. \n (이스케이프 코드) 삽입.
2. 연속된 따옴표 사용. 
``` python
>>> multiline = '''
... Life is too short
... You need python
... '''
```

### 2) 문자열 연산
- **'+'** **이용**
```python
>>> a = 'Hello'
>>> b = ' World'
>>> a + b
'Hello World'
```

- **'x'** **이용**
```python
>>> a = 'Hello '
>>> a * 3
'Hello Hello Hello '
```

### 3) 문자열 인덱싱과 슬라이싱
- **인덱싱**
```python
>>> a = 'Hello'
>>> a[0]
'H'
>>> a[-1]
'o'
>>> a[-0]
'H'
```

- **슬라이싱**  
a [시작번호:끝번호] (끝번호는 포함 X)
```python
>>> a = 'Hello World'
>>> a[0:6]
'Hello'
>>> a[6:]
'World'
>>> a[:3]
'Hel'
>>> a[:]
'Hello World'
>>> a[-2:]
'ld'
```
<a id="q1"></a>
#### ** Question01: "Hello" 문자열을 'Hallo'으로 바꾸려면? [정답보기](#sol1)

### 4) 포맷팅

```python
# 숫자와 문자열 포매팅
>>>"I have %d apples." %5
'I have 5 apples.'
>>>"I have %s apples." % "seven"
'I have seven apples.'

# 2개 이상 값 넣기
>>>"I have %d apples. So I eat %s apples." % (10, 'three')
'I have 10 apples. So I eat three apples.'
```

- **format() 이용한 포매팅**
```python
>>> number = 10
>>> day = "three"
>>> "I ate {0} apples. So I was sick for {1} days.".format(number, day)
'I ate 10 apples. So I was sick for three days.'

# 정렬
>>>"{0:<10}".format("hello")
'hello     '
>>>"{0:>10}".format("hello")
'     hello'
>>>"{0:^10}".format("hello")
'  hello   '

```

- **f 문자열 포매팅 (3.6이상 버전)**
```python
>>> name = '유현지'
>>> gender = '여자'
>>> f'나의 이름은 {name}이며, 성별은 {gender}입니다.'
'나의 이름은 유현지이며, 성별은 여자입니다.'

# 딕셔너리 사용가능
>>> d = {'name':'유현지', 'gender':'여자'}
>>> f'나의 이름은 {d["name"]}이며, 성별은 {d["gender"]}입니다.'
'나의 이름은 유현지이며, 성별은 여자입니다.'
```

### 5) 문자열 관련 함수

- 문자 개수: **count()**
- 위치: **find() & index()**
- 문자열 삽입: **join()**
- 소문자 ↔ 대문자: **upper() & lower()**
- 공백 지우기: **lstrip() & rstrip() & strip()**
- 문자열 바꾸기: **replace()**
- 문자열 나누기: **split()**

```python
>>> a = "Python is so fun"
>>> a.split()
['Python', 'is', 'so', 'fun']

# 특정 구분자로 나누기
>>> a = "Python*is*so*fun"
>>> a.split('*')
['Python', 'is', 'so', 'fun']
```

---
<a id="sol1"></a>
- **Answer01**  
[문제로 돌아가기](#q1)
```python
>>> a = 'Hello'
>>> a[1] = 'a'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object does not support item assignmen
```

**문자열, 튜플 등의 자료형은 요소값 변경 안됨.**
```python
>>> a = 'Hello'
>>> a[:1] + 'a' + a[2:]
'Hallo'
```
