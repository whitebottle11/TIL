# 20240112
## git 사용법
- git init - 초기화, 처음에만 하면 됨(저장소 안에 저장소를 넣으면 안됨 주의)
- git add [파일 이름]
- git commit -m "이름"
- git status - 현재상태 확인 빨강 - 워킹 디렉토리, 초록 - 스테이징
- git log - commit 목록보기(한줄은 --oneline 추가)

## git 저장소 추가
- git remote add origin [주소](물결있으면 지우기)
- git push origin(저장소 이름) master(가지)
- git pull origin master - push랑 동작 같음
- git clone [https: 주소 ] - clone으로 받은 프로젝트는 이미 git init이 되어잇음, git remote add 안해도됨, 저장소가 아닌곳에서 clone 받아야함
- git remote -v(저장소 목록)

## git 사용자 바꾸기
- git config --global user.email "name@naver.com"
- git config --unset user.email
- git config —global -l (list) - git global 설정 정보 보기
- 윈도우 검색 - 자격증명


## gitignore
- gitignore(특정 파일이나 디렉토리 추적x - 텍스트 파일임)(파일명앞에 . 확장자 없음) - gitigonore.io(싸이트)

## 추가로 알게된것
- 저장소가 다르면 이름이 같아도 상관없다(origin) - 저장소 주소가 중요
-----
# 20240115
## 프로그램

- 명령어들의 집합
- 새 연산을 정의하고 조합하여 유용한 작업을 수행하는 것
- **문제를 해결하는 매우 강력한 방법**

---

## 프로그래밍 언어

- 컴퓨터에게 작업을 지시하고 문제를 해결하는 도구

---

## 파이썬을 사용하는 이유

- 간결하고 읽기 쉬운 문법
- 다양한 응용분야(데이터 분석, 인공지능, 웹개발)
- 세계적인 규모의 커뮤니티, 포럼

---

## 파이썬 프로그램이 실행되는 법

인터프리터가 사용자의 명령어를 운영체제가 이해하는 언어로 바꿈

인터프리터를 사용하는 방법

1. shell 이라는 프로그램으로 한번에 한 명령어 씩 입력해서 실행
2. 확장자각 .py인 파일에 작성된 파이썬 프로그램을 실행 

---

## 표현식과 값

- 표현식 - 값, 변수, 연산자 등을 조합하여 계산되고 결과를 내는 코드 구조(표현식이 평과
- 평가
    - 표현식이나 문장을 순차적으로 평가하여 프로그램의 동작을 결정
    - 문장 - 실행 가능한 동작을 기술하는 코드(조건문 반복문 함수)
    

---

## 타입

값이 어떤 종류의 데이터인지, 어떻게 해석되고 처리되어야 하는지를 정의

타입은 2가지 요소로 이루어짐

- 값
- 값에 적용할 수 있는 연산

 

---

## 연산자

-2 ** 4의 경우 -16이 나옴(**이 우선순위가 높아서)

→ (-2) ** 4 가 되어야 16이 나옴

---

## 변수

값을 **참조**하는 이름

메모리에 저장됨 - 변수는 그 변수가 참조하는 객체의 **메모리 주소**를 가짐(참조)

객체 - 타입을 갖는 메모리 주소 내 값(값이 들어있는 상자)

기존에 존재했던 변수에 재사용시 **메모리 주소를 변경**

---

## 스타일 가이드

프로그래밍의 맞춤법

---

## 주석

ctrl + / (한번에 주석달고 풀 수 있는 단축키)

---

## 진수표현

- 2진수(binary) :  0b
- 8진수(octal) :  0o
- 16진수(hexadecimal) : 0x

---

# 유한 정밀도

콤퓨터 메모리 용량이 한정돼 있고 한 숫자에 대해 저장하는 용량이 제한 됨 - 실제 값이 아닌 가장 가까운 근사값을 저장

floating point rounding error 해결책

- 두 수의 차이가 매우 작은 수보다 작은지 확인 - abs(a-b) ≤ 1e - 10
- math 모듈 활용 - math.isclose(a,b)

---

# 지수 표현 방식

314 * 0.01 = 314e-2

---

# sequence Type

- 값들이 순서대로 저장( **정렬이 되어있는것은 아님**)
    - sequence Type은 정렬되어 있다 → (X)

## 문자열 표현

작은따옴표’ 또는 큰따옴표”로 감싸서 표현 - 둘 중 하나로 통일해주어야 함

따옴표 안에 따옴표를 표현할 경우 다른 따옴표를 사용하여 표현

## f-string

문자열에 f 또는 F 접두어를 붙이면 {}안에 변수나 표현식을 삽입 가능

**{변수}[ : ]가 가능함** 

ex) little = ‘작은별’    

