# 1일차 복습
# OpenCV: Open Source Computer Vision Library

## Resources
* Homepage: https://opencv.org
    * Courses: https://opencv.org/courses
* Docs: https://docs.opencv.org/4.x/
* Q&A forum: https://forum.opencv.org
    * previous forum (read only): https://answers.opencv.org
* Issue tracking: https://github.com/opencv/opencv/issues
* Additional OpenCV functionality: https://github.com/opencv/opencv_contrib

## Contributing
Please read the [contribution guidelines]() before starting work on a pull request.

### Summart of the guidelines:
* One pull request per issue;
* Choose the right base branch;
* Include tests and documentation;
* Clean up "oops" commits before submitting;
* Followw the [coding style guide]()


# 2일차 시작 여러명이 한 레포 사용하기.
* 조원들과 한 레포에서 질의응답을 해보자
* 조장이 만들고 초대 -> 조원들은 초대받아서 한사람이 push 하면 다음사람이 pull해서 수정후 push 반복<br>

# 깃의 구조
* 지금까지는 3단계 구조로<br>
remote-local-작업폴더 라고 생각했지만<br>
이제부터는 4단계 구조로 생각하자<br>
remote-local-staging area<커밋대기실>-작업폴더<br>
git에는 존재하지만 github에는 숨겨두고있다!!!<br>
* 추적 = 자동감지<br>
변경된 내용을 감지하는 것을 추적이라고 한다.(자동으로 git이 알아서 추적함)
* staging area에 올리기(add)
* commit 하기
* push 하기

# 인증 Factor

## 본인인증하는방법
- 보통 password많이씀

## two factor 인증
-password + 공인인증서

## multi-Factor 인증
2개 이상 Factor로 인증하는 방식<br>
ex)password+공인인증서+휴대폰인증 등등<br>

## 키파일 인증 
 -> 내 컴퓨터에 key-file이 있으면 내 컴퓨터에만 사용가능<br>
 -> 실수로 github에 업로드하면 다운받는 사람 누구나 사용가능해짐.<br>

 그러므로 깃허브에 업로드하고 싶지 않은 파일들을 ignore기능을 사용한다!<br>
 키파일 비밀번호 등등...<br>

 굳이 업로드 할 필요 없는 파일들도 ignore 해도 된다.

 1. .gitignore 파일에 ignore할 문서를 적어놓는다.
 2. github desktop에서 repo. setting 에 들어가서 ignore란에 파일작성.

 한번에 ignore하기
 -> temp*로 할시 temp로 시작하는 모든 파일 감지x<br>
 폴더도 ignore가능

 [참고]<br>
 옛날에는 디렉토리를 폴더라 불렀음<br>
 즉, 디렉토리 == 폴더

# 운영체제
 * 아이폰의 운영체제
    * IOS
 * 갤러시의 운영체제
    * Android
 * 우리집 tv의 운영체제
    * 리눅스
 * 등등

 ## 리눅스
 전자제품에 많이 들어가는 운영체제<br>
 슈퍼컴퓨터 대부분에 많이 들어감<br><br>
 리눅스는 Android,타이젠(삼성tv등에 들어가는 운영체제) 의 조상

 ### 대학생들에게는
 대학교 컴공과 학생들에게는 "운영체제"라는 핵심과목이 있다.<br>
 이 과목은 오픈소스인 리눅스를 기준으로 배운다!

 ### 리눅스의 개발
 유닉스에서 발전

 ### 유닉스란?
 전화기 회사 "벨 연구소"에서 C언어를 제작한 켄 톰슨과 데니스 리치 가 C언어를 만들고 나서, 이 대단함을 널리 알리고자, 본인들이 만든 C언어로 운영체제를 만들었는데 그게 UNIX.<br><br>
 그래서 리눅스 책을 사든 유닉스 책을 사든 명령어가 비슷해서 아무거나 공부해도 된다.

# 개발자 공부과정
1. 언어(기본) : C++,JAVA,PYTHON 등등
2. PS(Problem solving) : 자료구조, 알고리즘<br>
    자료구조 : 입력된 자료를 어디에,어떤 규칙에 따라 저장할 것인가?<br>
    알고리즘 : 문제해결하는 빠른 방법.<br>
어디에나 사용하는 기본체력같은 파트. -> 코딩테스트
3. CS(conputer science)-컴퓨터기본지식<br>
이걸 못하면 문제가 생겼을때 어디에서 문제가 생겼는지 알 수 없음. 이걸 잘 알면 알기 쉬움.
4. 분야 - 전문분야(web,app,embeded,security 등등)<br><br>
비전공자에게 자격증 추천하는 이유 -> 자격증을 공부하는 과정중에 모르는 단어가 나오거나하면 찾아보면서 내 CS지식이 늘어난다!!!

## 운영체제의 핵심소스코드 "커널"    

