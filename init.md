# init

`git-init` - Create an empty Git repository or reinitialize an existing one

## Create an empty Git repository
```bash
$ mkdir new_repository
$ cd new_repository
$ git init
Initialized empty Git repository in /tmp/work/.git/

$ ls -a
.git
```

## Create file and add to repository
```bash
$ echo 'hello' > hello.txt
$ git add hello.txt
```

## Resources
- https://git-scm.com/docs/git-init
