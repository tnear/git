# worktree

`git-worktree` - Manage multiple working trees

`git worktree` allows managing multiple working directories ("worktrees") attached to a single Git repository.

## Setup

```bash
# list current worktrees
$ git worktree list

# Add existing path on disk as worktree.
# git worktree add <new_dir_path>

# Use existing branch user/hotfix
$ git worktree add ../hotfix user/hotfix

# Use -b to create a new branch
$ git worktree add ../hotfix -b user/hotfix

# Remove worktree when done
$ git worktree remove <path_to_worktree>

# prune if has been deleted (prefer 'worktree remove')
$ git worktree prune
```

## Advantages separate `git clone`
- Using `git switch` to switch to another branch already in the worktree errors. This prevents two directories with the same branch.
- Uses a single `.git` folder to save disk space

## Resources
- https://git-scm.com/docs/git-worktree
