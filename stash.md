# stash

git-stash - Stash the changes in a dirty working directory away

`git stash` is useful for saving changes locally without committing anything.

## Create stash
Using the `-u` flag is recommended because it includes untracked files.
```
# create stash (this saves changes elsewhere and reverts your changes
git stash -u

# apply the stash. this does not delete the stash
git stash apply
```

## Create stash with name
This is a useful way to identify what a stash contains. Use the `-m` flag to add a message.

```
git stash -u -m 'my stash'
```

## List stashes
`git stash list` lists all stashes. The newest stashes are listed at the top with the lowest index number.
```
$ git stash list
stash@{0}: On main: my third line
stash@{1}: On main: my second line
```

## Apply by index (number)
Use `git stash apply n` where `n` is the index to apply:
```
$ git stash list
stash@{0}: On main: my third line
stash@{1}: On main: my second line

$ git stash apply 1
```

## Resources
- https://git-scm.com/docs/git-stash