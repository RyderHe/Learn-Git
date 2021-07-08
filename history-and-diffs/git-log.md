# Git Log

## git log --since

```text
git log --since="yesterday"

git log --since="2 weeks ago"
```

## git log --follow

```text
git log --name-status --follow -- <file>
```

## git log --grep &lt;regexp&gt;

```text
git log --grep=mail --author=ryder --since=2.weeks
```

## git log diff-filter

```text
git log --diff-filter=R --stat
```

## Referencing Commits

* ^ 
  * no args \[ ^ \] == ^1: the first parent commit
  * ^n: the nth parent commit
* ~ 
  * no args \[~\]: the first commit back, following first parent
  * ~n: n number of commits back, following only 1st parent