### 리눅스 커널 소스코드 구분해보기
* 메모장은 커널 소스코드일까?<br> X -> 메모장이 없다고 윈도우가 안돌아가지않음.
* CPU, 모니터 등 장치 관리 소스코드는 커널 소스코드일까?
<br> Y -> 없으면 윈도우가 돌아가지 않을 수 있음.

## 리눅스란?
정확히 말하면 운영체제의 커널의 이름!

### 리눅스 "배포판"
운영체제 - "커널" + 기타 S/W들
<br>
<br>
가장 유명한 리눅스 배포판<br>
Android : 모바일<br>
우분투 : 서버 컴퓨터<br>

## 운영체제 다루는 방법

### Shell
사람이 tv를 사용하고, 설정 등 할 수 있도록 해주는 중간다리 역할 = 'tv 리모컨'<br><br>
사람이 운영체제를 사용하고, 설정 등 할 수 있도록해주고 명령에 대한 결과도 보여주는 중간다리 역할 프로그램 = '셸'<br>
<br>
[참조] Interface?<br>
lg tv건 삼성tv건 사용법은 모른다, 내부원리도 모른다 하지만 리모컨만 잘 사용하면 조종할 수 있다. 이런 중간다리 역할을 하는 것을 Interface 라고 한다.
<br>
<br>

## 셸의 두가지 인터페이스
1. GUI (EX - 깃허브 데스크탑)<br>
키보드 마우스를 이용하여 조종
2. CLI - 소스코드.<br>
키보드를 사용하여 글자로 운영체제를 사용하고, 글자로 결과를 확인
<br>
<br>

GUI를 사용하는 이유
* 쉽게 느껴진다<br>

CLI를 사용하는 이유
* 만약 알집이라는 프로그램을 설치한다고 해보자.<br>
설치과정 -> APT INSTALL ALZIP
<br> 직접 클리하는 과정을 건너뛰고 한번에 실행한다.

GUI 단점
* Window 업데이트가 두렵다.<br>
제어판 못 찾고, 바탕화면 바꾸는거 또 배워야한다 ....etc

CLI 장점
* 한번 배우기가 어렵지만 한번 명령어를 외웠다면?<br>
버전업데이트를 하더라도 명령어가 똑같다.<br>

## 윈도우 사용자 미션!
키보드로만 수행한다
* 시작버튼+R
* CMD 입력 후 엔터
* tree 입력(딱히 의미는 없음)

리눅스 배포판
<br> 리눅스 배포판 -> 쉘 -> 커널

# Unix CLI 명령어 공부 준비!!!
윈도우 사용자는 Linux CLI Shell 설치!<br><br>
가장 많이 사용하는 프로그램 : Bash 배쉬 -> git 설치하면, 함께 설치됨.<br>

## 명령어
### touch 명령어
 빈 파일을 하나 생성한다.

 ### mkdir
  mkdir [디렉토리 이름]
  <br>-> 폴더 생성
  <br>
  ls = 결과확인

### 도전 CLI 명령어 연습 1
1. mc.txt bbq.txt 파일생성
2. test1, text2 디렉토리 생성
3. ls 명령어로 결과확인
4. 화면지우기
5. 윈도우에서 결과확인해본뒤 지우기
6. ls로 결과확인

### cd : 디렉토리로 이동하자
 먼저 디렉토리를 만든다
* mkdir abc
* ls
<br>
이동하자
 * cd abc

cd 입력후 한칸 띄고 .. 입력
<br> -> cd .. -> 상위 디렉토리로 이동

### rm -r [파일 or 디렉토리 이름]
rm : remove<br>
-r :<br>
* rm 명령어의 추가 옵션으로 r을 지정했다.
* 지정된 폴더 내부의 폴더들 까지도 모두 제거하라는 의미이다.
* 이거 안써주면, 폴더 안에 폴더가 있는 경우 지울 수 없다고 나옴
* 그래서 -r 옵션은 무조건 써주는 것으로 암기하자.

## 도전 cli 명령어 연습2 2분
1. aaa 디렉토리 생성후 파일 목록 확인
2. aaa 디렉토리 이동
3. bts.txt 생성후 목혹 확인
4. bbb 디렉토리 생성 후 이동
5. ccc.txt 생성 후 목록 확인
6. ddd.txt 생성 후 목록 확인
7. ccc.txt 파일 삭제 후 확인
8. 상위 디렉토리 이동후 확인
9. bbb 삭제후 목록 확인
10. 상위 이동후 확인
11. aaa 디렉토리 삭제 후 확인
12. 화면 지우기

## [경로]
path

## [역슬래시]
 \\\\\\\\\\

 ## [바]
 |||||||||

 ## 폴더 이동하기
 Unix CLI 를 사용하니 역슬래시가 아닌, 슬래시로 디렉토리 구분<br>
 <br>
 cd 경로/목표 = 목적지로 한번에 이동
 <br>
 <br>
 mkdir aa/bb/cc = aa 안에 bb 안에 cc를 만든다.

 # 자격증 목록
 * 정보처리기사
 * 컴활 1급
 * 네트워크 관리사
 * 리눅스 마스터 1급,2급