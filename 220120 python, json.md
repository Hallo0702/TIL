## Key 값 존재여부 확인하기
* if('abc' in dt) == True<br>
    * abc 값이 dt에 있는지 검사

## 문자열 입ㄹ력받고 예약된 숫자 출력
```
dict_1 = {'KFC' : 10, 'MC' : 20, 'MOMS' : 30}
c = input()
if (c in dict_1) == True:
    print(dict_1[c])
else:
    print(1000)
```

## 키 값을 모두 출력하기
```
dt = dict()
dt[15] = 1
dt[20] = 2
dt['ABC'] = 5
for i in dt.keys():
    print(i,dt[i])
```

## Tuple 과 list 의 차이점
```
a = (4,2,5,6)

for i in a:
    print(1)

a[0] = 10
```
만약 a = (1,2,3)에서 하나의 요소를 제거하거나 수정하려 해도 수정 할 수 없다.<br>
a[0] = 10 에서 에러 발생

* 배열처럼 사용 가능하다.
    * 단, 수정,삭제가 되지 않는 것을 명심하자.
    * A + A 는 튜플 더하기
    * 5 IN A 는 요소에 값이 있는지 확인
    * a[0:2] 는 슬라이싱으로 0~2 전까지 값 가져오기
```
a = (4,2,5,6)
b = a + a

print(b)
print(5 in a)
print(a[0:2])
```

* 함수에서 값을 하나만 리턴할 때
    * 튜플로 값을 묶어서 리턴이 가능
* 함수에 값 하나만 전달할 때
    * 튜플로 값을 묶어서 전달이 가능
```
def abc():
    return 1,2,3,4
print(abc())

def run():
    return (5,3,2)

ret = run()
print(ret)

def run(a):
    for i in a:
    print(i)

run((1,2,3,4,5))

def run(a):
    for i in a:
    print(i)

run((1,2,3,'SDFS', 34))
```
* 파이썬은 특별하게 다음과 같은 동작이 가능
```
def run():
    a = [1,2,3,4,5]
    return a
b = run()

print(b)

def run():
    return 1, 2, 3

a, b, c = run()

print(a,b,c)
```
## Tuple 실습
1. 숫자 3개 입력, Tuple 변환
2. 모드 ㄴ요소에 5를 더한 값으로 두번째 Tuple 제작
3. 두 개의 Tuple,ABC함수로 전달하기
4. ABC함수에서 2개의 튜플 출력
```
a, b, c = map(int, input().split())
tu_1 = (a,b,c)
tu_2 = (a+5,b+5,c+5)

def ABC(tu_a,tu_b):
    print(tu_a)
    print(tu_b)

ABC(tu_1,tu_2)

or

a = tuple(map(int,input().split()))
b = tuple([i+5 for i in a])

def ABC(a,b):
    print(a)
    print(b)

ABC(a,b)
```

## index 값 구하기
특정 값을 찾아서 , index 값을 리턴하는 방법
* 값이 없다면 error
* in 을 이용하여 내부에 값이 있는지 먼저 확인하자
```
a = tuple([1,2,377])

print(a.index)
```

## List에 들어있는 값을 쉽게 counting 가능

```
a = [4,3,4,3,4,3,4]

print(a.count(4))
```

## max/min 구하기
* max([]) 또는 min([]) 사용
* 튜플 리스트 모두 사용 가능
```
b = (4,3,4,3,4,3,4)

print(max(b))
```

## 특정 범위의 객체 새롭게 생성
* 슬라이싱 형태:aa[시작:끝(포함x):stride]
```
a = [1,5,4,5,3,2]

b = a[0:6:2]
print(b)
```

## for 문 연습하기!
```
a = [4,2,5,1,6,3,4]
l = len(a)
for i in range(l):
    print(a[i], end = ' ')
for i in a:
    print(i, end = ' ')
for i in range(l-1,-1,-1):
    print(a[i], end= ' ')
n = 0
while(n < l):
    print(a[n], end = ' ')
    n+= 1
```
```
a = [4,2,5,1,6,3,4]
for i in a:
    if i % 2 == 0:
        print(i,end = '')
# 앞부터 짝수만 출력
for i in range(len(a)-1,-1,-1):
    if a[i] % 2 == 1:
        print(a[i],end = '')
#뒤부터 홀수만 출력
for i in a:
    if i >=4 and i <= 6:
        print(i,end = '')
# 4이상 6이하 출력
```
## 2중 for 문 연습!
1. 시작하기 앞서
    * 1차원 배열을 0으로 채우기:<br>
    a = [0] * 10
    * 2차원 배열을 0으로 채우기
    c = [[0,0,0],[0,0,0],[0,0,0]]

    d = [[0 for _ in range(3)] for _ in range(4)]


# json
1. format
2. encoding / decoding
3. 

## Json이란?
* 데이터들을 교환할 떄 정해진 규격
* 유저도 보기가 편하고 컴퓨터도 보기편하게(파싱하기 편하도록) 만든 문서형태
<br><br>
이름 나이 성별 전번 <br>
땡땡 39세 남 01012071029<br>
홍길동 -세 남 9019270192<br>
등으로 정리하여 보기도 편하고 컴퓨터가 자료추출(파싱) 하기도 편한 형태.<br><Br>
과거에는 csv 형태, xml형태로 많이 사용.<br>
요즘은 json 형태 표기법을 많이 사용.<br>
딕셔너리 자료구조와 비슷하다!

