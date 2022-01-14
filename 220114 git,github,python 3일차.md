# 3일차 수업!
## 2일차 리뷰
* 4단계로 된 구조
    * 작업폴더<br>
    ->add->
    * staging area(커밋 대기실)<br>
    ->commit->
    * 로컬 repo.<br>
    ->push->
    * remote repo.


## 3일차!
### GIT 프로그램에 내 정보 기입하기
-Git config --global user.name "내 이름"<br>
-git config --global user.email "이메일 주소"<br>
-git config --global --list

* 시작하기전 리눅스 상식!<br>
Linux 에서는 파일 또는 디렉토리 이름이 . 으로 시작되면 숨김파일을 의미한다!
    * .test라는 파일생성
    * ls 로 결과 확인했지만, 숨겨져서 안나왔다.
<br>
<br>
* 숨김파일까지 보는 방법은?<br>
    * ls -a

* 현재 작업디렉토리를 local repo로 만들자!<br>
    * git init 이라고 입력
* 자동으로 만들어진 디렉토리<br>
.git이라는 디렉토리가 만들어졌다<br>
HEAD  config  description  hooks/  info/  objects/  refs/
라는 내용물들이 들어있다<br>

* 로컬 레포가 만들어졌다.<br>
Work 디렉토리에서 code 띄고 . 입력하자(code .)
    * vscode가 실행되면서 새로 팝업

### 작업폴더를 local repo 등록 방법
1. work 작업 폴더 만들고 만든 작업 폴더를 local repo. 등록
2. 클론 하면... local repo에 작업 폴더가 자동으로 생성

* git add .<br>
작업 디렉토리에 있는 모든 파일들을 staging area에 등록한다.

* git status<br>
작업 폴더와 staging area에 있는 파일들의 상태를 알려주는 명령어
    * 단 한번이라도, staging에 올렸던 적이 있는 파일들은 status 명령어로 상태 변화를 확인 할 수 있음.

* 이제 commit 을 하자!<br>
staging area에 올라간 파일들을 commit 할 수 있다!<br>
    * 명령어<br>
    git commit -m "신규 파일 추가함"

* Clone 으로 local repo. 만들기<br>
    * git hub에서 주소 복사해두기
    * 작업디렉토리 준비
    * git clone 명령어<br>
    clone 후 그 안에 repo이름으로 폴더가 만들어지고 이 폴더가 local repo.가 된다.
        * 이 폴더 안에는 .git이라는 숨겨진 파일이 있음<br>
* 클론한 내용을 수정 add commit push 하기
    * code . 입력으로 vscode 실행
    * 자격 증명 삭제<br>
    이미 연동이 되있어서 일단 끊고 cli로 해보자
    * git add .<br>
    git status<br>
    git commit -m "메세지"<br>
    * git remote -v<br>
    클론 받았기 때문에 local repo.에 remote repo. 설정이 다 되있음<br><br>
    git remote -v 입력하면 remote repo.가 등록된 것이 보임
    * git push<br>
    로그인 창 뜨고 로그인 하면 푸시댐!

# https://git-scm.com/book/ko/v2/ 나중에 깃 기억안나거나 할때 찾아볼 페이지!