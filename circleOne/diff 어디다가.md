```
git diff
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
커밋 vs staging area
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
커밋해고나서 git diff --cached/--staged GR?과 staging area 같아서 안나옴
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
## 3가지의 차이전
그 밑에 그림을 보길 바랍니다 
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
