# rebase

`git-rebase` - Reapply commits on top of another base tip

See also: [`merge-base`](merge-base.md)

## Overview

`git rebase` is useful for updating your changes when the `main` branch is updated by someone else. It follows these high-level steps:

1. Takes your changes and sets them aside temporarily
1. Fast forward: updates your branch to match the current state of the main branch
1. Replay your changes. It applies your changes on top of the updated branch, one by one.

Rebase should be done after committing but before pushing changes.

## Rebase main on top of your feature branch
```bash
git switch feature_branch
git rebase main  # or git rebase origin/main
# <resolve conflicts>
git add <file_with_fixed_conflict>
git rebase --continue  # continue after resolving conflict
# <finish conflicts>
git status  # will indicate if rebasing is done
git push --force-with-lease # push changes when rebase is done
```

Specifying `origin` can potentially pick up newer changes than are saved locally in your repository.

### Alt syntax when above doesn't work
```bash
git fetch origin
git rebase origin/master
git push -f origin HEAD    # force push your rebased branch
```

## `--abort`
To undo/cancel everything, run `git rebase --abort`.

## Interactive
Use `-i, --interactive` to make a list of commits to rebase.

```bash
# list the last 4 commits
$ git rebase -i HEAD~4

# choose pick/drop for each of the 4 (oldest on top)
pick abc1234 Commit message 1
pick def5678 Commit message 2  <- Change to 'pick' to 'drop' to remove
pick ghi9012 Commit message 3  <- Change to 'pick' to 'drop' to remove
pick jkl3456 Commit message 4
```

### Squashing commits

```bash
# Find where you branched
git merge-base main HEAD

# Rebase from that point
git rebase -i $(git merge-base main HEAD)

# mark all commits except the first as 'squash'

# force push to rewrite history
git push --force-with-lease
```

## Resources
- https://git-scm.com/docs/git-rebase
- https://youtu.be/DkWDHzmMvyg?t=358
