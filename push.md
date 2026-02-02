# push

`git-push` - Update remote refs along with associated objects

Uploads local changes to remote repository.

## Basic usage
```bash
$ git push

Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 1.06 KiB | 1.06 MiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/tnear/git.git
   9208377..cb24eb1  main -> main
```

## Upload to branch
```bash
$ git push origin <branch_name>
```

## Force pushing
### `-f, --force` (not recommended)
Allows overwriting the remote branch with your local branch, even if they have diverged.

```bash
git push -f origin myBranch
```

### `--force-with-lease` (recommended)
This flag allows force pushing changes to a remote branch, but only if the remote branch is in the state you expect. This prevents accidental overwriting of changes made by others.

It can be useful after [rebasing](rebase.md).

```bash
git push --force-with-lease
```

## Delete a branch
Deleting a branch requires a `git push` to update the remote repository.

```bash
# First, switch away from branch to be deleted (branchToDelete)
$ git checkout main

# Next, delete branch 'branchToDelete' using -d flag
$ git branch -d branchToDelete
Deleted branch branchToDelete (was af242cb).

# Lastly, push the deletion to the remote repository
$ git push origin -delete branchToDelete
```

## Resources
- https://git-scm.com/docs/git-push
