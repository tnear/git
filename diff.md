# diff

`git-diff` - Show changes between commits, commit and working tree, etc

## Diff all unstaged files
```
$ git diff
diff --git a/file.txt b/file.txt
index ce01362..97531f3 100644
--- a/file.txt
+++ b/file.txt
@@ -1 +1,2 @@
 hello
+hello2
```

Annotated git diff output
```
a/file.txt:               version 'a' of file.txt (older)
b/file.txt:               version 'b' of file.txt (newer)
index ce01362..97 100644: metadata
--- a/file.txt:           version 'a' denoted by '-' symbol
+++ b/file.txt:           version 'b' denoted by '+' symbol
@@ -1:                    '-' = version a, 1 = num times it appears below
+1,2 @@:                  '+' = version b, 2 = 2 different lines, 1 = starting line number
```

## Diff one file
```bash
$ git diff <file_name>
```

## Diff staged files
By default, `git diff` does not diff stages files:
```bash
$ git add -A
$ git diff
<no output>
```

Diff staged files using '--cached':
```bash
$ git diff --cached
```

## Diff two different commits using `<checksum1>..<checksum2>`
```bash
# First, get history:
$ git log --oneline
475c427 Added line 2
64aa946 (myNewBranch) branch hello

# Then, diff the two checksums using '..':
$ git diff 475c427..64aa946
+hello
-main hello!
```

## Compact-summary
```bash
$ git diff --compact-summary
 hello.txt  | 1 +
 hello2.txt | 1 +
 2 files changed, 2 insertions(+)
```

## Show number of lines of code changed
Use the `--shortstat` flag.

```bash
# to include untracked files, add all files first
git add .

# use --cached to include untracked (new) files
git diff --shortstat --cached

 13 files changed, 403 insertions(+), 1 deletion(-)
```

## Diff a file with particular branch
```bash
# diff a file with main
git diff main -- path/to/file
```

## Resources
- https://git-scm.com/docs/git-diff
