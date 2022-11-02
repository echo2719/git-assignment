$
```
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ echo 'a=[]' > main.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git add -A
warning: in the working copy of 'main.py', LF will be replaced by CRLF the next time Git touches it

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git commit -m "add comp"
[master (root-commit) 1c83640] add comp
 1 file changed, 1 insertion(+)
 create mode 100644 main.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ echo "print(a)" >> main.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash
warning: in the working copy of 'main.py', LF will be replaced by CRLF the next time Git touches it
Saved working directory and index state WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash apply
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   main.py

no changes added to commit (use "git add" and/or "git commit -a")

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git add .

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   main.py


112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status --short
M  main.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ echo "print(10,20,30)" >> main.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status --short
MM main.py
```  
  
```
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash show 1 -p
diff --git a/main.py b/main.py
index 5219397..1b0d1fe 100644
--- a/main.py
+++ b/main.py
@@ -1 +1,2 @@
 a=[]
+print(a)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash show -p 1
diff --git a/main.py b/main.py
index 5219397..1b0d1fe 100644
--- a/main.py
+++ b/main.py
@@ -1 +1,2 @@
 a=[]
+print(a)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash show stash@{0} -p
diff --git a/main.py b/main.py
index 5219397..7623551 100644
--- a/main.py
+++ b/main.py
@@ -1 +1,3 @@
 a=[]
+print(a)
+print(10,20,30)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash show stash@{1} -p
diff --git a/main.py b/main.py
index 5219397..1b0d1fe 100644
--- a/main.py
+++ b/main.py
@@ -1 +1,2 @@
 a=[]
+print(a)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash show -p stash@{1}
diff --git a/main.py b/main.py
index 5219397..1b0d1fe 100644
--- a/main.py
+++ b/main.py
@@ -1 +1,2 @@
 a=[]
+print(a)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash apply
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   main.py

no changes added to commit (use "git add" and/or "git commit -a")

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ cat main.py
a=[]
print(a)
print(10,20,30)

```

```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff
diff --git a/main.py b/main.py
index 5219397..7623551 100644
--- a/main.py
+++ b/main.py
@@ -1 +1,3 @@
 a=[]
+print(a)
+print(10,20,30)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff --staged

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff head
diff --git a/main.py b/main.py
index 5219397..7623551 100644
--- a/main.py
+++ b/main.py
@@ -1 +1,3 @@
 a=[]
+print(a)
+print(10,20,30)

```
```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   main.py

no changes added to commit (use "git add" and/or "git commit -a")

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git add -A

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   main.py


112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git commit -m "print list"
[master a966272] print list
 1 file changed, 2 insertions(+)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git log --oneline
a966272 (HEAD -> master) print list
1c83640 add comp
```

```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ touch hello.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ ls
hello.py  main.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hello.py

nothing added to commit but untracked files present (use "git add" to track)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git add hello.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   hello.py

?????????????????????????????????????????????????????????????????????
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git commit -m "create hello.py"
[master 8caf349] create hello.py
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 hello.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git add main.py
warning: in the working copy of 'main.py', LF will be replaced by CRLF the next time Git touches it

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   main.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.py
????????????????????????????????????????????????????????????????????????????????????

6페이지 맨 위까지 임비다

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff head
warning: in the working copy of 'hello.py', LF will be replaced by CRLF the next time Git touches it
diff --git a/hello.py b/hello.py
index e69de29..f7642c5 100644
--- a/hello.py
+++ b/hello.py
@@ -0,0 +1 @@
+print("hellwowowowowowo")
diff --git a/main.py b/main.py
index 7623551..5effff7 100644
--- a/main.py
+++ b/main.py
@@ -1,3 +1,4 @@
 a=[]
 print(a)
 print(10,20,30)
+print("list")

```

## git stash -m "message"
or git stash save "mes"??
```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 1c83640 add comp
stash@{1}: WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash -m 'es un message for stashing'
warning: in the working copy of 'hello.py', LF will be replaced by CRLF the next time Git touches it
Saved working directory and index state On master: es un message for stashing

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: On master: es un message for stashing
stash@{1}: WIP on master: 1c83640 add comp
stash@{2}: WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash pop
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.py
        modified:   main.py

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (853e8a348239e4d6606152a582845ba71d9d66fe)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 1c83640 add comp
stash@{1}: WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash -m 'es un message for stashing'
Saved working directory and index state On master: es un message for stashing

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: On master: es un message for stashing
stash@{1}: WIP on master: 1c83640 add comp
stash@{2}: WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
nothing to commit, working tree clean

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff ehad
fatal: ambiguous argument 'ehad': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff head

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff --staged

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ cat main.py
a=[]
print(a)
print(10,20,30)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: On master: es un message for stashing
stash@{1}: WIP on master: 1c83640 add comp
stash@{2}: WIP on master: 1c83640 add comp

```
## applying
```
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash apply
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.py
        modified:   main.py

no changes added to commit (use "git add" and/or "git commit -a")


112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff
diff --git a/hello.py b/hello.py
index e69de29..f7642c5 100644
--- a/hello.py
+++ b/hello.py
@@ -0,0 +1 @@
+print("hellwowowowowowo")
diff --git a/main.py b/main.py
index 7623551..5effff7 100644
--- a/main.py
+++ b/main.py
@@ -1,3 +1,4 @@
 a=[]
 print(a)
 print(10,20,30)
+print("list")

```

