INIT

git-init - Create an empty Git repository or reinitialize an existing one
https://git-scm.com/docs/git-init

# Create an empty Git repository:
$ mkdir new_repository
$ cd new_repository
$ git init
Initialized empty Git repository in /tmp/work/.git/

$ ls -a
.git

# Create file and add to repository:
$ echo 'hello' > hello.txt
$ git add hello.txt

---