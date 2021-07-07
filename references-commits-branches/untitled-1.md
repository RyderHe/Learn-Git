# References

3 types of Git References:

1. Tags & Annotated Tags: pointer to a commit
2. Branches: pointer of current branch changes as new commits are made
3. HEAD: pointer to the name of the current branch \(can also point to a commit - detached HEAD\)

## Tags

The commit that a tag points doesn't change

* create annotated tag

```text
git tag -a <tag-name> -m <comments>
```

* list all the tags in repo

```text
git tag
```

* list all tags, and what commit they're pointing to

```text
git show-ref --tags
```

* list all the tags pointing at a commit

```text
git tag --points-at <commit>
```

* looking at the tag, or tagged contents

```text
git show <tag-name>
```

## HEAD

* show current head

```text
cat .git/HEAD
```

* show last commit in every branch

```text
git show-ref --heads
```