print(f’{little[:2]} {little[-1]}) → 작은 별

{변수:.2f} → 소수점 2자리까지 나타내라

{변수*변수*변수} 가능

{변수*변수*변수:.2f} → 변수의 곱의 결과값의 소수 2자리까지 나타내라

## slicing

step을 지정하여 추출 - my_str[0 : 5 : 2] → 한칸씩 건너뛰며 추출(0,2,4)

문자열 뒤집기 - my_str[ : : -1]

## 문자열은 불변

**문자열 일부를 바꿀수는 없다 - 메모리에 덩어리채로 들어가기 때문**

바꾸고 싶다면 새로운 문자열을 만들어야 함(메모리 유지 못함)

---

# 추가로 알게된 것

## f-string

문자열에 f 또는 F 접두어를 붙이면 {}안에 변수나 표현식을 삽입 가능

**{변수}[ : ]가 가능함** 

ex) little = ‘작은별’    

print(f’{little[:2]} {little[-1]}) → 작은 별

{변수:.2f} → 소수점 2자리까지 반올림하여 나타내라

f'{name:10} -> 최소 문자열 폭을 10자리까지 나타내라(문자열 정렬할 때 유용함)

{변수*변수*변수} 가능

{변수*변수*변수:.2f} → 변수의 곱의 결과값의 소수 2자리까지 나타내라

## slicing

step을 지정하여 추출 - my_str[0 : 5 : 2] → 한칸씩 건너뛰며 추출(0,2,4)
변수명[0:5:-1] → 실행안됨 ⇒ 반대로 출력하고 싶다면 변수명[ : : -1]

## string

따옴표는 쓰는 순서 관계없이 적용됨

따옴표 안에 큰따옴표를 넣고 싶다면 작은 따옴표 안에 큰 따옴표를 쓰거나 \”를 사용

## 문자열 format 매서드
print('{0}와{1}은 같지 않다'.format('사과','당근')) ==> 사과와 당근은 같지 않다
print('{1}와{0}은 같지 않다'.format('사과','당근')) ==> 당근와 사과은 같지 않다
print('We are the {} who say "{}!"'.format('knights', 'Ni')) ==> We are the knights who say "Ni!"
print('The story of {0}, {1}, and {other}.'.format('Bill', 'Manfred', other='Georg')) ==> The story of Bill, Manfred, and Georg.
---
# 2024-01-16

---

## sequence Types

여러 개의 값들을 순서대로 나열하여 저장하는 자료형(str, list, tuple, range) → **정렬 X**

### tuple(튜플)

여러 개의 값을 **순서대로 저장**하는 **변경 불가능**한 시퀸스 자료형

어떤 자료형도 저장 가능

```python
my_tuple_1 = ()

my_tuple_2 = (1**,**) → 콤마를 반드시 넣어줘야 함(빠지면 정수 1이 되어버림)

my_tuple_3 = (1, ‘a’, 3, ‘b’)
```

개발자가 의도적으로 쓰기보다 파이썬 내부 동작에서 쓰임

파이썬은 ,를 통해 한번에 할당 가능 → x,y = (10,20)

→ x = 10, y = 20 (괄호는 생략 가능하다)

### range

연속된 정수 시퀀스를 **생성**하는 **변경 불가능**한 자료형

range(n) → 0부터 n-1까지 숫자 시퀸스

range(n,m) → n부터 m-1까지의 숫자 시퀸스

print(range(5)) == range(0,5)

→ 리스트로 형변환 시 데이터 확인 가능 =⇒ print(list(my_range_1)) #[0,1,2,3,4] 

