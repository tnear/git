# ls-tree

`git-ls-tree` - List the contents of a tree object

## List all files
```bash
$ git ls-tree HEAD

100644 blob a40258339139515715734ed7b3a74d940bc8cfcb    README.md
100644 blob ae61fa170ac4ed85377cdc7b2d8ead4d837c67e9    add.md
100644 blob 201c8836c323c43e4662e2f67319ebc409692737    apply.md
100644 blob 0fb70bfc6eecacd4db1ed286e6f8c3b1fe825e0f    bisect.md
100644 blob c0eb91c4465cf7186b1b1c6ef38a1c72e92b0682    branch.md
...
```

### Show content of a file
Use `git show <commit_checksum>`.

```bash
$ git show a40258

# file contents here
```

## Resources
- https://git-scm.com/docs/git-ls-tree
