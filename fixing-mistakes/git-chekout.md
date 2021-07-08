---
description: Restore working tree files or switch branches
---

# Git Chekout

* 假设错误的更改还没有被add 进staging area， 仍然停留在working area：

输入以下指令可一键还原 &lt;file&gt; 到上一次staging area的状态

```text
git checkout -- <file>
```

* 假设错误的更改已经被add 进staging area:

此时, git status 查看可看到变化已经被追踪了\(绿色\)，直接输入 git checkout -- &lt;file&gt; 并不能一键还原。

所以，首先要撤销追踪: git status 变回红色

```text
git reset HEAD <file>
```

再输入

```text
git checkout -- <file>
```

* 所有文件回到指定commit 版本

master branch: version1  version2  version3  version4  version5&lt;- HEAD

```text
git reset --hard <commit id>

git reset --hard HEAD^                    回到上一个版本 - version5 -> version4
 
git reset --hard HEAD^^                   回到上2个版本 - version5 -> version3
```

* 指定文件回到指定commit 版本

```text
git checkout <commit id> -- <file>
```

