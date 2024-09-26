# branch

`git-branch` - List, create, or delete branches

## Show branches (no flags)
The '*' symbol indicates the current branch.
```
$ git branch
* main
  myNewBranch
```

## Create branch
```
$ git branch myNewBranch
```

## Switch to branch
```
$ git checkout myNewBranch
# or
$ git switch myNewBranch
```

## Delete branch
Use the `-d` flag to delete a branch (`-D` forces).

```
# First, switch away from branch to be deleted (branchToDelete)
$ git checkout main

# Next, delete branch 'branchToDelete' using -d flag
$ git branch -d branchToDelete
Deleted branch branchToDelete (was af242cb).

# Lastly, push the deletion to the remote repository
$ git push origin --delete branchToDelete
```

## Verbose output
Use `-v, --verbose` for verbose output.
```
$ git branch -v                                                 
* main 33bed56 push (-f), rebase, stash (apply index)
```

## Show all repositories
Use `-a` to show all repositories, including ones which have not been checked out.
```
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/experimental
```

## Resources
- https://git-scm.com/docs/git-branch
