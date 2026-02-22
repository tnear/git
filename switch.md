# switch

`git-switch` - Switch branches

See also: [`branch`](branch.md)

## Switch branch
```bash
# list branches
$ git branch
* main
  newBranch
```

```bash
# switch to newBranch
$ git switch newBranch

Switched to branch 'newBranch'
```

## Create branch and switch
Use the `-c, --create` flag to create a branch and change to it.

```bash
$ git switch -c anotherNewBranch

Switched to a new branch 'anotherNewBranch'
```

## Switch to previous branch
Use `git switch -`. Inspired by bash, `cd -`.

## Resources
- https://git-scm.com/docs/git-switch
