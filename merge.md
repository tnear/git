# merge

`git-merge` - Join two or more development histories together
https://git-scm.com/docs/git-merge

## Merge a branch into main
```
# First, checkout the branch you want to merge into (the destination branch):
$ git checkout main

# Next, merge the branch into main:
$ git merge myNewBranch
Updating 5323f9b..64aa946
Fast-forward
 hello2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 hello2.txt
```

## Conflicts cause errors
```
$ git merge feature-c
Auto-merging hello.txt
CONFLICT (content): Merge conflict in hello.txt
Automatic merge failed; fix conflicts and then commit the result.

# This modifies the file(s) in question:
hello
<<<<<<< HEAD
main hello!
=======
branch hello!
>>>>>>> feature-c

# First, modify the file and save changes:
$ vi hello.txt

# Show the updated changes:
$ cat hello.txt
hello
branch hello!

# Finally, run "git commit" with no message because this continues previous operation:
$ git commit
[main 4cee47f] Merge branch 'feature-c'

# (Alternative way to continue a merge process):
# $ git merge --continue

# 'Merge branch now appears at top'
$ git log --oneline
4cee47f (HEAD -> main) Merge branch 'feature-c'
7031fb6 (feature-c) Added branch line2
475c427 Added line 2
64aa946 (myNewBranch) branch hello
5323f9b hello
```

## Abort a merge
```
# --abort = abort (cancel) the current conflict resolution process
$ git merge --abort
```

## Merging main into your branch
This step is often needed before git allows a merge.

```bash
git checkout main
git switch main
git pull
git switch featureBranch
git merge main # merge main into your feature branch
```
