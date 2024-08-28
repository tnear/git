# config

git-config - Get and set repository or global options

## Set name and email
This is a required step for new installations of Git.

```
> git config --global user.email "see here: https://github.com/settings/emails"
> PS C:\repos\PowerShell> git config --global user.name "Your Name"
```

## Disable pager for `git branch`
By default, git uses a pager when listing branches. This config option changes that default.

```
git config --global pager.branch false
```

## Resources
- https://git-scm.com/docs/git-config
