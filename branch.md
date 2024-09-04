BRANCH

git-branch - List, create, or delete branches
https://git-scm.com/docs/git-branch

# Show branches (no flags), '*' indicates current:
$ git branch
* main
  myNewBranch

# Create branch:
$ git branch myNewBranch

# Switch to branch:
$ git checkout myNewBranch

# -d = delete branch (-D forces)
# First, switch away from branch to be deleted (myNewBranch):
$ git checkout main
# Next: delete branch 'myNewBranch' using -d flag:
$ git branch -d myNewBranch
Deleted branch myNewBranch (was af242cb).

# -v, --verbose = verbose output
$ git branch -v

---