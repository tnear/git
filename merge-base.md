# merge-base

`git-merge-base` - Find as good common ancestors as possible for a merge

See also: [`rebase`](rebase.md)

## Find branch point

This can be useful for squashing commits.
```bash
# syntax
git merge-base <branch_where_yours_diverged> HEAD

# example
git merge-base main HEAD
<checksum output>

# proceed with squashing using that checksum...
```

## Resources
- https://git-scm.com/docs/git-merge-base
