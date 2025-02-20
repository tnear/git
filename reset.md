# reset

`git-reset` - Reset current HEAD to the specified state

## Unstage all files
Use `git reset` to unstage all files. This command is safe and no data is lost.
```
$ git reset
Unstaged changes after reset:
M       hello.txt
M       hello2.txt
```

## Revert all modified files (warning: loses changes)
```bash
$ git reset --hard
$ git reset --hard origin/main # reset specified branch
```

Example:
```bash
$ cat hello.txt
hello
hello2

$ git log --oneline
c3ba033 (HEAD -> main) hello2
2d2b069 hello

# Delete history up to (but not including) 2d2b069.
# This undoes the 'hello2' change by deleting history.
# It does NOT modify files.
$ git reset 2d2b069

# Show the deleted history:
$ git log --oneline
2d2b069 hello

# Show that changes (addition of "hello2") are retained:
$ cat hello.txt
hello
hello2

# --hard = delete history AND delete local changes
# --hard can wipe out selected parts of commit history.
# More dangerous than 'git checkout' or 'git revert':
$ git reset 2d2b069 --hard

# Show that file changes are also gone:
$ cat hello.txt
hello
```

## Resources
- https://git-scm.com/docs/git-reset
