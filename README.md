# git 내용 정리

## 2 Git의 기초

### 2.1 Git 저장소 만들기
다음 두가지 방법으로 Git 저장소 사용 가능
- 로컬 디렉토리 선택해서 적용 (적용할 디렉토리에서 git init)
- clone 해서 사용 (git clone ***url***)

### 2.2 수정하고 저장소에 저장하기
- 파일 상태 확인 (git status)
- 파일 새로 추적 (git add ***file***)
- 변경사항 커밋 (git commit)
- 파일 삭제 (git rm ***file***)
- 파일 이름 변경 (git mv ***file***)

### 2.3 커밋 히스토리 조회하기
- 히스토리 조회하기 (git log)
시간 순으로 출력하고 각 커밋의 SHA-1 체크섬, 저자 이름, 저자 이메일, 커밋한 날짜, 커밋 메시지를 보여준다.
- 다양한 옵션 존재 (ex -p, --stat 등등)

### 2.4 되돌리기
- 완료한 커밋을 수정할때 (git commit --amend)
- unstaged 상태로 만들기 (git reset)
- 수정된 파일 되돌리기 (git checkout -- ***file***)
- 프로젝트 공유할때 (git push ***리모트 저장소 이름, 브랜치 이름***)

### 2.5 리모트 저장소
- 현재 프로젝트에 등록된 리모트 저장소 확인 (git remote)
- 리모트 저장소에서 데이터 가져오기 (git fetch ***remote***)
- 리모트 저장소 이름 바꾸기 (git remote rename)
- 리모트 저장소 삭제하기 (git remote rm)

### 2.6 태그
- 태그 조회하기, 생성하기
- 태크 종류 (lightweight, annotated)

### 2.7 Git Alias
- config 사용하여 각 명령의 alias 쉽게 만들 수 있다.

## 3 Git 브랜치

### 3.1 브랜치란 무엇인가
- 브랜치란 커밋 사이를 가볍게 이동할 수 있는 포인터 같은 것
- 처음 커밋하면 master 브랜치(기본)거 생성된 커밋을 가리킨다.
- 새 브랜치 생성 (git branch ***name***)
- 브랜치 이동하기 (git checkout ***name***)
- git log로 정보 확인 가능

### 3.2 브랜치와 Merge의 기초
- merge의 진행 방식은 다음과 같다.
- 작업 진행 -> 새로운 이슈 처리할 새 branch 생성 -> 새 branch에서 작업 진행 -> 이전 브랜치에서 merge 진행

### 3.3 브랜치 관리
- 브랜치 목록 확인 (git branch)
- -v 사용하면 커밋 메시지 확인가능
- -d 명령으로 삭제 가능

### 3.4 브랜치 워크플로
- 배포한 코드는 master 브랜치에 두고 개발을 진행하거나 안정화하는 브랜치는 추가로 따로 브랜치를 만들어서 관리한다.
- 테스트를 거쳐서 안정적이라 판단하면 해당 브랜치를 master 브랜치와 merge 하는 원리

### 3.5 리모트 브랜치
- 리모트 트래킹 브랜치 일종의 북마크 같은 역할 (로컬에 있지만 임의로 움직일 수 없음)
- 리모트 트래킹 브랜치의 이름은 remote/branch 형식
- git fetch로 서버의 데이터 내려받을 수 있음
- 리모트 트래킹 브랜치를 로컬 브랜치로 checkout하면 자동으로 트래킹 브랜치 만들어짐
- git pull 명령은 fetch 명령 이후에 merge 명령을 실행하는 것일 뿐이다.

### 3.6 Rebase 하기
- 변경된 사항을 patch로 만들고 이를 원래에 다시 적용시키는 방식
- git checkout... -> git rebase... 식으로 실행
- merge와는 달리 히스토리가 깔끔해진다. merge와 기능은 같다.
- 주의) 공개 저장소에 push한 커밋을 rebase 하면 코드가 엉키게 된다.

## 6 GitHub

### 6.1 계정 만들고 설정하기

### 6.2 GitHub 프로젝트에 기여하기
- 프로젝트 fork 하기 (프로젝트를 통째로 복사해준다)
- pull request (push 한 변경 내용을 원래 저장소로 보내는 것)
1.Fork 한 개인 저장소를 로컬에 Clone 한다.
2.무슨 일인지 설명이 되는 이름의 토픽 브랜치를 만든다.
3.코드를 수정한다.
4.잘 고쳤는지 확인한다.
5.토픽 브랜치에 커밋한다.
6.GitHub의 개인 저장소에 토픽 브랜치를 Push 한다.
- pull request는 토론을 통해 결정

### 6.3 GitHub 프로젝트 관리하기

### 6.4 Organization 관리하기

### 6.5 GitHub 스크립팅
- 서비스 (설정하면 누군가 저장소에 push 할 때마다 이메일이 날라감, 다양한 이벤트 처리가능, 보통은 push 할 때 그 데이터를 가지고 한다.)
- 훅 (서비스에 없는 사이트나 외부 서비스와 연동하고 싶을 때 사용, url로 http 페이로드를 보내줌)
- API (API에 연결하면 이슈에 코멘트하고, pull request의 상태 변경 등 가능)


# docker 내용 정리

## 1 시스템과 인프라 기초 지식

### 1.1 시스템 기반의 기초 지식
- 시스템 기반의 구성 요소
  + 기능 요구사항

### 1.2 하드웨어와 네트워크 기초 지식
### 1.3 OS 기초 지식
### 1.4 미들웨어 기초 지식
### 1.5 인프라 구성 관리 기초 지식

## 2 컨테이너 기술과 Docker의 개요
### 2.1 컨테이너 기술의 개요
### 2.2 Docker의 개요
### 2.3 Docker의 기능
### 2.4 Docker의 작동 구조

## 3 Docker 설치와 튜토리얼
### 3.1 Docker 설치와 작동 확인
### 3.2 웹 서버를 작동시켜 보자

## 4 Docker 명령
### 4.1 Docker 이미지 조작
### 4.2 Docker 컨테이너 생성/시작/정지
### 4.3 Docker 컨테이너 네트워크
### 4.4 가동 중인 Docker 컨테이너 조작
### 4.5 Docker 이미지 생성

## 5 Dockerfile을 사용한 코드에 의한 서버 구축
### 5.1 Dockerfile을 사용한 구성 관리
### 5.2 Dockerfile의 빌드와 이미지 레이어
### 5.3 멀티스테이지 빌드를 사용한 애플리케이션 개발
### 5.4 명령 및 데몬 실행
### 5.5 환경 및 네트워크 설정
### 5.6 파일 설정

## 6 Docker 이미지 공개
### 6.1 Docker 이미지의 자동 생성 및 공개
### 6.2 Docker Registry를 사용한 프라이빗 레지스트리 구축
### 6.3 클라우드 서비스를 사용한 프라이빗 레지스트리 구축

## 7 여러 컨테이너의 운용 관리
### 7.1 여러 컨테이너 관리의 개요
### 7.2 웹 애플리케이션을 로컬에서 움직여 보자
### 7.3 Docker Compose를 사용한 여러 컨테이너의 구성 관리
### 7.4 Docker Compose를 사용한 여러 컨테이너의 운용
