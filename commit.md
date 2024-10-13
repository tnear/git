COMMIT

git-commit - Record changes to the repository
https://git-scm.com/docs/git-commit

# -m, --message = commit with message:
$ commit -m "My changes"
[main ffc81de] My changes
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename file.txt => newDirectory/file.txt (100%)

# -a, --all = commit all
# note: new files are NOT affected by -a, only files which git already knows about
$ git commit -a -m "hello"
[main 08809da] hello
 1 file changed, 1 insertion(+)

---