---

## Non-sequence Type

### dict - 딕셔너리

**key - value** 쌍으로 이루어진 **순서와 중복이 없는 변경 가능**한 자료형

key는 변경 불가능한 자료형만 사용 가능(str, int, float, tuple, range…)

value는 모든 자료형 사용 가능

{}로 표시 my_dic = {’key’ : ‘value’, ‘list’ : [1,2,3]}

key로 접근(my_dict[’apple’]) - 순서가 없기때문에 인덱스로 접근 못함

중복안됨 → 마지막에 넣은 값이 나옴

### set

**순서와 중복이 없는 변경 가능**한 자료형

{}로 표기

```python
my_set_1 = set()

my_set_2 = {1, 2, 3} 

my_ set_3 = {1, 1, 1} == {1}
```

set는 **집합연산**이 가능함 - 합집합, 차집합, 교집합

---

## Other types

### None

값이 없음을 표현하는 자료형

print 가능

N이 대문자임

### Boolean

참과 거짓을 표현하는 자료형 (T와 F를 대문자로 써야함)

collection

---

## Type Conversion

### 암시적 형변환

파이썬이 자동으로 형변환 하는 것

```python
print(3+0.5) = 8.0

print(True + 3) = 4       True는 1 False는 0 거의 다 적용됨

print(True + False) = 1
```

### 명시적 형변환

개발자가 직접 형변환 하는 것(암시적 형변환이 아닌 모든 경우)

str → integer : 형식에 맞는 숫자만 가능

integer → str : 모두 가능

---

## 비교 연산자

### is 비교 연산자

메모리 내에서 같은 객체를 참조하는지 확인(주소를 비교)

==은 동등성(equality), is 는 식별성(identitiy)

```python
print(1==True) → True (암시적 형변환 일어남)

print(1 is True) → False
```

---

## 논리 연산자

### 단축평가

논리 연산에서 두 번째 피연산자를 평가하지 않고 결과를 결정하는 동작

```python
vowels = ’aeiou’

print((’a’ and ‘b’) in vowels) == b in vowels

print((’b’ and ‘a’) in vowels) == a in vowels

print(3 and 5) = 5

print(0 and 3) = 0 → 단축평가

print(5 or 3) = 5 → 단축평가

print(3 or 0) = 3 → 단축평가

print(0 or 3) = 3
```

---

## 추가로 알게 된 것

### mutable

값이 변한다

### immutable

값이 변하지 않는다

### 얕은 복사(shallow copy)

b에 a를 할당하면 값이 할당되는 것이 아니라 같은 메모리 주소를 바라본다

따라서 b를 변경하면 a도 바뀐다

```python
a = [1, 2, 3]
>>> b = a # shallow copy
>>> b[0]= 5
>>> a
[5, 2, 3]
>>> b
[5, 2, 3]
>>> id(a)
4396179528
>>> id(b)
4396179528
```

### 깊은 복사(deep copy)

내부의 객체들까지 모두 새롭게 copy되는 것

```python
import copy
>>> a = [[1,2],[3,4]]
>>> b = copy.deepcopy(a)
>>> a[1].append(5)
>>> a
[[1, 2], [3, 4, 5]]
>>> b
[[1, 2], [3, 4]]
```

a를 변경해도 b가 바뀌지 않는다


# 20240117

# 함수
&emsp; 특정 작업을 수행하기 위한 **재사용 가능**한 코드 묶음

## 내장함수
- 파이썬이 기본적으로 제공하는 함수
별도의 **import없이** 바로 사용 가능
```
result = abs(-1)
```

## 함수 구조
- parameter : 매개변수
- body
- return value : 반환값

## 함수의 정의와 호출
- Docstring
    ```
    """
    함수의 설명법
    """
    ```로 함수의 사용법을 적음
- return
    함수의 실행을 종료하고 결과를 호출 부분으로 반환

## 매개변수와 인자
### 매개변수(parameter)
&emsp; 함수를 **정의**할 때 함수가 받을 값을 나타내는 변수
### 인자(argument)
&emsp; 함수를 **호출**할 때, 실제로 전달되는 값

