# add

`git-add` - Add file contents to the index.

## -A = add all changed files
```bash
$ git add -A
```

## Add multiple files
```bash
$ git add file1.c file1.h file.out
```

## Add all .c files
```bash
$ git add *.c
```

## Differences between `-A`, `.` and `-u`
```bash
            New files   Modified  Deleted
git add -A      x          x         x
git add .       x          x
git add -u                 x
```

## Resources
- https://git-scm.com/docs/git-add
