# switch

`git-switch` - Switch branches

## Switch branch
```
# list branches
$ git branch
* main
  newBranch
```

```
# switch to newBranch
$ git switch newBranch

Switched to branch 'newBranch'
```

## Create branch and switch
Use the `-c, --create` flag to create a branch and change to it.

```
$ git switch -c anotherNewBranch

Switched to a new branch 'anotherNewBranch'
```

## Resources
- https://git-scm.com/docs/git-switch
