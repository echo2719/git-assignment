diff와 체크아웃 4페이지에 명령어 설명이 잘 되어있다.

pdf와 하몎 보는걸

```
git diff
```

Working directory와 staging area 사이의 차이

```
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))

```

```
디프 --깃 스테이징(a) 디렉(b)
인덱스???..??? 권한
(스테이징) dtype파이
(working directory) dtype파이

+추가된곳
```

파일끝에뉴라인안하면  No newline at end of file 빼액 한다

```
git diff --cached
```

?git repo vs staging area
커밋?

```
diff --git a/dtype.py b/dtype.py
new file mode 100644
index 0000000..c32d8d7
--- /dev/null
+++ b/dtype.py
@@ -0,0 +1 @@
+print("python")

```

```
커밋 안해서 0000000..
/dev/null
```

git add하고 diff하면 아무것도 안나옵니다
커밋해고나서 git diff --cached/--staged git repository와 staging area 같아서 안나옴

```
git diff HEAD
```

HEAD vs working directory

```
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))


```

## 지금 3가지의 차이전

그 밑에 그림을 보길 바랍니다
head vs working directory

```
$ git diff HEAD
diff --git a/dtype.py b/dtype.py
index c32d8d7..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,3 @@
 print("python")
+print(list('python'))
+print({i:ord(i) for i in 'python'})
```

staging area vs working directory

```
$ git diff --cached
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))
```

```
$ git diff
diff --git a/dtype.py b/dtype.py
index 61a6d40..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1,3 @@
 print("python")
 print(list('python'))
+print({i:ord(i) for i in 'python'})

```

### 추가

```
git diff HEAD^ / HEAD~ 
```

이전 커밋
...여러분 책에는 자세히 안나와요 그래서 보면은 128쪽에 4-10절에 나와요 diff 명령어가 그러나 여기선 2,3줄로 간단하...

```
git diff head head~
```

앗 너무 혼란스러워요!

```
diff --git a/dtype.py b/dtype.py
index 61a6d40..c32d8d7 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1 @@
 print("python")
-print(list('python'))
```

```
git diff head~ head
```

```
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))


```

## 다시 3가지 차이

```
git repository(HEAD)
print('python')
print(list('python'))

staging area
print('python')
print(list('python'))
print({i:ord(i) for i in 'python'})

working directory
print('python')
print(list('python'))
print({i:ord(i) for i in 'python'})
print({i for i in range(5)})

```

전에 썼던 working tree는 working directory와 같은 말 앗 용어통일안함

0그림과 함꼐 7주diff.pdf 보자
소스트리로 보는건 pdf
GUI툴은 이러이러한 좋은 점이 이써요 손으로 옮길수이싸여

##### detatched head state

브랜치의 마지막 커밋을 가기켜야하느느디 헤드를 옮기면 디테치트해드스테이트가 되낟.브랜치가 커밋아이디로나오죠
다시원복을로하면 main으로다시오시면되어요

디태치드헤드인상태에서git log하면 현재 head이전만 나와요

디태치드헤드에서는 시간여행을 할수이써요