1. Positional Arguments(위치인자)  
   - 함수 호출시 인자의 위치에 따라 전달되는 인자  
   - **위치인자는 함수 호출 시 반드시 값을 전달해야 함**
2. Default Argument Value(기본 인자 값)
   - 함수 정의에서 매개변수에 기본 값을 할당하는 것
   - 함수 호출 시 인자를 전달하지 않으면, 기본값이 매개변수에 할당됨
3. Keyword Argument(키워드 인자)
   - 함수 호출시 인자의 이름과 함께 값을 전달하는 인자
   - **호출 시 키워드 인자는 위치 인자 뒤에 위치해야 함**(인자가 어느 위치인지 알 수 없기 때문)
4. Arbitrary Argument Lists(임의의 인자 목록)
   - 정해지지 않은 개수의 인자를 처리하는 인자
   - 함수 정의 시 매개변수 앞에 '*'를 붙여 사용하며, 여러개의 인자를 tuple로 처리
5. Arbitrary Keyword Argument Lists(임의의 키워드 인자 목록)
   - 정해지지 않은 개수의 키워드 인자를 처리하는 인자
   - 함수 정의 시 매개변수 앞에 '**'를 붙여 사용
   - 여러 개의 인자를 dictionary로 묶어 처리

### 함수 인자 권장 작성순서  
&emsp; 위치 -> 기본 -> 가변 -> 가변키워드
```
def func(pos1, pos2, age =30, *args, **kargs):
print(pos1, pos2, age, args, kargs)
func(10, 10, 50, (10,30), {})
-> 10 10 50 10 30 {}
```
## 파이썬의 범위(Scope)
- 로컬 변수를 글로벌에서 사용할 수 없음
- 이는 변수의 **수명주기**와 연관있음

### 이름 검색 규칙(Name Resolution)
- LEGB Rule
- **함수 내에서는 바깥 Scope의 변수에 접근 가능하나 수정은 할 수 없음**
- 반대로(안쪽으로) 찾아가는것은 불가

## 유용한 내장함수
### map(function, iterable)
- 순회 가능한 데이터구조(iterable)의 모든 요소에 함수를 적용하고, 그 결과를 map object로 반환
- map 함수로 쓴 데이터는 mpa object 덩어리기 때문에 list로 감싸주어야 함
- map에 함수 매개변수를 줄 때 ()을 빼고 함수명만 넣어야 함("()"을 넣으면 map이 실행될때 매개변수로 넣은 함수가 같이 실행되기 때문)

### zip(*iterables)
- 임의의 iterable을 모아 튜플을 원소로 하는 zip object를 반환

### lambda(람다)함수
- 이름 없이 정의되고 사용되는 익명 함수
- lambda 매개변수 : 표현식
- map의 첫번째 인자에 많이 쓰임
```
numbers = [1, 2, 3, 4, 5]
def func(x):
    return x ** 2

result = list(map(func, numbers))
pritn(result)

result2 = list(map(lambda x: x**2, numbers))
print(result2)
```
## Packing & Unpacking
### Packing
- 여러개의 값을 하나의 변수에 묶어서 담는 것
- 변수에 담긴 값들은 튜플(tuple)형태로 묶임

### unpacking
- 패킹된 변수의 값을 개별적인 변수로 분리하여 할당하는 것
- *는 리스트 요소를 언패킹
- **는 딕셔너리의 키-값 쌍을 함수의 키워드 인자로 언패킹(인자와 매개변수가 같아야 함)
---
# 추가로 알게된 것
1. 파이썬에서는 return이 없는 함수는 자동을 none을 리턴
   ```
   a = print(1)
   print(a) # None
   ```
