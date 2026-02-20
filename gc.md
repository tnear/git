# gc

`git-gc` - Cleanup unnecessary files and optimize the local repository

## Introduction
git garbage collection compresses file revisions, removes unreachable objects, and prunes unnecessary files. It helps reduce the size of the `.git` directory.

`git gc` is safe to run and will only remove data which cannot be reached. It should be run periodically when the `.git` directory has grown large.

```bash
$ git gc
Enumerating objects: 19670, done.
Counting objects: 100% (19670/19670), done.
Delta compression using up to 32 threads
Compressing objects: 100% (7401/7401), done.
Writing objects: 100% (19670/19670), done.
Total 19670 (delta 14022), reused 16867 (delta 11953), pack-reused 0
Enumerating cruft objects: 876, done.
Traversing cruft objects: 1280, done.
Counting objects: 100% (876/876), done.
Delta compression using up to 32 threads
Compressing objects: 100% (493/493), done.
Writing objects: 100% (876/876), done.
Total 876 (delta 505), reused 643 (delta 354), pack-reused 0
```

## Resources
- https://git-scm.com/docs/git-gc
