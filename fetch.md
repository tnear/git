# fetch

`git-fetch` - Download objects and refs from another repository

`git fetch` downloads all commits, files, and refs from a remote repository into your local repository. Fetch does not require you to merge any changes. It has no impact on your local work.

## Basic usage
```
$ git fetch
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 655 bytes | 218.00 KiB/s, done.
From https://github.com/tnear/git
   3d5e90b..edecaac  main       -> origin/main
```

## `-p, --prune origin`
This prunes (removes) anything which has been deleted, such as branches.

`origin` gets updates from the origin remote.

## Resources
- https://git-scm.com/docs/git-fetch
- https://www.atlassian.com/git/tutorials/syncing/git-fetch
