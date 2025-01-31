# bisect

`git-bisect` - Use binary search to find the commit that introduced a bug.

## Workflow
### Start by showing history
```bash
$ git log --oneline
4cee47f (HEAD -> main) Merge branch 'feature-c'
7031fb6 (feature-c) Added branch line2
475c427 Added line 2
64aa946 (myNewBranch) branch hello
5323f9b hello
```

### Start bisect
```bash
$ git bisect start
```

### Tell bisect a known bad state. Assume latest (HEAD) is bad
```bash
$ git bisect bad HEAD
```

### Assume first submit (5323f9b) is a good state
```bash
$ git bisect good 5323f9b

Bisecting: 1 revision left to test after this (roughly 1 step)
[475c42743ddfde1cc7d305731fd638f25a835e02] Added line 2
```

### Bisection
```bash
# Bisect has now checked out a change for you to verify.
# Note how the top two entries from history are gone:
$ git log --oneline
475c427 (HEAD) Added line 2
64aa946 (myNewBranch) branch hello
5323f9b (refs/bisect/good-5323f9bb55afe5c82cf9a4a558ce25661721d030) hello

# If this is a bad state, let bisect know:
$ git bisect bad
Bisecting: 0 revisions left to test after this (roughly 0 steps)
[64aa9467e10745ea06a5b0f54eb44153d0fac046] branch hello

# Now only the last two commits remain. We already said 5323f9b is bad, so 64aa946 should be good:
$ git log --oneline
64aa946 (HEAD, myNewBranch) branch hello
5323f9b (refs/bisect/good-5323f9bb55afe5c82cf9a4a558ce25661721d030) hello

# Let bisect know this state is good:
$ git bisect good
475c42743ddfde1cc7d305731fd638f25a835e02 is the first bad commit
commit 475c42743ddfde1cc7d305731fd638f25a835e02

# When done, let bisect know using 'reset':
$ git bisect reset
```

## Resources
- https://git-scm.com/docs/git-bisect
