# References

3 types of Git References:

1. Tags & Annotated Tags: pointer to a commit
2. Branches: pointer of current branch changes as new commits are made
3. HEAD: pointer to the name of the current branch \(can also point to a commit - detached HEAD\)

## Tags

{% hint style="info" %}
**git tag &lt;tag name&gt;** 默认把tag加到最新commit

**git tag &lt;tag name&gt; &lt;commit id&gt;** 加到指定commit

git tag 查看所有tag

git log 查看tag对应commit

**git tag -d &lt;tag name&gt;** 删除tag

**git push origin &lt;tag name&gt;** 推送tag至远程仓库
{% endhint %}



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



