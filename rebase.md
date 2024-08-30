# rebase

`git-rebase` - Reapply commits on top of another base tip

`git rebase` is useful for updating your changes when the `main` branch is updated by someone else. It follows these three high-level steps:

1. Takes your changes and sets them aside temporarily
1. Fast forward: updates your branch to match the current state of the main branch
1. Replay your changes. It applies your changes on top of the updated branch, one by one.

Rebase should be done before pushing changes.

## Basic usage
Perform `rebase` on current branch:
```
git rebase
```

## Rebase specific branch
```
git rebase <branch>
# ex:
git rebase origin/main
```

Specifying `origin` can potentially pick up newer changes than are saved locally in your repository.

## `--continue`
Use `git rebase --continue` after resolving conflicts to continue the `rebase` process.

To undo everything, run `git rebase --abort`.

## Resources
- https://git-scm.com/docs/git-rebase
