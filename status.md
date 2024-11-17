# status

`git-status` - Show the working tree status

## List differences you have made but not committed
```
$ git status
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   init.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        clone.txt
        status.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

## Common alias `gs`
A common alias for 'git status' is `gs`

```
$ alias gs='git status'
$ gs
```

## Short summary
Use the `-s, --short` flag to see a short summary:

```bash
$ git status -s
 M status.md
?? new_file.md
```

- ` M`: modified
- `??`: untracked file

## Resources
- https://git-scm.com/docs/git-status
