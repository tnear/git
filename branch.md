# branch

`git-branch` - List, create, or delete branches

See also: [git switch](switch.md).

## Show branches (no flags)
The `*` symbol indicates the current branch.
```bash
$ git branch
* main
  myNewBranch
```

## Create branch
```bash
$ git branch myNewBranch
```

## Switch to branch
```bash
$ git checkout myNewBranch
# or
$ git switch myNewBranch
```

## Delete branch
Use the `-d` flag to delete a branch (`-D` forces).

```bash
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
```bash
$ git branch -v
* main 33bed56 push (-f), rebase, stash (apply index)
```

## Show all repositories
Use `-a` to show all repositories, including ones which have not been checked out.
```bash
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/experimental
```

## List all remote branches
Use `-r, --remotes` to list all remote branches.
```bash
$ git branch --remotes
  origin/HEAD -> origin/master
  origin/master
  origin/user1/dev
  origin/user2/bug_fix
```

You can checkout a remote branch using `git checkout origin/user1/dev`.

## Resources
- https://git-scm.com/docs/git-branch
