# revert

`git-revert` - Revert some existing commits

Revert adds a *new* commit which *undoes* a previous commit. Unlike `git checkout`, you can make additional changes after reverting.

## Example
```bash
# Assume hello.txt was created with "hello" then appended with "hello2":
$ cat hello.txt
hello
hello2

$ git log --oneline
39e07ac (HEAD -> main) hello2
22f3e1c hello

# Revert latest change to get back to "hello" state:
$ git revert 39e07ac
[main ac8e310] Revert "hello2"
 1 file changed, 1 deletion(-)

$ cat hello.txt
hello

$ git log --oneline
ac8e310 (HEAD -> main) Revert "hello2"
39e07ac hello2
22f3e1c hello
```

## Resources
- https://git-scm.com/docs/git-revert
