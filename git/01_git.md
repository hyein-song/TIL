# git 기초 명령어

> 분산버전관리시스템(DVCS)

## 0. 로컬 저장소(repository) 설정

```bash
$ git init
# 초기화 되었다..
Initialized empty Git repository in C:/Users/shi95/OneDrive/바탕 화면/practice/.git/
(master) $
```

* `.git` 폴더가 생성되고, 여기에 모든 git과 관력된 정보들이 저장된다. (최초에 한번만)

## 기본 작업 흐름

> 모든 작업은 touch로 파일을 만드느것으로 대체

### 1. add

```bash
$ git add. #.:현재 디렉토리
$ git add a.txt # 특정 파일
$ git add my_folder #특정 폴더
$ git add a.txt b.txt #복수의 파일
```

* working dirextory 의 변경사항(첫번째 통)을 staging area(두번째 통) 상태로 변경 시킨다.
* 커밋의 대상 파일을 관리한다.

```bash
$ touch a.txt
$ git status
On branch master

No commits yet
#트래킹이 되고 있지 않는 파일들..
# ==> 새로 생성된 파일
Untracked files:
	# add 명령을 사용해!
	#커밋이 퇼 것에 포함 시키기 위하여..
	# => Staging Area(두번째 통)
  (use "git add <file>..." to include in what will be committed)
        a.txt

nothing added to commit but untracked files present (use "git add" to track)
```

* add 이후

```bash
$ git add .
$ git status
On branch master

No commits yet

#커밋이 될 변경사항
#SA 두번째 통에 있는 애들..
Changes to be committed:

  (use "git rm --cached <file>..." to unstage)
        new file:   a.txt
```



### 2. commit

```bash
$ git commit -m 'First commit'
[master (root-commit) 2e4f7aa] First commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.txt
```

* `commit`은 지금 상태를 스냅샷을 찍는것
* 커밋 메시지는 지금 기록하는 이력을 충분히 잘 나타낼 수 있도록 작성한다.
* `git log` 명령어를 통해 지금까지 기록된 커밋들을 확인할 수 있다.

## 기타 명령어

### 1. status

```bash
$ git status
```



## 2. log

> 커밋 히스토리

```bash
$ git log #로그
commit 2e4f7aaff8b272c4ed43c0baf7abff03d9e194d0 (HEAD -> master)
Author: song <shi9512@naver.com>
Date:   Tue Dec 29 14:11:19 2020 +0900

    First commit

$ git log --oneline #하나의 로그를 한줄로
2e4f7aa (HEAD -> master) First commit

$ git log -1 

$ git log --oneline -1
```

