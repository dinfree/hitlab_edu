# [스터디] 파이썬 :: 8. 클래스
> 작성일: 2018.07.27 , 작성자: 오정훈

이번 장에서는 파이썬의 클래스에 대해 살펴봅니다.

### 목차
1. [클래스](#m1)
2. [클래스 멤버](#m2)
3. [객체 생성과 사용](#m1)
4. [클래스 상속과 다형성](#m4)
5. [예제:날짜 클래스 만들기](#m5)
---

<a id="m1"></a> 
## 1. 클래스
파이썬은 객체지향 프로그래밍을 기본적으로 지원합니다. 클래스의 정의 방법은 다음과 같습니다.
```python
class 클래스이름:
    def 메서드(self):
      코드
```

<a id="m2"></a> 
## 2. 클래스 멤버
클래스는 메서드, 속성, 클래스 변수 등으로 구성됩니다. 파이썬에서는 필드와 메서드 모두 그 객체의 attribute라고 합니다. 다른 OOP 언어와 달리 **파이썬은 새로운 attribute를 동적으로 추가할 수 있습니다.**

### 클래스 구성
```python
class Rectangle:
    count = 0  # 클래스 변수
 
    # 초기자(initializer)
    def __init__(self, width, height):
        # self.* : 인스턴스변수
        self.width = width
        self.height = height
        Rectangle.count += 1
 
    # 메서드
    def calcArea(self):
        area = self.width * self.height
        return area
```
#### 메서드
메서드는 클래스의 행위를 표현합니다. 메서드는 인스턴스 메서드, 정적 메서드, 클래스 메서드가 있습니다. 가장 흔히 쓰이는 인스턴스 메서드는 인스턴스 변수에 엑세스할 수 있도록 메서드의 첫번째 파라미터에 항상 자신을 의미하는 'self'라는 파라미터를 갖습니다. (self를 사용하기로 되어있지만 다른 이름을 사용해도 됩니다.)

#### 클래스 변수
클래스 정의에서 메서드 밖에 존재하는 변수를 클래스 변수(class variable)라 하는데, 이는 해당 클래스를 사용하는 모두에게 공용으로 사용되는 변수입니다. 클래스 변수는 클래스 내외부에서 "클래스명.변수명" 으로 엑세스 할 수 있다. 위의 예제에서 count는 클래스변수로서 "Rectangle.count"와 같이 엑세스할 수 있습니다. (객체를 통해 r.count와 같은 것을 의미하기 때문에 혼동이 있어 주로 클래스 변수를 엑세스 할 때는 '클래스명.변수명'을 사용합니다.)

#### 인스턴스 변수
하나의 클래스로부터 여러 객체 인스턴스를 생성해서 사용할 수 있습니다. 클래스 변수가 하나의 클래스에 하나만 존재하는 반면, 인스턴스 변수는 각 객체 인스턴스마다 별도로 존재합니다. 클래스 정의에서 메서드 안에서 사용되면서 "self.변수명"처럼 사용되는 변수를 인스턴스 변수(instance variable)라 하는데, 이는 각 객체별로 서로 다른 값을 갖는 변수입니다. 인스턴스 변수는 클래스 내부에서는 self.width 과 같이 "self." 을 사용하여 엑세스하고, 클래스 밖에서는 "객체변수.인스턴스변수"와 같이 엑세스 합니다.

Python은 다른 언어에서 흔히 사용하는 public, protected, private 등의 접근 제한자 (Access Modifier)를 갖지 않습니다. Python 클래스는 기본적으로 모든 멤버가 public이라고 할 수 있습니다. Python 코딩 관례(Convention)상 내부적으로만 사용하는 변수 혹은 메서드는 그 이름 앞에 하나의 밑줄(_) 을 붙입니다. 하지만 이는 코딩 관례에 따른 것일 뿐 실제 밑줄 하나를 사용한 멤버도 public 이므로 필요하면 외부에서 엑세스할 수 있습니다. 
만약 특정 변수명이나 메서드를 private으로 만들어야 한다면 두개의 밑줄(__)을 이름 앞에 붙이면 됩니다.
```python
def __init__(self, width, height):
    self.width = width
    self.height = height
 
    # private 변수 __area
    self.__area = width * height
 
# private 메서드
def __internalRun(self):
    pass
```
#### initializer(초기자)
클래스로부터 새 객체를 생성할 때마다 실행되는 특별한 메서드로 __init__() 이라는 메서드가 있는데, 이를 흔히 클래스 Initializer 라 부릅니다 (주: 파이썬에서 두개의 밑줄 (__) 시작하고 두개의 밑줄로 끝나는 레이블은 보통 특별한 의미를 갖습니다). Initializer는 클래스로부터 객체를 만들 때, 인스턴스 변수를 초기화하거나 객체의 초기상태를 만들기 위한 문장들을 실행하는 곳입니다.

#### 정적 메서드와 클래스 메서드
인스턴스 메서드가 객체의 인스턴스 필드를 self를 통해 엑세스할 수 있는 반면, **정적 메서드는 이러한 self 파라미터를 갖지 않고 인스턴스 변수에 엑세스할 수 없다.** 따라서, 정적 메서드는 보통 객체 필드와 독립적이지만 로직상 클래스내에 포함되는 메서드에 사용된다. 정적 메서드는 메서드 앞에 **@staticmethod** 라는 Decorator를 표시하여 해당 메서드가 정적 메서드임을 표시한다.

클래스 메서드는 메서드 앞에 @classmethod 라는 Decorator를 표시하여 해당 메서드가 클래스 메서드임을 표시한다. 클래스 메서드는 정적 메서드와 비슷한데, 객체 인스턴스를 의미하는 self 대신 cls 라는 클래스를 의미하는 파라미터를 전달받는다. 정적 메서드는 이러한 cls 파라미터를 전달받지 않는다. 클래스 메서드는 이렇게 전달받은 cls 파라미터를 통해 클래스 변수 등을 엑세스할 수 있다.

일반적으로 인스턴스 데이타를 엑세스 할 필요가 없는 경우 클래스 메서드나 정적 메서드를 사용하는데, 이때 보통 클래스 변수를 엑세스할 필요가 있을 때는 클래스 메서드를, 이를 엑세스할 필요가 없을 때는 정적 메서드를 사용한다.

아래 예제에서 isSquare() 메서드는 정적 메서드로서 cls 파라미터를 전달받지 않고 메서드 내에서 클래스 변수를 사용하지 않고 있다. 반면, printCount() 메서드는 클래스 메서드로서 cls 파라미터를 전달받고 메서드 내에서 클래스 변수 count 를 사용하고 있다.
```python
class Rectangle:
    count = 0  # 클래스 변수
 
    def __init__(self, width, height):
        self.width = width
        self.height = height
        Rectangle.count += 1
 
    # 인스턴스 메서드
    def calcArea(self):
        area = self.width * self.height
        return area
 
    # 정적 메서드
    @staticmethod
    def isSquare(rectWidth, rectHeight):
        return rectWidth == rectHeight   
 
    # 클래스 메서드
    @classmethod
    def printCount(cls):
        print(cls.count)   
```
<a id="m1"></a> 
## 3. 객체의 생성과 사용
클래스를 사용하기 위해서는 먼저 클래스로부터 객체(Object)를 생성해야 한다. 파이썬에서 객체를 생성하기 위해서는 "객체변수명 = 클래스명()"과 같이 클래스명을 함수 호출하는 것처럼 사용하면 된다. 만약 __init__() 함수가 있고, 그곳에 입력 파라미터들이 지정되어 있다면, "클래스명(입력파라미터들)"과 같이 파라미터를 괄호 안에 전달한다. 이렇게 전달된 파라미터들은 Initializer 에서 사용된다.

아래 예제를 보면, Rectangle 클래스로부터 r 이라는 객체를 생성 하고 있는데, Rectangle(2, 3)와 같이 2개의 파라미터를 전달하고 있다. 이는 Rectangle 초기자에서 각각 width와 height 인스턴스 변수를 초기화하는데 사용된다.
```python
# 객체 생성
r = Rectangle(2, 3)
 
# 메서드 호출
area = r.calcArea()
print("area = ", area)
 
# 인스턴스 변수 엑세스
r.width = 10
print("width = ", r.width)
 
# 클래스 변수 엑세스
print(Rectangle.count)
print(r.count)
```

<a id="m4"></a> 
## 4. 클래스 상속과 다형성

파이썬은 객체지향 프로그래밍의 상속(Inheritance)을 지원하고 있다. 클래스를 상속 받기 위해서는 파생클래스(자식클래스)에서 클래스명 뒤에 베이스클래스(부모클래스) 이름을 괄호와 함께 넣어 주면 된다. 즉, 아래 예제에서 Dog 클래스는 Animal 클래스로부터 파생된 파생클래스이며, Duck 클래스도 역시 Animal 베이스클래스로부터 파생되고 있다.

```python
class Animal:
    def __init__(self, name):
        self.name = name
    def move(self):
        print("move")
    def speak(self):
        pass
 
class Dog (Animal):
    def speak(self):
        print("bark")
 
class Duck (Animal):
    def speak(self):
        print("quack")
```

파생 클래스의 사용
```python
dog = Dog("doggy") # 부모클래스의 생성자
n = dog.name # 부모클래스의 인스턴스변수
dog.move()   # 부모클래스의 메서드
dog.speak()  # 파생클래스의 멤버
```

## 5. 예제 : 날짜클래스 만들기
문제 :
다음 소스 코드에서 Date 클래스를 완성하세요. is_date_valid는 문자열이 올바른 날짜인지 검사하는 메서드입니다. 날짜에서 월은 12월까지 일은 31일까지 있어야 합니다.
```python
class Date:
                                                                
    ...
                                                                
 
if Date.is_date_valid('2000-10-31'):
    print('올바른 날짜 형식입니다.')
else:
    print('잘못된 날짜 형식입니다.')
```
실행 결과 예시:
```python
올바른 날짜 형식입니다.
```






정답
```python
    @staticmethod
    def is_date_valid(date_string):
        year, month, day = map(int, date_string.split('-'))
        return month <= 12 and day <= 31
```
