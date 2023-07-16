- API : Application Programming Interface

  다른 프로그램끼리 데이터를 주고받거나 서비스를 호출하는 등의 작업을 수행할 수 있도록 프로그래밍 된 방법을 제공한다.

  쉽게 말하면 리모컨과 같은 것. 내부에서 어떻게 동작하는 지는 잘 모르지만, 역할은 아는 것.

- CLI : Command Line Interface

  명령어를 통해 사용자와 컴퓨터가 상호 작용하는 방식

- GUI : Graphic User Interface

  그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식.



### GIT

분산 버전 관리 시스템

Working Directory(작업 공간) / Staging Area(임시 공간) / Repository(외부 컴퓨터)



- 명령어

cd 이동, 폴더 변경(change directory)

tap 자동 완성

방향키 윗키 : 최근 명령어

rm -r 파일/폴더 이름 : 삭제

add 내 컴퓨터에서 임시 공간으로 추가한다.

commit 추가한 것에다가 변경사항 또는 메모를 추가한다.

push :임시 공간에 있는 것을 외부 컴퓨터로 보낸다.

pull 외부 컴퓨터에서 내 컴퓨터로 가져온다.(변경사항만 가져옴)

touch  파일 생성

touch 파일명.txt : txt파일 생성

(https://rheem-hm.tistory.com/11 참고)



- git 관련 명령어

git clone : 복제

git status 상태 확인

git log commit 확인

git init : git 디렉토리 생성

git remote add origin 레포지토리 주소 추가

*(origin : 별칭, 꼭 오리진이라고 안해도 되지만 푸시할 때 명령어 맞춰줘야 한다)*

git remote remove origin : origin 삭제

*(파일명이나 폴더명 띄어쓰기 사용 시 ' ' 로 사용)*



- Git 설정

git config --global user.email "이메일 주소"

git config --global user.name "이름"



- Github에 파일 올리기

  1) Github에서 레포지토리 생성
  2) 바탕화면에 폴더 생성
  3) git bash에서 폴더로 이동 후 git init
  4) 파일 생성
  5) git add 파일명(전부 올릴 때는 '.' 사용)
  6) git commit -m "커밋 내용"
  7) git remote add origin 레포지토리 주소
  8) git push -u origin master/main

  이후 해당 레포지토리에 파일을 올릴 때는 add, commit, push만 하면 된다.

  

- Pull Requset

  자신의 branch를 가져가 검토 후 병함해 달라는 요청

  pr이라고 하기도 한다.



- git ignore

  push 하지 않을 파일 선택(개인 정보, 용량이 큰 파일 등)

  https://www.toptal.com/developers/gitignore : git ignore만들어주는 사이





### Branch

바로 본 서버에 적용할 수 없기 때문에, 평행세계처럼 만들어서 사용하는 것.



- 브랜치 종류

dev 개발 브랜치  / feature 기능 브랜치(기능 하나를 개발하기 위해) / hotfix 긴급 개발 브랜치



- 브랜치 관련 명령어

git branch 브랜치명 : 브랜치 생성

git checkout 브랜치명 : 브랜치 이동

git branch : 브랜치 확인, 자기 현재 위치

(브랜치에서 처음 푸시할 때도 git push -u origin 브랜치명)



----

#### 기타 메모

- 백틱 : "`"

- const : 초기 할당 이후 변경되지 않는 변수

- string : 문자열

- boolean : 참거짓

- for 문

```python
for x in familly
family의 각 항목 x에 대하여
```

- +=, -=, *=

```python
i += 1  #i = i+1
i -= 1  #i = i-1
i *= 2  #i = i*2
```

- 파이썬의 첫 값은 0부터 시작한다.

- 입력

```python
int(input()) #정수형 입력
float(input()) #실수형 입력
```

- 마크다운(확장자 .md) 

  코드를 넣을 때는 백틱 3개를 넣고 쓴다.

- GitHub에 이미지 삽입

  1. 올리려고 하는 Repository에 들어가서 issues 탭 > new issue > 이미지 드래그 앤 드랍

  2. 시간 지나면 url생김

  3. 변환된 텍스트 파일 복사 붙여넣기

  4. 원하는 md파일에 넣기.