# Merging and Fast Forward

## Fast Forward

Fast forward occurs when there are no commits on the base branch that occurred after the feature branch was created.

🔵 &lt;-  🔵 &lt;- 🔵 &lt;- ⚪ &lt;- ⚪ &lt;- ⚪

                        \|                                \|

                    master                    feature



```text
git checkout master

git merge feature
```

🔵 &lt;-  🔵 &lt;- 🔵 &lt;- ⚪ &lt;- ⚪ &lt;- ⚪

                                                        \|

                                                    master, feature

This linear approach may cause a problem: possibly lose track of a feature that was merged back into master. When you working on a feature and merge it back to master, might have trouble to find which commit caused the bug.

## Git Merge --no-ff

retain the history of a merge commit

```text
git checkout master

git merge new_feature --no-ff
```

🔵 &lt;-  🔵 &lt;- 🔵 &lt;- ⚪ &lt;- ⚪ &lt;- ⚪

                        \|                                \|

                        master                   new\_feature

                                      ⚪ &lt;- ⚪ &lt;- ⚪ - new\_feature

                                   ⬇️                    ⬆️

🔵 &lt;-  🔵 &lt;-             🔵     &lt;-            🔴 ..... merge commit

                                                              \|

                                                        master