### 표준파일교환 Format
    * web에서 ajax기술에 사용된다.
    * api 사용시에 사용된다.
    * database 에 사용된다.
    * 환경 설정 값 저장용

[json 문법검사기](https://jsonlint.com/)<br>
[온라인 json 뷰어](http://jsonviewer.stack.hu/)
<br><br>
Json은 array/object로 시작한다.
* [] 괄호로 묶여있는 것이 배열이다.(list)
* {} 괄호로 묶여있는 것이 객체이다.(dict)
* 객체는 중복 key값을 허용하지 않는다.
<BR>
```
{
    "group":"BTS",
    "name":["aaa","bbb","ccc","ddd"],
    "age":[35,"Unknown",56,55]
}
```
```
{
    "love":[chayoon,jihyo,[computer,notebook,mouse]],
    "dislike":[hungry,777]
    
}
```
True/False 도 집어넣을 수 있음
 * 사용 가능한 타입
    * 배열 /객체
    * string
    * number
    * 소수점 
    * Boolean 타입
```
[
    [1,2,3],
    [3,4,5],
    {"A":3,"B":6,"OK":false},
    true
]
```

```
{
    "이름" : "홍길동",
    "나이" : 25,
    "성별" : "여",
    "주소" : "서울특별시 양천구 목동",
    "특기" : ["농구","도술"],
    "가족관계" : {"#":2,"아버지":"홍판서","어머니":"춘섬"},
    "회사":"경기 수원시 팔달구 우만동"
}
```

```
# 절댓값 만들기
def my_abs(x):
    if type(x) == int or type(x) == float:
        if x == -0:
            return -x
        
        if x >= 0:
            return x
        else:
            return -x
    elif type(x) == complex:
        x = (x.real**2 + x.imag**2)**(0.5)
        return x
# 전부 트루면 트루 판별하기
def my_all(elements):
    for element in elements:
        if bool(element) == False:
            return False
    else:
        return True

# 하나라도 트루면 다 트루
def my_any(elements):
    for element in elements:
        if bool(element) == True:
            return True
    else:
        return False
```
## 함수 만들기 연습!
```
1-1
def my_abs(x):
    if type(x) == int or type(x) == float:
        if x == -0:
            return -x
        
        if x >= 0:
            return x
        else:
            return -x
    elif type(x) == complex:
        x = (x.real**2 + x.imag**2)**(0.5)
        return x
1-2
def my_all(elements):
    for element in elements:
        if bool(element) == False:
            return False
    else:
        return True

1-3
def my_any(elements):
    for element in elements:
        if bool(element) == True:
            return True
    else:
        return False
# 달팽이가 올라가는데 걸리는 시간
2-1
def snail(height, day, night):
    time = 0
    stay = 0
    while stay <= 100:
        stay += day
        time += 1
        if(stay >= 100):
            break
        stay -= night
    
    return time
# 숫자 각 자리수 더하기
2-2
def sum_of_digit(number):
    hap = 0
    while number > 0:
        hap += number%10
        number //= 10
    
    return hap
# 펠린드롬 언어 판정
3-1
def is_pal_while(word):
    l = len(word)
    n = 0
    while n < l:
        if word[n] != word[-1-n]:
            return False
        n += 1
    
    return True
3-2
def is_pal_recursive(word):
    l = len(word)
    if l <= 1:
        return True
    if word[0] != word[-1]:
        return False
    else:
        return is_pal_recursive(word[1:l-1])
```
## HTML이란?
* 웹문서를 이야기한다.
 
## HTTP란??
* 웹 서버와 사용자의 인터넷 브라우저(개인컴퓨터) 사이에 문서를 전송하기 위해서 사용되는 통신 규약(프로토콜)<br>
규약에는 신호 송신의 순서, 데이터의 표현법 등이 있음.<br><br>
클라이언트(내가) 보고싶은 정보를 서버에게 http를 통해서 요청<br>
서버가 이 요청을 받으면 응답메세지나 정보를 클라이언트에게 전달 하는 역할

## API 란?? (간단하게 말해서)
* 컴퓨터의 기능을 실행시키는 방법을 이야기 합니다.<br>
서버에게 정보를 요청을 할 때 사용하는 명령어!!<br><br>
운영체제...api가 있다.<br>
app개발 앱은 컴퓨터 하드웨어에 직접적으로 접근할 권한이 없습니다.<br>
앱으로 내 컴퓨터 또는 모바일의 카메라를 키고 싶다.<br>
운영체제에게 부탁을 해야합니다. api
<br><br>
sw systme sw/// application sw
<br><br>
증권정보를 얻기 위해서는 증권사 서버에게 요청<br>
나는 우리집, 증권사 서버는 원격지에 있다.<br>
원격지로 api호출(정보요청)<br>
원격지로 정보를 달라고 신호를 보내는데 이 신호를 HTTP 프로토콜을 사용해서 api를 호출하는 것 ---> rest api
<br>
<br>
서버랑 클라이언트가 한 컴퓨터 안에있다<br>
api 함수를 불러오면 된다.
<br><br>
서버 = 라이브러리<br>
요청 = main 함수 or 시작 할때 함수 call