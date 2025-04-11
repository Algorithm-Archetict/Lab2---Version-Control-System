# Lab2---Version-Control-System

### To delete the 2 created branches locally (dev , test):
git branch -d dev
git branch -d test

### To delete the 2 created branches remotely (dev , test):
git push origin --delete main
git push origin --delete test


### Leightweght Tag vs. Annotated Tag
- Each of both is a references to commit
- Annotated Tag also contains metadata (tagger (his username and his password), date, message)


### When to use rebase over merge
-  both rebase and merge are used to integrate changes from one branch into another.
-  Rebase is prefered in these cases:
  1. To maintain a clean and linear commit history: Rebase moves your feature branch commits onto the tip of the target branch (e.g., main). This results in a history without extra merge commits, making it easier to follow the sequence of changes and understand when each change was introduced relative to the main codebase.
  2. When working on a local feature branch that hasn't been shared with others: Since rebase rewrites history, it's generally safe to do on my private branches. Rewriting history on shared branches can cause significant problems for collaborators.
  3. To clean up your local commits before sharing: You can use interactive rebase (git rebase -i) to squash multiple small commits into a single logical commit, reorder commits, or edit commit messages, resulting in a more understandable and well-organized contribution.
  4. To resolve conflicts on a commit-by-commit basis: When rebasing, if conflicts arise, you resolve them for each commit being replayed. This can sometimes make complex conflicts easier to manage as you deal with smaller, incremental changes.


### How to list tags ?
- git tag


### How to delete tag locally ?
- git tag --d v1.7

### How to delete tag remotely ?
- git push origin --delete v1.7


