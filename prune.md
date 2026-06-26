# prune

`git-prune` - Prune all unreachable objects from the object database

See also: [`gc`](gc.md)

## Introduction
`git prune` removes unreachable Git objects from your local repository database. Typically, users should run `git gc` instead of `git prune`.

### Unreachable objects
Git stores commits, trees, blobs, and tags as objects. Normally, objects are reachable from refs like branches, tags, reflog. An object becomes *unreachable* when nothing points to it anymore.

For example:
```bash
$ git commit
$ git reset --hard HEAD~1
```

## Resources
https://git-scm.com/docs/git-prune
