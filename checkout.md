# checkout

`git-checkout` - Switch branches or restore working tree files

## Checkout branch
```bash
$ git checkout <branch_name>
```

## Checkout older version
```bash
# Assume hello.txt was created with "hello" then appended with "hello2":
$ cat hello.txt
hello
hello2

# Have two changes, want to checkout oldest (bottom):
$ git log --oneline
39e07ac (HEAD -> main) hello2
22f3e1c hello

# Checkout older version by checksum:
$ git checkout 22f3e1c

# Verify older file's contents (i.e., no "hello2" anymore)
$ cat hello.txt
hello

# Get latest version of branch again:
$ git checkout main

# Verify latest version of files:
$ cat hello.txt
hello
hello2
```

## Create branch
Use `-b` to create new branch (and checkout)
```bash
$ git checkout -b myNewBranch
Switched to a new branch 'myNewBranch'

$ git branch  # Verify myNewBranch was created and is active
  main
* myNewBranch
```

## Checking out tags
Checking out a tag puts your repository in a 'detached HEAD' state. See [`git tag`](tag.md) for more information.

```bash
$ git checkout v2.0.0

# undo operation when done
$ git switch -
```

## Resources
- https://git-scm.com/docs/git-checkout
