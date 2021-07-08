# Merge Conflicts

Attempt to merge, but files have diverged.

Git stops until the conflicts are resolved.

## Git RERERE - REUSE RECORDED RESOLUTION

* Trun it on:
  1. git config rerere.enabled true
  2. use --global flag to enable for all projects

```text
git config rerere.enabled true

git checkout master

git merge feature
// conflict: merge conflict in file

git rerere diff
// see conflicts

// sloving conflict .....

git add file
git commit -m "Resolve conflict"
# recorded resolution
# next time the same conflict shows up, it will be matched (auto reapplied)
```



