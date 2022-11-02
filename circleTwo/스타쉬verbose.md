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

```

```



```