## applying with --index o
```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: On master: es un message for stashing
stash@{1}: WIP on master: 1c83640 add comp
stash@{2}: WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash
Saved working directory and index state WIP on master: 8caf349 create hello.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 8caf349 create hello.py
stash@{1}: On master: es un message for stashing
stash@{2}: WIP on master: 1c83640 add comp
stash@{3}: WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash apply --
--index      --no-...     --no-quiet   --quiet

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash apply --index
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   main.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status --short
 M hello.py  빨강
M  main.py   초록

```
__여태껏 여러면 gui로 봐왔는데 아주 유용하더라ㅏㅏㅏ,,,.__


## git stash -k (--[no-]keep-index)
```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash -h
usage: git stash list [<options>]
   or: git stash show [<options>] [<stash>]
   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash clear
   or: git stash [push [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [-m|--message <message>]
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [<message>]


112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash -k
Saved working directory and index state WIP on master: 8caf349 create hello.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 8caf349 create hello.py
stash@{1}: WIP on master: 8caf349 create hello.py
stash@{2}: On master: es un message for stashing
stash@{3}: WIP on master: 1c83640 add comp
stash@{4}: WIP on master: 1c83640 add comp


112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   main.py
        
이러면 더욱 안되유 안 클린해면 브랜치간 이동을 못하자나
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git diff --staged
diff --git a/main.py b/main.py
index 7623551..5effff7 100644
--- a/main.py
+++ b/main.py
@@ -1,3 +1,4 @@
 a=[]
 print(a)
 print(10,20,30)
+print("list")

SA니 네줄짜리가 들어가있다는 거유

원복
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash apply
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   main.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.py


```

untracked는 기본적으로 복사가 안되유
## 추적 안된 파일을 할라믄
### git stash -u(--include-untracked)
222p 에 보시면 하단부에 git reset '-'soft 앗 오탈자가 있네유
```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ touch wowitsnot_tracked

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   main.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        wowitsnot_tracked




112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash
Saved working directory and index state WIP on master: 8caf349 create hello.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        wowitsnot_tracked

nothing added to commit but untracked files present (use "git add" to track)

아닛 안되잔하

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash -u
Saved working directory and index state WIP on master: 8caf349 create hello.py

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git status
On branch master
nothing to commit, working tree clean

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 8caf349 create hello.py
stash@{1}: WIP on master: 8caf349 create hello.py
stash@{2}: WIP on master: 8caf349 create hello.py
stash@{3}: WIP on master: 8caf349 create hello.py
stash@{4}: On master: es un message for stashing
stash@{5}: WIP on master: 1c83640 add comp
stash@{6}: WIP on master: 1c83640 add comp

와우 잘되네됴


```

## 스테쉬를 브랜치에다가 하기 !!!!

```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash branch sbrch1
Switched to a new branch 'sbrch1'
Already up to date.
On branch sbrch1
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        wowitsnot_tracked

nothing added to commit but untracked files present (use "git add" to track)
Dropped refs/stash@{0} (252e67f56d645b05b878c1cd57d1c5bbfa4d8f37)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (sbrch1)
$ git diff head

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (sbrch1)
$ git diff

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (sbrch1)
$ git diff --staged

all clean?

```


## git stash pop (vs apply(doesnt pop) )

### 최근 동향 : git stash push가 기본으로 되어...
```
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash pop
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.py
        modified:   main.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        wowitsnot_tracked

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (078659f9e2ab374e8c2fcc660d3bc3908693a9e2)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 8caf349 create hello.py
stash@{1}: WIP on master: 8caf349 create hello.py
stash@{2}: On master: es un message for stashing
stash@{3}: WIP on master: 1c83640 add comp
stash@{4}: WIP on master: 1c83640 add comp

필요하려n?

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash show
 hello.py | 1 +
 main.py  | 1 +
 2 files changed, 2 insertions(+)

```

## git stash drop
only drop
```

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 8caf349 create hello.py
stash@{1}: WIP on master: 8caf349 create hello.py
stash@{2}: On master: es un message for stashing
stash@{3}: WIP on master: 1c83640 add comp
stash@{4}: WIP on master: 1c83640 add comp

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash drop
Dropped refs/stash@{0} (3b7f4cccaff0d54be14890bd7433457e57a2cae2)

112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git stash list
stash@{0}: WIP on master: 8caf349 create hello.py
stash@{1}: On master: es un message for stashing
stash@{2}: WIP on master: 1c83640 add comp
stash@{3}: WIP on master: 1c83640 add comp
```

drop by stash num??
```



```

## git stash clear (o shiva)

```



```


## 번외: remove untracked files
```
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git clean wowitsnot_tracked
fatal: clean.requireForce defaults to true and neither -i, -n, nor -f given; refusing to clean
```
### git clean ( __-f__ -n -i )
```
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git clean -f wowitsnot_tracked
Removing wowitsnot_tracked
```
```
...
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        a
        b
        c

no changes added to commit (use "git add" and/or "git commit -a")
```
### -n (?
```
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git clean -n
Would remove a
Would remove b
Would remove c

ok!
```
### -i
```
112@112-32 MINGW64 /d/peef/@PortableGit/9w/stash (master)
$ git clean -i
Would remove the following items:
  a  b  c
*** Commands ***
    1: clean                2: filter by pattern    3: select by numbers
    4: ask each             5: quit                 6: help
What now> 타잎

오~
조금 파고들면 자세하고 친절하게 뭘 삭제할지 정할수이따. 끝.
```
**-i 옵션 리베이스따위를 할때도 통한다!!!! 머야 개편해!!**
