# Git Commit

```text
echo "Hello World" > hello.txt

git add hello.txt

git commit -m "Initial commit"
```

* head: special pointer points to the current commit \(when checkout a branch, head points to the current branch\) 
  * very last commit you made
  * current branch

```text
tree .git

git log --oneline

git log --oneline --graph 分支图

git log --oneline <file>

git show <commit id>

git log -p <commit id>

git --no-pager log --oneline
```



