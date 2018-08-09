# [스터디] 파이썬 :: 4. 함수와 모듈
> 작성일: 2018.7.17 , 작성자: 박병기

이번 장에서는 파이썬의 함수와 모듈에 대해서 알아보도록 하겠습니다.

### 목차
1. [함수란 무엇인가?](#m1)
2. [함수의 구조](#m2)
3. [함수의 형태](#m3)
4. [lambda](#m4)
5. [연습문제](#m5)

---

<a id="m1"></a> 
## 1. 함수란 무엇인가?
- **함수**란 **입력값**을 받아 어떠한 일을 수행한 후 **결과값**을 나타내주는 것을 나타냅니다.

- 프로그래밍 코드를 작성하다보면 **반복되는 코드**가 나오게되는데, 이러한 코드를 함수로 만들어 간편하게 사용할 수 도 있습니다.

<a id="m2"></a>
## 2. 함수의 구조
파이썬의 함수의 구조는 아래와 같다.
```python
def 함수명(매개변수):
  <수행할 문장1>
  <수행할 문장2>
  ...
```
**def**는 함수를 만들 때 사용하는 예약어 이며, 함수명은 임의로 만들 수 있다. 함수명 뒤 괄호 안의 **매개변수**는 이 함수에 입력으로 전달되는 값을 받는 변수이다.

다음 예를 보며 자세히 알아보자.
```python
def sum(a, b):
  return a + b
```
위 함수는 다음과 같이 풀이된다.
<table>
<td border: 1px>
이 <b>함수의 이름(함수명)</b>은 <b>sum</b>이고 입력으로 <B>2개의 값</b>을 받으며 결과값은 <u>2개의 입력값을 더한 값</u>이다.
</table>

이제 직접 sum 함수를 사용해 보자.

```python
>>> def sum(a,b):
...   return a + b
... 
... a = 1
... b = 2
>>> print(sum(a,b))

4
```
매개변수 a에 1, b에 2를 대입한 다음 **print(sum(a,b))** 으로 값을 출력할 수 있다.

#### 매개변수
- 함수에 입력으로 전달된 값을 받는 변수를 의미
#### 인수
- 함수를 호출할 때 전달하는 입력값을 의미
```python
def sum(a, b): # a, b는 매개변수
  return a + b

print(sum(1,3)) # 1, 3 은 인수
```

<a id="m3"></a>
## 3. 함수의 형태
함수의 형태는 입력값과 결과값의 존재 유무에 따라 4가지 유형으로 나뉜다.

### 일반적인 함수
**입력값**이 있고 **결과값**이 있는 함수가 <u>**일반적인 함수**</u>이다. 우리가 프로그래밍을 할 때 만들 함수는 대부분 이러한 형태이다.
```python
def 함수이름(매개변수):
  <수행할 문장>
  ...
  return 결과값
```

### 입력값이 없는 함수
일반적인 함수와 다르게 함수명 뒤의 **괄호안이 비어져 있는 함수**이다.
```python
def say():
  return 'Hi'
```
사용하는 방법은 **매개변수 입력 없이** 함수를 사용하면 된다.
```python
>>> print(say())
Hi
```

### 결과값이 없는 함수
결과를 반환하는 **return**이 없는 함수이다.
다른 프로그래밍 언어의 **void 함수**와 비슷하다.
```python
def NoReturn(a):
  print("입력받은 값은 %d 입니다." % a)
```
위의 함수를 선언하고 실행해 보자.
```python
>>> b = NoReturn(2)
>>> print(b)

입력받은 값은 2 입니다.
None
```
**print**의 경우 함수의 **return 값을 출력**해 주는건데, NoReturn함수의 경우 return값이 없어서 **None** 값이 출력되었다.

### 입력값도 결과값도 없는 함수
입력과 결과값이 없는 함수이다.
```python
def say():
  print('Hi')
```
이 함수를 실행하면 다음과 같다.
```python
>>> say()

Hi
```
<br></br>
> ### 입력값이 여러개를 받는 함수
함수를 만들다 보면 여러개의 입력값을 받야아 하는 경우가 생긴다. 그럴경우 아래와 같이 함수를 만들면 된다.
```python
def sum_many(*args): # *을 사용하여 배열을 받는다
  sum = 0
  for i in args:
    sum = sum + i
  return sum
```
위 함수는 입력된 수들의 핪을 반환하는 함수이다. 사용예는 아래와 같다.
```python
>>> result = sum_many(1,2,3,4)
>>> print(result)

10

>>> result = sum_many(1,2,3,4,5,6,7,8,9,10)
>>> print(resutl)

55
```

<a id="m4"></a>
## 4. lambda
**lambda**는 함수를 생성할 때 사용하는 예약어로, **def**와 동일한 역할을 한다.
<u>**def**를 사용해야 할 정도로 복잡하지 않거나 **def**를 사용할 수 없는 곳</u>에 주로 쓰이고, **함수**를 **한줄로 간결하게** 만들 때도 사용한다.

<table>
<td border: 1px>
<b>lambda</b> 매개변수1, 매개변수2, ...: 매개변수를 이용한 표현식
</table>

간단한 **lambda** 를 만들어보자.

```python
>>> sum = lambda a, b: a+b
>>> sum(3,4)

7
```

#### def를 이용할 수 없는 경우
```python
>>> myList = [lambda a,b: a+b, lambda a,b: a*b]
>>> myList[0](5,6)

11

>>> myList[1](5,6)

30
```

<a id="m4"></a>
## 5. 연습문제
- 숫자들로 이루어진 리스트를 입력받아 5보다 큰 수만 필터링하여 리턴해 주는 함수를 작성하라.
```python
myfunc([2,3,4,5,6,7,8])

[6,7,8]
```

<details>
  <summary>정답보기</summary>
  
  ```python
  >>> def myfunc(numbers):
  ...     result = []
  ...     for number in numbers:
  ...        if number > 5:
  ...            result.append(number)
  ...     return result

  >>> myfunc([2,3,4,5,6,7,8])

  [6,7,8]
  ```
</details>
<Br>

- 위에서 만든 함수를 lambda로 변경해 보시오.

<details>
  <summary>정답보기</summary>
  
  ```python
>>> myfunc = lambda numbers:[number for number in numbers if number > 5]
>>> myfunc([2,3,4,5,6,7,8])

[6,7,8]
```
</details>
