# show

`git-show` - Show various types of objects

## Show most recent changes
Use `git show` with no arguments:
```
git show
commit d84f426e458adad490d4786aee9adb7899bc1459 (HEAD -> main, origin/main, origin/HEAD)
Author: name <email>
Date:   Mon Nov 18 10:29:25 2024 -0600
    gitattributes
diff --git a/gitattributes.md b/gitattributes.md
new file mode 100644
index 0000000..58cbbb2
--- /dev/null
+++ b/gitattributes.md
@@ -0,0 +1,8 @@
```

## Show a particular commit
Use `git show <checksum>` or `git show HEAD~#` where `#` is the number of commits to go back.

```
$ git show ca6d6e7
$ git show HEAD~2 # show two commits before HEAD
```

## Resources
- https://git-scm.com/docs/git-show
