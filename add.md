# add

`git-add` - Add file contents to the index. https://git-scm.com/docs/git-add

## -A = add all changed files
```
$ git add -A
```

## Add multiple files
```
$ git add file1.c file1.h file.out
```

## Add all .c files
```
$ git add *.c
```

## Differences between `-A`, `.` and `-u`
```
            New files   Modified  Deleted
git add -A      x          x         x
git add .       x          x
git add -u                 x
```
