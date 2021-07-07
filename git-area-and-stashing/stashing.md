# Stashing

* save un-committed work
* safe

**Git Stash - Basic Use**:

* stash changes

```text
git stash
```

* list changes 🔥

```text
git stash list
```

* show the contents

```text
git stash show stash@{0}
```

* apply the last stash

```text
git stash apply
```

* apply the specific stash

```text
git stash apply stash@{0}
```

**Git Stash - Keeping Files**:

* keep untracked files

```text
git stash --include-untracked
```

* keep all files \(even files in .gitignore\)

```text
git stash --all
```

**Advanced Stash**:

* name stashes for easy reference 🔥

```text
git stash save "WIP: making progress on foo"
```

* start a new branch from a stash

```text
git stash branch <optional stash name>
```

* grab a single file from a stash

```text
git checkout <stash name> -- <filename>
```

**Advanced Stash - Cleaning the Stash**:

* remove the last stash and applying changes 🔥

```text
git stash pop
```

* remove the last stash 🔥

```text
git stash drop
```

* remove the nth stash

```text
git stash drop stash@{n}
```

* remove all stashes 🔥

```text
git stash clear
```



