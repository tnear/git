# pull

`git-pull` - Fetch from and integrate with another repository or a local branch

`git pull` incorporates changes from a remote repository into the current branch. `git pull` runs git fetch with the given parameters and then depending on configuration options or command line flags, will call either git rebase or git merge to reconcile diverging branches.

## Pull with rebase (recommended to try first)
This will set aside your changes, rebase with a branch, then replay your changes. This is similar to a regular [rebase](rebase.md). If someone else has committed to your branch, this helps to retain a cleaner, linear history.

```bash
$ git pull --rebase
```

## Regular pull
```bash
$ git pull
```

### Conflict
If there is a conflict, run `git rebase --abort`. Then, do a regular `git pull`.

## Autostash
Autostash will stash your changes, run `git pull`, then apply your stash.

```bash
git pull --rebase --autostash
```

## Resources
- https://git-scm.com/docs/git-pull
- https://youtu.be/xN1-2p06Urc
