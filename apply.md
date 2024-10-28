# apply

`git-apply` - Apply a patch to files and/or to the index

## Share changes using patch files
Use `git diff` to share changes which have not been submitted. Then, use `git apply` to apply the patches. This is similar to shelving and unshelving in Perforce.

```
# if you have untracked files, they must be staged
$ git add .

# create patch file
$ git diff --staged > myChanges.patch
```

In another sandbox, apply the patch:
```
$ git apply myChanges.patch
```

## Resources
- https://git-scm.com/docs/git-apply
