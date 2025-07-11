# tag

`git-tag` - Create, list, delete or verify a tag object signed with GPG

Tags are used to create specific versions of a repository (ex: `v1.0`, `v2.0`, etc.). Tags are like branches which do not change.

## List tags
Tags are listed in alphabetical order (not the order they were created).
```bash
git tag
v1.0
v2.0
```

### `-l, --list`
Use the `-l` flag to query by name.
```bash
git tag -l 'v2*'
v2016.07.29.00
v2016.08.01.00
```

## Creating tags
Git supports two types of tags: lightweight and annotated.

Annotated tags are generally recommended because they contain additional metadata such as tagger name, email, and date. Lightweight tags are little more ethan a commit checksum stored in a file with no other information.

### Creating annotated tag
Use `-a, --annotate`. The `-m` flags allows specifying a message.

```bash
$ git tag -a v1.4 -m "my version 1.4"
$ git tag
v0.1
v1.3
v1.4
```

## Checking out tags
Checking out a tag puts your repository in a 'detached HEAD' state.

```bash
$ git checkout v2.0.0

# undo operation when done
$ git switch -
```

## Get date of a tag name
```bash
# tag name here is 1.0.401
$ git --no-pager log -1 --format=%ad --date=short 1.0.401
2025-05-16
```

- `--no-pager`: optional flag to prevent paging


## Resources
- https://git-scm.com/docs/git-tag
- https://git-scm.com/book/en/v2/Git-Basics-Tagging
