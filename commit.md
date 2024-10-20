# commit

`git-commit` - Record changes to the repository

## Commit with message
Use `-m, --message` to commit with message
```
$ commit -m 'My changes'
[main ffc81de] My changes
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename file.txt => newDirectory/file.txt (100%)
```

## Commit all
Use `-a, --all` to commit all. Note: new files are NOT affected by -a, only files which git already knows about
```
$ git commit -a -m 'hello'
[main 08809da] hello
 1 file changed, 1 insertion(+)
```

## Resources
- https://git-scm.com/docs/git-commit
