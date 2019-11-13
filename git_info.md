# git

* (분산)버전 관리 시스템
* 개발자 linus forvalds : 리눅스, git - gis linus Tovalds on git
* 코드의 History를 관리하는 도구
* 개발된 과정과 역사를 볼 수 있으며, 프로젝트의 이전 버전을 복원하고 변경 사항을 비교, 분석 및 병합도 가능
* git을 기반으로(hosting) 한 서비스 : Github(MS에 인수됨), Gitlab, GitKraken, GitBash
* 디렉토리(Directory) 단위로 관리-어떤 폴더에서 git을 생성하는지가 중요cd
* 스냅샷을 찍어주지 않음

## 목록

* 명령어
* bitbucket



## 기본 명령어

* cat [파일 명] : 해당 파일의 문서내용 보기

* cd : 폴더를 들어가거나 나오기
  
  * cd [폴더명] : 해당 폴더로 들어감
  * cd .. : 뒤로가기
  * cd : 홈 디렉토리로 가기
  * cd/ : 루트 디렉토리로 가기
  
* clear : 작성된 내용 삭제

* code [위치] : 원하는 위치에서 mscode를 시작함(mscode 설치되어있을 시)

  * code . : 현재 위치에서 mscode를 실행함

* cp : copy(복사)

  * cp [복사하고자 하는 파일] [저장하고자 하는 폴더] : 파일 복사
  * cp -r [복사하고자 하는 폴더] [복사된 폴더의 이름] : 폴더 복사

* echo

  * echo '[출력하고자 하는 문자열]' : 문자열 출력

  * 변수값 출력

    ```git
    $ [변수명]="[변수값]"
    $ echo $[변수명]
    ```

  * echo '[저장하고자 하는 값]' > [파일명] : 특정 파일을 생성하여 값(문자열)을 저장

    ```git
    echo 'hello' > a.txt
    ```

  * echo '[저장하고자 하는 값]' >> [파일명] : 존재하는 특정 파일에 값(문자열)을 추가

    ```git
    echo 'world' >> a.txt
    ```

* ls : 목록보기(숨김파일 미포함)

  * ls -al : 목록보기(숨김파일 포함)

* man [알아보고자 하는 명령어] : 명령어에대한 설명

* mkdir : 디렉토리 만들기

* mv : 이름변경 또는 이동

  * mv [이동하고자 하는 파일명] [저장하고자 하는 폴더명] : 파일 이동

    ```git
    mv templates/app.py . # templates폴더의 app.py파일을 현재 폴더로 이동
    ```

  * mv *.[확장자명] [폴더명] : [확장자명]에 해당하는 모든 파일을 [폴더명]으로 이동

  * mv * [폴더명] : 현재 폴더에 있는 모든 파일을 [폴더명]으로 이동(issue가 발생하는 파일 제외)

  * mv [변경하려는 파일] [변경하고자 하는 파일 이름] : 파일이름 변경

* pwd : 현재있는 폴더의 주소 출력

* reset : add한 내용을 취소함

* rm : 제거/삭제하기

  * rm -rf [폴더 명] : 폴더 삭제

* start : 파일/디렉토리 열기
  * start [파일명]
  * start [디렉토리명]
  * start . : 현재있는 폴더 열기
  
* touch : 파일 만들기

* tree : 폴더 구조 보기



## git 명령어

* git add [파일/폴더명] : 커밋할 목록에 추가/ 파일이 삭제된 경우 삭제된 내용을 저장
  * git add . : 현재 폴더의 모든 내용을 추가
  * git add --update : 추적하고 있는 파일만 추가
* git branch : 모든 branch 조회
  * git branch [branch명] : branch생성
* git checkout
  * git checkout [branch명] : 원하는 branch로 이동
  * git checkout -- [파일명] : 삭제된 파일 되돌리기
* git commit : 커밋(create a snapshot) 만들기
  * git commit -m "[커밋메세지]" : 커밋메세지 작성
  * git commit --ament -m "[수정된 커밋 메세지]" : 커밋 메세지 수정
* git config : 환경설정
  * git config --global user.email "[이메일]" : 이메일 지정
  * git config --global user.name "[사용자 이름]" : 사용자 이름 지정
  * --global : 전역으로 사용
* git diff : 무엇을 수정했는지 확인
* git init : 현재 폴더 기준으로 버전관리(선언, 초기화)
* git log : 저장소의 commit history를 시간순으로 보여줌
* git merge
  * git merge [합치고자 하는 branch명] : 현재 branch에(기준) 특정 branch를 합치기
* git push : 현재까지의 역사(commits)가 기록되어 있는 곳에 새로 생성한 커밋을 반영하기
  * git push origin master : origin이라는 이름을 가진 master branch에 push함
  * git push origin :test_branch : test_branch라는 이름을 가진 remote branch 삭제
* git remote : 현재 프로젝트에 등록된 리모트 저장소 확인
  * git remote -v : 리모트 저장소의 단축이름과 url확인
  * git remote add [단축이름] [url] : 리모트 저장소 추가
  * git remote update : 원격저장소의 정보를 업데이트(fetch)함
  * git remote remove origin : 주소를(잘못 입력했을 경우) 삭제함
* git rm --cached [파일명] : 추적 중지(add 취소) / 파일은 그대로 보존됨
  * git rm [파일명] : 파일이 삭제된 경우 삭제된 것을 그대로 적용
* git status : 현재상태(버전 등)



## 단축키

* `ctrl` + `l` : clear
* `ctrl` + `c/d` : 원상복귀



### git bash를 통해 업로드하기

1. git clone

(directory : git_practice)

```git
student@M7011 MINGW64 ~/git_practice
$ git clone https://piie@bitbucket.org/piie/bitbucket_test.git
```

```git
Cloning into 'bitbucket_test'...
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (3/3), done.
```

2. cd directory

```git
student@M7011 MINGW64 ~/git_practice
$ cd bitbucket_test/
```

3. README.md 파일을 bitbucket_test에 만들기
4. add

```git
student@M7011 MINGW64 ~/git_practice/bitbucket_test (master)
$ git add README.md
```

5. commit

```git
student@M7011 MINGW64 ~/git_practice/bitbucket_test (master)
$ git commit -m "modify README.md"
```

```git
[master 7c55ad4] modify README.md
 1 file changed, 4 insertions(+), 45 deletions(-)
 rewrite README.md (99%)
```

6. push

```git
student@M7011 MINGW64 ~/git_practice/bitbucket_test (master)
$ git push origin master
```

```git
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 312 bytes | 312.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://bitbucket.org/piie/bitbucket_test.git
   2776e78..7c55ad4  master -> master
```

