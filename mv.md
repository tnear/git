# mv

`git-mv` - Move or rename a file, a directory, or a symlink
https://git-scm.com/docs/git-mv

## Rename file: file.txt to file_new.txt
```
$ git mv file.txt file_new.txt
# Status will show 'renamed' status:
$ git status
Changes to be committed:
        renamed:    file.txt -> file_new.txt
```

## Move file into sub-directory
```
$ mkdir newDirectory
$ git mv file.txt newDirectory
$ git status
Changes to be committed:
        renamed:    file.txt -> newDirectory/file.txt
```
