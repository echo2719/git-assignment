# 깃 자주쓸만할 것

git init

git add .

git clone existing new
git clone ??/://???

git status

git diff

- --cached see files ready for commit
- asdf
- asdfg

git rm

git commit
git commit -m "asdf"
git commit -am "asdf"
git commit --amend

git revert head  revert changes

git reset --hard head  return to last commit state

git log

git blame 누구?

git merge _branch_
git rebase _branch_
git rebase master branch
git merge, rebase --abort

git rebase merge --continue

git remote -v
git remote add path/url
git fetch
git pull remote branch
git push remote branch
git push remote :branch

git branch

git switch branch
git checkout branch
git branch -d branch

```text
UNDO
List all operations on repository
git reflog

reflog

커밋 수정하기 (이놈은 치트시트로 이동하자)
commit --amend 여러 옵션 가능

git rebase --interactive (-i) head^n

https://stackoverflow.com/questions/134882/undoing-a-git-rebase

..

또 뭐

Discard all local changes in your working directory
git reset --hard HEAD

Discard local changes in a file
git checkout HEAD <file>

Revert a commit (add a new commit with contrary changes)
git revert <commit>

Change the last commit
git commit --amend
Be careful: don't amend a published commit!

Remove from repository but not on disk
git rm --cached <file>
```

.gitignore

git stash
git stash pop
git stash list
git stash drop
