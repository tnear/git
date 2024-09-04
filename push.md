# push

`git-push` - Update remote refs along with associated objects

Uploads local changes to remote repository.

## Basic usage
```
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
```
$ git push origin <branch_name>
```

## `-f, --force`
Allows overwriting the remote branch with your local branch, even if they have diverged.

```
git push -f origin myBranch
```

## Delete a branch
Deleting a branch requires a `git push` to update the remote repository.

```
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