2. global 글로벌변수 의 값을 변경할 경우 재할당을 해야하기 때문에 global 변수명을 적어야 한다 - print()는 변수명을 안 적어도 가능(참조는 가능, 재할당은 불가능)
3. 함수의 매개변수로 Unpacking을 줄 경우 튜플로 만들어져서 나온다
   ```
   def create_user(*total_user_info):
    print(total_user_info)
    name, age, address = total_user_info
    increase_user()
    user_info = {'name': name, 'age' : age, "address" : address}
    print(f'{user_info["name"]}님 환영합니다!')
    return user_info



    name = ['김시습', '허균', '남영로', '임제', '박지원']
    age = [20, 16, 52, 36, 60]
    address = ['서울', '강릉', '조선', '나주', '한성부']
    total_user_info = list(zip(name, age, address)) 
    print(list(map(create_user, total_user_info)))
   ```
   결과 : ValueError: not enough values to unpack (expected 3, got 1)
   이유 : (('김시습', 20, '서울'),)

    ### 올바른 코드
   ```
   def create_user(*total_user_info):
    name, age, address = total_user_info
    increase_user()
    user_info = {'name': name, 'age' : age, "address" : address}
    print(f'{user_info["name"]}님 환영합니다!')
    return user_info



    name = ['김시습', '허균', '남영로', '임제', '박지원']
    age = [20, 16, 52, 36, 60]
    address = ['서울', '강릉', '조선', '나주', '한성부']
    print(list(map(create_user, name, age, address)))
   ```
   결과 :('김시습', 20, '서울')로 매개변수가 들어감
   
4. map의 인자는 여러개 들어갈 수 있다 - map(함수, args1, args2, ...)
5. lambda 함수에 딕셔너리가 바로 들어갈 수 있다
    ```
   list(map(lambda user_info: {'name' : user_info['name']}, iterable))
   ```
6. 함수의 바디가 존재하면 lambda함수로 만들 수 없다.
7. map의 인자로 리스트를 줄 경우 리스트가 벗겨져서 들어간다 - [{'ㅁ' : 1, 'ㄴ' : 2}] -> {'ㅁ' : 1, 'ㄴ' : 2} ( 안의 요소들만 들어가기 때문)

# 2024-01-18
## 모듈
- 한 파일로 묶인 변수와 함수의 모음 -> .py 파일
- .(dot)는 왼쪽의 객체에서 오른쪽 이름을 찾아라 라는 의미의 연산자
- 만약 서로 다른 모듈이 같은 이름의 함수를 제공할 경우 문제 발생 -> 마지막에 import된 이름으로 대체됨

## 파이썬 표준 라이브러리(PSL)
파이썬 언어와 한께 제공되는 다양한 모듈과 패키지의 모음

## pip
- 외부 패키지들을 설치하도록 도와주는 파이썬의 패키지 관리 시스템

## List comprehension 구조
- 간결하고 효율적인 리스트 생성 방법
- [expression for 변수 in iterable]
- [expression for 변수 in iterable if 조건식]
  
## enumerate(iterable, start = 0)
- iterable 객체의 각 요소에 대해 인덱스와 함께 반환하는 내장함수

## 추가로 알게 된 것
- 함수 return의 데이터 타입은 다르게 리턴할 수 있다(리턴될 때 데이터 타입 결정)
```
def func():
   return "ex"
   return a,b  #튜플로 출력 됨
``` 
- 딕셔너리의 출력 순서는 만들어질 때 정해짐

# 20240122
## 메서드
 - 메서드는 클래스 내부에 정의되는 함수
 - 클래스는 파이썬에서 '타입을 표현하는 방법이며 은연중에 사용해왔음
 - 객체.메서드
 ### 문자열 조작 메서드
