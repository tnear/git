# clean

`git-clean` - Remove untracked files from the working tree

## Dry run
Use the `-n, --dry-run` flag to see what git would remove:
```bash
$ git clean --dry-run
Would remove clean.md
Would remove ls-tree.md
Would remove restore.md
Would remove show.m
```

## Force delete
Use the `-f` flag to force delete untracked files. Be sure to use `--dry-run` first to preview what will be deleted.

## Resources
- https://git-scm.com/docs/git-clean
