```
112@112-32 MINGW64 /d/peef/@PortableGit/7w
$ git init gdiff
Initialized empty Git repository in D:/peef/@PortableGit/7w/gdiff/.git/

112@112-32 MINGW64 /d/peef/@PortableGit/7w
$ cd gdiff/

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff
$ git status
fatal: detected dubious ownership in repository at 'D:/peef/@PortableGit/7w/gdiff'
To add an exception for this directory, call:

        git config --global --add safe.directory D:/peef/@PortableGit/7w/gdiff

Set the environment variable GIT_TEST_DEBUG_UNSAFE_DIRECTORIES=true and run
again for more information.

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff
$  git config --global --add safe.directory D:/peef/@PortableGit/7w/gdiff

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ ls

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ touch dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        dtype.py

nothing added to commit but untracked files present (use "git add" to track)

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git status --
--ahead-behind        --long                --short
--branch              --no-...              --show-stash
--column              --no-renames          --untracked-files
--find-renames        --null                --verbose
--ignore-submodules   --porcelain
--ignored             --renames

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git status --short
?? dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ code ~/.gitconfig

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.s status

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        dtype.py

nothing added to commit but untracked files present (use "git add" to track)

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.ss status -s

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        dtype.py

nothing added to commit but untracked files present (use "git add" to track)

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.ss status --short

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        dtype.py

nothing added to commit but untracked files present (use "git add" to track)

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.ss "status -s"
warning: alias.ss has multiple values
error: cannot overwrite multiple values with a single value
       Use a regexp, --add or --replace-all to change alias.ss.

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.ss 'status -s'
warning: alias.ss has multiple values
error: cannot overwrite multiple values with a single value
       Use a regexp, --add or --replace-all to change alias.ss.

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.ss --replace-all 'status -s'

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
unknown option: --replace-all
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global --replace-all alias.ss 'status -s'

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
?? dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global core.editor 'code --wait'

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ ls
dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ cat dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ code dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        dtype.py

nothing added to commit but untracked files present (use "git add" to track)

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ cat dtype.py
print("python")
112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ code dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ cat dtype.py
print("python")

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ code dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        dtype.py

nothing added to commit but untracked files present (use "git add" to track)

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
?? dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git add .

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   dtype.py


112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
A  dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   dtype.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   dtype.py


112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
AM dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff --cached
diff --git a/dtype.py b/dtype.py
new file mode 100644
index 0000000..c32d8d7
--- /dev/null
+++ b/dtype.py
@@ -0,0 +1 @@
+print("python")

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff HEAD
fatal: ambiguous argument 'HEAD': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git log
fatal: your current branch 'main' does not have any commits yet

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git commit -m "add string type"
[main (root-commit) adf5297] add string type
 1 file changed, 1 insertion(+)
 create mode 100644 dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
 M dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   dtype.py

no changes added to commit (use "git add" and/or "git commit -a")

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
 M dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git log --oneline
adf5297 (HEAD -> main) add string type

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff HEAD
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ ^C

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.
alias.

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.lgg1
.git/     dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git config --global alias.lgg1 'log --oneline --graph'

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git lgg12
git: 'lgg12' is not a git command. See 'git --help'.

The most similar command is
        lgg1

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git lgg1
* adf5297 (HEAD -> main) add string type

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff HEAD
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff --cached

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
 M dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   dtype.py

no changes added to commit (use "git add" and/or "git commit -a")

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git add .

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   dtype.py


112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
M  dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   dtype.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   dtype.py


112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
MM dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git dif
git: 'dif' is not a git command. See 'git --help'.

The most similar commands are
        diff
        config
        difftool
        init

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff
diff --git a/dtype.py b/dtype.py
index 61a6d40..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1,3 @@
 print("python")
 print(list('python'))
+print({i:ord(i) for i in 'python'})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff HEAd
diff --git a/dtype.py b/dtype.py
index c32d8d7..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,3 @@
 print("python")
+print(list('python'))
+print({i:ord(i) for i in 'python'})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff HEAD
diff --git a/dtype.py b/dtype.py
index c32d8d7..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,3 @@
 print("python")
+print(list('python'))
+print({i:ord(i) for i in 'python'})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff --cached
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff
diff --git a/dtype.py b/dtype.py
index 61a6d40..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1,3 @@
 print("python")
 print(list('python'))
+print({i:ord(i) for i in 'python'})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   dtype.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   dtype.py


112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
MM dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git commit -m 'add list tyle'
[main caf3c04] add list tyle
 1 file changed, 1 insertion(+)

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   dtype.py

no changes added to commit (use "git add" and/or "git commit -a")

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
 M dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git log
commit caf3c0422267f1f7fa27dd0be749fc4a6e185746 (HEAD -> main)
Author: echo2719 <echo2719@dongyang.ac.kr>
Date:   Wed Oct 19 15:07:35 2022 +0900

    add list tyle

commit adf52979e8851f040ffed50282e8ba647d3ad9ce
Author: echo2719 <echo2719@dongyang.ac.kr>
Date:   Wed Oct 19 14:38:56 2022 +0900

    add string type

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git log1
git: 'log1' is not a git command. See 'git --help'.

The most similar command is
        lgg1

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git lgg1
* caf3c04 (HEAD -> main) add list tyle
* adf5297 add string type

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff head head~
diff --git a/dtype.py b/dtype.py
index 61a6d40..c32d8d7 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1 @@
 print("python")
-print(list('python'))

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff head~ head
diff --git a/dtype.py b/dtype.py
index c32d8d7..61a6d40 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,2 @@
 print("python")
+print(list('python'))

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ ^C

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   dtype.py

no changes added to commit (use "git add" and/or "git commit -a")

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git add dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   dtype.py


112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
M  dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git s
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   dtype.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   dtype.py


112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git ss
MM dtype.py

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff --cached
diff --git a/dtype.py b/dtype.py
index 61a6d40..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1,3 @@
 print("python")
 print(list('python'))
+print({i:ord(i) for i in 'python'})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff head
diff --git a/dtype.py b/dtype.py
index 61a6d40..3606911 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1,4 @@
 print("python")
 print(list('python'))
+print({i:ord(i) for i in 'python'})
+print({i for i in range(5)})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff --cached head
diff --git a/dtype.py b/dtype.py
index 61a6d40..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1,3 @@
 print("python")
 print(list('python'))
+print({i:ord(i) for i in 'python'})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff --cached head~
diff --git a/dtype.py b/dtype.py
index c32d8d7..8fca451 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,3 @@
 print("python")
+print(list('python'))
+print({i:ord(i) for i in 'python'})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff head
diff --git a/dtype.py b/dtype.py
index 61a6d40..3606911 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1,2 +1,4 @@
 print("python")
 print(list('python'))
+print({i:ord(i) for i in 'python'})
+print({i for i in range(5)})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$ git diff head~
diff --git a/dtype.py b/dtype.py
index c32d8d7..3606911 100644
--- a/dtype.py
+++ b/dtype.py
@@ -1 +1,4 @@
 print("python")
+print(list('python'))
+print({i:ord(i) for i in 'python'})
+print({i for i in range(5)})

112@112-32 MINGW64 /d/peef/@PortableGit/7w/gdiff (main)
$

```