- 바꿀 수 없기 때문에 새로운 문자열을 리턴한다
- .replace(old, new[, count]) - []는 선택인자라는 뜻(안넣어도 됨)
- 언어가 다르더라도 공통적으로 표기(베커스 나우르 표기법)
- .split(sep = None, maxsplit = -1) 아무것도 안넣을 시 공백이 기준
- 앞의 결과가 None이라면 이어서 활용 불가
- print(my_list.append([10,9,,8])) - None이 출력, 원본을 바꾸는 함수는 반환값이 없다
- .pop(i) i 값을 안주면 마지막요소 삭제
- .sort() 반환값 None -> 원본을 바꾼다, sort(reverse = False)가 기본 (reverse = True)로 바꿀 시 내림차순 가능
### 복사
- 변경가능한 데이터 타입의 복사와 변경 불가능한 데이터 타입의 복사는 다르다
- 리스트 복사 : 할당 연산자를 통한 복사는 해당 객체에 대한 객체 참조를 복사한다
- 얕은 복사의 한계 : 2차원 리스트 까지는 복사를 못한다(원본과 같은 주소를 가짐)
## 추가로 알게 된 것
- min(리스트), max(리스트)는 내장함수로 최솟값과 최댓값을 구해준다.
- revered(리스트)를 사용하면 object 형태로 반환되기 때문에 join()이나 list()를 사용하여 문자나 리스트 형태로 바꿔주어야 한다.
- sort()를 사용하면 반환값이 없다 (원본을 바꾸기 때문에 return 값이 필요없다) 따라서 결과를 다른 변수에 할당하지 못한다(reserved()를 대신 사용)
- 빈배열.extend(arr)을 하면 arr의 각 문자열이나 원소를 모두 나누어 빈 배열에 담는 것이 가능하다
  ```
  original_word = '코딩 공부는ㄴ 1일ㄹ 1커ㅓ밋ㅅ @@@#^()#_+!&~:"'

  arr = []
   arr.extend(original_word)
   print(arr)
   # ['코', '딩', ' ', '공', '부', '는', 'ㄴ', ' ', '1', '일', 'ㄹ', ' ', '1', '커', 'ㅓ', '밋', 'ㅅ', ' ', '@', '@', '@', '#', '^', '(', ')', '#', '_', '+', '!', '&', '~', ':', '"']
   ```
- int 타입을 extend()를 사용하여 배열의 넣을 경우 []로 감싸 리스트로 만들어 주면 된다.
- .split('구분자')를 사용하면 구분자는 문자열에 포함되지 않는다
  ```
  text = 'hello world ioioi'
   a = text.split('o')
   print(a)
   # ['hell', ' w', 'rld i', 'i', 'i']
  ```
- 파이썬의 변수는 타입을 명시하지 않아 자유롭게 바꿀 수 있다
   ```
   a = [1,2,3]
   b = a
   a = 50
   print(a,b)
   # 50 [1, 2, 3]
   ```

# 20240123
## 비시퀸스 데이터 구조
### set
- .remove(x) x가 없다면 에러 but .discard(x)는 없어도 에러없음
### 딕셔너리 관련 키원드
- .keys()를 사용하면 []형태로 나옴
- .update(key=value)형태로도 사용가능, 인자 여러개 넣어도 가능하다
### 해시
- 순서가 상관이 없다
- set pop메서드: 정수 값 자체가 곧 해시 값이기 때문에 결과가 항상 같다, 문자는 항상 다름
- 정수는 해시 값이 정해져 있다(정수 값 == 해시 값) - 불피요한 연산을 줄일 수 있기 때문에
- 해시 테이블에 나열된 순서(색인)는 인덱스와 상관없다
- pop은 해시 테이블에서 먼저 있는 순서대로 값을 뺀다
- **정수는 해시 값이 고정되어 있을 뿐이지 순서가 있는 것은 아니다**
- "arbitrary" the docs don't mean "random"
- 배치된 순서대로 뽑아오지만 배치 순서는 임의로 정해진다
- tuple은 불변형이지만 list와 같이 해시 불가능한 객체를 참조 할 때는 tuple 자체도 해시 불가능해질 수 있다
- set안에 list 못들어감
## 추가로 알게 된 것
- set는 불변이기 때문에 가변적인 요소가 들어갈 수 없다.
- 정수와 문자를 섞었을 때 정수의 반환값도 바뀌는 이유: 해시값을 변수에 넣어진 순서대로 받기 때문에 같은 주소를 가질 수 없어 정수가 다른 주소를 가질 수 있다.
   ```
   my_str_set = {'a','b','c','d','e','f',3,2,1,9,100,4,87,39,10,52}
   print(my_str_set.pop())
   print(my_str_set.pop())
   print(my_str_set.pop())
   # 값이 매번 달라짐
   ```
- 정수의 해시값이 정수와 같은데 숫자의 순서대로 안나오는 이유: 해시 테이블은 정수 순서대로 정렬되어 있지 않기 떄문이다