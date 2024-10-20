# log

`git-log` - Show commit logs

## Show repository log
```
# Show full repository log:
$ git log

# Show condensed log:
$ git log --oneline

# Show history for a file:
$ git log <file>
$ git log --oneline <file>
```

## Show history for a branch
```
$ git log <branch_name>

# Limit date range:
$ git log --before={2023-03-25} --after={2023-03-18}

# Search commit messages for string for 2+ digits.
# Note: grep here does not supported extended-regexp (e.g., no '\d' or '{2}'):
$ git log --grep='[0-9][0-9]' --oneline
87bf03d (HEAD -> main) Adding 123 file 5
```

### Draw textual graph of commit history
```
$ git log --graph
* 87bf03d (HEAD -> main) Adding 123 file 5
*   4cee47f Merge branch 'feature-c'
|\
| * 7031fb6 (feature-c) Added branch line2
* | 475c427 Added line 2
|/
* 64aa946 (myNewBranch) branch hello

# -p, --patch = show diff (useful when also filtering):
$ git log -p
$ git log -p <hash>

# Show history for a directory:
$ git log myDir/
```

### Show most recent commits
```
# Show 3 most recent commits:
$ git log -3
```

## Resources
- https://git-scm.com/docs/git-log
