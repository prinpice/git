# git

## 목록

* 명령어
* bitbucket



## 기본 명령어

* cd : 폴더를 들어가거나 나오기
  * cd [폴더명] : 해당 폴더로 들어감
  * cd .. : 뒤로가기
  * cd : 홈 디렉토리로 가기
  * cd/ : 루트 디렉토리로 가기
* clear : 작성된 내용 삭제
* ls : 목록보기
* touch : 파일만들기
* mkdir : 디렉토리 만들기
* start : 파일/디렉토리 열기
  * start [파일명]
  * start [디렉토리명]
  * start . : 현재있는 폴더 열기
* rm : 제거/삭제하기
  * rm 
* pwd : 현재있는 폴더의 주소 출력
* reset : add한 내용을 취소함



## 단축키

* `ctrl` + `l` : clear
* 



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

