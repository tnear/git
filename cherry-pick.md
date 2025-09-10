# cherry-pick

`git-cherry-pick` - Apply the changes introduced by some existing commits

## Apply commit from one branch onto another branch

```bash
# Switch to target branch
git switch target-branch

# Apply a specific commit
git cherry-pick <commit-hash>

# Example
git switch main
# apply commit from another branch to main
git cherry-pick abc123def

# Cherry-pick multiple commits
git cherry-pick commit1 commit2 commit3
```

## Resources
- https://git-scm.com/docs/git-cherry-pick
